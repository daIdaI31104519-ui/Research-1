# CONNECTION — 01_EXTERNAL_DATA v0.1.1

**Document Role:** Partial Connection Map  
**Status:** REVIEWED / WORKING BASELINE  
**Parent:** `02_ARCHITECTURE/CONNECTION_MAP.md`  
**Purpose:** 外部世界の情報を市場理解OS内部へ安全に取り込み、次のMarket Understandingが利用できる `Qualified Market Observation Set` へ変換するまでの接続境界を定義する。

---

# 0. このMapの役割

`01_EXTERNAL_DATA` は、市場理解OS外部に存在する情報を取得し、内部で扱える最低限信頼可能なObservationへ変換し、次の `02_MARKET_UNDERSTANDING` へ渡すまでを担当する。

```text
外部世界
↓
取得
↓
Raw Observation
↓
Ingest Integrity
↓
Normalization
↓
Data Quality Evaluation
↓
Time / Freshness Evaluation
↓
Qualified Market Observation Set
↓
02_MARKET_UNDERSTANDING
```

このMap自身は、市場を解釈せず、原因を推測せず、Signalを作らず、Trade判断を行わず、Researchを直接実行しない。

---

# 1. Upstream Boundary

上流境界は `External Sources` とする。

主なSource候補:

```text
Market Price
Trades
Orderbook
Open Interest
Funding Rate
Liquidation
ETF Flow
On-chain
Whale Activity
News
Macro
SNS / Sentiment
Exchange Status
その他市場観測Source
```

この段階では具体的なProvider / API / Endpointは固定しない。

---

# 2. Downstream Boundary

下流境界は一つに統一する。

```text
Qualified Market Observation Set
```

次の `02_MARKET_UNDERSTANDING` は、この名称をUpstream Boundaryとして受け取る。

```text
01_EXTERNAL_DATA
Downstream Boundary:
Qualified Market Observation Set

↓

02_MARKET_UNDERSTANDING
Upstream Boundary:
Qualified Market Observation Set
```

---

# 3. 基本Connection Flow

```text
External Source
      │
      │ DATA
      ▼
Collector / Adapter
      │
      ▼
Raw Observation
      │
      ▼
Ingest Integrity Check
      │
      ▼
Normalization
      │
      ▼
Data Quality Evaluation
      │
      ▼
Time / Freshness Evaluation
      │
      ▼
Qualified Market Observation Set
      │
      ▼
02_MARKET_UNDERSTANDING
```

本流Connection Typeは原則 `DATA` とする。

---

# 4. External Sourceの責任境界

External Sourceは市場理解OSの管理外に存在する。

そのため、以下を前提とする。

```text
停止
遅延
欠損
仕様変更
Rate Limit
Timestamp異常
値の巻き戻り
誤配信
一部Dataのみ取得可能
```

市場理解OSは「外部Sourceだから正しい」と仮定しない。

取得できたDataは、そのまま信頼済み内部Dataにはならない。

---

# 5. Collector / Adapterの責任

Collector / Adapterは以下を担当する。

```text
外部Sourceへ接続
Data取得
取得時刻の記録
Source識別
取得失敗の記録
外部形式をRaw Observationとして内部へ搬入
```

また、Normalization以前に最低限の `Ingest Integrity` を確認する。

例:

```text
レスポンス自体が存在するか
壊れたPayloadではないか
必須構造が存在するか
Timestampを読み取れるか
想定外の形式変更がないか
```

Collector / Adapterは、市場解釈、Signal生成、因果推測、都合のよい異常値削除を行わない。

---

# 6. Raw Observation

外部Sourceから受け取った直後の記録を `Raw Observation` とする。

```text
Raw Observation
≠ Qualified Market Observation
```

Raw状態とQualified状態を概念上分ける。

Raw Dataの保存方式やRetention期間は、後のStorage / Retention設計で定義する。

---

# 7. Ingest Integrity

`Ingest Integrity` は「取得そのものが成立したか」を確認する責任である。

対象例:

```text
Malformed Response
Missing Required Structure
Unreadable Timestamp
Unexpected Payload Shape
Transport Corruption
```

