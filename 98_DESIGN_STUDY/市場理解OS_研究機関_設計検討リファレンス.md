# 市場理解OS 研究機関 設計検討リファレンス

**Document Role:** Design Study / Working Reference  
**Status:** WORKING REFERENCE / NOT CURRENT DESIGN / NOT CANONICAL  
**Purpose:** 正式な市場理解OS Architectureを作り直す前に、これまで議論してきた研究機関の思想・責任候補・接続候補・未決定事項を、人間とAIが後から再確認できる形で整理する。  
**Current Design Authority:** NONE  
**Adoption Status:** NOT ADOPTED

---

# 0. この文書の位置付け

この文書は正式Current Designではない。

ここに記載される、

- Market Foundation
- Proactive Research
- Reactive Research
- Dual-Entry / Single-Core Research
- Research Question
- Research Candidate
- Research Ledger
- Red Team / Independent Validation
- Market DNAの位置付け
- Cause Candidateの位置付け
- Hypothesisの位置付け
- Research Route / Mode / Method
- Research Result / Knowledgeとの境界

等は、今後の正式設計を考えるための設計検討材料である。

重要:

~~~text
この文書にある
≠ Current Design

Gitに保存された
≠ 採用済み

詳細に書かれている
≠ 正式Architecture

良い案
≠ 即採用
~~~

正式採用時は必ず、

~~~text
PROJECT_CHARTER
Current Architecture
Current Connection Map
Legacy Reference
他Domainとの責任境界
Authority
Source of Truth
Failure Path
~~~

を再確認する。

---

# 1. なぜ研究機関を再検討するのか

これまでの市場理解OSでは、Research側のうち特に、

- 異常
- 矛盾
- Unknown
- Cause Candidate
- Knowledge劣化
- Unexpected Loss
- Unexpected Profit
- Defense Block
- Missed Opportunity
- Execution Failure
- Post-Decision Finding

等が発生した後に、

~~~text
Research Candidate
↓
Research Intake
↓
Routing
↓
Research Plan
↓
Hypothesis
↓
Historical / OOS / Forward / Stress
↓
Refutation
↓
Failure Boundary
↓
Research Result
↓
Validation
~~~

へ進める診断・検証型Researchはかなり強くなっている。

一方で弱いのが、

> **まだ異常や失敗が起きていない平常時に、市場そのものへ疑問を持ち、能動的に探索して新しい理解を作るResearch**

である。

例:

~~~text
なぜBTC価格は動くのか？

OI増加の意味は市場状態で変わるのか？

Fundingは本当に何を表しているのか？

曜日・時間帯で参加者構造は変わるのか？

SpotとPerpのどちらがPrice Discoveryを主導するのか？

LiquidityとBreakout失敗率の関係は？

ETF FlowはどのLagで価格へ影響するのか？

BTCとNASDAQの関係はどのRegimeで強まるのか？
~~~

したがって今後は、

~~~text
異常・失敗が出た後の研究能力
+
異常がなくても市場を掘る探索能力
~~~

の両方を持つ研究機関を目指す。

---

# 2. 研究機関の中心思想

市場理解OSのResearch Instituteは、

> **市場について何が起き、なぜ起きる可能性があり、どの条件で再現し、どの条件で壊れ、どこまで分かっていて何がまだ分からないかを、反証可能・再現可能・追跡可能なResearch Assetへ変換する学習中枢**

として考える。

研究機関の目的は、

~~~text
最強Strategyを大量生産すること
~~~

ではない。

より重要なのは、

~~~text
何が分かっているか
どこで成立するか
なぜ成立する可能性があるか
どこで壊れるか
何を使ってはいけないか
何がまだ分からないか
~~~

の境界を年月とともに正確にすること。

---

# 3. 研究機関は Dual-Entry / Single-Core を基本候補とする

研究入口を大きく二つに分ける。

## 3.1 Proactive Research — 探索・発見型研究

問題が起きていなくても、市場そのものを能動的に研究する。

入口候補:

~~~text
Market Foundation
Current / Historical Data
Existing Knowledge
External Research
Open Discovery
Periodic Revalidation
Market Expansion Research
~~~

主な問い:

~~~text
何がある？
なぜ？
どんな関係がある？
このMarket Mechanismは本当に存在する？
どんな条件で変わる？
まだ見えていないPatternはある？
~~~

