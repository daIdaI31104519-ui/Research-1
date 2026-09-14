# CONNECTION — 03_RESEARCH v0.1.1

**Document Role:** Partial Connection Map  
**Status:** REVIEWED / WORKING BASELINE  
**Parent:** `02_ARCHITECTURE/CONNECTION_MAP.md`  
**Purpose:** 市場理解OSの各領域で発生した研究価値のあるCandidate・異常・矛盾・失敗・未知状態を共通研究入口から受け取り、研究課題として整理・Routingし、Hypothesis化・検証・反証・Stress・Failure Boundary確認を通じて、次のKnowledge領域へ渡せる `Validated Research Result` を生成するまでの接続境界を定義する。

---

# 0. このMapの役割

`03_RESEARCH` は、

> **市場理解OSで発見された「これは本当に正しいのか？」「なぜ起きたのか？」「どこまで通用するのか？」という問題を、いきなりProductionへ使わず、正式な研究対象として受け取り、検証・反証して次のKnowledge領域へ渡す研究所**

である。

基本経路:

```text
Candidate / Finding
↓
Research Candidate
↓
Research Intake
↓
Routing / Prioritization
↓
Research Plan
↓
Research Question / Hypothesis
↓
Validation Channels
↓
Refutation / Alternative / Failure Boundary
↓
Research Result
↓
Validation Gate
↓
Validated Research Result
↓
04_KNOWLEDGE_APPLICABILITY
```

重要:

```text
Candidate
≠ Hypothesis
≠ Research Result
≠ Knowledge
≠ Production Authority
```

---

# 1. 中心的な問い

このMapが扱う中心的な問いは、

> **「この考え・現象・関係は、本当に再現可能で、どの条件で成立し、どこで壊れるのか？」**

である。

```text
02_MARKET_UNDERSTANDING
= 今、市場で何が起きている？

03_RESEARCH
= その理解・Cause・関係は本当に正しい？
  どこまで通用する？
  どこで壊れる？

04_KNOWLEDGE_APPLICABILITY
= 研究結果をKnowledgeとしてどう扱い、
  現在市場で利用可能か？
```

Productionとの責任も分ける。

```text
Research
= 真偽・再現性・条件・限界を研究する

Production
= 研究済みKnowledgeを現在市場へ適用する
```

---

# 2. Upstream Inputは二つの身分に分ける

03へ入る情報を、最低限以下に分ける。

```text
A. Research Candidate Source
B. Research Context / Reference
```

研究対象候補と、研究のための参照材料を混同しない。

---

# 3. Research Candidate Source

研究対象候補を発生させる主なSource:

```text
Cause Candidate
Market Understanding Anomaly
Observation / Feature Contradiction
Unknown Market Structure
Repeated Failure Pattern
Post-Decision Finding
Unexpected Success
Unexpected Failure
Defense / BLOCK Pattern
Missed Opportunity
Existing Knowledge Contradiction
AI Research Suggestion
新しい市場現象
```

これらは、

```text
Candidate Source
↓
Research Candidate
```

へ変換され得る。

ただし、

```text
発見された
≠
必ず研究する
```

である。

---

# 4. Research Context / Reference

研究時に参照するもの:

```text
Market DNA Snapshot
Qualified Observation
Derived Feature / Context
Current Market Understanding
Historical Market Data
Past Cases
Existing Knowledge
Existing Hypothesis
Previous Research Result
Failure Boundary
Constraint
Runtime / Observational Evidence
```

重要:

```text
Market DNA Snapshot
≠ Research Candidate
```

Market DNA Snapshotは、研究対象を比較・分類・条件付けするための市場状態Contextとして利用できる。

ただしMarket DNA上で未知状態・異常が検出された場合は、

```text
DNA Anomaly
↓
Research Candidate
```

を生成できる。

---

# 5. 共通研究入口

各ModuleがResearch内部の具体機能へ直接接続する設計にしない。

```text
Cause Candidate
Post-Decision Finding
Anomaly
Contradiction
Failure Pattern
AI Suggestion
        │
        ▼
Research Candidate
        │
        ▼
Research Intake
```

各領域は、

```text
Historical Test
OOS
Forward Validation
Stress Lab
Hypothesis Engine
```

等を直接起動しない。

---

# 6. Research Candidate

Research Candidateとは、

> **正式研究へ進める価値があるか評価される前段階の研究候補**

