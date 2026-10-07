# 市場理解OS — PROJECT CHARTER v0.1

**Document Role:** Project Constitution / Top-Level Mission  
**Status:** DRAFT / LEADING CANDIDATE  
**Purpose:** 市場理解OSが何のために存在し、何を優先し、どの方向へ育てるかを定義する最上位方針文書。  
**Current Scope:** Section 1 `Project Mission`、Section 2 `Success Definition`、Section 3 `What Not To Maximize`、Section 4 `Survival / Profit Priority`、Section 5 `Research Mission`、Section 6 `Research Category Philosophy`、Section 7 `Capital / Risk Philosophy`、Section 8 `Knowledge / Data Asset Philosophy`、Section 9 `Extensibility / Replaceable Capability Philosophy`、Section 10 `Market Scope / Future Expansion Governance`、Section 11 `Research Results Usage Governance` を設計済み。Section 12以降は未設計であり、現時点では固定しない。

---

# 1. Project Mission

## 1.1 存在目的

市場理解OSは、一つのTrading Strategyを完成させ、それを永久に使い続けるためのシステムではない。

市場は、参加者、資金、Liquidity、Leverage、Regime、Macro、News、Regulation、Exchange環境、予測不能なEvent等によって継続的に変化する。

そのため市場理解OSは、

> **市場を継続的に観測・理解し、研究価値のある変化・未知・矛盾・失敗・利益機会を選択的に研究し、その成果を再利用可能なKnowledgeとResearch Assetとして蓄積しながら、市場変化へ適応し、長期的に正の期待値を持つ利益機会を追求するために存在する。**

---

## 1.2 Software完成後も研究は続く

市場理解OSでは、

```text
Software完成
≠
Research終了
```

とする。

Software完成は、長期研究の終了地点ではなく開始地点である。

市場理解OSが運用され続ける限り市場を観測し、

```text
新しい市場状態
未知
矛盾
Knowledgeの劣化
Failure
新しい利益機会
```

等を発見する。

ただし、発見された全てを無条件に研究するのではない。

Research価値を評価し、研究すべき対象を選択する。

基本循環は、

```text
Observation
↓
Understanding
↓
Research Candidate
↓
Research
↓
Validation / Refutation
↓
Research Result
↓
Knowledge
↓
Applicability
↓
Decision
↓
Risk
↓
Execution
↓
Post-Analysis
↓
Re-Research
```

とする。

---

## 1.3 市場変化への二種類の適応

市場理解OSは、市場変化への適応を大きく二つに分ける。

### Fast Adaptation

既に研究・検証されたKnowledgeの中から、現在市場で利用可能なものを選び直す。

```text
Current Market変化
↓
Knowledge Applicability再評価
↓
現在使えるKnowledgeへ適応
```

### Research Adaptation

既存Knowledgeでは十分に対応できない市場状態は、無理に既存Patternへ当てはめない。

```text
未知 / 矛盾 / Knowledge不足
↓
Research Candidate
↓
Research
↓
Validation / Refutation
↓
新しいKnowledge
```

として研究へ戻す。

> **迅速な市場適応と、未検証Knowledgeの即時Production利用を混同しない。**

---

## 1.4 Economic Missionと長期生存

市場理解OSは純粋な学術研究だけを目的としない。

Research・Knowledge・市場理解は、

> **正の期待値が確認された利益機会を実際の市場で選択的に利用するため**

にも使う。

利益獲得は市場理解OSのEconomic Objectiveである。

一方で、短期利益を追うことで資本・Research能力・Knowledgeの信頼性・System継続性を破壊してはならない。

したがって、

> **長期生存を維持しながら、ResearchとKnowledgeによって利益機会へ適応し続ける。**

ことを基本とする。

具体的なCapital Allocation、Drawdown、Risk Budget等は別項目で定義する。

---

## 1.5 Current Scope — Crypto First

当面の研究・Production対象は、

```text
仮想通貨FX
+
仮想通貨現物
```

とする。

現在はこの二つへResearch・Design・Implementation資源を集中させる。

まず仮想通貨市場において、

```text
Observation
→ Understanding
→ Research
→ Knowledge
→ Applicability
→ Decision
→ Risk
→ Trade
→ Post-Analysis
→ Re-Research
```

という市場理解OSの循環を成立・成熟させる。

株式、通常FX、その他金融市場は、現在の完成条件には含めない。

将来、市場理解OSが十分成熟し、新しい市場を追加する価値と余力が生じた場合に拡張を検討する。

基本方針は、

> **Crypto First. Future Expansion Ready.**

とする。

将来拡張の可能性は残すが、それを理由に現在のOSを不必要に複雑化しない。

---

## 1.6 Research NoteとResearch Asset

市場理解OSは、最終的なKnowledgeだけを残して研究過程を捨てない。

重要なResearchについては、

> **なぜ研究したのか、何を調べ、どのEvidenceを使い、何が支持・反証され、どの条件で成立・失敗したのかを、人間と将来のAIが再確認できるResearch Noteとして残す。**

Research NoteはKnowledgeそのものではない。

```text
Research Note
≠ Knowledge
≠ Production Rule
≠ Trade Permission
```

Research Note、Evidence、Graph、Research Result、Failure Boundary、Constraint、Knowledge、Decision / Trade Result等は、長期間再利用可能なResearch Assetとして扱う。

ただし、すべてのRaw Dataを永久保存することを意味しない。

将来の再検証・再現・説明に必要なEvidence、Context、Version、Historyを保持できることを重視する。

具体的なResearch Note Template、保存形式、DB Schema、Graph Formatは後続設計で定義する。

---

## 1.7 Research成果を人間にも還元する

市場理解OSのResearch Assetは、自動Tradingだけで利用するものに限定しない。

研究成果の一部を、

> **人間が理解・利用できる研究Data、Graph、Research Note、Market Intelligence等へ変換し、無料Application / Interface等を通じて利用可能にする方向を持つ。**

基本関係は、

```text
Research Core
├─→ Automated Trading
└─→ Human-readable Research Publication
```

とする。

Research PublicationのためにResearch Coreの結論を歪めてはならない。

無料Applicationの具体機能、UI、ユーザー獲得方法、事業モデル、収益化方法はProject Missionでは固定しない。

---

## 1.8 長期的に育てるもの

市場理解OSは、年月が経つほど単にTrade回数を増やすシステムではない。

長期間の運用によって、

```text
何が機能するのか
どの市場状態で機能するのか
なぜ機能する可能性があるのか
どこで壊れるのか
何を使ってはいけないのか
何がまだ分からないのか
```

を説明・再検証できるResearch Assetを増やす。

コード、AI Model、API、Data Source、Infrastructure、計算方法は将来変更され得る。

しかし、

> **市場から学んだ研究事実・Evidence・失敗・条件・Knowledge・判断履歴を失わず、次の市場変化へ再利用できる能力を育て続ける。**

ことを長期Missionとする。

---

# Project Mission — 一文定義

> **市場理解OSは、当面は仮想通貨FXと仮想通貨現物へ集中し、市場を継続的に観測・理解して研究価値のある変化・未知・失敗・利益機会を選択的に研究し、Research Note・Evidence・Knowledge等の再利用可能なResearch Assetを蓄積しながら、市場変化へ適応し、長期生存を維持して正の期待値を持つ利益機会を追求するとともに、その研究成果を人間にも利用可能な形で還元し続ける市場研究・意思決定基盤である。**

---

# 2. Success Definition

## 2.1 Successの中心思想

市場理解OSにおけるSuccessは、特定の利益額、勝率、研究数、予測精度等へ到達することだけでは定義しない。

市場は変化するため、現在成功している方法・Knowledge・Edge・判断基準が、将来も同じように成功を生む保証はない。

したがって市場理解OSでは、

> **資本・Research Asset・意思決定能力を成長させながら、そのSuccess状態と成立条件を継続的に再検証し、市場変化へ適応する循環を止めない状態**

をSuccessの中心思想とする。

簡潔には、

> **稼ぐ。学ぶ。疑う。適応する。そして止めない。**

と表現する。

ここで「疑う」とは、EvidenceのあるKnowledgeを無条件に捨てることではない。

> **Knowledgeを信用する。しかし永久には信用しない。**

という意味である。

---

## 2.2 Successは到達地点ではなく維持される循環である

市場理解OSでは、

```text
Success
≠
完成地点
```

とする。

例えば、

```text
利益が増えた
Researchが増えた
Decision精度が改善した
```

としても、それだけで市場理解OSが完成したとは考えない。

むしろ、

```text
利益 / 結果が出る
↓
なぜその結果になったか検証する
↓
Knowledge / Edgeの成立条件を確認する
↓
Failure / Contradiction / Unknownを確認する
↓
市場構造の変化を確認する
↓
必要なら再Researchする
↓
Knowledgeを更新・非適用・Retire候補へ送る
↓
新しいDecisionへ利用する
↓
再び結果を検証する
```

という循環を維持できることをSuccessとする。

> **成功している時にも検証を止めないこと自体がSuccessの一部である。**

---

## 2.3 Success Loop

市場理解OSのSuccessは、概念上次のLoopとして維持する。

```text
Market Observation
↓
Market Understanding
↓
Research
↓
Knowledge
↓
Applicability
↓
Decision
↓
Risk Control
↓
Execution / No Action
↓
Economic / Decision Result
↓
Post-Analysis
↓
Research Asset蓄積
↓
既存Knowledge / Edge / Success状態を再検証
↓
必要なら再Research
↓
市場変化へ適応
↓
再びMarket Observation
```

一時的なProfitが大きくても、

```text
Research停止
Knowledge固定
Failure無視
市場変化無視
```

となった場合は、Success状態が劣化していると考える。

---

## 2.4 Successを支える3つの成長

市場理解OSでは、長期的に少なくとも以下の3つが成長していることを重視する。

### A. Economic Capability

Research・Knowledge・Decisionを利用し、Cost・Fee・Slippage・Risk等を考慮した上で、適切な期間において正の期待値を持つ利益機会へ接続できる能力を育てる。

これは、毎日・毎月必ず資本残高が増え続けることを意味しない。

短期ProfitだけでEconomic Successを判定しない。

### B. Research Asset Capability

市場理解OSが運用されるほど、

```text
Research Note
Evidence
Research Result
Refutation
Failure
Failure Boundary
Constraint
Knowledge
Unknown
Decision History
Post-Analysis
```

等の再利用可能なResearch Assetが増え、次の市場理解・研究・再検証へ利用できる状態を育てる。

単なるData量の増加をSuccessとはしない。

### C. Decision Capability

市場理解OSは年月が経つほど、

```text
TRADEすべき時
WAITすべき時
REDUCEすべき時
NO TRADEすべき時
UNKNOWNとしてResearchへ戻す時
```

をより適切に区別できる能力を育てる。

Resultだけで過去Decisionを正当化せず、その時点で利用可能だったEvidence・Knowledge・Risk・UncertaintyからDecisionを後から検証できることを重視する。

---

## 2.5 成功したKnowledgeも再検証する

市場理解OSは、過去に利益を生んだKnowledgeを永久の正解として扱わない。

Evidenceが維持されているKnowledgeは利用する。

ただし継続的に、

```text
成立条件は維持されているか？
Edgeは弱くなっていないか？
Market Regimeは変化していないか？
参加者構造は変化していないか？
新しいFailureは発生していないか？
LossはVarianceか、Knowledge Decayか？
```

を確認する。

重大なContradiction・Edge Decay・Failure・未知状態等が確認された場合は、必要に応じてResearchへ戻す。

---

## 2.6 疑うことと不安定に変更し続けることを混同しない

継続的な再検証は、

```text
すべてを信用しない
毎回Strategyを変更する
過去Researchを無視する
```

という意味ではない。

基本方向は、

```text
Evidenceが維持されている
↓
Knowledgeを利用する

Evidenceが弱まる / 条件が変わる
↓
Applicabilityを再評価する

重大な矛盾・未知・Failureが発生する
↓
Researchへ戻す
```

とする。

目的は頻繁に変えることではなく、

> **Evidenceに基づいて安定性と適応性を両立すること**

である。

---

## 2.7 Success状態と評価基準も再検証可能とする

市場理解OSでは、現在使っているOperationalなSuccess Metricや評価方法も、長期Observation・Research・System成熟度に応じて再検証可能とする。

例:

```text
Profit評価期間
Expected Value評価方法
Risk評価方法
Edge評価方法
Knowledge利用基準
Research再現性の評価
Adaptationの評価
```

ただし、

```text
結果が悪くなった
↓
都合よくSuccess基準を変更する
```

ことは禁止する。

Success Metricや評価方法を変更する場合は、Evidence・Research Result・明確な変更理由・履歴を必要とする。

また、これは `PROJECT_CHARTER` 自身を自動的・継続的に書き換えるという意味ではない。

Charter本文の変更は、後続の `Charter Change Governance` に従って明示的に行う。

---

## 2.8 Core SuccessとSecondary Successを分ける

市場理解OS本体のCore Successでは、少なくとも、

```text
Economic Valueへ接続できる
Research Assetを蓄積・再利用できる
Decision能力を改善・検証できる
既存Knowledgeを再検証できる
未知市場をResearchへ戻せる
Production結果を再Researchへ戻せる
市場変化へ適応できる
この循環を長期間維持できる
```

ことを重視する。

これらを一つの万能Scoreへ潰し、一つの強い成果で重大なFailureを相殺しない。

一方、以下は市場理解OSの価値を拡張するSecondary Successとする。

```text
Human-readable Research Publication
無料Application / Interface
User Growth
External Trust
Business Opportunity
他市場へのExpansion
```

Secondary Successは重要だが、Core OSが成立するための絶対条件ではない。

またSecondary SuccessのためにResearch Integrity・Risk Control・長期生存を犠牲にしてはならない。

最大化禁止事項はSection 3、SurvivalとProfitの優先順位はSection 4で定義する。Business / Publicationの詳細は後続Sectionで定義する。

---

## 2.9 Current ScopeにおけるSuccess

現在のCore Success判定対象は、

```text
仮想通貨FX
+
仮想通貨現物
```

とする。

株式、通常FX、その他市場への対応は現在のCore Success成立条件ではない。

現在はCrypto市場において、Research → Knowledge → Applicability → Decision → Risk → Result → Re-Researchの循環を成立・成熟させることを優先する。

---

## 2.10 Failureを単純なLossと同一視しない

市場理解OSにとって、

```text
Loss
≠
Project Failure
```

である。

例えば、

```text
Loss
↓
正しく記録
↓
原因分析
↓
Failure Boundary発見
↓
Knowledge改善
```

であれば、LossはResearch Assetへ変換され得る。

一方、

```text
Profit
↓
理由不明
↓
再現不能
↓
記録なし
↓
過信
```

であれば、Profitが出ても市場理解OSとして健全なSuccessとは言えない。

市場理解OSにとって重大なFailureは、Lossそのものより、

```text
学ばない
記録しない
再検証しない
Evidenceを無視する
同じFailureを理由なく繰り返す
市場変化へ適応しない
```

状態が継続することである。

---

# Success Definition — 一文定義

> **市場理解OSのSuccessとは、資本・Research Asset・意思決定能力を成長させながら、過去に成功したKnowledgeやEdgeを固定された正解とせず、その成立条件とSuccess状態を継続的に再検証し、未知・変化・失敗を必要に応じてResearchへ戻し、市場変化へ適応する循環を長期間止めないことである。**

---


# 3. What Not To Maximize

## 3.1 このSectionの目的

市場理解OSは利益を追求する。

しかし、

> **測りやすい一つの数字を最大化することと、市場理解OS全体を良くすることを同一視しない。**

市場理解OSには、

~~~text
Profit
Expected Value
Win Rate
Prediction Accuracy
Trade Count
Research Count
Data Amount
Backtest Result
Model Score
User Growth
~~~

等、多数のMetricが存在し得る。

これらは評価・比較・監視・改善の材料として利用してよい。

しかし、

~~~text
一つのMetricが良くなる
=
市場理解OS全体が良くなる
~~~

とはしない。

---

## 3.2 「最大化しない」≠「重要ではない」

~~~text
Not To Maximize
!= Not To Measure
!= Not To Improve
!= Not Important
~~~

とする。

例えば、

~~~text
Profitを単独最大化しない
~~~

とは、Profitを軽視するという意味ではない。

同様に、

~~~text
Win Rateを単独最大化しない
~~~

とは、勝率を観測しないという意味ではない。

意味は、

> **単一Metricを、それ以外の重要な条件・Mission・Research Integrity・Knowledge Integrity・Risk・長期生存を破壊してまで最大化しない。**

ことである。

---

## 3.3 Short-Term Profitを単独最大化しない

利益獲得は市場理解OSのEconomic Objectiveである。

ただし、

~~~text
短期Profit最大化
↓
過大Leverage
過大Exposure
Failure Boundary無視
Unknown無視
未検証KnowledgeのProduction利用
~~~

となる設計は、市場理解OSのMissionと両立しない。

したがって、

> **Short-Term Profitだけを最上位Objectiveとして最大化しない。**

Profitを評価するときは、

~~~text
どのように作られた利益か
どのRiskを負ったか
Costを考慮したか
再現可能か
成立条件は何か
どこで壊れるか
~~~

を合わせて確認する。

高Profitそれ自体を悪いものとは扱わない。

---

## 3.4 Win Rateを最大化しない

高Win Rateは有用なMetricになり得る。

しかし、

~~~text
高Win Rate
+
稀な巨大Loss
~~~

のような構造も存在する。

したがって、

> **Win Rateそれ自体をSuccess条件として最大化しない。**

勝率を見る場合も、

~~~text
Expected Value
Loss Size
Tail Risk
Cost
Failure Boundary
Long-Term Survival
~~~

等と分離せず確認する。

具体的なRisk優先順位・Risk Budget・Leverage Limitは後続Sectionで定義する。

---

## 3.5 Prediction Accuracyを最大化しない

市場理解OSは、

~~~text
未来を最も多く当てる機械
~~~

を最終目的としない。

Prediction Accuracyが高くても、

~~~text
判断理由不明
Risk不明
Cost未考慮
Failure条件不明
市場変化時の適応不能
~~~

であれば、市場理解OSとして十分ではない。

逆にPredictionが外れても、その時点で利用可能だったEvidence・Knowledge・Unknown・Riskから合理的なDecisionであった可能性がある。

したがって、

> **Prediction AccuracyをMarket UnderstandingやDecision Qualityの代替Metricとして最大化しない。**

---

## 3.6 Trade Frequencyを最大化しない

市場理解OSは常に市場へ参加することを目的にしない。

正常なDecisionには、

~~~text
TRADE
WAIT
REDUCE
NO TRADE
UNKNOWN → Research
~~~

が含まれ得る。

したがって、

> **Trade回数・市場参加時間を、それ自体の目的として最大化しない。**

~~~text
No Edge
Unknown
Constraint
Insufficient Evaluation
~~~

等の状態で、取引回数を増やすためだけにTradeしない。

---

## 3.7 Capital Utilization / Exposureを最大化しない

資本を保有していることは、常時100%市場へ投入しなければならないことを意味しない。

~~~text
良いOpportunityがない
Riskが高い
Knowledgeが不十分
Current MarketがUNKNOWN
~~~

等であれば、資本を使わないこと自体が合理的Decisionになり得る。

したがって、

> **Capital Utilization・Exposure・Leverageを、それ自体の目的として最大化しない。**

具体的なCapital Allocation・Risk Budget・Leverage数値は後続Sectionで定義する。

---

## 3.8 Research Countを最大化しない

市場理解OSは、発見した全てを無条件にResearchへ送らない。

Research対象を無制限に増やすと、

~~~text
重要Researchの遅延
計算資源消費
Data / API Cost増加
Review不能
未完了Research蓄積
~~~

等につながり得る。

したがって、

> **Research件数ではなく、Research Value・再利用性・検証価値・意思決定への意味を重視する。**

~~~text
1000本の浅いResearch
~~~

が、

~~~text
10本の重要なResearch
~~~

より自動的に優れているとはしない。

---

## 3.9 Data Amountを最大化しない

取得できるDataを無条件に全て集め、全て永久保存することをSuccessとはしない。

重視するのは、

~~~text
何を表すDataか
品質はどうか
どのResearch / Decisionに必要か
再現・検証・説明に必要か
Costに見合うか
~~~