## 3.2 Reactive Research — 診断・検証型研究

市場理解OS内で異常・矛盾・失敗・未知等が見つかった時に研究する。

入口候補:

~~~text
Cause Candidate
Market Understanding Anomaly
Observation / Feature Contradiction
Unknown Market Structure
Existing Knowledge Contradiction
Applicability Contradiction
Unexpected Success
Unexpected Failure
Defense Block
Missed Opportunity
Execution Failure
Post-Decision Finding
~~~

主な問い:

~~~text
何が壊れた？
何が変わった？
なぜ想定と違った？
既存Knowledgeはまだ正しい？
Failure Boundaryを超えた？
別の原因がある？
~~~

## 3.3 入口の後は共通化する

探索型と診断型で研究Engineを二重化しない。

~~~text
Proactive Research ───┐
                      ▼
                Research Question
                      ↓
                Research Candidate
                      ↓
                 Research Intake
                      ↓
               Single Research Core
                      ↑
Reactive Research ────┘
~~~

重要:

~~~text
探索専用Hypothesis
探索専用Evidence
探索専用Knowledge

診断専用Hypothesis
診断専用Evidence
診断専用Knowledge
~~~

のような重複構造は作らない。

---

# 4. Research Foundation — 研究者の土台

Researchを、

~~~text
何も知らない
↓
Feature総当たり
~~~

から始めない。

研究者が最低限理解しているべき背景知識を、Research Foundationとして持たせる候補とする。

ただし、

~~~text
Research Foundation
≠ Production Knowledge
≠ 永久の真実
~~~

である。

Research Foundationは、

> **研究効率を高めるための教科書・背景モデル・Research Prior**

として扱う。

---

# 5. Crypto FirstにおけるMarket Foundation候補

当面はCrypto Spot / Crypto FXを対象にする。

## 5.1 Instrument Mechanics

~~~text
Spot
Perpetual
Futures
Options
Long / Short
Leverage
Margin
Funding
Open Interest
Liquidation
~~~

## 5.2 Market / Trading Mechanics

~~~text
Market Order
Limit Order
Orderbook
Spread
Liquidity
Slippage
Order Flow
Price Discovery
Basis
Arbitrage
~~~

## 5.3 Participant Model

~~~text
Retail
Whale
Market Maker
Arbitrageur
Leveraged Trader
Institution
ETF-related participant
Algorithmic Trader / BOT
~~~

## 5.4 Basic Economics / External Context

~~~text
Interest Rate
Inflation
USD
Global Liquidity
Risk On / Risk Off
Regulation
Macro Event
ETF Flow
~~~

## 5.5 Trading Archetype / Benchmark Knowledge

代表的な取引の型を、正解としてではなく比較対象として持つ候補。

~~~text
Buy & Hold
Trend Following
Pullback
Breakout
Mean Reversion
Momentum
Range
Funding / Basis
Event Driven
~~~

重要:

~~~text
Trading Archetype
≠ Production Rule
≠ 正解集
~~~

新しい複雑な研究結果が単純なBaselineより本当に価値があるかを比較するためにも利用する。

---

# 6. Foundationに確からしさの身分を持たせる候補

Foundation内の知識を全部同じ確度で扱わない。

概念候補:

~~~text
STRUCTURAL FACT
= 制度・仕様・仕組みとしてかなり明確

SUPPORTED MECHANISM
= 強い根拠を持つ市場メカニズム

WORKING MODEL
= 有力だが完全確定ではない説明

HEURISTIC
= 経験則

UNKNOWN
= 不明
~~~

例:

~~~text
PerpetualにはFunding構造がある
→ STRUCTURAL FACT寄り

Funding極端時は価格反転しやすい
→ FACTではなく研究対象候補
~~~

Foundation自身も必要ならResearch対象になる。

---

# 7. Market FoundationとResearch Knowledgeを分ける

Market Foundation:

> 市場を研究するための背景理解。

Research Knowledge:

> 市場理解OS自身が研究・検証して得た再利用可能な知識。

例:

~~~text
FundingはPerpetual市場に存在する
→ Foundation

High Funding
+
OI Expansion
+
Weak Spot Flow
+
Thin Liquidity
の条件で、
一定HorizonのDownside Riskが上がる
→ Research Knowledge候補
~~~

この二つを同じKnowledge Poolに機械的に混ぜない。

---

# 8. Research Questionを研究の共通入口にする候補