ここで失敗したDataは、通常のNormalizationへ進めない。

重要:

```text
Ingest Integrity
≠ Data Quality Evaluation
```

前者は取得成立性、後者は取得できたObservationの利用品質を評価する。

---

# 8. Normalizationの責任

Normalizationは、Source固有形式を、意味を失わず内部で扱える標準的なObservation表現へ変換する。

対象例:

```text
名前
単位
Timestamp形式
Symbol
Direction
Numeric Format
Null表現
Event表現
```

重要:

> すべてのDataを一つの同一Schemaへ押し込むことを目的にしない。

将来、例えば以下のように異なるObservation型へ分かれる可能性を残す。

```text
Numeric Observation
Event Observation
Text Observation
State Observation
```

具体Schemaは後のData Contractで定義する。

---

# 9. Data Quality Evaluation

`01_EXTERNAL_DATA` が持つ局所責任は `Data Quality Evaluation` である。

最低限の評価候補:

```text
Missing
Malformed
Outlier
Duplicate
Inconsistent
Source Error
Timestamp Error
Partial
Stale
Unavailable
```

概念状態候補:

```text
VALID
DEGRADED
STALE
INVALID
UNAVAILABLE
```

このMapは「品質を評価する」ところまでを担当する。

---

# 10. Quality Propagation / Policyとの境界

品質低下を下流でどう扱うかはCross-Cutting責任とする。

```text
Data Quality Evaluation
= 01_EXTERNAL_DATA

Quality Propagation / Policy
= CROSS-CUTTING
```

例えば以下はこのMapでは最終決定しない。

```text
Market Intelligenceを停止するか
Productionを止めるか
Signalを弱めるか
AIへ警告するか
Research Candidate化するか
```

---

# 11. Time / Cycle / Freshness

市場Dataは値だけでなく時間的身分を持つ必要がある。

最低限追跡できる必要があるもの:

```text
Observation Time
Collection Time
Current Cycleとの関係
Freshness
```

概念状態候補:

```text
CURRENT
DELAYED
STALE
UNKNOWN
```

具体Timestamp Field、Cycle ID、Freshness Thresholdは後のContract / Cross-Cutting設計で決める。

---

# 12. Evidenceとしての身分

External Dataは `Measurement / Observation` として扱う。

```text
Measurement
≠ Interpretation
≠ Hypothesis
```

例:

```text
OI +20%
= Observation

Longが積み上がりすぎている
= Interpretation

Long Squeezeが起きる
= Hypothesis Candidate
```

`01_EXTERNAL_DATA` はObservationまでを担当する。

---

# 13. Failure Path

Failureを大きく二種類に分ける。

## 13.1 Source Availability Failure

```text
Timeout
Rate Limit
Provider Down
Connection Failure
Authentication / Access Failure
Source Unavailable
```

出力候補:

```text
Availability / Failure Record
```

## 13.2 Data Quality Failure

```text
Malformed
Invalid
Stale
Inconsistent
Partial
Duplicate
Timestamp Error
```

出力候補:

```text
DEGRADED
STALE
INVALID
```

重要:

> Sourceが取れないことと、Sourceは取れたが内容が悪いことを同一Failureとして扱わない。

また、Dataが取れない場合に古い値をCurrent Dataとして黙って使用しない。

---

# 14. Multi-Source

同一の市場事実を複数Sourceから取得できる構造を許容する。

```text
BTC Price
├─ Source A
├─ Source B
└─ Source C
```

ただし、この段階では以下を固定しない。

```text
Source Priority
Consensus Formula
Weighted Price
Fallback順序
Conflict Resolution
```

各Sourceを個別に取得・Normalize・Quality評価できる構造だけを持つ。

---

# 15. Dependency Strength

Connection Typeとは別に、Dependency Strengthを持てる構造を要求する。

候補:

```text
HARD
SOFT
OPTIONAL
ASYNC
```

例:

```text
Primary Price Data
→ Market Understanding
= HARD候補

SNS Sentiment
→ Market Understanding
= OPTIONAL候補
```

正式割当は後のSource Requirement設計で決める。

---

# 16. Connection Type

v0.1の有効方針を継承する。

