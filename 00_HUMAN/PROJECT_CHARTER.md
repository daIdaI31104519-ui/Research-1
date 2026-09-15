# 市場理解OS — PROJECT CHARTER v0.1

**Document Role:** Project Constitution / Top-Level Mission  
**Status:** DRAFT / LEADING CANDIDATE  
**Purpose:** 市場理解OSが何のために存在し、何を優先し、どの方向へ育てるかを定義する最上位方針文書。  
**Current Scope:** Section 1 `Project Mission` のみ設計済み。Section 2以降は未設計であり、現時点では固定しない。

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

# 未設計

以下は今後、一項目ずつ設計する。

```text
2. Success Definition
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

これらは現時点では `TBD` であり、Section 1から自動的に詳細内容を確定しない。