これまでResearch Candidateを入口としてきたが、その前に、

~~~text
Research Question
~~~

を置く案を重視する。

Research Question:

> **何を知りたいのか？**

Research Candidate:

> **その問いを今、正式研究へ進める価値があるか審査される対象。**

概念Flow:

~~~text
Observation / Finding / Foundation / Discovery
↓
Research Question
↓
Research Candidate
↓
Research Intake
~~~

---

# 9. Research Questionの種類候補

全部をCause Researchへ押し込まない。

~~~text
EXPLANATION
= なぜ起きる？

CAUSAL
= AがBを引き起こすと言える？

EMPIRICAL
= 条件付きで再現可能な関係がある？

STATE
= どんな市場状態か？

BOUNDARY
= どの条件で壊れる？

GENERALIZATION
= 別Regime / Asset / Venueでも成立する？

FAILURE
= なぜ失敗した？

REPLICATION
= 以前の研究は今も再現する？

DISCOVERY
= まだ説明できないPatternはある？
~~~

正式Taxonomyは後で決める。

---

# 10. Cause Candidateの位置付け候補

Cause Candidateを研究全体の共通入口にはしない。

Cause Candidate:

> **「なぜ？」を問うExplanation / Causal系Researchで使う原因候補。**

例:

~~~text
BTC急上昇
↓
なぜ？

ETF買い？
Short Cover？
新規Leveraged Long？
Liquidity Vacuum？
Macro Reaction？
~~~

重要:

~~~text
Cause Candidate
≠ Confirmed Cause
≠ Research Result
≠ Knowledge
≠ Trade Permission
~~~

---

# 11. Hypothesisの位置付け候補

Hypothesis:

> **検証・反証可能な形へ整理された研究上の主張。**

例:

~~~text
Spot buying supportが弱い状態で
OIとFundingが急増している上昇は、
一定条件でDownside Liquidation Riskが高まる。
~~~

概念的には、

~~~text
Causal Hypothesis
Empirical Hypothesis
Mechanism Hypothesis
Regime Hypothesis
Failure Hypothesis
~~~

等を区別できる余地を持つ。

ただしPython Objectを種類ごとに分割するかは後で決める。

重要:

~~~text
Hypothesis
≠ Evidence
≠ Result
≠ Knowledge
~~~

---

# 12. Market DNAの位置付け候補

Market DNAをBUY / SELL SignalやHypothesis判定器にしない。

研究機関から見るMarket DNAは、

> **市場状態を比較可能にする共通座標系・研究Instrument**

に近い。

## 12.1 Market DNA Definition

~~~text
何を軸として市場状態を表現するか
~~~

候補:

~~~text
Trend
Volatility
Liquidity
Leverage
Funding
Flow
Participant State
Macro
Session / Time
~~~

DefinitionそのものはResearch対象になり得る。

## 12.2 Market DNA Snapshot

~~~text
ある時点の市場を
固定されたDNA Definitionで表した状態
~~~

SnapshotはMarket Understanding側で作る候補。

Researchでは比較材料として使う。

ApplicabilityではCurrent Contextとして使う。

概念関係:

~~~text
Research
→ DNA Definitionを研究 / 改善候補

Market Understanding
→ DNA Snapshot生成

Research
← DNA SnapshotをCase比較に利用

Applicability
← DNA Snapshotを現在市場条件確認に利用
~~~

重要:

~~~text
DNA Similarity
≠ Hypothesis Support
≠ Applicability確定
≠ Trade Signal
~~~

---

# 13. Feature探索の位置付け

Feature CombinationをResearchそのものと同一視しない。

原則候補:

~~~text
Research Question
↓
何を測れば答えられる？
↓
Feature / Metric
~~~

一方、Open Discoveryでは、

~~~text
Feature / Pattern探索
↓
未知関係
↓
Research Question
~~~

も許容する。

重要:

~~~text
Feature Discovery
≠ Knowledge
≠ Edge確定
~~~

---

# 14. Open Discoveryを正式なResearch Capability候補とする

Open Discoveryは、

> **既存KnowledgeやMarket Foundationだけでは説明できないPattern・Anomaly・構造変化をData側から見つける能力。**

探索候補:

~~~text
Anomaly
Feature Interaction
Structural Break
Unexpected Relationship
Unknown Regime
Cross-Market Relation
Session Effect
Participant Shift
~~~

