# CONNECTION — 02_MARKET_UNDERSTANDING v0.1.1

**Document Role:** Partial Connection Map  
**Status:** REVIEWED / WORKING BASELINE  
**Parent:** `02_ARCHITECTURE/CONNECTION_MAP.md`  
**Purpose:** `Qualified Market Observation Set` を受け取り、観測・派生測定・Context・Interpretationの身分を分離したまま「現在市場で何が起きているか」を整理し、Current Market Understanding・Cause Candidate・Market DNA Snapshotへ接続する境界を定義する。

---

# 0. このMapの役割

`02_MARKET_UNDERSTANDING` は、

> **市場観測をそのままTrade判断へ使うのではなく、複数のObservationを時間・品質・市場文脈の中で組み合わせ、「現在市場で何が起きているか」を理解可能な状態へ変換する領域**

である。

基本経路:

```text
01_EXTERNAL_DATA
↓
Qualified Market Observation Set
↓
Observation Context Assembly
↓
Derived Feature / Context Construction
↓
Market Intelligence
↓
Current Market Understanding
├─→ Cause Candidate
└─→ Market DNA Snapshot
```

このMap自身は、

```text
Hypothesisを立証しない
Researchを実行しない
Knowledgeを承認しない
Expected Valueを計算しない
BUY / SELLを決定しない
Risk Permissionを出さない
Executionを行わない
```

。

---

# 1. Upstream Boundary

Upstream Boundaryは、

```text
Qualified Market Observation Set
```

とする。

これは `01_EXTERNAL_DATA` のDownstream Boundaryと完全一致させる。

```text
01_EXTERNAL_DATA
Downstream:
Qualified Market Observation Set

↓

02_MARKET_UNDERSTANDING
Upstream:
Qualified Market Observation Set
```

入力には概念上、

```text
Observation
Source Context
Observation Time
Collection Time
Quality State
Freshness State
Normalization Context
```

等が含まれ得る。

具体Object Schemaはここでは固定しない。

重要:

> `Qualified` は「すべてVALID」という意味ではなく、品質・Freshness等の身分が評価され、下流がその状態を認識して扱えるObservationであることを意味する。

したがって、`DEGRADED` や `STALE` 等の状態を伴うObservationが境界を通る可能性を残す。

---

# 2. このMapで扱う問い

中心的な問いは、

> **「今、市場では何が起きているのか？」**

である。

以下とは区別する。

```text
何が観測された？
= Observation

どのような変化・関係が測定できる？
= Derived Feature / Context

今、市場では何が起きている？
= Market Understanding

なぜ起きている可能性がある？
= Cause Candidate

今後どうなる？
= Prediction / Hypothesis

Tradeすべきか？
= Decision
```

重要原則:

```text
Observation
≠ Derived Feature
≠ Interpretation
≠ Cause Candidate
≠ Hypothesis
≠ Signal
```

---

# 3. 基本Connection Flow

```text
Qualified Market Observation Set
              │
              │ DATA
              ▼
Observation Context Assembly
              │
              ▼
Derived Feature / Context Construction
              │
              ▼
Market Intelligence
              │
              ▼
Current Market Understanding
        ┌─────┴─────────────┐
        │                   │
        ▼                   ▼
Cause Candidate       Market DNA Snapshot
        │                   │
        │                   ├──→ 03_RESEARCH
        │                   │
        └──→ 03_RESEARCH    └──→ 04_KNOWLEDGE_APPLICABILITY
```

Cause CandidateをResearch Candidateへどう変換し、どのResearchへRoutingするかは `03_RESEARCH` の責任とする。

この図は概念Connectionであり、Python Module構造ではない。

---

# 4. Observation Context Assembly

01から受け取ったObservationを、単純にバラバラなDataとして扱わない。

Observation同士を、

```text
Asset
Market
Time
Cycle
Source
Quality
Freshness
Observation Type
```

などの文脈を失わず組み合わせられる状態にする。

目的:

> **異なるObservationを「同じ現在市場についての観測」として比較可能にする。**

例:

```text
BTC Price
OI
Funding
Liquidation
Spot CVD
ETF Flow
News Event
Macro Event
```

が同じ市場・同じ時間文脈に属するかを判断できる必要がある。

ただし、

```text
Observation Context Assembly
≠ Market Interpretation
```

である。

---

# 5. Derived Feature / Context Construction