である。

したがって、

> **Data Quantityではなく、Information Value・Quality・Traceability・再利用性を重視する。**

具体的Retention Policyは後続設計で定義する。

---

## 3.10 Feature / Metric Countを最大化しない

独自Data・Derived Metric・Research Outputを追加できる構造は重要である。

しかし、

~~~text
Feature数
独自Metric数
Indicator数
~~~

が多いこと自体を成熟度とは扱わない。

増加によって、

~~~text
Overlap
Dependency
Noise
Overfitting
Maintenance Cost
~~~

が増える可能性がある。

したがって、

> **Feature数・Metric数を、それ自体の目的として最大化しない。**

---

## 3.11 Historical / Backtest Performanceを単独最大化しない

Historical ValidationやBacktestは重要なResearch手段である。

しかし、

~~~text
Past Profit
Past Return
Historical Win Rate
Historical Sharpe
~~~

等を単独で最大化すると、過去への過剰適合をSuccessと誤認する可能性がある。

したがって、

> **Historical / Backtest Performanceを、Future Validity・Current Applicability・Production Authorityの代替にしない。**

具体的OOS・Forward・Leakage・Overfitting対策はResearch設計で定義する。

---

## 3.12 AI / Model Scoreを最大化しない

AI / Prediction Modelが、

~~~text
Confidence
Accuracy
AUC
Loss
Internal Score
~~~

等を持つことはあり得る。

しかし、

~~~text
Model Scoreが高い
=
Market Truth
=
Trade Permission
~~~

とはしない。

したがって、

> **AI / Model内部ScoreをResearch Evidence・Knowledge Validity・Decision Authorityの代替として最大化しない。**

具体的なAI / Human / Production Authorityは後続Sectionで定義する。

---

## 3.13 System Complexityを最大化しない

市場理解OSは高度なSystemを目指すが、

~~~text
Layer数
AI数
Model数
Service数
Code量
~~~

が多いほど高度とは限らない。

必要なComplexityは受け入れる。

不要なComplexityは避ける。

~~~text
Simple
!= Primitive

Complex
!= Advanced
~~~

とする。

> **ComplexityそのものをSystem Quality・高度さ・完成度の代理Metricとして最大化しない。**

---

## 3.14 Automation Percentageを最大化しない

市場理解OSは自動化を重視する。

しかし、完全自動化という数字そのものを目的にはしない。

~~~text
Automation率が高い
=
Decisionが正しい
=
Authorityが正しい
=
Riskが適切
~~~

ではない。

したがって、

> **Automation PercentageをSystem Qualityの代理Metricとして最大化しない。**

具体的なHuman / AI / Production Authorityは後続Sectionで定義する。

---

## 3.15 Publication Reach / User GrowthをCore OSより優先しない

Human-readable Research Publication・Application・User Growth等はSecondary Successとして価値を持つ。

しかし、

~~~text
PV
User数
Download数
SNS反応
売上
~~~

等を伸ばすために、

~~~text
Research Conclusion
Evidence
Risk
Uncertainty
Unknown
~~~

を歪めてはならない。

> **Publication Reach・User Growth・Business ResultをResearch Integrityより上位に置かない。**

---

## 3.16 一つの万能Scoreへ潰さない

市場理解OS全体を、

~~~text
Profit
+
Win Rate
+
Prediction Accuracy
+
Research Count
+
Model Score
↓
One Total Score
~~~

だけで最適化しない。

一つの高い成果で、

~~~text
重大Risk Violation
Data Leakage
Knowledge Corruption
Research Integrity Failure
~~~

を相殺してはならない。

> **市場理解OSのSuccessを、一つの万能Scoreだけで最適化しない。**

---

## 3.17 Metric Gamingを禁止する

市場理解OSは、Metricを良く見せることを目的にしない。

例えば、

~~~text
Win Rate目標を満たすためだけにCaseを除外する

Profit目標を満たすためだけにRiskを増やす

Research Countを増やすためだけに小さなResearchを量産する

Prediction Accuracyを上げるためだけに曖昧Caseを隠す
~~~

等は禁止方向とする。

> **Metricを良く見せるために、そのMetricが本来測るべき目的・Mission・Integrityを壊してはならない。**

---

## 3.18 Metricの正しい位置付け

市場理解OSではMetricを、

~~~text
Evidence
Indicator
Diagnostic
Constraint Input
Review Trigger
~~~

として利用できる。

Metricは重要な判断材料である。

しかし、

> **Metricは判断材料であり、Project Missionそのものではない。**

例えばWin Rate低下は、

~~~text
Variance
Edge Decay
Regime Shift
Cost増加
Execution Problem
~~~

等を調べるTriggerになり得るが、Win Rate低下だけで原因を自動確定しない。

---

## 3.19 Core Not-To-Maximize List

市場理解OSは、以下を単独目的として最大化しない。

~~~text
1. Short-Term Profit
2. Win Rate
3. Prediction Accuracy
4. Trade Frequency
5. Capital Utilization / Exposure
6. Research Count
7. Data Amount
8. Feature / Metric Count
9. Historical / Backtest Performance
10. AI / Model Score
11. System Complexity
12. Automation Percentage
13. Publication Reach / User Growth
14. Any Single Universal Success Score
~~~

重要:

~~~text
Not Maximize
!= Ignore
~~~

必要なMetricは測る。

必要なら改善する。

ただし、そのMetricを良くするためにProject Mission・Research Integrity・Knowledge Integrity・Risk・長期生存を壊さない。

---

# What Not To Maximize — 一文定義

> **市場理解OSは、短期Profit・Win Rate・Prediction Accuracy・Trade回数・資本稼働率・Research数・Data量・Model Score・System Complexity・User Growth等の単一Metricを、それ自体の目的として最大化せず、それらを市場理解・Research Integrity・Knowledgeの再利用性・Decision Quality・Risk・長期生存を評価するための部分的な指標として扱う。**

簡潔には、

> **測りやすい数字を最大化するのではなく、市場を理解し、学び、適応し、生存しながらEconomic Valueへ接続できるSystem全体を育てる。**



---

# 4. Survival / Profit Priority

## 4.1 Core Principle

市場理解OSは、SurvivalとProfitのどちらか一方だけを最大化するSystemではない。

> **市場理解OSは、長期生存をEconomic ActivityのHard Operating Boundaryとし、その境界を壊さない範囲で、Research・Knowledge・Decisionに基づく正のExpected Economic Valueを持つ利益機会を選択的かつ積極的に追求する。**

基本関係は、

~~~text
Survival
= Hard Operating Boundary

Profit / Positive Economic Value
= Objective pursued inside that boundary
~~~

とする。

SurvivalのためにEconomic Missionを恒常的に放棄せず、Profitのために市場理解OS全体の継続能力を賭けない。

---

## 4.2 SurvivalはHard Operating Boundaryである

Survivalは、Profit・Win Rate・Model Score等と同列の一つのMetricとして扱わない。

Hard Survival Boundaryを満たさないOpportunityを、

~~~text
高Profit
高Expected Value
高Confidence
高Backtest Result
~~~

等で数値的に相殺しない。

概念順序は、

~~~text
Survival Gate
↓
PASS
↓
Economic Evaluation / Decision
~~~

とする。

Hard Survival Violationを万能Scoreの中へ埋め込み、他の高いScoreで打ち消してはならない。

---

## 4.3 ProfitはEconomic Objectiveであり続ける

Survival Boundaryを設けることは、Profitを軽視することではない。

市場理解OSは純粋な保存・防御Systemではなく、Research・Knowledge・Decisionを利用してEconomic Valueへ接続するSystemである。

したがって、

> **Hard Survival Boundaryの内側では、正のExpected Economic Valueを持つ利益機会を選択的かつ積極的に追求する。**

ただし、

~~~text
Positive Expected Value
!= automatic Trade Permission
!= automatic Capital Permission
~~~

とする。

Survival Boundaryを通過した後でも、Expected Value一つだけで最終Actionを決めない。

---

## 4.4 SurvivalはZero Riskを意味しない

市場理解OSはRiskを完全に避けるSystemではない。

~~~text
Survival
!= Zero Risk
~~~

とする。

Riskを一切取らなければ、Economic Missionそのものを失う。

市場理解OSは、

> **理解・制限・回復可能なRiskを選択的に引き受ける。**

ことを基本方向とする。

どの程度のRiskを許容するか、どのようなRisk Budgetを持つかは後続のCapital / Risk設計で定義する。

---

## 4.5 Project-ending / Unrecoverable Risk

市場には完全には予測できないEventが存在するため、市場理解OSは「あらゆる未来で絶対に損失しない」ことを保証しない。

一方で、

> **合理的に認識可能なProject-ending / Unrecoverable Failure Pathを、単一OpportunityのExpected Profitだけを理由に受け入れない。**

とする。

ここでいうProject-ending / Unrecoverable Failureは、Capital残高がゼロになる場合だけを意味しない。

市場理解OSが今後も、

~~~text
観測する
研究する
Knowledgeを保持する
判断する
運用する
復旧する
再研究する
~~~

能力を現実的に継続できなくなるFailureを含む。

---

## 4.6 Recoverability

Survivalには、LossやFailureの発生を完全に防ぐことだけでなく、発生後に市場理解OSの主要Loopへ戻れることを含める。

> **Recoverabilityとは、Loss・Failure・System Damageの後でも、必要なCapital・Research・Knowledge・Decision・Operation能力を再構築し、Observation → Research → Decision → Operation → Re-Researchへ現実的に復帰できる能力である。**

~~~text
生き残った
!=
Recovery Pathが残っている
~~~

場合があるため、単に現在動いていることだけでSurvivalを判定しない。

また、

~~~text
一回のLossからRecover可能
!=
同じRiskを無制限に繰り返してよい
~~~

とする。

累積DamageによってRecoverabilityが失われる可能性を考慮する。

---

## 4.7 SurvivalはCapitalだけではない

市場理解OSのSurvivalは、少なくとも以下の能力を含む。

~~~text
Capital Survival
Research Capability
Knowledge Integrity
Decision Integrity
Operational Continuity
~~~

したがって、

~~~text
Capitalが残った
=
市場理解OS全体がSurviveした
~~~

とは限らない。

Trading活動によってResearch能力・Knowledge履歴・Decision Trace・復旧能力等を恒常的に破壊してはならない。

---

## 4.8 Loss / Drawdownは自動的にSurvival Failureではない

市場でRiskを取る以上、LossやDrawdownは発生し得る。

~~~text
Loss
!= Survival Failure

Drawdown
!= automatically Project Failure
~~~

とする。

理解・許容されたRisk Boundary内で発生し、Decisionと原因を後から検証可能なLossは、正常な市場結果になり得る。

一方、同じ金額のLossでも、

~~~text
Constraint無視
Material Unknown無視
Failure Boundary無視
Recovery不能
~~~

等によって発生した場合は意味が異なる。

具体的Drawdown上限・Loss Limitは後続Risk設計で定義する。

---

## 4.9 過剰なRisk Avoidanceも目的ではない

市場理解OSはSurvivalを理由に、

~~~text
常にWAIT
常にNO TRADE
常に最小Exposure
~~~

を選び続けるSystemではない。

十分に研究・検証され、Hard Survival Boundary内にあり、正のExpected Economic Valueを持つOpportunityを恒常的に捨て続けることもEconomic Missionと両立しない。

> **Survivalは利益機会を永久に避ける理由ではなく、利益機会を継続的に利用できる状態を守るための境界である。**

---

## 4.10 複数のRisk Postureを許容する

市場理解OSは、通常時と高い非対称性を持つOpportunity時で、異なるRisk Postureを持つことを将来許容できる。

概念上、

~~~text
CORE MODE
+
OPPORTUNITY MODE
~~~

等の異なる運用姿勢を後続設計で定義してよい。

ただしSection 4では、

~~~text
Mode entry条件
Mode exit条件
Risk Envelope差
Exposure差
Risk倍率
具体Threshold
~~~

は固定しない。

これらはSection 7 Capital / Risk Philosophyと後続Detailed Designで扱う。

---

## 4.11 どのModeもHard Survival Boundaryを回避できない

異なるRisk Postureを許容しても、

~~~text
CORE MODE
+
OPPORTUNITY MODE
↓
same Hard Survival Boundary
~~~

とする。

Opportunity Mode等は、Risk Governanceを解除する例外ではない。

特に、

~~~text
COREでRisk制約に抵触した
↓
Opportunity扱いへ変更
↓
制約を回避
~~~

というMode Shoppingを禁止方向とする。

また、

~~~text
Profit Target不足
過去Loss
過去Profit
連勝
AI / Model Confidence
~~~

等を、それ自体でHard Survival Boundaryの緩和理由にしない。

---

## 4.12 Survival-Critical Unknown

市場理解OSはUnknownを自動的に安全扱いしない。

~~~text
UNKNOWN
!= SAFE
~~~

とする。

ただしUnknownが存在するだけで全てのActionを禁止するわけではない。

> **SurvivalにMaterialなUnknownは、安全が確認された既知状態として扱わず、明示的な判断・制約・Research対象とする。**

具体的なMateriality判定方法は後続設計で定義する。

---

## 4.13 Hard Survival ViolationをEconomic Scoreで相殺しない

Hard Survival Boundary違反を、

~~~text
高Profit
Positive EV
高Win Rate
高Confidence
高Model Score
~~~

等で相殺しない。

~~~text
Economic attractiveness
!= Survival permission
~~~

とする。

これはSection 3の、

~~~text
一つの万能Scoreで重大Failureを相殺しない
~~~

という原則をRisk / Survivalへ適用するものである。

---

## 4.14 Fast SafetyとResearch / Knowledge Truthを分離する

市場急変・Execution異常・Actual Exposure Risk等によってImmediate Safety Actionが必要な場合、Research完了を待たずに保護Actionを実行できる方向を持つ。

一方で、

~~~text
Immediate Safety Action
!= Knowledge Invalidity
!= Research Refutation
~~~

とする。

> **Survival保護の即時Actionと、Knowledgeが正しいか・壊れたかというResearch判断を別のAuthorityとして扱う。**

Safety Actionを行ったことだけを理由にKnowledgeを無効化せず、Knowledge評価のために危険なExposureを放置もしない。

---

## 4.15 Aggregate / Sequence-level Survival

Survivalは単一Trade・単一Decisionだけで評価しない。

~~~text
Individually bounded risk
!= Aggregate risk bounded
~~~

とする。

複数の小さいRiskでも、

~~~text
同時Exposure
累積Exposure
共通原因
同一Market Direction
同一Liquidity Risk
同一Exchange Risk
~~~

等によって、System全体では大きなSurvival Riskになる可能性がある。

具体的なCorrelation・Portfolio Risk・Stress計算は後続Risk設計で定義する。

---

## 4.16 Research TruthとSurvival PolicyのAuthorityを分離する

Survivalを守る必要があっても、Research / Knowledgeの結論をRisk都合で書き換えてはならない。

~~~text
Research / Knowledge
= What is supported / known?

Survival / Risk Policy
= May we act on it under current constraints?
~~~

と分離する。

したがって、

~~~text
Knowledge is valid
!= Capital / Risk Permission

Risk blocks use
!= Knowledge is false
~~~

とする。

同様に、Profit期待が高いことを理由にKnowledgeのValidity・Applicability・Unknownを都合よく変更してはならない。

---

## 4.17 このSectionで決めないこと

Section 4ではPriorityとBoundary Philosophyを定義し、具体的なRisk数値・Formula・Implementationは固定しない。

以下は後続設計で扱う。

~~~text
Maximum Drawdown %
Single Trade Risk %
Daily / Weekly Loss Limit
Leverage Limit
Exposure Limit
Capital Reserve Ratio
Position Size Formula
Stop Loss Rule
CORE / OPPORTUNITY Mode Threshold
Mode-specific Risk Envelope
Emergency Threshold
Correlation / Portfolio Risk Formula
Exchange Concentration Limit
Tail Risk Budget
~~~

---

## 4.18 Core Invariants

~~~text
SP-01 Survival and Profit are both Project requirements.
SP-02 Survival is a Hard Operating Boundary, not one interchangeable score.
SP-03 Profit / Positive Economic Value is pursued inside that boundary.
SP-04 Survival != Zero Risk.
SP-05 Positive EV != automatic Trade / Capital Permission.
SP-06 Reasonably foreseeable project-ending / unrecoverable risk is not justified by one opportunity's expected profit alone.
SP-07 Loss != automatically Survival Failure.
SP-08 Drawdown != automatically Project Failure.
SP-09 Excessive permanent Risk Avoidance is not the intended Economic behavior.
SP-10 Recoverability is part of Survival.
SP-11 Capital Survival alone != total OS Survival.
SP-12 Single-event bounded risk != aggregate / sequence-level bounded risk.
SP-13 Different Risk Postures may exist, but no Mode may bypass the Hard Survival Boundary.
SP-14 Profit shortfall / past Loss / past Profit / Model Confidence do not independently justify Hard Boundary relaxation.
SP-15 Material Survival-Critical UNKNOWN != SAFE.
SP-16 Hard Survival Violation cannot be numerically offset by Economic Score.
SP-17 Immediate Safety Action != Knowledge Invalidity.
SP-18 Safety protection may act before slow Research completion.
SP-19 Survival Policy does not own Research / Knowledge Truth.
SP-20 Knowledge Validity != Risk / Capital Permission.
~~~

---

# Survival / Profit Priority — 一文定義

> **市場理解OSは、長期生存をEconomic ActivityのHard Operating Boundaryとし、その境界を壊さない範囲で正のExpected Economic ValueとProfitを積極的に追求する。Riskをゼロにするのではなく理解・制限・回復可能なRiskを選択的に引き受け、異なるRisk Postureを許容してもHard Survival Boundaryを回避する例外は作らず、単一Opportunityの利益のために市場理解OS全体の継続能力を交換しない。**

簡潔には、

> **生き残るために利益を捨て続けず、利益のために生き残る能力を賭けない。**



---

# 5. Research Mission

## 5.1 Core Research Mission

市場理解OSにおけるResearchは、Hypothesis数・Experiment数・Research件数を増やすために存在しない。

Researchの中心目的は、

> **市場変化・未知・矛盾・Failure・Economic Opportunity・Post-Decision Findingを選択的に研究し、仮説を正当化するのではなく検証・反証・限界確認を行い、その結果を再利用可能なResearch ResultとResearch Assetとして残し、市場理解OSの長期生存・市場適応・意思決定・Economic Value創出能力を継続的に高めること。**

とする。

基本関係は、

~~~text
Research
!= Research Count Maximization

Research
!= Hypothesis Confirmation Factory

Research
!= Production Permission

Research
= Reusable Understanding / Evidence / Failure / Unknown Creation
~~~

とする。

---

## 5.2 Software完成後もResearchは終わらない

市場理解OSでは、

~~~text
Software完成
!= Research終了
~~~

である。

市場・参加者・Liquidity・Leverage・Regime・Macro・Exchange環境・利用可能Data等が変化する以上、現在有効なKnowledge・Edge・Failure Boundaryも永久の正解ではない。

したがって、

~~~text
Observation
↓
Unknown / Change / Contradiction / Failure
↓
Research
↓
Research Result
↓
Knowledge側で評価
↓
Decision / Production利用
↓
Post-Decision
↓
Re-Research
~~~

という循環を長期的に維持する。

> **市場理解OSが運用される限り、Research Missionも継続する。**

---

## 5.3 Researchは選択的に行う

市場で発見された全ての変化・異常・未知・Cause Candidate・Failure・Opportunityを無条件に正式Researchへ進めない。

Research対象は、

~~~text
Research Value
Reusability
Decisionへの意味
Survivalへの意味
Economicへの意味
Evidence / Researchability
Cost
Urgency
~~~

等を踏まえて選択する。

> **研究しない・後回しにする・既存Researchへ統合する判断も、正常なResearch Governanceの一部である。**

これはSection 3の、

~~~text
Research Count
!= Project Success
~~~

という原則を維持する。

---

## 5.4 ResearchはConfirmationのために行わない

Researchは、既存Hypothesis・Strategy・Knowledge・Trade Thesisを正しいことにするための場所ではない。

Researchは少なくとも、

~~~text
Validation
Refutation
Contradiction
Alternative Hypothesis
Failure Boundary
Constraint
Unknown
Inconclusive
~~~

を扱える必要がある。

