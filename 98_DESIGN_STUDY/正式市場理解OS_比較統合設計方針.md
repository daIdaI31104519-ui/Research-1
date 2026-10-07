# 正式市場理解OS — 比較統合設計方針

**Document Role:** Long-Term Comparative Design Strategy / Formalization Goal  
**Status:** DRAFT / STRATEGIC DIRECTION  
**Purpose:** 旧市場理解OS、ダイスケ案市場理解OS、GPT独立案市場理解OSを独立した設計Candidateとして育て、比較・反証・採否判断・統合を経て、最終的な正式市場理解OSを構築するための長期設計方針を固定する。  
**Important:** NOT CURRENT DESIGN / NOT FORMAL ARCHITECTURE / NOT PROJECT CHARTER / NOT AUTOMATIC ADOPTION

---

# 0. この文書の役割

この文書は、現在の市場理解OSそのものを定義する設計書ではない。

目的は、

> **「どのCandidateをどう作り、どのように比較し、最終的に正式な市場理解OSへ到達するか」**

という長期的な設計研究方針を、将来このRepositoryを見るHuman / AIが失わないようにすることである。

現在進めている `PROJECT_CHARTER.md`、既存Architecture、旧BOT実装、ダイスケ原案、将来作るGPT独立案の身分を混同しない。

```text
Current Design
!= Final Integrated Market Understanding OS

Candidate Design
!= Current Design

Detailed Design
!= Automatic Adoption

Gitに存在する
!= 正式採用
```

とする。

---

# 1. なぜ比較統合方式を使うのか

これまでの市場理解OS設計では、

```text
ダイスケが考える
↓
AIへ「考えて」「深掘りして」と依頼
↓
AIが案を拡張
↓
レビュー
↓
設計へ保存
```

という方法を多く利用してきた。

この方式は、ダイスケ自身の思想を精密化するうえでは有効である。

一方、最終的な正式市場理解OSまで同じ経路だけで作ると、

```text
最初の前提への引っ張られ
AIによる追認
同じ思想の再表現
既存構造へのAnchoring
過去の設計判断を前提とした最適化
人間とAIの相互Confirmation Bias
```

等によって、設計Noiseや盲点が残る可能性がある。

そのため正式版は、一つの設計系統をそのまま完成形にするのではなく、**異なる起源を持つ複数Candidateを独立に作り、後から衝突させる方式**を基本方向とする。

---

# 2. 比較対象となる3つの主要Candidate

## 2.1 旧市場理解OS — Legacy Candidate

旧市場理解OSは、古いという理由だけで捨てない。

主な価値は、

```text
実際に作ったCode
実装可能だった構造
Import / Dependency問題
Collector / Indicator / Signal / Risk / Logger / Analyzer / Trainer等の実装経験
Backtest経験
実際に発生したFailure
設計と実装のズレ
過去に有効だった発想
過去に複雑化した原因
```

等の**Implementation Reality / Historical Evidence**を持つことである。

したがって、

```text
Legacy
!= Wrong

Old
!= Useless

Implemented
!= Correct
```

とする。

旧OSは、正式版の比較において「過去の現実」を提供するCandidate / Evidence Sourceとして扱う。

## 2.2 ダイスケ案市場理解OS — Human-Origin Candidate

現在詳細化している市場理解OSは、ダイスケ本人の考えを起点とする設計Candidateである。

このCandidateでは、

```text
何を市場理解と考えるか
何を研究したいか
どのようなKnowledgeを残したいか
なぜResearchを重視するか
どのようにRiskと利益を分けたいか
将来どの市場へ広げたいか
人間がどのように理解・管理したいか
```

等を、Destruction / Precision / Human Review等によって可能な限り精密化する。

現在の `PROJECT_CHARTER.md` 作成は、このHuman-Origin Candidateを上位思想から閉じていく主要工程である。

ただし、

```text
Daisuke Design
!= Final Integrated Design
```

である。

詳細化の完成度が高くても、将来の比較工程を免除しない。

## 2.3 GPT独立案市場理解OS — AI-Origin Independent Candidate

ダイスケ案が十分に閉じた後、GPTが独立して市場理解OSを設計する。

ここで最も重要なのは、

> **ダイスケ案の詳細設計を言い換えるだけのGPT案にしないこと。**

である。

GPT独立案の初期生成では、必要以上にダイスケ案の詳細構造へAnchoringさせない。

原則として、最初に与えるのは市場理解OSの最小Problem Statementと必要なHard Constraintに留める。

例:

```text
市場を観測・理解する
継続的に研究する
Knowledgeを蓄積・再検証する
安全な資本運用へ利用できる
初期対象はCrypto Spot / Crypto FX
将来他市場へ拡張可能
長期運用可能
失敗を追跡できる
AI / Python / Databaseを利用可能
```

この条件から、

> **GPT自身ならどのような市場研究・意思決定OSをゼロから構築するか**

を独立に詳細化する。

GPT案を作った後に初めて、ダイスケ案・旧OSとの比較へ進む。

---

# 3. Candidate Independence Principle

正式比較を意味あるものにするため、Candidate同士を早期に融合しない。

```text
Independent Candidate Generation
↓
Candidate Closure
↓
Cross-Candidate Comparison
```

を基本とする。

特にGPT独立案について、

```text
Daisuke設計を大量に先読み
↓
同じLayer名・同じ責任・同じ思想を再構成
↓
GPT Independent Designと呼ぶ
```

ことを避ける。

完全な情報隔離が不可能な場合でも、少なくとも、

```text
どこが独立発想か
どこが既知情報の影響か
どのConstraintは共通Problem Statement由来か
```

を区別する。

---

# 4. 正式版は3案の平均ではない

Formal Integrationは、

```text
Legacy 33%
+
Daisuke 33%
+
GPT 33%
```

のような平均化ではない。

設計項目ごとに、

```text
採用
部分採用
修正採用
保留
却下
新規第4案
```

を選べる。

場合によっては、

```text
Legacy = reject
Daisuke = reject
GPT = reject
↓
New Formal Candidate
```

も許容する。

したがって、

> **Candidate Comparisonの目的は勝者を決めることではなく、より壊れにくいFormal Designを作ること。**

とする。

---

# 5. Formal Integrationの基本工程

正式版作成時の基本候補は次とする。

```text
Candidate Designs
↓
Conflict Extraction
↓
Assumption Comparison
↓
Comparative Evaluation
↓
Destruction Review
↓
Decision Record
↓
Integrated Candidate
↓
Cross Check
↓
Human Review
↓
Implementation Reality Check
↓
Formal Baseline
```

この順序自体は将来再設計してよい。

重要なのは、

> **比較前にCandidateを混ぜないこと、採否理由を残すこと、統合後に再度破壊検査すること。**

である。

---

# 6. 比較評価軸

Formal Integrationでは少なくとも以下を比較候補とする。

```text
Mission Fit
Semantic Clarity
Research Integrity
Failure Resilience
Adaptability
Extensibility
Production Safety
Observability / Traceability
Implementability
Complexity Cost
Long-Term Maintainability
Human Understandability
Evidence / Provenance Integrity
Authority Clarity
Recovery Cost
```

これらを必ず単一Scoreへ潰す必要はない。

```text
Comparison Matrix
!= Universal Final Score
```

である。

評価軸自体も正式統合工程開始時に再検討する。

---

# 7. Decision Recordを残す

Formal Designでは「何を採用したか」だけでなく、

```text
何と何を比較したか
どの前提が異なったか
何を採用したか
何を却下したか
なぜ却下したか
どのFailureを避けたかったか
何を保留したか
将来どの条件で再検討するか
```

を残す。

例:

```text
Topic:
Market DNA Responsibility

Legacy Candidate:
Signal寄り

Daisuke Candidate:
Current Market State Representation

GPT Candidate:
State Representation + Similarity Context

Final Decision:
Daisuke + GPT conceptsを再設計して採用

Reason:
Market StateとDecision Authorityを分離するため

Rejected:
Legacy Signal-like responsibility

Rejection Reason:
Semantic Boundaryが弱くDecision Layerへ侵入するため
```

このDecision Recordが、正式市場理解OSの設計理由を将来復元する基礎になる。

---

# 8. Source Identityを消さない

比較・統合時には、

```text
Legacy由来
Daisuke由来
GPT由来
Formal Integrationで新規生成
```

を必要な範囲で区別できるようにする。

統合したからといって、

```text
最初からFormal Designだった
```

ことに書き換えない。

Formal DesignのSource Historyを保持する。

---

# 9. 現在のGitルールをFormal Integrationへ自動継承しない

現在の `AI_WORKFLOW.md` とGit運用は、現段階の市場理解OSを安全に詳細化・保存するために利用する。

しかし将来の正式統合段階では、

> **現在の作業方法そのものも比較・再設計対象にする。**

つまり、

```text
Current Git Workflow
!= Future Formal Integration Workflow

Current Directory Structure
!= Mandatory Final Repository Structure
```

とする。