Market Intelligenceへ入る前に、Observationから再現可能な派生測定・時間変化・関係量を作れる責任を持つ。

候補例:

```text
Return / Change Rate
Velocity
Acceleration
Spread
Divergence
Imbalance
Relative Change
Rolling Volatility
Flow Change
OI Change
Funding Change
Liquidation Pressure
Time-aligned Event Context
```

重要:

```text
Derived Feature
= Observationから再現可能な測定・変換

Interpretation
= その測定が市場で何を意味するかという意味付け
```

したがって、

```text
OI acceleration = +X
```

はDerived Featureになり得るが、

```text
Leverage crowding is dangerous
```

はInterpretation側である。

具体Feature一覧・計算式・Window・Thresholdは後のDetailed Designで定義する。

---

# 6. Market Intelligenceの責任

Market Intelligenceは、

> **複数のObservation・Derived Feature・Contextの関係を読み、単独Dataでは見えない現在市場の現象を整理する。**

例:

```text
Price ↑
OI ↑↑
Funding ↑
Spot CVD ↓
Liquidation ↑
```

というObservation / Featureから、

```text
Leverage participation増加
Spot buying supportは相対的に弱い可能性
Position crowdingが進んでいる可能性
値動きがLeverage主導である可能性
```

などを整理する。

重要:

```text
Measurement / Feature
↓
Market Intelligence
↓
Interpretation
```

であり、

```text
Interpretation
≠ Confirmed Cause
```

である。

---

# 7. Market Intelligenceで扱える観測視点

具体的な計算式やFeatureは後で決めるが、少なくとも以下の市場視点を統合可能にする。

```text
Price / Trend
Volume / Flow
Open Interest
Funding
Liquidation
Orderbook / Liquidity
Spot / Derivatives relationship
ETF Flow
Whale / Large Participant
On-chain
Volatility
News
Macro
SNS / Sentiment
Market Event / Exchange State
```

ここでは、各視点の詳細アルゴリズムではなく、複数視点を市場理解へ接続できる責任だけを定義する。

---

# 8. Current Market Understanding

Market Intelligenceの結果を、

> **現在市場について、今この時点でOSがどう理解しているか**

という状態へ整理する。

概念例:

```text
Trend:
上昇傾向

Leverage:
増加

Liquidity:
低下

Spot Participation:
弱い可能性

Volatility:
上昇

Market Structure:
Leverage-driven movementの可能性

Uncertainty:
Medium
```

ただし、ここでは正式Field・Score・Thresholdを定義しない。

---

# 9. Current Market Understandingは予測ではない

重要:

```text
Current Market Understanding
= 現在市場の説明 / Interpretation

Current Market Understanding
≠ Future Prediction
```

例えば、

```text
Leverageが増えている
```

は現在理解。

```text
だからBTCが下落する
```

は未来に関するHypothesis。

この境界を維持する。

---

# 10. UNKNOWN / Uncertaintyを許可する

市場理解OSは、Observationが存在するからといって必ず一つの結論を出さない。

Observation同士が、

```text
矛盾
不足
Quality低下
時間的不整合
Source disagreement
未知の市場状態
```

を含む場合、

```text
UNKNOWN
MIXED
UNCERTAIN
INSUFFICIENT
```

等の状態を将来表現できる必要がある。

重要原則:

> **理解できない市場を、無理にBullish / Bearishへ変換しない。**

具体State名は後で正式化する。

---

# 11. Quality / Freshnessの引き継ぎ

01でData Quality Evaluationは行われている。

02はその結果を無視してはいけない。

概念上、

```text
Observation
+
Quality Context
+
Freshness Context
↓
Derived Feature / Context
↓
Market Understanding
```

とする。

例えば、

```text
Price = VALID
OI = VALID
Orderbook = DEGRADED
ETF = STALE
```

なら、LiquidityやETFを強く根拠としたUnderstandingの信頼性は低下し得る。

ただし、

```text
どのQuality Stateなら停止するか
どのObservationを除外するか
どの程度Confidenceを下げるか
```

等の共通PolicyはCross-Cutting側で定義する。

---

# 12. Quality Responsibility Boundary

```text
01_EXTERNAL_DATA
= Data Quality Evaluation

CROSS-CUTTING
= Quality Propagation / Policy

02_MARKET_UNDERSTANDING
= Quality Contextを考慮したFeature / Understanding生成
```