出力候補:

~~~text
Discovery Finding
↓
Research Question
~~~

Open Discoveryから直接Knowledgeへ昇格しない。

---

# 15. Research Routingを4軸で考える候補

研究種類を一つの分類へ潰さない。

~~~text
Research Domain
Research Intent
Research Mode
Research Method
~~~

を分ける。

例:

~~~text
Domain:
Market Microstructure

Intent:
Empirical Relationship

Mode:
Confirmatory

Method:
Historical + OOS + Regime Stability
~~~

---

# 16. Research Domain候補

「どこ・何の問題を研究しているか」。

候補:

~~~text
Data Quality
Feature / Formula
Market Intelligence
Market Structure
Causal
Market DNA
Applicability
Defense / Risk
Execution
Production Evaluation
Research Structure
~~~

正式Domain Registryは後で再設計する。

---

# 17. Research Intent候補

「何を知りたい研究なのか」。

~~~text
CAUSAL_EXPLANATION
EMPIRICAL_RELATIONSHIP
CASE_STRUCTURE_COMPARISON
GENERALIZATION_VALIDATION
FAILURE_DIAGNOSIS
CONTRADICTION_REFUTATION
BOUNDARY_ROBUSTNESS
ALTERNATIVE_EXPLANATION
MODEL_REALISM
APPLICABILITY_BOUNDARY
REPLICATION
DISCOVERY
~~~

正式Enumは後で決める。

---

# 18. Research Mode候補

Research Methodとは別軸。

## EXPLORATORY

何があるか自由に探す。

## CONFIRMATORY

事前にQuestion / Hypothesis / 評価方法等を固定して検証する。

## REPLICATION

別期間・別Venue・別Asset・別Regime等で再現性を確認する。

重要:

~~~text
発見
≠ 確認
≠ 再現
~~~

探索Dataを見た後で、その同じDataを「最初から決めていた検証」として扱わない。

---

# 19. Research Method候補

一つのResearch Questionに複数Methodを組み合わせられる。

候補:

~~~text
Causal Research
Empirical Research
Historical Validation
Case Comparison
Market DNA Comparison
OOS Validation
Forward Validation
Stress Test
Failure Analysis
Contradiction Analysis
Alternative Hypothesis
Regime Stability
Replication
~~~

重要:

~~~text
1 Question
≠ 1 Method固定
~~~

---

# 20. Research Planは共通Research Coreの中心候補

Research Planは、

> **研究Questionを再現可能な実験仕様へ変換するもの。**

含める候補:

~~~text
Research Question
Hypothesis / Claim
Research Mode
Research Method
Data
Feature / Formula
Comparison
Benchmark
Evidence Channel
Evaluation Rule
Refutation Rule
Alternative Hypothesis
Stress
Failure Criteria
Version
~~~

重要研究では、結果を見る前にPlanをFreezeする候補を持つ。

結果を見てMaterialな変更を行う場合は新Versionとして扱う。

---

# 21. Research Trial / Experiment

Research Planに基づきTrialを実行する。

候補:

~~~text
Historical
Replay
OOS
Forward
Paper / Demo
Shadow
Stress
Counterfactual
Production Evidence Review
Case Comparison
Market DNA Comparison
~~~

重要:

~~~text
Method
≠ Experiment Mode
≠ Evidence Channel
~~~

を維持する。

---

# 22. Evidenceの扱い

Evidenceを一つの総件数・総勝率へ潰さない。

最低限のChannel候補:

~~~text
Runtime / Observational
Historical
OOS
Forward
Stress
Production / Live
~~~

Evidence Role候補:

~~~text
Supporting
Contradicting
Discriminating
Conditioning
Boundary
Contextual
Process Validation
~~~

Evidence Outcome候補:

~~~text
Supportive
Contradicting
Neutral
Mixed
Inconclusive
Unknown
~~~

重要:

~~~text
Evidence Channel
≠ Evidence Role
≠ Evidence Outcome
~~~

---

# 23. Research Ledgerを横断機能候補とする

勝った研究だけ保存しない。

Research Ledgerは、

> **どんな探索・変更・試行を経てResearch Resultへ到達したかを残す研究履歴。**

記録候補:

~~~text
Research ID
Question
Candidate Origin
Data Seen
Features Tried
Hypotheses Tried
Plan Versions
Parameters Tried
Trials
Failed Trials
Rejected Results
Method Changes
Data Window Changes
Final Results
~~~

