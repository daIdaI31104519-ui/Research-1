# 市場理解OS — PROJECT CHARTER v0.1

**Document Role:** Project Constitution / Top-Level Mission  
**Status:** DRAFT / LEADING CANDIDATE  
**Purpose:** 市場理解OSが何のために存在し、何を優先し、どの方向へ育てるかを定義する最上位方針文書。  
**Current Scope:** Section 1 `Project Mission` と Section 2 `Success Definition` を設計済み。Section 3以降は未設計であり、現時点では固定しない。

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

具体的な最大化禁止事項、SurvivalとProfitの優先順位、Business / Publicationの詳細は後続Sectionで定義する。

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

# 未設計

以下は今後、一項目ずつ設計する。

```text
3. What Not To Maximize
4. Survival / Profit Priority
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