Formal Integration開始前に、

```text
Candidateの保存構造
比較方法
Conflict管理
Decision Record
Rejected Design管理
Canonicalization
Baseline
Recovery
Human Review
AI Review
Git Branch / Commit / Tag運用
```

等を、Formal Integration専用Workflowとして設計する。

現在のルールを理由なく捨てる必要もないが、理由なくそのまま継承もしない。

---

# 10. Formal CandidateとCurrent Designを混ぜない

将来GPT案や比較結果を作成しても、

```text
New Candidate
!= Current Design

Comparative Winner
!= Automatic Formal Design

Integrated Draft
!= Formal Baseline
```

とする。

Current Designを書き換えるのは、Formal Integration側で定めるReview / Approval / Baseline条件を満たした後とする。

---

# 11. 現在のProject Sequencing

現時点の優先順位は次とする。

```text
PHASE A
ダイスケ案市場理解OSを十分な深さまで詳細化する
↓
PHASE B
GPT独立案市場理解OSを同等レベルまで詳細化する
↓
PHASE C
旧市場理解OSをImplementation Reality / Historyとして整理する
↓
PHASE D
3 Candidateを比較・衝突させる
↓
PHASE E
Formal Integration専用Workflow / Git Governanceを設計する
↓
PHASE F
正式市場理解OS Candidateを作る
↓
PHASE G
Destruction / Precision / Human / Implementation Review
↓
PHASE H
Formal Baseline
```

Phase順は将来の設計によって調整してよい。

ただし、現段階でGPT案との早期融合へ移らず、**まずダイスケ案の詳細化を継続する**。

---

# 12. Noiseを抑えるためのGuardrails

今後のAIは次を守る。

```text
Candidate
!= Formal

Detailed
!= Correct

AI Agreement
!= Independent Validation

Human Preference
!= Automatic Adoption

Legacy
!= Automatic Rejection

GPT Proposal
!= Superior by Default

Daisuke Proposal
!= Superior by Default

Comparison
!= Averaging

Same Terminology
!= Same Semantics

Different Terminology
!= Different Semantics
```

さらに、

- 一つのCandidateの用語を他Candidateへ無断で移植しない。
- 比較する時は同じ抽象度・責任レベルを揃える。
- CandidateごとのAssumptionを明示する。
- 不一致を無理に解消せずConflictとして保持できる。
- 正式統合前にSource / Decision Historyを消さない。
- 「AIがそう言った」ことを採用理由にしない。
- 「ダイスケがそう考えた」ことだけを採用理由にしない。
- 実装経験と理論設計を別Evidenceとして扱う。

---

# 13. 今後のAIがこの文書を読んだ時の行動

この文書を見つけても、現在Taskを勝手にFormal Integrationへ切り替えない。

まず、

```text
00_AI/AI_CONTEXT.md
↓
Current Task / Current Phase確認
```

を行う。

現在がダイスケ案詳細化Phaseなら、

> **その作業を継続する。**

GPT独立案作成Phaseへ正式に移行した場合のみ、この文書を比較設計の上位方針として利用する。

Formal Integration Phaseへ移る時は、

> **最初にFormal Integration専用WorkflowとGit Governanceを設計する。**

---

# 14. この文書でまだ決めないこと

現時点では以下を固定しない。

```text
Formal Repo Directory Tree
Candidate用Branch構造
具体的Comparison Score
Approval人数 / Authority
Decision Record Schema
Formal Baseline条件
GPT Independent Designの正確なPrompt
Candidate Closure条件
Legacy整理方法の詳細
Formal Integrationの自動化
具体的Python / DB設計
```

これらは各Phaseへ入る直前に設計する。

---

# 15. 最終目標

最終的に作りたいものは、

> **「ダイスケがAIに考えさせて作った市場理解OS」でも、「GPTが勝手に作った市場理解OS」でも、「旧BOTを改修しただけの市場理解OS」でもない。**

目標は、

> **旧市場理解OSの実装現実、ダイスケの独立した市場理解思想、GPTの独立した設計案を比較・反証し、採用・却下理由を残しながら再構成した正式市場理解OSを作ること。**

である。

---

# 一文定義

> **正式市場理解OSの比較統合設計方針とは、旧OS・ダイスケ案・GPT独立案を早期に混ぜず独立Candidateとして育て、Implementation Reality・Human思想・AI独立設計を同じ審査台で比較・破壊・採否判断し、そのDecision Historyを保持したうえで、Formal Integration専用Workflowを通して最終的な市場理解OSへ再構築するための長期戦略である。**