目的:

~~~text
1個試して成功
~~~

と、

~~~text
100000個試して一番良い1個だけ成功
~~~

を区別できること。

重要:

~~~text
Research Result
≠ Research History
~~~

Search History自体をResearch Integrityの一部として扱う。

---

# 24. Red Team / Independent Challenge候補

Hypothesisを作る責任と、Hypothesisを壊す責任を概念上分離する。

Red Team / Challengeが見る候補:

~~~text
Alternative Hypothesis
Confounder
Contradiction
Look-ahead
Leakage
Data Snooping
Selection Bias
Overfit
Shared Evidence
Common Cause
Regime Dependence
Cost
Slippage
Venue Dependence
Parameter Sensitivity
Timing
~~~

重要:

~~~text
研究者が自分で合格判定
~~~

だけに依存しない。

Python Moduleを必ず別にするという意味ではなく、Responsibility / Review Authorityを分ける候補。

---

# 25. Stress Researchの目的

Stressは、

~~~text
勝てるか
~~~

だけを見る場所ではない。

主目的:

> **どこからHypothesis / Edge / Knowledgeが壊れるかを能動的に探す。**

Stress候補:

~~~text
Extreme Volatility
Liquidity Collapse
Spread Expansion
Exchange Failure
Funding Extreme
OI Shock
ETF Flow Reversal
Macro Shock
Correlation Break
Data Delay
Missing Source
Participant Structure Change
~~~

出力候補:

~~~text
Failure Boundary
Constraint Candidate
Unknown
New Research Question
~~~

---

# 26. Research Synthesis

複数Evidenceを単純多数決しない。

例:

~~~text
Historical = Support
OOS = Weak
Forward = Support
Stress = Failure
~~~

を、

~~~text
3対1だからSUPPORTED
~~~

とはしない。

Synthesisで見る候補:

~~~text
Evidence Channel
Evidence Role
Independence / Dependency
Quality
Coverage
Contradiction
Failure Boundary
Regime
Alternative Explanation
Uncertainty
~~~

同じData・同じMarket Event・同じCauseから派生したEvidenceを独立件数として水増ししない。

---

# 27. Research Resultの結論は二値にしない

正式State名は後で決めるが、思想としては、

~~~text
Supported
Supported with Boundary
Weak Support
Regime Dependent
Mixed
Contradicted
Refuted
Inconclusive
Insufficient Evidence
Data Limited
Process Limited
Unknown
~~~

等を表現できる方がよい。

重要:

~~~text
Research Process Failure
≠ Hypothesis Refutation
~~~

を守る。

---

# 28. Negative Knowledgeを重要なResearch Assetとする

研究成功を、

~~~text
儲かるStrategyが見つかった
~~~

だけにしない。

Research Asset候補:

~~~text
Positive Result
Negative Result
Refutation
Failure Boundary
Constraint Candidate
Contradiction
Unknown
Empirical Edge
Causal Evidence
Mechanism Understanding
Revalidation Requirement
~~~

例:

~~~text
Funding単独にはDirectional Edgeが確認できなかった

このDNA条件ではBreakout Knowledgeを利用しない

この関係はOOSで消えた
~~~

も価値あるResearch Asset。

---

# 29. Knowledge Systemとの境界

Research Instituteの出口は、

~~~text
Validated Research Result
~~~

までとする方向を重視する。

その後は別責任として、

~~~text
Validated Research Result
↓
Knowledge Admission
↓
Knowledge Record / Knowledge Pool
~~~

へ進む。

重要:

~~~text
Research Result
≠ Knowledge

SUPPORTED
≠ Knowledge自動採用

Knowledge化
≠ Production利用許可
~~~

---

# 30. Applicabilityとの境界

Research:

> **どこで成立したか、どこで壊れたか、何が不明かを作る。**

Applicability:

> **その条件が今の市場に存在するかを確認する。**

概念:

~~~text
Research
= Where / Why / How it worked or failed

Applicability
= Does that condition exist now?
~~~

重要:

~~~text
Knowledge
≠ Applicable Knowledge
~~~

---

# 31. Decisionとの境界

Research InstituteはTrade ThesisやFinal Trade Decisionを直接作らない方向を重視する。

Research Output:

~~~text
Claim
Effect
Condition
Failure Boundary
Evidence
Uncertainty
~~~