02がData Qualityそのものを再判定する領域にならないようにする。

---

# 13. Time / Cycle / Freshness

異なる時刻のObservationを、同じ現在市場として無条件に混ぜない。

02では最低限、

```text
Observation Time
Current Cycleとの関係
Freshness State
Observation間の時間整合
Derived FeatureのWindow Context
```

を考慮できる必要がある。

例:

```text
Current Price
+
2時間前のOI
+
昨日のETF Flow
```

を、すべて同じ現在情報として扱わない。

具体Window、Cycle ID、Timestamp Contractは後の詳細設計で決める。

---

# 14. Cause Candidate

Current Market Understandingから、

> **「なぜこの状態が起きている可能性があるのか」**

をCause Candidateとして生成できる。

例:

```text
Price上昇
+
OI急増
+
Spot弱い

↓

Cause Candidate:
Short Covering?
New Leveraged Long?
Liquidity Vacuum?
ETF-related Flow?
Macro Reaction?
```

重要:

```text
Cause Candidate
≠ Confirmed Cause

Cause Candidate
≠ Production Knowledge

Cause Candidate
≠ Trade Permission
```

。

---

# 15. Cause CandidateのAuthority境界

Cause Candidateは研究対象候補である。

`02_MARKET_UNDERSTANDING` の責任はCause Candidateを出力するところまでとし、Research Candidateへの変換・優先順位付け・Intake・Routingは `03_RESEARCH` 側で行う。

概念接続:

```text
Cause Candidate
↓
03_RESEARCH
↓
Research Candidate / Intake / Router
```

`02_MARKET_UNDERSTANDING` からResearch内部を直接実行しない。

---

# 16. Market DNA Snapshot

このMapは、現在市場を過去市場やKnowledgeと比較できるRuntime状態表現へ接続する。

これを、

```text
Market DNA Snapshot
```

とする。

重要:

```text
Market DNA Snapshot
≠ BUY / SELL Signal

Market DNA Snapshot
≠ Hypothesis Evaluator

Market DNA Snapshot
≠ Expected Value

Market DNA Snapshot
≠ Future Prediction
```

。

---

# 17. Market DNA Snapshotの入力境界

Market DNA Snapshotを `Current Market Understanding` の文章的Interpretationだけから生成する設計にはしない。

概念的には、

```text
Qualified Observation
+
Derived Feature / Context
+
Current Market Understanding
+
Reliability Context
↓
Market DNA Snapshot
```

のように、測定・派生測定・Interpretationの身分を保持したまま比較可能な状態へ落とす。

これにより、Market DNAの客観的な状態軸までAI Interpretationだけに依存することを防ぐ。

将来、Causal Confidence等の研究由来情報をDNAへ含める場合も、それをRuntime必須入力とはせず、出所・Version・身分を区別する。

---

# 18. Market DNA Definitionとの分離

以下を区別する。

```text
Market DNA Definition
= Market DNAをどう計算・表現するかという定義

Market DNA Snapshot
= Definitionに基づき、特定時点で生成された現在市場状態
```

Researchが改善する対象と、Runtimeで利用するSnapshotを混同しない。

具体的なDNA軸・計算式・Version管理は後のDetailed Designで決める。

---

# 19. Market DNA Snapshotの分岐

Market DNA SnapshotはResearchだけを経由しない。

概念上、

```text
Market DNA Snapshot
├─→ 03_RESEARCH
└─→ 04_KNOWLEDGE_APPLICABILITY
```

へ分岐する。

理由:

```text
Research
= 現在市場を研究対象・過去Case比較等に利用

Knowledge / Applicability
= 現在市場でどの研究済みKnowledgeが利用可能か判断
```

Production側が現在Market DNAを利用するために、毎回Researchへ同期依存する構造にしない。

---

# 20. Evidence / Interpretationの身分

このMapでは身分を混ぜない。

```text
Qualified Observation
= Runtime / Observational Evidence候補

Derived Feature
= Observationから再現可能な派生測定

Current Market Understanding
= Interpretation / Context

Cause Candidate
= Research対象候補
```

したがって、Current Market UnderstandingをそのままResearch Evidenceとして扱わない。

Research Evidence、Production / Live Evidenceの正式定義は後続設計で分離する。

現在市場のObservationは既存KnowledgeのApplicability評価には利用できるが、現在そう見えたという理由だけで新しい未検証EdgeをProduction Knowledgeへ昇格させない。