である。

例:

```text
OI急増
+
Spot Participation低下
の状態では、
Long-side liquidation riskが上昇するのではないか？
```

重要:

```text
Research Candidate
≠ Hypothesis確定
≠ Edge
≠ Knowledge
```

---

# 7. Research Candidateが追跡できるContext

具体Schemaは後で決めるが、概念上以下を追跡可能にする。

```text
何が発見されたか
どこから発生したか
なぜ研究価値があるのか
Asset / Market
Time / Cycle
関連Observation
関連Feature
関連Market Understanding
関連Cause Candidate
関連Market DNA Snapshot
Quality / Reliability Context
既存研究との関係
```

Field名・ID・DB構造はここでは固定しない。

---

# 8. Research Intake

Research Intakeは、研究所の共通受付である。

主な責任:

```text
Candidateの身分確認
最低限Context確認
重複研究確認
既存Hypothesisとの関係確認
研究可能性確認
Evidence不足確認
緊急度確認
Production影響確認
研究価値確認
```

将来の状態候補:

```text
ACCEPT
DEFER
MERGE
REJECT
NEED_MORE_CONTEXT
```

具体State名は後で正式化する。

---

# 9. Intakeで研究しない判断も正常

Candidateがすべて正式Researchへ進む必要はない。

例:

```text
既存研究と完全重複
Observation不足
Data Quality不足
再現不能
研究目的不明
単なるNoise
Hypothesisとして成立しない
```

この場合、`REJECT / DEFER / MERGE` 等になり得る。

> **研究しない判断もResearch Systemの正常な結果である。**

---

# 10. Routing / Prioritization

受付されたCandidateについて、

> **「何を、どの研究経路の組み合わせで調べるべきか」**

を整理する。

候補となる研究経路:

```text
Causal Research
Empirical Research
Historical Validation
Case Comparison
Market DNA Comparison
OOS Validation
Forward Validation
Stress Lab
Failure Analysis
Contradiction Analysis
Regime Stability Research
Alternative Hypothesis Research
```

重要:

> **Routerは必ず一つの研究方法だけを選ぶものではない。**

一つのResearch Candidateに対して、複数のValidation Channelを組み合わせた `Research Plan` を作れる構造を持つ。

Prioritizationでは概念上、

```text
Potential Impact
Novelty
Evidence Availability
Production Relevance
Risk Relevance
Repeated Occurrence
Contradiction Severity
Research Cost
Urgency
```

等を考慮可能にする。

具体Scoreや順位式は後で決める。

---

# 11. Research Plan

Routing結果を、研究実行可能な計画へ整理する。

Research Planは概念上、

```text
Research Question
必要なHypothesis
使用するEvidence Channel
比較対象
Validation方法
Refutation方法
Stressの必要性
Success / Failure判定に必要な条件
```

等を束ねる。

具体Object Schemaは後で定義する。

---

# 12. Research Question / Hypothesis

Research Candidateを、検証可能な問いへ変換する。

```text
Cause Candidate
↓
Research Candidate
↓
Research Question
↓
Hypothesis
```

Hypothesisは、

> **検証・反証可能な形へ整理された研究上の主張**

である。

```text
Hypothesis
≠ Confirmed Cause
≠ Knowledge
≠ Production Rule
```

現在市場に都合がよいようにHypothesis自体を書き換えない。
変更する場合は新Versionとして再Researchする。

---

# 13. Causal / Empiricalを両方許容する

ResearchはCausalだけに限定しない。

```text
Causal Research
= なぜ起きるか？
  Mechanismは？
  Temporal Orderは？
  Confounderは？
  Alternative Hypothesisは？

Empirical Research
= 原因説明が完全でなくても、
  条件付きで再現可能なEdgeが存在するか？
```

重要:

```text
因果説明が綺麗
≠ Profitability

因果説明が不完全
≠ Edge不存在
```

---

# 14. Evidence Channelを分離する

Research Evidenceを一つの総件数へ潰さない。

最低限、以下のChannelを区別可能にする。

```text
Runtime / Observational Evidence
Historical Evidence
OOS Evidence
Forward Evidence
Stress Evidence
Production / Live Evidence
```

これらは意味が異なる。

```text
Historical 100件
+
Forward 5件
+
Stress 20件
=
単純に125件の同質Evidence
```

とは扱わない。