まで。

Production Decision側が、

~~~text
Applicable Knowledge
+
Current Market Context
↓
Trade Thesis
↓
Expected Value
↓
Decision
~~~

を担当する。

重要:

~~~text
研究でEdge発見
≠ 今BUY / SELL
~~~

---

# 32. Risk / Defenseとの境界

Researchは、

~~~text
この条件でKnowledgeが壊れやすい
~~~

というFailure BoundaryやConstraint Candidateを作れる。

しかし、

~~~text
今このRiskを取ってよい
~~~

というRuntime Permissionは作らない。

重要:

~~~text
Research Constraint Candidate
≠ Runtime Authorized Constraint

Positive Expected Value
≠ Trade Permission
~~~

---

# 33. Executionとの関係

ExecutionはResearch Instituteの所属ではない。

Executionからは、

~~~text
Slippage
Partial Fill
Latency
Rejected Order
Venue Difference
Protection Failure
Execution Divergence
~~~

等がProduction Evaluation / Finding経由でResearchへ戻る。

~~~text
Execution
↓
Evaluation / Finding
↓
Research Question
~~~

を基本候補とし、ExecutionがResearch内部Methodを直接起動しない。

---

# 34. Post-Tradeより広いProduction Evaluation

研究対象は実際にTradeしたCaseだけではない。

~~~text
TRADE
NO_TRADE
WAIT
REDUCE
Defense BLOCK
Missed Opportunity
Unexpected Success
Unexpected Failure
~~~

等も後から評価できる必要がある。

概念候補:

~~~text
Decision Evaluation
Defense Evaluation
Execution Evaluation
Trade / Position Evaluation
Counterfactual
↓
Cross-Analysis
↓
Finding
↓
Research Question
~~~

つまり、Researchへの戻り口は単純なPost-Tradeだけではない。

---

# 35. External Researchを正式なResearch Source候補とする

外部論文・Exchange Documentation・GitHub・Regulatory Source・Quant Research等を参照できる。

ただし、

~~~text
External Research Claim
≠ Market Understanding OS Knowledge
~~~

とする。

概念:

~~~text
External Claim
↓
Replication / Research Question
↓
Local Research
↓
Validated Research Result
~~~

外部SourceをそのままProductionへ昇格させない。

---

# 36. AIの位置付け

独立したAI Layerを作るより、Research Institute全体へ横断配置する方向を重視する。

AI Role候補:

~~~text
Question Generator
Literature Researcher
Hypothesis Generator
Alternative Hypothesis Generator
Causal Critic
Experiment Design Assistant
Skeptic / Red Team
Research Reviewer
Human Explainer
~~~

重要:

~~~text
AI Suggestion
≠ Evidence

AI Judgment
≠ Validation Result

AI Approval
≠ Production Authority
~~~

AI停止時にもResearch / Production全体が完全停止しない構造を目指す。

---

# 37. Python / Rule / AIの分担候補

概念上:

~~~text
Python / Rule
= 測定
  計算
  Version固定
  Dataset分離
  Validation Rule
  Reproducible Test
  Trace
  Constraint Check

AI
= 解釈
  Question生成
  Hypothesis候補
  Alternative
  Confounder候補
  反証観点
  外部Research整理
  査読
  説明
~~~

Hard RuleやTraceをAI判断だけで無効化しない。

---

# 38. 研究機関を支える横断機能候補

研究責任群そのものとは分ける。

~~~text
AI Assistance
Research Ledger
Trace / Provenance
Versioning
Data Quality
Research Budget
Compute Budget
Security
Storage
Scheduling
Monitoring
Reproducibility
Research Governance
~~~

これらを研究Layerとして大量増殖させない。

---

# 39. 研究機関の責任群候補

細かい機能をそのままLayerへしない。

現段階では5つのResponsibility Groupへ圧縮する案を第一候補とする。

## 39.1 Research Foundation

~~~text
Market Foundation
Basic Economics
Market Mechanics
Trading Mechanics
Benchmark
External Research
~~~

## 39.2 Discovery & Question

~~~text
Proactive Discovery
Open Discovery
Reactive Finding
Cause Candidate
Knowledge Gap
Research Question
Research Candidate
~~~

## 39.3 Research Design & Experiment

~~~text
Research Intake
Routing
Hypothesis
Research Plan
Plan Validation
Trial
Historical
OOS
Forward
Stress
DNA / Case Comparison
~~~