> **Hypothesisを守ることではなく、どこまで成立し、どこで壊れ、何がまだ分からないかを明らかにすることを重視する。**

Research中に現在市場・Profit期待・Publication都合に合わせてHypothesisやConclusionを都合よく書き換えない。

---

## 5.5 Research SuccessとSupported Hypothesisを同一視しない

Researchの成功は、Hypothesisが支持されたことだけではない。

例えば、

~~~text
SUPPORTED
REFUTED
FAILURE BOUNDARY FOUND
CONSTRAINT FOUND
INCONCLUSIVE
INSUFFICIENT EVIDENCE
UNKNOWN
~~~

はいずれも、正しく検証されTrace可能であれば価値あるResearch Resultになり得る。

> **Research Successとは、望んだ結論を得ることではなく、何が支持され、何が否定され、どこまで通用し、何がまだ分からないかを再利用可能な形で明らかにすること。**

---

## 5.6 Research ResultはKnowledge / Production Authorityではない

ResearchはResearch Resultを生成する。

しかし、

~~~text
Research Candidate
!= Hypothesis

Hypothesis
!= Research Result

Validated Research Result
!= Knowledge

Knowledge
!= Current Applicability

Current Applicability
!= Trade Permission
~~~

とする。

> **ResearchはKnowledge領域で評価可能なResearch Resultを生成するが、Research自身がKnowledge Promotion・Current Applicability・Trade Permission・Capital Permissionを所有しない。**

ResearchとProductionの責任境界を維持する。

---

## 5.7 Primary Research Mission Families

市場理解OSでは、Research Missionを大きく次の5 Familyとして扱う。

~~~text
RM-1
FOUNDATIONAL / MECHANISM RESEARCH

RM-2
SURVIVAL / FAILURE RESEARCH

RM-3
ECONOMIC EDGE RESEARCH

RM-4
ADAPTATION / REVALIDATION RESEARCH

RM-5
DECISION / EXECUTION QUALITY RESEARCH
~~~

これはPython Module・Folder・DB Tableを意味しない。

> **Researchを何のために行うかを表す上位Mission Familyである。**

一つのResearchが複数Missionへ関係することを許容する。

---

## 5.8 RM-1 — FOUNDATIONAL / MECHANISM RESEARCH

FOUNDATIONAL / MECHANISM RESEARCHは、

> **市場で何が起き、なぜそのように動くのかを理解するための基礎研究。**

とする。

研究対象候補には、

~~~text
Market Structure
Participant Behavior
Price Formation
Liquidity Mechanism
Leverage Mechanism
Causal Chain
Cross-Market Transmission
Unknown Market Structure
~~~

等を含み得る。

このResearchは、直接Trade Edgeになることを必須条件にしない。

> **Economic Valueへ接続する前段階として、市場を理解すること自体にResearch Valueを認める。**

Research Resultは、将来のKnowledge・Economic Edge・Failure Research・Adaptation Research等の基礎へ再利用できる。

---

## 5.9 RM-2 — SURVIVAL / FAILURE RESEARCH

SURVIVAL / FAILURE RESEARCHは、

> **何が市場理解OSを壊し得るか、どこにFailure Boundaryがあり、どのRiskが許容可能で、どこで停止・縮小・再研究すべきかを理解するためのResearch。**

とする。

研究対象候補には、

~~~text
Tail Risk
Failure Pattern
Failure Boundary
Constraint
Liquidity Failure
Exchange / Infrastructure Failure
No-Trade Condition
Survival-Critical Unknown
Recoverability
Repeated Failure
~~~

等を含み得る。

これは全てのRiskを避けるためのResearchではない。

~~~text
Takeable Risk
vs
Unacceptable Risk
~~~

を区別するためのResearchでもある。

Immediate Safety ActionのAuthorityはResearch自身が所有しない。

---

## 5.10 RM-3 — ECONOMIC EDGE RESEARCH

ECONOMIC EDGE RESEARCHは、

> **Market Understandingを、どの条件で再利用可能なExpected Economic Valueへ接続できるかを研究する。**

とする。

Researchでは単に「儲かったか」を確認するのではなく、

~~~text
なぜ機能する可能性があるか
どの条件で成立するか
どのRegimeで利用可能か
どのCostに耐えられるか
どこでEdgeが弱まるか
どこでFailureするか
どの程度再現可能か
~~~

を研究する。

Economic Edge Researchには、将来、

~~~text
CORE EDGE
OPPORTUNITY
~~~

等の異なるResearch Philosophyを持つことができる。

ただし、CORE EDGE / OPPORTUNITYの正式定義・関係・Research Philosophyの詳細はSection 6で設計する。

~~~text
Economic Edge Research Result
!= Trade Permission
!= Opportunity Mode Permission
~~~

を維持する。

---

## 5.11 RM-4 — ADAPTATION / REVALIDATION RESEARCH

ADAPTATION / REVALIDATION RESEARCHは、

> **既存Knowledge・Edge・Failure Boundary等の成立条件が現在も維持されているかを再検証し、市場構造が変化した場合、その原因と影響を研究する。**

とする。

研究対象候補には、

~~~text
Regime Shift
Edge Decay
Knowledge Failure
Knowledge Contradiction
Applicability Contradiction
Participant Structure Change
Structural Change
Periodic Revalidation
~~~

等を含み得る。

これはEvidenceなしに全てを変更し続けるためのResearchではない。

> **Knowledgeを信用するが永久の正解にはせず、Evidenceに基づいて安定性と適応性を両立する。**

CORE EDGE / OPPORTUNITY / Adaptationのより詳細な研究思想はSection 6で定義する。

---

## 5.12 RM-5 — DECISION / EXECUTION QUALITY RESEARCH

DECISION / EXECUTION QUALITY RESEARCHは、

> **市場理解・Knowledge・Decision Reasoningが、Decision・Defense・Trade / No-Trade・Execution・Post-Decision Outcomeへ意図した通り接続されたかを研究する。**

とする。

研究対象候補には、

~~~text
TRADE
WAIT
REDUCE
NO TRADE
Defense
Missed Opportunity
Post-Decision Finding
Execution Cost
Slippage
Unexpected Failure
Decision Quality
~~~

等を含み得る。

例えば、

~~~text
Market Understandingは妥当だった
Trade Thesisも妥当だった
しかしExecution CostでEconomic Valueが失われた
~~~

場合、市場理解そのものとExecution Qualityを区別して研究する。

ResearchはExecutionを直接操作するAuthorityではなく、Resultを研究対象として評価する。

---

## 5.13 Research Integrity / Methodologyは全Missionへ適用する

Research Integrityを6つ目のResearch Missionにはしない。

~~~text
RM-1
RM-2
RM-3
RM-4
RM-5
↓
Research Integrity / Methodology applies to all
~~~

とする。

Researchでは少なくとも、

~~~text
Evidence Provenance
Evidence Source / Role / Time / Version
Validation / Refutation separation
Alternative Hypothesis
Reproducibility
Leakage avoidance
Look-ahead avoidance
Research Process Failure separation
Traceability
~~~

を重視する。

具体的なValidation Method・Research Contract・ThresholdはResearch Architecture / Detailed Designで定義する。

> **Research UrgencyやEconomic Opportunityを理由にResearch Integrityを緩和しない。**

---

## 5.14 Research Candidate SourceとResearch Missionを分ける

Researchが発生した理由と、何のために研究するかを混同しない。

~~~text
Research Candidate Source
!= Research Mission
~~~

市場理解OSでは、

~~~text
Cause Candidate
Unknown
Contradiction
Failure
Post-Decision Finding
Missed Opportunity
AI Suggestion
~~~

等がResearch Candidateを発生させ得る。

しかし、SourceだけでResearch Mission・Priority・Conclusionを確定しない。

---

## 5.15 一つのResearch Candidateから複数Research Questionを許容する

一つの発見が複数のResearch Questionを持つことを許容する。

例えば、

~~~text
Liquidity Collapse Anomaly
↓
なぜ起きた？
→ Mechanism

どこまで危険？
→ Survival / Failure

Economic Edgeになる？
→ Economic Edge

既存Knowledgeが壊れた？
→ Adaptation / Revalidation
~~~

のように、一つのCandidateから複数MissionへResearch Questionが分岐してよい。

~~~text
One Candidate
!= Exactly One Mission
~~~

とする。

同じSourceを別々の独立Evidenceとして水増ししない。

---

## 5.16 Mission ClassificationはConclusionではない

Research Missionは、

> **何を知ろうとしているか**

を表す。

~~~text
Mission = SURVIVAL
!= Danger Confirmed

Mission = ECONOMIC EDGE
!= Edge Confirmed

Mission = ADAPTATION
!= Knowledge Invalid

Mission = DECISION QUALITY
!= Execution Failure Confirmed
~~~

とする。

Mission ClassificationをResearch ResultやAuthorityの代替にしない。

---

## 5.17 Mission / Priority / Method / Resultを分離する

市場理解OSでは、

~~~text
Research Mission
!= Intake Disposition
!= Research Priority
!= Validation Method
!= Research Result
~~~

とする。

Research Missionは、なぜ研究するかを表す。

Research Priorityは、いつ・どれだけ優先して研究するかを表す。

Validation Methodは、どう検証するかを表す。

Research Resultは、何が分かったかを表す。

これらを一つのLabelへ潰さない。

---

## 5.18 Research Priorityの上位原則

Mission名だけでResearch Priorityを決めない。

特に、

~~~text
SURVIVAL
= always highest priority

FOUNDATIONAL
= always low priority

OPPORTUNITY
= always urgent

Novel
= automatically important

Repeated
= automatically important
~~~

とはしない。

Research Priorityでは概念上、

~~~text
Importance
Potential Impact
Risk / Production Relevance
Urgency
Contradiction Severity
Evidence / Researchability
Research Cost
Reusability
~~~

等を分離して判断できる方向を持つ。

> **Research Priorityを一つの万能Scoreだけへ潰し、一軸の高Scoreで他の重大な問題を相殺しない。**

具体Priority Formula・Queue・Allocationは後続設計で定義する。

---

## 5.19 UrgencyとImportanceを混同しない

~~~text
Urgent
!= Important

Important
!= Urgent
~~~

とする。

Current Opportunityの消失が近いことはUrgencyを高め得るが、それだけでResearch Value・Evidence Quality・Importanceを確定しない。

一方で、Foundational ResearchやLong-Term Revalidationは緊急でなくても長期的に重要である可能性がある。

> **短期Current MarketのUrgencyだけでResearch Capacity全体を恒常的に支配させない。**

---

## 5.20 Fast Safety NeedとResearch Priorityを分離する

SurvivalにMaterialな問題が現在Exposureへ影響している場合、

~~~text
Fast Safety / Defense
+
Research
~~~

が並列に必要なことがある。

~~~text
Research Priority = Critical
!= Safety Action
~~~

とする。

> **Immediate Safety Protectionが必要な場合、Research完了を待たない。**

Researchは、なぜ危険だったか・どこまで危険か・再発防止に何が必要かを後から研究できる。

---

## 5.21 Negative / Failure / UnknownをResearch Assetとして残す

市場理解OSはPositive ResultだけをResearch Assetとしない。

~~~text
Refutation
Failure
Failure Boundary
Constraint
Contradiction
Unknown
Inconclusive
Insufficient Evidence
Research Process Failure
~~~

も、将来の再Research・Knowledge評価・Decision Reviewに利用できるResearch Assetになり得る。

> **何が使えるかだけでなく、何を使ってはいけないか、どこで壊れるか、何がまだ分からないかを残す。**

---

## 5.22 Research Process FailureとResearch Conclusionを分ける

~~~text
Hypothesis Refuted
!= Research Process Failure
~~~

とする。

例えば、

~~~text
Data不足
Experiment Failure
Computation Failure
Evidence Conflict
Invalid Test Design
Leakage
Look-ahead Bias
External Dependency Failure
~~~

等によって研究そのものが成立しなかった場合と、正しく研究した結果Hypothesisが反証された場合を混同しない。

Research Process Failureを都合よくNegative ResultまたはPositive Resultへ変換しない。

---

## 5.23 Human-readable Research Outputは下流Consumerである

Research Resultは自動Tradingだけでなく、人間向けResearch Outputへ再利用できる。

基本関係は、

~~~text
Research Core
↓
Validated Research Result
├─→ Knowledge
├─→ Re-Research
├─→ Future Decision / Production Use
└─→ Human-readable Research Output
~~~

とする。

ただし、

> **Publication Demand・User Growth・Business ResultはResearch Truthを書き換えるAuthorityを持たない。**

Research Output / Publicationの具体Mission・形式・User ValueはSection 11で設計する。

---

## 5.24 AIはResearch支援者でありResearch Truthそのものではない

AIはResearchにおいて、

~~~text
Research Question候補
Hypothesis候補
Alternative Hypothesis
Contradiction探索
Research Plan支援
Research Review
説明
~~~

等を支援できる。

しかし、

~~~text
AI Output
!= Research Evidence
!= Validation Result
!= Production Authority
~~~

とする。

AI / Human / Production Authorityの詳細はSection 12で定義する。

---

## 5.25 このSectionで決めないこと

Section 5ではResearch Mission・上位責任・境界を定義し、具体Implementationや詳細Research Contractは固定しない。

以下は後続設計で扱う。

~~~text
Research Candidate Schema
Mission ID / Enum
Primary / Secondary Mission Field
Intake State詳細
Mission Classification Algorithm
Research Priority Formula
Research Queue
Research Capacity Allocation
Routing Algorithm
Validation Threshold
Evidence Score
Hypothesis Score
DB Schema
Python Class
AI Classifier Prompt
OOS具体期間
Forward具体期間
Stress Scenario詳細
CORE EDGE正式定義
OPPORTUNITY正式定義
Adaptation詳細思想
Publication詳細Mission
AI / Human / Production Authority詳細
~~~

CORE EDGE / ADAPTATION / OPPORTUNITYの詳細研究思想はSection 6へ送る。

---

## 5.26 Core Invariants

~~~text
RM-01 Research Count != Research Value.
RM-02 Software Completion != Research Completion.
RM-03 Research is selective; not every Candidate must become formal Research.
RM-04 Research != Confirmation Factory.
RM-05 Supported Hypothesis != only successful Research outcome.
RM-06 Refutation / Failure / Boundary / Constraint / Unknown may be valuable Research Result.
RM-07 Validated Research Result != Knowledge != Production Authority.
RM-08 Foundational understanding may have value before direct Economic use.
RM-09 Survival Research != Safety Action Authority.
RM-10 Economic Edge Research Result != Trade / Capital Permission.
RM-11 Adaptation / Revalidation does not mean changing everything continuously.
RM-12 Decision / Execution Quality is a valid Research Mission.
RM-13 Research Integrity / Methodology applies across all Research Missions.
RM-14 Research Candidate Source != Research Mission.
RM-15 One Candidate may generate multiple Research Questions / Missions.
RM-16 Mission Classification != Research Conclusion.
RM-17 Mission != Intake Disposition != Priority != Method != Result.
RM-18 Mission name alone does not determine Priority.
RM-19 Urgency does not relax Research Integrity.
RM-20 Short-term Urgency must not permanently starve long-term Research.
RM-21 Fast Safety Need != Research Priority.
RM-22 Research Process Failure != Hypothesis Refutation.
RM-23 Publication / Business demand does not own Research Truth.
RM-24 AI Output != Research Evidence / Validation Result / Production Authority.
~~~

---

# Research Mission — 一文定義

> **市場理解OSのResearch Missionは、市場変化・未知・矛盾・Failure・Economic Opportunity・Post-Decision Findingを選択的に研究し、仮説を正当化するのではなく検証・反証・限界確認を行い、Market Mechanism・Survival / Failure・Economic Edge・Adaptation / Revalidation・Decision / Execution Qualityについて、Knowledge領域・再研究・将来のDecision・人間向けResearch Outputへ再利用可能なResearch ResultとResearch Assetを増やすことで、市場理解OSの長期生存・市場適応・意思決定・Economic Value創出能力を継続的に高めることである。**

簡潔には、

> **研究する目的は、正解を増やすことではなく、なぜ起き、何が通用し、何が壊れ、何がまだ分からず、判断Systemが正しく機能したかを明らかにし、その結果を次の研究と判断へ再利用すること。**



---

# 6. Research Category Philosophy

## 6.1 このSectionの役割

Section 5では、Research Missionとして `ECONOMIC EDGE RESEARCH` と `ADAPTATION / REVALIDATION RESEARCH` を定義した。

Section 6では、その下位思想として、

~~~text
CORE EDGE
OPPORTUNITY
ADAPTATION / REVALIDATION
~~~

の関係を定義する。

ただし、これらを3つの同格Categoryとして扱わない。

~~~text
CORE EDGE / OPPORTUNITY
= Economic Edge Character

ADAPTATION / REVALIDATION
= Cross-Temporal Research Philosophy
~~~

とする。

> **Section 6は「どのようなEdgeとして研究するか」を定義し、Knowledge Lifecycle・Current Applicability・Trade Permission・Capital / Risk Permissionを所有しない。**

---

## 6.2 Economic Edge Character

市場理解OSでは、Economic Edgeを単純に、

~~~text
勝った
負けた
高Win Rate
高Backtest
~~~

だけで分類しない。

Economic Edgeについて、

~~~text
どの条件で成立するか
なぜ成立する可能性があるか
どこで弱まるか
どこで壊れるか
どの程度再利用可能か
時間とともにどう変化するか
~~~

を研究し、その性質を `Edge Character` として扱う。

Edge CharacterはKnowledge LifecycleやCurrent Applicabilityとは別概念である。

---

## 6.3 CORE EDGE

CORE EDGEとは、

> **成立条件・Mechanism候補・Counter-Evidence・Failure Boundaryを研究可能であり、異なるCaseや時間Contextを通じて再検証・再利用できる可能性を持つEconomic Edge Character。**

とする。

COREは、

~~~text
Universal
Permanent
Always Applicable
High Win Rate
Strong Backtest
~~~

を意味しない。

~~~text
CORE
!= Universal

CORE
!= Permanent

CORE
!= Always Applicable
~~~

とする。

COREの意味は、

> **理解された条件下で、繰り返し研究・再利用できる可能性があること。**

である。

---

## 6.4 Repeated ProfitだけでCOREとしない

~~~text
Repeated Profit
!= CORE EDGE

Case Count
!= Independent Repeatability

Backtest Strength
!= Core Strength
~~~

とする。

複数回利益が出ても、

~~~text
同一Regimeへの偏り
同一Eventへの依存
Data Leakage
Look-ahead
Cost未考慮
Failure Boundary不明
Mechanism不明
~~~

等があれば、COREとして十分に理解されたとは限らない。

> **CORE Researchでは、Performanceだけでなく成立条件・反証・限界を含めて再利用可能性を研究する。**

---

## 6.5 CORE Researchは成功条件とFailure条件を両方研究する

CORE EDGEは、

~~~text
Where it works
+
Where it weakens
+
Where it fails
~~~

をセットで研究する。

したがって、

~~~text
Strong Conditions
Weak Conditions
Invalid / Failure Conditions
Unknown Conditions
~~~

を区別できる方向を持つ。

> **成功Caseだけを集めてCOREを作らず、Counter-EvidenceとFailure BoundaryもCORE理解の一部として扱う。**

---

## 6.6 COREは歴史的成功によって再検証を免除されない

過去に長期間成功したCORE EDGEでも、市場構造・参加者・Liquidity・Cost・Exchange構造等が変化する可能性がある。

~~~text
Historical Success
!= Revalidation Exemption
~~~

とする。

COREは利用可能な限り利用できるが、永久の正解として固定しない。

---

## 6.7 OPPORTUNITY

OPPORTUNITYとは、

> **特定の一時的なDistortion・Imbalance・Event・Market Structure等へEconomic Valueが強く依存し、その条件の消滅とともに価値がDecayする可能性を持つEconomic Edge Character。**

とする。

OPPORTUNITYは単に大きく動いた市場を意味しない。

~~~text
Rare
!= Opportunity

Volatile
!= Opportunity

Large Move
!= Opportunity

Large Potential Profit
!= Opportunity

Unknown
!= Opportunity
~~~

とする。

---

## 6.8 OPPORTUNITYは一時的Economic Structureとして研究する

OPPORTUNITY Researchでは、少なくとも概念上、