Evidence Source / Role / Time / Versionを後から追跡できることを要求する。

---

# 15. Historical Validation

過去Dataを用いて、

```text
この現象は過去にも存在したか？
どれくらい再現したか？
どのMarket DNAで成立したか？
どの条件で失敗したか？
```

を見る。

```text
Historical success
≠ Future guarantee
```

---

# 16. Market DNA / Past Caseの利用

Researchでは、

```text
Current / Target Market DNA
↓
Past Market DNA / Past Cases
↓
Similarity / Difference
↓
Hypothesis behavior
```

を利用できる。

Market DNAの役割は市場状態比較であり、Hypothesis自動判定器ではない。

---

# 17. OOS Validation

研究で使用したDataと独立したData領域で、

> **研究時に見ていなかった市場でも成立するか**

を確認する。

具体Split方式は後で決める。

```text
In-Sample成功
≠ OOS成功
```

---

# 18. Forward Validation

研究後に新しく発生する市場でも挙動を確認できる経路を持つ。

Forward EvidenceをHistorical Evidenceと同じ身分へ潰さない。

---

# 19. Stress Lab

Hypothesis / Edgeについて、

> **どの条件で壊れるかを意図的に探す**

研究経路を持つ。

候補:

```text
Extreme Volatility
Liquidity Collapse
Exchange Failure
Black Swan-like Shock
Regime Shift
News Shock
Data Degradation
Adversarial Market Condition
```

目的はHypothesisを守ることではなく、Hypothesisを壊して限界を知ること。

---

# 20. Refutation / Alternative Hypothesis

ResearchはHypothesisを証明するだけの場所ではない。

最低限、

```text
反証Evidence
Contradiction
Alternative Hypothesis
Confounder
Temporal inconsistency
Regime failure
```

を探せる構造を持つ。

Hypothesisを正しいことにするためのResearchにしない。
Hypothesis数による多数決もしない。

---

# 21. Failure Boundary / Constraint

Research Resultには、

```text
どこで成立するか
```

だけでなく、

```text
どこから壊れるか
```

を持てるようにする。

Failure Boundary候補:

```text
Regime
Volatility
Liquidity
Leverage
Time Horizon
Market Session
Macro Condition
Data Quality
Event Condition
```

さらに、

```text
この条件では使ってはいけない
```

というConstraintもResearch成果として扱う。

具体Object設計は後で行う。

---

# 22. UNKNOWN / INCONCLUSIVEを許可する

Researchは `SUPPORTED / REFUTED` の二択ではない。

将来表現可能な結果候補:

```text
SUPPORTED
WEAK
REFUTED
INCONCLUSIVE
INSUFFICIENT EVIDENCE
CONTRADICTED
REGIME DEPENDENT
DATA LIMITED
UNKNOWN
```

具体Lifecycle Stateは後のDetailed Designで決める。

---

# 23. Research Result

Researchの出口候補を、まず `Research Result` とする。

概念上保持できるもの:

```text
何を研究したか
Research Question
Hypothesis
使用Evidence Channel
Validation結果
反証結果
Alternative Hypothesis
成立条件
Failure Boundary
Constraint
Uncertainty
Regime依存
再現性
未解決事項
Research Process Failure
```

成功だけでなく失敗・矛盾・UNKNOWNもResearch Resultになる。

---

# 24. Validation Gate

Research Resultを次のKnowledge領域へ渡す前に、研究結果として最低限追跡可能かを確認するGateを持つ。

確認対象候補:

```text
Research Questionが追跡できる
Hypothesis Versionが分かる
Evidence Source / Roleが分かる
Validation Channelが分かる
反証結果が残っている
Failure Boundary / Constraintがあれば残っている
Research Process FailureとHypothesis Refutationを区別できる
結果の再現・説明に必要なTraceがある
```

---

# 25. Validated Research Resultの意味

`Validated Research Result` の `Validated` は、

> **Hypothesisが正しいと証明された**

という意味ではない。

意味は、

> **Research Resultが定義された研究・検証・Trace要件を満たし、次のKnowledge領域で評価可能な形になっている**

ことである。

したがって、以下もValidなResearch Resultになり得る。

```text
REFUTED
INCONCLUSIVE
FAILURE BOUNDARY FOUND
REGIME DEPENDENT
INSUFFICIENT EVIDENCE
```

重要:

