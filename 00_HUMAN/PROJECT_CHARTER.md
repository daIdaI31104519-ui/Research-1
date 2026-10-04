# 市場理解OS — PROJECT CHARTER v0.1

**Document Role:** Project Constitution / Top-Level Mission  
**Status:** DRAFT / LEADING CANDIDATE  
**Purpose:** 市場理解OSが何のために存在し、何を優先し、どの方向へ育てるかを定義する最上位方針文書。  
**Current Scope:** Section 1 `Project Mission`、Section 2 `Success Definition`、Section 3 `What Not To Maximize`、Section 4 `Survival / Profit Priority` を設計済み。Section 5以降は未設計であり、現時点では固定しない。

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


# 未設計

以下は今後、一項目ずつ設計する。

```text
5. Research Mission
6. Research Category Philosophy
7. Capital / Risk Philosophy
8. Knowledge / Data Asset Philosophy
9. Independent Data / Metric Extensibility
10. Market Scope / Future Expansion Governance
11. Research Output / Publication Mission
12. AI / Human / Production Authority
13. Changeable / Non-Changeable Principles
14. Charter Change Governance
```

これらは現時点では `TBD` であり、Section 1〜2から自動的に詳細内容を確定しない。