~~~text
何が歪みを作ったか
何が歪みを維持しているか
何が歪みを解消するか
どのようなDownside / Failure Pathがあるか
Opportunity自体がどのようにDecayするか
~~~

を研究する。

> **OPPORTUNITYは「面白い値動き」というLabelではなく、一時的Economic Structureに関するResearch Hypothesisとして扱う。**

---

## 6.9 Asymmetryは最初から確定事実にしない

Opportunityが非対称に見える場合でも、

~~~text
Potential Asymmetry
!= Confirmed Asymmetry
~~~

とする。

Upside・Downside・Liquidity・Cost・Failure Scenario・Time Decay等を研究し、期待される非対称性が本当に存在するかを検証対象とする。

---

## 6.10 Opportunity ClosureとResearch Failureを分ける

Temporary Opportunityは、条件消滅によって正常に終了する場合がある。

~~~text
Opportunity disappeared
!= Research Failure

Expected Opportunity Closure
!= Edge Decay
~~~

とする。

例えば、Arbitrage・Market Repricing・Event Resolution等によって歪みが消えることは、Opportunityの正常なLifecycleになり得る。

> **Opportunityが消えたこと自体ではなく、なぜ消えたか・想定されたClosureか・最初から誤分類だったかを研究する。**

---

## 6.11 Opportunity ResearchとRisk / Capital Permissionを分離する

~~~text
Opportunity Research Result
!= Opportunity Mode Permission

Opportunity Research Result
!= Trade Permission

Opportunity Research Result
!= Capital Permission
~~~

とする。

Section 6はOpportunityのResearch Characterを定義する。

そのOpportunityへどのRisk・Capital・Exposureを許容するかはSection 7以降の責任とする。

---

## 6.12 Edge CharacterがUNRESOLVEDであることを許容する

Economic Edge Candidateが発見されても、

~~~text
CORE
or
OPPORTUNITY
~~~

へ必ず即時分類しない。

Repeatability・Persistence・Temporary Dependency等がまだ不明な場合、

> **Edge Characterが未解決である状態を許容する。**

とする。

Evidence不足を埋めるためだけにCORE / OPPORTUNITYへ強制分類しない。

---

## 6.13 CORE / OPPORTUNITY Characterは永久固定しない

一時的Opportunityとして研究された現象が、後の研究で、

~~~text
Repeated Occurrence
Mechanism Stability
Conditional Repeatability
~~~

を持つと分かる場合がある。

逆に、COREとして研究されたEdgeの成立範囲が狭くなる場合もある。

ただし、

~~~text
Character Change
!= Historical Rewrite
~~~

とする。

> **Edge Characterの再評価は新しいResearch Conclusionとして扱い、過去のResearch Historyを消さない。**

---

## 6.14 ADAPTATION / REVALIDATION

ADAPTATION / REVALIDATIONとは、

> **CORE / OPPORTUNITYを永久固定せず、成立条件・Economic Effect・Market Structure・Mechanism・Failure Boundaryが時間とともにどう変化したかを再研究する思想。**

とする。

ADAPTATIONは3つ目のEconomic Edge Characterではない。

~~~text
CORE / OPPORTUNITY
= Edge Character

ADAPTATION / REVALIDATION
= Edge Characterを時間軸で再検証するResearch Philosophy
~~~

とする。

---

## 6.15 Adaptationは変更すること自体を目的にしない

~~~text
Adaptation
!= Always Change
~~~

とする。

市場理解OSは、Evidenceが維持されているKnowledge / Edgeを理由なく変更し続けない。

同時に、過去に成功したことだけを理由に重大なContradictionを無視し続けない。

> **AdaptationはStabilityとResponsivenessの両方を維持するために行う。**

---

## 6.16 Adaptation TriggerとAdaptation Conclusionを分ける

Loss・Unexpected Outcome・Contradiction等は再研究のTriggerになり得る。

しかし、

~~~text
Unexpected Outcome
!= Edge Decay

One Contradiction
!= Material Change
~~~

とする。

> **異常結果はAdaptation Researchの入口であり、Edge Decay・Knowledge Failure・Structural Breakの結論そのものではない。**

---

## 6.17 Data / Decision / Execution FailureをEdge Failureへ誤変換しない

Economic Outcomeが悪かった場合でも、原因はEconomic Edgeそのものとは限らない。

~~~text
Data / Observation Failure
Decision Failure
Defense Failure
Execution Failure
Temporary Event
Regime Mismatch
Variance
Unknown
~~~

等を区別する必要がある。

~~~text
Bad PnL
!= Edge Failure
~~~

とする。

原因を最も近いSemantic Ownerへ返し、別領域のFailureを理由にEdge Truthを書き換えない。

---

## 6.18 Regime / Applicability MismatchとKnowledge Failureを分離する

既存Knowledgeの成立条件からCurrent Marketが外れた場合、

~~~text
Current Applicability Mismatch
!= Knowledge Failure
~~~

とする。

例えば、

~~~text
Knowledge:
Bull Lateで成立

Current Market:
Crash
~~~

であれば、そのKnowledge自体が過去から間違っていたとは限らない。

現在使えるかどうかの最終評価はKnowledge / Applicability領域の責任とする。

---

## 6.19 Edge Decay

Edge Decayは、

> **Materialに比較可能な条件下でも、以前観測されたEconomic Effectが時間とともに継続的に弱まっている現象候補。**

とする。

~~~text
One Loss
!= Edge Decay

Temporary Shock
!= Edge Decay
~~~

である。

Edge Decayが疑われる場合でも、その原因としてMarket Participant・Arbitrage・Liquidity・Cost・Exchange Mechanics・Crowding等の変化をさらに研究できる。

---

## 6.20 Structural Break

Structural Breakは、

> **Edgeを支えていたMarket Mechanism・Participant Structure・Market Microstructure・Institutional Condition等の生成構造自体がMaterialに変化した状態候補。**

とする。

Regime ShiftとStructural Breakを同一視しない。

~~~text
Regime Shift
= Market State Change

Structural Break
= Generative Market Structure Change
~~~

とする。

また、

~~~text
New Event
!= Structural Break

Temporary Shock
!= Structural Break

Edge Decay
!= Structural Break
~~~

とする。

---

## 6.21 COREとOPPORTUNITYでAdaptation Questionを分ける

COREでは主に、

> **このEdgeは現在も再利用可能か？**

を問う。

OPPORTUNITYでは主に、

> **このTemporary Economic Structureはまだ存在するか？**

を問う。

Edge Characterが未解決の場合は、

> **そもそもこのEdgeのCharacterは何か？**

をResearch対象とする。

---

## 6.22 Overreaction / Underreactionの両方を避ける

Adaptationが敏感すぎる場合、

~~~text
One Loss
↓
Knowledge変更
↓
Overreaction
~~~

となり、安定したKnowledgeを破壊する。

Adaptationが遅すぎる場合、

~~~text
Persistent Contradiction
↓
無視
↓
Stale Knowledge継続
~~~

となる。

したがって、

> **過剰適応と古いKnowledgeへの固執の両方をAdaptation Failureとして扱う。**

---

## 6.23 Edge Character / Lifecycle / Applicabilityを分離する

~~~text
CORE / OPPORTUNITY
= Edge Character

ACTIVE / SUSPENDED / RETIRED 等
= Knowledge Lifecycle

APPLICABLE / NOT_APPLICABLE 等
= Current Applicability
~~~

と分離する。

したがって、

~~~text
CORE
!= ACTIVE

OPPORTUNITY
!= WEAK

CORE
!= Currently Applicable

OPPORTUNITY
!= Currently Applicable

ADAPTATION RESULT
!= automatic Lifecycle Change
~~~

とする。

Knowledge Lifecycle・Current ApplicabilityのAuthorityはKnowledge / Applicability領域へ残す。

---

## 6.24 Historical Research Truthを保存する

Later Edge DecayやStructural Breakによって、過去の成立条件下で支持されていたResearch Resultを、

~~~text
最初から間違いだった
~~~

ことに書き換えない。

~~~text
Historically supported under C1
↓
Later market changed under C2
~~~

として両方を保存する。

> **現在使えないことと、過去に成立していたResearch Historyを消すことを分離する。**

---

## 6.25 このSectionで決めないこと

Section 6ではResearch Category Philosophyと責任境界を定義し、具体的なQualification Formula・Threshold・Risk数値・Implementationは固定しない。

以下は後続設計で扱う。

~~~text
CORE Qualification Formula
OPPORTUNITY Qualification Formula
Minimum Case Count
Independent Case Definition
Minimum Expected Value
Minimum Win Rate
OOS Period
Mechanism Confidence Threshold
Contradiction Threshold
Edge Decay Threshold
Structural Break Threshold
Revalidation Interval
Opportunity Time Window
Opportunity Decay Formula
Asymmetry Formula
Stress Scenario Count
Knowledge Lifecycle Rule
Applicability State Rule
Position Size
Leverage
Capital Allocation
Risk Budget
CORE / OPPORTUNITY Mode Risk Envelope
DB Schema
Python Class
Enum / Queue / Scheduler
~~~

Research Method詳細はResearch Architectureへ、Knowledge Lifecycle / ApplicabilityはKnowledge領域へ、Risk / Capital PhilosophyはSection 7以降へ送る。

---

## 6.26 Core Invariants

~~~text
RC-01 CORE / OPPORTUNITY are Economic Edge Character, not Knowledge Lifecycle or Current Applicability.
RC-02 ADAPTATION / REVALIDATION is a cross-temporal Research Philosophy, not a peer Edge Character.
RC-03 Repeated Profit != CORE.
RC-04 CORE != Universal / Permanent / Always Applicable.
RC-05 CORE Research includes both success conditions and failure conditions.
RC-06 Rare / Volatile / Large Move / Unknown != Opportunity.
RC-07 Opportunity Research Result != Opportunity Mode / Trade / Capital Permission.
RC-08 Opportunity disappearance may be expected closure, not Research Failure.
RC-09 Edge Character may remain UNRESOLVED.
RC-10 Unexpected Outcome != Edge Decay.
RC-11 Regime / Applicability Mismatch != Knowledge Failure.
RC-12 Edge Decay != Structural Break.
RC-13 Temporary Shock != Structural Break.
RC-14 One Contradiction != Material Change.
RC-15 Adaptation Trigger != Adaptation Conclusion.
RC-16 Overreaction and Underreaction are both Adaptation failures.
RC-17 PnL alone does not determine Edge Character or Adaptation truth.
RC-18 Adaptation Research Result != automatic Knowledge Lifecycle change.
RC-19 Later failure / decay must not erase historical Research validity.
RC-20 Section 6 does not own Capital / Risk permission.
~~~

---

# Research Category Philosophy — 一文定義

> **市場理解OSのResearch Category Philosophyは、Economic Edgeを、成立条件・Failure Boundaryを理解し再検証・再利用可能なCORE EDGEと、一時的なDistortion・Imbalance・Event・Market Structure等へ価値が依存するOPPORTUNITYとして研究しつつ、判定不能なEdge Characterを無理に分類せず、ADAPTATION / REVALIDATIONによって両者の成立条件・Economic Effect・Market Structure・Mechanismの時間変化を継続的に再研究することで、過剰適応と古いKnowledgeへの固執の双方を防ぐことである。**

簡潔には、

> **繰り返し使えるものはCOREとして育て、一時的な歪みはOPPORTUNITYとして研究し、分からないものは分からないまま残し、どれも永久の正解にせずADAPTATIONで再検証する。**



# 7. Capital / Risk Philosophy

## 7.1 このSectionの役割

Section 4では、

~~~text
Survival
= Hard Operating Boundary

Profit / Positive Economic Value
= Objective pursued inside that boundary
~~~

と定義した。

Section 6では、

~~~text
CORE EDGE / OPPORTUNITY
= Economic Edge Character
~~~

と定義し、Edge CharacterそのものはCapital / Risk Permissionを与えないことを明確にした。

Section 7では、その上位原則をCapital / Riskへ落とし、

> **市場理解OSが現在どの程度のRiskを引き受けられるか、そのRiskをどこへ割り当て、どの条件で利用し、具体的なTrade Thesisへ現在Capitalを許可できるかを判断するための最上位思想を定義する。**

とする。

Section 7は、Market Truth・Research Truth・Knowledge Validity・Current Applicability・Economic Valueを再定義する領域ではない。

~~~text
Research / Knowledge
= What is supported / known?

Decision / Economic Evaluation
= What action has economic meaning?

Capital / Risk
= May the OS take this risk now?
~~~

というAuthority分離を維持する。

---

## 7.2 CapitalとRiskを同一視しない

市場理解OSでは、

~~~text
Capital
!= Risk

Exposure
!= Risk

Loss
!= Risk
~~~

とする。

CapitalはEconomic Activityを継続するための有限資源であり、RiskはそのCapital・Operation・Recoverability等が受ける可能性のあるDamage構造である。

例えば、同じCapital Amountを利用していても、

~~~text
Leverage
Liquidity
Volatility
Correlation
Concentration
Venue / Counterparty
Execution
Tail Event
Unknown
Recoverability
~~~

等によって実際のRiskは異なり得る。

したがって、

~~~text
Capital Balance
=
Risk Capacity
~~~

とはしない。

---

## 7.3 Hard Survival BoundaryとRisk Capacityを分離する

Section 4で定義したHard Survival Boundaryは、Risk Capacityと同じものではない。

~~~text
Hard Survival Boundary
= 越えてはならないProject-level Boundary

Risk Capacity
= そのBoundaryの内側で現在引き受けられるRisk能力
~~~

とする。

Hard Survival Boundaryは、Opportunity・Mode・Profit状況等によって都合よく変更しない。

一方、Risk Capacityは、

~~~text
Market Condition
Capital Condition
Liquidity
Current Exposure
Venue状態
Operational状態
Recoverability
Material Unknown
~~~

等によって時間とともに変化し得る。

~~~text
Hard Boundary
= constitutional

Risk Capacity
= dynamic
~~~

とする。

---

## 7.4 Risk Capacity Profile

市場理解OSでは、Risk Capacityを、

~~~text
口座残高
利用可能証拠金
単一Risk Score
~~~

だけで表現しない。

Risk Capacityとは、

> **現在の市場理解OSが、主要なRisk ScopeにおいてDamageを吸収・制御し、必要な場合にRecoveryできる能力。**

とする。

その評価には、概念上、

~~~text
Capital / Financial Buffer
Liquidity / Exit Ability
Current / Aggregate Exposure
Venue / Counterparty Condition
Operational / Control Ability
Recoverability
Material Unknown
~~~

等が関係し得る。

ただし、これらを現時点で固定Schemaや固定Scoreへしない。

Risk Capacityは、

> **多面的かつScope-sensitiveな現在状態**

として扱う。

---

## 7.5 Risk Capacityを万能Scoreへ潰さない

Risk Capacityの異なるDimensionを、一つの高いScoreだけで相殺しない。

例えば、

~~~text
Capital Buffer = strong
Liquidity = strong

but

Position Visibility = lost
~~~

の場合に、

~~~text
平均すると安全
~~~

とは扱わない。

同様に、

~~~text
High Expected Value
High Win Rate
High Model Confidence
Large Capital Balance
~~~

等によって、CriticalなOperational / Liquidity / Venue / Unknown Riskを自動的に相殺しない。

> **一つのCapacity Dimensionが強いことは、別のCritical Capacity Failureを無効化する理由にならない。**

また、Risk CapacityはScopeを持ち得る。

例えば一つのVenueで障害が発生しても、それだけで無関係な全ScopeのCapacityを自動的にゼロとはしない。

影響範囲を確認し、System-level RiskとScope-specific Riskを分離して評価する方向を持つ。

---

## 7.6 Risk Capacity Contraction

Risk Capacityは、

~~~text
Capital Loss
Drawdown
Liquidity Deterioration
Exit Ability低下
Venue / Exchange Failure
Execution Control喪失
Operational Failure
Risk Observability低下
Aggregate Exposure増加
Concentration
Material Unknown
~~~

等によって縮小し得る。

ただし、

~~~text
Capital Loss %
=
Risk Capacity Reduction %
~~~

のような単純対応を上位思想として固定しない。

同様に、

~~~text
連敗回数
=
Risk Capacity Truth
~~~

とも扱わない。

Loss・Drawdown・連続Loss等は、Risk Capacityを再評価する重要Triggerになり得るが、原因として、

~~~text
Expected Variance
Edge-related Failure
Regime / Applicability Mismatch
Liquidity Shock
Execution Failure
Operational Failure
Common-Cause Exposure
Unknown
~~~

等を区別する。

> **結果の悪化だけでRisk Capacityの原因を自動確定しない。**

---

## 7.7 Risk Capacity Recovery / Recoverability

Risk Capacityが縮小した場合、

~~~text
時間が経過した
一回勝った
Priceが戻った
Capital Balanceが戻った
~~~

だけで完全Recoveryとは扱わない。

~~~text
Time Passed
!= Recovery

One Win
!= Recovery

Price Recovery
!= System Recovery

Capital Balance Recovery
!= Full Risk Capacity Recovery
~~~

とする。

Risk Capacity Recoveryは、

> **縮小原因となったCapacity Dimensionに対応するRecovery Evidenceによって確認する。**

方向を持つ。

例えば、

~~~text
Liquidity問題
→ Liquidity / Exit Abilityの回復

Venue障害
→ Order / Cancel / Position Reconciliation等の回復

Operational問題
→ Monitoring / Control / State Visibility等の回復
~~~

のように、原因とRecovery Evidenceを対応させる。

Risk CapacityはMaterial Riskに対して速やかに縮小できる一方、関連するRecovery Evidenceが得られた後まで根拠なく保守状態を固定し続けない。

必要に応じて段階的Recoveryを許容するが、具体Stage・Threshold・Cooldownは後続設計で定義する。

---

## 7.8 Risk Budget

Risk CapacityとRisk Budgetを分離する。

~~~text
Risk Capacity
= 現在どの程度Riskを吸収できるか

Risk Budget
= そのCapacityをどのScopeへどの程度割り当ててよいか
~~~

とする。

Risk Budgetは、

~~~text
Asset
Market
Venue
Edge Family
Risk Posture
Time Window
Portfolio Scope
~~~

等へ将来割り当てられる可能性を持つ。

ただし具体的なAllocation Unit・Formula・Hierarchyは後続Risk Architectureで定義する。

重要なのは、

~~~text
Risk Budget
cannot create Risk Capacity
~~~

ことである。

Risk Budgetの合計や再配分によって、Systemが実際に吸収可能なRisk能力そのものを増加させてはならない。

---

## 7.9 Risk Budgetは使用目標ではない

Risk Budgetは、

~~~text
使わなければならない金額
最大化すべきExposure
Profit Target達成用のQuota
~~~

ではない。

~~~text
Unused Risk Budget
!= Inefficiency

Risk Budget Available
!= Trade Permission
~~~

とする。

Economic Opportunityが存在しない場合、Current Applicabilityが成立しない場合、Risk Envelopeを満たさない場合等には、Budgetを利用しないことが正常な判断になり得る。

また、Risk Capacityが縮小した場合、過去に割り当てられたRisk Budgetを永久の利用権として扱わない。

~~~text
Capacity Contraction
may require
Budget Re-evaluation
~~~

とする。

---

## 7.10 Risk Posture Philosophy

市場理解OSは、すべてのEconomic Edgeを完全に同一のRisk条件で扱う必要はない。

そのため、将来のRisk / Capital Governanceでは、

~~~text
CORE RISK POSTURE
OPPORTUNITY RISK POSTURE
~~~

等の異なるRisk Postureを許容する。

人間向けには、

~~~text
CORE MODE
OPPORTUNITY MODE
~~~

と表現できる。

ただし正式な意味は、

> **異なるEconomic Edge CharacterやMarket Contextを、どのRisk条件の下で扱うかを示すRisk Posture Profile**

である。

~~~text
Risk Posture
!= Economic Edge Character
~~~

とする。

---

## 7.11 CORE RISK POSTURE

CORE RISK POSTUREは、

> **成立条件・Failure Boundary・再利用可能性等が継続的に研究されているCORE EDGEを扱うための通常Risk Posture。**

とする。

ただし、

~~~text
CORE
!= SAFE

CORE RISK POSTURE
!= Zero-Risk Mode
~~~

である。

CORE EDGEでも、