```text
Validated Research Result
≠ Supported Hypothesis
≠ Production Knowledge
≠ Current Market Applicable
```

---

# 26. Downstream Boundary

03の主要Downstream Boundaryを、

```text
Validated Research Result
```

とする。

```text
03_RESEARCH
↓
Validated Research Result
↓
04_KNOWLEDGE_APPLICABILITY
```

04側でKnowledge Promotion・Knowledge State・Version・Applicability等を扱う。

03自身がProduction Knowledgeへ直接昇格させない。

---

# 27. Productionへ直結しない

禁止方向:

```text
Research
↓
SUPPORTED
↓
Signal
```

```text
Research
↓
Production Rule Update
```

基本方向:

```text
Research
↓
Validated Research Result
↓
Knowledge Layer
↓
Applicability
↓
Decision
```

---

# 28. Post-Decisionとの戻り経路

将来06から、

```text
Trade Result
WAIT
NO TRADE
BLOCK
Unexpected Success
Unexpected Failure
Missed Opportunity
```

等のPost-Decision Findingが返る可能性がある。

03はそれを直接Knowledge Updateしない。

```text
Post-Decision Finding
↓
Research Candidate
↓
Research Intake
↓
Research
```

へ戻す。

```text
WIN
≠ Hypothesis証明

LOSS
≠ Hypothesis反証
```

---

# 29. AIの役割

AIは補助役として、

```text
Research Question候補
Hypothesis候補
Alternative Hypothesis
Confounder候補
反証観点
Stress Scenario候補
Research Result査読
矛盾検出
人間向け説明
```

等に利用できる。

ただし、

```text
AI Suggestion
≠ Research Evidence

AI Judgment
≠ Validation Result

AI Approval
≠ Production Authority
```

を守る。

---

# 30. Python / RuleとAIの役割

概念上、

```text
Python / Rule
= Data処理
  計算
  Backtest
  OOS
  統計
  再現可能な検証
  Stress実行

AI
= 仮説
  解釈
  反証案
  Alternative
  査読
  説明
```

とする。

AIだけでHypothesisをSUPPORTEDへ昇格させない。

---

# 31. Research Process Failure

Research自体も失敗する。

例:

```text
Data不足
Experiment failure
Computation failure
Evidence conflict
Invalid test design
Leakage
Look-ahead bias
Research timeout
External dependency failure
```

重要:

```text
Hypothesis Refuted
≠ Research Process Failure
```

研究プロセスが壊れて結論不能なのか、正しく研究した結果Hypothesisが反証されたのかを分ける。

---

# 32. Trace / Version

最低限、

```text
Candidate
↓
Research Intake
↓
Research Plan
↓
Research Question
↓
Hypothesis Version
↓
Experiment / Validation
↓
Evidence
↓
Result
```

を後から辿れる構造にする。

HypothesisやResearch Methodを変更する場合は、同じ研究を都合よく上書きせず、新Versionとして再Researchできる構造を前提とする。

具体ID / Trace Schemaは後で決める。

---

# 33. Connection Type

既存方針を維持する。

```text
DATA
REFERENCE
FEEDBACK
GATE
ADVISORY
```

例候補:

```text
Cause Candidate
→ Research Intake
= DATA

Market DNA Snapshot
→ Research
= REFERENCE

Post-Decision Finding
→ Research Candidate
= FEEDBACK

Validation Gate
→ Validated Research Result
= GATE

AI Review
→ Research
= ADVISORY
```

正式割当はMaster統合時に確認する。

---

# 34. Dependency Strength

Connection Typeとは別に、

```text
HARD
SOFT
OPTIONAL
ASYNC
```

を保持できる構造を維持する。

例候補:

```text
Research Candidate
→ Research Intake
= HARD

Market DNA Snapshot
→ 全Research
= SOFT / OPTIONAL候補

AI Review
→ Research
= OPTIONAL

Post-Decision Finding
→ Research
= ASYNC
```

ProductionがResearch完了待ちで毎回停止する構造にはしない。

---

# 35. Boundary Summary

## Research Candidate Source

```text
Cause Candidate
Post-Decision Finding
Anomaly
Contradiction
Failure Pattern
Unknown State
AI Research Suggestion
```

## Research Context / Reference

```text
Market DNA Snapshot
Qualified Observation
Derived Feature / Context
Current Market Understanding
Historical Data
Past Case
Existing Knowledge
Previous Research Result
```