## 39.4 Challenge & Validation

~~~text
Alternative Hypothesis
Confounder
Contradiction
Red Team
Leakage Check
Evidence Dependency
Research Synthesis
Result Validation
~~~

## 39.5 Research Output & Learning

~~~text
Validated Research Result
Positive Result
Negative Result
Failure Boundary
Constraint Candidate
Unknown
Revalidation Need
Knowledge Handoff
~~~

重要:

> これはPython Folder / Class構成ではない。

現段階ではResponsibility Group。

---

# 40. 他Domainとの責任境界候補

## External Data

Research InstituteはCollector / Adapter / Raw Data取得を所有しない。

受け取るのは研究可能なData / Observation / Evidence Context。

## Market Understanding

Current Market UnderstandingをResearch Instituteが毎回作り直さない。

Market Understandingは、

~~~text
Current Market Understanding
Cause Candidate
Anomaly
Unknown
Market DNA Snapshot
~~~

等をResearch Source / Contextとして渡せる。

## Knowledge

Research InstituteはValidated Research Resultまで。

Knowledge Admission / Maintenanceは別責任。

## Applicability

Researchが作った条件を、現在市場へ適用可能か確認する責任。

## Decision

Applicable KnowledgeをTrade Thesis / Decisionへ統合する責任。

## Risk / Defense

現在Riskを許可するかを判断する責任。

## Execution

許可されたRiskを実際の注文・Positionへ変換する責任。

## Production Evaluation

Decision / Risk / Execution / Trade / No-Trade等を後から評価し、FindingをResearchへ返す責任。

---

# 41. 全体Connection候補

~~~text
External Market / Sources
        ↓
Observation / Data Quality
        ↓
Current Market Understanding
        │
        ├─ Cause Candidate
        ├─ Anomaly
        ├─ Unknown
        └─ Market DNA Snapshot
        │
        │
        │     Market Foundation
        │     Existing Knowledge
        │     External Research
        │     Open Discovery
        │     Production Findings
        │              │
        └──────────────┼─────────────┐
                       ▼             │
                Research Question    │
                       ↓             │
                Research Candidate   │
                       ↓             │
                 Research Intake     │
                       ↓             │
                  Research Core      │
                       ↓             │
              Validated Research     │
                    Result            │
                       ↓             │
                Knowledge System     │
                       ↓             │
                  Applicability ←────┘
                       ↓
                    Decision
                       ↓
                 Risk / Defense
                       ↓
                   Execution
                       ↓
             Production Evaluation
                       ↓
                    Finding
                       └────────────→ Research Question
~~~

---

# 42. 現在のCurrent 01〜04との比較メモ

これはCurrent Designを変更する記述ではなく、将来比較するためのメモ。

## 01_EXTERNAL_DATA

現思想:

~~~text
External Source
→ Collector
→ Quality
→ Qualified Observation
~~~

は研究機関との境界上かなり相性が良い。

Research InstituteがRaw Data取得責任を奪わない。

## 02_MARKET_UNDERSTANDING

現思想:

~~~text
Observation
→ Market Intelligence
→ Current Market Understanding
→ Cause Candidate / Market DNA Snapshot
~~~

は有用。

将来比較するポイント:

~~~text
Cause Candidateだけでなく
Anomaly
Unknown
Research Question Trigger
Open Discovery Trigger
をどう扱うか
~~~

## 03_RESEARCH

後半の、

~~~text
Intake
Routing
Plan
Evidence
OOS
Forward
Stress
Refutation
Failure Boundary
Result
Validation
~~~

は強い。

追加検討候補:

~~~text
Research Foundation
Research Question
Proactive Research
Open Discovery
Research Mode
Research Ledger
Red Team
External Research
Benchmark
~~~

## 04_KNOWLEDGE_APPLICABILITY

以下の境界思想は強く残す価値が高い。

~~~text
Research Result
≠ Knowledge

Knowledge
≠ Applicable Knowledge

Applicable Knowledge
≠ Trade
~~~

---

# 43. 旧市場理解OSから再利用価値が高い研究思想

旧ReferenceはCurrent Authorityではないが、次の研究運用思想は再検討価値が高い。