~~~text
Tail Risk
Liquidity Dependency
Leverage Sensitivity
Correlation
Concentration
Venue Risk
~~~

等が大きい可能性がある。

COREであることだけを理由に、大きいRisk Budget・Exposure・Leverageを自動的に許可しない。

---

## 7.12 OPPORTUNITY RISK POSTURE

OPPORTUNITY RISK POSTUREは、

> **特定のTemporary Distortion・Imbalance・Event・Market Structure等へEconomic Valueが依存するOpportunityを、通常Postureとは異なるRisk条件で扱うための限定Risk Posture。**

とする。

ただし、

~~~text
OPPORTUNITY RISK POSTURE
!= Aggressive Mode

OPPORTUNITY
!= Higher Risk Permission
~~~

である。

Opportunityでは、

~~~text
Upside
Downside
Liquidity
Exit Ability
Time Decay
Tail Risk
Unknown
Failure Boundary
~~~

等によって、COREより大きいExposureが合理的な場合もあれば、逆に小さいExposureやNO TRADEが合理的な場合もある。

> **Opportunity Risk Postureは「Riskを増やすMode」ではなく、「Riskの扱い方をOpportunityの構造へ合わせるPosture」である。**

---

## 7.13 Edge CharacterとRisk Postureを分離する

Section 6の、

~~~text
CORE EDGE
OPPORTUNITY
~~~

はEconomic Edge Characterである。

Section 7の、

~~~text
CORE RISK POSTURE
OPPORTUNITY RISK POSTURE
~~~

はRisk Treatmentである。

したがって、

~~~text
CORE EDGE
!= CORE RISK POSTURE Permission

OPPORTUNITY
!= OPPORTUNITY RISK POSTURE Permission
~~~

とする。

Economic Edge Characterが特定されたことだけで、Risk Posture Entry・Capital Permission・Exposure Amountを自動決定しない。

Risk Postureは、Current Applicability・Economic Evaluation・Current Risk Capacity・Aggregate Risk・Risk Policy等を踏まえて評価される方向を持つ。

---

## 7.14 Risk PostureはScope-boundである

Risk Postureを、一つのGlobal System Switchとして扱わない。

~~~text
SYSTEM MODE
= CORE only

or

SYSTEM MODE
= OPPORTUNITY only
~~~

とは固定しない。

市場理解OSでは、異なるRisk Scopeに、

~~~text
CORE RISK POSTURE
+
OPPORTUNITY RISK POSTURE
~~~

が同時に存在することを許容できる。

ただし、

> **複数のRisk Postureが存在しても、それぞれが独立した無限Risk Capacityを持つわけではない。**

全てのRisk Postureは共通のSystem Risk CapacityとHard Survival Boundaryの制約を受ける。

また、

~~~text
Different Risk Posture
!= Independent Risk
~~~

とする。

---

## 7.15 Mode Shopping / Risk Rule Escapeを禁止する

Risk Postureは、Risk制約を回避するためのSemantic Label変更に利用しない。

例えば、

~~~text
CORE RISK POSTUREではRisk条件に抵触
↓
Opportunityと再Label
↓
OPPORTUNITY RISK POSTUREへ変更
↓
同じRiskを許可
~~~

というMode Shoppingを禁止方向とする。

~~~text
Risk Rejection
cannot be solved
by semantic relabeling
~~~

とする。

Risk Postureは、

~~~text
Risk Capacityを増やす
Hard Survival Boundaryを緩和する
Research Truthを書き換える
Knowledge Validityを書き換える
Current Applicabilityを書き換える
Economic Valueを書き換える
UNKNOWNをSAFEへ変える
既存Exposureを消す
Consumed Risk Historyを消す
~~~

Authorityを持たない。

> **Risk PostureはRisk Treatmentを変えるが、Risk Truthや上流Truthを変更しない。**

---

## 7.16 Risk Envelope

Risk Envelopeとは、

> **あるRisk Scope / Risk Posture / Capital Requestが守らなければならないRisk条件の集合。**

とする。

Risk Envelopeには将来、概念上、

~~~text
Exposure
Leverage
Liquidity
Exit Ability
Concentration
Correlation
Venue Condition
Tail Risk
Time Dependency
Unknown
~~~

等が関係し得る。

ただし、現時点で具体Field・Threshold・Score・Formulaを固定しない。

また、

~~~text
Risk Posture
!= Single Risk Multiplier
~~~

とする。

COREを 1x、Opportunityを 3x とするような単一倍率だけでRisk Posture全体を定義しない。

---

## 7.17 Risk BudgetとRisk Envelopeを分離する

Risk BudgetとRisk Envelopeは同じものではない。

~~~text
Risk Budget
= How much risk may this scope consume?

Risk Envelope
= Under what risk conditions may this scope operate?
~~~

とする。

したがって、

~~~text
Budget Available
!= Envelope PASS

Envelope PASS
!= Budget Available
~~~

である。

Risk Budgetが残っていてもRisk Envelopeを満たさなければCapital Permissionは与えない方向を持つ。

同様に、Risk Envelope内であっても利用可能Risk Budgetがなければ新しいRiskを取らない方向を持つ。

---

## 7.18 Aggregate / Common-Cause Risk

Riskを単一Trade・単一Positionだけで評価しない。

~~~text
Different Position
!= Independent Risk
~~~

とする。

例えば、

~~~text
BTC Long
ETH Long
SOL Long
~~~

が別Positionであっても、

~~~text
同一Crypto Beta
同一Market Direction
同一Macro Factor
同一Liquidity Shock
同一Venue
同一Failure Source
~~~

等を共有していれば、System全体として大きなCommon-Cause Riskを持つ可能性がある。

同様に、

~~~text
CORE RISK POSTURE
+
OPPORTUNITY RISK POSTURE
~~~

へ分かれていることだけでRisk Independenceを仮定しない。

> **Risk Capacity・Risk Budget・Capital Permissionは、個別RiskだけでなくAggregate / Sequence / Common-Cause Riskを考慮する方向を持つ。**

具体的なCorrelation・Portfolio Risk・Stress Formulaは後続設計で定義する。

---

## 7.19 Material Unknown

Section 4の、

~~~text
UNKNOWN
!= SAFE
~~~

をCapital / Riskへ適用する。

Unknownが存在するだけで全Riskを自動的に禁止するわけではない。

一方で、

~~~text
Maximum Downside UNKNOWN
Exit Route UNKNOWN
Actual Exposure UNKNOWN
Position State UNKNOWN
Venue Condition UNKNOWN
~~~

等のMaterial Unknownを、Lossがまだ発生していないことだけを理由に安全扱いしない。

> **Material Unknownは、現在利用可能なRisk Capacity・Risk Envelope・Capital Permissionを縮小・保留する理由になり得る。**

Unknownは件数だけで評価せず、

~~~text
何がUnknownか
どのRisk Scopeへ影響するか
Failure Pathへどう影響するか
Recoverabilityへどう影響するか
~~~

を見る。

具体的Materiality Ruleは後続設計で定義する。

---

## 7.20 Capital Permission

Capital Permissionとは、

> **Current-use validなTrade Thesisに基づき、現在のRisk Capacity・Risk Budget・Risk Posture・Risk Envelope・Aggregate Exposure・Material Unknown等を踏まえて、そのCapital / Exposure Riskを現在許可できるかを判断するCapital Governance結果。**

とする。

Capital Permissionは、

~~~text
Decision Candidate
Economic Value
Candidate Advancement
Trade Thesis
~~~

そのものではない。

基本関係は、

~~~text
Decision / Economic Evaluation
↓
Trade Thesis
↓
Capital / Risk Authority
↓
Capital Permission
~~~

とする。

Capital / Risk領域は、上流のMarket Judgment・Economic Value・Research Truthを都合よく書き換えてCapital Permissionを成立させてはならない。

---

## 7.21 Capital Permissionと他Authorityを分離する

Capital Permissionは、

~~~text
Knowledge Validity
Current Applicability
Economic Value
Candidate Advancement
Trade Thesis
Execution Permission
~~~

と分離する。

~~~text
Knowledge is valid
!= Capital Permission

Trade Thesis exists
!= Capital Permission

Capital Permission
!= Execution Permission
~~~

とする。

Capital / Risk側がBLOCKしても、

~~~text
Knowledge is false
Trade Thesis is invalid
Economic Value is false
~~~

ことを自動的に意味しない。

同様にCapital Permissionが与えられても、その後のExecution / Runtime Safetyが、

~~~text
Exchange Failure
Liquidity Collapse
Spread Explosion
Order Route Failure
Actual Exposure Risk
~~~

等によってExecutionを停止できる方向を持つ。

> **Capital Permissionは「Risk側として現在許可できる」という判断であり、必ずOrderを実行する命令ではない。**

---

## 7.22 Capacity ContractionとExisting Exposure

Risk Capacityは、Position保有中にも縮小し得る。

例えば、

~~~text
Existing Exposure Risk
>
Current Available Risk Capacity
~~~

となる可能性がある。

この状態を理由に、

~~~text
即時
全Position
Market Exit
~~~

を上位原則として強制しない。

Liquidity Collapse等では、Blind Forced Liquidation自体がDamageを拡大する可能性がある。

したがって、

~~~text
Capacity Contraction
!= Automatic Forced Liquidation

No New Risk
!= Immediate Exit
~~~

とする。

Risk Capacity縮小によって既存Exposureが過剰となった場合、

~~~text
New Risk抑制
Existing Exposure再評価
Aggregate Risk再評価
Fast Safety / Defense
~~~

へ進み、利用可能な選択肢の中からSurvival Damageを抑える対応を取れる方向を持つ。

具体的なREDUCE / HOLD / EXIT Policyは後続Risk / Runtime / Execution設計で定義する。

---

## 7.23 Risk Governance ResultとPnLを分離する

Risk判断の品質をPnLだけで判定しない。

~~~text
Profit
!= Risk Governance Success

Loss
!= Risk Governance Failure
~~~

とする。

例えば、

~~~text
Risk Rule違反
↓
結果はProfit
~~~

であっても、Risk Decision自体が正しかったとは限らない。

逆に、

~~~text
定義されたRisk Boundary内
↓
正常なMarket VarianceでLoss
~~~

であれば、そのLossだけを理由にRisk Governance Failureとはしない。

Post-Analysisでは可能な限り、

~~~text
Economic Outcome Quality
Risk Decision Quality
Edge / Knowledge Quality
Execution Quality
~~~

を分離して評価する方向を持つ。

---

## 7.24 Recoveryは過去のPermissionを自動復活させない

Risk Capacityが回復しても、

~~~text
Previous Risk Budget
Previous Capital Permission
Previous Opportunity
Previous Risk Posture Permission
~~~

を自動的に復活させない。

~~~text
Capacity Recovery
!= Automatic Budget Restoration

Capacity Recovery
!= Old Capital Permission Revival

Capacity Recovery
!= Opportunity Recovery
~~~

とする。

Recovery後には、

~~~text
Current Market Context
Current Applicability
Current Economic Condition
Current Opportunity existence
Current Risk Budget
Current Aggregate Exposure
Current Material Unknown
~~~

等を現在時点で再評価する。

一度許可されたCapital Permissionを永久Tokenとして扱わない。

~~~text
Approved Once
!= Approved Forever
~~~

とする。

---

## 7.25 このSectionで決めないこと

Section 7ではCapital / Risk Philosophyと上位責任境界を定義し、具体的なRisk数値・Formula・Runtime Contract・Implementationは固定しない。

以下は後続Risk / Capital / Decision / Runtime設計で扱う。

~~~text
Single Trade Risk %
Maximum Drawdown %
Daily / Weekly Loss Limit
Leverage Limit
Exposure Limit
Capital Reserve Ratio
Protected Reserve Rule
Position Size Formula
Stop Loss Rule
VaR / CVaR
Correlation Formula
Portfolio Risk Formula
Exchange Concentration Limit
Tail Risk Budget

Risk Capacity exact dimensions
Risk Capacity Score / Aggregation Formula
Capacity Contraction Threshold
Capacity Recovery Threshold
Recovery Stage
Cooldown Duration

Risk Budget Allocation Formula
Budget Reallocation Rule
Budget Borrowing Rule

CORE RISK POSTURE Entry / Exit Threshold
OPPORTUNITY RISK POSTURE Entry / Exit Threshold
Mode-specific Risk Envelope
Risk Posture State Machine

Risk Envelope Field / Threshold
Capital Permission TTL
Capital Permission Contract
Over-Capacity State Definition

DB Schema
Python Class
Enum
Queue
Scheduler
Runtime Implementation
~~~

Section 7は、

> **Riskをどのように考え、どのAuthorityを分離し、何を越えてはならないか**

を固定する。

具体的に「何%」「何倍」「何分」「何件」で判定するかは後続設計へ送る。

---

## 7.26 Core Invariants

~~~text
CR-01 Capital != Risk; Risk Capacity != Capital Balance.

CR-02 Risk Capacity is multidimensional and scope-sensitive.

CR-03 Critical failure in one Capacity dimension cannot be silently offset by strength in another.

CR-04 Risk Capacity != Risk Budget; Budget allocates Capacity and cannot create it.

CR-05 Unused Risk Budget != Inefficiency; Risk Budget != Trade Permission.

CR-06 Economic Edge Character != Risk Posture.

CR-07 Risk Posture is scope-bound, not one global system switch.

CR-08 Risk Posture cannot create Capacity, rewrite upstream truth, convert UNKNOWN to SAFE, erase existing Risk, or bypass the Hard Survival Boundary.

CR-09 Risk Budget != Risk Envelope; Budget governs allocation quantity, Envelope governs admissible risk conditions.

CR-10 Risk Posture != Single Risk Multiplier.

CR-11 Different Positions / Postures != Independent Risk; Aggregate / Common-Cause Risk must remain visible.

CR-12 Capital Permission is downstream of a current-use valid Trade Thesis and does not rewrite Decision / Economic truth.

CR-13 Capital Permission is time-, scope-, and exposure-specific; Capital Permission != Execution Permission.

CR-14 Risk Capacity Contraction != Knowledge / Edge / Research Failure; Capital / Risk BLOCK does not rewrite upstream truth.

CR-15 Capacity Contraction != automatic Forced Liquidation; existing Exposure must be re-evaluated rather than blindly exited.

CR-16 Risk Capacity Recovery requires evidence relevant to the failed Capacity dimension; Recovery does not automatically restore Budget, old Permission, or Opportunity.
~~~

---

# Capital / Risk Philosophy — 一文定義

> **市場理解OSのCapital / Risk Philosophyは、長期生存という共通Hard Survival Boundaryの内側で、Capital残高だけではなくLiquidity・Exposure・Venue・Operational Control・Recoverability・Material Unknown等を含む現在のRisk Capacityを多面的に評価し、そのCapacityを必要なScopeへRisk Budgetとして割り当て、CORE / OPPORTUNITY等のRisk PostureとRisk EnvelopeによってRisk条件を管理し、Current-use validなTrade Thesisへ今そのCapital / Exposure Riskを許可できるかを判断することで、Economic Opportunityを追求しながらも、一時的利益・Mode変更・単一Metricによって市場理解OSの継続能力を賭けないことである。**

簡潔には、

> **利益がありそうだから賭けるのではなく、今のOSが耐えられ、制御でき、壊れても戻れるRiskだけを選んでCapitalを出す。**

---

# 8. Knowledge / Data Asset Philosophy

## 8.1 このSectionの役割

Section 1では、市場理解OSがResearch Note・Evidence・Research Result・Failure・Knowledge・Decision History等を再利用可能なResearch Assetとして蓄積しながら、すべてのRaw Dataを永久保存するのではなく、将来の再検証・再現・説明に必要なEvidence・Context・Version・Historyを保持する方向を定義した。

Section 8では、その上位方針をKnowledge / Data Assetへ落とし、

> **将来のResearch・Revalidation・Explanation・Audit・Failure Learningに必要なIdentity・Meaning・History・Material Dependency・Required Fidelityを失わせず、同時に全Data・全History・全Physical Representationの永久保存も要求しないための長期保存哲学を定義する。**

とする。

市場理解OSは、

~~~text
保存量が多い
=
Knowledge / Research能力が高い
~~~

とは考えない。

同様に、

~~~text
最新版だけ残す
=
十分なKnowledge管理
~~~

とも考えない。

基本方向は、

~~~text
Preserve what must remain understandable and reusable.

Do not preserve every physical representation forever.
~~~

とする。

---

## 8.2 Semantic OwnershipとResearch Asset Boundary

ArtifactのSemantic IdentityおよびHistorical Factは、それを生成・管理するOriginal Domainが所有する。

例えば、

~~~text
Raw Observation
Derived Feature
Research Result
Knowledge Version
Decision / Trade Thesis
Execution Outcome
~~~

等の身分を、Section 8がPreservation上の都合によって別のSemantic Objectへ再定義しない。

したがって、

~~~text
Research Asset designation
!= Semantic Object Type
~~~

とする。

Research Asset は、

> **将来のResearch・Revalidation・Explanation・Decision Review・Failure Learning等へ再利用価値を持つArtifact・Context・History・Relationshipを横断的に捉えるための上位概念**

として扱う。

Evidenceについても、Evidence Channel・Source・Role・Time・Version等のResearch上の意味論はResearch Domainが所有する。

Section 8は、それらがMaterialに利用された場合に生じるPreservation Requirementを扱う。

---

## 8.3 PreservationとValidity / Applicability / Authorityを分離する

市場理解OSでは、

~~~text
Stored
!= Valid
!= Applicable
!= Authorized
~~~

とする。

Artifactが保存されていることは、

~~~text
Research上正しい
Knowledgeとして有効
Current MarketでApplicable
Decisionで利用可能
Trade可能
Risk / Capital許可済み
~~~

であることを自動的には意味しない。

同様に、

~~~text
RETIRED
!= DELETE

SUPERSEDED
!= ERASED

NOT_APPLICABLE
!= RETIRED
~~~

とする。

Lifecycle・Validity・Applicability・Decision / Production Authorityと、Preservation Requirement / Retention判断を混同しない。

---

## 8.4 Preservation Obligation

Preservation Obligationとは、

> **ArtifactまたはそのMaterialなContextについて、削除・圧縮・Migration・Replacement・Correction等によって、将来必要なResearch・Revalidation・Explanation・Audit・Failure Learning能力をMaterialに破壊してはならないという保存上の義務**

である。

~~~text
Preservation Obligation
!= Retention期間
!= Storage場所
!= Backup数
!= File Format
!= DB Schema
~~~

とする。

また、

~~~text
Assetとして価値がある
=
永久に同じPhysical Dataを保持する
~~~

とも限らない。

Preservationの目的は、

> **同じPhysical Bytesを永久に残すことではなく、必要なMeaning・History・Relationship・Fidelityを失わせないこと**

とする。

---

## 8.5 Material Dependency

Preservation Requirementを判断する際は、Material Dependencyを考慮する。

Material Dependencyとは、

> **あるArtifact、Research Result、Knowledge Version、Decision等について、そのDependencyが失われたり変更された場合に、Meaning・Reproducibility・Historical Interpretation・Explanation・Auditability等へMaterialな影響を与える依存関係**

をいう。

ただし、

~~~text
Material Dependency
!= Every Reference
!= Operational Dependencyそのもの
!= Evidence Roleそのもの
!= Version Lineageそのもの
~~~

とする。

また、

~~~text
Material Dependency
→ 全Upstream Ancestorを永久Full Retention
~~~

とはしない。

必要なのは、Materialな依存関係を将来正しく理解・追跡するためのPreservationであり、Dependency Chain全体の無制限Retentionではない。

---

## 8.6 Preservation Requirement

Preservation Requirementとは、

> **あるArtifactまたはContextについて、将来必要なPreservation Capabilityを維持するために、何を失ってはいけないか**

を表す。

Requirementを一つの万能Scoreへ潰さない。

対象に応じて、例えば、

~~~text
Identity Continuity
Semantic Interpretability
Integrity
Retrievability
Sufficient Provenance
Historical State Distinguishability
Temporal / As-Of Interpretability
Material Dependency Reference Continuity
Required Preservation Fidelity
~~~

等を必要な範囲で組み合わせる。

全Artifactへ同一Requirementを要求しない。

Required Preservation Fidelityも、

~~~text
Exact Content
Exact Historical State
Method Reproduction
Result Verification
Historical Reconstruction
Explanation
~~~