---

# 21. AIの役割

AIはこの領域で補助的に利用可能。

候補:

```text
複数Observationの意味整理
News / Text Eventの解釈
観測間の関係候補
代替Interpretationの生成
Cause Candidateの提案
矛盾・不足の説明
人間向け説明
```

ただし、

```text
Measurement
≠ AI Interpretation
≠ AI Hypothesis Candidate
```

を守る。

AI Outputには概念上、

```text
ADVISORY
INTERPRETATION
CANDIDATE
```

等の身分を持たせられるようにする。

AIはCurrent Market UnderstandingやCauseを無制限に確定するAuthorityではない。

---

# 22. Rule / PythonとAIの関係

概念上、

```text
Python / Rule
= 測定・集計・Feature生成・再現可能な処理

AI
= 解釈・疑問・代替説明・Cause Candidate補助
```

とする。

Market UnderstandingはAIだけに依存しない。

AIが利用不能でも、OS全体が即停止する設計を前提にしない。

具体Fallbackは後で設計する。

---

# 23. Failure Path

正常理解だけでなく、理解できない場合も設計対象とする。

候補:

```text
Observation不足
Quality不足
Freshness不足
Observation contradiction
Source disagreement
Context mismatch
Feature calculation unavailable
Interpretation conflict
Unknown market structure
```

その場合、Current Market Understandingを `UNCERTAIN / UNKNOWN / INSUFFICIENT` 等として扱えるようにする。

---

# 24. Failure時にやってはいけないこと

以下を禁止方向とする。

```text
不足Dataを推測で埋める
古いDataをCurrent扱いする
矛盾したObservationを無視する
Feature欠損を都合よくゼロ扱いする
理解不能をBullish / Bearishへ強制変換する
AI解釈をMeasured Factへ昇格する
UNKNOWNだから直接Researchを実行する
Cause Candidateを即Productionへ渡す
```

---

# 25. Researchへの戻り口

以下のようなものはResearch価値を持つ可能性がある。

```text
新しい市場現象
既存理解と合わないObservation
新しいCause Candidate
Market DNAで表現できない状態
繰り返すInterpretation conflict
未知のRegime候補
```

しかし、

```text
02_MARKET_UNDERSTANDING
↓
Research直接実行
```

にはしない。

Cause Candidateや異常候補を `03_RESEARCH` へ渡し、Research Candidate化・Intake / Routerはそこで扱う。

---

# 26. Downstream Boundaries

02は一つの万能Outputへ潰さない。

最低限、以下を別の概念Boundaryとして持つ。

## Boundary A — Current Market Understanding

```text
現在市場で何が起きていると理解しているか
```

Runtime Contextとして後続が参照できる。

## Boundary B — Cause Candidate

```text
なぜその市場状態が起きている可能性があるか
```

`03_RESEARCH` へ渡す。

## Boundary C — Market DNA Snapshot

```text
現在市場を比較可能な状態として表したRuntime Snapshot
```

`03_RESEARCH` および `04_KNOWLEDGE_APPLICABILITY` へ渡す。

---

# 27. Connection Type

既存方針を維持する。

```text
DATA
REFERENCE
FEEDBACK
GATE
ADVISORY
```

主な候補:

```text
Qualified Observation
→ Observation Context Assembly
= DATA

Derived Feature / Context
→ Market Intelligence
= DATA

AI Interpretation
→ Market Intelligence
= ADVISORY

Quality / Freshness Policy
→ Market Understanding
= GATE / REFERENCE候補

Cause Candidate
→ 03_RESEARCH
= DATA

Market DNA Snapshot
→ 03_RESEARCH / 04_KNOWLEDGE_APPLICABILITY
= DATA / REFERENCE候補
```

隣接MapとのBoundary Checkで最終割当を確認する。

---

# 28. Dependency Strength

Connection Typeとは別に、

```text
HARD
SOFT
OPTIONAL
ASYNC
```

を持てる構造を維持する。

例候補:

```text
Primary Qualified Market Observation
→ Market Intelligence
= HARD候補

AI Interpretation
→ Market Intelligence
= OPTIONAL候補

Cause Candidate
→ Research
= ASYNC候補

Market DNA Snapshot
→ Research
= ASYNC候補
```

`04_KNOWLEDGE_APPLICABILITY` 側のRuntime依存強度は、04設計時に確定する。

---

# 29. このMapが保証すること