~~~text
Research Intake
Domain / Method Routing
Research Plan
Plan Validation
Research Trial
Evidence Channel Separation
OOS
Forward
Stress
Alternative Hypothesis
Confounder
Research Process Failure separation
Research Synthesis
Evidence Dependency
Failure Boundary
Result Validation
Knowledge Admission boundary
~~~

特に、

~~~text
Research Process Failure
≠ Hypothesis Refutation

Evidence Count
≠ Independent Evidence Count

Method
≠ Evidence Channel
≠ Experiment Mode
~~~

は重要な教訓として残す。

---

# 44. 現段階の最重要Semantic Boundary候補

~~~text
Market Foundation
≠ Research Knowledge

Observation
≠ Interpretation

Interpretation
≠ Cause

Research Question
≠ Research Candidate

Candidate
≠ Hypothesis

Cause Candidate
≠ Confirmed Cause

Hypothesis
≠ Evidence

Evidence
≠ Research Result

Research Result
≠ Knowledge

Knowledge
≠ Applicable Knowledge

Applicable Knowledge
≠ Decision

Research Constraint Candidate
≠ Runtime Authorized Constraint

Research Result
≠ Production Permission

Market DNA
≠ Signal

Market DNA Similarity
≠ Applicability Proof

AI Judgment
≠ Evidence

WIN
≠ Hypothesis Correctness

LOSS
≠ Hypothesis Refutation
~~~

---

# 45. 現段階で決めないこと

このReferenceではまだ固定しない。

~~~text
正式Architecture Layer数
正式Directory
Python package構造
Python Class
DB Schema
Object ID
正式Enum / State
正式Research Domain一覧
正式Research Method一覧
Market DNA軸
Market DNA Formula
Feature Selection Formula
Hypothesis Score
Evidence Score
Applicability Score
Risk Threshold
Production Permission
Research Budget Formula
AI Prompt
External Provider
~~~

---

# 46. 今後の設計順序候補

このReferenceをそのままCurrent Architectureへ変換しない。

候補順:

~~~text
Step 1
Research Foundationを深掘り

Step 2
Research Question / Candidate / Intakeを深掘り

Step 3
Proactive / Reactiveの入口を深掘り

Step 4
Research Domain / Intent / Mode / Methodを整理

Step 5
Market DNA / Cause Candidate / Hypothesisの位置を確定

Step 6
Experiment / Evidence / Ledger / Red Teamを整理

Step 7
Synthesis / Validation / Outputを整理

Step 8
他Domainとの境界を再確認

Step 9
市場理解OS全体の大分類候補を白紙から作成

Step 10
新しい全体像とCurrent 01〜04を比較

Step 11
KEEP / REDESIGN / DROP / MERGEを判断

Step 12
正式Current Architectureを作り直す
~~~

---

# 47. 現時点の研究機関 一文定義候補

> **市場理解OSのResearch Instituteとは、Market Foundation・現在市場・既存Knowledge・Production結果・外部Research・未知Pattern等から研究すべきQuestionを継続的に生成し、探索型と診断型の二つの入口を一つの共通Research Coreへ統合し、因果・経験則・市場構造・Regime・Failure等を複数視点から検証・反証・Stress・Replicationし、成功だけでなく失敗・Unknown・成立条件・Failure Boundaryまで追跡可能なResearch Assetへ変換してKnowledge Systemへ渡す、市場理解OSの学習中枢である。**

---

# 48. このReferenceの扱い

この文書は今後、

~~~text
議論
↓
批判
↓
修正
↓
候補追加 / 削除
↓
責任境界確認
~~~

を続けてよい。

ただし正式Current Designへ移す場合は、

~~~text
このReferenceをコピー
~~~

ではなく、

~~~text
Current Charter確認
↓
Current Architecture確認
↓
Legacy Failure確認
↓
他Domain境界確認
↓
必要Conceptだけ正式採用
~~~

とする。

---

# 最終メモ

現時点で最も強い方向性は、

~~~text
Dual-Entry
=
Proactive Discovery
+
Reactive Diagnosis

Single-Core
=
共通Research Process

Research Foundation
=
研究者の教科書

Research Question
=
研究の共通意味入口

Research Ledger
=
探索履歴を失わない

Red Team
=
自分の仮説を壊す

Validated Research Result
=
Researchの出口

Knowledge / Applicability / Decision / Risk / Execution
=
Researchとは別責任
~~~

である。

この構造を正式設計へ昇格するかは、今後の深掘りと全体Architecture再設計で判断する。