等のどこまで必要かをContextごとに判断する。

---

## 8.7 Preservation AssessmentとReassessment

Preservation Assessmentは、

> **Original Domainが所有する事実、Material / Historical Reliance、Projectとして維持すべきCapability、Replaceability / Reconstructability、Hard Constraint、Material Unknown等から、そのContextでApplicableなPreservation Requirementを導出する保存上の解釈**

とする。

Preservation Assessment自身は、

~~~text
Research Truth
Knowledge Truth
Applicability
Decision Authority
Risk Authority
~~~

を生成・変更しない。

必要なFuture Capabilityは、

~~~text
Project Charterで要求される長期Capability
+
Original DomainがMaterialに必要とするCapability
~~~

を基礎とする。

単に、

~~~text
いつか役に立つかもしれない
~~~

という曖昧な可能性だけで、無制限Retentionを正当化しない。

Preservation Requirementは一度決めて永久固定するものではない。

~~~text
Material Dependency
Historical Reliance
Research利用
Replacement
Revalidation
Hard Constraint
~~~

等の変化に応じてReassessment可能とする。

ただし、

~~~text
古い
高コスト
現在使っていない
~~~

という理由だけでRequirementを低下させない。

---

## 8.8 Preservation Equivalence

市場理解OSは長期運用において、

~~~text
Migration
Replacement
Reacquisition
Compression
Historical Representation変更
~~~

を許容する。

別Representationが、

> **Original Artifactに対するApplicable Preservation RequirementをRequired Fidelityで維持できる場合**

Preservation上の代替候補となり得る。

したがって、

~~~text
Preservation Equivalence
!= Physical Equality
~~~

とする。

File Format・Storage Technology・Provider等が変化しても、

~~~text
Identity
Meaning
Required Precision
Historical / Temporal Context
Material Reference
Integrity
Retrievability
~~~

等のApplicable Requirementを満たせるなら、Preservationを維持できる。

---

## 8.9 Historical SubstitutionとIrreversible Destruction

Replacement・Migration・Reacquisitionによって、過去をSilentに書き換えてはならない。

特に、

~~~text
Reacquirable
!= Historically Identical

Current Best Historical Data
!= Past-used Historical Data

Replacement
!= Historical Rewrite
~~~

とする。

同じSource・Symbol・期間から再取得できても、Correction・Backfill・Cleaning・Schema変更等によって、過去に実際に利用したDataと同一とは限らない。

また、

~~~text
Preservation Equivalence
!= Automatic Destruction Permission
~~~

とする。

Original Artifactへの不可逆な破棄は、少なくとも、

~~~text
Applicable Preservation Requirement
Required Fidelity
Historical Identity / Reliance
Material Dependency Reference Continuity
Integrity / Retrievability
Material Unknown
Original Physical FormそのものへのRequirement
~~~

等を確認した上で扱う。

具体的なApproval Workflow、Gate、State、Enumは後続設計で定義する。

---

## 8.10 Historical Truth

市場理解OSはCurrent Stateを更新し続ける。

しかし、その更新によってMaterialなPast TruthをSilentに書き換えてはならない。

基本原則は、

~~~text
Current Truth
!= Historical Truth

Current Best
!= Past Used

Known Now
!= Known Then

Historical Fact
!= Later Interpretation
~~~

とする。

DatasetがCorrectionされ、KnowledgeがSUPERSEDED / RETIREDされ、後のCausal Researchでより良い説明が得られても、

> **過去に実際に何が存在し、何が使用され、何がKnown / Unknownであり、どのStateにあったか**

は必要な範囲で区別可能にする。

Later InterpretationはHistorical Factを補強・訂正・再評価できるが、

~~~text
当時も現在と同じことを知っていた
~~~

ことにはしない。

---

## 8.11 Material Historical Preservation

Historical Preservationは、

~~~text
全Log
全Field変更
全Calculation
全Intermediate State
~~~

を永久保存することではない。

対象Historyの喪失が、

~~~text
Research
Revalidation
Decision Review
Failure Learning
Material Dependency
Historical Meaning
~~~

のMaterialな誤解につながる場合、そのHistoryをPreservation対象とする。

したがって、

~~~text
Historical Preservation
!= Exhaustive Event Sourcing
~~~

とする。

Detailed Historyは、Applicable Preservation RequirementとRequired Historical Fidelityを維持できる場合、圧縮・縮約・別Representationへの変更を許容する。

ただし、Materialな、

~~~text
Historical Identity
Historical State
Historical Reliance
Temporal Context
Known / Unknown distinction
~~~

等を失う縮約はPreservation Successとはみなさない。

---

## 8.12 Physical DeletionとHistorical Continuity

~~~text
Physical Deletion
!= Historical Non-Existence
~~~

とする。

Material ArtifactのPhysical Contentが正当に削除された場合でも、Applicable Preservation Requirementに応じて、

~~~text
Artifactが存在したこと
Artifact Identity / Meaning
Material Historical Role
Material Reliance
Correction / Replacement Relation
Known Limitation
~~~

等を残し得る。

Physical Representationを削除したことを理由に、

~~~text
最初から存在しなかった
~~~

状態へ書き換えない。

---

## 8.13 Retention / Disposal Philosophy

市場理解OSは、

~~~text
一度価値があった
→ 永久保存
~~~

とはしない。

RetentionはApplicable Preservation Requirementに基づく。

Requirementが維持される範囲で、

~~~text
Detailed Content
↓
Reduced / Compressed Representation
↓
Historical Identity / Material Relation
~~~

等へ縮小できる。

一方、

~~~text
Age
Storage Cost
No Current Use
RETIRED
SUPERSEDED
~~~

だけではRetention終了理由としない。

Costは、

~~~text
何を失ってよいか
~~~

を単独では決めず、

~~~text
どのようにRequirementをより効率的に満たすか
~~~

を検討する理由として扱う。

---

## 8.14 Requirement ReductionとRetention Reduction

以下を分離する。

### Requirement Reduction

必要なPreservation Capability自体が正当に低下すること。

例:

~~~text
Exact Reproduction Required
↓
Historical Explanationで十分
~~~

### Retention Reduction

必要なPreservation Capabilityは維持したまま、より小さい・効率的なRepresentationで満たすこと。

例:

~~~text
Raw JSON
↓
Preservation-equivalent Representation
~~~

Storage Costや管理都合を理由に、

~~~text
必要だったCapabilityそのものを
不要だったことにする
~~~

ことはしない。

---

## 8.15 Remaining Historical ObligationとNo Remaining Material Preservation Obligation

Detailed ContentへのRetention Requirementが終了しても、

~~~text
Artifactが存在した
Researchが利用した
DecisionがMaterialに依存した
Correction / Replacementされた
~~~

等のHistorical Identity / Relationが将来必要なら、Preservation Obligationは終了していない。

したがって、

~~~text
Historical Identity / Relation Only
!= No Preservation Obligation
~~~

とする。

No Remaining Material Preservation Obligation とみなせるのは、

> **現在合理的に把握可能な範囲で、そのArtifactまたはHistorical Informationについて、MaterialなIdentity・Meaning・Historical State・Dependency・Provenance・Research・Revalidation・Explanation・Audit・Failure Learning・Original Physical Formその他のPreservation Requirementが残っておらず、未解決のMaterial Unknownまたは保持を要求するHard Constraintも存在しない場合**

とする。

また、

~~~text
Requirement Unsatisfied
!= Requirement Ended
~~~

を維持する。

Artifactを失ったこと、または保持不能になったことを理由に、Preservation Requirement自体が存在しなかったことにはしない。

---

## 8.16 Hard Constraints

市場理解OSは、Legal・Licensing・Contract・Regulatory等のHard Constraintを無視しない。

Hard Constraintには、

~~~text
Retentionを要求するConstraint
~~~

と、

~~~text
Disposalを要求するConstraint
~~~

の両方があり得る。

ConstraintによってFull Preservationが不可能な場合でも、可能な範囲で、

~~~text
Provenance
Derived Result
Research Context
Material Dependency
Historical Identity
Known Limitation
~~~

等を保持する。

特に、

~~~text
Forced Disposal
!= Preservation Obligation End
~~~

とする。

必要だった情報をConstraintによって保持できなかった場合、そのLimitationを隠さない。

---

## 8.17 Technology Replaceability

市場理解OSは長期運用の中で、

~~~text
Data Source
API
DB / Storage
File Format
AI Model
Infrastructure
~~~

等を変更可能とする。

TechnologyやPhysical Representationを永久固定しない。

基本原則は、

> **Technologyは交換可能とする。ただし、Applicable Preservation Requirementが要求するMeaning・History・Material Reliance・Required Fidelityを破壊しない。**

とする。

---

## 8.18 このSectionで決めないこと

Section 8ではKnowledge / Data Assetの長期保存哲学と上位責任境界を定義し、具体的なRetention Policy・Contract・Implementationは固定しない。

以下は後続Detailed Design / Contract / Implementationで扱う。

~~~text
具体Retention期間

Storage / DB / File Format

Archive / Compression / Backup / Replication

Delete / Purge / Migration Workflow

具体Schema / Contract / Enum / State Machine

Preservation / Materiality Score

具体Legal / Regulatory保持期間

Python / Runtime Implementation
~~~

Section 8は、

> **何をなぜ失ってはいけないか、Representationをどの条件で変更できるか、そしてRetentionをどの条件で縮小・終了できるか**

という上位哲学を固定する。

---

## 8.19 Core Invariants

~~~text
KA-01 Research Asset designation != Semantic Object Type.

KA-02 Semantic / Historical Truth remains owned by the original domain.

KA-03 Stored != Valid != Applicable != Authorized.

KA-04 RETIRED != DELETE; SUPERSEDED != ERASED.

KA-05 Current Best != Past Used.

KA-06 Known Now != Known Then.

KA-07 Historical Fact != Later Interpretation.

KA-08 Physical Existence != Preservation Success.

KA-09 Physical Deletion != Historical Non-Existence.

KA-10 Reacquirable != Historically Identical.

KA-11 Material Dependency != Full Transitive Retention.

KA-12 Preservation Equivalence != Destruction Permission.

KA-13 Equivalence Satisfaction != Preservation Obligation End.

KA-14 Unsatisfied Requirement != Requirement Ended.

KA-15 Age / Cost / No Current Use alone do not authorize disposal.

KA-16 Technology may change; required meaning and history must survive.
~~~

---

# Knowledge / Data Asset Philosophy — 一文定義

> **市場理解OSのKnowledge / Data Asset Philosophyは、Data・Research Result・Knowledge・Failure・Decision / Outcome History等のSemantic / Historical AuthorityをOriginal Domainに残したまま、将来のResearch・Revalidation・Explanation・Audit・Failure Learningに必要なIdentity・Meaning・History・Material Dependency・Required Fidelityを失わせず、Current TruthによってPast Truthを書き換えず、同時に全DataやPhysical Representationの永久保存を要求せず、Applicable Preservation Requirementが維持される範囲でMigration・Replacement・Compression・Retention Reduction・Disposalを可能にする長期保存哲学である。**

簡潔には、

> **必要な意味と研究史は失わない。しかし、同じPhysical Dataを永久に抱え続けることもしない。**

---

# 9. Extensibility / Replaceable Capability Philosophy

## 9.1 このSectionの役割

市場理解OSは、長期間の運用を前提とする。

その間には、

- Data Sourceの変更
- Provider / APIの変更
- 新しいObservationの追加
- 新しいDerived Feature / Metricの追加
- Research Methodの改善
- Research Outputの追加
- 新市場への拡張
- Failure・Degradation・Replacement
- 市場構造そのものの変化

が発生し得る。

したがって、市場理解OSは現在のData・Metric・Provider・Research Method・Technologyを永久固定するSystemにはしない。

一方で、変更しやすさを理由として、

- Semanticを曖昧にする
- Research Integrityを省略する
- Authority Boundaryを迂回する
- Historical Truthを書き換える
- Failure Impactを隠す
- 市場ごとに別OSへ分裂する

ことも許さない。

Section 9では、

> **市場理解OSとして守るべき意味・責任・Integrityを維持したまま、変化するCapabilityを追加・交換・Version変更できるための上位Extensibility原則**

を定義する。

具体的なPlugin Class、Registry、Python Interface、DB Schema、JSON Contract、Version Numbering、Failover Implementation等はこのSectionでは固定しない。

---

## 9.2 Extensibilityの正式定義

市場理解OSにおけるExtensibilityとは、

> **Project-level Mission・Semantic Boundary・Authority Boundary・Research Integrity・Historical / Version Principle・Change / Failure Principle・Survival Principleを維持したまま、市場・Data Source・Measurement・Research Need等の変化へ対応するCapabilityを追加・交換・Version変更でき、その変更によるMaterial Impactを必要な範囲へ伝えながら、無関係なCore Responsibility全体の再設計を要求しない能力**

とする。

簡潔には、

> **OSの意味と責任を壊さず、必要な能力だけを後から足し、替え、進化させられること。**

とする。

Extensibilityは、

~~~text
Extension数を増やすこと
Plugin数を増やすこと
Technologyを増やすこと
Automation率を高めること
~~~

自体を目的としない。

---

## 9.3 Core / Extension Boundary

### 9.3.1 Core

Section 9におけるCoreとは、

> **対象市場・Data Source・Metric・Research Method等が変化しても、市場理解OS全体として維持すべきProject-level Mission・Semantic Ownership / Boundary・Authority Boundary・Integrity / Survival Invariant・共通Responsibility Principle**

をいう。

Coreは、

~~~text
重要なもの全て
広く使われるもの全て
core/ Folder
共通Python Class
現在存在するArchitecture全体
~~~

を意味しない。

したがって、

~~~text
Important
!= Core

Widely Used
!= Core

Shared Usage
!= Core
~~~

とする。

### 9.3.2 Extension

Extensionとは、

> **Coreを維持したまま、特定のMarket・Data・Measurement・Research Need等へ対応するために追加・交換・Version変更できるCapability**

をいう。

Extension候補には、

~~~text
Data Source
Observation
Derived Feature / Metric
Research Method
Research Output / Representation
Market-specific Capability
~~~

等を含み得る。

ただし、この一覧を閉じたEnumとはしない。

### 9.3.3 Extension Change

Extension Changeとは、

> **Core Semantic・Authority・Integrityを変更せず、Extension Capabilityを局所的に追加・交換・Version変更する変更**

をいう。

### 9.3.4 Core Change Candidate

新Capabilityが既存CoreのSemantic / Authority / Integrity Boundaryでは正しく表現できず、

~~~text
Project Mission
Semantic Ownership / Meaning
Authority Boundary
Research Integrity
Survival Invariant
複数Domain共通のResponsibility
~~~

そのものを変更する必要がある場合、その変更をExtension内部へ隠さない。

その場合は、

> **Core Change Candidate**

として上位設計へEscalateする。

Section 9自身はCore Changeを最終承認しない。

具体的なChange Governanceは後続Sectionで扱う。

---

## 9.4 Semantic / Authority / Adoption Boundary

Extensionを追加できることと、そのExtensionが何者であり、誰が何を決め、どこで利用されるかは分離する。

### Semantic

Semanticとは、

> **Artifact・Extension・Outputが何であり、何を意味し、どのDomain上の身分として扱われるか**

を表す。

Semantic Identityは、

~~~text
Validity
Quality
Evidence Strength
Current Applicability
Authorization
~~~

とは別である。

### Authority

Authorityとは、

> **特定のResponsibility / Questionについて、その判断を市場理解OS上の正式判断として成立させる責任境界**

をいう。

Authorityは、

> 他DomainのSemanticやResearch Truthを自由に書き換える権利

ではない。

### Adoption

Extension Adoptionとは、

> **特定VersionのExtensionを、そのSemantic Identityを変更せず、既存Domain Authorityを迂回せずに、特定Scope / Purposeにおける正式利用対象として受け入れること**

をいう。

したがって、

~~~text
Extension Exists
!= Adopted

Adopted
!= Validated

Adopted
!= Semantic Promotion

Adopted
!= Knowledge Admission

Adopted
!= Current Knowledge Applicability

Adopted
!= Production Authority

Adopted
!= Trade Permission

Adopted
!= Capital Permission
~~~

とする。

Adoptionは原則として、

~~~text
Version
Scope
Purpose
~~~

に依存する。

単独の、

~~~text
adopted = true
~~~

だけで全用途を表現することを前提にしない。

また、

> **Extension AdoptionとKnowledge Current Applicabilityを同じ概念にしない。**

Current ApplicabilityはKnowledge / Applicability Domainが所有する。

---

## 9.5 Version / Replacement / Compatibility

市場理解OSはCapabilityを変更・交換できる。

しかし、

> **変更可能であることと、変更前後を同じものとして扱えることは別**

とする。

### 9.5.1 Version

Versionとは、

> **既存Capabilityの基本Semantic Identityを維持した変更について、変更前後のMeaning・Behavior・Dependency・Historical Relianceを必要に応じて区別可能にするIdentity Boundary**

をいう。

Version NumberそのものがMaterialityを決めるわけではない。

~~~text
v1.0.1
~~~

であってもMaterialな変更はあり得る。

逆に大きなImplementation変更でも、Downstream MeaningへMaterialでない場合がある。

したがって、

~~~text
Version Label
!= Change Materiality
~~~

とする。

MaterialなMeaning / Behavior変更を、区別不能なままSilentに上書きしてはならない。

### 9.5.2 Version Change

Version Changeとは、

> **既存Capabilityの基本Semantic Identityを維持したEvolution**

をいう。

Semantic Identityそのものが変わる場合は、単純なVersion Changeとして押し込まず、

~~~text
New Extension Candidate
Core Change Candidate
~~~

のどちらが適切か再評価する。

### 9.5.3 Replacement

Replacementとは、

> **あるCapability・Provider・Technology等が担っていた今後の役割を別対象へ移すこと**

をいう。

したがって、

~~~text
Replaceable
!= Semantically Identical

Replacement
!= Historical Rewrite

Replacement
!= Automatic Adoption Transfer
~~~

とする。

Provider AからProvider Bへ変更できても、

~~~text
Timestamp
Aggregation
Coverage
Precision
Correction
Latency
Missing Handling
~~~

等が同じとは限らない。

### 9.5.4 Compatibility

Compatibilityとは、

> **特定Version / Capabilityと、特定Consumer・Contract・Use Contextとの間で、必要なMeaning・Behavior・Interactionを維持できるかを表すContext-sensitiveな関係**

をいう。

したがって、

~~~text
Interface Compatible
!= Semantically Equivalent

Runtime Compatible
!= Research Equivalent

Compatible
!= Adopted

Adopted
!= Universally Compatible
~~~

とする。

Compatibilityを、

~~~text
compatible = true
~~~

という万能Booleanだけで扱うことを前提にしない。

### 9.5.5 VersionとOriginal Domain

Section 9は、

> **Material ChangeをSilentに上書きしない**

という共通Version原則を所有する。

一方で、

~~~text
Hypothesis Version
Research Method Version
Knowledge Version
その他Domain-specific Version
~~~

の具体的Meaning・Revalidation Requirementは、Original Domainが所有する。

Section 9が全DomainのVersion Lifecycleを一つへ統合しない。

### 9.5.6 Adoption継承

~~~text
Adoption of Version N
!= Automatic Adoption of Version N+1
~~~

とする。

ただし、すべての変更について完全なゼロからの再評価を必須とも定めない。

変更内容・Compatibility・Material Impact等に応じた評価方法は後続設計で定義する。

### 9.5.7 Fallbackとの境界

Operational Failure時に代替Provider / Capabilityへ一時的にFallbackしても、

~~~text
Operational Fallback
!= Automatic Durable Replacement
~~~

とする。

一時代替と正式Replacement Decisionを混同しない。

---

## 9.6 Historical Truthとの関係

Section 8で定義したHistorical Truthを維持する。

~~~text
Current Best
!= Past Used

Known Now
!= Known Then

Later Recalculation
!= Past-used Value

Replacement
!= Historical Rewrite
~~~

とする。

新Versionを用いて過去Dataを再計算できても、それを過去に実際に使った値として扱わない。

また、

~~~text
SUPERSEDED
!= ERASED
!= Automatically Invalid
~~~

とする。

具体的Preservation Requirement・Required FidelityはSection 8がOwnerであり、Section 9では再定義しない。