## Internal Flow

```text
Research Candidate
↓
Research Intake
↓
Routing / Prioritization
↓
Research Plan
↓
Research Question / Hypothesis
↓
Validation Channels
↓
Refutation / Alternative
↓
Failure Boundary / Constraint
↓
Research Result
↓
Validation Gate
```

## Downstream Boundary

```text
Validated Research Result
```

Next Map:

```text
04_KNOWLEDGE_APPLICABILITY
```

---

# 36. このMapが保証すること

Working Baselineとして最低限、

```text
各領域がResearch内部へ直接依存しない
Research CandidateとContextを区別できる
Cause CandidateとHypothesisを区別できる
HypothesisとKnowledgeを区別できる
ResearchとProductionを分離できる
Causal / Empirical両方を扱える
複数Validation Channelを組み合わせられる
Historical / OOS / Forward / Stress / Live Evidenceを区別できる
反証とAlternativeを扱える
Failure Boundary / ConstraintをResearch成果にできる
UNKNOWN / INCONCLUSIVEを許容できる
AIがAuthorityにならない
Post-Decisionから直接Knowledge更新しない
Research Resultを即Productionへ送らない
Validated Research Resultの意味がHypothesis支持と混同されない
04へ接続できる
```

ことを要求する。

---

# 37. このMapで決めないこと

この段階では以下を最終固定しない。

```text
Research Candidate Schema
Hypothesis DB Schema
Research Priority Score
Evidence Score
Hypothesis Score
具体的統計手法
具体的Backtest方法
Train / Test Split
OOS期間
Forward期間
Stress Scenario詳細
StressResult Object
FailureBoundary Object
Constraint Object
Lifecycle詳細State
SUPPORTED判定Threshold
AI Prompt
AI Model
Python Class
DB Table
Experiment ID
Trace ID
Knowledge Promotion Rule
```

これらはDetailed Design / Contract / Implementation Specで扱う。

---

# 38. v0.1 Failure Reviewとの対応

このMapで直接扱う主要MUST FIX:

```text
MUST FIX 05
Evidence Role / Sourceを区別
→ Runtime / Historical / OOS / Forward / Stress / Liveを分離

MUST FIX 07
Research Intake / Routerを共通入口化
→ 対応

MUST FIX 08
Post-TradeからKnowledge直接更新禁止
→ Post-Decision → Research Candidateへ戻す

MUST FIX 09
Dependency Strength
→ 概念導入

MUST FIX 10
Time / Cycle / Freshness
→ Research Contextとして保持可能

MUST FIX 11
AI Outputの身分
→ ADVISORY / CANDIDATEとして扱う

MUST FIX 13
Market DNA Definition / Snapshot
→ SnapshotはResearch Context / Referenceとして利用
```

---

# 39. Completion Gate

```text
□ Research Candidate SourceとResearch Contextを分離
□ Cause Candidateを受け取れる
□ Market DNA SnapshotをReferenceとして利用できる
□ 共通Research Intakeがある
□ Routing / Prioritization責任が明確
□ Routerが単一Method選択器に限定されていない
□ Research Planを持てる
□ Candidate / Hypothesis / Result / Knowledgeを分離
□ Causal / Empirical両方を許容
□ Historical / OOS / Forward / Stress / Live Evidenceを区別
□ Refutation / Alternative Hypothesisを扱える
□ Failure Boundary / Constraintを出力できる
□ UNKNOWN / INCONCLUSIVEを許容
□ Post-Decisionから直接Knowledge更新しない
□ AIがResearch Authorityにならない
□ Validated Research Resultの意味が明確
□ Validated Research Resultを04へ渡せる
□ ResearchからProductionへ直結しない
□ Detailed Designへ踏み込みすぎていない
```

---

# 一文定義

> **03_RESEARCHとは、市場理解OSの各領域で発生したCause Candidate・異常・矛盾・失敗・未知状態等をResearch Candidateとして共通入口から受け取り、Market DNA・Observation・Past Case等をResearch Contextとして利用しながら、複数のValidation Channelを組み合わせたResearch Planの下でHypothesis化・検証・反証・Alternative Hypothesis・Failure Boundary・Constraint確認を行い、その結果をProductionへ直接渡さず、Knowledge領域で評価可能な `Validated Research Result` として `04_KNOWLEDGE_APPLICABILITY` へ渡す研究Connection Mapである。**