Working Baselineとして最低限、

```text
01_EXTERNAL_DATAと接続できる
QualifiedがVALIDのみを意味しないことが分かる
ObservationとDerived Featureを分離できる
FeatureとInterpretationを分離できる
UnderstandingとCause Candidateを分離できる
Cause CandidateとConfirmed Causeを分離できる
Market DNA SnapshotとSignalを分離できる
Market DNA DefinitionとSnapshotを分離できる
DNAがInterpretationだけに依存しない
Quality / Freshnessを引き継げる
UNKNOWN / Uncertaintyを許可できる
AI Interpretationの身分を区別できる
Researchへ直接依存しない
Runtime Market DNAがResearchを経由せずApplicabilityへ進める
```

ことを要求する。

---

# 30. このMapで決めないこと

この段階では以下を最終固定しない。

```text
Market Intelligence具体アルゴリズム
全Feature一覧
各Indicator計算式
Feature Window
Market DNA全軸
Market DNA Score
Cause Candidate生成詳細Rule
Cause Candidate Score
Confidence数式
Quality Threshold
Freshness Threshold
AI Prompt
AI Model
DB Schema
Object ID
Python Class
Python Function
API仕様
Research Protocol
Expected Value
Signal
Risk
Execution
```

これらはDetailed Design / Contract / Implementation Specへ送る。

---

# 31. v0.1 Failure Reviewとの対応

このMapで直接扱う主なMUST FIX:

```text
MUST FIX 01
Current Market DNA → Production側への経路
→ Market DNA SnapshotをResearch / Knowledge Applicabilityへ分岐

MUST FIX 05
Evidence Role / Source分離
→ Observation / Feature / Interpretation / Candidateの身分を分離

MUST FIX 07
Research Intake / Router
→ 02はCause Candidate出力まで。Research Candidate化・Intakeは03へ委譲

MUST FIX 09
Dependency Strength
→ HARD / SOFT / OPTIONAL / ASYNCを保持可能

MUST FIX 10
Time / Cycle / Freshness
→ Observation / Feature Contextで引き継ぐ

MUST FIX 11
AI Outputの身分
→ Measurement / Interpretation / Candidate分離

MUST FIX 13
Market DNA Definition / Snapshot
→ 明確に分離
```

---

# 32. Boundary Summary

```text
Upstream Boundary:
Qualified Market Observation Set

Internal Responsibilities:
Observation Context Assembly
Derived Feature / Context Construction
Market Intelligence
Current Market Understanding

Downstream Boundary A:
Current Market Understanding

Downstream Boundary B:
Cause Candidate

Downstream Boundary C:
Market DNA Snapshot

Next Maps:
03_RESEARCH
04_KNOWLEDGE_APPLICABILITY
```

---

# 33. Completion Gate

`02_MARKET_UNDERSTANDING` をWorking Baselineとする最低条件:

```text
□ Upstreamが Qualified Market Observation Set と一致
□ QualifiedがVALIDのみを意味しないと明確
□ ObservationとDerived Featureを分離
□ Derived FeatureとInterpretationを分離
□ Observation Context Assemblyの責任が明確
□ Market Intelligenceの責任が明確
□ Current Market Understandingを定義
□ Predictionとの境界を定義
□ Cause Candidateとの境界を定義
□ Cause Candidate ≠ Confirmed Cause
□ Research Candidate化は03へ委譲
□ Market DNA Snapshot ≠ Signal
□ Market DNA DefinitionとSnapshotを分離
□ DNAがInterpretationだけから生成されない
□ Market DNA SnapshotがResearch / Applicabilityへ分岐
□ Quality / Freshnessを引き継げる
□ UNKNOWN / Uncertaintyを許容
□ AI InterpretationがAuthorityにならない
□ Researchへ直接接続しない
□ Dependency Strengthを保持可能
□ Detailed Designへ踏み込みすぎていない
```

---

# 一文定義

> **02_MARKET_UNDERSTANDINGとは、`01_EXTERNAL_DATA` から受け取った `Qualified Market Observation Set` を、Quality・Freshness・時間・市場文脈を保持したままObservation → Derived Feature / Context → Market Intelligence → Current Market Understandingへ変換し、そこから研究対象となるCause Candidateと、測定・派生測定・Interpretationの身分を保った比較可能なMarket DNA Snapshotへ分岐させる市場理解Connection Mapである。**