```text
DATA
REFERENCE
FEEDBACK
GATE
ADVISORY
```

このMapの本流は主に `DATA`。

品質やAvailabilityが後続利用を制限する場合、将来的に `GATE` 的責任と接続する可能性を残す。

---

# 17. Researchへの接続境界

`01_EXTERNAL_DATA` からResearch本体へ直接接続しない。

異常・新規現象がResearch価値を持つ場合でも、概念的には以下を通す。

```text
External / Data Anomaly
↓
Research Candidate
↓
Research Intake / Router
```

Research側の正式接続は `03_RESEARCH` で設計する。

---

# 18. AIへの接続境界

Raw External DataからAIへ無制限に直接Authorityを与えない。

AIが参照する場合でも、基本は以下を伴う。

```text
Normalized / Qualified Observation
+
Source Context
+
Quality Context
+
Freshness Context
```

AI OutputをMeasurementそのものとして扱わない。

詳細はCross-Cutting AI設計で扱う。

---

# 19. Downstream Concept

`02_MARKET_UNDERSTANDING` へ渡す概念Boundaryを `Qualified Market Observation Set` とする。

含まれる情報候補:

```text
Observation
Source Identity
Observation Time
Collection Time
Quality State
Freshness State
Normalization Status
```

これは正式Object Schemaではない。
Field名、型、ID、DB構造はData Contractで決める。

---

# 20. Boundary Summary

```text
Upstream Boundary:
External Sources

Internal Entry Boundary:
Collector / Adapter

Downstream Boundary:
Qualified Market Observation Set

Next Map:
02_MARKET_UNDERSTANDING
```

---

# 21. このMapが保証すること

このMapがWorking Baselineとして成立するには、最低限以下が分かる必要がある。

```text
外部Sourceがどこから入るか
RawとQualifiedの違い
取得成立性とData Qualityの違い
Normalizationの責任
Quality EvaluationとQuality Policyの境界
Freshnessの必要性
Source FailureとData Quality Failureの違い
MeasurementとInterpretationの違い
Dependency Strengthを持てること
02_MARKET_UNDERSTANDINGへの出口
```

---

# 22. このMapで決めないこと

```text
具体的API Provider
API Key
Endpoint
Collector Class
DB Table
具体Field型
Retention期間
Freshness秒数
Outlier Threshold
Source Priority
Consensus Formula
Retry回数
Circuit Breaker詳細
Python Module
具体Alert方法
```

これらはDetailed Design / Contract / Implementation Specで決める。

---

# 23. v0.1 Failure Reviewとの対応

このMapで直接扱うMUST FIX:

```text
MUST FIX 05
Evidence Role / Source分離
→ ObservationをMeasurementとして明確化

MUST FIX 06
Data Quality EvaluationとQuality Propagation分離
→ 対応

MUST FIX 09
Dependency Strength
→ 概念導入

MUST FIX 10
Time / Cycle / Freshness
→ Data側必要条件を明示

MUST FIX 11
AI Outputの身分
→ Measurementとの境界を明示
```

---

# 24. Completion Gate

```text
□ Upstream Boundaryが明確
□ Downstream Boundaryが `Qualified Market Observation Set` に統一
□ Raw / Normalized / Qualifiedを区別
□ Ingest IntegrityとData Quality Evaluationを分離
□ 数値・Event・Text等を一つのSchemaへ無理に統一しない
□ Local Data Quality責任を定義
□ Cross-Cutting Qualityとの境界を定義
□ Freshnessの必要性を定義
□ Source Availability FailureとData Quality Failureを分離
□ MeasurementとInterpretationを分離
□ Dependency Strengthを保持可能
□ 02_MARKET_UNDERSTANDINGと接続可能
□ Detailed Designへ踏み込みすぎていない
```

---

# 一文定義

> **01_EXTERNAL_DATAとは、市場理解OS外部のMarket / News / Macro / On-chain等の情報を取得し、外部形式のまま信用せず、取得成立性・Normalization・Data Quality・Time / Freshnessの確認を通じて、次のMarket Understandingが利用できる `Qualified Market Observation Set` へ変換するまでの接続境界を定義するPartial Connection Mapである。**