---

## 9.7 Change Localization / Material Impact

Extensibilityは、変更を無関係な領域へ広げないことも含む。

ただし、

> **Change LocalizationはMaterial Impactを隠すことではない。**

### 9.7.1 Change Localization

Change Localizationとは、

> **変更によるMaterial Impactを必要なConsumer / Responsibilityへ伝えながら、Materialに関係しないDomainへ不必要な再設計・Version変更・停止・再検証を拡散させない設計原則**

をいう。

人間向けには、

> **変わった所から、意味が変わる所まで追い、意味が変わらない所で止める。**

とする。

### 9.7.2 Material Impact

Material Impactとは、

> **変更・Failure・Degradation・Replacement等によって、ConsumerのMeaning・Behavior・Result・Reproducibility・Research Interpretation・Decision Quality・Risk / Safety判断等へ無視できない変化・欠損・不確実性を与える影響**

をいう。

Material ImpactはConsumer / Purpose / Contextに依存し得る。

したがって、

~~~text
Dependency Exists
!= Material Impact
~~~

とする。

### 9.7.3 Section 8 Material Dependencyとの境界

Section 8のMaterial Dependencyと、Section 9のMaterial Impactを統合しない。

~~~text
Section 8
Material Dependency
=
将来のPreservation / History /
Reproducibility / Explanation / Audit上の依存

Section 9
Material Impact
=
現在のChange / Failureが
Consumerへ与える影響
~~~

と分離する。

---

## 9.8 Failure Propagation / Containment

Extension Failureは、

~~~text
Automatic Core Failure
~~~

を意味しない。

一方で、

~~~text
Local Extensionだから無視可能
~~~

とも限らない。

### 9.8.1 Failure Propagation

Failure Propagationとは、

> **Capability / DependencyのFailure・Degradation・Unavailability等によるMaterial Impact Contextを、そのCapabilityへMaterialに依存するConsumerへ必要な範囲で伝えること**

をいう。

ここでいうPropagationは、

> 故障そのものを他Domainへ複製すること

ではない。

### 9.8.2 Containment

Containmentとは、

> **変更・FailureによるExecution / Operational上の障害や不必要な影響を、Materialに依存しないDomain / Capabilityへ拡散させず、影響範囲を必要な責任境界内へ抑えること**

をいう。

したがって、

~~~text
Containment
!= Information Suppression
~~~

とする。

### 9.8.3 中心原則

> **Execution / Operational Failureは可能な限りContainし、Material Impactは必要なConsumerへPropagateする。**

これをSection 9のChange / Failure基本原則とする。

### 9.8.4 FailureとTruthを分離する

~~~text
Operational Failure
!= Semantic Invalidity

Current Failure
!= Historical Invalidity

Dependency Failure
!= Knowledge Invalidity

Research Process Failure
!= Hypothesis Refutation
~~~

とする。

一時的に評価不能であることと、対象自体が無効であることを混同しない。

### 9.8.5 Missing / Failureを正常値へ変換しない

~~~text
Unavailable
!= Zero

Unknown
!= Neutral

Failed
!= False
~~~

とする。

Missing / Failed DependencyをConsumerにとって正常な観測値へSilent変換してはならない。

### 9.8.6 Fallback / Redundancy

FallbackやMulti-SourceはFailure Impactを軽減できる可能性がある。

しかし、

~~~text
Fallback Exists
!= No Impact

Fallback Success
!= Semantic Equivalence

Multiple Sources
!= Equivalent Redundancy
~~~

とする。

### 9.8.7 Failure PropagationとAuthority

~~~text
Impact Propagation
!= Authority Transfer
~~~

とする。

Upstream CapabilityはFailure Contextを伝える。

そのContextを受けて、

~~~text
Continue
Wait
Reduce
Block
Safety Action
~~~

等を判断するAuthorityは、該当するDownstream Domainに残す。

具体Action RuleはSection 9では定義しない。

---

## 9.9 Market-Specific Extensibility

市場理解OSは、

~~~text
Crypto
FX
Stocks
Gold
Other Markets
~~~

を全て同一Data・Metric・Research Methodへ押し込むことを目的としない。

市場構造が異なる以上、市場固有能力を許容する。

### 9.9.1 Market-Specific Capability

Market-Specific Capabilityとは、

> **特定市場のMarket Structure・Data Availability・Participant Behavior・Institutional Rule・Research Need等へ対応するため、Coreを変更せずに追加・交換・Version変更できる専門Capability**

をいう。

候補には、

~~~text
Market-specific Data Source
Observation Content / Type
Derived Feature / Metric
Market Intelligence Method
Research Question / Method
Evidence Source
Market DNA Dimension
Market Context
Risk Input
Output Representation
~~~

等を含み得る。

この一覧を閉じたEnumにはしない。

### 9.9.2 市場固有化してよいもの

市場ごとに、

~~~text
何を観測するか
何を測定するか
どのMetricを作るか
どのResearch Questionを持つか
どう研究するか
どのEvidence Sourceを使うか
Market DNAのどのAxisを重視するか
~~~

は異なってよい。

例えば、

~~~text
Crypto
→ Funding / OI / Liquidation / On-chain

Stocks
→ Earnings / Guidance / Sector / Corporate Action

FX
→ Rates / Central Bank / Macro / Intervention

Gold
→ Real Yield / USD / Central Bank Demand / ETF Flow
~~~

等を市場固有Capabilityとして扱える。

### 9.9.3 市場ごとに変えてはいけないもの

一方で、

~~~text
Observationとは何か
Derived Featureとは何か
Interpretationとは何か
Research Resultとは何か
Knowledgeとは何か
Current Applicabilityとは何か
Authorityとは何か
Historical Truthをどう扱うか
Research Integrityをどう守るか
Hard Survival Boundaryをどう扱うか
~~~

というCommon Core Principleを市場別に独自化しない。

### 9.9.4 Market-specific Method vs Research Integrity

~~~text
Research Method
= Market-specificに変更可能

Research Integrity
= Marketを問わず共通
~~~

とする。

したがって、

> **市場ごとに研究方法は変えてよいが、研究として守る条件は変えない。**

例えば市場が異なっても、

~~~text
Evidence Trace
Version Trace
Refutation
Alternative Hypothesis
Failure Boundary
Constraint
Uncertainty
UNKNOWN / INCONCLUSIVE
Research Process Failure separation
~~~

等のIntegrityを市場固有理由で省略しない。

### 9.9.5 Market-specific Extension != Separate OS

Market-Specific Capabilityを持つことは、

~~~text
Crypto OS
Stock OS
FX OS
Gold OS
~~~

という独立OSを作ることではない。

市場固有Moduleが、

~~~text
Research
Knowledge
Decision
Capital
Execution
~~~

まで独自Authority体系として閉じ始めた場合、それは通常のMarket-Specific Extensionではなく、Core Change / OS Fragmentation Candidateとして再評価する。

9-Fで使用してきたCommon OS Skeletonは独立Formal Objectとはせず、

> **9.3で定義したCore Principleを市場横断視点から説明する表現**

として扱う。

### 9.9.6 Market-specific Capability != Authority Island

~~~text
Market-specific Extension
!= Authority Island
~~~

とする。

Market-specific Metric・Research Method・AI・Human Expertise等が存在しても、それだけで、

~~~text
Knowledge Admission Authority
Decision Authority
Capital Permission
Execution Permission
~~~

を取得しない。

具体的なAI / Human / Production Authorityは後続Sectionで定義する。

### 9.9.7 Market-specific Risk

市場固有Risk Input / Risk Methodを許容する。

しかし、

~~~text
Market-specific Risk
!= Hard Survival Boundary Exemption
~~~

とする。

市場ごとのRisk構造差を認めても、共通Survival Principleを回避しない。

### 9.9.8 Cross-Market Research

Market-specific specializationはMarket Isolationを意味しない。

~~~text
Rates
USD
Gold
Stocks
Crypto
~~~

等のCross-Market Transmissionを研究できる余地を維持する。

Cross-Market Researchでは、各Market-specific Observation / Featureの元Semantic Identityを保持する。

~~~text
Cross-Market Research
!= Semantic Collapse
~~~

とする。

---

## 9.10 ExtensibilityとMarket Scopeを分離する

Section 9は、

> **新しい市場へ対応するCapabilityを追加できるか**

を扱う。

一方、

> **どの市場をCurrent Research / Production / Trading Scopeへ正式に入れるか**

は後続のMarket Scope Governanceで扱う。

したがって、

~~~text
Market-Specific Extension Exists
!= Market Scope Authorized
~~~

とする。

また、

~~~text
Future Expansion Ready
!= Pre-build Every Future Market
~~~

とする。

Crypto Firstを維持しながら、将来拡張のBoundaryだけを壊さない。

---

## 9.11 Cross-Section Responsibility Boundary

Section 9は他Sectionの責任を奪わない。

~~~text
Section 8
=
Preservation / Historical Continuity
何を失わせてはいけないか

Section 9
=
Extensibility / Replacement
何をどの境界で変更可能にするか

Section 10
=
Market Scope / Future Expansion Governance
どの市場をいつScopeへ入れるか

Section 11
=
Research Output / Publication Mission
Research Outputをなぜ・誰へ・どう利用するか

Section 12
=
AI / Human / Production Authority
誰が実際のAuthorityを持つか

Section 13 / 14
=
Core / Charter Change Governance
Coreをいつ・どう変更できるか
~~~

という責任境界を維持する。

---

## 9.12 このSectionで固定しないもの

以下は後続Architecture / Contract / Detailed Design / Implementationで扱う。

~~~text
Plugin Class
Extension Base Class
Extension Registry
Market Registry
Dynamic Loader
Universal Extension Object
Universal Market Object
JSON Schema
Python Interface
DB Schema
SemVer MAJOR / MINOR / PATCH
Version Registry
Compatibility Enum
Adoption State Machine
Dependency Graph
Impact Graph
Health State Enum
Failure Severity Score
Fallback Priority
Automatic Failover Rule
Recovery Gate
Retry / Timeout
Circuit Breaker
Market Capability Matrix
RBAC
Deployment Strategy
Automatic Revalidation Rule
Automatic Version Propagation
~~~

Section 9では、これらを実装可能にする上位Boundaryだけを定義する。

---

## 9.13 Section-wide Core Invariants

~~~text
EX-01 Extensibility != Authority Bypass.
EX-02 Extension designation != Semantic Object Type.
EX-03 Important / Widely Used != Core.
EX-04 New Capability != Automatically Extension.
EX-05 Unrepresentable Core Semantic Change must escalate as Core Change Candidate.
EX-06 Extension Exists != Version / Scope / Purpose-specific Adoption.
EX-07 Adoption != Semantic Promotion != Validation != Production Authority.
EX-08 Adoption of Version N != Automatic Adoption of Version N+1.
EX-09 Version Change != Silent Semantic Mutation.
EX-10 Replaceable != Semantically Identical.
EX-11 Replacement != Historical Rewrite.
EX-12 Compatibility != Identity != Adoption.
EX-13 Permanent Backward Compatibility is not required.
EX-14 Change Localization != Material Impact Suppression.
EX-15 Dependency Exists != Material Impact.
EX-16 Operational Failure != Semantic / Historical Invalidity.
EX-17 Extension Failure != Automatic Core Failure and != Always Ignorable.
EX-18 Containment != Information Suppression.
EX-19 Missing / Failed Dependency != Normal Value.
EX-20 Impact Propagation != Authority Transfer.
EX-21 Market-specific Method != Research Integrity Exemption.
EX-22 Market-specific Extension != Separate OS != Authority Island.
EX-23 Common Semantic != Identical Physical Schema.
EX-24 Market-specific Extension Exists != Market Scope Authorized.
EX-25 Future-ready != Future-overengineered.
~~~

---

# Extensibility / Replaceable Capability Philosophy — 一文定義

> **市場理解OSのExtensibilityとは、Project-level Mission・Semantic Boundary・Research Integrity・Authority Boundary・Historical / Version Principle・Change / Failure Principle・Survival Principleを維持したまま、Data Source・Observation・Derived Feature / Metric・Research Method・Research Output・Market-Specific Capability等を必要に応じて追加・交換・Version変更でき、変更やFailureのMaterial Impactを必要なConsumerへ伝えながら無関係なDomainへ不必要に拡散させず、新Version・Replacement・Compatibility・Adoption・Market Scopeを互いに混同せず、個々のExtension導入だけを理由として無関係なCore OS全体の再設計を要求しない能力である。**

簡潔には、

> **OSの意味と研究原則は守りながら、必要な能力だけを後から安全に足し、替え、進化させられるようにする。**

---

# 未設計

以下は今後、一項目ずつ設計する。

~~~text
10. Market Scope / Future Expansion Governance
11. Research Output / Publication Mission
12. AI / Human / Production Authority
13. Changeable / Non-Changeable Principles
14. Charter Change Governance
~~~

これらは現時点では TBD であり、Section 1〜9から自動的に詳細内容を確定しない。

---

# 10. Market Scope / Future Expansion Governance

## 10.1 Purpose and Market Scope Meaning

Market Scope defines the **Project-level responsibility boundary** by which the Market Intelligence OS determines what formal responsibility, if any, it assumes toward a Market or Market Domain.

A **Scope Responsibility** is a Project-level responsibility formally assumed toward a Market or Market Domain within one or more Scope Dimensions.

Market Scope shall not be reduced to a single list of Markets, a binary `IN / OUT` state, the existence of available data, the existence of an Extension, the existence of Research activity, or permission to deploy Real Capital.

A Market may participate in the system under different responsibilities and contexts without all such responsibilities being implied simultaneously.

Accordingly:

```text
Data Presence
!= Market Scope

Extension Exists
!= Market Scope

Research Activity
!= Market Scope

Reference Use
!= Target Responsibility

Market Scope
!= Trade Permission
```

Market Scope governs what Scope Responsibility the Project formally assumes, not merely what the system is technically capable of observing or processing.

External Context may participate in Research, Knowledge, Dependency, or Decision support without thereby becoming a Market Scope object.

## 10.2 Scope Dimensions

Market Scope shall be representable through separable Scope Dimensions rather than a single universal inclusion state.

Scope Dimensions may include, where applicable:

```text
Research Responsibility
Reference / Context Responsibility
Production Decision Responsibility
Real-Capital Execution Responsibility
```

The presence of one Scope Dimension shall not automatically imply the presence of another.

Accordingly:

```text
Reference Responsibility
!= Research Target Responsibility

Research Target Responsibility
!= Production Decision Responsibility

Production Decision Responsibility
!= Real-Capital Execution Responsibility
```

These Dimensions do not constitute a mandatory progression or closed permanent set.

The exact state representation, schema, fields, thresholds, or storage mechanism belongs to lower-level design and is not fixed by this Charter.

## 10.3 Scope Responsibility and Actual Project Responsibility

Formal Scope shall be interpreted through the Scope Responsibility actually assumed by the Project.

The existence of a Market in data, Research, Knowledge, Models, Experiments, Dependencies, or historical records shall not by itself establish Project-level Scope Responsibility.

A declared Role shall not conceal a material mismatch between formal Scope and actual Project responsibility.

Actual Project responsibility may be evaluated through materially relevant factors including:

```text
Purpose
Persistence
Operational Dependency
Resource Commitment
Formal Output Responsibility
Downstream Materiality
```

Where such factors materially diverge from the declared Scope or Role, the mismatch may trigger Scope Review.

Role labels shall not be used to evade Scope Governance.

## 10.4 Current Scope and Crypto First

The current primary Market direction of the Project is **Crypto First**.

Crypto First establishes present Project priority. It does not establish a permanent restriction against other Markets or Market Domains.

Accordingly:

```text
Crypto First
!= Crypto Only

Crypto First
!= Crypto Forever
```

Non-Crypto Markets may be observed, researched, referenced, experimented upon, or later admitted into formal Scope when justified under this Section.

However, Reference activity, Experiment activity, or supporting Market activity shall not accumulate in a manner that silently replaces the current primary Project priority without explicit Scope Review and authorization.

Future expansion is permitted.

Silent priority replacement is not.

## 10.5 Scope Candidate and Discovery

A Market or Market Domain may first appear through or be identified in connection with:

```text
Observation
AI Discovery
Research Question
Experiment
Correlation
Cross-Market Relationship
Causal Candidate
Dependency Discovery
Operational Need
```

External Context may reveal, motivate, or support the identification of a Scope Candidate without itself thereby becoming that Scope Candidate or a Market Scope object.

Such discovery may create a Scope Candidate or otherwise make a Market or Market Domain eligible for evaluation.

A Candidate does not by itself establish Scope Responsibility or Scope Authorization.

`Candidate` shall not be interpreted as an independent formal Scope State unless lower-level Governance explicitly defines such a state consistently with this Charter.

A Market may therefore exist as a Candidate, exploratory object, Reference Candidate, or Experiment-level Target before the Project assumes Project-level Scope Responsibility for it.

Casual, temporary, or exploratory observation shall not by itself require formal Scope modification.

## 10.6 Entry and Expansion Criteria

Formal entry or expansion into Market Scope shall require a defined Purpose and justified Scope Responsibility.

Evaluation shall consider, where materially applicable:

```text
Purpose
Expected Understanding Value
Research Value
Decision Value
Material Relevance
Evidence
Cost
Complexity
Operational Burden
Dependency Burden
Risk
Project Capacity
Compatibility with Current Priority
```

Potential relevance alone shall not be sufficient.

The existence of technically available data, an available Extension, a temporary correlation, a single successful Experiment, or an AI recommendation shall not independently justify Scope expansion.

Expansion shall remain proportional to the Scope Responsibility actually required.

`Material` shall be interpreted within the relevant governance context and shall not require a universal fixed numerical threshold at Charter level.

## 10.7 Evidence, Review and Authorization Boundary

Evidence may support a Scope decision.

Evidence shall not itself constitute a Scope decision or Scope Authorization.

This applies to:

```text
AI Discovery
Correlation
Causal Candidate
Experiment Result
Cross-Market Evidence
Model Dependency
Reference Criticality
Runtime Behavior
Failure
```

Accordingly:

```text
Strong Evidence
!= Scope Authorization

Experiment Evidence
!= Scope Authorization

Dependency
!= Scope Authorization
```

A **Scope Review** is a governance evaluation of whether an existing or proposed Scope Responsibility remains justified.

Scope Review does not itself authorize a Scope State Change.

Accordingly:

```text
Scope Review
!= Scope Authorization

Scope Review
!= Scope State Change
```

The conceptual sequence is:

```text
Discovery / Evidence
↓
Scope Review
↓
Authorized Scope Decision
↓
Scope State Change
```

This conceptual separation does not require separate organizations, persons, systems, or services to perform each step.

No discovery, Research result, Model behavior, Dependency, or Failure shall silently create Project-level Scope authority.

## 10.8 Scope Change Authority

A change to formal Market Scope shall require explicit authority appropriate to Scope Governance.

Authority shall not arise implicitly from:

```text
Data Availability
AI Output
Research Output
Experiment Success
Knowledge Creation
Dependency Criticality
Production Use
Failure Propagation
```

AI output shall not acquire Scope-changing authority merely by being AI output.

Any Scope-changing authority delegated to an AI, human, service, process, or other actor shall require explicit authorization under Governance.

The identity and implementation of the authorized decision-maker may be defined by lower-level Governance, but the existence of explicit Scope authority shall not be optional.

This Charter does not prescribe the exact human role, AI role, committee, service, database writer, approval interface, or implementation mechanism through which such authority is exercised.

## 10.9 Scope Lifecycle

Formal Market Scope shall be capable of changing over time.

Scope Governance shall support, where applicable:

```text
Entry
Expansion
Promotion
Maintenance
Reduction
Suspension
Exit
Re-entry
```

These states or transitions shall not be interpreted as one mandatory linear ladder.

In particular:

```text
Reference
→ Research
→ Decision
→ Execution
```

is not a required universal progression.

Promotion means a justified addition, strengthening, or formalization of Scope Responsibility within an applicable Scope Dimension.

Promotion does not require progression through every other Scope Dimension.

Current Scope and Historical Scope shall remain distinguishable.

## 10.10 Reduction, Suspension and Exit

A Scope Responsibility may be reduced, suspended, or exited when its Purpose, value, evidence, feasibility, risk, cost, dependency structure, Project priority, or continuing justification no longer supports the existing responsibility.

Reduction narrows an existing Scope Responsibility.

Suspension temporarily ceases or disables an applicable current Scope Responsibility without treating its historical identity as though it never existed.

Exit ends the applicable current Scope Responsibility.

These conceptual distinctions do not require a specific lower-level State Machine.

A temporary technical or runtime problem shall not automatically constitute a Scope change.

Accordingly:

```text
Provider Failure
!= Market Exit

Temporary Data Failure
!= Scope Reduction

Capability Failure
!= Automatic Scope Suspension

Runtime Restriction
!= Scope Suspension
```

Failure shall first be handled according to its operational and downstream consequences.

Persistent inability to maintain the required Scope Responsibility may trigger Scope Review, but Failure itself shall not silently perform the Scope change.

## 10.11 Re-entry

A Market or Market Domain that has previously been reduced, suspended, or exited may later be considered for re-entry.

Re-entry shall evaluate the current environment, current Purpose, current evidence, and current justification rather than blindly restoring the former Scope state.

Accordingly:

```text
Re-entry
!= Blind Restoration
```

At the same time, re-entry shall not treat the Market or Market Domain as though no history exists.

Previous Research, Evidence, Failure, Knowledge, Scope history, and historical reasoning may remain relevant subject to their current validity and applicable Preservation obligations.

## 10.12 Reference and Context Markets

The Project may formally use another Market or Market Domain as a Reference or Context in support of Market Understanding, Research, Decision, or another authorized responsibility.

A formal Reference may carry a limited Scope Responsibility appropriate to its Purpose and Materiality.

However:

```text
Reference Responsibility
!= Target Responsibility

Reference Scope Expansion
!= Target Responsibility Expansion

Reference Membership
!= Mandatory Usage

Reference Membership
!= Material Dependency
```

A formal Reference does not automatically establish Research Target Responsibility, Production Decision Responsibility, or Real-Capital Execution Responsibility.

Reference Scope Responsibility shall remain bounded by the Purpose for which the Reference was authorized.

A material change in Reference Purpose may trigger Scope Review rather than being treated as automatically covered by the original authorization.

Adding one Reference shall not imply collection, modeling, Research, or Governance of the entire surrounding Market universe.

## 10.13 Experiment-Level and Project-Level Targets

A Market may be directly studied within a specific Research Question, Experiment, Validation, or Comparison without thereby establishing Project-level Target Responsibility.

Accordingly:

```text
Experiment-level Target
!= Project-level Target Responsibility
```

Experiment evidence may support future Scope expansion but shall not itself authorize that expansion.

Temporary and bounded Experiment activity may occur without rewriting Project-level Scope.

However, the Experiment label shall not be used to evade Scope Governance.

Where Experiment activity becomes materially persistent through continuing Research, dedicated infrastructure, resource commitment, operational dependence, or formal output responsibility, the activity may trigger Project-level Scope Review.

A Market may hold different Roles at different governance levels.

A context-specific Role shall not automatically propagate into another governance level.

## 10.14 Material Dependency Boundary

Material Dependency and Market Scope Responsibility are distinct concepts.

A Market, Data Source, Context, or Capability may materially affect another authorized Research, Decision, Risk, or Execution responsibility without becoming a Target Responsibility itself.

Accordingly:

```text
Material Dependency
!= Scope Responsibility

Dependency Criticality
!= Target Responsibility Promotion

Material Dependency
!= Proven Causality
```

Greater Dependency Criticality may justify stronger:

```text
Monitoring
Data Quality Responsibility
Freshness Responsibility
Uncertainty Handling
Fallback
Failure Handling
Recovery Responsibility
```

without changing the Market's Scope Role.

Dependency evidence shall not be treated as causal proof.

Capability Dependency design itself remains subject to the appropriate lower-level and Extensibility Governance rather than being redefined by this Section.

## 10.15 Cross-Market Research and Knowledge Identity

The Project may conduct Cross-Market Research without assuming equivalent Project-level or Trading responsibility for every participating Market.

Accordingly:

```text
Cross-Market Research
!= Multi-Market Trading

Causal Chain Participation
!= Formal Target Responsibility

Production Input
!= Production Target Responsibility
```

Cross-Market Knowledge may represent relationships involving multiple Markets or Market Domains.

Cross-Market Knowledge shall not be semantically reduced to a single Market where doing so would destroy or materially distort the represented relationship.

Its relevant Participating Markets, Research Context, Usage Context, and Historical Identity shall remain distinguishable where required for correct interpretation.

A current Market Role shall not rewrite the historical Role under which Knowledge was originally produced.

Market Scope change shall not automatically change the lifecycle or historical meaning of Cross-Market Knowledge.

## 10.16 Failure Propagation and Aggregate Burden

Failure may propagate through a Material Dependency.

Scope Responsibility shall not propagate merely because Failure does.

Accordingly:

```text
Failure Propagation
!= Scope Propagation
```

A Reference failure may affect downstream Confidence, Availability, Decision Permission, Fallback behavior, Runtime Permission, or Recovery requirements according to its Materiality.

It shall not automatically establish Target Responsibility for the failed Reference or automatically suspend the associated Market Scope.

Scope Governance shall consider aggregate burden where cumulative effects may become Material.

A collection of individually justified References, Dependencies, or Scope Responsibilities may collectively create material:

```text
Operational Complexity
Research Cost
Monitoring Cost
Dependency Complexity
Failure Surface
Resource Burden
```

Accordingly:

```text
Individual Reference Justification
!= Aggregate Reference Burden Acceptability
```

Aggregate burden may trigger Scope Review but shall not itself determine which Scope Responsibilities must be reduced, suspended, or exited.

No fixed Market-count limit is established by this Charter.

## 10.17 Extensibility, Preservation and Historical Boundary

Market Scope Governance is distinct from System Extensibility Governance.

Accordingly:

```text
Capability Extension
!= Market Scope Expansion

Market Scope Expansion
!= Necessarily Capability Extension
```

A newly authorized Market may be supportable through the existing Common OS Skeleton.

Where new capability is genuinely required, that capability shall be governed under the Extensibility principles of Section 9 rather than treating Market expansion itself as permission to alter the Core.

Market Scope Lifecycle is also distinct from Information Lifecycle.

Accordingly:

```text
Scope Lifecycle
!= Information Lifecycle

Scope Exit
!= Historical Erasure

Scope Exit
!= Automatic Termination of Preservation Obligation
```

Reduction, Suspension, Exit, or Role Change modifies current Scope Responsibility.

It does not independently authorize destruction of Historical Data, Evidence, Research Results, Cross-Market Knowledge, Decision History, Failure knowledge, or other preserved information.

Preservation and destruction remain governed by Section 8.

## 10.18 Governing Invariants and Interpretation Guard

The preceding provisions shall be interpreted consistently with the following non-equivalence constraints.

These constraints are Interpretation Guards. They do not independently redefine the concepts established in Sections 10.1–10.17.

```text
Market Scope
!= Data Presence

Market Scope
!= Trade Permission

Extension Exists
!= Scope Inclusion

Observation
!= Formal Scope Responsibility

External Context Participation
!= Market Scope Responsibility

Candidate
!= Formal Scope Responsibility

Discovery
!= Scope Authorization

Strong Evidence
!= Scope Authorization

Scope Review
!= Scope Authorization

Scope Review
!= Scope State Change

Reference Responsibility
!= Target Responsibility

Reference Membership
!= Mandatory Usage

Reference Membership
!= Material Dependency

Experiment-level Target
!= Project-level Target Responsibility

Material Dependency
!= Scope Responsibility

Dependency
!= Causal Proof

Dependency Criticality
!= Target Responsibility Promotion

Cross-Market Research
!= Multi-Market Trading

Production Input
!= Production Target Responsibility

Failure Propagation
!= Scope Propagation

Temporary Failure
!= Automatic Scope Reduction or Exit

Runtime Restriction
!= Scope Suspension

Capability Extension
!= Market Scope Expansion

Market Scope Expansion
!= Necessarily Capability Extension

Scope Lifecycle
!= Information Lifecycle

Scope Exit
!= Historical Erasure

Scope Exit
!= Automatic Termination of Preservation Obligation

Current Role
!= Historical Role

Crypto First
!= Crypto Only

Crypto First
!= Crypto Forever

Re-entry
!= Blind Restoration
```

Material Purpose Drift, persistent mismatch between declared Scope and actual Project responsibility, or materially excessive Aggregate Burden may trigger Scope Review.

None of those conditions shall independently constitute Scope Authorization or Scope State Change.

Role labels such as `Reference`, `Experiment`, `Candidate`, or other limited-purpose designations shall not be used to conceal material Project responsibility or evade Scope Governance.

Actual responsibility, persistence, resource commitment, operational dependence, formal output responsibility, Purpose, and material burden may therefore require Scope Review when the declared Role no longer reflects the Project's material reality.

At the same time, Scope Governance shall not be interpreted so aggressively that every observation, temporary Experiment, Reference use, External Context use, or technical Failure requires Project-level Scope modification.

The purpose of this Section is to preserve a deliberate and governable distinction between:

```text
what the Project can observe,

what the Project can study,

what the Project can use as context,

what the Project depends upon,

what the Project formally accepts Scope Responsibility for,

and what the Project is authorized to act upon.
```

---

# 11. Research Results Usage Governance

## 11.1 Purpose

The system shall govern how Research Outputs are identified, consumed, considered as Knowledge Candidates, promoted where justified into Reusable Knowledge, adopted for authorized use, transformed or derived into downstream Objects, and evaluated for downstream Material Impact when their Sources materially change or fail.

Research results shall not acquire stronger Evidence, broader Scope, greater Authority, independent Provenance, or unrestricted downstream usability merely through consumption, reuse, transformation, derivation, aggregation, representation change, model training, or repeated use.

## 11.2 Research Output Boundary

A Research Output shall represent an identifiable result produced by a Research activity.

The existence, generation, storage, or availability of a Research Output shall not by itself establish that the Output is Reusable Knowledge, adopted information, Production-authorized information, or Independent Evidence.

Research Output status shall remain distinct from downstream decisions concerning consumption, reuse, Knowledge Promotion, Adoption, Authority, Transformation, and Production Use.

## 11.3 Consumer and Usage Context

Use of a Research Output shall occur within an identifiable Consumer and Usage Context.

Consumption shall not by itself constitute Adoption, Knowledge Promotion, Evidence strengthening, or Production authorization.

Repeated consumption, frequent use, or use by multiple Consumers shall not by itself promote a Research Output into Reusable Knowledge or increase its Authority.

A change of Consumer shall not by itself remove material restrictions, Scope, Evidence limitations, Source Lineage, or other applicable Governance attached to the information being consumed.

## 11.4 Knowledge Candidate and Reusable Knowledge

A Research Output may become a Knowledge Candidate where it is considered for durable reuse beyond its immediate Research context.

A Knowledge Candidate shall not become Reusable Knowledge solely because it is useful, repeatedly consumed, widely referenced, or consistent with existing expectations.

Knowledge Promotion shall preserve material Evidence, Scope, restrictions, Material Provenance, Source Lineage, contradictions, and other material limitations necessary to interpret and reuse the resulting Knowledge correctly.

Reusable Knowledge shall mean information permitted for reuse under its applicable Governance and shall not imply unrestricted use, Production authorization, universal validity, or broader Market Scope.

## 11.5 Independent Evidence

Reuse, duplication, Transformation, Derivation, aggregation, representation change, or repeated observation of materially dependent information shall not create Independent Evidence merely by producing additional Objects or additional agreement.

Independent Evidence shall require sufficient independence to prevent a common Source, shared Material Provenance, or derived Evidence from being counted as independent confirmation of itself.

Derived agreement shall not be used to artificially strengthen the Evidence supporting its own materially shared Source.

## 11.6 Material Provenance and Source Lineage

Material Provenance and Source Lineage shall remain sufficiently traceable for downstream users and processes to understand material origin and dependency where such origin or dependency affects interpretation, validity, reuse, Authority, or Failure Impact.

Creation of a new Object, representation, version, summary, Feature, Market DNA representation, Model, Signal, or other Derived Object shall not by itself establish independent Provenance.

Loss, omission, or absence of Source Lineage shall not be interpreted as proof that no Material Dependency exists.

## 11.7 Adoption Boundary

Knowledge existence and Reusability shall remain distinct from Adoption.

Adoption shall represent a Governance decision permitting information to be used for an identified purpose under applicable conditions.

Consumption, reuse, Knowledge Promotion, Transformation, successful historical performance, or repeated use shall not by itself constitute Adoption.

## 11.8 Production Use and Authority

Production Use shall require applicable Authority and shall not be established merely by the existence, usefulness, reusability, Transformation, or Derivation of Research information.

Reusable Knowledge shall not automatically become Production-authorized Knowledge.

Transformation into a Feature, Market DNA representation, AI output, Model input, Model output, Signal, Defense input, or other downstream Object shall not by itself create Production Authority.

Multiple Sources lacking the required Authority shall not acquire such Authority merely through aggregation or combination.

## 11.9 Authority Preservation Through Derivation

Derivation, Transformation, summarization, aggregation, representation change, model training, or Propagation shall not be used to bypass an Authority restriction applicable to a Source, its material properties, or the intended use.

A Derived Object may possess a distinct Object Identity while remaining materially dependent on one or more Sources.

Distinct Object Identity shall not be treated as independent Authority, independent Provenance, or absence of Material Dependency.

## 11.10 Derivation and Transformation

Transformation shall create a changed representation or form without, by itself, changing the material meaning, Evidence status, Scope, restrictions, Authority, or Provenance required for correct interpretation.

Derivation shall create a downstream Object materially informed by one or more Sources without implying that the Derived Object is independent from those Sources.

Simplification, summarization, quantification, Feature generation, Market DNA conversion, AI interpretation, Knowledge aggregation, model training, or Signal generation shall not by themselves strengthen Evidence, remove restrictions, broaden Scope, or create Authority.

## 11.11 Propagation and Semantic Preservation

Where Research-derived information propagates across Consumers, Knowledge, Features, Market DNA, AI systems, Models, Signals, Defense mechanisms, or other downstream processes, material meaning and applicable Governance shall not be removed or altered solely as a consequence of crossing an Object, Consumer, representation, or system-layer boundary.

A system-layer boundary, Consumer boundary, Object boundary, or representation change shall not by itself constitute a Provenance boundary, Authority reset, or Material Dependency boundary.

Material contradictions, limitations, Failure Boundaries, and other material qualifications shall not be removed solely through downstream Propagation.

## 11.12 Aggregation and Dependent Evidence

Aggregation of multiple Objects shall not be treated as Independent Evidence merely because multiple inputs produce the same or similar conclusion.

Where multiple inputs share a material Source or materially dependent Evidence, that shared dependency shall remain relevant when interpreting aggregated Evidence.

Repeated or transformed expressions of materially shared Evidence shall not be treated as Independent Evidence.

## 11.13 Model and AI Boundary

Use of Research-derived information in AI processing, model training, inference, summarization, classification, prediction, or other computational Transformation shall not sever Material Provenance, Source Lineage, or Material Dependency merely because the information has been encoded, transformed, learned, or represented differently.

Observed downstream performance shall not by itself prove Source independence or absence of Material Impact from a Source defect.

A newer Model, AI output, or Derived Object version shall not by itself establish that relevant Material Dependencies have been removed.

## 11.14 Scope Preservation

Reuse, Knowledge Promotion, Derivation, Transformation, aggregation, generalization, AI processing, or successful downstream use shall not independently expand the Market Scope or Usage Scope permitted for the underlying information.

Reusable Knowledge shall not by itself establish Market Entry Authority.

Where a Source Scope is narrowed, expanded, restricted, or otherwise materially changed, dependent uses shall be evaluated according to their Material Dependency and applicable Scope rather than assuming either universal invalidation or universal continued validity.

Section 11 shall not provide a mechanism for bypassing the Market Scope and Future Expansion Governance established by Section 10.

## 11.15 Material Dependency and Material Impact

Material Dependency shall remain distinct from Material Impact.

The existence of Material Dependency shall not by itself establish that a particular Source change materially affects every dependent Object.

Material Impact shall be determined from the relationship between a material change, failure, contradiction, invalidation, correction, restriction, Scope change, version change, Lifecycle change, or other materially relevant event affecting a Source and the Material Dependency of the downstream Object, Consumer, or Process.

A materially relevant event affecting a Source may create Material Impact without rendering the Source itself universally invalid.

## 11.16 Failure Impact

Failure Impact shall represent Material Impact arising from a failure-related event through Material Dependency.

Source failure, invalidation, retirement, contradiction, Failure Boundary discovery, correction, or Evidence weakening shall not by itself establish either total downstream failure or absence of downstream impact.

Failure Impact shall not automatically imply that an affected Derived Object is invalid, retired, disabled, or unusable in every context.

Likewise, recording a failure, preserving it in the Failure Museum, or correcting the original Source shall not by itself establish that downstream Failure Impact has been resolved.

## 11.17 Impact Boundary

For a materially relevant event affecting a Source, the Impact Boundary shall distinguish the downstream extent for which Material Impact is relevant based on Material Dependency and the material relevance of the event.

The Impact Boundary shall neither be expanded beyond nor truncated before the extent justified by those relationships.

Graph distance, system-layer distance, Object type, Consumer identity, or descendant status shall not by itself establish the Impact Boundary.

A failure shall therefore neither trigger unjustified total Cascade nor be artificially isolated before materially affected dependencies have been considered.

## 11.18 Affected Object

An Affected Object shall be an Object for which Material Impact has been established with respect to a particular materially relevant event affecting a Source and applicable Material Dependency.

Affected status shall not by itself mean invalid, retired, suspended, deleted, retrained, rebuilt, or otherwise remediated.

Material Impact on one material property shall not automatically establish Material Impact on every property of the Object.

Impact determination shall remain distinct from the choice of remediation or operational action.

## 11.19 Unresolved Impact

Unresolved Impact shall apply where available Material Dependency, Source Lineage, Material Provenance, event relevance, or other necessary information is insufficient, unavailable, contradictory, or otherwise inadequate to reasonably determine whether Material Impact exists.

Unresolved Impact shall not be treated as evidence of No Material Impact.

Unresolved Impact shall also not automatically establish that Material Impact exists.

Absence of lineage or dependency information shall not by itself establish absence of Material Dependency or Material Impact.

Unresolved Impact shall represent genuine uncertainty and shall not be used as a substitute for a determination that can reasonably be supported by available information.

## 11.20 Source Change, Version, and Remediation

A change in Source version, correction, replacement, supersession, or remediation shall not by itself establish either Material Impact or absence of Material Impact.

Source correction shall not automatically mean downstream correction.

Source supersession shall not automatically mean migration of existing Derived Objects to the superseding Source.

A newer downstream version shall not by itself establish independence from earlier Material Provenance, Source Lineage, or Material Dependency.

Section 11 shall preserve the Version, Replacement, and Continuity Governance established by Section 9 rather than redefining it.

## 11.21 Governance Structure Is Not a Mandatory Runtime Pipeline

The ordering of Section 11 Governance boundaries shall not require every Research Output to pass through every boundary as a mandatory runtime execution sequence.

A Research Output may terminate at Research use, may never become Reusable Knowledge, may never be adopted for Production Use, and may follow different technical processing paths.

However, omission of a runtime stage or use of a shorter technical path shall not create Authority to bypass any Governance boundary applicable to the actual use.

The structural ordering of these Governance boundaries shall not be interpreted as a mandatory execution order; applicable Governance shall remain applicable regardless of runtime path length.

## 11.22 End-to-End Governance Preservation

Across the complete Research-result usage lifecycle, Research information shall not acquire stronger Evidence, broader Scope, greater Authority, independent Provenance, or immunity from downstream Failure Impact merely by being consumed, reused, promoted, transformed, aggregated, encoded, learned, propagated, or represented as a new Object.

The system shall preserve sufficient semantic and dependency continuity to support both forward use from Research through downstream usage and reverse impact analysis from a materially relevant Source change or failure through Material Dependency to downstream Impact determination.

Research-result usage shall therefore remain sufficiently traceable to prevent unjustified strengthening, removal, reset, expansion, or bypass of Authority, Evidence, Material Provenance, Scope, or failure-related Governance across the Research-to-Production lifecycle.
