# 市場理解OS 全体再構築 設計ログ

**Document Role:** Reconstruction Design Log / Working Reference  
**Status:** ACTIVE WORKING LOG / NOT CURRENT DESIGN / NOT CANONICAL  
**Purpose:** 市場理解OSの全体再構築における議論・判断・候補・却下理由・変更理由を時系列で保存し、最終Architectureが「なぜその形になったか」を追跡可能にする。  
**Design Authority:** ダイスケ = 最終判断者 / GPT = 設計士・構造化・批判・矛盾検出・代替案提示  
**Adoption Rule:** このログへの保存は正式採用を意味しない。

---

# 0. 運用原則

このログは、旧市場理解OS、途中Current市場理解OS、Research Institute設計検討、新しいダイスケ案を再構築する過程を保存する。

重要:

```text
Gitへ保存
≠ Current Designへ採用

詳細に議論
≠ 固定

過去に時間をかけた
≠ 残す

新しい
≠ 優れている
```

正式採用は、再構築・比較・破壊レビューを通過した後に別途判断する。

---

# 1. 再構築の基本方針

既存Architectureをそのまま修正する方式を採らない。

```text
旧市場理解OS
+
途中Current市場理解OS
+
Research Institute検討
+
ダイスケの新しい市場理解OS思想
↓
Source Extraction
↓
Design Intent
↓
Capability Map
↓
複数の白紙Architecture候補
↓
Reconstruction
↓
Destruction Review
↓
Final Principles
↓
Final Architecture
```

目的は「全部入り巨大OS」を作ることではない。

過去設計から、名称ではなく存在理由・責任・守ろうとしていた価値を回収し、現在の目的に必要なものだけを再構築する。

---

# 2. WHY / WHAT / HOW 分離

再構築では必ず以下を分離する。

```text
WHY
なぜ必要なのか

WHAT
OSは何ができなければならないのか

HOW
どのConcept / Object / Engine / Algorithmで実現するのか
```

HOWは破壊・交換可能。

WHYとWHATを先に守る。

例:

```text
WHY
異常市場でも実資金を守りたい

WHAT
通常状態からの逸脱を検出できる必要がある

HOW候補
Market DNA
Regime Model
Distribution Shift Detection
Anomaly Detection
```

Market DNAを後でDROPしても、WHY / WHATまで消してはいけない。

---

# 3. 再構築Phase

## Phase 1 — Source Extraction

対象:

- 旧市場理解OS
- Current市場理解OS
- PROJECT_CHARTER
- HUMAN_MAP
- Research Institute Working Reference
- ダイスケの新しい市場理解OS思想
- 必要に応じて関連設計資料

抽出するもの:

- 何を実現しようとしていたか
- なぜ必要だったか
- 何を守る責任だったか
- 入力 / 出力の意味
- 他責任との重複
- 消した場合に失う能力

この段階では採用判断をしない。

## Phase 2 — Design Intent

ダイスケが市場理解OSで最終的に実現したい目的を抽出する。

例:

- 経済市場を理解する
- 実資金を長期的に増やす
- 大きなDrawdown / Ruinを避ける
- 通常市場を研究する
- 異常市場にも適応する
- 原因を研究する
- Unexpected Resultから逆方向にも調査する
- Research Asset / Knowledgeを長期蓄積する
- Crypto以外へ拡張可能にする
- AI / API / Exchange / Data Provider等を交換可能にする
- 長期間運用可能にする

この段階でもArchitectureを固定しない。

## Phase 3 — Capability Map

Design Intentから、

「市場理解OSは何ができなければならないか」

を抽出する。

Concept名やLayer名より能力を優先する。

## Phase 4 — Multiple Blank Architecture Candidates

既存01〜04等を修正するのではなく、同じDesign Intent / Capabilityを満たす白紙Architectureを複数案作る。

1案へ早期固定しない。

## Phase 5 — Reconstruction

以下を照合する。

```text
旧OS
Current OS
新思想
白紙Architecture候補
```

Concept単位で、

```text
KEEP
REDESIGN
SPLIT
MERGE
DROP
DEFER
NEW
```

候補を作る。

まだ最終固定ではない。

## Phase 6 — Destruction Review

ここで初めて既存・新規Conceptを意図的に壊す。

各Conceptについて、

- 本当に必要か
- 消したら何を失うか
- 他責任で代替可能か
- 分割した方がよいか
- 統合した方がよいか
- 10年後も意味があるか
- 市場追加時に障害にならないか
- Research品質へ本当に寄与するか
- 実資金保護へ本当に寄与するか
- 長期保守性を壊さないか

を確認する。

破壊そのものを目的にしない。

**重要な意味を持つ破壊 = 問題発見手段**

とする。

## Phase 7 — Final Principles / Architecture

Destruction Reviewを生き残ったものだけを対象に、

```text
思想
↓
責任
↓
大分類
↓
Connection
```

を固定候補へ進める。

その後、

```text
Object
Source of Truth
Authority
State
Contract
Failure
DB
Python
```

へ落とす。

---

# 4. Destruction Reviewを今すぐ実行しない理由

破壊レビューは重要だが、再構築の最初には行わない。

理由:

```text
守るべきWHY / WHATが未整理
↓
HOWだけ先に壊す
↓
必要能力まで誤って失う可能性
```

したがって現在は、

**Destruction Review = Phase 6まで保留**

とする。

---

# 5. 現在の作業位置

```text
Current Reconstruction Phase:
Phase 1 — Source Extraction

Next:
旧市場理解OS
Current市場理解OS
Research Institute Reference
ダイスケ新思想
から、名称ではなく存在理由・責任・守る能力を抽出する。
```

---

# 6. 保存ルール

今後この再構築作業で重要な判断が出た場合、このログへ追記する。

保存対象:

- 新しい重要思想
- 設計方針変更
- Concept追加候補
- Concept削除候補
- 大きな矛盾
- 破壊レビュー結果
- KEEP / REDESIGN / SPLIT / MERGE / DROP / DEFER / NEW判断
- 判断理由
- 未解決問題
- Checkpoint

保存しないもの:

- 軽微な言い換え
- 単なる説明例
- 一時的な思いつきで設計判断に影響しないもの

---

# 7. 現在の重要Boundary

```text
Working Log
≠ Current Design

Design Candidate
≠ Adopted Design

Research Result
≠ Knowledge

Knowledge
≠ Applicable Knowledge

Applicable Knowledge
≠ Trade

HOW
≠ WHY

Concept Name
≠ Required Capability
```

---

# 8. Checkpoint 001

**State:** SAVED  
**Stage:** Reconstruction Preparation  
**Decision:** 全体再構築はPhase方式で行う。破壊レビューはPhase 6へ移動。  
**Current Next Action:** Phase 1 Source Extraction。  
**Formal Current Architecture Changed:** NO


---

# 9. Checkpoint 002 — ダイスケ案正式原案の固定

**State:** SAVED  
**Stage:** Reconstruction Source Preparation  
**Formal Current Architecture Changed:** NO

正式な再構築Sourceとして以下を追加した。

```text
98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md
```

Status:

```text
AUTHORITATIVE DAISUKE PROPOSAL
NOT FINAL CURRENT DESIGN
NOT FINAL ARCHITECTURE
NOT CANONICAL CURRENT
```

この文書は、ダイスケ本人が考える市場理解OSの正式原案として今後の再構築で必ず比較対象にする。

特に以下を原案の重要Intentとして保持する。

- 基礎的な市場・経済構造から研究を開始する
- 人間が市場を見る時の「関係性による理解」をAI / Python / Databaseが扱える形へ形式化する
- Flow / Distortion / Cycle / Propagation / Amplification / Constraint / Substitution / Accumulation / Expectations / Lag / Threshold / Equilibrium等を共通関係候補として扱う
- 世界経済図書館と、OS自身が研究して得る知識図書館を分離する
- 通常探索と、旧OS由来の異常・因果・Stress・Failure研究を両立する
- Knowledgeを直接リアルTradeへ接続しない
- Trade中も現在市場を観測し、Knowledge成立条件の変化へ対応する
- Unexpected Resultを単純再学習せずRoot Causeを調査する
- 順方向だけでなく結果から原因候補へ戻る逆方向研究を持つ
- 市場固有研究を交換可能にし、Crypto以外へ拡張可能にする
- 長期運用、Research Asset蓄積、実資金保護を同時に考える
- 運用監視系を必要能力として持つ
- 研究結果の人間向け資産化も将来可能にする

## Source Preservation Rule

ダイスケ案は最終設計に合わせて後から改変しない。

変更が必要になった場合は原案を書き換えるのではなく、Reconstruction / Destruction Review側で、

```text
Original Intent
↓
Problem
↓
Change Reason
↓
Replacement
↓
Preserved Intent / Lost Intent
```

を記録する。

## Current Position

```text
Source Preparation = COMPLETE

NEXT:
Phase 1 — Source Extraction
```


---

# 10. Checkpoint 003 — Phase 1 Closure / Phase 2 Design Intent

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Current Reconstruction Stage:** Phase 2 COMPLETE → Phase 3 READY

## 10.1 Phase 1 Closure

4つの再構築Sourceを、Layer / Engine / Object名ではなく「何を実現しようとしていたか」で比較した。

対象:

1. 旧市場理解OS
2. 途中Current市場理解OS
3. Research Institute Working Reference
4. ダイスケ正式原案

Phase 1で回収した主要な意味:

```text
旧市場理解OS
=
異常・矛盾・失敗・本番事故を、
原因を雑に決めず研究・防御・実行・事後分析へ分離し、
適切な責任へ戻す能力が強い

Current
=
Observation / Interpretation / Candidate / Hypothesis / Result /
Knowledge / Applicability / Decision / Risk 等の意味と責任を混ぜない能力が強い

Research Institute Reference
=
Reactive ResearchだけでなくProactive Researchを追加し、
探索・確認・再現・反証・Ledger・Red Team等によって
Researchそのものの科学性を高める能力が強い

Daisuke Proposal
=
人間が市場を見る時の「関係性による理解」を
AI / Python / Databaseが扱える共通言語へ形式化し、
通常市場からの研究、逆方向調査、長期Research Asset、
実資金運用との接続を強化する
```

Phase 1で重要な共通Capabilityとして確認したもの:

- 市場を観測する
- 観測から即Tradeしない
- 市場を理解してから判断する
- Researchを持つ
- 仮説・関係を検証する
- 反証・失敗を扱う
- Knowledgeを蓄積する
- Knowledgeを直接Tradeしない
- 現在市場との適合を確認する
- Economic ValueとRiskを分離する
- Production結果を分析する
- Researchへ戻るLoopを持つ
- Unknownを許す
- 長期的に適応する
- ResearchとProductionを分離する

Phase 1で確認した重要Gap:

- RelationをMachine-readableにする正式表現
- Foundation内のFact / Mechanism / Model / Heuristic等の身分管理
- Long-term Storage / Retention
- Temporal Integrity / Information Availability
- Reverse InvestigationのHindsight Bias対策
- Research Priority
- Capital / Portfolio Architecture
- Runtime Knowledge Condition Monitoring
- Unknown管理
- Market追加Contract
- FoundationとCurrent MarketのRelevant Retrieval
- Self-Modification Governance
- Human / AI / Production Authority
- PublicationとInternal Knowledgeの分離
- Research Asset Migration
- OS自身のResearch
- Multi-Knowledge Conflict Resolution
- Market Understanding Quality評価

重要:

```text
Market DNA
Causal Engine
World Economic Library
Knowledge Library
AI Team
Signal Engine
Defense Layer
Stress Lab
Failure Museum
Quantum Layer
Knowledge Graph
```

等は、この段階ではRequired CapabilityではなくHOW Candidateとして扱う。

---

## 10.2 Phase 2 Review Result

Phase 2 Design Intentは、4SourceとCurrent Charterに照合した結果、大きな矛盾なし。

ただし以下を補正した。

### Correction A — Survival / Profit Priority

Current Charterでは、

```text
Survival / Profit Priority
```

の厳密な優先順位は未設計。

したがってPhase 2では、

> 短期ProfitのためにCapital・Research Capability・Knowledge Integrity・System Continuityを破壊しない

までをDesign Intentとして保持する。

```text
Survival > Profit
```

という厳密な序列はまだCanonical化しない。

### Correction B — Reverse Investigation

```text
Unexpected Outcome
↓
Reverse Investigation
↓
Cause Candidate
↓
Formal Research
```

とする。

```text
Reverse Investigation
≠ Root Cause Confirmation
```

後知恵のStoryをCause確定として扱わない。

### Correction C — Temporal / Decision Integrity

追加Design Intent:

> 過去のDecision / Research / Tradeを、後から判明した情報ではなく、その時点で利用可能だったEvidence・Knowledge・Risk・Uncertainty・Data Qualityに基づいて検証できること。

重要:

```text
Good Outcome
≠ Good Decision

Bad Outcome
≠ Bad Decision

Later Knowledge
≠ Information Available At Decision Time
```

これはCurrentのTime / Freshness思想、Decision検証思想、LegacyのOutcome分離と整合する。

---

# 10.3 Final Phase 2 Design Intent Set

## A. Primary Intent

1. 市場・経済・世界の出来事を、価格だけでなく関係性から理解する
2. 人間の「関係を結んで考える能力」を、AI / Python / Databaseが扱える検証可能な形へ形式化する
3. 通常市場からもProactiveに研究する
4. 異常・矛盾・失敗からもReactiveに研究する
5. ResearchをKnowledgeへ変える
6. KnowledgeをCurrent Marketへ慎重に適用する
7. Economic Valueへ接続する
8. 実資金運用結果を再びResearchへ戻す
9. Capital・Research Asset・Decision Capabilityを長期間成長させる
10. この循環を市場変化に合わせて止めずに適応させる

## B. Research / Integrity Intent

- 観測と解釈を混ぜない
- 発見と確認を混ぜない
- 相関と因果を混ぜない
- AI JudgmentとEvidenceを混ぜない
- Research ResultとKnowledgeを混ぜない
- KnowledgeとApplicabilityを混ぜない
- ApplicabilityとEconomic Valueを混ぜない
- Economic ValueとRisk Permissionを混ぜない
- Trade OutcomeとHypothesis / Thesis / Execution / Risk Outcomeを混ぜない
- Unknownを無理に答えへ変えない
- 失敗・反証・Negative / UnknownもResearch Assetとして扱う
- Research Historyを保持する
- 過去判断を当時利用可能だった情報だけで再検証可能にする

## C. Adaptation / Learning Intent

- 成功Knowledgeも永久の正解にしない
- Foundationを絶対法則として扱わない
- Knowledge成立条件を再検証する
- Unexpected ResultをResearch入口へ変える
- Reverse InvestigationはCause Candidate生成として利用する
- Root Causeに応じて適切な責任へ戻す
- 同じFailureを理由なく繰り返さない
- Runtime中もKnowledge成立条件の変化を観測できる方向を持つ

## D. Capital / Survival Intent

- Researchは実資金のEconomic Valueへ接続する
- 短期ProfitのためにCapital・Research Capability・Knowledge Integrity・System Continuityを破壊しない
- Expected Valueが正でもRisk上不適切なら資金を出さない
- Trade / WAIT / REDUCE / NO TRADE / UNKNOWNを有効なDecision Outcomeとして扱える方向を持つ
- Drawdown / Ruin / Portfolio Risk等の詳細Priorityは後続設計へ残す

## E. Longevity / Extensibility Intent

- AI / API / Data Provider / Exchange / Python実装等を交換可能にする方向を持つ
- 実装よりResearch Assetを長生きさせる
- Long-term Storageを無限膨張させない
- Crypto Firstを維持しつつFuture Expansion Readyとする
- 市場固有のData / Research / Execution差を無理に同一化しない
- Migration後もKnowledge意味・Evidence・Historyを失わない方向を持つ

## F. Human / Secondary Intent

- Research結果を人間が理解できる形にする
- Research Note / Research Diary / Graph等を再利用可能にする
- 将来のApplication / Publication / Business Opportunityを許容する
- External OutputのためにResearch Integrityを歪めない

---

# 10.4 Phase 2 One-Sentence Candidate

> **市場理解OSは、市場・経済・世界の出来事を関係性から理解し、そこから生まれる疑問を検証・反証可能なResearchへ変え、その成果を条件付きKnowledgeとして蓄積し、現在市場・Economic Value・Riskと照合して実資金へ慎重に接続し、結果を当時利用可能だった情報に基づいて検証しながら再び研究へ戻すことで、Capital・Research Asset・Decision Capabilityを長期間成長させ続ける市場研究・資金運用OSを目指す。**

この一文はReconstruction Working Intentであり、PROJECT_CHARTERの正式文を置換しない。

---

# 10.5 Unresolved Intent Tensions

Phase 3以降でCapability / Architectureへ落とす際に解決対象とする。

```text
Profit
↔
Survival

Foundation
↔
Open Discovery

Stability
↔
Adaptation

Knowledge Utilization
↔
Knowledge Re-Validation

Long-Term Preservation
↔
Storage Cost / Volume

Multi-Market Expansion
↔
Crypto First Simplicity

Automation
↔
Human / Production Authority

Runtime Safety
↔
Strategy Continuation

Research Freedom
↔
Production Safety

Publication
↔
Research Integrity
```

---

# 10.6 Phase State

```text
Phase 1 — Source Extraction
STATUS:
COMPLETE

Phase 2 — Design Intent
STATUS:
COMPLETE / WORKING RECONSTRUCTION BASELINE

Phase 3 — Capability Map
STATUS:
NEXT
```

重要:

```text
Phase 2 COMPLETE
≠
Final Philosophy Fixed

Phase 2 Design Intent
≠
Current Canonical Design

Phase 3 Capability
≠
Architecture Layer

HOW Candidate
≠
Required Capability
```


---

# 11. Checkpoint 004 — Phase 3 Capability Map Closure

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Current Reconstruction Stage:** Phase 3 COMPLETE → Phase 4 READY

## 11.1 Review Method

Phase 3 Capability Mapを以下の5 Testで再確認した。

```text
A. Remove Test
Capabilityを消した時、Design Intentが失われるか

B. Merge Test
別Capabilityと統合しても責任・失敗原因・意味を失わないか

C. Split Test
一つのCapabilityが大きすぎて異なる責任を抱えていないか

D. Coverage Test
Phase 2 Design Intentが最低1つのCapabilityで実現可能になっているか

E. HOW Contamination Test
Market DNA / Engine / Layer / DB / AI Team等の実現手段がRequired Capabilityへ混入していないか
```

## 11.2 Important Review Findings

### Finding A — Decision Synthesis Gap

旧Mapでは、

```text
Applicability
↓
Economic Value
```

の間に、

> 複数Applicable Knowledge、反対Thesis、Conflict、WAIT / NO TRADE等を統合し、Decision Candidateへ変換する能力

が明示されていなかった。

そのため新Capabilityとして追加する。

```text
Decision Synthesis / Conflict Resolution
```

重要:

```text
Applicable Knowledge
≠
Decision Candidate

Knowledge Conflict
≠
Majority Vote

Decision Synthesis
≠
Risk Permission
```

### Finding B — Execution / Position Split

旧C14相当の、

```text
Execution / Position
```

は責任が広すぎる。

以下を分離する。

```text
Execution Fidelity
=
意図した注文をVenueへ安全に提出・確認・Reconcileする能力

Position / Runtime Protection
=
成立したExposureを追跡し、Protection / Exit / Runtime Safetyを維持する能力
```

### Finding C — Human-readable Research Projection Gap

Phase 2 Secondary Intentに、

- Human-readable Research
- Research Note / Research Diary / Graph
- Application / Publication / Business Opportunity
- External OutputでResearch Integrityを歪めない

があるが、Main Capabilityに直接対応するCapabilityが不足していた。

Secondary Capabilityとして、

```text
Human-readable Research Projection
```

を追加する。

これは内部Knowledgeを書き換える能力ではなく、

```text
Internal Research Asset
↓
traceable projection
↓
Human-readable output
```

を作る能力。

```text
Publication Output
≠
Knowledge Source of Truth
```

## 11.3 Merge / Keep Results

以下は似ているが統合しない。

```text
Observation Integrity
≠
System Monitoring

Relation Understanding
≠
Current Market Understanding

Research Validation
≠
Boundary Discovery

Knowledge Formation
≠
Knowledge Lifecycle

Knowledge Lifecycle
≠
Generic State / Lifecycle Integrity

Applicability
≠
Decision Synthesis

Decision Synthesis
≠
Economic Value

Economic Value
≠
Capital / Risk Permission

Outcome Understanding
≠
Feedback Routing

Research Asset Preservation
≠
Storage / Retention / Migration

Trace / Provenance
≠
Version / Lineage

Authority / Governance
≠
Human Control
```

理由:
責任、入力、出力、Failure Mode、Authorityが異なるため。

## 11.4 HOW Contamination Result

以下はRequired Capabilityへ固定しない。

```text
Market DNA
Causal Engine
World Economic Library
Knowledge Library
AI Team
Signal Engine
Defense Layer
Stress Lab
Failure Museum
Quantum Layer
Knowledge Graph
Telegram
Specific Database
Specific AI Model
Specific Exchange
Specific Python Library
```

これらはPhase 4以降のHOW / Architecture Candidate。

AIについてはRequired Semantic Coreではなく、

> Replaceable Cognitive Assistanceを安全に接続できる横断Capability

として扱う。

## 11.5 Final Main Capability Map

### Family A — OBSERVE / UNDERSTAND

```text
C01 World / Market Observation
C02 Observation Integrity
C03 Relation / Foundation Representation
C04 Current Market Understanding
```

### Family B — DISCOVER / RESEARCH

```text
C05 Research Question Discovery
C06 Research Priority / Admission
C07 Validation / Refutation / Replication
C08 Boundary / Constraint Discovery
```

### Family C — KNOWLEDGE / DECISION PREPARATION

```text
C09 Knowledge Formation
C10 Knowledge Lifecycle / Revalidation
C11 Knowledge Applicability / Runtime Assumption Monitoring
C12 Decision Synthesis / Conflict Resolution
C13 Economic Value Assessment
```

### Family D — CAPITAL / PRODUCTION

```text
C14 Capital Allocation / Risk / Portfolio Governance
C15 Execution Fidelity
C16 Position / Runtime Protection
```

### Family E — LEARN / FEEDBACK

```text
C17 Outcome / Decision Quality Understanding
C18 Feedback / Research Routing
```

### Family F — LONG-TERM FOUNDATION

```text
C19 Research Asset Preservation
C20 Replaceability / Market Extensibility / System Evolution
```

### Family G — HUMAN VALUE / SECONDARY

```text
C21 Human-readable Research Projection
```

重要:

```text
21 Capabilities
≠
21 Layers
```

Capability MapはArchitectureではない。

## 11.6 Final Cross-Cutting Capability Map

```text
X01 Time / Temporal Integrity
X02 Trace / Provenance
X03 Version / Lineage
X04 Uncertainty / Calibration
X05 State / Lifecycle Integrity
X06 Authority / Governance
X07 Human Control
X08 Cognitive Assistance Integration
X09 Security / Identity / Credential / Classification
X10 Monitoring / Incident / Recovery
X11 Storage / Retention / Migration
```

補足:

```text
Auditability
=
X01 + X02 + X03 + X05 + X06

Reproducibility
=
C07 + C19 + X01 + X02 + X03
```

の組合せで成立可能なため、現時点では独立Cross-Cutting Capabilityを追加しない。

## 11.7 Coverage Check

Phase 2 Intent Coverage:

```text
Relationship-based understanding
→ C03 / C04

Proactive + Reactive Research
→ C05 / C06 / C07 / C08 / C18

Research → Knowledge
→ C09

Knowledge re-validation
→ C10

Current usability / runtime assumption
→ C11

Conflicting Knowledge / action alternatives
→ C12

Economic opportunity
→ C13

Real capital / drawdown / portfolio
→ C14

Safe venue action
→ C15

Runtime position safety
→ C16

Outcome / hindsight-safe evaluation
→ C17 + X01

Root Cause candidate / correct return path
→ C18

Long-term Research Asset
→ C19 + X11

Replaceable AI/API/Provider/Market
→ C20 + X03 / X06 / X10 / X11

Human-readable research / publication
→ C21 + X02 / X09

Unknown
→ X04 + C05 / C11 / C17

Human / Production authority
→ X06 / X07

Temporal integrity
→ X01
```

No major Phase 2 Intent remains completely uncovered.

## 11.8 Remaining Open Questions

Capability existenceは確認できたが、Phase 4で複数Architectureを作るまで固定しない。

```text
- C03 Relation / Foundationをどこに置くか
- C03とC04を同一Domainにするか分離するか
- C05への複数Entryをどう構成するか
- Research Dual-Entry / Single-Coreを採用するか
- C11 Runtime Assumption MonitoringとC16 Runtime Protectionの境界
- C12 Decision SynthesisとC13 EVの責任境界
- C14 Capital / Portfolioを一つのDomainにするか
- C19とX11のStorage responsibility split
- X08 Cognitive AssistanceをどこまでCore Runtimeから切り離すか
- C21 PublicationをCore Runtimeから完全分離するか
```

## 11.9 Phase State

```text
Phase 1 — Source Extraction
COMPLETE

Phase 2 — Design Intent
COMPLETE / WORKING RECONSTRUCTION BASELINE

Phase 3 — Capability Map
COMPLETE / WORKING RECONSTRUCTION BASELINE

Phase 4 — Multiple Blank Architecture Candidates
NEXT
```

重要:

```text
Phase 3 COMPLETE
≠
Final Architecture

Capability
≠
Layer

Cross-Cutting Capability
≠
Cross-Cutting Layer

Architecture Candidate
≠
Adopted Architecture
```


---

# 12. Checkpoint 005 — Phase 4 Blank Architecture Stress Comparison

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Current Reconstruction Stage:** Phase 4 COMPLETE → Phase 5 READY

## 12.1 Blank Architecture Candidates

同一Capability Set:

```text
C01-C21
+
X01-X11
```

を満たす前提で、既存Current 01-04を出発点にせず4案を作成した。

### Candidate A — Research-Centered

中心:
Research Question / Research Core

性格:
市場・異常・失敗・外部研究をResearchへ集約し、Research品質を中心にOSを組む。

### Candidate B — Relation / World-Model-Centered

中心:
Relation / Foundation Representation

性格:
世界・経済・市場を共通関係として表現し、Current Market / Research / Knowledgeをそこから派生させる。

### Candidate C — Knowledge-Loop-Centered

中心:
Knowledge Core / Lifecycle

性格:
Research・Applicability・Decision・OutcomeをKnowledgeの成長と再検証を中心に循環させる。

### Candidate D — Multi-Core Hybrid

中心:
特定Conceptではなく責任境界

候補Core:
```text
Perception
Research
Knowledge / Decision
Capital / Production
Learning / Feedback
```

Cross-Cuttingは共通横断Capabilityとして扱う。

重要:

```text
Candidate
≠ Recommendation
≠ Adoption
```

---

# 12.2 Common Stress Cases

4案すべてに同じCaseを流した。

```text
Case 1  通常BTC市場で新しいEdgeを探索
Case 2  突然の規制暴落
Case 3  KnowledgeがLongなのにBTC急落
Case 4  Exchange API障害
Case 5  3つのKnowledgeがLong / Short / WAITで衝突
Case 6  AI停止
Case 7  CryptoからGold追加
Case 8  10年後にData Provider変更
Case 9  過去KnowledgeのEdge Decay
Case 10 Research結果を日本語Reportへ出力
```

---

# 12.3 Case Results

## Case 1 — 通常BTC市場で新しいEdgeを探索

### A Research-Centered

自然なFlow:

```text
Observation / Current Understanding
↓
Question Discovery
↓
Research Priority
↓
Research Core
↓
Knowledge
```

Strength:
Research integrityが高い。

Risk:
Question増殖によりResearch backlog化しやすい。

### B Relation / World-Model-Centered

自然なFlow:

```text
Observation
↓
Relation / Current Model
↓
Known relation / unexplained relation
↓
Research Question
```

Strength:
ダイスケ案の「関係性から研究」に最も自然。

Risk:
Relation Model拡張そのものが目的化しやすい。

### C Knowledge-Loop-Centered

自然なFlow:

```text
Current Market
↓
Knowledge retrieval
↓
Gap / conflict
↓
Research
```

Strength:
既知Knowledgeとの比較が容易。

Risk:
既存Knowledgeにない現象をNoiseとして見落としやすい。

### D Multi-Core Hybrid

自然なFlow:

```text
Perception
↓
Question Discovery
↓
Research
↓
Knowledge
```

Strength:
Relation理解とOpen Discoveryの両方を持てる。

Risk:
Core間Contractが曖昧だと責任が重複する。

---

## Case 2 — 突然の規制暴落

必要条件:

```text
Researchを待たずRuntime Safetyが動けること
```

### A

Research側では原因調査に強いが、Production SafetyがResearchに依存すると遅い。

必要:
Runtime Safety Fast PathをResearchから独立。

### B

Regulation → Participant Behavior → Flow → MarketのPropagation表現に強い。

Risk:
Relation Model更新を待ってPosition保護が遅れると危険。

必要:
World Model理解とRuntime Protectionを分離。

### C

既存Knowledge Applicabilityの崩壊を検知しやすい。

Risk:
未知規制を既存Knowledge Lifecycle問題として誤分類する可能性。

### D

```text
Perception
→ Runtime Context
→ Capital / Production Safety

並行:

Perception
→ Research Question
→ Research
```

と二速度化しやすい。

Phase 4 Finding:

> Emergency / runtime safetyはResearch completionを待たないArchitectureが必要。

---

## Case 3 — KnowledgeがLongなのにBTC急落

### A

```text
Unexpected Outcome
→ Research Question
→ Reverse Investigation
→ Formal Research
```

に自然。

### B

```text
Expected Relation Network
≠
Observed Outcome
↓
Missing / broken relation candidate
```

を作りやすい。

Risk:
説明可能なStoryをRelationで後付けしやすい。

### C

```text
Knowledge contradiction
→ Lifecycle / Revalidation
```

に最も自然。

Risk:
Knowledge自身のFailureと、外部Event / Data / Execution Failureを混同しない仕組みが必須。

### D

```text
Outcome
↓
Feedback
├ Perception failure?
├ Research failure?
├ Knowledge failure?
├ Applicability failure?
├ Capital failure?
└ Execution failure?
```

とFailure routingしやすい。

Phase 4 Finding:

> Reverse Investigationは独立Root Cause Authorityではなく、FeedbackからResearch Candidateを生成するMethodとして扱う方が安全。

---

## Case 4 — Exchange API障害

### A

Research中心Architectureでは、Operation FailureがResearch問題へ誤流入しないBoundaryが必要。

### B

Relation / World Modelとは無関係なSystem Failureであり、中心Modelへ入れない方が良い。

### C

Knowledge failureではないため、Knowledge Lifecycleを汚さないBoundaryが必要。

### D

```text
X10 Monitoring / Incident / Recovery
+
Capital / Production
```

で市場理解Loopと分離しやすい。

Phase 4 Finding:

```text
System Failure
≠
Market Failure
≠
Knowledge Failure
```

をArchitecture Boundaryとして守る必要がある。

---

## Case 5 — KnowledgeがLong / Short / WAITで衝突

### A

Researchへ戻すだけでは不十分。

Research済みKnowledge同士がConflictしていても、現在Decisionを作る必要がある。

### B

Relation ModelからConflict Contextを説明しやすいが、Relationの多数決はDecisionにならない。

### C

Knowledge Coreとの相性が高い。

ただし:

```text
3 Knowledge中2つLong
→ Long
```

の多数決は禁止。

### D

Knowledge / Decision責任内に、

```text
C11 Applicability
↓
C12 Decision Synthesis
↓
C13 Economic Value
```

を置きやすい。

Phase 4 Finding:

> C12 Decision Synthesis / Conflict Resolutionは独立責任として残す価値が高い。

---

## Case 6 — AI停止

### A

新規Research能力は低下してよいが、既存Knowledge利用・Risk・Execution Protectionまで停止してはいけない。

### B

Relation Interpretation更新は低下し得るが、Raw Observation / Safetyは維持すべき。

### C

既存Knowledge利用をRule / deterministic logicで継続しやすい。

### D

X08 Cognitive AssistanceをCross-Cuttingとして切り離し、

```text
AI停止
≠
Capital Protection停止
```

を最も明示しやすい。

Phase 4 Finding:

> AIはCore AuthorityではなくReplaceable Cognitive Assistanceとして扱う方向が強く支持された。

---

## Case 7 — CryptoからGold追加

### A

Research Method / Question入口をMarket Profile化すれば拡張可能。

### B

Flow / Constraint / Expectations / Lag等のRelation Vocabularyを再利用しやすく、共通知識に強い。

Risk:
Crypto固有RelationをUniversal Relationとして誤適用しないこと。

### C

Market-specific Knowledge分離が必要。

Knowledge reuseは強いが、Market identity / applicabilityを厳密に持つ必要がある。

### D

Shared responsibility + Market-specific adapter / profileへ分離しやすい。

Phase 4 Finding:

> 共通OSとMarket-specific knowledge/method/data/executionを分ける必要性が強く支持された。

---

## Case 8 — 10年後にData Provider変更

### A

Research AssetがSource Providerに密結合していると再現性が壊れる。

### B

Relation ModelのSource lineage移行が複雑になりやすい。

### C

KnowledgeがProvider-independent semantic assetなら強い。

### D

C19 / C20 + X02 / X03 / X11を共通Foundationに置きやすい。

Phase 4 Finding:

> Provider / AI / Exchange / ImplementationはSemantic CoreのSource of Truthにしない。

---

## Case 9 — 過去KnowledgeのEdge Decay

### A

Revalidation Researchへ戻すのが自然。

### B

Underlying relation / market structure changeとして調べやすい。

### C

Knowledge Lifecycle中心なので非常に自然。

### D

```text
Knowledge Lifecycle
↓
Applicability
↓
Contradiction / decay
↓
Feedback
↓
Research
```

を責任分離して表現できる。

Phase 4 Finding:

```text
Knowledge Aging
≠
Applicability Failure
≠
Single Trade Loss
```

を維持する必要がある。

---

## Case 10 — 日本語Research Reportへ出力

### A

Research Noteから出力しやすいが、Research途中の未検証結論を公開しないGateが必要。

### B

Relation Graph / causal narrativeを説明しやすい。

Risk:
Model上のRelationを確定事実として表現しないこと。

### C

Validated KnowledgeからReportへ投影しやすい。

Risk:
Research过程 / uncertaintyが落ちる可能性。

### D

C21を内部Coreの外側に置き、

```text
Research Asset / Knowledge
↓
Traceable Projection
↓
Human Output
```

としやすい。

Phase 4 Finding:

```text
Publication Output
≠
Knowledge Source of Truth
```

を維持する。

---

# 12.4 Cross-Case Findings

10 Caseを通して、4案すべてから以下が強く支持された。

## Finding 1 — Two-Speed Architecture Requirement

市場理解OSには少なくとも二つの速度が必要。

```text
Slow / Evidence Path
=
Research
Validation
Knowledge formation
Revalidation

Fast / Safety Path
=
Current monitoring
Risk restriction
Position protection
Emergency response
```

重要:

```text
Fast Safety
≠
Fast Unvalidated Knowledge Promotion
```

Researchを待たないSafetyは必要だが、未検証Hypothesisを即Productionへ入れることとは別。

## Finding 2 — Relation Modelは共通言語として有望だが、Final Authorityにはしない

C03は重要。

ただし:

```text
Relation Model
≠
Truth
≠
Research Result
≠
Knowledge
≠
Trade Permission
```

Relation / FoundationはResearch Question生成とCurrent Understandingに強い共通言語候補。

World ModelそのものをOS中心Authorityにすると膨張Riskが高い。

## Finding 3 — ResearchはTruth-Seeking Coreとして重要だが、全責任を支配させない

Researchは、

- Proactive discovery
- Reactive investigation
- Validation
- Refutation
- Replication
- Boundary discovery

に強い。

しかし:

```text
Research
≠
Runtime Safety
≠
Capital Permission
≠
Execution
```

Research-centered思想はResearch Domain内部では強く保持できるが、Whole OS中心Authorityにはしない方が安全な可能性が高い。

## Finding 4 — Knowledgeは中心資産だが、世界を見るLensを独占させない

Knowledgeは長期資産の中心候補。

しかし:

```text
Current Observation
→ 既存Knowledgeへ当てはめるだけ
```

ではUnknown / Novel Structureを見落とす。

そのためOpen Discovery / unexplained observation pathが必要。

## Finding 5 — Production Safetyは独立責任が必要

10 Case中、規制暴落・API障害・AI停止・Knowledge conflictで共通して、

```text
Research Confidence
≠
Risk Permission
```

が必要。

Capital / Risk / Execution / Position Protectionは研究・Knowledgeから独立したAuthority Boundaryを必要とする方向が強く支持された。

## Finding 6 — Feedback RouterはWhole OSの重要接続点

Unexpected Resultを全部Trainerへ送るのではなく、

```text
Data
Understanding
Research
Knowledge
Applicability
Decision
Capital
Execution
System
```

のどこへ戻すかを分類できる必要がある。

C18はArchitecture上重要な責任候補。

## Finding 7 — Cross-CuttingはLayer化せずPolicy / Shared Capabilityとして扱う方が自然

Time / Trace / Version / Authority / Security / Monitoring等をMain Flowへ並べると意味が壊れる。

```text
X01-X11
=
all-domain constraints / services / governance capabilities
```

として扱う方向が4案すべてで自然だった。

---

# 12.5 Candidate Character After Stress

## A Research-Centered

Stress後の評価:

- Research Domain architectureとして非常に強い
- Whole OS architectureにするとResearch過剰・Safety遅延Risk
- 採用するなら「Whole OS」ではなくResearch Core設計思想として再利用価値が高い

## B Relation / World-Model-Centered

Stress後の評価:

- C03 / C04設計思想として非常に強い
- Multi-Market / Proactive Question generationに強い
- Whole OS centerにするとOntology / Graph / world-model膨張Riskが高い
- Relation ModelはCommon Language / Perception Foundationとして再利用価値が高い

## C Knowledge-Loop-Centered

Stress後の評価:

- C09-C11 / C19長期資産思想として非常に強い
- Knowledge lifecycle / decay / publicationに強い
- Whole OS centerにするとKnown-Knowledge Biasが出る
- Knowledge System設計思想として再利用価値が高い

## D Multi-Core Hybrid

Stress後の評価:

- Whole OS responsibility separationに最も自然
- Two-speed Research / Safetyを表現しやすい
- Failure routingが明確
- A/B/Cの強みを専用Domainとして取り込める
- 最大RiskはContract / Object / State過多による官僚化

重要:

```text
Dが最終採用
```

とはまだ決定しない。

Phase 5ではDをそのまま採用するのではなく、

> A / B / Cの強い責任思想を、D型責任分離または別Hybridへどう再構築するか

を比較する。

---

# 12.6 Phase 4 Architecture Learnings

Architecture単位ではなく、再利用すべきDesign Principle候補として以下をPhase 5へ送る。

```text
P1 Relation / Foundation
= 共通市場理解言語候補
≠ Truth Authority

P2 Research
= Common Research Core候補
≠ Whole Runtime Authority

P3 Knowledge
= Long-term semantic asset候補
≠ Exclusive perception lens

P4 Capital / Production
= Independent real-capital authority candidate

P5 Feedback
= Cross-domain failure routing candidate

P6 Cross-Cutting
= horizontal capability / governance candidate
≠ normal sequential layer

P7 Whole OS
= Two-speed system candidate
  Evidence / Learning path
  Runtime / Safety path

P8 Human-readable Publication
= Derived projection
≠ internal source of truth
```

---

# 12.7 Phase 4 State

```text
Phase 1 — Source Extraction
COMPLETE

Phase 2 — Design Intent
COMPLETE / WORKING RECONSTRUCTION BASELINE

Phase 3 — Capability Map
COMPLETE / WORKING RECONSTRUCTION BASELINE

Phase 4 — Multiple Blank Architecture Candidates
COMPLETE / WORKING RECONSTRUCTION BASELINE

Phase 5 — Reconstruction
NEXT
```

重要:

```text
Phase 4 Stress Result
≠
Architecture Adoption

Candidate D strongest fit in several stress cases
≠
Candidate D is Final Architecture

Phase 5
=
Concept / Responsibility level Reconstruction
```


---

# 13. Checkpoint 006 — Phase 5 Reconstruction / Top-Level Responsibility Pass

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Current Reconstruction Stage:** Phase 5 ACTIVE

## 13.1 Reconstruction Rule

Phase 5ではConcept名を保存することを目的にしない。

```text
Original Concept Name
↓
Original Intent
↓
Capability Served
↓
Problem / Overlap
↓
Reconstruction Decision Candidate
↓
Replacement Responsibility
```

で再構築する。

判定:

```text
KEEP
REDESIGN
SPLIT
MERGE
DROP
DEFER
NEW
```

はWorking Candidateであり、Phase 6 Destruction Review前の最終採用ではない。

---

# 13.2 Top-Level Responsibility Reconstruction Candidate

Phase 3 Capability MapとPhase 4 Stress結果を基に、Whole OSを以下の責任群として再構築する候補を置く。

```text
R1 Perception / Relation / Current Understanding
R2 Research
R3 Knowledge / Applicability / Decision Preparation
R4 Capital / Production
R5 Learning / Feedback
R6 Long-Term Foundation / Operations / Human Projection
X  Cross-Cutting Capabilities
```

重要:

```text
R1-R6
≠
Final Layers
≠
Python packages
≠
Processes
≠
DB schemas
```

責任再構築のためのWorking Skeleton。

---

# 13.3 R1 — Perception / Relation / Current Understanding

## Original Intents Recovered

Legacy:
- Observation / Feature / MarketEvent / MarketContextを分離
- CauseCandidateを原因確定と分離
- Market DNAで現在市場と過去状態を比較したい

Current:
- Qualified ObservationからCurrent Market Understandingを作る
- Observation / Feature / Context / Interpretationを分離
- Current Understanding自身はResearch / Trade / Riskを行わない

Daisuke Proposal:
- 人間の「関係性による理解」を形式化する
- Flow / Constraint / Propagation / Lag等を共通言語候補にする
- 世界・経済の基礎をResearchの土台として利用する

Phase 4:
- Relation/Foundationは有望
- ただしWorld ModelをTruth Authorityにしない
- Relation Modelの無制限膨張を防ぐ
- Current SafetyはResearch完了を待たない

## Reconstruction Candidate

```text
External / World Observation
↓
Observation Integrity
↓
Relation / Foundation Context
+
Current Observation Context
↓
Current Market Understanding
↓
├─ Research Question sources
├─ Runtime Context
└─ Unexplained / Contradiction / Cause Candidate sources
```

### Concept Decisions

```text
Observation semantics
→ KEEP

Observation Integrity
→ KEEP

Current Market Understanding
→ KEEP / REDESIGN
  Relation/Foundation Contextを利用可能にする
  Prediction / Signal / Trade Authorityは持たない

Market Intelligence
→ REDESIGN
  独立最上位Engineとして固定せず、
  Current Understandingを作るInterpretation / synthesis responsibilityへ吸収候補

World Economic Library
→ REDESIGN / MERGE
  「Library」という物理構造を固定しない
  Relation / Foundation Representation責任へ統合候補

Research Foundation
→ MERGE
  Research専有物ではなく、R1の共有Foundation/Relation Contextへ寄せる候補

Cause Candidate
→ KEEP semantics / REDESIGN placement
  Current Understandingから生成され得るResearch Question sourceの一種
  原因確定ではない
  全Market Understanding cycleで必須生成にはしない

Causal Engine
→ SPLIT
  Candidate generationはR1/R5側
  causal validation / confounder / temporal order等はR2 Research側

Market DNA
→ REDESIGN / DEFER exact form
  保存するのは「Current Market Stateを比較可能に表現する能力」
  Market DNAという名称・Object・EngineをRequired Architectureにはしない

Market DNA Snapshot
→ DEFER exact object
  C04 Current Market Understandingのrepresentation candidateとしてPhase 6以降再評価

Feature / Derived Context
→ KEEP responsibility
  HOW / object granularityは後
```

## R1 Key Boundary

```text
Relation/Foundation
≠ Truth

Current Understanding
≠ Hypothesis Proof
≠ Knowledge
≠ Signal
≠ Trade Permission
```

---

# 13.4 R2 — Research

## Original Intents Recovered

Legacy:
- ResearchCandidate / Intake / Routing / Plan / Trial / Validation
- Evidence independence
- Stress / Failure Boundary
- causal research
- Result Validation

Current:
- Research ResultとKnowledgeを分離
- Research Candidateを共通入口へ
- Historical / OOS / Forward / Stress / Refutation / Alternativeを扱う
- Process FailureとHypothesis Refutationを分離

Research Institute Reference:
- Proactive + Reactive entry
- Research Question
- Exploratory / Confirmatory / Replication
- Research Ledger
- Red Team
- Open Discovery
- External Research Replication

Daisuke Proposal:
- Foundationから通常市場も研究
- 異常・矛盾・失敗も研究
- reverse investigationで新しい原因候補を作る

Phase 4:
- Research-centered思想はResearch Domain内部で非常に強い
- Whole Runtime Authorityにはしない
- Researchを待たないRuntime Safetyが必要

## Reconstruction Candidate

```text
Multiple Question Sources
↓
Research Question
↓
Priority / Admission
↓
Common Research Core
├─ Exploratory
├─ Confirmatory
├─ Replication
├─ Causal / Alternative / Confounder
├─ Stress / Boundary
└─ External Research Replication
↓
Validated Research Result
```

### Concept Decisions

```text
Research Question
→ NEW / KEEP candidate
  Cause Candidateより広いCanonical conceptual entry候補

Research Candidate
→ REDESIGN
  QuestionがResearch queueへ入るAdmission candidateとして配置候補

Research Intake + Priority + Router
→ MERGE / REDESIGN
  C05/C06としてAdmission / Priority / route responsibilitiesを整理

Dual-Entry / Single-Core
→ KEEP principle / REDESIGN
  実際はMulti-Entry / Common Core候補
  Foundation / anomaly / failure / knowledge decay / external research等から入る

Research Plan / Trial / Execution
→ KEEP responsibility

Exploratory / Confirmatory / Replication
→ KEEP distinction candidate

Research Ledger
→ KEEP responsibility
  trial history / search historyを保持

Red Team
→ KEEP responsibility / DEFER exact implementation
  independent challenge roleとして保持
  AI Team固定はしない

Stress Lab
→ MERGE / REDESIGN
  独立Layer必須ではなくResearch Method / Boundary Discovery familyへ

Causal Engine
→ SPLIT
  causal validation methodsをResearch Coreへ

Validated Research Result Boundary
→ KEEP

Research Result → Knowledge direct mutation
→ DROP
  Knowledge admissionを必ず分離
```

## R2 Key Boundary

```text
Research
≠ Runtime Safety
≠ Capital Permission
≠ Execution

Research Result
≠ Knowledge
```

---

# 13.5 R3 — Knowledge / Applicability / Decision Preparation

## Original Intents Recovered

Legacy:
- Knowledge Admission / Record / Relationship / Lifecycle
- Applicability
- Applicable Knowledge Set
- Decision Context / Thesis / EV
- Knowledge ≠ Applicability ≠ Positive EV ≠ Trade Permission

Current:
- Validated Research Result → Knowledge
- Knowledge maintenanceとruntime applicabilityを分離
- Current Understanding / Market contextをApplicabilityで利用
- Knowledge多数決禁止
- Conflict Resolutionは後段責任

Daisuke Proposal:
- 世界/基礎情報とOS自身が得たKnowledgeを分離
- Knowledgeを直接Real Tradeへ使わない
- RuntimeでもKnowledge成立条件を観測する

Phase 4:
- KnowledgeはLong-term semantic assetとして強い
- 既存KnowledgeだけをPerception Lensにしない
- Decision Synthesis独立責任が必要

## Reconstruction Candidate

```text
Validated Research Result
↓
Knowledge Admission / Formation
↓
Knowledge Lifecycle / Revalidation
↓
Current Applicability
↓
Decision Synthesis / Conflict Resolution
↓
Economic Value Assessment
↓
R4 Capital / Production
```

Runtime side:

```text
Current Market Context
↓
Knowledge Assumption Monitoring
↓
Applicability degradation / runtime warning
↓
R4 Runtime Protection and/or R5 Feedback
```

### Concept Decisions

```text
Knowledge Admission
→ KEEP

Knowledge Library / Knowledge Pool
→ MERGE / REDESIGN
  Logical Knowledge Domainとして保持
  物理巨大Store名は固定しない

Knowledge Record / Conditional Knowledge
→ KEEP responsibility

Knowledge Graph
→ REDESIGN
  Canonical duplicate storeではなくView / relationship representation candidate

Knowledge Lifecycle
→ KEEP
  exact state / writer authorityはDEFER

Applicability
→ KEEP

Runtime Knowledge Assumption Monitoring
→ SPLIT responsibility from static/pre-decision applicability
  semanticsは共有するがTwo-Speed pathで別処理候補

Decision Synthesis / Conflict Resolution
→ NEW
  Applicable Knowledge群・opposing thesis・WAIT/UNKNOWNを統合する責任

Expected Value
→ KEEP / REDESIGN
  Decision SynthesisとRiskから分離

Signal Engine
→ DROP as required top-level concept
  Signalは後のHOW / derived output candidate
  CapabilityとしてはDecision Synthesis / EVで代替可能

Knowledge majority vote
→ DROP

Knowledge direct Trade Permission
→ DROP
```

## R3 Key Boundary

```text
Knowledge Valid
≠
Applicable Now

Applicable Now
≠
Decision Candidate

Decision Candidate
≠
Positive Economic Value

Positive Economic Value
≠
Capital Permission
```

---

# 13.6 R4 — Capital / Production

## Original Intents Recovered

Legacy:
- DecisionとDefenseを分離
- RiskState single-writer principle
- Emergency Fast Path
- Execution / Reconciliation
- Logical Position / Protection / Exit
- venue actionとcanonical exposure truthを分離

Current:
- 05 / 06未完成だがApplicability → Decision → Risk → Executionの境界思想あり

Daisuke Proposal:
- Real capitalを長期的に増やす
- DDを抑える
- Trade中もCurrent Marketを監視
- 単純価格StopではなくKnowledge成立条件変化を扱いたい

Phase 4:
- Capital / Productionの独立Authority Boundaryが強く支持
- Two-Speed Runtime Safetyが必要
- API failure / AI failure / market failureを分離

## Reconstruction Candidate

```text
Economic Opportunity
↓
Capital / Portfolio / Risk Permission
↓
Execution Fidelity
↓
Position / Exposure Truth
↓
Runtime Protection / Exit
↓
Outcome
```

Fast Safety Path:

```text
Current Runtime Context
+
System Health
+
Risk State
+
Knowledge Assumption Deviation
↓
Restriction / Reduce / Protect / Stop
```

### Concept Decisions

```text
Decision vs Risk separation
→ KEEP

Capital Allocation / Portfolio Risk
→ NEW / REDESIGN
  Legacy部品を統合しWhole Capital viewを追加

Defense Layer
→ SPLIT / DROP monolithic form
  - capital/risk permission
  - runtime protection
  - emergency restriction
  に責任分解候補

RiskState single-writer principle
→ KEEP principle / DEFER exact object

Emergency Fast Path
→ KEEP / REDESIGN
  Research completionを待たない
  未検証Knowledge promotionとは分離

Execution
→ KEEP

Execution Reconciliation
→ KEEP

Position / Exposure canonical truth
→ KEEP responsibility

Protection / Exit / In-Trade Defense
→ MERGE / REDESIGN under Position / Runtime Protection responsibility

Exchange Adapter as final canonical truth
→ DROP

Production Promotion as Trade Permission
→ DROP legacy meaning
```

## R4 Key Boundary

```text
Research Confidence
≠
Risk Permission

Order Sent
≠
Execution Success

Exchange Response
≠
Canonical Position Truth

Fast Safety
≠
Fast Research Promotion
```

---

# 13.7 R5 — Learning / Feedback

## Original Intents Recovered

Legacy:
- Production Evaluation
- Finding normalization
- Cross-analysis
- Candidate Promotion
- Feedback → Research
- Loss ≠ Thesis Failure
- Finding ≠ Root Cause

Current:
- Post-Analysis → Re-Research
- OutcomeとHypothesis / Thesis / Execution / Riskを分離

Daisuke Proposal:
- Unexpected Resultを単純再学習しない
- 順方向 + 逆方向で原因候補を探索
- 根本原因に応じて適切な場所へ戻す

Phase 4:
- Feedback RouterはWhole OSを閉Loopにする重要接続点
- Reverse InvestigationはRoot Cause AuthorityではなくCandidate generation Method

## Reconstruction Candidate

```text
Outcome / Production Evidence
↓
Decision-Quality / Execution / Risk / Market Evaluation
↓
Finding / Contradiction / Unknown
↓
Failure Classification / Feedback Routing
├─ R1 perception / data
├─ R2 research
├─ R3 knowledge / applicability / decision
├─ R4 capital / execution
└─ X / operations
```

Research route:

```text
Unexpected Outcome
↓
Reverse Investigation
↓
Cause / Explanation Candidates
↓
R2 Formal Research
```

### Concept Decisions

```text
Production Evaluation
→ KEEP / REDESIGN

TradeResult alone as learning signal
→ DROP

Finding concept
→ KEEP semantics / REDESIGN
  Root Causeではなくresearch / correction candidate

Finding Pipeline
→ MERGE into Feedback Routing responsibility

Cross-Analysis
→ KEEP method candidate
  Conflict / relation detection
  Root Cause Authorityではない

Reverse Investigation
→ NEW method
  Candidate generation only

Trainer as universal feedback destination
→ DROP
  Failure-specific routingへ置換

Failure Museum
→ MERGE / REDESIGN
  Negative / failure research assetsとしてC19 / Knowledge domainへ
  独立Top-Level Layer必須ではない

Direct Knowledge mutation from outcome
→ DROP

Counterfactual
→ KEEP method candidate / DEFER exact implementation
```

## R5 Key Boundary

```text
Outcome
≠
Decision Quality

Finding
≠
Root Cause

Reverse Story
≠
Causal Proof

Feedback
≠
Automatic Retraining
```

---

# 13.8 R6 — Long-Term Foundation / Operations / Human Projection

## Original Intents Recovered

Legacy:
- Monitoring / Recovery / Deployment
- Telegram / Outer Control
- Security / Credential / Classification
- State / Approval / Audit / Migration / Backup

Current Charter:
- Research Assetを長期保存
- Human-readable research
- implementationよりmeaning / evidence / historyを残す

Daisuke Proposal:
- long-term storage pressure
- AI / API / Python / market交換
- Debug / API / Error / system monitoring
- Telegram / iPhone control
- Japanese research output

Phase 4:
- X01-X11は横断
- Publicationはderived projection
- Provider / AI / Exchangeをsemantic source of truthにしない

## Reconstruction Candidate

Cross-Cutting:

```text
X01 Time / Temporal Integrity
X02 Trace / Provenance
X03 Version / Lineage
X04 Uncertainty / Calibration
X05 State / Lifecycle Integrity
X06 Authority / Governance
X07 Human Control
X08 Cognitive Assistance Integration
X09 Security / Identity / Credential / Classification
X10 Monitoring / Incident / Recovery
X11 Storage / Retention / Migration
```

Long-term semantic responsibilities:

```text
Research Asset Preservation
Replaceability / Market Extensibility
Human-readable Projection
```

### Concept Decisions

```text
AI Team
→ REDESIGN / DROP monolithic form
  X08 Cognitive Assistanceとして各責任へ接続
  AI consensusをAuthorityにしない

Telegram Interface
→ REDESIGN
  Human Control Adapter候補
  Authorityそのものではない

Monitoring
→ KEEP
  State writer / market interpretation authorityではない

Recovery / Incident
→ KEEP

Security / Credential / Classification
→ KEEP

Auditability
→ MERGE as property from Time + Trace + Version + State + Authority

Research Asset Preservation
→ KEEP / REDESIGN
  raw-data hoardingではなくmeaning / evidence / history preservation

Storage / Retention / Migration
→ NEW / REDESIGN as explicit long-term responsibility

Market-specific extensibility
→ NEW / KEEP intent
  shared OS + market-specific data/method/execution boundary候補

Human-readable Research Projection
→ NEW
  internal SoTを変更しないderived output

Publication as internal Knowledge writer
→ DROP
```

---

# 13.9 First-Pass Reconstruction Skeleton

Phase 5 Working Candidate:

```text
WORLD / MARKET
      ↓
[R1 PERCEPTION / RELATION / CURRENT UNDERSTANDING]
      │
      ├──────────────→ FAST RUNTIME CONTEXT ───────────────┐
      │                                                    │
      ↓                                                    │
Research Question Sources                                  │
      ↓                                                    │
[R2 RESEARCH]                                              │
      ↓                                                    │
Validated Research Result                                  │
      ↓                                                    │
[R3 KNOWLEDGE / APPLICABILITY / DECISION PREPARATION]      │
      ↓                                                    │
Economic Opportunity                                       │
      ↓                                                    │
[R4 CAPITAL / PRODUCTION] ◀────────────────────────────────┘
      ↓
Outcome
      ↓
[R5 LEARNING / FEEDBACK]
      ├→ R1
      ├→ R2
      ├→ R3
      ├→ R4
      └→ Operations / Cross-Cutting

[R6 LONG-TERM FOUNDATION / HUMAN PROJECTION]
supports all

[X01-X11 CROSS-CUTTING]
applies horizontally to all responsibilities
```

Two-speed candidate:

```text
EVIDENCE / LEARNING PATH
R1 → R2 → R3 → R4 → R5

FAST RUNTIME / SAFETY PATH
R1 runtime context + X10 system health + R3 assumption monitoring
→ R4 capital / position protection
```

Important:

```text
Fast Runtime Path
does not create new Knowledge.

Slow Research Path
does not block emergency protection.
```

---

# 13.10 Major Concept Classification — First Pass

| Concept | Phase 5 Candidate | Reconstruction Meaning |
|---|---|---|
| Observation / Quality / Time | KEEP | R1 foundation |
| Current Market Understanding | KEEP / REDESIGN | relation-aware, non-trading understanding |
| Market Intelligence | REDESIGN / MERGE | R1 interpretation responsibility |
| World Economic Library | REDESIGN / MERGE | Relation/Foundation responsibility |
| Research Foundation | MERGE | shared R1 foundation, not Research-only |
| Cause Candidate | KEEP / REDESIGN | optional Research Question source |
| Causal Engine | SPLIT | candidate generation vs formal research |
| Market DNA | REDESIGN / DEFER | preserve state-comparison capability, not mandatory concept |
| Research Question | NEW / KEEP | broad conceptual research entry |
| Research Intake / Router | MERGE / REDESIGN | Priority / Admission / routing |
| Research Core | KEEP / REDESIGN | common multi-entry research |
| Stress Lab | MERGE / REDESIGN | research method / boundary discovery |
| Research Ledger | KEEP | research integrity asset |
| Red Team | KEEP / DEFER implementation | independent challenge responsibility |
| Knowledge Library / Pool | MERGE / REDESIGN | logical Knowledge domain |
| Knowledge Graph | REDESIGN | view / relationship representation |
| Knowledge Lifecycle | KEEP | revalidation / aging |
| Applicability | KEEP | current usability |
| Decision Synthesis | NEW | conflict / action candidate synthesis |
| Expected Value | KEEP / REDESIGN | economic assessment |
| Signal Engine | DROP as top-level requirement | optional later implementation |
| Defense Layer | SPLIT / DROP monolith | risk permission / protection / emergency |
| Capital / Portfolio | NEW / REDESIGN | whole-capital responsibility |
| Execution | KEEP | venue action fidelity |
| Position / Protection | KEEP / REDESIGN | exposure truth + runtime protection |
| Finding Pipeline | MERGE / REDESIGN | feedback routing |
| Reverse Investigation | NEW method | cause candidate generation |
| Trainer universal loop | DROP | failure-specific routing |
| Failure Museum | MERGE / REDESIGN | negative/failure research asset |
| AI Team | REDESIGN / DROP monolith | cognitive assistance |
| Telegram | REDESIGN | human-control adapter |
| Monitoring / Recovery | KEEP | operations |
| Human Research Report | NEW / KEEP intent | derived projection |
| Storage / Migration | NEW / REDESIGN | explicit long-term responsibility |

---

# 13.11 Phase 5 Open Questions Before Concept-Level Reconstruction

以下はまだ決めない。

```text
1. Relation / Foundationは独立Responsibilityか、R1内部Subdomainか
2. Current Market UnderstandingのCanonical representationを何にするか
3. Market DNAというConcept名を残すか
4. Research Question / Candidate / Intakeを何段階にするか
5. Causal ResearchをResearch Method familyとしてどこまで統合するか
6. Knowledge Lifecycle writer / final authority
7. Runtime ApplicabilityとRuntime Protectionのexact boundary
8. Decision SynthesisのOutput semantics
9. EVとCapital Allocationのexact handoff
10. Capital / Portfolio / Riskを一つのresponsibilityにするか分割するか
11. Runtime Protectionのemergency authority
12. Feedback Routerのclassification authority
13. Relation/FoundationとKnowledgeのrelationship storageを共通化するか
14. Human / AI / Production final authority
15. Market-specific extension contract
```

---

# 13.12 Phase State

```text
Phase 5 — Reconstruction
STATUS:
ACTIVE

Top-Level Responsibility Pass:
COMPLETE

NEXT:
Concept-Level Reconstruction Matrix
starting with R1:
Perception / Relation / Current Understanding
```

重要:

```text
Reconstruction Skeleton
≠
Final Architecture

Phase 5 Candidate
≠
KEEP decision after Destruction Review

Market DNA / Causal Engine / World Economic Library etc.
remain replaceable HOW / concept candidates until Phase 6.
```


---

# 14. Checkpoint 007 — Phase 5 R1 Concept-Level Reconstruction

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction  
**Scope:** R1 — Perception / Relation / Current Understanding

## 14.1 R1 Purpose Candidate

R1の責任候補:

> 外部世界・市場から得たObservationを、品質・時間・Source・市場文脈を失わず整理し、共通Relation / Foundationを参照しながら「現在市場で何が起きているか」を説明可能な状態へ変換し、Research・Runtime・Applicabilityへ渡す。

R1は以下を行わない。

```text
Hypothesisを立証しない
Causeを確定しない
Knowledgeを生成・承認しない
Expected Valueを計算しない
Capital Permissionを出さない
Tradeを決定しない
Executionを行わない
```

---

# 14.2 Epistemic Status Separation

R1で最重要の分離候補:

```text
Observation
≠ Derived Measurement
≠ Relation Vocabulary
≠ Foundation Claim
≠ Current Relation Interpretation
≠ Cause Candidate
≠ Hypothesis
≠ Knowledge
```

この身分差を失うと、

```text
経済の一般論
↓
Current Market Fact扱い

AI Interpretation
↓
Knowledge扱い

Current Correlation
↓
Cause扱い
```

が発生するため、R1では意味境界を強く保持する。

---

# 14.3 Observation

## Decision Candidate
KEEP

Observationは市場理解OSの事実入力として残す。

最低限の意味:

```text
何が観測されたか
どのSourceか
いつ起きた / 公開された / 取得されたか
Quality / Freshnessはどうか
```

重要:

```text
Observation
≠ Interpretation
```

Raw / Normalized / Qualifiedの具体Object構造は後続Contractで決める。

---

# 14.4 Market Event

## Decision Candidate
SPLIT / MERGE

旧MarketEventという一語は曖昧。

以下を分ける候補:

```text
A. Observed Event
= 外部Sourceから得たEvent fact
→ Observation familyへMERGE

B. Detected / Interpreted Market Event
= 複数ObservationからOSが認識した市場現象
→ Current Understanding / Derived Interpretation側
```

例:

```text
規制当局が発表した
= Observed Event

その発表後にSpot売り + Liquidation + Liquidity低下が同時発生し、
市場がregulation shock状態にある
= Interpreted Market Event
```

「MarketEvent」という単一身分で両者を混ぜない。

---

# 14.5 Feature / Derived Measurement

## Decision Candidate
KEEP / REDESIGN

FeatureはR1で必要。

ただし定義を狭める。

```text
Feature / Derived Measurement
=
Observationから再現可能な測定・変換
```

例:

```text
Return
OI change
Funding change
Spread
Imbalance
Volatility
Divergence
Velocity
```

重要:

```text
Feature
≠ Interpretation
≠ Knowledge
```

Feature Combinationの探索自体をResearch Resultとみなさない。

---

# 14.6 Context

## Decision Candidate
SPLIT

Contextは曖昧語なので一つのConceptにしない。

候補:

```text
Observation Context
=
Asset / Market / Venue / Time / Source / Quality / Freshness等、
Observationを比較可能にする文脈

Current Market Context
=
現在市場Understandingを構成する解釈済みContext

Runtime Context
=
Applicability / Capital / Position protectionが現在参照するContext
```

同じContext Objectへ全意味を詰め込まない。

---

# 14.7 Relation Vocabulary

## Decision Candidate
NEW / KEEP from Daisuke Intent

ダイスケ案の人間的な「関係性による市場理解」を残すため、
Relationを共通語彙として持てる責任をR1へ置く候補。

初期候補:

```text
Flow
Distortion / Imbalance
Cycle
Propagation
Amplification
Constraint / Bottleneck
Substitution / Redistribution
Stock / Accumulation
Expectations
Lag
Threshold / Regime Shift
Equilibrium / Arbitrage
```

重要:

```text
Relation Vocabulary
=
関係を表現する言葉・型

Relation Vocabulary
≠
「その関係が現在成立している」という主張
```

Relation一覧はまだ最終固定しない。

---

# 14.8 Relationの3身分分離

Relationを一種類にしない。

## A. Relation Definition / Vocabulary

```text
Flowとは何を意味するか
Propagationとは何を意味するか
```

共通言語。

## B. Foundation Relation Claim

```text
市場・経済を研究するための背景的な関係主張
```

例:

```text
金利上昇はCredit Costへ影響し得る
FundingはPerpetual市場構造の一部である
```

TruthではなくEpistemic Statusを持つ。

## C. Current Relation Interpretation

```text
今の市場でどのRelationが成立している可能性があるかというCurrent Interpretation
```

例:

```text
現在、ETFからBTC Spotへの資金Flowが強い可能性
```

重要:

```text
Vocabulary
≠ Foundation Claim
≠ Current Interpretation
```

---

# 14.9 Foundation

## Decision Candidate
REDESIGN / MERGE

```text
世界経済図書館
+
Research Foundation
```

を物理Libraryとして二重に固定しない。

保持する本質:

> Feature総当たりからResearchを始めず、市場・経済・Instrument・Participant・Mechanism等の背景理解をResearch priorとして利用できること。

Foundation候補内容:

```text
Instrument Mechanics
Market / Trading Mechanics
Participant Model
Basic Economics / External Context
Relation Definitions
Trading Benchmark / Archetype
Market-specific background
```

ただし:

```text
Foundation
≠ Production Knowledge
≠ 永久の真実
```

---

# 14.10 Foundation Epistemic Status

## Decision Candidate
KEEP / REDESIGN

Research Referenceの候補を保持する価値が高い。

```text
STRUCTURAL FACT
SUPPORTED MECHANISM
WORKING MODEL
HEURISTIC
UNKNOWN
```

ただし正式Enumは後で決める。

目的:

```text
制度上明確な仕組み
と
経験則
と
未検証説明
```

を同じ確度で扱わない。

Foundation自身もResearch対象になり得る。

---

# 14.11 Foundation Relevance Gate

## Decision Candidate
NEW

World-model explosion対策として新しい責任候補。

Foundationは世界中の全情報を常時Current Understandingへ投入しない。

概念:

```text
Target Market / Research Question / Current Context
↓
Relevant Foundation Selection
↓
R1 / R2へ供給
```

目的:

- 世界情報無限膨張を防ぐ
- Crypto Firstを維持
- Research Noiseを減らす
- Market追加時にMarket-specific Foundationを差し替え可能にする

重要:

```text
Foundation exists
≠
Foundation is relevant now
```

---

# 14.12 Current Market Understanding

## Decision Candidate
KEEP / REDESIGN

R1の主要Outputとして残す。

定義候補:

> Qualified Observation、Derived Measurement、Relevant Foundation、Relation Interpretation、Quality / Time / Uncertaintyを用いて、「今この市場で何が起きているとOSが理解しているか」を表現するCurrent Interpretation。

重要:

```text
Current Market Understanding
≠ Future Prediction
≠ Hypothesis
≠ Confirmed Cause
≠ Knowledge
≠ Signal
≠ Trade Decision
```

UNKNOWN / MIXED / INSUFFICIENTを許す。

---

# 14.13 Market Intelligence

## Decision Candidate
MERGE / REDESIGN

Market Intelligenceを独立Top-Level Engine必須とはしない。

残す責任:

```text
複数Observation
+
Derived Measurement
+
Relevant Foundation
+
Relation Vocabulary
↓
Current Market Understandingを形成するsynthesis / interpretation
```

したがって:

```text
Market Intelligence
=
R1内部のInterpretation capability candidate
```

名称を後で残すかはPhase 6以降。

---

# 14.14 Contradiction

## Decision Candidate
KEEP semantics / REDESIGN placement

ContradictionはCurrent Understandingが単一結論へ無理に収束しないために必要。

候補:

```text
Observation vs Observation
Observation vs Foundation expectation
Current Interpretation vs Current Interpretation
Current Understanding vs existing Knowledge expectation
```

ただし最後のKnowledge contradictionはR3/R5との共有責任候補。

R1で扱うのは主に、

> Current perception上の説明不整合を記録し、Research Question sourceへ渡す。

Contradiction
≠ Cause
≠ Refutation completed.

---

# 14.15 Unexplained / Unknown

## Decision Candidate
KEEP / STRENGTHEN

Current Understandingは説明不能を正式状態として保持できる必要がある。

```text
UNKNOWN
MIXED
UNCERTAIN
INSUFFICIENT
UNEXPLAINED
```

正式state名は後。

目的:

```text
説明できない
↓
既存Foundationへ無理に当てはめる
```

ことを防ぎ、Open Discovery / Research Questionへ送る。

---

# 14.16 Cause Candidate

## Decision Candidate
KEEP semantics / REDESIGN placement

Cause Candidateは残すが、R1の必須Outputにはしない。

```text
Current Understanding
↓
Explanation / Causal Questionが必要な場合
↓
Cause Candidate(s)
↓
R2 Research
```

重要:

```text
Cause Candidate
≠ Research Question全般
≠ Confirmed Cause
≠ Hypothesis Result
≠ Knowledge
```

Cause Candidateを生成しない研究も正式に許可する。

---

# 14.17 Causal Engine

## Decision Candidate
SPLIT

R1側:

```text
Cause Candidate generation
Alternative explanation generation
```

R2側:

```text
Temporal order
Lag validation
Confounder analysis
Alternative hypothesis
Contradiction
Evidence
Historical / OOS / Forward
Causal / empirical research
```

巨大な単一Causal EngineとしてArchitecture必須にはしない。

---

# 14.18 Current Market State Representation / Market DNA

## Decision Candidate
Capability KEEP / Market DNA DEFER

必要能力:

> Current Market Understandingを、Historical Case / Research / Applicabilityが比較可能な形へ投影すること。

候補軸:

```text
Trend
Volatility
Liquidity
Leverage
Funding
Flow
Participant State
Macro
Session / Time
```

しかし:

```text
Market DNA
という名前
DNA Definition
DNA Snapshot
Vector形式
Score形式
Similarity Formula
```

はまだ固定しない。

重要:

```text
State similarity
≠
Hypothesis support
≠
Applicability proof
≠
Signal
```

Current Market State Representationは
Current Understandingの全内容そのものではなく、
比較用途へのprojection候補として扱う方が自然。

---

# 14.19 R1 Outputs Candidate

R1から同じOutputを全Downstreamへ送らない。

候補:

## R1 → R2 Research

```text
Research Question Source
Contradiction
Unknown / Unexplained
Cause Candidate
Current Understanding Context
Relevant Foundation Context
State Representation / Case Context
```

## R1 → R3 Knowledge / Applicability

```text
Current Market Understanding
Current State Representation candidate
Quality / Time / Uncertainty Context
Relevant current relation interpretation
```

## R1 → R4 Fast Runtime / Safety

```text
Runtime Market Context
Material Change / Deviation indicators
Quality / Freshness degradation
Relevant market-state change
```

重要:

```text
R1 → R4
does not mean
R1 can issue Trade Permission.
```

---

# 14.20 R1 Candidate Flow

```text
External World / Market
        ↓
Observation
        ↓
Observation Integrity / Time / Quality
        ↓
Observation Context
        ↓
Derived Measurement
        ↓
        ├─────────────────────────────┐
        │                             │
Relevant Foundation / Relation       │
        │                             │
        └──────────────┬──────────────┘
                       ↓
             Current Interpretation
                       ↓
             Current Market Understanding
              ┌────────┼──────────────┐
              │        │              │
              ↓        ↓              ↓
        Contradiction  Unknown   State Representation
              │        │              │
              └──┬─────┘              ├→ R3
                 ↓                    └→ R2
        Research Question Source
                 ↓
             Cause Candidate
             only when relevant
                 ↓
                R2

Parallel:
Current Market Understanding
→ Runtime Market Context
→ R4 Fast Safety
```

Foundation / RelationはCurrent Observationと同じFact streamとして扱わない。

---

# 14.21 Concept Classification — R1

| Concept | Phase 5 R1 Candidate |
|---|---|
| Observation | KEEP |
| Raw / Qualified distinction | KEEP responsibility |
| Market Event | SPLIT / MERGE into observed vs interpreted |
| Feature / Derived Measurement | KEEP / REDESIGN |
| Context | SPLIT |
| Relation Vocabulary | NEW / KEEP intent |
| Foundation Relation Claim | NEW / REDESIGN |
| Current Relation Interpretation | NEW / REDESIGN |
| World Economic Library | REDESIGN / MERGE |
| Research Foundation | MERGE into shared Foundation responsibility |
| Foundation Epistemic Status | KEEP / REDESIGN |
| Foundation Relevance Gate | NEW |
| Market Intelligence | MERGE / REDESIGN |
| Current Market Understanding | KEEP / REDESIGN |
| Contradiction | KEEP / REDESIGN |
| Unknown / Unexplained | KEEP / STRENGTHEN |
| Cause Candidate | KEEP semantics / REDESIGN placement |
| Causal Engine | SPLIT |
| Market DNA | DEFER exact concept |
| Current Market State Representation | KEEP capability / REDESIGN |
| Signal / Prediction in R1 | DROP |
| Trade / Risk authority in R1 | DROP |

---

# 14.22 R1 Open Questions for Phase 6 / Detailed Design

```text
1. Relation Vocabularyの正式最小集合
2. Relation DefinitionとFoundation Claimのstorage分離
3. Foundation ClaimのEpistemic Status正式Enum
4. Foundation Source / Evidence provenance
5. Foundation Relevance Gateの選別原則
6. Current Relation Interpretationを独立Objectにするか
7. Current Market Understandingのminimum semantic contract
8. Contradictionの責任範囲
9. Unknown / Unexplainedのstate taxonomy
10. Cause Candidate生成条件 / 禁止条件
11. State Representationが必要な最小軸
12. Market DNA名称を残す価値
13. Current Understanding → Runtime Contextのmaterial-change判定
14. Foundation変更がCurrent Understandingへ与えるversion影響
15. Market-specific Foundation extension contract
```

---

# 14.23 Phase State

```text
Phase 5 R1 Concept-Level Reconstruction
COMPLETE / WORKING CANDIDATE

NEXT:
R2 Research Concept-Level Reconstruction
```

重要:

```text
R1 COMPLETE
≠
Final R1 Architecture

World Economic Library MERGE candidate
≠
Daisuke intent dropped

Market DNA DEFER
≠
state comparison capability dropped

Causal Engine SPLIT
≠
causal research dropped
```


---

# 15. Checkpoint 008 — Phase 5 R2 Concept-Level Reconstruction

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction  
**Scope:** R2 — Research

## 15.1 R2 Purpose Candidate

R2の責任候補:

> 市場理解OS内外から生まれる「何を知りたいか」というQuestionを正式研究へAdmissionし、再現可能なResearch Planへ変換し、探索・確認・再現・因果・経験・Stress・反証・Alternative等のMethodを用いてEvidenceを収集・統合し、成立条件・失敗条件・不確実性・未解決点まで含むValidated Research Resultへ変換する。

R2は以下を行わない。

~~~text
Current Marketを直接Trade Signalへ変換しない
Knowledgeを自動採用しない
Capital Permissionを出さない
Executionを行わない
Runtime Safetyを支配しない
AI意見をEvidence扱いしない
~~~

---

# 15.2 Research Entry — Research Question

## Decision Candidate
NEW / KEEP

Research QuestionをR2の最上位Conceptual Entry候補として採用する。

定義候補:

> 何を知りたいのか、何が分からないのか、何を確認・反証・再現したいのかを表す研究上の問い。

Source候補:

~~~text
Foundation / Relation
Current Market Understanding
Open Discovery
Contradiction
Unknown / Unexplained
Cause Candidate
Knowledge contradiction
Knowledge decay
Applicability contradiction
Unexpected Outcome
Failure
External Research
Market Expansion
Periodic Revalidation
~~~

重要:

~~~text
Research Question
≠ Research Candidate
≠ Hypothesis
≠ Research Result
~~~

Question自体は研究価値を意味しない。

---

# 15.3 Research Question Type

## Decision Candidate
KEEP / REDESIGN

全ResearchをCause Researchへ押し込まない。

候補:

~~~text
EXPLANATION
CAUSAL
EMPIRICAL
STATE
BOUNDARY
GENERALIZATION
FAILURE
REPLICATION
DISCOVERY
~~~

正式Enumは後。

目的:

- 原因研究だけでなく再現可能な経験則研究を許す
- Failure診断を正式研究として扱う
- Open Discoveryを正式入口にする
- Research Intentに応じてPlan / Methodを変えられるようにする

---

# 15.4 Research Candidate

## Decision Candidate
REDESIGN

Research CandidateはQuestionより後に置く。

定義候補:

> Research Questionを「今、正式研究へ進める価値がある対象」として審査可能にしたAdmission対象。

~~~text
Research Question
↓
Research Candidate
↓
Admission / Priority
~~~

Candidateは、

~~~text
何が発見されたか
Origin
Market / Asset
Time
Current Context
Relevant Foundation
Evidence availability
Existing research relationship
Potential impact
Risk relevance
Research cost
~~~

等を追跡可能にする。

重要:

~~~text
Question exists
≠ Candidate admitted

Candidate exists
≠ Research starts
~~~

---

# 15.5 Research Intake / Admission / Priority

## Decision Candidate
MERGE / REDESIGN

旧:

~~~text
Research Intake
Research Router
Prioritization
~~~

を責任として整理する。

候補Flow:

~~~text
Research Candidate
↓
Admission
├ ACCEPT
├ DEFER
├ MERGE
├ REJECT
└ NEED MORE CONTEXT
↓
Priority / Scheduling
↓
Research Design
~~~

研究しない判断も正常なOutput。

評価候補:

~~~text
Research value
Economic relevance
Risk relevance
Unknown severity
Novelty
Repeated occurrence
Evidence availability
Data quality
Research cost
Expected reuse
Urgency
Existing duplicate research
~~~

重要:

~~~text
High curiosity
≠ High research priority
~~~

---

# 15.6 Routing Axes

## Decision Candidate
REDESIGN / KEEP principle

Research Routerを単一Method選択器にしない。

研究を少なくとも以下の別軸として扱える候補:

~~~text
Research Domain
Research Intent
Research Mode
Research Method
~~~

例:

~~~text
Domain:
Market Microstructure

Intent:
Empirical Relationship

Mode:
CONFIRMATORY

Methods:
Historical + OOS + Regime Stability
~~~

重要:

~~~text
1 Question
≠ 1 Method
~~~

---

# 15.7 Research Mode

## Decision Candidate
KEEP / STRENGTHEN

正式に分離する価値が高い。

~~~text
EXPLORATORY
= 何があるか探す

CONFIRMATORY
= 事前Question / Hypothesis / Evaluationを固定して確認

REPLICATION
= 別期間 / Asset / Venue / Regime等で再現確認
~~~

最重要原則:

~~~text
発見
≠ 確認
≠ 再現
~~~

探索Dataを見た後で、同じDataを事前仮説検証として扱わない。

---

# 15.8 Research Plan

## Decision Candidate
KEEP / STRENGTHEN

Research PlanをCommon Research Coreの中心責任候補とする。

目的:

> Questionを再現可能な実験仕様へ変換する。

候補内容:

~~~text
Research Question
Claim / Hypothesis
Research Mode
Methods
Data
Feature / Formula
Comparison
Benchmark
Evidence Channels
Evaluation Rules
Refutation Rules
Alternative Hypotheses
Stress
Failure Criteria
Temporal rules
Version
~~~

重要研究では、結果を見る前にPlan Freezeを行える候補を持つ。

Materialな変更:

~~~text
Plan v1
↓
結果を見て変更
↓
Plan v2
~~~

としてVersion管理し、v1を上書きしない。

---

# 15.9 Hypothesis / Claim

## Decision Candidate
KEEP / REDESIGN

Hypothesisは、

> 検証・反証可能な形へ整理された研究上の主張。

ただし、すべてのResearch Questionが同じHypothesis形式を必要とするとは限らないため、上位概念としてClaimを許容する候補を残す。

候補:

~~~text
Causal Hypothesis
Empirical Hypothesis
Mechanism Hypothesis
Regime Hypothesis
Failure Hypothesis
Comparison Claim
Replication Claim
~~~

重要:

~~~text
Hypothesis
≠ Evidence
≠ Result
≠ Knowledge
~~~

現在市場に都合よく書き換えない。

---

# 15.10 Research Trial / Experiment

## Decision Candidate
KEEP

Planに基づく実行単位。

Trial候補:

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
State Representation Comparison
~~~

重要:

~~~text
Research Method
≠ Trial / Experiment Mode
≠ Evidence Channel
~~~

を維持する。

---

# 15.11 Causal / Empirical Research

## Decision Candidate
KEEP / MERGE into Method Family

Causal Engineを独立巨大Architectureにせず、Research Method familyへ統合候補。

### Causal Research

見るもの:

~~~text
Mechanism
Temporal Order
Lag
Confounder
Alternative Hypothesis
Common Cause
Contradiction
Counter Evidence
~~~

### Empirical Research

見るもの:

~~~text
条件付き再現性
Effect Size
Stability
OOS
Forward
Regime Dependence
Cost-adjusted behavior
~~~

重要:

~~~text
綺麗な因果説明
≠ Profitability

因果が完全証明できない
≠ Empirical Edge不存在
~~~

---

# 15.12 Evidence Model

## Decision Candidate
KEEP / STRENGTHEN

Evidenceを一つのScoreや総件数へ潰さない。

### Evidence Channel候補

~~~text
Runtime / Observational
Historical
OOS
Forward
Stress
Production / Live
~~~

### Evidence Role候補

~~~text
Supporting
Contradicting
Discriminating
Conditioning
Boundary
Contextual
Process Validation
~~~

### Evidence Outcome候補

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
≠ Evidence Strength
~~~

---

# 15.13 Evidence Independence / Dependency

## Decision Candidate
KEEP / STRENGTHEN

複数Evidenceが同じData / Event / Causeから派生している場合、独立確認として水増ししない。

~~~text
Evidence Count
≠ Independent Evidence Count
≠ Evidence Strength
≠ Hypothesis Truth
~~~

Shared Evidence / Dependencyを追跡可能にする。

---

# 15.14 Research Ledger

## Decision Candidate
KEEP / STRENGTHEN

Research Resultだけではなく、探索履歴をResearch Integrityの一部として保存する。

候補:

~~~text
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
Window Changes
Final Results
~~~

目的:

~~~text
1回試して成功
~~~

と、

~~~text
100000回試して最良1個だけ成功
~~~

を区別する。

重要:

~~~text
Research Result
≠ Research History
~~~

Research LedgerはCherry-picking / Data Snooping / Hidden Search Space対策として重要。

---

# 15.15 Red Team / Independent Challenge

## Decision Candidate
KEEP responsibility / DEFER implementation

Hypothesisを作る責任と壊す責任を概念上分離する。

Challenge候補:

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
Researcher self-approval only
~~~

に依存しない。

別AI / 別Module / Human / Ruleのどれで実現するかは後。

---

# 15.16 Stress / Boundary Research

## Decision Candidate
MERGE / STRENGTHEN

Stress Labを独立Top-Level Layer必須にしない。

R2内のBoundary Discovery Method familyとして扱う候補。

目的:

> Hypothesis / Edgeを守るのではなく、どこから壊れるかを能動的に探す。

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

Output候補:

~~~text
Failure Boundary
Constraint Candidate
Unknown
New Research Question
~~~

重要:

~~~text
Stress Failure
≠ Entire Hypothesis always false
~~~

条件付き成立を明確にする。

---

# 15.17 Failure Boundary / Constraint Candidate

## Decision Candidate
KEEP / REDESIGN

研究成果は「成功条件」だけではなく「利用禁止 / 壊れる条件」を持つ。

候補Dimension:

~~~text
Regime
Volatility
Liquidity
Leverage
Time Horizon
Session
Macro Condition
Data Quality
Event Condition
Venue
Participant Structure
~~~

重要:

~~~text
Research Constraint Candidate
≠ Runtime Authorized Constraint
~~~

R2は研究上の制約候補まで。

Productionで強制するAuthorityはR4 / X06側。

---

# 15.18 Alternative / Contradiction / Confounder

## Decision Candidate
KEEP / STRENGTHEN

ResearchはHypothesisを守るための場所ではない。

必ず扱える方向を持つ:

~~~text
Alternative Hypothesis
Confounder
Contradiction
Temporal inconsistency
Common Cause
Counter Evidence
Regime failure
~~~

Cause Candidateが複数ある場合も多数決しない。

---

# 15.19 Research Synthesis

## Decision Candidate
KEEP / STRENGTHEN

複数Evidenceを一つの投票へ潰さない。

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

Synthesis候補:

~~~text
Channel
Role
Independence / Dependency
Quality
Coverage
Contradiction
Failure Boundary
Regime
Alternative Explanation
Uncertainty
~~~

SynthesisはResultを作るための統合責任。

---

# 15.20 Research Result

## Decision Candidate
KEEP / REDESIGN

Research Resultは二値にしない。

候補意味:

~~~text
SUPPORTED
SUPPORTED WITH BOUNDARY
WEAK SUPPORT
REGIME DEPENDENT
MIXED
CONTRADICTED
REFUTED
INCONCLUSIVE
INSUFFICIENT EVIDENCE
DATA LIMITED
PROCESS LIMITED
UNKNOWN
~~~

正式State名は後。

Resultに保持可能な意味:

~~~text
Question
Hypothesis / Claim
Methods
Evidence Summary
Refutation
Alternative
Conditions
Failure Boundary
Constraint Candidate
Uncertainty
Regime Dependence
Reproducibility
Unresolved Questions
Process Failure
~~~

---

# 15.21 Research Process Failure

## Decision Candidate
KEEP / STRENGTHEN

研究プロセス自身の失敗をHypothesis反証と分ける。

候補:

~~~text
Data insufficient
Experiment failure
Computation failure
Evidence conflict
Invalid design
Leakage
Look-ahead bias
Research timeout
External dependency failure
Insufficient statistical power
~~~

重要:

~~~text
Research Process Failure
≠ Hypothesis Refutation
~~~

Process Failureなら結論不能 / 再設計 / 再実行へ。

---

# 15.22 Validation Gate

## Decision Candidate
KEEP / REDESIGN

Validation Gateの意味を「Hypothesis正解認定」にしない。

確認対象候補:

~~~text
Question traceable
Plan/version traceable
Hypothesis/Claim version known
Evidence Channel / Role / Dependency traceable
Research Mode known
Methods known
Refutation attempted
Alternative considered when relevant
Failure Boundary / Constraint recorded when found
Process Failure separated
Research Ledger available
Temporal integrity satisfied
Result reproducible/explainable enough for downstream evaluation
~~~

---

# 15.23 Validated Research Result

## Decision Candidate
KEEP as logical boundary

Validatedの意味:

> Research Resultが定義されたResearch Integrity / Trace / Validation要件を満たし、R3 Knowledgeで評価可能な身分になっている。

重要:

~~~text
Validated Research Result
≠ Supported Hypothesis
≠ Knowledge
≠ Applicable Knowledge
≠ Trade Permission
~~~

したがって、

~~~text
REFUTED
INCONCLUSIVE
BOUNDARY FOUND
REGIME DEPENDENT
INSUFFICIENT EVIDENCE
~~~

もValidated Research Resultになり得る。

---

# 15.24 Negative / Null / Unknown Research Asset

## Decision Candidate
KEEP / STRENGTHEN

価値あるResearch AssetはPositive Edgeだけではない。

~~~text
Negative Result
Refutation
Failure Boundary
Constraint Candidate
Contradiction
Unknown
No Edge
OOS disappearance
Replication failure
Mechanism uncertainty
~~~

もR3 / C19へ渡す価値がある。

---

# 15.25 Proactive / Reactive / Reverse Research

## Decision Candidate
MERGE into Multi-Entry / Common Core

Dual-Entryという名称より広く、

~~~text
Multi-Entry
↓
Common Research Core
~~~

候補へ再設計する。

Entry例:

~~~text
Foundation-driven
Observation-driven
Open Discovery
Anomaly-driven
Contradiction-driven
Failure-driven
Knowledge-driven
Applicability-driven
Reverse / Outcome-driven
External-research-driven
Replication / periodic-revalidation
Market-expansion-driven
~~~

重要:

~~~text
Entry differs
≠ Separate Hypothesis system
≠ Separate Evidence system
≠ Separate Knowledge system
~~~

---

# 15.26 Reverse Investigation Placement

## Decision Candidate
KEEP as Method before formal research

R5から、

~~~text
Unexpected Outcome
↓
Reverse Investigation
↓
Cause / Explanation Candidates
↓
Research Question
↓
R2
~~~

と接続。

R2で正式にAlternative / Confounder / Temporal Order / Evidenceを検証する。

重要:

~~~text
Reverse Investigation
≠ Evidence
≠ Root Cause Confirmation
~~~

---

# 15.27 External Research

## Decision Candidate
KEEP / REDESIGN

論文・外部分析・第三者Researchを正式Question Source / Referenceとして利用可能にする。

ただし:

~~~text
External Paper
≠ Internal Knowledge
~~~

原則候補:

~~~text
External Claim
↓
Replication / Validation Question
↓
R2
↓
Validated Research Result
↓
R3 Knowledge Admission
~~~

外部結論をそのまま内部Truthにしない。

---

# 15.28 AI / Python / Rule Boundary

## Decision Candidate
KEEP / STRENGTHEN

AI候補:

~~~text
Question suggestion
Hypothesis generation
Alternative generation
Confounder suggestion
Red Team critique
Contradiction detection
Research review
Explanation
~~~

Python / Rule候補:

~~~text
Data processing
Calculation
Backtest
OOS
Statistics
Replay
Reproducible testing
Stress execution
Trace checks
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

---

# 15.29 R2 Candidate Flow

~~~text
Multiple Question Sources
        ↓
Research Question
        ↓
Research Candidate
        ↓
Admission / Priority
        ↓
Research Design
        ↓
Research Plan
        ↓
        ├─ EXPLORATORY
        ├─ CONFIRMATORY
        └─ REPLICATION
        ↓
Research Trials / Experiments
        ↓
Evidence
        ├─ Historical
        ├─ OOS
        ├─ Forward
        ├─ Stress
        ├─ Runtime / Observational
        └─ Production / Live
        ↓
Independent Challenge / Refutation
        ↓
Research Synthesis
        ↓
Research Result
        ↓
Validation Gate
        ↓
Validated Research Result
        ↓
R3 Knowledge Admission
~~~

Cross-cutting:

~~~text
Research Ledger
Time / Temporal Integrity
Trace / Provenance
Version
Uncertainty
State / Lifecycle
AI Assistance
Storage
~~~

---

# 15.30 R2 Concept Classification

| Concept | Phase 5 R2 Candidate |
|---|---|
| Research Question | NEW / KEEP |
| Research Question Type | KEEP / REDESIGN |
| Research Candidate | REDESIGN |
| Research Intake | MERGE / REDESIGN |
| Research Priority | KEEP / STRENGTHEN |
| Research Router | REDESIGN as multi-axis |
| Research Domain / Intent / Mode / Method | KEEP distinction |
| EXPLORATORY / CONFIRMATORY / REPLICATION | KEEP / STRENGTHEN |
| Research Plan | KEEP / STRENGTHEN |
| Plan Freeze / Version | NEW / KEEP principle |
| Hypothesis / Claim | KEEP / REDESIGN |
| Research Trial | KEEP |
| Causal Research | KEEP as Method family |
| Empirical Research | KEEP as Method family |
| Evidence Channel | KEEP |
| Evidence Role | KEEP / REDESIGN |
| Evidence Outcome | KEEP / REDESIGN |
| Evidence Dependency / Independence | KEEP / STRENGTHEN |
| Research Ledger | KEEP / STRENGTHEN |
| Red Team / Independent Challenge | KEEP responsibility |
| Stress Lab | MERGE / REDESIGN into Research Method |
| Boundary Discovery | KEEP / STRENGTHEN |
| Constraint Candidate | KEEP / REDESIGN |
| Alternative / Confounder / Contradiction | KEEP |
| Research Synthesis | KEEP / STRENGTHEN |
| Research Result | KEEP / REDESIGN |
| Process Failure | KEEP / STRENGTHEN |
| Validation Gate | KEEP / REDESIGN |
| Validated Research Result | KEEP logical boundary |
| Negative / Unknown Result | KEEP / STRENGTHEN |
| Dual-Entry / Single-Core | REDESIGN → Multi-Entry / Common Core |
| Reverse Investigation | KEEP method before R2 |
| External Research | KEEP / REDESIGN |
| AI Team inside Research | DROP monolith |
| AI as Evidence | DROP |
| Research → direct Knowledge mutation | DROP |
| Research → direct Production | DROP |

---

# 15.31 R2 Open Questions for Later Design

~~~text
1. Research Question Type正式Taxonomy
2. Candidate Admission state machine
3. Priority formula / scheduling policy
4. Domain / Intent / Mode / Method registry
5. Plan Freeze対象となる研究レベル
6. HypothesisとGeneric Claimのexact boundary
7. Evidence independence判定方法
8. Evidence Strengthの算定方法
9. Statistical method / sample adequacy
10. OOS / Forward / Replication requirements
11. Red Teamのindependence requirement
12. Research Synthesis authority
13. Validation Gate authority
14. Research Result state taxonomy
15. Constraint Candidate → Runtime Authorized Constraintのhand-off
16. External Research licensing / provenance / replication contract
17. AI-assisted researchのreproducibility
18. Research backlog / compute-budget governance
19. Research Ledger retention
20. Research self-study / method-performance evaluation
~~~

---

# 15.32 Phase State

~~~text
Phase 5 R1
COMPLETE / WORKING CANDIDATE

Phase 5 R2
COMPLETE / WORKING CANDIDATE

NEXT:
R3 — Knowledge / Applicability / Decision Preparation
~~~

重要:

~~~text
R2 COMPLETE
≠
Final Research Architecture

Stress Lab MERGED
≠
stress research removed

Causal Engine removed as monolith
≠
causal research removed

Multi-Entry / Common Core
≠
every question must be researched
~~~


---

# 16. Checkpoint 009 — Phase 5 R3 Concept-Level Reconstruction

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction  
**Scope:** R3 — Knowledge / Applicability / Decision Preparation

## 16.1 R3 Purpose Candidate

R3の責任候補:

> R2のValidated Research Resultから、再利用可能な意味を条件付きKnowledgeとしてAdmission・Version管理し、現在市場Contextと照合してApplicabilityを評価し、複数KnowledgeのConflict / Dependency / Overlapを整理してDecision Candidateへ統合し、その候補のEconomic Valueを評価してR4 Capital / Productionへ渡す。

R3は以下を行わない。

~~~text
FoundationをTruthへ昇格しない
Researchを再実行しない
一回のRuntime結果でKnowledgeを書き換えない
Runtime Constraintを勝手にAuthorizedにしない
Capital Permissionを出さない
Position Sizeを最終決定しない
Executionを行わない
~~~

---

# 16.2 R3内部は3責任群に分ける

R3を一つの巨大Filterにしない。

候補:

~~~text
A. Knowledge Maintenance
B. Applicability / Runtime Assumption
C. Decision Preparation / Economic Value
~~~

重要:

~~~text
Knowledge Formation
≠ Applicability

Applicability
≠ Decision Synthesis

Decision Synthesis
≠ Expected Value

Expected Value
≠ Capital Permission
~~~

---

# 16.3 FoundationとKnowledgeの境界

## Decision Candidate
KEEP / STRENGTHEN

R1 Foundation:

> 市場・経済・Instrument・Participant・Mechanism等を研究するためのprior / background model。

R3 Knowledge:

> R2で研究・検証され、再利用可能な意味としてAdmissionされた市場理解OS自身の研究成果。

重要:

~~~text
Foundation Claim
≠ Research Knowledge

Textbook Mechanism
≠ Internal Validated Knowledge

Current Relation Interpretation
≠ Knowledge
~~~

Foundation自身が研究されValidated Resultになれば、R3でKnowledge Admissionされ得る。

ただし元のFoundation Claimを自動上書きしない。

---

# 16.4 Knowledge Admission

## Decision Candidate
KEEP / STRENGTHEN

入力:

~~~text
Validated Research Result
~~~

Admissionの問い:

> このResearch Resultには、将来再利用する価値がある「分かったこと」があるか？

確認候補:

~~~text
意味が明確
Research Result traceable
成立条件 traceable
Failure Boundary traceable
Evidence / uncertainty traceable
対象Market / Asset / Horizonが明確
Version可能
既存Knowledgeとの関係を識別可能
再利用可能なClaim / Boundary / Negative conclusionがある
~~~

重要:

~~~text
Validated Research Result
≠ Automatic Knowledge
~~~

---

# 16.5 Knowledge Admission Outputは一つではない

## Decision Candidate
NEW / REDESIGN

Validated Resultをすべて同じKnowledge Recordへ押し込まない。

候補:

~~~text
A. Knowledge Admission
= 再利用可能な意味が確立

B. Research Asset Only
= 研究履歴・未解決・Process Limitとして価値はあるが、
  Knowledge Claimとしてはまだ弱い

C. Merge / Update Candidate
= 既存KnowledgeのVersion / Boundary / Relationship更新候補

D. No Knowledge Admission
= 再利用可能なKnowledge semanticを作らない
~~~

例:

~~~text
OOSでFunding単独Edgeなし
→ Negative Knowledge候補

Liquidity一定以下でBreakout Edge崩壊
→ Failure Boundary / Constraint Knowledge候補

Data不足で結論不能
→ Research Asset
  ≠ Knowledge Claim
~~~

---

# 16.6 Knowledge Semantics

## Decision Candidate
KEEP / REDESIGN

Knowledgeを一文Ruleにしない。

最低限、意味として持てる候補:

~~~text
Claim / Effect / Conclusion
Knowledge Type
Market / Asset scope
Time Horizon
成立条件
Supporting Context
Weakening Conditions
Failure Boundary
Research Constraint Candidate
Evidence Profile reference
Uncertainty
Regime Dependence
Validation History
Version
Source Research
~~~

重要:

~~~text
Knowledge
≠ Trade Rule
≠ Signal
≠ Runtime Permission
~~~

---

# 16.7 Knowledge Type

## Decision Candidate
KEEP / REDESIGN

KnowledgeはPositive Edgeだけではない。

候補family:

~~~text
Mechanism Knowledge
Empirical Relationship Knowledge
Negative / Refutation Knowledge
Failure / Boundary Knowledge
Constraint Knowledge
State / Case Knowledge
Formula / Feature Knowledge
Uncertainty / Known-Unknown Knowledge
~~~

ただし、

~~~text
INCONCLUSIVE
PROCESS LIMITED
DATA LIMITED
~~~

を無条件でKnowledge化しない。

「何が分からないか」が再利用可能な形で確立している場合のみKnown-Unknown / Uncertainty Knowledge候補。

---

# 16.8 Knowledge Record / Relationship / Graph

## Decision Candidate
KEEP semantics / REDESIGN storage

Knowledge SemanticsとKnowledge Relationshipを分ける。

~~~text
Knowledge Record
= 何が分かったか

Knowledge Relationship
= 他Knowledgeとどう関係するか
~~~

Relationship候補:

~~~text
SUPPORTS
CONTRADICTS
CONDITIONAL_ON
SUPERSEDES
DERIVED_FROM
SHARES_EVIDENCE
SHARES_CAUSE
OVERLAPS
GENERALIZES
SPECIALIZES
REPLICATES
~~~

Knowledge Graph:

~~~text
Derived / queryable relationship view candidate
≠ duplicate canonical Knowledge store
~~~

Knowledge Pool:

~~~text
Logical Knowledge Domain
≠ giant monolithic DB object
~~~

---

# 16.9 Knowledge Version / Lineage

## Decision Candidate
KEEP / STRENGTHEN

Knowledgeを後から上書きして歴史を消さない。

~~~text
Knowledge v1
↓
new Validated Research Result
↓
Knowledge v2 candidate
~~~

追跡候補:

~~~text
Source Research
Created At
Version
Supersedes
Superseded By
Last Validation
Evidence update
Boundary change
Semantic change
~~~

重要:

~~~text
Knowledge Update
≠ History overwrite
~~~

---

# 16.10 Knowledge Lifecycle

## Decision Candidate
KEEP / STRENGTHEN

Knowledgeが存在することと現在健康であることを分ける。

Lifecycle候補意味:

~~~text
ACTIVE
WEAK / DEGRADED
UNDER REVIEW
SUPERSEDED
RETIRED
~~~

正式Stateは後。

重要:

~~~text
Lifecycle Status
≠ Applicability State
~~~

例:

~~~text
Knowledge = ACTIVE
Current Market = NOT_APPLICABLE
~~~

は正常。

また、

~~~text
Knowledge = UNDER_REVIEW
Current Context similar
~~~

でもProduction利用を制限し得る。

---

# 16.11 Knowledge Revalidation

## Decision Candidate
KEEP / STRENGTHEN

Revalidation Trigger候補:

~~~text
Validation age
New contradictory evidence
Repeated applicability contradiction
Replication failure
Market structure change
Regime shift
External mechanism change
Production evidence accumulation
Boundary breach
~~~

重要:

~~~text
Revalidation Trigger
→ Research Question / R2
~~~

R3自身が再研究しない。

---

# 16.12 Negative Knowledge

## Decision Candidate
KEEP / STRENGTHEN

Negative Resultを捨てない。

例:

~~~text
Funding単独には安定Directional Edgeを確認できない

このRegimeではBreakout relationは再現しない

このExplanationはAlternative Hypothesisに負けた
~~~

Negative Knowledgeの目的:

- 同じ無駄研究を繰り返さない
- Decisionで過剰期待を防ぐ
- Research Priorityを改善する

重要:

~~~text
Negative Knowledge
≠ NOT_APPLICABLE
~~~

前者は研究上の再利用Knowledge。
後者は現在市場との不一致。

---

# 16.13 Failure Boundary

## Decision Candidate
KEEP / STRENGTHEN

Knowledgeの成立条件と対で保持する。

~~~text
Success / Validity Conditions
+
Failure Boundary
~~~

Failure Boundaryは、

> Knowledgeが弱くなる / 壊れることがResearchで確認された境界。

Applicabilityで必ず参照可能にする。

---

# 16.14 Constraint

## Decision Candidate
SPLIT / REDESIGN

少なくとも3身分へ分ける候補。

~~~text
A. Research Constraint Candidate
= R2で発見された制約候補

B. Knowledge Constraint
= R3で再利用可能な意味としてAdmissionされた制約知識

C. Runtime Authorized Constraint
= R4 / X06で本番強制権限を持つ制約
~~~

重要:

~~~text
Research Constraint Candidate
≠ Runtime Authorized Constraint

Knowledge Constraint
≠ Risk Rule automatically
~~~

---

# 16.15 Knowledge Retrieval

## Decision Candidate
NEW / REDESIGN

Applicability前に、全Knowledgeを毎回評価しない。

Current Market Contextから関連KnowledgeをRetrievalする責任候補を置く。

Retrieval参考:

~~~text
Market / Asset
Time Horizon
Current State
Relation / Foundation context
Regime
Knowledge type
Semantic similarity
Historical state similarity
~~~

ただし:

~~~text
Retrieved
≠ Applicable
~~~

Retrievalは候補選択のみ。

---

# 16.16 Applicability

## Decision Candidate
KEEP / STRENGTHEN

中心問い:

> このKnowledgeは、今この市場でDecision Materialとして使ってよいか？

入力候補:

~~~text
Knowledge
Current Market Understanding
Current Market State Representation
Runtime Observation
Quality / Freshness
Relevant Current Relation Interpretation
Knowledge Lifecycle
Validation Age
Failure Boundary
Constraint Knowledge
Uncertainty
~~~

重要:

~~~text
Evidence Strong
≠ Applicable

State Similar
≠ Applicable Proof

Applicable
≠ Positive EV
~~~

---

# 16.17 Applicability State

## Decision Candidate
KEEP / REDESIGN

二値にしない。

候補意味:

~~~text
APPLICABLE
PARTIALLY_APPLICABLE
NOT_APPLICABLE
UNCERTAIN
BLOCKED_BY_CONSTRAINT
NOT_EVALUATED
~~~

正式Enumは後。

重要:

~~~text
NOT_APPLICABLE
≠ Knowledge RETIRED
~~~

---

# 16.18 Applicability Assessment

## Decision Candidate
KEEP

単なるStateではなく理由を追跡可能にする。

候補内容:

~~~text
Knowledge reference
Applicability state
Matched conditions
Missing conditions
Current state differences
Failure boundary status
Constraint status
Contradictions
Evidence context
Validation age
Uncertainty
Overlap / dependency context
~~~

---

# 16.19 Excluded Knowledge Trace

## Decision Candidate
KEEP / STRENGTHEN

使わなかったKnowledgeも消さない。

追跡候補:

~~~text
NOT_APPLICABLE
UNCERTAIN
BLOCKED
NOT_EVALUATED
~~~

と理由。

目的:

> 後から「なぜこのKnowledgeをDecisionに使わなかったか」を説明できる。

C17 Outcome / Decision Quality評価にも重要。

---

# 16.20 Runtime Assumption Monitoring

## Decision Candidate
SPLIT from pre-decision applicability / KEEP shared semantics

Trade前Applicabilityと、Position中のKnowledge前提監視は意味を共有するが速度が違う。

候補:

~~~text
Knowledge assumptions
+
Current Runtime Context
↓
Assumption Monitoring
↓
NORMAL
DEGRADED
MATERIAL DEVIATION
UNKNOWN
~~~

正式Stateは後。

Output:

~~~text
Applicability Degradation
Assumption Violation
Material Market Change
Contradiction
Quality degradation
~~~

Downstream:

~~~text
→ R4 Runtime Protection / Risk
→ R5 Feedback
→ 必要に応じてR2 Research Question
~~~

重要:

~~~text
Runtime Assumption Monitoring
≠ Knowledge mutation
≠ Exit Decision Authority
~~~

---

# 16.21 Applicability Contradiction

## Decision Candidate
KEEP / STRENGTHEN

例:

~~~text
Knowledge conditions seem satisfied
↓
but repeated observed behavior contradicts expectation
~~~

R3の対応:

~~~text
Contradiction Finding
↓
R5 / R2 Question
~~~

一回の矛盾でKnowledgeをRetireしない。

---

# 16.22 Applicable Knowledge Context

## Decision Candidate
REDESIGN

旧Applicable Knowledge Setを単なるID listにしない。

候補:

~~~text
Applicable Knowledge
Conditional / Partial Knowledge
Constraint / Boundary proximity
Contradictions
Dependency / Overlap
Uncertainty
Excluded-knowledge trace reference
Current Market Context
~~~

これをC12 Decision SynthesisのInputにする。

---

# 16.23 Knowledge Conflict / Dependency / Overlap

## Decision Candidate
KEEP / STRENGTHEN

複数Knowledgeが同時に使える場合:

~~~text
A → Long support
B → Short support
C → Wait / avoid
D → volatility opportunity
~~~

単純多数決しない。

さらに、

~~~text
A and B share evidence
A and C derive from same underlying mechanism
B is a specialization of D
~~~

等を認識できる必要がある。

重要:

~~~text
Knowledge Count
≠ Independent Evidence Count
≠ Decision Weight
~~~

---

# 16.24 Decision Synthesis

## Decision Candidate
NEW / STRONG

R3に新しく明示する。

責任:

> Applicable Knowledge、Current Understanding、Conflict / Dependency / Uncertaintyを統合し、「どんな行動候補 / Thesisが成立するか」を作る。

Output候補:

~~~text
Decision Candidate
Decision Thesis
Action Alternatives
WAIT
NO ACTION
UNKNOWN
Directional / non-directional opportunity candidate
~~~

正式用語は後。

重要:

~~~text
Decision Synthesis
≠ Majority Vote
≠ Expected Value
≠ Capital Permission
~~~

---

# 16.25 Trade Thesis / Decision Thesis

## Decision Candidate
REDESIGN / DEFER name

Legacy TradeThesisの本質:

> どのKnowledgeとCurrent Contextから、どの行動仮説を構成したかをTraceできること。

この責任は残す価値が高い。

ただし、

~~~text
Trade Thesis
~~~

という名前を必須にせず、

~~~text
Decision Thesis / Action Thesis
~~~

等もPhase 6で比較する。

Thesisには、

~~~text
Supporting Knowledge
Contradicting Knowledge
Current context
Assumptions
Uncertainty
Expected direction / structure
Time horizon
Invalidation context
~~~

等を持てる方向。

---

# 16.26 Decision Outcome Vocabulary

## Decision Candidate
REDESIGN

Legacy BUY / SELLだけをCanonical Outcomeにしない。

候補意味:

~~~text
TRADE CANDIDATE
WAIT
NO TRADE / NO ACTION
REDUCE CANDIDATE
UNKNOWN
INSUFFICIENT EDGE
CONFLICTED
~~~

具体Action taxonomyはR4との境界設計で確定。

重要:

> 「何もしない」を正常なDecision Candidateにする。

---

# 16.27 Expected Value Assessment

## Decision Candidate
KEEP / REDESIGN

ApplicabilityやThesisと分離する。

中心問い:

> このDecision Candidateには、Cost / Uncertaintyを含めても経済的にRiskを検討する価値があるか？

候補要素:

~~~text
Expected return / payoff
Probability / scenario weighting
Loss magnitude
Fee
Slippage
Liquidity cost
Holding time
Opportunity cost
Uncertainty
Model / knowledge dependence
Tail sensitivity
~~~

重要:

~~~text
Applicable
≠ Positive EV

Positive directional probability
≠ Positive EV

Positive EV
≠ Capital Permission
~~~

---

# 16.28 EVとRiskの境界

## Decision Candidate
KEEP / STRENGTHEN

R3:

~~~text
Economic Value
= opportunity economics
~~~

R4:

~~~text
Capital / Risk Permission
= user capitalを実際に晒してよいか
~~~

例:

~~~text
EV positive
but
Portfolio exposure too concentrated
↓
R4 BLOCK / REDUCE
~~~

R3がRisk Authorityを持たない。

---

# 16.29 R3 → R4 Handoff

## Decision Candidate
NEW / REDESIGN

R3の主要Output候補:

~~~text
Decision Proposal / Economic Opportunity Context
~~~

含む意味候補:

~~~text
Decision Thesis / candidate action
Supporting applicable knowledge
Contradicting knowledge
Applicability reasoning
Expected Value assessment
Uncertainty
Time horizon
Assumptions
Invalidation / boundary context
Excluded alternative trace
Current market context reference
~~~

重要:

~~~text
R3 Output
≠ Order Intent
≠ Position Size
≠ Capital Permission
~~~

---

# 16.30 Runtime PathとMaintenance Pathの分離

## Decision Candidate
KEEP / STRENGTHEN

### Slow / Maintenance

~~~text
Validated Research Result
↓
Knowledge Admission
↓
Knowledge Version / Lifecycle
↓
Knowledge Domain
~~~

### Runtime / Decision

~~~text
Current Market
+
Existing Knowledge
↓
Retrieval
↓
Applicability
↓
Decision Synthesis
↓
EV
↓
R4
~~~

### Fast Assumption Monitoring

~~~text
Position-linked Knowledge Assumptions
+
Current Runtime Context
↓
Assumption Monitoring
↓
R4 Protection / R5 Feedback
~~~

Production Runtimeが毎回R2 Research完了を待たない。

---

# 16.31 RuntimeでKnowledgeを直接更新しない

## Decision Candidate
KEEP / HARD BOUNDARY

禁止:

~~~text
single loss
↓
Knowledge RETIRED

single win
↓
Knowledge promoted

runtime deviation
↓
Knowledge semantics overwritten
~~~

正しい候補:

~~~text
Runtime Finding
↓
R5 Feedback
↓
Research Question
↓
R2
↓
Validated Research Result
↓
R3 Maintenance
~~~

---

# 16.32 AI / Ruleの役割

AI候補:

~~~text
Knowledge retrieval assistance
semantic comparison
conflict explanation
thesis drafting
contradiction explanation
human-readable reasoning
~~~

Rule / deterministic候補:

~~~text
Explicit condition matching
version checks
constraint checks
state comparison
dependency metadata
EV arithmetic
trace checks
~~~

重要:

~~~text
AI Similarity
≠ Applicability

AI Preference
≠ Decision Authority

AI EV narrative
≠ Risk Permission
~~~

---

# 16.33 R3 Candidate Flow

~~~text
R2 Validated Research Result
        ↓
Knowledge Admission
   ┌────┼──────────────┐
   │    │              │
   ↓    ↓              ↓
New    Update /      Research Asset
Knowledge Merge      Only
   │    │
   └────┘
      ↓
Knowledge Version / Lifecycle
      ↓
Logical Knowledge Domain
      │
      │            Current Market Understanding
      │            Current State / Runtime Context
      │                     ↓
      └──────────────→ Knowledge Retrieval
                            ↓
                     Applicability Assessment
                            ↓
                  Applicable Knowledge Context
                            ↓
              Conflict / Dependency / Overlap
                            ↓
                    Decision Synthesis
                            ↓
                 Decision Thesis / Candidate
                            ↓
                 Expected Value Assessment
                            ↓
               Economic Opportunity Context
                            ↓
                           R4
~~~

Parallel Runtime:

~~~text
Position-linked Knowledge Assumptions
+
Current Runtime Context
↓
Runtime Assumption Monitoring
├→ R4 Protection / Risk
├→ R5 Feedback
└→ R2 Question when research needed
~~~

---

# 16.34 R3 Concept Classification

| Concept | Phase 5 R3 Candidate |
|---|---|
| Foundation vs Knowledge boundary | KEEP / STRENGTHEN |
| Knowledge Admission | KEEP / STRENGTHEN |
| Research Asset Only path | NEW |
| Knowledge Semantics | KEEP / REDESIGN |
| Knowledge Type | KEEP / REDESIGN |
| Knowledge Record | KEEP semantics |
| Knowledge Relationship | KEEP / STRENGTHEN |
| Knowledge Graph | REDESIGN as view |
| Knowledge Pool | REDESIGN as logical domain |
| Knowledge Version / Lineage | KEEP / STRENGTHEN |
| Knowledge Lifecycle | KEEP / STRENGTHEN |
| Knowledge Revalidation | KEEP / STRENGTHEN |
| Negative Knowledge | KEEP / STRENGTHEN |
| Failure Boundary | KEEP / STRENGTHEN |
| Research Constraint Candidate | KEEP R2 semantic |
| Knowledge Constraint | NEW / REDESIGN |
| Runtime Authorized Constraint | DEFER to R4/X06 |
| Knowledge Retrieval | NEW / REDESIGN |
| Applicability | KEEP / STRENGTHEN |
| Applicability Assessment | KEEP |
| Applicable Knowledge Set | REDESIGN → richer context |
| Excluded Knowledge Trace | KEEP / STRENGTHEN |
| Runtime Assumption Monitoring | SPLIT / KEEP |
| Applicability Contradiction | KEEP / STRENGTHEN |
| Knowledge Conflict | KEEP / STRENGTHEN |
| Knowledge Dependency / Overlap | KEEP / STRENGTHEN |
| Decision Synthesis | NEW / STRONG |
| Trade Thesis | REDESIGN / DEFER name |
| Decision Thesis / Candidate | NEW candidate |
| Expected Value | KEEP / REDESIGN |
| Signal Engine | DROP as required top-level |
| BUY / SELL only outcome | DROP |
| Direct Knowledge → Trade | DROP |
| Runtime direct Knowledge mutation | DROP |

---

# 16.35 R3 Open Questions for Later Design

~~~text
1. Knowledge Admission authority
2. Knowledge Type taxonomy
3. Negative Knowledge admission criteria
4. Known-UnknownをKnowledge化する条件
5. Knowledge canonical semantic minimum
6. Knowledge Relationship taxonomy
7. Lifecycle state machine
8. Lifecycle writer authority
9. Revalidation trigger thresholds
10. Retrieval strategy / relevance model
11. Applicability state taxonomy
12. Applicability scoring vs rule-based matching
13. Runtime assumption monitoring latency
14. C11 monitoringとR4 protectionのexact authority boundary
15. Conflict Resolution method
16. Decision Thesis object / naming
17. Multi-horizon decision synthesis
18. Decision alternatives / abstention semantics
19. EV probability / scenario model
20. Fee / slippage / opportunity cost handling
21. EV uncertainty representation
22. R3 → R4 exact contract
23. Constraint candidate → authorized runtime constraint promotion
24. Market-specific Knowledge extension contract
25. Knowledge decay / structural break policy
~~~

---

# 16.36 Phase State

~~~text
Phase 5 R1
COMPLETE / WORKING CANDIDATE

Phase 5 R2
COMPLETE / WORKING CANDIDATE

Phase 5 R3
COMPLETE / WORKING CANDIDATE

NEXT:
R4 — Capital / Production
~~~

重要:

~~~text
R3 COMPLETE
≠
Final Knowledge Architecture

Knowledge admitted
≠
Applicable

Applicable
≠
Decision

Decision Candidate
≠
Positive EV

Positive EV
≠
Capital Permission

Runtime deviation
≠
Knowledge rewrite
~~~


---

# 16. Checkpoint 009 — Phase 5 R3 Concept-Level Reconstruction

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction  
**Scope:** R3 — Knowledge / Applicability / Decision Preparation

## 16.1 R3 Purpose Candidate

R3の責任候補:

> R2から受け取ったValidated Research Resultを再利用可能な条件付きKnowledgeとしてAdmissionし、Version・Lifecycle・Relationship・Failure Boundary・Uncertaintyを維持しながら、現在市場で利用可能かを評価し、複数KnowledgeのConflict / Overlapを整理してDecision Candidateへ統合し、Economic Valueを評価したうえでR4 Capital / Productionへ渡す。

R3は以下を行わない。

~~~text
FoundationをResearch Knowledgeへ無条件昇格しない
Research Resultを自動Knowledge化しない
KnowledgeがApplicableだからTradeと決めない
Economic Valueが正だからCapital Permissionを出さない
Runtime中の一回のLossでKnowledgeをRetireしない
Research Constraint Candidateを自動でProduction強制Ruleにしない
~~~

---

# 16.2 Foundation vs Research Knowledge

## Decision Candidate
KEEP SEPARATION / STRENGTHEN

R1 FoundationとR3 Research Knowledgeを明確に分ける。

### Foundation

~~~text
研究を始めるための背景理解
市場構造
制度
Mechanics
Participant model
Economic relation prior
Working model / heuristic
~~~

### Research Knowledge

~~~text
市場理解OS自身がR2で研究・検証し、
再利用可能な意味としてAdmissionした知識
~~~

重要:

~~~text
Foundation Claim
≠ Research Knowledge

外部で一般的
≠ 内部で検証済み

Foundationを参照した
≠ FoundationがEvidence
~~~

Foundation自体が研究され、Validated Research Resultを経てR3へ来た場合は、そのResearch ResultからKnowledge化を評価できる。

---

# 16.3 Knowledge Admission / Formation

## Decision Candidate
KEEP / REDESIGN

Validated Research ResultをそのままKnowledgeへしない。

候補Flow:

~~~text
Validated Research Result
↓
Knowledge Admission
↓
Knowledge Formation
↓
Knowledge Record / Relationship
~~~

Admissionで確認する意味候補:

~~~text
再利用可能なClaim / Findingがあるか
Research Resultの身分が明確か
成立条件を追跡できるか
Failure Boundaryを追跡できるか
Constraint Candidateを追跡できるか
Evidence lineageを辿れるか
Uncertaintyが残っているか
Market / Asset / Horizonが明確か
Versionを識別できるか
既存Knowledgeとの重複・更新関係が分かるか
~~~

重要:

~~~text
Validated Research Result
≠ Knowledge

Knowledge Admission
≠ Positive Edge Approval
≠ Production Approval
~~~

旧「Promotion」という語はProduction昇格と誤解しやすいため、Knowledge Formation / Admissionへ名称再検討候補。

---

# 16.4 Knowledge Semantics

## Decision Candidate
KEEP / STRENGTHEN

Knowledgeを単純なルール文へ潰さない。

Knowledgeが保持すべき意味候補:

~~~text
Claim / Effect / Finding
対象Market / Asset
Time Horizon
成立条件
成立しやすい状態
弱くなる条件
Failure Boundary
Constraint semantics
Evidence lineage / profile
Uncertainty
Regime dependence
Known alternatives / contradictions
Version
Validation history
~~~

重要:

~~~text
Knowledge
≠ Rule
≠ Signal
≠ Position instruction
~~~

---

# 16.5 Knowledge Family

## Decision Candidate
REDESIGN / STRENGTHEN

成功KnowledgeだけをKnowledgeとしない。

候補Family:

~~~text
Positive / Edge Knowledge
Negative / No-Edge Knowledge
Refutation Knowledge
Failure / Boundary Knowledge
Constraint Knowledge
Mechanism Knowledge
Context / Regime Knowledge
Uncertainty / Unknown Knowledge
Replication Knowledge
~~~

正式Taxonomyは後。

目的:

- 失敗研究を資産として残す
- 同じ無駄なResearchを繰り返さない
- 「使える条件」と「使ってはいけない条件」を同じ重要度で扱う

---

# 16.6 Knowledge Relationship

## Decision Candidate
KEEP / REDESIGN

Knowledge同士の関係を追跡可能にする。

候補:

~~~text
SUPPORTS
CONTRADICTS
REFINES
SUPERSEDES
DEPENDS_ON
SHARES_EVIDENCE
SHARES_CAUSE
OVERLAPS
GENERALIZES
SPECIALIZES
REPLICATES
FAILS_UNDER
~~~

正式Relation語彙は後。

重要:

~~~text
Knowledge Relationship
≠ Knowledge Semantics本体

Knowledge Graph
≠ duplicate Knowledge store
~~~

Knowledge Graphを使う場合はDerived View候補。

---

# 16.7 Knowledge Pool / Library

## Decision Candidate
MERGE / REDESIGN

「Knowledge Library」「Knowledge Pool」を物理巨大DB名として固定しない。

保持する本質:

> Admission済みResearch Knowledgeを、意味・Version・Relationship・Lifecycleを保ったまま検索・再利用できるLogical Knowledge Domain。

~~~text
Knowledge Pool
= logical domain
≠ one giant table
≠ Knowledge Graphそのもの
~~~

---

# 16.8 Knowledge Version

## Decision Candidate
KEEP / STRENGTHEN

Knowledgeを上書きしない。

~~~text
Knowledge v1
↓
New Research
↓
Evidence / Boundary / Meaning change
↓
Knowledge v2
~~~

追跡候補:

~~~text
created_from
supersedes
superseded_by
last_validated
validation lineage
semantic change
boundary change
evidence change
~~~

重要:

~~~text
Knowledge Update
≠ History Deletion
~~~

---

# 16.9 Knowledge Lifecycle

## Decision Candidate
KEEP / REDESIGN

Knowledgeが存在することと、現在利用可能であることを分離する。

Lifecycle候補:

~~~text
ACTIVE
WEAKENED
UNDER_REVIEW
DEGRADED
SUPERSEDED
RETIRED
UNKNOWN
~~~

正式State名は後。

最重要:

~~~text
Knowledge Lifecycle State
≠ Runtime Applicability State
~~~

例:

~~~text
Knowledge = ACTIVE
Current Applicability = NOT_APPLICABLE
~~~

は正常。

---

# 16.10 Lifecycle Assessment vs Lifecycle Authority

## Decision Candidate
NEW / STRENGTHEN

老化・矛盾・Validation Ageを見て、

~~~text
Knowledge may be degraded
Revalidation needed
~~~

と評価する責任と、

~~~text
ACTIVE → RETIRED
~~~

と正式Stateを変更するAuthorityを分ける。

~~~text
Lifecycle Assessment
≠ Lifecycle Transition
~~~

候補原則:

- Runtime observationだけでRetireしない
- R5 Finding / contradictionからR2再研究へ戻す
- MaterialなKnowledge state transitionはValidated Research Result等の根拠を要求する方向
- exact writer / approval authorityはX06 Governanceで後決め

---

# 16.11 Knowledge Aging / Revalidation

## Decision Candidate
KEEP / STRENGTHEN

Data FreshnessとKnowledge Validation Ageを分離する。

候補Context:

~~~text
Research Date
Last Validation
Last Replication
Last Forward Evidence
Last Production Evidence
Market Structure Change
Validation Age
~~~

Knowledgeが古い可能性は、

~~~text
Revalidation Requirement
~~~

を生成できる。

重要:

~~~text
Old
≠ False

Recent
≠ Valid
~~~

---

# 16.12 Failure Boundary

## Decision Candidate
KEEP

R2で発見されたFailure BoundaryをKnowledge Semanticsへ保持する。

意味:

> Knowledgeがどの条件から成立しにくくなる / 壊れると研究されたか。

ApplicabilityではSuccess Conditionと同等以上に参照する。

---

# 16.13 Constraint Semantics

## Decision Candidate
SPLIT / REDESIGN

Constraintを3身分へ分離する候補。

~~~text
A. Research Constraint Candidate
= R2で発見された研究上の利用制限候補

B. Knowledge Constraint
= AdmissionされたKnowledgeの条件・禁止条件として保持される意味

C. Runtime Authorized Constraint
= R4 / X06がProductionで強制する正式制約
~~~

重要:

~~~text
Research Constraint Candidate
≠ Knowledge Constraint automatically

Knowledge Constraint
≠ Runtime Authorized Constraint automatically
~~~

---

# 16.14 Applicability

## Decision Candidate
KEEP / STRENGTHEN

Knowledge + Current Market Contextを照合して、

> このKnowledgeを今のDecision Materialとして使ってよいか

を評価する。

Input候補:

~~~text
Knowledge conditions
Failure Boundary
Knowledge Constraint
Evidence context
Validation age
Current Market Understanding
Current State Representation
Current Relation Interpretation
Quality / Freshness
Runtime Observation
Market / Asset / Horizon
~~~

重要:

~~~text
Knowledge Validity
≠ Current Applicability
~~~

---

# 16.15 Applicability State

## Decision Candidate
KEEP / REDESIGN

TRUE / FALSEだけにしない。

候補:

~~~text
APPLICABLE
PARTIALLY_APPLICABLE
NOT_APPLICABLE
UNCERTAIN
BLOCKED_BY_CONDITION
NOT_EVALUATED
~~~

正式State名は後。

重要:

~~~text
NOT_APPLICABLE
≠ RETIRED
~~~

---

# 16.16 Applicability Assessment

## Decision Candidate
KEEP / STRENGTHEN

各Knowledgeについて、結論だけでなく理由を追跡可能にする。

候補意味:

~~~text
Knowledge reference
Applicability State
Matched Conditions
Missing Conditions
Failure Boundary status
Constraint status
Contradictions
Evidence context
Validation age
Current quality/time context
Uncertainty
Relationship / overlap context
~~~

OutputはDecision Synthesisが理由付きで利用できる必要がある。

---

# 16.17 Applicable Knowledge Set

## Decision Candidate
REDESIGN

単なるID一覧ではなく、

> Current Decisionで利用候補となるKnowledgeと、そのApplicability理由・条件・Conflict / Overlap情報を含むlogical set。

ただし「Set」というObject名は後で再検討可能。

除外されたKnowledgeもTraceとして残す。

~~~text
why used
why not used
why uncertain
why blocked
~~~

を後から説明可能にする。

---

# 16.18 Runtime Assumption Monitoring

## Decision Candidate
NEW / SPLIT FROM PRE-DECISION APPLICABILITY

ダイスケ案の「Trade開始後も現在市場を見る」を正式責任へする。

Pre-decision:

~~~text
Knowledge
+
Current Context
→ Applicable now?
~~~

Runtime:

~~~text
Active Decision / Position
+
Knowledge assumptions
+
Current Runtime Context
→ assumptions still hold?
~~~

監視候補:

~~~text
成立条件
Failure Boundary proximity
Liquidity
Leverage
Flow
Event state
Data quality
Market structure deviation
Relevant relation change
~~~

Output候補:

~~~text
STABLE
DEGRADED
MATERIAL_DEVIATION
UNKNOWN
~~~

正式Stateは後。

重要:

~~~text
Runtime Assumption Monitoring
≠ Position close authority
≠ Knowledge rewrite authority
~~~

R4へFast Runtime Contextを送り、R5へFinding candidateを送れる。

---

# 16.19 Runtime Contradiction

## Decision Candidate
KEEP / REDESIGN

Knowledge条件では成立するはずなのに、Current Runtimeが繰り返し矛盾する場合、

~~~text
Runtime contradiction
↓
R5 Finding / Feedback
↓
R2 Research Question
~~~

へ戻す。

R3自身がKnowledgeを自動修正しない。

---

# 16.20 Knowledge Conflict Detection

## Decision Candidate
KEEP

複数Applicable Knowledgeが同時に存在し得る。

例:

~~~text
Knowledge A → Long support
Knowledge B → Short support
Knowledge C → WAIT condition
Knowledge D → High uncertainty
~~~

Applicabilityは各Knowledgeの利用可能性を評価する。

Conflict Detectionは、

~~~text
方向
Horizon
Assumption
Evidence dependency
Boundary
Constraint
~~~

の衝突を検出する。

重要:

~~~text
Conflict Detection
≠ Conflict Resolution
~~~

---

# 16.21 Knowledge Independence / Overlap

## Decision Candidate
KEEP / STRENGTHEN

複数Knowledgeが同じResearch / Evidence / Causeから派生している場合、独立票として扱わない。

候補Context:

~~~text
Shared Evidence
Shared Cause
Same Research Family
Derived Knowledge
Duplicate / Near Duplicate
Common Dependency
~~~

重要:

~~~text
3 Knowledge support
≠ 3 independent confirmations
~~~

---

# 16.22 Decision Synthesis / Conflict Resolution

## Decision Candidate
NEW / KEEP

Phase 3 Gapとして追加したCapabilityをR3へ正式配置候補。

Input:

~~~text
Applicability Assessments
Applicable Knowledge
Excluded / uncertain Knowledge trace
Knowledge Relationships
Conflict / Overlap
Current Market Understanding
Decision Scope / Horizon
Uncertainty
~~~

責任:

> 複数KnowledgeとCurrent Contextを統合し、「何をする候補か」「なぜその候補なのか」を構築する。

重要:

~~~text
Decision Synthesis
≠ Majority Vote
≠ Risk Permission
≠ Execution
~~~

---

# 16.23 Trade Thesis → Decision Thesis / Action Candidate

## Decision Candidate
REDESIGN

LegacyのTrade Thesisは価値が高いが、名前がTradeに偏りすぎる。

市場理解OSでは、

~~~text
TRADE
WAIT
NO TRADE
REDUCE
UNKNOWN
~~~

も正当なDecision Outcome候補。

したがって上位概念として、

~~~text
Decision Thesis
Action Thesis
Decision Candidate
~~~

等へ名称再設計候補。

意味:

> Current Marketで、どのKnowledge・Context・Assumptionを根拠に、どのAction候補を支持するかを説明するDecision-level thesis。

Tradeする場合のみ、後でTrade-specific thesisへprojectionできる。

---

# 16.24 Decision Scope / Horizon

## Decision Candidate
NEW / STRENGTHEN

同じKnowledgeでもHorizonによって結論が異なり得る。

例:

~~~text
5m = short downside risk
4h = long support
1d = uncertain
~~~

Decision SynthesisはScopeを明示する必要がある。

候補:

~~~text
asset
market
venue relevance
time horizon
decision window
position context
~~~

複数Horizonを一つのBUY/SELLへ潰さない。

---

# 16.25 Economic Value Assessment

## Decision Candidate
KEEP / REDESIGN

ApplicabilityとDecision Thesisの後に、

> そのAction CandidateへRiskを取るだけの経済的意味があるか

を評価する。

候補Input:

~~~text
Expected return distribution
Probability / calibration
Potential loss magnitude
Fee
Slippage
Liquidity
Holding time
Opportunity cost
Uncertainty
Evidence / applicability quality
Execution feasibility context
~~~

重要:

~~~text
Applicable
≠ Positive EV

Positive EV
≠ Capital Permission
~~~

Economic ValueはMarket / Strategyの経済評価まで。

資本配分・Portfolio / Drawdown / Ruin判断はR4。

---

# 16.26 Expected Value Representation

## Decision Candidate
KEEP / REDESIGN

EVを単一平均値だけに潰さない方向。

候補意味:

~~~text
Expected return
Downside distribution
Upside distribution
Probability / calibration
Uncertainty range
Horizon
Costs
Scenario dependence
~~~

正式数式は後。

重要:

~~~text
High expected return
with huge uncertainty / tail loss
≠ automatically desirable
~~~

Tail / portfolio riskはR4へ渡す。

---

# 16.27 R3 Output to R4

## Decision Candidate
NEW / REDESIGN

R3からR4へBUY/SELL Signalだけを渡さない。

候補Output:

~~~text
Economic Decision Candidate
or
Decision Thesis Package
~~~

含む意味候補:

~~~text
Action candidate
Decision scope / horizon
Supporting Knowledge
Opposing / excluded Knowledge
Current Context
Applicability rationale
Assumptions
Failure / invalidation conditions
Economic Value assessment
Uncertainty
Runtime assumptions to monitor
Trace / version
~~~

R4はここからCapital / Portfolio / Risk Permissionを評価する。

重要:

~~~text
R3 Output
≠ Capital Permission
≠ Order Intent
~~~

---

# 16.28 Signal Engine

## Decision Candidate
DROP AS REQUIRED TOP-LEVEL CONCEPT

Signalが必要なら、

~~~text
Decision Thesis / Economic Decision Candidate
↓
downstream projection
~~~

として作れる。

必須ArchitectureとしてSignal Engineを置かない。

理由:

- WAIT / NO TRADE / UNKNOWNを扱いにくい
- Knowledge conflictやHorizonを単一Signalへ早く潰しやすい
- DecisionとRisk Permissionを混同しやすい

---

# 16.29 Knowledge Lifecycle / Applicability / RuntimeのTwo-Speed

R3自身にもTwo-Speedがある。

### Slow Knowledge Maintenance

~~~text
Validated Research Result
↓
Knowledge Admission / Version
↓
Lifecycle / Revalidation
~~~

### Fast Runtime Applicability

~~~text
Existing Knowledge
+
Current Context
↓
Applicability
↓
Decision Synthesis / EV
~~~

### Active Runtime Assumption Monitoring

~~~text
Active Decision / Position assumptions
+
Current Runtime Context
↓
Deviation assessment
↓
R4 Fast Safety / R5 Feedback
~~~

重要:

~~~text
Fast Runtime
does not create new Knowledge.

Knowledge Maintenance
does not need to block every Production cycle.
~~~

---

# 16.30 R3 Failure Paths

R3自身のFailure候補:

~~~text
Knowledge unavailable
Version ambiguity
Condition missing
Relationship conflict unresolved
Current Market Context insufficient
Applicability evaluation failure
Stale validation
Constraint semantics unclear
Decision horizon conflict
EV data insufficient
Cost estimate unavailable
AI interpretation unavailable
~~~

原則:

~~~text
Evaluation failure
→ UNCERTAIN / NOT_EVALUATED / DEFER candidate

Evaluation failure
≠ force TRADE
~~~

Fail-openを避ける方向。

---

# 16.31 AI / Python / Rule Boundary

## Decision Candidate
KEEP / STRENGTHEN

Python / Rule候補:

~~~text
Condition matching
Version checks
Boundary checks
Constraint matching
Relationship / dependency lookup
Deterministic applicability
Cost / EV calculations
Runtime deviation measurement
Trace construction
~~~

AI候補:

~~~text
Text Knowledge interpretation
Context comparison
Conflict explanation
Alternative Decision Thesis generation
Knowledge relationship suggestion
Human-readable rationale
~~~

重要:

~~~text
AI says similar
≠ Applicable

AI says Long
≠ Decision

AI says safe
≠ Capital Permission
~~~

Hard constraintsをAIだけで解除しない。

---

# 16.32 R3 Candidate Flow

~~~text
R2 Validated Research Result
        ↓
Knowledge Admission / Formation
        ↓
Knowledge Domain
        ├─ Semantics
        ├─ Relationships
        ├─ Version
        ├─ Lifecycle
        └─ Revalidation
        ↓
        │
Current Market Understanding / State / Quality
        │
        └──────────────┐
                       ↓
              Applicability Assessment
                       ↓
             Applicable / Excluded Trace
                       ↓
          Conflict / Overlap Detection
                       ↓
              Decision Synthesis
                       ↓
           Decision Thesis / Candidate
                       ↓
            Economic Value Assessment
                       ↓
          Economic Decision Candidate
                       ↓
                      R4

Parallel Runtime:
Active Decision / Position Assumptions
+
Current Runtime Context
↓
Runtime Assumption Monitoring
├→ R4 Fast Safety
└→ R5 Feedback / Research
~~~

---

# 16.33 R3 Concept Classification

| Concept | Phase 5 R3 Candidate |
|---|---|
| Foundation vs Research Knowledge separation | KEEP / STRENGTHEN |
| Knowledge Admission | KEEP / REDESIGN |
| Knowledge Promotion naming | REDESIGN |
| Knowledge Formation | NEW / KEEP responsibility |
| Knowledge Semantics | KEEP / STRENGTHEN |
| Knowledge Family | REDESIGN |
| Knowledge Relationship | KEEP / REDESIGN |
| Knowledge Pool / Library | MERGE / REDESIGN logical domain |
| Knowledge Graph | REDESIGN as derived view |
| Knowledge Version | KEEP / STRENGTHEN |
| Knowledge Lifecycle | KEEP / REDESIGN |
| Lifecycle Assessment | NEW / KEEP |
| Lifecycle Transition Authority | NEW / DEFER exact authority |
| Knowledge Aging / Revalidation | KEEP / STRENGTHEN |
| Failure Boundary | KEEP |
| Constraint | SPLIT into research / knowledge / runtime-authorized |
| Applicability | KEEP / STRENGTHEN |
| Applicability Assessment | KEEP |
| Applicable Knowledge Set | REDESIGN |
| Runtime Assumption Monitoring | NEW / KEEP |
| Runtime contradiction → research | KEEP / REDESIGN |
| Knowledge Conflict Detection | KEEP |
| Knowledge Independence / Overlap | KEEP / STRENGTHEN |
| Decision Synthesis / Conflict Resolution | NEW / KEEP |
| Trade Thesis | REDESIGN to broader Decision Thesis candidate |
| Decision Scope / Horizon | NEW |
| Expected Value | KEEP / REDESIGN |
| Economic Value Assessment | KEEP / STRENGTHEN |
| Signal Engine | DROP as required top-level |
| R3 → R4 Economic Decision Candidate | NEW / REDESIGN |
| Runtime direct Knowledge update | DROP |
| Knowledge direct Capital Permission | DROP |

---

# 16.34 R3 Open Questions for Later Design

~~~text
1. Knowledge Admission authority
2. Knowledge semantic minimum contract
3. Knowledge Family taxonomy
4. Knowledge Relationship vocabulary
5. Knowledge Lifecycle state machine
6. Lifecycle transition writer / approval authority
7. Aging / revalidation trigger policy
8. Foundation → Knowledge transition rule after research
9. Applicability state taxonomy
10. Applicability hard vs soft condition rules
11. Runtime assumption monitoring threshold
12. Knowledge conflict taxonomy
13. Conflict resolution policy
14. Decision Thesis exact name / contract
15. Decision Scope representation
16. EV model / calibration / distribution representation
17. cost / slippage source and freshness
18. uncertain EV handling
19. R3 → R4 exact handoff object
20. Knowledge Constraint → Runtime Authorized Constraint governance
21. Knowledge Graph / relation-view implementation need
22. Runtime applicability performance requirements
23. AI interpretation failover
~~~

---

# 16.35 Phase State

~~~text
Phase 5 R1
COMPLETE / WORKING CANDIDATE

Phase 5 R2
COMPLETE / WORKING CANDIDATE

Phase 5 R3
COMPLETE / WORKING CANDIDATE

NEXT:
R4 — Capital / Production
~~~

重要:

~~~text
R3 COMPLETE
≠ Final Knowledge / Decision Architecture

Trade Thesis redesign
≠ trading removed

Signal Engine dropped as mandatory concept
≠ no action output

Runtime monitoring
≠ Knowledge mutation authority
~~~


---

# 16. Checkpoint 009 — Phase 5 R3 Concept-Level Reconstruction

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction  
**Scope:** R3 — Knowledge / Applicability / Decision Preparation

## 16.1 R3 Purpose Candidate

R3の責任候補:

> R2のValidated Research Resultを、その結果の身分・条件・限界・Evidence・Uncertaintyを失わず再利用可能なResearch KnowledgeへAdmissionし、KnowledgeのVersion / Lifecycle / Revalidationを管理し、R1のCurrent Market Contextと照合して現在のApplicabilityを評価し、複数KnowledgeのConflict / Overlap / Horizon差を整理したうえでDecision Thesis候補へ統合し、Known Cost / Uncertaintyを含むEconomic Valueを評価してR4へ渡す。

R3は以下を行わない。

~~~text
FoundationをResearch Knowledgeとして自動昇格しない
Research Resultを自動Knowledge化しない
Runtime LossだけでKnowledgeを直接Retireしない
Applicable Knowledgeを多数決でDecisionへ変換しない
Positive EVだけでCapital Permissionを出さない
Executionを行わない
Positionを直接閉じない
~~~

---

# 16.2 R3は4つの主要責任に分ける候補

~~~text
A. Knowledge Maintenance
B. Current Applicability
C. Decision Synthesis / Conflict Resolution
D. Economic Value Assessment
~~~

さらにFast Runtime側で、

~~~text
E. Runtime Knowledge Assumption Monitoring
~~~

を持つ候補。

重要:

~~~text
Knowledge Health
≠
Current Applicability
≠
Decision Thesis
≠
Expected Value
≠
Capital Permission
~~~

---

# 16.3 FoundationとResearch Knowledgeを分離

## Decision Candidate
KEEP / STRENGTHEN

R1 Foundation:

> Research prior / background understanding / mechanism candidate / structural fact等。

R3 Research Knowledge:

> 市場理解OS自身のResearchを通じて、再利用可能な意味としてAdmissionされた条件付き知識。

重要:

~~~text
Foundation
≠
Research Knowledge

Foundation Claim
≠
Validated Research Result

Validated Research Result
≠
Knowledge
~~~

Research KnowledgeがFoundationと矛盾することも許容する。

一回のResearch ResultでFoundationを自動書換えしない。
Foundation変更は別のReview / Research routeへ送る。

---

# 16.4 Knowledge Admission

## Decision Candidate
KEEP / STRENGTHEN

Input:

~~~text
Validated Research Result
~~~

Admissionが確認する候補:

~~~text
再利用可能な意味があるか
Claim / Findingの身分が明確か
対象Market / Asset / Horizonが分かるか
成立条件が追跡できるか
Failure Boundaryが追跡できるか
Constraint Candidateが追跡できるか
Evidence provenanceを辿れるか
Uncertaintyが保存されているか
Research Mode / Validation historyを辿れるか
Version / lineageを作れるか
既存Knowledgeとの重複・更新・矛盾を判定可能か
Negative / Null resultとして保存価値があるか
~~~

Output候補:

~~~text
ADMIT
MERGE / UPDATE CANDIDATE
DEFER
REJECT AS KNOWLEDGE
NEED MORE CONTEXT
~~~

重要:

~~~text
Research ResultがSUPPORTED
≠
Knowledge Admission必須

Research ResultがREFUTED
≠
Knowledge価値なし
~~~

---

# 16.5 Knowledge Formation

## Decision Candidate
KEEP / REDESIGN

Knowledgeは単純な一文にしない。

最低限保持すべき意味候補:

~~~text
Claim / Effect / Finding
Knowledge Type
Target Market / Asset
Time Horizon
Scope
成立条件
成立しやすいMarket State
弱くなる条件
Failure Boundary
Constraint Knowledge
Evidence Profile reference
Uncertainty
Regime dependence
Version
Validation history
Source Research Result
Known exceptions
Open questions
~~~

重要:

~~~text
Knowledge
=
条件付きで再利用可能な意味

Knowledge
≠
Trade Rule
≠
Signal
~~~

---

# 16.6 Positive / Negative / Boundary / Unknown Knowledge

## Decision Candidate
KEEP / STRENGTHEN

Knowledge family候補:

~~~text
Positive / Edge Knowledge
Negative / No-Edge Knowledge
Refutation Knowledge
Failure / Boundary Knowledge
Constraint Knowledge
Mechanism Knowledge
Context Knowledge
Uncertainty / Unknown Knowledge
Replication / Generalization Knowledge
~~~

正式Type Registryは後。

例:

~~~text
Funding単独ではDirectional Edgeを確認できなかった
~~~

もKnowledge候補。

~~~text
High Volatility + Thin LiquidityではこのEdgeが崩れる
~~~

もKnowledge候補。

~~~text
原因は特定不能だが、特定Regimeで再現性が消える
~~~

も価値あるKnowledge候補。

---

# 16.7 Knowledge Relationship

## Decision Candidate
KEEP / REDESIGN

Knowledge同士の関係を追跡できる責任を残す。

候補意味:

~~~text
supports
contradicts
refines
narrows
generalizes
overlaps
depends_on
derived_from
supersedes
replicates
fails_under
shares_evidence_with
~~~

正式Relation Enumは後。

目的:

- 多数決防止
- Duplicate / overlap識別
- Shared Evidence識別
- Version / supersession理解
- Multi-horizon coexistence理解
- Knowledge GraphをDerived Viewとして作れるようにする

重要:

~~~text
Knowledge Relationship
≠
新しいKnowledgeの自動生成
~~~

---

# 16.8 Knowledge Pool / Knowledge Graph

## Decision Candidate
MERGE / REDESIGN

~~~text
Knowledge Pool
=
Logical Knowledge Domain

Knowledge Graph
=
Knowledge / Relationを探索するDerived View候補
~~~

とする。

重要:

~~~text
Knowledge Graph
≠
Duplicate Source of Truth

Knowledge Pool
≠
One giant database object
~~~

Knowledge semanticsのCanonical sourceと、検索 / Graph / Vector等のViewを分ける。

---

# 16.9 Knowledge Version / Lineage

## Decision Candidate
KEEP / STRENGTHEN

~~~text
Knowledge v1
↓
Revalidation / New Evidence
↓
Knowledge v2
~~~

を許容する。

過去Versionを消さない。

追跡候補:

~~~text
Created From
Version
Valid From
Last Validation
Supersedes
Superseded By
Reason for Change
Evidence delta
Boundary delta
Scope delta
~~~

重要:

~~~text
Knowledge Update
≠
History Rewrite
~~~

---

# 16.10 Knowledge LifecycleとKnowledge Healthを分ける

## Decision Candidate
REDESIGN

Knowledge Ageだけで自動Retireしない。

分離候補:

### Lifecycle State

~~~text
ACTIVE
UNDER_REVIEW
WEAK / DEGRADED
RETIRED
SUPERSEDED
ARCHIVED
~~~

正式Stateは後。

### Health / Revalidation Assessment

見る候補:

~~~text
Validation Age
Recent contradiction
Replication status
Forward evidence age
Production evidence drift
Market structure change
Boundary violations
Source / method obsolescence
External structural change
~~~

重要:

~~~text
Old
≠
False

Recent Loss
≠
Knowledge Invalid

Age
≠
Health
~~~

AgeはRevalidation Priorityを上げる要因になり得るが、単独でRetire理由にしない。

---

# 16.11 Knowledge Revalidation

## Decision Candidate
KEEP / STRENGTHEN

Revalidation trigger候補:

~~~text
Periodic schedule
Validation age
Repeated contradiction
Replication failure
Applicability mismatch
Production drift
Market structure change
Regulation / venue change
New competing Knowledge
Foundation revision
Major data-method change
~~~

Flow候補:

~~~text
Knowledge Revalidation Need
↓
Research Question
↓
R2
↓
Validated Research Result
↓
R3 Knowledge Maintenance
↓
new version / lifecycle update candidate
~~~

重要:

~~~text
Revalidation Need
≠
Immediate Retire
~~~

---

# 16.12 Knowledge Lifecycle Writer / Authority

## Decision Candidate
NEW / DEFER exact authority

Knowledge Health AssessmentとKnowledge State変更を分離する。

~~~text
Assessment:
Knowledge weak / stale / contradicted可能性

≠

State Transition:
ACTIVE → UNDER_REVIEW / RETIRED
~~~

誰が最終State Transition Authorityを持つかはX06 Governanceで後決め。

AI / Runtime Monitorが直接Retire writerにならない。

---

# 16.13 Current Applicability

## Decision Candidate
KEEP / STRENGTHEN

Input候補:

~~~text
Knowledge
+
R1 Current Market Understanding
+
Current State Representation
+
Quality / Freshness
+
Current Relation Interpretation
+
Runtime / Event Context
~~~

問い:

> このKnowledgeは、今この市場を理解・判断する材料として使えるか？

見る候補:

~~~text
Market / Asset
Horizon
Regime
Trend
Volatility
Liquidity
Leverage
Funding
Flow
Participant state
Macro
Event
Session
Data Quality
Freshness
Knowledge validation age
Failure Boundary
Constraint
Uncertainty
~~~

---

# 16.14 Applicability State

## Decision Candidate
KEEP / REDESIGN

候補:

~~~text
APPLICABLE
PARTIALLY_APPLICABLE
NOT_APPLICABLE
UNCERTAIN
BLOCKED_BY_CONSTRAINT
NOT_EVALUATED
~~~

正式Enumは後。

重要:

~~~text
NOT_APPLICABLE
≠
RETIRED

UNCERTAIN
≠
NEGATIVE

APPLICABLE
≠
TRADE
~~~

---

# 16.15 Applicability Assessment

## Decision Candidate
KEEP / STRENGTHEN

各Knowledgeについて理由を残す。

候補意味:

~~~text
Knowledge reference
Applicability state
Matched conditions
Missing conditions
Current deviations
Failure Boundary status
Constraint status
Contradictions
Evidence / validation-age context
Uncertainty
Overlap / dependency context
Evaluation time
~~~

Downstreamが、

> なぜ今回このKnowledgeを使った / 使わなかったか

を後から説明できるようにする。

---

# 16.16 Runtime Assumption Monitoring

## Decision Candidate
NEW / SPLIT from pre-decision Applicability

Trade開始後もKnowledge成立条件を監視する責任候補。

監視対象:

~~~text
Entry時に成立していたKnowledge assumptions
Current Market State deviation
Failure Boundary approach / crossing
Constraint activation
Data Quality degradation
Material relation change
Unexpected regime shift
~~~

Output候補:

~~~text
ASSUMPTION_STABLE
ASSUMPTION_DEGRADED
MATERIAL_DEVIATION
BOUNDARY_APPROACHING
BOUNDARY_CROSSED
UNCERTAIN
~~~

正式Stateは後。

重要:

~~~text
Runtime Assumption Monitoring
≠
Knowledge Rewrite

Runtime Assumption Monitoring
≠
Position Close Authority
~~~

R3はsemantic deviationを検出。

R4が、

~~~text
continue
reduce
protect
exit
block new exposure
~~~

等のCapital / Position actionを判断する。

---

# 16.17 Applicability Contradiction

## Decision Candidate
KEEP / STRENGTHEN

Repeated case:

~~~text
Knowledge says conditions matched
↓
Runtime repeatedly behaves outside expected range
~~~

の場合、

~~~text
Applicability Contradiction
↓
R5 / R2 Research Question
~~~

へ戻す。

R3自身が即Knowledgeを書き換えない。

---

# 16.18 Knowledge Conflictの前にScope / Horizonを揃える

## Decision Candidate
NEW / STRENGTHEN

見かけ上のConflictが本当の矛盾とは限らない。

例:

~~~text
K1:
4h horizon bullish

K2:
5m horizon bearish
~~~

は同時成立可能。

したがってConflict Resolution前に、

~~~text
Market
Asset
Horizon
Scope
Regime
Decision objective
~~~

を正規化する。

重要:

~~~text
Different direction
≠
Contradiction automatically
~~~

---

# 16.19 Knowledge Conflict / Overlap / Dependency

## Decision Candidate
KEEP / STRENGTHEN

Conflict候補:

~~~text
semantic contradiction
effect-direction conflict
condition conflict
boundary conflict
constraint conflict
horizon conflict
evidence conflict
~~~

Overlap候補:

~~~text
same evidence
same source research
same mechanism
derived knowledge
duplicate scope
shared cause
~~~

重要:

~~~text
Knowledge Count
≠
Independent Support Count
~~~

---

# 16.20 Decision Synthesis / Conflict Resolution

## Decision Candidate
NEW / KEEP

R3に明示的責任として置く。

Input:

~~~text
Applicable Knowledge Assessments
Current Market Understanding
Knowledge Relationships
Conflict / Overlap / Dependency
Horizon / Scope
Uncertainty
Current decision objective
~~~

目的:

> 複数Knowledgeから、現在の市場に対して何をする経済的Thesis候補が存在するかを組み立てる。

Output候補:

~~~text
Decision Thesis Candidate
Action Direction Candidate
WAIT candidate
NO-TRADE candidate
UNKNOWN candidate
Multiple competing thesis candidates
~~~

重要:

~~~text
Decision Synthesis
≠
Majority Vote

Decision Synthesis
≠
Risk Permission

Decision Synthesis
≠
Execution
~~~

---

# 16.21 Trade Thesisという名称

## Decision Candidate
REDESIGN / DEFER name

Legacy TradeThesisの責任は有用。

ただし将来Multi-Market / Non-trade decisionも考慮し、

~~~text
Decision Thesis
Economic Thesis
Trade Thesis
Opportunity Thesis
~~~

のどの名称を使うかは後決め。

必要な意味:

~~~text
何を期待しているか
どの方向か
どのHorizonか
どのKnowledgeに基づくか
どの条件で成立するか
何が反証するか
どのUncertaintyがあるか
~~~

---

# 16.22 Decision Synthesisの正常Output

## Decision Candidate
NEW / STRENGTHEN

必ずTrade候補を作る必要はない。

正常Output候補:

~~~text
LONG thesis candidate
SHORT thesis candidate
WAIT
NO TRADE
UNKNOWN
MULTIPLE COMPETING THESIS
INSUFFICIENT ECONOMIC BASIS
~~~

重要:

~~~text
No Trade
≠
System Failure
~~~

---

# 16.23 Economic Value Assessment

## Decision Candidate
KEEP / REDESIGN

Decision Thesis候補について、

> Riskを取る前に、経済的に意味のあるOpportunityか？

を評価する。

候補Input:

~~~text
Outcome distribution
Expected gain
Expected loss
Probability / calibration
Uncertainty
Time horizon
Fees
Funding / carry
Estimated slippage / impact
Liquidity assumptions
Opportunity cost
Expected holding time
Known failure probability / tail sensitivity
~~~

重要:

~~~text
Win Rate
≠
Expected Value
~~~

~~~text
Applicable
≠
Positive EV
~~~

~~~text
Positive EV
≠
Capital Permission
~~~

---

# 16.24 EVとExecution Costの境界

## Decision Candidate
NEW / REDESIGN

R3はEconomic Value計算に必要なCost Estimateを参照できる。

ただし実際のExecution条件の最終責任はR4。

候補:

~~~text
R3:
expected / modeled fee, funding, slippage, impact assumptions

R4:
current executable liquidity, order constraints, actual venue / size impact
~~~

R4でCost条件が materially differentなら、Economic Opportunityを再評価 / blockできる。

---

# 16.25 Economic Opportunity Boundary

## Decision Candidate
NEW

R3 → R4の主要Boundary候補。

含む意味候補:

~~~text
Decision Thesis Candidate
Direction / Action semantics
Horizon
Applicable Knowledge references
Conflict / overlap context
Expected Value assessment
Cost assumptions
Uncertainty
Invalidation conditions
Boundary / constraint context
Decision timestamp / information set
~~~

重要:

~~~text
Economic Opportunity
≠
Risk Permission
≠
Capital Allocation
≠
Execution Intent
~~~

---

# 16.26 R3 Two-Speed Structure

## Slow / Maintenance Path

~~~text
Validated Research Result
↓
Knowledge Admission
↓
Knowledge Formation / Version
↓
Lifecycle / Revalidation
↓
Knowledge Domain
~~~

## Runtime Decision Path

~~~text
Knowledge Domain
+
Current Market Understanding
↓
Applicability
↓
Decision Synthesis
↓
Economic Value
↓
Economic Opportunity
↓
R4
~~~

## Fast Runtime Monitoring Path

~~~text
Active Decision / Position Knowledge Assumptions
+
Current Runtime Context
↓
Assumption Monitoring
↓
Deviation / Boundary Warning
↓
R4 Fast Safety
+
R5 Feedback
~~~

重要:

~~~text
Runtime path
does not wait for new Knowledge creation.

Maintenance path
does not directly modify live Position.
~~~

---

# 16.27 R3 → R2 Feedback

R3がResearchへ戻す主なQuestion Source候補:

~~~text
Knowledge Revalidation Need
Knowledge contradiction
Applicability contradiction
Repeated boundary approach
Unexpected regime dependency
Knowledge conflict unresolved by scope
Evidence / validation age concern
Foundation vs Research Knowledge contradiction
Runtime assumption repeated failure
~~~

R3自身がResearchを直接実行しない。

---

# 16.28 R3 → R4 Boundary

R4へ渡すもの候補:

~~~text
Economic Opportunity
Current Decision Thesis candidate
Expected Value
Uncertainty
Invalidation / assumption conditions
Constraint / boundary context
Required execution assumptions
Relevant applicability trace
~~~

R4が決めるもの:

~~~text
Capital permission
Position size
Portfolio compatibility
Risk budget
Exposure limits
ALLOW / REDUCE / BLOCK
Execution admission
Runtime protection action
~~~

---

# 16.29 R3 Candidate Flow

~~~text
R2 Validated Research Result
          ↓
Knowledge Admission
          ↓
Knowledge Formation
          ↓
Knowledge Version / Relationship
          ↓
Knowledge Lifecycle / Revalidation
          ↓
       Knowledge Domain
          │
          │ + R1 Current Market Understanding
          ↓
Applicability Evaluation
          ↓
Applicability Assessments
          ↓
Scope / Horizon Normalization
          ↓
Conflict / Overlap / Dependency Analysis
          ↓
Decision Synthesis
          ↓
Decision Thesis Candidate(s)
          ↓
Economic Value Assessment
          ↓
Economic Opportunity
          ↓
R4 Capital / Production
~~~

Parallel runtime:

~~~text
Active Thesis / Knowledge Assumptions
+
R1 Runtime Context
↓
Runtime Assumption Monitoring
↓
Deviation / Boundary Signal
├→ R4 Fast Safety
└→ R5 / R2 Feedback
~~~

---

# 16.30 R3 Concept Classification

| Concept | Phase 5 R3 Candidate |
|---|---|
| Foundation vs Research Knowledge separation | KEEP / STRENGTHEN |
| Knowledge Admission | KEEP / STRENGTHEN |
| Knowledge Formation | KEEP / REDESIGN |
| Positive / Negative / Boundary / Unknown Knowledge | KEEP / STRENGTHEN |
| Knowledge Relationship | KEEP / REDESIGN |
| Knowledge Pool | KEEP as logical domain |
| Knowledge Graph | REDESIGN as derived view |
| Knowledge Version / Lineage | KEEP / STRENGTHEN |
| Knowledge Lifecycle | KEEP / REDESIGN |
| Knowledge Health Assessment | NEW / KEEP |
| Automatic age-based retirement | DROP |
| Revalidation | KEEP / STRENGTHEN |
| Lifecycle Writer Authority | NEW / DEFER |
| Applicability | KEEP / STRENGTHEN |
| Applicability Assessment | KEEP / STRENGTHEN |
| Runtime Assumption Monitoring | NEW / SPLIT |
| Runtime direct Knowledge rewrite | DROP |
| Knowledge Conflict | KEEP / STRENGTHEN |
| Scope / Horizon normalization | NEW |
| Majority-vote Knowledge integration | DROP |
| Decision Synthesis | NEW / KEEP |
| TradeThesis exact name | REDESIGN / DEFER |
| WAIT / NO TRADE / UNKNOWN outcomes | KEEP / STRENGTHEN |
| Expected Value | KEEP / REDESIGN |
| Win-rate-as-EV | DROP |
| Economic Opportunity boundary | NEW |
| Signal Engine as required top-level concept | DROP |
| R3 direct Risk Permission | DROP |
| R3 direct Execution | DROP |

---

# 16.31 R3 Open Questions for Later Design

~~~text
1. Knowledge Admission authority
2. Knowledge Type Registry
3. Knowledge Relationship formal taxonomy
4. Canonical Knowledge semantics / minimum contract
5. Knowledge lifecycle state machine
6. Knowledge Health assessment formula / policy
7. Revalidation scheduling / priority
8. Knowledge state transition writer
9. Applicability state taxonomy
10. Applicability matching method
11. Market State Representation dependency level
12. Runtime Assumption Monitoring thresholds
13. Semantic deviation vs noise distinction
14. Multi-horizon thesis normalization
15. Knowledge conflict resolution method
16. Decision Thesis exact object / name
17. WAIT / NO TRADE / UNKNOWN semantics
18. EV probability calibration
19. Cost / slippage model ownership
20. Tail risk representation before R4
21. Economic Opportunity minimum contract
22. Constraint Candidate → Runtime Authorized Constraint governance
23. Foundation contradiction handling
24. Knowledge migration across market expansion
25. AI-assisted applicability / synthesis reproducibility
~~~

---

# 16.32 Phase State

~~~text
Phase 5 R1
COMPLETE / WORKING CANDIDATE

Phase 5 R2
COMPLETE / WORKING CANDIDATE

Phase 5 R3
COMPLETE / WORKING CANDIDATE

NEXT:
R4 — Capital / Production
~~~

重要:

~~~text
R3 COMPLETE
≠
Final Knowledge / Decision Architecture

Knowledge Admission
≠
Production Approval

Applicability
≠
Decision

Decision Thesis
≠
Positive EV

Positive EV
≠
Capital Permission
~~~


---

# 17. Checkpoint 010 — Phase 5 R4 Concept-Level Reconstruction

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction  
**Scope:** R4 — Capital / Production

## 17.1 R4 Purpose Candidate

R4の責任候補:

> R3から受け取ったEconomic Opportunityを、資本全体・Portfolio Exposure・Risk Budget・Drawdown・Tail Risk・Liquidity・Authorized Constraint・System Health等と照合して「実資金を出してよいか」「どの程度まで許可するか」を判断し、許可されたIntentをVenueへ安全にExecutionし、成立したExposureをCanonical Positionとして追跡しながら、Runtime中のMarket / Knowledge Assumption / System変化に応じてPositionを保護し、最終OutcomeをR5へ渡す。

R4は以下を行わない。

~~~text
Research ResultをKnowledgeへ変換しない
Knowledge Applicabilityを再定義しない
Positive EVだけで自動Tradeしない
Emergency Fast Pathで新しいEdgeを作らない
Exchange Adapter responseをCanonical Position Truthにしない
Runtime LossだけでKnowledgeをRetireしない
Execution FailureをMarket Failureへ変換しない
~~~

---

# 17.2 R4を5責任へ分ける候補

~~~text
A. Capital / Portfolio Permission
B. Execution Admission / Intent
C. Execution Fidelity / Reconciliation
D. Position / Exposure Truth
E. Runtime Protection / Exit
~~~

横断:

~~~text
RiskState
Authorized Constraints
Emergency Fast Path
System Health
Human / Governance Authority
~~~

重要:

~~~text
Economic Opportunity
≠ Capital Permission
≠ Execution Intent
≠ Filled Position
≠ Runtime Protection Decision
~~~

---

# 17.3 R3 → R4 Entry Boundary

## Decision Candidate
KEEP / STRENGTHEN

R3からの主要Input候補:

~~~text
Economic Opportunity
Decision Thesis / Action Candidate
Expected Value assessment
Uncertainty
Decision horizon / scope
Supporting Knowledge
Opposing / excluded Knowledge
Applicability rationale
Invalidation conditions
Failure Boundary / Constraint context
Runtime assumptions to monitor
Cost / liquidity assumptions
Decision timestamp / information set
~~~

R4はこれを、

~~~text
BUY/SELL signal
~~~

だけへ潰して受け取らない。

目的:

- Risk判断時に根拠を追える
- Position保有中にThesis / assumptionsを再参照できる
- Outcome後にDecision Qualityを評価できる

---

# 17.4 Capital Permission

## Decision Candidate
NEW / KEEP responsibility

R4で最初に答える問い:

> Economic Opportunityが存在するとして、現在の資本状態でRiskを取ることを許可できるか？

Output候補:

~~~text
ALLOW
ALLOW_WITH_LIMIT
REDUCE_ONLY
BLOCK_NEW_EXPOSURE
BLOCK
DEFER / UNKNOWN
~~~

正式Enumは後。

重要:

~~~text
Positive EV
≠ ALLOW

High Confidence
≠ ALLOW

Applicable Knowledge
≠ ALLOW
~~~

---

# 17.5 Capital State / Portfolio Context

## Decision Candidate
NEW / STRENGTHEN

単一Tradeではなく資本全体を見る。

参照候補:

~~~text
Total Capital
Free Capital
Reserved Capital
Current Exposure
Gross Exposure
Net Exposure
Leverage
Open Positions
Pending Orders
Unrealized PnL
Realized Drawdown
Current Drawdown
Risk Budget Used
Venue Exposure
Asset Concentration
Directional Concentration
Strategy / Knowledge Concentration
Correlation / Common Factor
Liquidity Exposure
Tail Exposure
Operational Exposure
~~~

重要:

~~~text
3 positions
≠
3 independent risks
~~~

例:

~~~text
BTC Long
ETH Long
NASDAQ Long
~~~

が同一Risk-On factorへ強く依存するなら、Portfolioでは集中Riskとして扱える必要がある。

---

# 17.6 Risk Budget

## Decision Candidate
NEW / KEEP

資本を無制限にOpportunityへ割り当てない。

候補概念:

~~~text
Global Risk Budget
Portfolio Risk Budget
Market / Asset Risk Budget
Strategy / Thesis Risk Budget
Position Risk Budget
Venue Risk Budget
Emergency Reserve
~~~

正式階層は後。

Risk Budgetは、

> 「何円使えるか」だけでなく、「どれだけ損失分布 / Exposure / Tailを許容するか」を表す責任候補。

重要:

~~~text
Capital Available
≠ Risk Budget Available
~~~

---

# 17.7 Position Sizing

## Decision Candidate
NEW / STRENGTHEN

Position Sizeを固定額やConfidenceだけで決めない。

入力候補:

~~~text
Economic Value
Expected loss distribution
Uncertainty
Failure Boundary distance
Liquidity
Slippage / impact
Volatility
Current portfolio exposure
Correlation / common factor
Risk budget
Drawdown state
Venue limits
Leverage constraints
Tail sensitivity
Decision horizon
~~~

重要:

~~~text
Higher confidence
≠ linearly larger size

Positive EV
≠ maximum size
~~~

Position sizingはCapital Permissionの一部または直後責任候補。

---

# 17.8 Drawdown / Ruin / Survival Context

## Decision Candidate
NEW / STRENGTHEN

Phase 2で厳密なSurvival > Profit序列は未固定だが、R4は少なくとも以下を扱える必要がある。

~~~text
Current Drawdown
Drawdown acceleration
Loss streak
Risk budget exhaustion
Tail loss scenario
Ruin / near-ruin condition
Margin exhaustion
Liquidity shock
Cross-position cascade
Venue failure exposure
~~~

重要:

~~~text
High EV opportunity
+
capital survival threat
↓
can still be BLOCKED
~~~

具体Thresholdは後。

---

# 17.9 Concentration / Correlation / Common Dependency

## Decision Candidate
NEW

Portfolio riskは単純なAsset別合計だけにしない。

見る候補:

~~~text
Asset correlation
Cross-market correlation
Shared macro factor
Shared liquidity factor
Shared venue
Shared collateral
Shared stablecoin
Shared Knowledge / Strategy
Shared data dependency
Shared event sensitivity
~~~

目的:

> 見かけ上分散していても同じFailure原因へ集中しているPortfolioを検出できること。

---

# 17.10 Runtime Authorized Constraint

## Decision Candidate
NEW / STRENGTHEN

R2のResearch Constraint Candidate、R3のKnowledge Constraintと、本番強制Constraintを分離する。

~~~text
R2:
Research Constraint Candidate

R3:
Knowledge Constraint

R4 / X06:
Runtime Authorized Constraint
~~~

Runtime Authorized Constraint候補:

~~~text
Max leverage
Max position size
Max portfolio exposure
Venue limit
Liquidity minimum
Data quality minimum
Event restriction
Market-hours restriction
Drawdown restriction
RiskState restriction
Emergency restriction
~~~

重要:

~~~text
Research found constraint
≠ Production constraint automatically
~~~

本番強制化にはAuthority / Governanceを通す。

---

# 17.11 RiskState

## Decision Candidate
KEEP / REDESIGN

LegacyのRiskState思想は再利用価値が高い。

目的:

> 現在のProduction risk postureを一つのCanonical Stateとして表現し、Capital / Execution / Runtime Protectionが同じSafety postureを参照できるようにする。

State候補イメージ:

~~~text
NORMAL
CAUTION
RESTRICTED
REDUCE_ONLY
EMERGENCY
RECOVERY
~~~

正式Stateは後。

重要:

~~~text
RiskState
≠ Market Regime
≠ Knowledge Applicability
≠ System Health
~~~

---

# 17.12 RiskState Writer

## Decision Candidate
KEEP single-writer principle / DEFER implementation

同じRiskStateを複数Moduleが直接書き換えない。

~~~text
Recommendation
↓
Risk evaluation
↓
Authorized transition
↓
RiskState
~~~

を基本候補とする。

重要:

~~~text
Monitoring Alert
≠ RiskState Change

AI Recommendation
≠ RiskState Change

Research Constraint
≠ RiskState Change
~~~

exact writer / authorityはX06で後決め。

---

# 17.13 Emergency Fast Path

## Decision Candidate
KEEP / STRENGTHEN

Phase 4 Two-Speed思想をR4へ正式配置候補。

Fast Path Input候補:

~~~text
R1 Runtime Market Context
R3 Runtime Assumption Monitoring
R4 Position / Exposure
X10 System Health / Incident
Venue status
Liquidity collapse
Data quality collapse
Margin state
Authorized emergency constraints
~~~

重要原則:

> Emergency Fast PathはResearch完了を待たずにRiskを減らせる。

---

# 17.14 Emergency Fast Pathの非対称性

## Decision Candidate
NEW / STRONG CANDIDATE

Fast PathはRiskを増やす方向へ使わない。

許容候補:

~~~text
BLOCK new exposure
CANCEL pending exposure
REDUCE
PROTECT
EXIT
HEDGE within pre-authorized limits
FREEZE
~~~

禁止候補:

~~~text
新しい未検証Tradeを開始
Positionを拡大
新しいKnowledgeを作る
Risk Limitを緩和
Emergencyを理由にResearch Ruleを飛ばす
~~~

原則:

~~~text
Fast Safety
=
risk-reducing / risk-containing path

Fast Safety
≠
fast alpha path
~~~

これはR4の重要Safety候補。

---

# 17.15 Recovery Strict Path

## Decision Candidate
KEEP / REDESIGN

Emergency状態から通常状態へ戻す時は、Risk低減より厳格にする候補。

~~~text
Emergency
↓
Condition recovered?
↓
System healthy?
↓
Data reliable?
↓
Position reconciled?
↓
Risk authority approval?
↓
RECOVERY
↓
NORMAL / CAUTION
~~~

重要:

~~~text
危険検知
→ 自動で厳しくする
~~~

ことと、

~~~text
危険解除
→ 自動ですぐ緩める
~~~

ことを対称にしない。

Risk relaxationはより厳しいGateを持つ候補。

---

# 17.16 Defense Layer

## Decision Candidate
SPLIT / DROP monolith

旧Defense Layerの責任を分解する。

~~~text
A. Capital / Portfolio Permission
B. Authorized Constraint
C. RiskState
D. Emergency Fast Path
E. Position Runtime Protection
~~~

「Defense」という一つの巨大LayerはRequired Architectureにしない。

Defense思想は各責任へ保持する。

---

# 17.17 Execution Admission

## Decision Candidate
KEEP / REDESIGN

Capital Permission後も、Execution可能とは限らない。

確認候補:

~~~text
Capital permission still valid
RiskState permits action
Authorized constraints satisfied
Venue available
Instrument tradable
Liquidity sufficient
Order size allowed
Price / spread conditions acceptable
No duplicate reservation
System health acceptable
Credential / permission valid
Decision not stale
~~~

Output候補:

~~~text
EXECUTION_ALLOWED
REDUCE_SIZE
DEFER
BLOCK
UNKNOWN
~~~

正式Stateは後。

---

# 17.18 Decision Staleness / Time Validity

## Decision Candidate
NEW / STRENGTHEN

R3で作られたOpportunityが古くなっている可能性をExecution前に確認する。

見る候補:

~~~text
Decision timestamp
Market movement since decision
Current spread
Current liquidity
Current RiskState
Knowledge assumption deviation
Material event since decision
Data freshness
~~~

重要:

~~~text
Decision was valid at T0
≠
still executable at T1
~~~

必要ならR3再評価へ戻す。

---

# 17.19 Execution Intent

## Decision Candidate
KEEP / REDESIGN

Execution Intentは、

> Capital PermissionとExecution Admissionを通過したActionを、Venueへ渡せる意味へ変換したProduction instruction。

含む意味候補:

~~~text
Action
Asset / Instrument
Side
Target exposure / size
Allowed price / slippage boundaries
Time validity
Venue constraints
Protection requirements
Decision / Opportunity reference
Risk permission reference
Authorized constraints
Idempotency / reservation reference
~~~

重要:

~~~text
Execution Intent
≠ Order sent
≠ Fill
≠ Position
~~~

---

# 17.20 Execution Reservation / Idempotency

## Decision Candidate
KEEP / STRENGTHEN

重複発注防止。

例:

~~~text
API timeout
↓
response unknown
↓
same intent retried
↓
double order
~~~

を防ぐ。

候補責任:

~~~text
Intent reservation
Idempotency key
Pending execution ownership
Retry safety
Duplicate detection
~~~

重要:

~~~text
Timeout
≠
Order not accepted
~~~

---

# 17.21 Venue Routing

## Decision Candidate
KEEP / REDESIGN

複数Venueへ対応する場合、

~~~text
Venue availability
Fees
Liquidity
Spread
Capability
Order types
Minimum size
Collateral
Operational health
Counterparty / venue risk
~~~

を見てRouting可能にする。

ただしVenue RouterはCapital Authorityではない。

~~~text
Venue Router
≠
Risk Permission
~~~

---

# 17.22 Execution Attempt / Event

## Decision Candidate
KEEP

Executionは一発のBoolean successではない。

候補:

~~~text
Intent created
Submitted
Accepted
Rejected
Partially filled
Filled
Canceled
Expired
Unknown
Retry
Venue error
~~~

イベント履歴を追跡可能にする。

重要:

~~~text
API 200 OK
≠
Position exists
~~~

---

# 17.23 Execution Reconciliation

## Decision Candidate
KEEP / STRENGTHEN

Execution EventとVenue実状態を照合し、

> 本当に何が約定し、現在どのExposureが存在するか

を確認する。

入力候補:

~~~text
Execution Intent
Execution Attempts
Venue order status
Fills
Balance / position snapshot
Fees
Funding / carry
Cancellations
Unknown responses
~~~

Output候補:

~~~text
Reconciled execution facts
Unresolved execution state
Mismatch / incident
~~~

重要:

~~~text
Adapter response
≠
Canonical Execution Truth
~~~

---

# 17.24 Execution Record

## Decision Candidate
KEEP / REDESIGN

Reconciliation済みのExecution事実をCanonicalに保持する責任。

候補意味:

~~~text
What was intended
What was submitted
What was filled
At what price
At what size
Fees / cost
Which venue
Timing
Slippage
Unresolved differences
Trace to Decision / Risk permission
~~~

Execution RecordはTrade Resultではない。

---

# 17.25 Logical Position / Exposure Truth

## Decision Candidate
KEEP / STRENGTHEN

Venueごとの表示をそのままPosition Source of Truthにしない。

Logical Position候補:

> Reconciled Execution / Position Eventsから構成される、OSが認識するCanonical Exposure。

見る候補:

~~~text
Asset / Instrument
Net exposure
Gross exposure
Average entry
Venue distribution
Collateral
Leverage
Unrealized PnL
Protection status
Decision / Thesis references
Knowledge assumptions
Opened time
Current state
~~~

重要:

~~~text
Exchange position screen
≠
Canonical Logical Position automatically
~~~

---

# 17.26 Position Event

## Decision Candidate
KEEP

Positionは一つの静的RecordではなくEventで変化する。

候補:

~~~text
OPEN
INCREASE
REDUCE
PARTIAL EXIT
HEDGE
TRANSFER
PROTECTION ADDED
PROTECTION CHANGED
CLOSE
FORCED CHANGE
RECONCILIATION CORRECTION
~~~

Current PositionはEvent / execution factsからProjection可能にする方向。

---

# 17.27 Protection Requirement Ownership

## Decision Candidate
NEW / RESOLVE LEGACY GAP

Legacyで曖昧だった責任。

候補:

> R4 Capital / Productionが、Positionを持つために必要な最低Protection RequirementのCanonical Ownerになる。

Protection Requirementは、

~~~text
R3 Thesis invalidation / boundary
+
R4 Risk Permission
+
Position size
+
Liquidity / Venue capability
+
Global RiskState
+
Authorized Constraint
~~~

から生成・維持する候補。

重要:

~~~text
Knowledge Boundary
≠
Stop Order price directly
~~~

研究上のBoundaryを本番Protectionへ変換するのはR4責任。

---

# 17.28 Runtime Protection

## Decision Candidate
KEEP / STRENGTHEN

Position保有中は、

~~~text
R1 Runtime Market Context
R3 Assumption Monitoring
R4 Logical Position
RiskState
System Health
Liquidity
Margin
Authorized Constraints
Protection Requirement
~~~

を参照してProtectionを評価する。

Action候補:

~~~text
CONTINUE
WATCH
REDUCE
HEDGE
TIGHTEN PROTECTION
EXIT
BLOCK ADDITION
EMERGENCY CLOSE
~~~

正式Enumは後。

---

# 17.29 Runtime ProtectionとKnowledge Monitoringの境界

## Decision Candidate
KEEP SEPARATION

R3:

~~~text
Knowledge / thesis assumptionsが崩れたか？
~~~

を判断。

R4:

~~~text
その崩れ方とPosition / Risk状態を踏まえて、
資金をどう守るか？
~~~

を判断。

重要:

~~~text
R3 MATERIAL_DEVIATION
≠
automatic close

R4 EXIT
≠
Knowledge invalidated
~~~

---

# 17.30 Exit Decision

## Decision Candidate
KEEP / REDESIGN

Exit理由を一つにしない。

候補:

~~~text
Thesis fulfilled
Thesis invalidated
Economic value decayed
Risk budget exceeded
Portfolio conflict
Failure Boundary crossed
Constraint activated
Liquidity deteriorated
Emergency safety
Time horizon expired
Operational failure
Manual / governance override
~~~

Exitは、

~~~text
勝ち / 負け
~~~

だけで分類しない。

---

# 17.31 Protection Order Intent

## Decision Candidate
KEEP / REDESIGN

ProtectionのActionも通常Executionと同じくIntent → Attempt → Event → Reconciliationを通す。

~~~text
Protection Decision
↓
Protection Order Intent
↓
Execution
↓
Reconciliation
↓
Protection State
~~~

Protection आदेशだけ別の無追跡経路にしない。

---

# 17.32 Protection State

## Decision Candidate
KEEP / STRENGTHEN

現在Positionがどの程度保護されているかを追跡する。

候補意味:

~~~text
Required protection
Actual protection
Gap
Pending protection
Failed protection
Protection venue
Protection validity
Emergency backup state
~~~

重要:

~~~text
Protection order submitted
≠
Protection active
~~~

---

# 17.33 Operational / System Failure During Position

## Decision Candidate
KEEP / STRENGTHEN

例:

~~~text
Exchange API down
Websocket stale
Order status unknown
DB outage
Network failure
Credential failure
AI unavailable
Monitoring failure
~~~

をMarket Failure / Knowledge Failureと分ける。

必要に応じてX10 Incident / RecoveryとR4 Fast Safetyが協調する。

重要:

~~~text
System Failure
≠
Market Thesis Failure
~~~

---

# 17.34 Execution / Position Failure Paths

候補:

~~~text
Duplicate order
Partial fill
Unexpected fill
Rejected order
Stale order
Slippage breach
Venue unavailable
Position mismatch
Protection missing
Protection failed
Margin risk
Reconciliation unresolved
Unknown exposure
~~~

原則:

> Unknown Exposureは通常状態として扱わず、risk-reducing / freeze方向へ寄せる。

exact policyは後。

---

# 17.35 Production Outcome Boundary

## Decision Candidate
NEW / REDESIGN

R4の出口を単なるPnLにしない。

R5へ渡す候補:

~~~text
Decision / Opportunity reference
Capital permission decision
Risk context
Execution intent
Execution record
Position history
Protection history
Exit reason
Realized PnL
Unrealized path
Fees / funding / slippage
Runtime deviations
Incidents
Constraint activations
RiskState transitions
Counterfactual-relevant context
Information available at each decision time
~~~

これを、

~~~text
Production Outcome Package
~~~

等のLogical Boundary候補として扱う。

名称は後。

---

# 17.36 TradeResult

## Decision Candidate
REDESIGN

TradeResultはR4 Outcomeの一部として残せるが、Whole Outcome Source of Truthにはしない。

~~~text
TradeResult
=
financial result projection

Production Outcome
=
decision + risk + execution + position + protection + incident + financial result
~~~

重要:

~~~text
Profit
≠ Good Decision

Loss
≠ Bad Decision
~~~

R5がこれを評価する。

---

# 17.37 R4 Fast Safety Inputs

Fast pathへ直接利用可能な候補:

~~~text
R1:
material market change
quality / freshness degradation
liquidity shock
event shock

R3:
assumption degradation
boundary approaching
boundary crossed
applicability contradiction

R4:
portfolio exposure
margin / leverage
drawdown
protection state
unknown exposure

X10:
system incident
venue outage
data pipeline failure
credential failure
~~~

Fast pathはこれらを統合してRiskを減らせる。

---

# 17.38 R4 Slow / Fast Structure

## Slow Capital / Entry Path

~~~text
R3 Economic Opportunity
↓
Capital / Portfolio Evaluation
↓
Risk Permission
↓
Position Sizing
↓
Execution Admission
↓
Execution Intent
↓
Execution
↓
Position
~~~

## Fast Safety Path

~~~text
Runtime Market / Knowledge / System / Position change
↓
Emergency / Runtime Protection Evaluation
↓
Risk-reducing Action
↓
Execution / Reconciliation
↓
Updated Position / Protection
~~~

重要:

~~~text
Fast path can reduce risk
without waiting for R2 Research.

Fast path cannot create new Knowledge
or loosen Risk permission.
~~~

---

# 17.39 R4 AI / Rule Boundary

Python / Rule候補:

~~~text
Exposure calculation
Risk budget checks
Position sizing formula
Constraint enforcement
Drawdown checks
Leverage / margin checks
Order validation
Idempotency
Reconciliation
Position projection
Protection gap detection
Emergency deterministic guards
~~~

AI候補:

~~~text
Risk explanation
Scenario interpretation
Human-readable rationale
Unusual conflict review
Operational diagnostic assistance
~~~

重要:

~~~text
AI says safe
≠ Risk Permission

AI says exit
≠ Execution authority

AI unavailable
≠ Protection unavailable
~~~

Hard safetyはAI依存を避ける方向。

---

# 17.40 R4 Candidate Flow

~~~text
R3 Economic Opportunity
        ↓
Capital / Portfolio Context
        ↓
Risk Budget / Constraint / RiskState
        ↓
Capital Permission
        ↓
Position Sizing
        ↓
Execution Admission
        ↓
Execution Intent
        ↓
Reservation / Venue Routing
        ↓
Execution Attempt / Events
        ↓
Reconciliation
        ↓
Execution Record
        ↓
Logical Position / Exposure
        ↓
Protection Requirement / State
        ↓
Runtime Protection / Exit
        ↓
Position Closed / Finalized
        ↓
Production Outcome Boundary
        ↓
R5 Learning / Feedback
~~~

Parallel Fast Safety:

~~~text
R1 Runtime Context
+
R3 Assumption Monitoring
+
R4 Exposure / Protection
+
X10 System Health
        ↓
Emergency Fast Path
        ↓
risk-reducing action only
        ↓
Execution / Reconciliation
        ↓
Updated Position / Protection
~~~

---

# 17.41 R4 Concept Classification

| Concept | Phase 5 R4 Candidate |
|---|---|
| Economic Opportunity → Risk boundary | KEEP / STRENGTHEN |
| Capital Permission | NEW / KEEP |
| Capital / Portfolio Context | NEW / STRENGTHEN |
| Risk Budget | NEW / KEEP |
| Position Sizing | NEW / STRENGTHEN |
| Drawdown / Ruin context | NEW / STRENGTHEN |
| Correlation / Concentration | NEW |
| Runtime Authorized Constraint | NEW / STRENGTHEN |
| RiskState | KEEP / REDESIGN |
| RiskState single-writer | KEEP principle |
| Defense Layer | SPLIT / DROP monolith |
| Emergency Fast Path | KEEP / STRENGTHEN |
| Fast Path risk-increase | DROP |
| Recovery Strict Path | KEEP / REDESIGN |
| Execution Admission | KEEP / REDESIGN |
| Decision Staleness check | NEW |
| Execution Intent | KEEP / REDESIGN |
| Reservation / Idempotency | KEEP / STRENGTHEN |
| Venue Routing | KEEP / REDESIGN |
| Execution Attempt / Event | KEEP |
| Reconciliation | KEEP / STRENGTHEN |
| Execution Record | KEEP / REDESIGN |
| Logical Position | KEEP / STRENGTHEN |
| Position Event | KEEP |
| Current Position Projection | KEEP as derived view |
| Protection Requirement | NEW / resolve legacy gap |
| Runtime Protection | KEEP / STRENGTHEN |
| Exit Decision | KEEP / REDESIGN |
| Protection Order Intent | KEEP / REDESIGN |
| Protection State | KEEP / STRENGTHEN |
| Adapter as canonical truth | DROP |
| API success = execution success | DROP |
| TradeResult as whole outcome | DROP / REDESIGN |
| Production Outcome Boundary | NEW |
| AI as risk authority | DROP |

---

# 17.42 R4 Open Questions for Later Design

~~~text
1. Capital hierarchy / account model
2. Risk Budget hierarchy
3. Position sizing method
4. Portfolio correlation / common-factor model
5. Drawdown / ruin thresholds
6. Tail-risk representation
7. RiskState exact state machine
8. RiskState transition authority
9. Runtime Authorized Constraint approval / writer
10. Emergency Fast Path exact allowed actions
11. Hedge authority and limits
12. Recovery Gate
13. Execution Admission minimum contract
14. Decision staleness threshold
15. Venue routing policy
16. Idempotency / reservation protocol
17. Reconciliation canonical rules
18. Multi-venue logical position
19. Protection Requirement generation
20. Protection State canonical source
21. Unknown exposure policy
22. Exit taxonomy
23. Manual override / human emergency control
24. Production Outcome minimum contract
25. Paper / Demo / Live separation
26. Capital segregation across markets
27. Crypto spot vs leveraged derivatives risk differences
28. Market expansion execution contract
29. AI role in non-hard safety
30. Incident-to-position safety contract
~~~

---

# 17.43 Phase State

~~~text
Phase 5 R1
COMPLETE / WORKING CANDIDATE

Phase 5 R2
COMPLETE / WORKING CANDIDATE

Phase 5 R3
COMPLETE / WORKING CANDIDATE

Phase 5 R4
COMPLETE / WORKING CANDIDATE

NEXT:
R5 — Learning / Feedback
~~~

重要:

~~~text
R4 COMPLETE
≠
Final Capital / Production Architecture

Positive EV
≠
Capital Permission

Risk Permission
≠
Execution Success

Order Sent
≠
Position Exists

Emergency Fast Path
≠
Fast Alpha Path

Exit
≠
Knowledge Invalid
~~~


---

# 18. Checkpoint 011 — R3 Detailed Refinement / Knowledge Admission + Relationship

**Date:** 2026-09-30  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction — R3 Detailed Refinement  
**Purpose:** R3の大枠Checkpoint後に、Knowledge Lifecycle詳細設計へ入る前提として、Knowledge AdmissionとKnowledge Relationshipの意味境界を精密化する。

## 18.1 Knowledge Admission Refinement

Validated Research ResultをそのままKnowledgeへしない。

候補Flow:

~~~text
Validated Research Result
↓
Result Classification
↓
Knowledge Worthiness Gate
↓
Knowledge Type Classification
↓
Condition Extraction
↓
Boundary / Constraint Extraction
↓
Evidence / Uncertainty Link
↓
Existing Knowledge Comparison
↓
Duplicate / Conflict / Version Analysis
↓
Knowledge Candidate
↓
Admission Decision
~~~

重要:

~~~text
Validated Research Result
≠ Knowledge Candidate
≠ Knowledge Record
~~~

Knowledge化の中心問い:

> このResearch Resultは、別時点・別判断でも再利用可能な意味を持つか？

Process Failure等、Knowledge化してはいけないResultはR2再研究へ戻す。

Negative / Refuted / Boundary / Unknownも、再利用可能な意味を持つ場合はResearch Asset / Knowledge Candidateになり得る。

Knowledge Admission Decisionは、単純Approve / Rejectだけに限定しない候補。

概念候補:

~~~text
ADMIT
ADMIT_WITH_BOUNDARY
NEGATIVE
UNKNOWN
MERGE
SUPERSEDE_CANDIDATE
RESEARCH_REQUIRED
DEFER
REJECT
~~~

正式State名は後。

重要:

~~~text
Research Validity
≠ Knowledge Worthiness
~~~

SUPPORTEDでも再利用性・条件・重複等の理由でKnowledge化しない場合があり得る。

---

# 18.2 Knowledge Record Refinement Principle

Knowledge RecordはResearch Resultの要約文ではない。

保持すべき意味候補:

~~~text
Identity
Claim
Knowledge Type
Market / Asset / Instrument / Venue Scope
Conditions
Time Horizon
Observed / Expected Effect semantics
Failure Boundary
Constraint semantics
Evidence Trace
Research Trace
Uncertainty
Known Contradictions
Version
Lifecycle reference
Provenance
~~~

重要:

~~~text
Knowledge
=
Claim
+
Conditions
+
Failure / Boundary
+
Evidence Trace
+
Uncertainty
~~~

Knowledge RecordへEvidence全文・Research Trial全文を複製しない。
R2をSource of Truthとして参照する。

---

# 18.3 Knowledge Relationship Purpose

Knowledge Relationshipは、

> Knowledge Record同士の意味上の関係だけをCanonicalに保存する。

重要:

~~~text
Knowledge Record
≠ Knowledge Relationship
≠ Knowledge Graph
~~~

Relationship側へKnowledge本文・Evidence全文を複製しない。

---

# 18.4 Canonical Knowledge Relationship — Initial Minimal Set

初期Canonical Relation候補:

~~~text
EQUIVALENT
DUPLICATE_CANDIDATE
SPECIALIZES
REFINES
EXTENDS
CONTRADICTS
SUPERSEDES
~~~

逆Relationは保存せずQuery時生成を検討。

例:

~~~text
SPECIALIZES
↔ GENERALIZES
~~~

曖昧な、

~~~text
RELATED
SIMILAR
ASSOCIATED
~~~

はCanonical Relationへ入れない方向。

これらはKnowledge Graph / Search / Derived View側で扱う。

---

# 18.5 Relation Meaning

## EQUIVALENT

意味・Scope・条件・Horizon等が実質同じ。

## DUPLICATE_CANDIDATE

重複疑い。
自動Merge / 自動削除を意味しない。

## SPECIALIZES

一方のKnowledgeが、もう一方より狭い条件領域を扱う。

## REFINES

Lag / Boundary / Effect / Participant / Condition等を、元Knowledgeより精密化する。

## EXTENDS

元Knowledgeを否定せず、別Market / Asset / Regime等へ適用範囲を拡張する。

## CONTRADICTS

同じ意味領域・同じ条件領域・同じ対象・同じRelevant Horizonで、両立不能なClaim。

## SUPERSEDES

別Knowledgeが旧Knowledgeを正式に置換する関係。
新しいという理由だけで自動付与しない。

---

# 18.6 Contradiction vs Condition Difference

矛盾判定前にApplicability Domainを比較する。

比較順候補:

~~~text
1. Market Scope
2. Asset / Instrument
3. Venue
4. Regime
5. Conditions
6. Time Horizon
7. Failure / Boundary
8. Claim / Effect semantics
~~~

Scope overlap候補:

~~~text
NO_OVERLAP
NESTED
PARTIAL_OVERLAP
SAME_SCOPE
~~~

重要:

~~~text
Claim A differs from Claim B
≠
CONTRADICTION
~~~

Contradiction候補条件:

~~~text
Scope overlap exists
AND
Condition overlap exists
AND
Same target / effect semantics
AND
Same relevant horizon
AND
Claims cannot simultaneously be true
~~~

例:

~~~text
1h bullish
+
24h bearish
~~~

は通常Contradictionではない。

~~~text
Thin Liquidity
vs
Deep Liquidity
~~~

で結論が違う場合も、まずCondition Differenceとして扱う。

同一条件領域で、

~~~text
Downside Risk ↑
vs
Downside Risk ↓
~~~

ならCONTRADICTS候補。

---

# 18.7 Relationship Candidate vs Canonical Relationship

AI / Python / similarity search等はRelationship Candidateを生成できる。

しかし:

~~~text
Detected Relationship
≠ Canonical Relationship
~~~

候補Flow:

~~~text
AI / Python / Search
↓
Relationship Candidate
↓
Scope Comparison
↓
Condition / Horizon / Claim Comparison
↓
Validation
↓
Canonical Knowledge Relationship
~~~

Embedding similarity等から直接CONTRADICTSを確定しない。

---

# 18.8 Knowledge Relationship Record — Minimal Meaning

候補:

~~~text
relationship_id

source_knowledge_id
target_knowledge_id

relationship_type
scope_overlap
relationship_basis
comparison_version

status

created_at
updated_at

provenance
~~~

Relationship Basisは、

> なぜこのRelationなのか

を短く説明できる意味を持つ。

Evidence全文はコピーしない。

---

# 18.9 Knowledge Graph Boundary

Knowledge GraphはCanonical Knowledge StoreではなくDerived View候補。

~~~text
Knowledge Record
+
Knowledge Relationship
↓
Graph Projection
↓
Knowledge Graph
~~~

Graphは消しても再生成可能にする方向。

Knowledge Graph側ではDerived Edgeを持てる。

例:

~~~text
SIMILAR_TO
NEAR_IN_EMBEDDING
SHARES_CONDITION
SAME_MARKET
SAME_RESEARCH_DOMAIN
COMMON_EVIDENCE_SOURCE
~~~

ただし:

~~~text
Derived Graph Edge
≠ Canonical Knowledge Relationship
~~~

---

# 18.10 Version Lineage vs Knowledge Relationship

同じKnowledge Identity内の、

~~~text
K021 v1
→
K021 v2
~~~

はVersion Lineageで管理する候補。

別Knowledge K044がK021を置換する場合に、

~~~text
K044 SUPERSEDES K021
~~~

を使える。

重要:

~~~text
Version Lineage
≠ Knowledge Relationship
~~~

---

# 18.11 Relationship Responsibility Boundary

Knowledge Relationshipは以下を行わない。

~~~text
Evidenceを保存しない
Knowledge本文を複製しない
Applicabilityを決定しない
Trade方向を決めない
Riskを決めない
Lifecycleを自動変更しない
Conflictを自動解決しない
Knowledgeを削除しない
~~~

Relationshipの責任は、

> このKnowledge同士が意味上どのような関係にあるかをCanonicalに表現すること。

まで。

---

# 18.12 Conflict Feedback

Canonical CONTRADICTSが確認された場合:

~~~text
Knowledge A
+
Knowledge B
↓
CONTRADICTS
↓
Conflict / Research Question
↓
R2 Research
↓
Validated Research Result
↓
Knowledge Admission
~~~

Knowledge Relationship自体がConflictを解決しない。

---

# 18.13 Current Detailed State

~~~text
Knowledge Admission
= detailed refinement saved

Knowledge Record minimum semantics
= detailed refinement saved

Knowledge Relationship
= detailed refinement saved

Knowledge Graph boundary
= detailed refinement saved

NEXT:
Knowledge Lifecycle detailed design
- minimal states
- transition triggers
- assessment vs transition authority
- writer / governance authority
- version vs lifecycle
~~~

重要:

~~~text
Detailed Refinement
≠ Final Object Schema
≠ DB Table
≠ Python Class
≠ Formal Current Architecture Adoption
~~~


---

# 19. Checkpoint 012 — R3 Detailed Refinement / Knowledge Lifecycle

**Date:** 2026-10-01  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction — R3 Detailed Refinement  
**Purpose:** Knowledge Admission / Record / Relationshipの詳細化後、Knowledge Versionが時間・新Evidence・矛盾・再検証・Integrity変化を受けながら、どのように維持・一時停止・退役されるかをPrecision Design → Precision Review → Authority Design → Human Viewの順で精密化する。

## 19.1 Knowledge Lifecycle Responsibility

Knowledge Lifecycleの責任候補:

> Admission済みKnowledge Versionが、現在も維持対象として扱えるか、一時的に通常利用を止めるべきか、Current Operational Knowledgeとしての通常利用を終了すべきかを、時間・新Evidence・矛盾・再検証・Integrity変化を追跡しながら管理する。

重要:

~~~text
Knowledge Lifecycle
≠ Researchそのもの

Knowledge Lifecycle
≠ Applicability

Knowledge Lifecycle
≠ Version Lineage

Knowledge Lifecycle
≠ Knowledge Relationship

Knowledge Lifecycle
≠ Runtime Position Action
~~~

真偽・再現性・成立条件・限界の研究はR2 Researchの責任。
Lifecycleは、そのResearch / Evidence / Integrity情報を受けてKnowledge Versionを現在どう扱うかを管理する。

---

## 19.2 Lifecycle Unit

Canonical Lifecycle Stateは原則としてKnowledge Identity全体ではなく、Knowledge Version単位で持つ候補。

例:

~~~text
K021
├─ v1 RETIRED
├─ v2 RETIRED
└─ v3 ACTIVE
~~~

重要:

~~~text
Lifecycle State
→ Knowledge Version

Knowledge Identity全体のCurrent Status
→ Version Lineage等から作るDerived View候補
~~~

同一Knowledge IdentityでどのVersionをCurrent Semantic Versionとして扱うかはVersion Lineage側の責任候補であり、Lifecycleだけで複数Version競合を解決しない。

---

## 19.3 Lifecycle Stateを一軸へ詰め込まない

以前候補にあった、

~~~text
ACTIVE
AGING
UNDER_REVIEW
DEGRADED
RETIRED
~~~

を一つのLifecycle State Machineへ入れない方向。

理由:

~~~text
AGING
= Recency / Review Need

UNDER_REVIEW
= Review進行状態

DEGRADED
= Assessment Finding

ACTIVE / SUSPENDED / RETIRED
= Canonical Operational Treatment
~~~

異なる意味軸を一つのEnumへ詰めるとState Explosionと責任混同が起きる。

---

## 19.4 Lifecycle Disposition — Minimal Canonical Set

Precision Review後の本命候補:

~~~text
ACTIVE
SUSPENDED
RETIRED
~~~

### ACTIVE

Current Knowledge Assetとして維持され、通常のApplicability評価対象になれる。

重要:

~~~text
ACTIVE
≠ Currently Applicable
≠ Positive Knowledge
≠ Trade Permission
~~~

Negative Knowledge / Constraint Knowledge等もACTIVEになり得る。

### SUSPENDED

Knowledgeは保存されているが、重大な未解決問題があり、通常のApplicability経路へ流すことを一時停止する。

重要:

~~~text
SUSPENDED
≠ Refuted
≠ Retired
≠ Deleted
~~~

再研究・Integrity確認後にACTIVEへ戻れる可逆的Safety State。

### RETIRED

Current Operational Knowledgeとしての通常利用を終了した状態。

重要:

~~~text
RETIRED
≠ DELETE
~~~

Research Asset / Historyとして保持する。
過去Decision・Trade・ResearchでどのKnowledge Versionが使われたかを後から追跡可能にする。

---

## 19.5 Review Status — Separate Axis

Lifecycle Dispositionとは別にReview状態を持つ候補。

~~~text
NO_REVIEW_DUE
REVIEW_DUE
IN_REVIEW
~~~

CURRENT という名称は、

~~~text
Current Knowledge
Current Version
Current Market
~~~

等と意味衝突しやすいため、Precision Reviewで NO_REVIEW_DUE へ変更候補。

重要:

~~~text
Review Status
≠ Lifecycle Disposition

REVIEW_DUE
≠ Automatic Suspension

Review Status
≠ Production Blocking Authority
~~~

重大性が高く通常利用を止める必要がある場合は、Lifecycle Assessmentを通してSUSPENDEDへ変更する。

---

## 19.6 Assessment Finding — Stateではない

以下はLifecycle StateではなくAssessment Finding / Trigger Contextとして扱う候補。

~~~text
Aging / Recency
Evidence Degradation
Contradiction
Structural Change
Integrity Problem
Production Mismatch
Repeated Applicability Mismatch
Validation Age
Replication Failure
OOS Deterioration
~~~

重要:

~~~text
Degradation
≠ Lifecycle State

Aging
≠ Lifecycle State

Finding
≠ Transition
~~~

---

## 19.7 Lifecycle Trigger

Trigger候補Source:

~~~text
Time / Recency
New Evidence
Replication Failure
OOS / Forward deterioration
Market Structure Change
New Failure Boundary
New Constraint
Canonical CONTRADICTS
SUPERSEDES candidate / relation
Repeated Applicability Mismatch
Production Feedback
Integrity Failure
Human concern
AI suggestion
~~~

重要:

~~~text
Trigger
=
「調べる理由が発生した」

Trigger
≠ Transition
≠ Evidence Strength
≠ Majority Vote
~~~

Trigger数が多いことをTransition根拠の多数決にしない。

---

## 19.8 Lifecycle Assessment

Triggerを受けた後、R3内部のLifecycle Assessmentが、

~~~text
対象Knowledge Version
Trigger Type
Materiality
Evidence / Research References
Known Contradictions
Integrity Status
Structural Change
Applicabilityだけの問題か
Productionだけの問題か
Revalidation Required?
Immediate Suspension Required?
Potential Impact
Unresolved Questions
Transition Recommendation
~~~

等の意味を評価する候補。

具体Field / Object Schemaは後。

重要:

~~~text
Lifecycle Assessment
≠ Research Truth Authority

Lifecycle Assessment
≠ Canonical Transition
~~~

Claimの真偽・再現性・条件・限界を研究するのはR2。

---

## 19.9 Revalidation Boundary

Lifecycleが再検証必要と判断しても、自身でResearchを実行しない。

~~~text
Lifecycle Trigger
↓
Lifecycle Assessment
↓
Revalidation Required
↓
R2 Research Candidate / Research Intake
↓
Replication / OOS / Forward / Stress等
↓
Validated Research Result
↓
R3 Lifecycle / Admission
~~~

再検証結果候補:

~~~text
SUPPORTED / meaning unchanged
→ ACTIVE維持
→ Review Status = NO_REVIEW_DUE
→ Validation History追加

SUPPORTED / semantics changed
→ New Knowledge Version Candidate
→ Knowledge Admission

REFUTED / no longer reusable
→ RETIRED candidate

INCONCLUSIVE
→ ACTIVE + REVIEW_DUE
or
→ SUSPENDED + IN_REVIEW

PROCESS LIMITED / RESEARCH FAILURE
→ Knowledge Falseとは扱わずResearch修復へ
~~~

---

## 19.10 Version vs Lifecycle Boundary

~~~text
Lifecycle
=
そのKnowledge Versionを現在どう扱うか

Version
=
Knowledgeの意味がどう変わったか
~~~

例:

~~~text
K021 v3
ACTIVE → SUSPENDED → ACTIVE
~~~

はSemantic Version変更なしでも可能。

一方、

~~~text
Claim変更
Conditions変更
Failure Boundary変更
Horizon変更
Scope変更
~~~

等、Knowledgeの意味が変わる場合は新Version候補。

重要:

~~~text
Lifecycle Transition
≠ Semantic Version Change

Semantic Version Change
≠ Lifecycle Transition
~~~

---

## 19.11 Relationship vs Lifecycle Boundary

Canonical Relationship自身はLifecycleを書き換えない。

~~~text
EQUIVALENT
→ direct lifecycle effectなし

DUPLICATE_CANDIDATE
→ direct lifecycle effectなし

SPECIALIZES
→ direct lifecycle effectなし

REFINES
→ direct lifecycle effectなし

EXTENDS
→ direct lifecycle effectなし

CONTRADICTS
→ Assessment / Revalidation Trigger候補

SUPERSEDES
→ Retirement Assessmentへの強いInput候補
~~~

重要:

~~~text
CONTRADICTS
≠ RETIRED

SUPERSEDES
≠ Lifecycle Writer
~~~

---

## 19.12 Applicability vs Lifecycle Boundary

~~~text
Lifecycle
=
Knowledge Version自体をCurrent Knowledgeとしてどう扱うか

Applicability
=
そのACTIVE Knowledgeを今のCurrent Marketで使えるか
~~~

基本候補:

~~~text
ACTIVE
→ Applicability評価対象になれる

SUSPENDED
→ Normal Applicabilityから除外

RETIRED
→ Normal Applicabilityから除外
~~~

重要:

~~~text
ACTIVE
≠ APPLICABLE

NOT_APPLICABLE
≠ SUSPENDED
≠ RETIRED
~~~

Repeated NOT_APPLICABLEは研究Trigger候補にはなり得るが、直接Lifecycle Transitionしない。

---

## 19.13 Runtime Observation Boundary

~~~text
Runtime Observation
Runtime Assumption Deviation
Trade Loss
Unexpected Outcome
~~~

からKnowledge Lifecycleへ直接State変更しない。

候補Flow:

~~~text
Runtime Observation / Outcome
↓
R4 Runtime Protection and/or R5 Feedback
↓
必要ならResearch Trigger
↓
R2 Research
↓
Lifecycle Assessment
~~~

重要:

~~~text
One Loss
≠ Knowledge Invalid

Repeated Loss
≠ Automatic Retirement

Runtime Assumption Deviation
≠ Lifecycle Transition

Lifecycle Change
≠ Position Action
~~~

Position保有中にKnowledgeがSUSPENDEDになった場合も、R3がEXITを命令しない。
Lifecycle State Changed EventをR4へ渡し、R4がHOLD / REDUCE / PROTECT / EXIT等を判断する。

---

## 19.14 Transition Matrix

初期候補:

| From | To | Candidate |
|---|---|---|
| ACTIVE | SUSPENDED | ALLOW |
| ACTIVE | RETIRED | ALLOW with strong basis |
| SUSPENDED | ACTIVE | ALLOW after issue resolution |
| SUSPENDED | RETIRED | ALLOW with strong basis |
| RETIRED | ACTIVE | NO DIRECT TRANSITION |
| RETIRED | SUSPENDED | NO |

RETIRED Knowledgeが後年再び成立しそうな場合:

~~~text
Retired Knowledge
↓
R2 Revalidation
↓
Knowledge Admission
↓
New Version / New Knowledge
↓
ACTIVE
~~~

とし、過去Versionを直接ACTIVEへ戻さない方向。

---

## 19.15 Precision Review / Destruction Test

以下のケースで3-state Disposition + separate Review Statusを破壊テストした。

~~~text
正常Knowledge
Canonical Contradiction
False Contradiction / Condition Difference
Market Structure Change
One Trade Loss
Repeated Loss
Revalidation Success
Semantic Change after Revalidation
Refutation
Revalidation Process Failure
Confirmed Leakage / Integrity Failure
SUPERSEDES
10-year Validation Age
Long-term NOT_APPLICABLE
Retired Knowledge becoming relevant again
Open Position during Suspension
Negative Knowledge
Constraint Knowledge
Multiple simultaneous Triggers
~~~

Result:

~~~text
ACTIVE / SUSPENDED / RETIRED
=
追加Canonical Stateなしで主要ケースを表現可能

AGING
→ Recency / Review情報

WEAK / DEGRADED
→ Evidence / Assessment Finding

UNDER_REVIEW
→ Review Status

SUPERSEDED
→ Relationship / Lineage

ARCHIVED
→ Storage / Retention

BLOCKED
→ LifecycleならSUSPENDED
  Current usabilityならApplicability
~~~

Stateを増やすより責任軸を分離する方が意味が安定する。

---

## 19.16 Precision Review Additional Invariants

~~~text
L-01 Knowledge CandidateにはLifecycle Stateを持たせない。
L-02 Canonical Lifecycle StateはKnowledge Version単位。
L-03 ACTIVE ≠ Currently Applicable。
L-04 NOT_APPLICABLE ≠ Knowledge Invalid。
L-05 Trigger ≠ Transition。
L-06 Assessment ≠ Transition。
L-07 R2 Research Result ≠ Lifecycle Writer。
L-08 AI / Python / Relationship / Runtime Observation ≠ Lifecycle Writer。
L-09 Lifecycle Transition ≠ Version Change。
L-10 Semantic ChangeはNew Version Candidate。
L-11 RETIREDから直接ACTIVEへ戻さない。
L-12 SUSPENDEDは可逆的Safety State。
L-13 RETIRED ≠ DELETE。
L-14 Past Lifecycle StateをLater Evidenceで書き換えない。
L-15 Lifecycle Change ≠ Position Action。
L-16 Review Status ≠ Lifecycle Disposition。
L-17 REVIEW_DUE ≠ Automatic Suspension。
L-18 Review StatusはProduction Blocking Authorityを持たない。
L-19 同一Knowledge IdentityのCurrent Semantic Version管理はVersion Lineage側の責任候補。
~~~

---

## 19.17 Lifecycle Transition Authority — Four Responsibility Split

Authorityは以下を分離する候補。

~~~text
1. Trigger Authority
2. Assessment Authority
3. Transition Decision Authority
4. Canonical Write Authority
~~~

重要:

~~~text
Triggerできる
≠ Assessmentできる

Assessmentできる
≠ Transitionを決定できる

Transitionを決定できる
≠ 直接Canonical Storeを書き換えてよい
~~~

---

## 19.18 Trigger Authority

Trigger発生源は広く許容できる。

候補:

~~~text
R1 Current Market Understanding
R2 Research
Knowledge Relationship
Applicability
R4 Production
R5 Feedback
Time / Scheduler
Integrity / Monitoring
AI
Human
~~~

ただし、AIはTrigger Candidate / Advisoryとして扱う。

~~~text
AI Suggestion
≠ Canonical Trigger Truth
≠ Transition Authority
~~~

---

## 19.19 Assessment Authority

R3内部のKnowledge Lifecycle AssessmentをLogical Responsibilityとして置く候補。

内部で利用可能:

~~~text
Python / Rule
→ Age / Trace / Version / Hard Integrity / deterministic checks

AI
→ contradiction explanation / context organization / alternative explanation / review assistance

R2
→ Validated Research Result / Evidence input
~~~

Assessment結果はAI OutputそのものではなくLifecycle Assessmentとして扱う。

---

## 19.20 Transition Proposal

AssessmentからCanonical Stateへ直接書かない。

~~~text
Lifecycle Assessment
↓
Transition Proposal
~~~

Transition Proposalは、

~~~text
Target Knowledge Version
Current Disposition
Recommended Disposition
Reason
Evidence / Research References
Revalidation Requirement
Materiality
~~~

等の意味を持てる候補。

重要:

~~~text
Transition Proposal
≠ Transition Decision
~~~

---

## 19.21 Transition Decision Authority

Logical Responsibility候補:

~~~text
Knowledge Lifecycle Governance
~~~

責任:

> Lifecycle Assessment、Validated Research Result、Knowledge Relationship、Version Lineage、Integrity Context、Governance Policy、必要ならAuthorized Human Overrideを基に、Lifecycle Transitionを承認・拒否・保留する。

Decision候補:

~~~text
APPROVE
REJECT
DEFER
REQUIRE_RESEARCH
REQUIRE_MORE_EVIDENCE
~~~

正式Enumは後。

---

## 19.22 Canonical Write Authority — Single Writer

Canonical Lifecycle StateはSingle Writerだけが更新する候補。

Logical Responsibility候補:

~~~text
Knowledge Lifecycle Writer
~~~

責任:

> Authorized Lifecycle DecisionだけをCanonical Lifecycle Stateへ反映し、Lifecycle Eventを残す。

以下は直接Writerにならない。

~~~text
AI
R1
R2
Knowledge Relationship
Applicability
R4
R5
Monitoring
Human UI
~~~

Human Overrideも直接DB Updateではなく、

~~~text
Human Authorized Override
↓
Lifecycle Governance
↓
Authorized Decision
↓
Single Writer
~~~

を通す方向。

---

## 19.23 Governance vs Writer Boundary

~~~text
Lifecycle Governance
=
何に変えるべきか判断

Lifecycle Writer
=
承認されたDecisionを正確にCanonical Stateへ反映
~~~

Semantic Responsibilityとして分ける。

実装上は同一Service内でもよい。

重要:

~~~text
Separate Responsibility
≠ Separate Process
≠ Separate Server
~~~

HOWは後。

---

## 19.24 Hard Integrity Fast Path

Confirmed Look-Ahead Leakage、Evidence Corruption、Wrong Dataset、Knowledge Identity Corruption、Broken Provenance等のHard Integrity Failureでは、通常の長い再研究完了を待たずSuspensionまで進めるFast Path候補。

~~~text
Verified Hard Integrity Failure
↓
Fast Lifecycle Assessment
↓
Pre-authorized Suspension Policy
↓
Lifecycle Governance
↓
Single Writer
↓
SUSPENDED
~~~

重要:

~~~text
Fast Safety Authority
→ SUSPENDまで

Fast Safety Authority
≠ RETIRE Authority

Immediate Suspension
≠ Immediate Retirement
~~~

原則:

> 止める判断は速く、捨てる判断は慎重に。

---

## 19.25 Transition Evidence Asymmetry

Transitionごとに必要Evidence強度を同じにしない候補。

~~~text
ACTIVE → SUSPENDED
= comparatively lower threshold
  reversible safety action

SUSPENDED → ACTIVE
= medium / high
  issue resolution evidence required

ACTIVE / SUSPENDED → RETIRED
= high
  long-term operational retirement decision

RETIRED → New Active Version
= R2 Research + Admission required
~~~

exact thresholdは後。

---

## 19.26 Lifecycle Event / Temporal Integrity

Canonical Stateだけを上書きして履歴を失わない。

Lifecycle Transition時に最低限、

~~~text
Knowledge Version
Previous State
New State
Trigger Reference
Assessment Reference
Research Result Reference
Decision Reason
Authority
Decision Time
Effective Time
Provenance
~~~

を後から追えるLifecycle Eventを持つ必要がある。

具体Schemaは後。

Temporal Integrity:

~~~text
2027:
Knowledge was ACTIVE

2030:
New evidence caused RETIRE decision
~~~

を両方保持する。

重要:

~~~text
Later Knowledge
≠ Information Available At Past Decision Time

Later Lifecycle Decision
≠ Rewrite Past Lifecycle State
~~~

---

## 19.27 Stale Decision Protection

Canonical Writerは判断主体ではないが、壊れたWriteを防ぐIntegrity Gateを持つ候補。

最低確認候補:

~~~text
Authorized Transition Decision exists
Expected Previous State matches
Target transition is legal
Knowledge Version exists
Decision not stale
Provenance / time valid
Duplicate writeではない
~~~

例:

~~~text
Assessment時:
ACTIVE

別Transition後:
SUSPENDED

古いDecision:
ACTIVE → RETIRED

↓
Expected Previous State mismatch
↓
WRITE REJECTED
↓
Re-assessment
~~~

---

## 19.28 Authority Matrix

| Domain | Trigger | Assessment | Transition Decision | Canonical Write |
|---|---:|---:|---:|---:|
| R1 Market Understanding | YES | NO | NO | NO |
| R2 Research | YES | Evidence only | NO | NO |
| Knowledge Relationship | YES | Relation meaning only | NO | NO |
| Applicability | YES | Current usability only | NO | NO |
| R4 Production | YES | Runtime safety only | NO | NO |
| R5 Feedback | YES | Outcome finding only | NO | NO |
| Monitoring / Integrity | YES | Integrity signal | NO | NO |
| AI | Candidate | Advisory | NO | NO |
| Human | YES | Review possible | Authorized Override possible | NO direct write |
| Lifecycle Assessment | — | YES | Proposal only | NO |
| Lifecycle Governance | — | Review | YES | NO |
| Lifecycle Writer | — | NO | NO | YES |

---

## 19.29 Authority Invariants

~~~text
A-01 Trigger Authority ≠ Transition Authority。
A-02 Trigger SourceはCanonical Lifecycle Stateを書けない。
A-03 AIはTrigger Candidate / Assessment Advisoryまで。
A-04 R2はValidated Research Resultを提供するがLifecycle Writerではない。
A-05 Knowledge RelationshipはLifecycle Triggerを発生させ得るがWriterではない。
A-06 ApplicabilityはCurrent usabilityを評価するがLifecycle Writerではない。
A-07 R4 / R5 OutcomeはTriggerになり得るがKnowledge Stateを直接変更しない。
A-08 Lifecycle AssessmentはTransition Proposalまで。
A-09 Lifecycle GovernanceだけがTransition Decisionを承認できる候補。
A-10 Canonical Lifecycle StateはSingle Writerだけが更新する。
A-11 Human OverrideもSingle Writer経由で記録する。
A-12 Hard Integrity Fast PathはSUSPENDまで。
A-13 Fast RETIREは禁止。
A-14 WriterはExpected Previous Stateを確認する。
A-15 State変更はLifecycle EventとしてTraceを残す。
~~~

---

## 19.30 Human View

人間向け中心Flow:

~~~text
Research
↓
Validated Research Result
↓
Knowledge Admission
↓
Knowledge誕生
↓
ACTIVE
↓
普段はApplicabilityで「今使えるか」を別確認
↓
時間経過 / 矛盾 / Loss / 市場変化 / 新Evidence / Integrity問題
↓
「このKnowledgeは怪しくないか？」
↓
Lifecycle Assessment
↓
軽い問題
→ ACTIVE + REVIEW_DUE

重大な未解決問題
→ SUSPENDED + IN_REVIEW
↓
必要ならR2で再研究
↓
問題なし
→ ACTIVE

意味が変わった
→ New Version Candidate
→ Knowledge Admission

現在のKnowledgeとして維持不能
→ RETIRED
→ ただしHistory / Research Assetとして保存
~~~

Human Viewで覚える重要定義:

~~~text
ACTIVE
=
Knowledge自体は現在も維持

SUSPENDED
=
問題が未解決なので通常利用を一時停止

RETIRED
=
Current Operational Knowledgeとして通常利用終了
ただし削除しない

Lifecycle
=
Knowledge自体を現在どう扱うか

Applicability
=
そのKnowledgeを今の市場で使えるか

Version
=
Knowledgeの意味がどう変わったか
~~~

---

## 19.31 Human Review Result

2026-10-01のConversationでHuman Viewを確認。

Result:

~~~text
No major conceptual issue found by Daisuke.
Proceed with this direction as Working Candidate.
~~~

重要:

~~~text
Human Review completed
≠ Formal Current Architecture Adoption
~~~

---

## 19.32 Checkpoint Result

~~~text
Knowledge Lifecycle Precision Design
= COMPLETE / WORKING CANDIDATE

Precision Review / Destruction Test
= COMPLETE

Lifecycle Transition Authority
= COMPLETE / WORKING CANDIDATE

Human View
= COMPLETE / REVIEWED IN CONVERSATION

Formal Current Architecture
= UNCHANGED
~~~

Current R3 detailed refinement state:

~~~text
Knowledge Admission
= detailed refinement saved

Knowledge Record minimum semantics
= detailed refinement saved

Knowledge Relationship
= detailed refinement saved

Knowledge Graph boundary
= detailed refinement saved

Version Lineage boundary
= detailed refinement saved

Knowledge Lifecycle
= detailed refinement saved
~~~

NEXT candidate:

~~~text
Knowledge Applicability detailed refinement
- pre-decision Applicability responsibility
- Runtime Assumption Monitoring boundary
- Applicability State semantics
- Knowledge Condition matching
- Constraint / Failure Boundary interaction
- Multi-Knowledge applicability context
- Lifecycle ↔ Applicability handoff
~~~

重要:

~~~text
Checkpoint 012
≠ Final Object Schema
≠ DB Table
≠ Python Class
≠ Formal Current Architecture Adoption
~~~


---

# 20. Checkpoint 013 — R3 Detailed Refinement / Knowledge Applicability

**Date:** 2026-10-01  
**State:** SAVED  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction — R3 Detailed Refinement  
**Purpose:** Knowledge Lifecycleの次段として、ACTIVE Knowledge VersionをCurrent Marketへ適用する責任、Runtime Assumption Monitoringとの境界、Applicabilityの状態分解、Condition Matching、Failure Boundary / Constraint、Multi-Knowledge Context、LifecycleとのHandoffをPrecision Design → Precision Review → Human Viewの順で精密化する。

## 20.1 Knowledge Applicability Responsibility

Pre-Decision Knowledge Applicabilityの責任候補:

> ACTIVEなKnowledge Versionの成立条件・Scope・Time Horizon・Failure Boundary等をCurrent Market Contextと照合し、Knowledge自体の真偽やTrade方向を決めることなく、そのKnowledgeを現在のDecision Material候補として利用可能か評価し、その根拠と不確実性を追跡可能にする。

重要:

~~~text
Knowledge Valid
≠ Applicable Now

Applicable Now
≠ Allowed To Use

Allowed To Use
≠ Decision

Decision
≠ Positive Economic Value

Positive Economic Value
≠ Capital Permission
~~~

ApplicabilityはResearch Truth Authorityではない。
Claimの真偽・再現性・成立条件・限界の研究はR2の責任。

---

## 20.2 Lifecycle Eligibility Boundary

Normal Applicability Evaluationの前にLifecycle Eligibilityを確認する。

~~~text
ACTIVE
→ Applicability評価資格あり

SUSPENDED
→ Normal Applicabilityから除外

RETIRED
→ Normal Applicabilityから除外
~~~

重要:

~~~text
ACTIVE
≠ APPLICABLE

SUSPENDED / RETIRED
≠ NOT_APPLICABLE

Lifecycle Ineligible
≠ Market Not Applicable
~~~

Review Statusは別軸。

~~~text
REVIEW_DUE
≠ Automatic Applicability Block

IN_REVIEW
≠ Automatic Applicability Block

Review Status
≠ Production Blocking Authority
~~~

重大問題で通常利用を止める場合はLifecycle SUSPENDED、または後述のAuthorized Knowledge-Use Constraintを使う。

---

## 20.3 Applicability Stateを一軸へ詰め込まない

旧候補:

~~~text
APPLICABLE
PARTIALLY_APPLICABLE
NOT_APPLICABLE
UNCERTAIN
BLOCKED_BY_CONSTRAINT
NOT_EVALUATED
~~~

は異なる意味軸を混在させるため、そのまま単一Canonical Enumへ固定しない。

Precision Candidate:

~~~text
Lifecycle Eligibility
+
Evaluation Status
+
Scope Status
+
Condition Match
+
Failure Boundary Status
+
Uncertainty Context
+
Semantic Applicability
+
Knowledge-Use Constraint
+
Decision Material Eligibility
+
Outcome Reason / Trace
~~~

Semantic Applicabilityの最小候補:

~~~text
APPLICABLE
NOT_APPLICABLE
UNDETERMINED
~~~

正式Enum / Schemaは後。

重要:

~~~text
PARTIAL
≠ final Applicability Outcome

BLOCKED
≠ Condition Match

UNCERTAIN
≠ Condition Mismatch

NOT_EVALUATED
≠ NOT_APPLICABLE
~~~

---

## 20.4 Scope vs Condition

Knowledge Applicability Domainを、ScopeとConditionに分ける。

Scope候補:

~~~text
Market
Asset
Instrument
Venue
Time Horizon
必要に応じてSession / Participant Domain等
~~~

Scope mismatchはCondition failureではない。

~~~text
BTC Perpetual Knowledge
vs
ETH Spot Current Market
↓
OUT_OF_SCOPE
~~~

重要:

~~~text
Scope
≠ Condition
~~~

---

## 20.5 Knowledge Condition Semantics

Condition Role本命候補:

~~~text
REQUIRED
SUPPORTING
EXCLUSION
~~~

### REQUIRED

Knowledge成立のために満たされる必要がある条件。

### SUPPORTING

成立性を補強するが、欠けたことだけで自動NOT_APPLICABLEにしない条件。

### EXCLUSION

Research上、Knowledgeの適用対象から除外される条件。

重要:

~~~text
EXCLUSION
≠ Failure Boundary
≠ Knowledge-Use Constraint
~~~

各Conditionの基本評価候補:

~~~text
SATISFIED
NOT_SATISFIED
UNKNOWN
~~~

UNKNOWNをFALSEへ潰さない。

---

## 20.6 Condition Expression / Temporal Meaning

Knowledge Conditionはflat listに限定しない。

候補:

~~~text
ALL_OF
ANY_OF
explicit NOT
research-defined composite
~~~

必要に応じてCondition semanticsへ、

~~~text
Threshold
Range
Category
Relevant Time Window
Temporal Order
Lag
Duration
Persistence
~~~

を保持可能にする。

例:

~~~text
OI increase > 8% within 30m
THEN
Funding increase within 15m
~~~

を、

~~~text
OI high
AND
Funding high
~~~

へ意味変換しない。

重要:

~~~text
Condition Count Majority
≠ Applicability

Threshold
= Research / Knowledge Version由来

Applicability
≠ Threshold Creator
~~~

---

## 20.7 Unknown / Missing / Unconditional Boundary

Precision Reviewで以下を分離した。

~~~text
UNKNOWN
≠ NOT_SATISFIED
≠ PARTIAL
~~~

Unknown propagationはMateriality依存。

~~~text
Required Condition UNKNOWN
→ Semantic Applicability UNDETERMINED候補

Supporting Condition UNKNOWN
→ 必ずしも全体をUNDETERMINEDにしない

Hard Failure Boundary UNKNOWN
→ UNDETERMINED候補

Non-material Context UNKNOWN
→ Uncertaintyとして保持可能
~~~

さらに、

~~~text
NO_REQUIRED_CONDITION
≠
MISSING_CONDITION_DEFINITION
~~~

を区別する。

前者はResearchで条件不要と分かったKnowledge semantics。
後者はKnowledge Formation / Research不足。

---

## 20.8 Current Context Integrity

ApplicabilityはCurrent Market Understanding / Market DNA / Qualified Observation等を参照するが、自身でMarket Understandingを再生成しない。

~~~text
R1
= Current Marketを理解

R3 Applicability
= そのContextを使ってKnowledgeを照合
~~~

Condition Evaluationでは、

~~~text
Observed / Interpreted Value
+
Quality
+
Freshness
+
Time Alignment
↓
Condition Result
~~~

を考慮可能にする。

重要:

~~~text
latest available values
≠ time-consistent current context
~~~

Logical Boundary候補:

~~~text
Applicability Context Snapshot / As-Of Context
~~~

具体Object Schemaは後。

---

## 20.9 Failure Boundary

Failure Boundary責任候補:

> Knowledgeが成立する領域と、成立性が劣化・消失・逆転する領域とのResearchで確認されたValidity Limit。

重要:

~~~text
Failure Boundary
= Research-derived semantic asset

Failure Boundary
≠ Safety Policy

Applicability
= Boundary Evaluator

Applicability
≠ Boundary Creator
~~~

Status候補:

~~~text
CLEAR
APPROACHING
BREACHED
UNKNOWN
~~~

APPROACHINGでもSemantic ApplicabilityはAPPLICABLEであり得る。
BREACHEDならNOT_APPLICABLE候補。

Known Failure Boundaryを越えたこと自体はKnowledge Failureではない。

~~~text
Known Boundary Breach
≠ Knowledge Refuted
≠ Lifecycle RETIRED
~~~

---

## 20.10 Constraintを一種類へ潰さない

Constraintを少なくとも次へ分離する。

~~~text
A. Knowledge-Use Constraint
B. Production / Capital Constraint
~~~

### Knowledge-Use Constraint

Knowledge VersionはACTIVE / SemanticにAPPLICABLEでも、特定用途でDecision Materialとして使用させないAuthorized Restriction。

例:

~~~text
Evidence Provenance確認待ちのため
Live Decision使用禁止
~~~

### Production / Capital Constraint

Portfolio exposure、Margin、Daily Loss、RiskState、Venue availability等、R4がCapital Permissionを制御するConstraint。

重要:

~~~text
Knowledge Semantic Applicability
≠ Knowledge-Use Permission

Knowledge-Use Permission
≠ Capital Permission

Production Risk Constraint
≠ Knowledge Not Applicable
~~~

また、

~~~text
Constraint Knowledge
≠ Knowledge-Use Constraint
~~~

とする。

Constraint KnowledgeはResearchから得られたKnowledge Record。
Knowledge-Use Constraintは利用制限。

---

## 20.11 Decision Material Eligibility

Semantic ApplicabilityとKnowledge-Use Permissionを分離する。

例:

~~~text
Semantic Applicability:
APPLICABLE

Knowledge-Use Constraint:
ACTIVE

Decision Material Eligibility:
BLOCKED
~~~

Decision Material Eligibilityの候補:

~~~text
ELIGIBLE
BLOCKED
UNDETERMINED
~~~

正式Enumは後。

一時的ConstraintをKnowledge semantics変更の永久代用にしない。

~~~text
temporary operational restriction
→ Constraint

validated semantic discovery
→ Knowledge Condition / Boundary / New Version candidate
~~~

---

## 20.12 Pre-Decision Applicability Flow

Precision Candidate:

~~~text
Canonical Knowledge Version
        +
Canonical Lifecycle State
        ↓
Lifecycle Eligibility Gate
        ↓
Scope Gate
        ↓
Applicability Context Availability / Integrity
        ↓
Condition Matching
        ↓
Failure Boundary Check
        ↓
Semantic Applicability
        ↓
Knowledge-Use Constraint
        ↓
Decision Material Eligibility
        ↓
Cross-Knowledge Context
        ↓
Decision Material Snapshot
        ↓
Decision Synthesis
~~~

Applicability自身は、

~~~text
Trade direction
Expected Value
Position Size
Capital Permission
Execution
~~~

を決めない。

---

## 20.13 Runtime Assumption Monitoring Boundary

Pre-Decision ApplicabilityとRuntime Assumption MonitoringはCondition semanticsを共有できるが責任を分ける。

~~~text
Pre-Decision Applicability
=
このKnowledgeを今Decision材料として使えるか？

Runtime Assumption Monitoring
=
このKnowledge / Thesisを使って既に行った判断の前提は
今も維持されているか？
~~~

RuntimeではKnowledge Pool全件ではなく、実際のDecision / Thesisが依存したKnowledge Versionと重要Assumptionを監視する。

Logical Boundary候補:

~~~text
Runtime Assumption Set
~~~

意味候補:

~~~text
Used Knowledge Version references
Thesis reference
Material Required Conditions
Material Supporting Conditions
Failure Boundaries
Relevant Constraints
Expected Effect / Horizon
Critical Uncertainty
Decision-time Context Reference
~~~

重要:

~~~text
Applicable Knowledge Context Set
≠ Runtime Assumption Set

Entry Thesis
≠ Runtime hindsight rewrite
~~~

Position中に新KnowledgeがApplicableになった場合、Original Decisionを書き換えずNew Decision Event候補として扱う。

---

## 20.14 R3 Runtime Monitoring vs R4 Runtime Protection

核心:

~~~text
R3 Runtime Assumption Monitoring
=
前提がどう変わったか

R4 Runtime Protection
=
その変化に対して資金をどう守るか
~~~

R3出力候補:

~~~text
Required condition broken
Failure boundary approaching
Failure boundary crossed
Constraint activated
Assumption unknown
Horizon expired
Material deviation
~~~

R4はPosition / Exposure / Margin / Liquidity / RiskState / Protection / Portfolio Context等と統合し、

~~~text
CONTINUE
WATCH
REDUCE
HEDGE
TIGHTEN PROTECTION
EXIT
BLOCK ADDITION
EMERGENCY CLOSE
~~~

等を判断する候補。

重要:

~~~text
R3 MATERIAL_DEVIATION
≠ automatic EXIT

R4 EXIT
≠ Knowledge invalidated

Unknown before Entry
≠ Unknown while Exposed
~~~

正式Runtime State / Action Enumは後。

---

## 20.15 Multi-Knowledge Applicability Context

複数Knowledgeが同時にApplicableでも、多数決しない。

~~~text
Multiple Applicable Knowledge
≠ Independent Support

Knowledge Count
≠ Evidence Count

Different Knowledge ID
≠ Independent Research
~~~

Cross-Knowledge Context候補:

~~~text
Canonical Semantic Relationship
Scope / Horizon Overlap
Evidence Overlap
Research Lineage Dependency
Cause / Mechanism Dependency
Data / Feature Source Overlap
Contradiction Context
Unknown Dependency
~~~

Canonical Relationship:

~~~text
EQUIVALENT
DUPLICATE_CANDIDATE
SPECIALIZES
REFINES
EXTENDS
CONTRADICTS
SUPERSEDES
~~~

を参照できるが、Applicability自身がRelationshipを作成・変更・Conflict Winner決定しない。

~~~text
Canonical CONTRADICTS
≠ Applicabilityがwinnerを決める

No known overlap
≠ Proven independent

Confidence Sum
≠ Independent Support
~~~

Negative / Boundary / Constraint-related / Unknown Knowledgeも、現在RelevantならDecision Materialになり得る。

---

## 20.16 Relationship / Version Compatibility

Precision Reviewで、Relationshipを新Versionへ盲目的に継承しない必要を確認した。

例:

~~~text
K021 v2 CONTRADICTS K044 v1
↓
K021 v3でClaim変更
~~~

の場合、

~~~text
K021 v3 CONTRADICTS K044 v1
~~~

を自動的なCurrent Truthにしない。

Cross-Knowledge ContextはRelationshipのVersion Compatibilityを確認可能にする必要がある。

exact Version Lineage / Relationship granularityは後の詳細設計で確定。

---

## 20.17 Lifecycle ↔ Applicability Handoff

方向は非対称。

~~~text
Lifecycle
↓
Applicability Eligibility
~~~

は直接影響。

一方、

~~~text
Applicability Finding
↓
Lifecycle State
~~~

は直接禁止。

Applicability Findingは分類する。

~~~text
A. Expected Current-Market Mismatch
→ Trace only

B. Research / Semantic Concern
→ R2 Research Candidate

C. Lifecycle / Integrity Concern
→ Lifecycle Trigger Candidate
~~~

重要:

~~~text
NOT_APPLICABLE
≠ Lifecycle Trigger automatically

Known Boundary Breach
≠ Lifecycle Problem automatically

Applicability Finding
≠ Lifecycle Transition

Applicability
≠ Canonical Lifecycle Writer
~~~

Lifecycle TransitionはCheckpoint 012のGovernance / Single Writer Authorityを維持する。

---

## 20.18 Stale Applicability / Temporal Integrity

Applicability AssessmentはPermanent Current Truthではない。

Stale化候補:

~~~text
Time elapsed
Material Market Change
Regime change
Liquidity shock
Data quality degradation
Lifecycle change
Knowledge-Use Constraint change
Knowledge Version change
~~~

Assessment時に最低限、

~~~text
Knowledge Version reference
Lifecycle reference / revision
Current Context reference
Assessment Time / As-Of
~~~

を追える必要がある。

Lifecycleが、

~~~text
ACTIVE → SUSPENDED
~~~

となった場合、

~~~text
Past Applicability Assessment
→ Historyとして保持

Current-use eligibility
→ 無効
~~~

とする。

SUSPENDED → ACTIVEに戻っても、古いAPPLICABLE判定を自動復活させない。
Fresh Applicability Evaluationが必要。

Later Knowledge / Relationship / Lifecycle情報でPast Decision Contextを書き換えない。

---

## 20.19 Decision Material Snapshot

Decision Synthesisへ渡す時点のLogical Boundary候補:

~~~text
Decision Material Snapshot
~~~

意味候補:

~~~text
Knowledge Versions
Applicability Assessments
Lifecycle references
Knowledge-Use Constraint references
Current Context references
Cross-Knowledge Context
As-Of Time
~~~

目的:

> そのDecisionが、その時点で何を知り、何を使い、何を使えなかったのかを後から復元可能にする。

重要:

~~~text
Later Knowledge
≠ Information Available At Past Decision Time

Later Relationship
≠ Past Decision Context

Later Version
≠ Original Decision Reason
~~~

具体Schemaは後。

---

## 20.20 Emergency Knowledge-Use Block

Precision ReviewでHard Integrity FindingとLifecycle Writer不通が同時に起こるケースを確認した。

候補Flow:

~~~text
Verified Hard Integrity Finding
↓
Pre-authorized Emergency Knowledge-Use Block
↓
New Decision Materialから即時除外
↓
並行して
Lifecycle Fast Suspension Path
↓
Lifecycle Governance / Writer
↓
SUSPENDED
~~~

重要:

~~~text
Emergency Knowledge-Use Block
≠ Canonical Lifecycle State mutation

Fast Safety
≠ Fast RETIRE
~~~

これにより、Lifecycle Single Writer原則を壊さず、新しいDecisionへの利用を安全側へ止められる。

exact implementation / fail-open / fail-closed policyは後。

---

## 20.21 Precision Review / Destruction Test

以下を含むケースで破壊テストした。

~~~text
Normal applicable Knowledge
Scope mismatch
Required data missing
Supporting condition unknown
Explicit unconditional Knowledge
Old validation age
Fresh market data + old Knowledge validation
Lifecycle change during evaluation
SUSPENDED → ACTIVE
Knowledge-Use Constraint only
Constraint information unavailable
Hard Integrity + Lifecycle Writer unavailable
Known Failure Boundary breached
Repeated unexpected mismatch inside valid domain
AI disagrees with hard condition rule
Time-misaligned current context
Temporal composite condition
Multiple same-direction Knowledge from same Research
Opposing Knowledge with different lineage
Stale Relationship after new Knowledge Version
Relationship Store unavailable
Knowledge Graph unavailable
Negative Knowledge
Constraint Knowledge
Unknown Knowledge
RETIRED Knowledge matching current market
New Applicable Knowledge during open position
Supporting Knowledge suspended during open position
Market shock immediately after Applicability assessment
Decision starts before material context/lifecycle change
~~~

Result:

~~~text
Pre-Decision Applicability Responsibility
= SURVIVED

Runtime Assumption Monitoring Boundary
= SURVIVED

State decomposition
= SURVIVED / STRENGTHENED

Condition Matching
= SURVIVED / REFINED

Failure Boundary / Constraint split
= SURVIVED / STRENGTHENED

Multi-Knowledge Context
= SURVIVED

Lifecycle ↔ Applicability
= SURVIVED / STRENGTHENED
~~~

Reviewで追加・強化された主な候補:

~~~text
Unknown Materiality
Explicit Unconditional semantics
Validation Age responsibility separation
Evaluation consistency / stale guard
Emergency Knowledge-Use Block
As-Of Context integrity
Relationship Version Compatibility
Constraint Knowledge vs Knowledge-Use Constraint
Semantic Staleness
Decision Material Snapshot
~~~

---

## 20.22 Applicability Precision Invariants

~~~text
P-01 ACTIVE ≠ APPLICABLE。
P-02 SUSPENDED / RETIRED ≠ NOT_APPLICABLE。
P-03 Scope mismatch ≠ Condition failure。
P-04 UNKNOWN ≠ FALSE。
P-05 Missing Data ≠ Condition mismatch。
P-06 Supporting Unknown ≠ automatic UNDETERMINED。
P-07 No Required Condition ≠ Missing Condition Definition。
P-08 Failure Boundary ≠ Constraint。
P-09 Known Boundary Breach ≠ Knowledge Failure。
P-10 Semantic Applicability ≠ Knowledge-Use Permission。
P-11 Knowledge-Use Permission ≠ Capital Permission。
P-12 Validation Age ≠ Semantic Applicability。
P-13 Constraint Knowledge ≠ Knowledge-Use Constraint。
P-14 Knowledge Count ≠ Evidence Count。
P-15 Different Knowledge ID ≠ Independent Research。
P-16 No known dependency ≠ Proven independence。
P-17 Relationship must not be blindly inherited across semantic versions。
P-18 AI Advisory ≠ Hard Applicability Authority。
P-19 Applicability Finding ≠ Lifecycle Transition。
P-20 Applicability Assessment ≠ permanent Current Truth。
P-21 Later Lifecycle / Relationship / Knowledge Version ≠ Past Decision Context rewrite。
P-22 Current Context must be sufficiently time-consistent。
P-23 Hard Integrity concern may block new use without bypassing Lifecycle Single Writer。
P-24 Applicable Knowledge Context Set ≠ Runtime Assumption Set。
P-25 R3 Runtime Deviation ≠ R4 Position Action。
~~~

---

## 20.23 Human View

人間向け中心Flow:

~~~text
Knowledge
↓
今もACTIVE？
├─ NO
│   → Normal Applicabilityには使わない
│
└─ YES
    ↓
対象Scope？
    ↓
成立条件は合っている？
    ↓
Exclusionはない？
    ↓
Failure Boundary内？
    ↓
Semantic Applicability
    ├─ APPLICABLE
    ├─ NOT_APPLICABLE
    └─ UNDETERMINED
    ↓
そのKnowledgeを今使ってよい？
    ├─ YES → Decision Material候補
    └─ NO  → BLOCKED
    ↓
他Knowledgeとの
Relationship / Evidence重複 / Research依存 / Contradiction確認
    ↓
Decision Material Snapshot
    ↓
Decision Synthesis
~~~

Trade / Position開始後:

~~~text
実際にDecisionが依存したKnowledge / Thesis
↓
Runtime Assumption Set
↓
Current Runtime Contextと継続比較
↓
前提維持 / 劣化 / 逸脱 / Unknown
↓
R4 Runtime Protection
+
R5 Feedback
~~~

人間向け重要定義:

~~~text
Lifecycle
=
Knowledge Version自体を現在どう扱うか

Semantic Applicability
=
ACTIVE Knowledgeが今の市場で成立するか

Knowledge-Use Eligibility
=
成立するKnowledgeを今Decision材料として使わせるか

Decision Synthesis
=
複数Decision Materialをどう統合するか

R4 Capital Permission
=
その判断へ実資金を出してよいか
~~~

---

## 20.24 Human Review Result

2026-10-01のConversationでHuman Viewを確認。

Result:

~~~text
No major conceptual issue found by Daisuke.
Proceed with this direction as Working Candidate.
~~~

重要:

~~~text
Human Review completed
≠ Formal Current Architecture Adoption
~~~

---

## 20.25 Checkpoint Result

~~~text
Knowledge Applicability Precision Design
= COMPLETE / WORKING CANDIDATE

Runtime Assumption Monitoring Boundary
= COMPLETE / WORKING CANDIDATE

Precision Review / Destruction Test
= COMPLETE

Human View
= COMPLETE / REVIEWED IN CONVERSATION

Formal Current Architecture
= UNCHANGED
~~~

Current R3 detailed refinement state:

~~~text
Knowledge Admission
= detailed refinement saved

Knowledge Record minimum semantics
= detailed refinement saved

Knowledge Relationship
= detailed refinement saved

Knowledge Graph boundary
= detailed refinement saved

Version Lineage boundary
= detailed refinement saved

Knowledge Lifecycle
= Precision refinement saved

Knowledge Applicability
= Precision refinement saved
~~~

NEXT candidate:

~~~text
Decision Synthesis / Conflict Resolution detailed refinement
using Precision-First workflow:

1. Decision Synthesis responsibility
2. Decision Material Snapshot input boundary
3. conflict / opposition handling
4. no-majority / no-double-count rule
5. WAIT / UNKNOWN / abstention semantics
6. Trade Thesis / Decision Candidate responsibility
7. Runtime Assumption Set handoff
8. Precision Review
9. Human View
~~~

Later Integration Reminder:

~~~text
R3前半のAdmission / Record / Relationship / Graph / Versionは
Precision-First導入前に作られた部分を含む。

今は回収を止めて全面再設計せず、
R3 detailed recovery一巡後の
R3 Integration Precision Reviewで
不足部分だけ再検証する。
~~~

重要:

~~~text
Checkpoint 013
≠ Final Object Schema
≠ DB Table
≠ Python Class
≠ Formal Current Architecture Adoption
~~~


---

# 21. Checkpoint 014 — R3 Detailed Refinement / Decision Synthesis

**State:** SAVED / WORKING CANDIDATE  
**Phase:** Phase 5 Reconstruction — R3 Detailed Refinement  
**Formal Current Architecture Changed:** NO  
**Human Review:** No major conceptual issue found by Daisuke  
**Save Role:** AI Precision Design + Precision Review + Human ViewをWorking Studyとして保存する。正式採用ではない。

## 21.1 Scope

このCheckpointは、Knowledge Applicabilityの下流に位置するDecision Synthesisを、次の7項目としてPrecision-Firstで精密化した結果を保存する。

1. Decision Synthesis Responsibility
2. Decision Material Snapshot Input Boundary
3. Conflict / Opposition Handling
4. Majority Vote / Evidence Double Counting / Weight Semantics
5. INCONCLUSIVE / WAIT / ABSTAIN / NO-TRADE separation
6. Decision Thesis / Decision Candidate / Trade Thesis / Formal Output
7. Trade Thesis → Runtime Assumption Set handoff

加えて、全体Precision Review / Destruction TestとHuman Viewを保存する。

---

## 21.2 Decision Synthesis Responsibility

正式責任候補:

> Decision Synthesisは、Decision Material Snapshotに含まれる利用可能なDecision Materialを、Conflict、Unknown、Boundary、Relationship、Evidence / Research / Data dependencyを失わずに統合し、現在のTarget / Scope / Horizonについて成立し得るDecision Thesis Candidateを構成する責任を持つ。

Decision Synthesisは次を決めない。

~~~text
Decision Synthesis
!= Knowledge Applicability
!= Knowledge Lifecycle
!= Research Truth Authority
!= Canonical Relationship Authority
!= Economic Value
!= Capital Permission
!= Position Sizing
!= Execution
~~~

中心的な意味:

~~~text
Applicability
= 何が今使えるか

Decision Synthesis
= 使える材料を合わせると今何が言えるか

Economic Value
= そのAction Candidateに経済価値があるか

R4
= 実資金を出してよいか
~~~

Conflict Resolutionを「勝者決定」として扱わない。

~~~text
Conflict Handling
!= Conflict Winner Selection
~~~

---

## 21.3 Decision Material Snapshot Input Boundary

Decision Material SnapshotはKnowledge一覧ではない。

正式候補:

> 特定Decision Context / As-Of時点に対して、Current Market Context、利用可能なKnowledge Version、Applicability、Boundary、Relationship、Dependency、Unknownおよび重要なExcluded / Blocked Traceを固定し、Decision Synthesisが途中で変化するCurrent Stateに引きずられず再現可能な判断を行うためのImmutable Decision Input。

Logical blocks:

~~~text
Decision Material Snapshot
|
|-- A. Snapshot Identity / Time Context
|-- B. Current Market Context
|-- C. Eligible Decision Materials
|-- D. Cross-Knowledge Context
+-- E. Excluded / Blocked / Unknown Trace
~~~

重要境界:

~~~text
Decision Material Snapshot
!= Knowledge Pool
!= Current Market Source of Truth
!= Canonical Knowledge Record
!= Decision Output
!= Raw Data Warehouse
~~~

Knowledge Version、Current Context reference、Relationship / Dependency contextをAs-Ofで固定する。

ただし:

~~~text
Immutable Snapshot
!= Forever Valid Snapshot
~~~

Snapshotの過去内容は書き換えないが、Lifecycle変更、Knowledge-Use Constraint、重大なMarket Change等によりCurrent-use validityは失われ得る。

そのため:

~~~text
Decision Material Snapshot
↓
Decision Material Validity Gate
├─ VALID → Synthesis
└─ STALE / INVALID → Snapshot再構築
~~~

### ACTIVE INPUT vs TRACE ONLY

~~~text
ACTIVE INPUT
= ThesisへInfluenceしてよい

TRACE ONLY
= Audit / Explanation / Findingには参照可能
  ただしThesis Support / Oppositionには使わない
~~~

重要:

~~~text
Readable
!= Influence-Eligible
~~~

Blocked Knowledgeを「見えているから」という理由で実質的な反対票・支持票にしてはならない。

---

## 21.4 Conflict / Opposition Handling

Opposite DirectionとContradictionを分離する。

~~~text
Opposite Direction
!= Contradiction
~~~

比較前に最低限、Target / Effect Semantics / Scope / Horizonを整列する。

候補分類:

~~~text
Compatible Diversity
Horizon / Scope Divergence
Mechanism Competition
Canonical Contradiction
Unresolved / Unknown Conflict
~~~

例:

~~~text
30m Bullish
24h Bearish
↓
Cross-Horizon Opposition
!= Neutral
!= automatic Contradiction
~~~

SpotとPerpetual等のSegment差も同様に、単純矛盾として潰さない。

Canonical CONTRADICTSが存在してもDecision SynthesisはKnowledgeのTruth Winnerを決めない。

~~~text
Canonical Contradiction
↓
Competing Thesis A
Competing Thesis B
or
Unresolved Conflict
~~~

Conflictがあるから必ずINCONCLUSIVEになるわけでもない。各Thesisがcoherentに構成できれば複数Thesisとして保持できる。

Decision-time CompetitionとKnowledge-level Contradictionを分離する。

---

## 21.5 Majority Vote / Double Counting / Influence

正式禁止:

> Knowledge数、同方向Material数、Support Cluster数、Confidence単純合計、独立Research数のいずれも、それ単独でThesisの真偽・採否・Winnerを決めるVoteとして使用しない。

~~~text
Knowledge Count
!= Vote Count

Same-direction Material Count
!= Thesis Strength

Independent Research Count
!= Automatic Winner

Confidence Sum
!= Thesis Strength
~~~

Evidence / Experiment / Dataset / Derived Feature / Mechanismが依存している複数Materialを、独立Evidence Contributionとして重複加算しない。

ただし、重複したKnowledge Recordを機械的に削除するという意味ではない。

~~~text
Deduplicate Influence
!= Delete Semantic Material
~~~

### Independent Convergence

多数決禁止は、独立Researchの収束を無視することではない。

~~~text
Independent Research Convergence
Independent Mechanism Convergence
Cross-Dataset Replication
~~~

等はConvergence Contextとして保持できる。

ただし:

~~~text
Convergence
!= Vote Count
!= Automatic Winner
~~~

### Material Influence Profile

Universal Knowledge WeightはSemantic Coreに置かない。

代わりにThesis-specificなMaterial Influence Profileを持つ方向を採る。

候補軸:

~~~text
Material Role
Decision Relevance
Semantic Directness
Research / Evidence Context
Dependency Context
Applicability Robustness
Boundary Context
Current Uncertainty
Effect Semantics
Source / Trace
~~~

重要分離:

~~~text
Evidence Strength
!= Decision Relevance

Independence
!= Evidence Strength

Boundary Proximity
!= Research Weakness

Current Uncertainty
!= Research Weakness
~~~

必要な数値化は後段でPurpose-Specificに行う。

~~~text
Universal Knowledge Weight
→ 採用しない

Semantic Context
↓
EV-specific interpretation
Risk-specific interpretation
etc.
~~~

---

## 21.6 Decision Synthesis Formal Output

正式Output候補:

~~~text
Decision Synthesis Result
~~~

定義:

> 特定Decision Material Snapshotを統合した結果として、形成されたDecision Thesis Candidate群、未解消Conflict、Critical Unknown、Boundary / Dependency Context、Synthesis outcomeを追跡可能に保持するDecision Synthesisの正式出力。

### State軸修正

COHERENT / COMPETING / INCONCLUSIVEを1個のEnumへ詰めない。

理由:

~~~text
COHERENT
= Thesis内部の一貫性

COMPETING
= 複数Thesis間の関係

INCONCLUSIVE
= 十分なThesis形成ができたか
~~~

したがって意味軸を分ける。

候補:

~~~text
A. Synthesis Outcome
   - THESIS_FORMED
   - INCONCLUSIVE

B. Thesis Set Structure
   - SINGLE
   - MULTIPLE_COMPATIBLE
   - MULTIPLE_COMPETING
~~~

Exact enumは未確定。

### Decision Thesis Candidate

定義:

> Decision Material Snapshotから構成された、特定Target / Scope / Horizonに関する市場判断仮説。Supporting / Opposing Material、Boundary、Critical Unknown、Dependency、Uncertaintyを保持するが、Action・Economic Value・Capital投入を決定しない。

~~~text
Decision Thesis
!= Directional Signal
~~~

Decision Thesisは非Directionalでもよい。

例:

~~~text
Volatility expansion likely
Spot / Perpetual divergence exists
Market structure fragile
~~~

### AI Synthesis Traceability

Decision ThesisのMaterialなClaimはSourceへ追跡可能でなければならない。

~~~text
Thesis Claim
↓
Source Materials / allowed composition
~~~

AIは新しいCause / Threshold / Mechanism / ProbabilityをDecision Truthとして勝手に発明しない。

価値ある新規推論は:

~~~text
Research Hypothesis Candidate
↓
R2
~~~

へ送る。

---

## 21.7 Decision Candidate / EV / Disposition Boundary

Decision Candidate:

> Decision Thesis Candidateから導出される、Economic Value評価対象となるAction Option。Target / Exposure Intent / Horizon / Preconditions / Invalidation referencesを持つが、まだ採用・資金投入・Position Size・Executionを決定しない。

~~~text
Decision Thesis
= 市場について何が言えるか

Decision Candidate
= その市場理解から何をAction Optionとして評価できるか
~~~

良いThesisでもActionable Candidateを作れない場合がある。

~~~text
Good Thesis
!= Actionable Opportunity
~~~

Decision Candidateが無い場合、Fake EVを作らない。

~~~text
No Decision Candidate
→ No Fake EV
~~~

### INCONCLUSIVE / WAIT / ABSTAIN / NO-TRADE

~~~text
INCONCLUSIVE
= 十分なDecision Thesisを形成できなかったSynthesis状態

WAIT
= Current Opportunityを終了せず、明示的な再評価条件を伴って一時保留

ABSTAIN
= Current Decision Opportunityへの参加を終了

NO-TRADE
= 結果として新規Tradeが発生しなかったDerived Outcome / Human Projection候補
~~~

重要:

~~~text
INCONCLUSIVE
!= WAIT
!= ABSTAIN
!= NO-TRADE
~~~

WAITには「何を待つか」「何が変われば再評価するか」が必要。

WAIT != HOLD。

ABSTAIN後に市場が変わった場合、Old Decisionを無言で再開せずNew Decision Event候補とする。

NO-TRADEは原因を失わせない。

例:

~~~text
NO TRADE
because
Synthesis INCONCLUSIVE → ABSTAIN

NO TRADE
because
Positive EV → R4 Portfolio Constraint BLOCK
~~~

同じNO-TRADEでもDecision Qualityは異なる。

### PROCEED refinement

PROCEEDは曖昧なOpportunity全体状態にせず、少なくとも具体的Decision Candidate Referenceを伴う。

Opportunity DispositionとCandidate Advancementを将来分離する可能性を残す。

---

## 21.8 Trade Thesis

Trade Thesis:

> Economic Value評価を通過し、Decision Disposition / Candidate AdvancementでR4へ進めるとされたDecision Candidateについて、どのDecision Thesis、Knowledge Version、Boundary、Critical Unknown、Invalidation条件に依存してR4へ提出するかを固定するTrade-specific reasoning package。

生成順:

~~~text
Decision Thesis
↓
Decision Candidate
↓
Economic Value
↓
Candidate Advancement / PROCEED
↓
Trade Thesis
↓
R4
~~~

重要:

~~~text
Trade Thesis
!= Knowledge
!= Market Truth
!= Capital Permission
!= Executed Trade
~~~

Trade Thesisは「その時点で採用したTrade理由」。

Snapshotに存在した全Knowledgeではなく、実際に依存したKnowledge Versionを固定する。

~~~text
Applicable Knowledge Set
!= Used Knowledge Set
~~~

Later Knowledge VersionやLater RelationshipでHistorical Trade Thesisを書き換えない。

---

## 21.9 R4 Boundary

R4はCapital Expressionを変更できるが、Decision Semanticsを書き換えない。

可能例:

~~~text
Position Size縮小
Leverage縮小
Protection追加
Capital BLOCK
~~~

Decisionへ戻す必要があるMaterial変更例:

~~~text
LONG → SHORT
BTC → ETH
15m → 4h
Materially different instrument / exposure meaning
~~~

原則:

~~~text
R4 adjusts capital expression
!= R4 rewrites market decision
~~~

MaterialなDirection / Instrument / Horizon変更は:

~~~text
New Decision Candidate
↓
EV再評価
↓
New Trade Thesis
~~~

を要求する。

---

## 21.10 Trade Thesis → Runtime Assumption Set Handoff

Precision refinementにより、Trade ThesisからActive Runtime Assumption Setへ直接飛ばさない。

~~~text
Trade Thesis
↓
Runtime Assumption Seed / Handoff
↓
R4 Capital Approval
↓
Execution
↓
Actual Exposure成立
↓
Pre-Activation Validity Recheck
↓
Active Runtime Assumption Set
~~~

Runtime Assumption Set:

> 実際に成立したDecision / Exposureについて、Trade Thesisが依存したKnowledge Version、Material Assumption、Failure Boundary、Trade-specific Invalidation、Critical Unknown、Horizon、Decision-time Baselineを固定し、保有中に「当初の判断前提が現在も維持されているか」を評価するためのRuntime baseline。

重要分離:

~~~text
Decision Material Snapshot
= 利用可能だった材料

Trade Thesis
= 実際に採用した理由

Runtime Assumption Set
= Active Exposureが依存する監視対象の重要前提
~~~

~~~text
Applicable Knowledge
!= Used Knowledge
!= Must-Monitor Assumption
~~~

### Handoff content candidates

~~~text
Decision / Trade Lineage
Relied-Upon Knowledge Versions
Knowledge Role
Material Assumptions
Knowledge-derived Assumptions
Thesis-derived Assumptions
Decision-context Assumptions
Failure Boundaries
Trade Thesis Invalidation Conditions
Critical Unknowns
Decision-Time Baseline
Horizon / Temporal Semantics
Evaluation Source References
~~~

Trade Thesis AssumptionはCanonical Knowledgeではない。

~~~text
Trade Thesis Assumption
!= Knowledge Record
~~~

### Boundary separation

~~~text
Knowledge Failure Boundary
!= Trade Thesis Invalidation Condition
!= R4 Stop / Capital Protection Rule
~~~

~~~text
Semantic Failure
!= Price Stop
~~~

Runtime Assumption CriticalityはPosition Actionを決めない。

~~~text
Assumption Criticality
!= EXIT Policy
~~~

### Activation boundary

No Fillの場合:

~~~text
Trade Thesis exists
R4 ALLOW
Order submitted
No Fill
↓
Active Runtime Assumption Set = none
~~~

Partial Fill等でActual Exposureが成立した場合のみRuntime activation対象。

Execution遅延等でDecision-time contextからMaterial Changeがある場合はPre-Activation Validity Recheck候補とする。

Trade Thesis creation
!= Position activation。

Execution economicsの悪化によるEV崩壊はDecision Synthesisではなく、将来のEV ↔ R4 ↔ Execution Contractで扱うPending。

### Runtime Monitoring

Runtime Monitorは、Handoffで定義されたMaterial / Critical / Time-Sensitive assumptionsを評価する。

Runtime Monitor自身が監視対象を勝手に増減し、Original Thesisを書き換えない。

~~~text
Runtime Monitoring
= 前提がどう変わったか

R4 Runtime Protection
= その変化に対して資金をどう守るか
~~~

Runtime data missing / staleはAssumption Violationへ変換しない。

~~~text
Missing Runtime Data
!= Assumption Violation
~~~

Horizon expiryもKnowledge Failureではない。

Knowledge Lifecycle / Knowledge-Use statusのMaterial ChangeはR4へEventとして渡せるが、自動EXITではない。

---

## 21.11 Precision Review / Destruction Test Result

代表破壊ケース:

- 単一の一貫したKnowledge群
- Bullish 3 vs Bearish 1
- 同一Evidenceから3 Knowledge
- 独立Researchが同方向へ収束
- 30m Bull / 24h Bear
- same-horizon Canonical CONTRADICTS
- Critical Data missing
- Snapshot作成後にKnowledge SUSPENDED
- BLOCKED KnowledgeがTRACE ONLYで存在
- AIが新Causeを発明
- INCONCLUSIVE + no Candidate
- COHERENTだがAction mappingなし
- Multiple competing Candidates
- Multiple positive EV candidates
- R4 BLOCK
- R4によるDirection / Instrument意味変更
- Trade Thesisあり / No Fill
- Execution Delay + Market急変
- Partial Fill
- Entry後のKnowledge Version更新
- Entry後のLifecycle SUSPEND
- Runtime Data missing
- Horizon expired
- Stop Loss到達
- Thesis崩壊だがPriceは利益中
- repeated runtime mismatch
- WAIT後の再評価
- ABSTAIN後のMarket change
- NO-TRADE Reason Chain
- Later EvidenceによるPast Decision rewrite

Result:

~~~text
① Decision Synthesis Responsibility
= SURVIVED

② Decision Material Snapshot
= SURVIVED / STRENGTHENED

③ Conflict / Opposition Handling
= SURVIVED

④ Majority Vote / Weight Semantics
= SURVIVED / STRENGTHENED

⑤ INCONCLUSIVE / WAIT / ABSTAIN / NO-TRADE
= SURVIVED / RESPONSIBILITY SPLIT REFINED

⑥ Decision Thesis / Candidate / Formal Output
= SURVIVED / STATE MODEL REFINED

⑦ Trade Thesis → Runtime Assumption Set
= SURVIVED / ACTIVATION BOUNDARY STRENGTHENED
~~~

Precision Gate:
PASS as Working Candidate with the refinements in this checkpoint.

---

## 21.12 Key Precision Invariants

~~~text
DS-01 Decision Synthesis != Applicability。
DS-02 Decision Synthesis != Economic Value。
DS-03 Decision Synthesis != Capital Permission。
DS-04 Decision Material Snapshot != Knowledge Pool。
DS-05 Immutable Snapshot != Forever Valid Snapshot。
DS-06 ACTIVE INPUTとTRACE ONLYを分離する。
DS-07 Readable != Influence-Eligible。
DS-08 Opposite Direction != Contradiction。
DS-09 Different Horizon / Scope != automatic Contradiction。
DS-10 Canonical CONTRADICTS != Winner Selection。
DS-11 Knowledge Count != Vote Count。
DS-12 Same-direction Material Count != Thesis Strength。
DS-13 Shared EvidenceをIndependent contributionとして二重計上しない。
DS-14 No known dependency != Proven independence。
DS-15 Independent Convergence != Vote Count。
DS-16 Universal Knowledge WeightをSemantic Core primitiveにしない。
DS-17 Material InfluenceはThesis-specificであり得る。
DS-18 Input Validity != Synthesis Outcome。
DS-19 THESIS_FORMEDとMULTIPLE_COMPETINGは別軸。
DS-20 INCONCLUSIVE + no Candidate → Fake EV禁止。
DS-21 Decision Thesis != Directional Signal。
DS-22 Decision ThesisのMaterial claimはSourceへ追跡可能であること。
DS-23 Decision Synthesis Inference != Canonical Knowledge Creation。
DS-24 Decision Thesis != Decision Candidate。
DS-25 Good Thesis != Actionable Opportunity。
DS-26 WAIT != INCONCLUSIVE。
DS-27 WAIT != HOLD。
DS-28 ABSTAIN != Knowledge Failure。
DS-29 NO-TRADEはReason Chainを失わせない。
DS-30 PROCEED != Trade Permission。
DS-31 PROCEED / advancementはCandidate Referenceを伴う。
DS-32 Trade Thesis != Knowledge Truth。
DS-33 Trade Thesis != Capital Permission。
DS-34 R4 may alter capital expression, not semantic decision meaning。
DS-35 Direction / Instrument / HorizonのMaterial変更はNew Decisionを要求する。
DS-36 Trade Thesis creation != Position activation。
DS-37 No Fill → no Active Runtime Assumption Set。
DS-38 Applicable Knowledge != Used Knowledge != Must-Monitor Assumption。
DS-39 Knowledge Failure Boundary != Trade Thesis Invalidation != R4 Stop。
DS-40 Runtime Assumption Deviation != Position Action。
DS-41 Runtime data missing != Assumption violation。
DS-42 Horizon expiry != Knowledge Failure。
DS-43 Later Knowledge / Relationship != Past Decision Context rewrite。
DS-44 Runtime MonitorはMonitoring Contractを勝手に再定義しない。
~~~

---

## 21.13 Human View

人間向けの最小理解:

~~~text
今使えるKnowledgeを集める
↓
その時点の判断材料を固定する
↓
SnapshotはまだCurrent Decisionに有効？
├─ NO → 作り直す
└─ YES
    ↓
矛盾・重複・Unknown・Boundary・Dependencyを見る
    ↓
「今の市場について何が言えるか」をまとめる
    ↓
Thesisを作れた？
├─ NO
│   → INCONCLUSIVE
│   ↓
│   近く解決可能？
│   ├─ YES → WAIT
│   └─ NO  → ABSTAIN
│
└─ YES
    ↓
Thesisは
├─ 1つ
├─ 複数だが両立
└─ 複数で競合
    ↓
Decision Candidateを作れる？
├─ NO → WAIT / ABSTAIN候補
└─ YES
    ↓
Economic Value
    ↓
進めるCandidateがある？
├─ NO → WAIT / ABSTAIN
└─ YES
    ↓
Trade Thesis
    ↓
Runtime Assumption Seed
    ↓
R4 Capital / Risk
    ↓
Execution
    ↓
Actual Exposure成立？
├─ NO → Runtime監視なし
└─ YES
    ↓
Pre-Activation Validity Recheck
    ↓
Runtime Assumption Set
    ↓
Runtime Monitoring
    ↓
R4 Runtime Protection
+
R5 Feedback
~~~

Human key definitions:

~~~text
Decision Material Snapshot
= その時、何を知っていた？

Decision Synthesis
= そこから何が言えた？

Decision Thesis
= 成立した市場判断は何？

Decision Candidate
= 何をAction候補として評価する？

Economic Value
= その候補に経済価値はある？

WAIT
= 今は待つ。再評価する。

ABSTAIN
= 今回のOpportunityは見送る。

Trade Thesis
= なぜこのTrade候補をR4へ出す？

R4
= 実際に金を出していい？

Runtime Assumption Set
= Entry時の重要前提は何だった？

Runtime Monitoring
= その前提はまだ生きている？
~~~

中心思想:

~~~text
大量Knowledge
↓
多数決
↓
Trade
~~~

にはしない。

~~~text
Knowledge
↓
重複・依存・矛盾・Unknownを整理
↓
Market Thesis
↓
Action Candidate
↓
Economic Value
↓
Capital Safety
↓
Trade
↓
Runtime前提監視
~~~

とする。

---

## 21.14 Human Review Result

Daisuke review:

> 問題は特に無さそう。

解釈:

- Major conceptual issue: NONE FOUND
- Precision DesignとHuman Viewの責任分離に大きな違和感なし
- Working Candidateとして継続可能
- Formal Current Architectureへの採用を意味しない

---

## 21.15 Save / Adoption Boundary

今回の保存先:

~~~text
98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
00_AI/AI_HANDOFF.md
~~~

今回変更しない:

~~~text
00_AI/AI_CONTEXT.md
00_HUMAN/HUMAN_MAP.md
02_ARCHITECTURE/CONNECTIONS/
~~~

Human Viewは現時点ではWorking Study内のReview Projectionとして保存する。

正式採用後に必要なら:

~~~text
02_ARCHITECTURE/
→ Formal Precision Architecture

00_HUMAN/HUMAN_MAP.md
→ Formal Human Projection
~~~

へ改めて圧縮・反映する。

Working Studyを保存したこと自体はFormal adoptionではない。

---

## 21.16 Later Integration Reminder

R3前半のAdmission / Record / Relationship / Graph / VersionにはPrecision-First導入前に作られた部分がある。

現在の回収を止めて全面書換えはしない。

R3 detailed recoveryが一巡した後:

~~~text
Admission
→ Record
→ Relationship
→ Graph
→ Version
→ Lifecycle
→ Applicability
→ Decision Synthesis
→ Economic Value
↓
R3 Integration Precision Review
~~~

を行い、そこで生き残った不足だけを修正する。

その後、Phase 6 Destruction Reviewへ進む。

---

## 21.17 NEXT

次の詳細設計候補:

~~~text
Economic Value / Opportunity Evaluation
~~~

開始点候補:

1. Economic Value responsibility
2. EVが評価する対象 = Decision Candidate
3. Expected Effect vs Expected Value
4. Probability / Uncertainty / Distribution semantics
5. Fees / Slippage / Funding / Carry / Opportunity Cost
6. Tail / Asymmetric risk
7. Multiple Candidate comparison boundary
8. WAIT / ABSTAIN / Candidate Advancement handoff
9. R4へのEconomic Contract
10. Precision Review
11. Human View

---

## 21.18 Checkpoint Result

Checkpoint 014:

~~~text
R3 Detailed Refinement
Decision Synthesis
= SAVED WORKING CANDIDATE

Precision Review
= PASS

Human View
= REVIEWED

Human Review
= NO MAJOR CONCEPTUAL ISSUE FOUND

Formal Current Architecture
= UNCHANGED
~~~


---

# 22. Checkpoint 015 — R3 Detailed Refinement / Economic Value

**State:** SAVED / WORKING CANDIDATE  
**Phase:** Phase 5 Reconstruction — R3 Detailed Refinement  
**Formal Current Architecture Changed:** NO  
**Human Review:** Daisuke: 「問題はなそうやな」  
**Save Role:** Economic Value / Opportunity Evaluation ①〜⑨、Precision Review / Destruction Test、Refinement、Human ViewをWorking Studyとして保存する。正式採用ではない。

## 22.1 Scope

このCheckpointではDecision Synthesisの下流に位置するEconomic Value / Opportunity Evaluationについて、以下をPrecision-Firstで設計・レビューした。

1. Economic Value / Opportunity Evaluation formal responsibility
2. Evaluation Target = Decision Candidate Version / Conditions / As-Of
3. Expected Effect vs Expected Economic Value
4. Probability / Uncertainty / Distribution separation
5. Economic Cost / Friction / Holding Flow Model
6. Downside / Tail Risk / Asymmetry vs R4 Risk Permission
7. Multiple Decision Candidate comparison boundary
8. Candidate Advancement / WAIT / ABSTAIN / Trade Thesis handoff
9. R4 Economic Contract
10. ①〜⑨ Precision Review / Destruction Test
11. Human View / Human Review

中心原則:

~~~text
Market Understanding
!= Economic Value

Expected Effect
!= Expected Economic Value

Economic Value
!= Candidate Advancement

Candidate Advancement
!= Capital Permission

Capital Permission
!= Execution
~~~

---

## 22.2 Economic Value Formal Responsibility

Working definition:

> Economic Value / Opportunity Evaluationとは、特定Decision Candidate Versionについて、Research-derived Market EffectをCandidate-specificなEconomic Outcomeへ変換し、Probability / Distribution / Uncertainty、Fees / Spread / Slippage / Funding / Carry、Downside / Tail / Asymmetry等をCurrent Economic Contextと結び付けて評価し、そのCandidateのEconomic Attractiveness / Risk Structureを追跡可能なEconomic Value Assessmentとして表現する責任である。

Economic Valueが決めないもの:

~~~text
Knowledge truth
Decision Thesis formation
Candidate direction generation
Candidate semantic mutation
WAIT / ABSTAIN / ADVANCE itself
Capital Permission
Position Size
Portfolio Allocation
Execution
~~~

短縮:

~~~text
Decision Synthesis
= 今の市場について何が言える？

Decision Candidate
= 何を行動候補として評価する？

Economic Value
= その候補は実際にどんな利益・損失・Cost・Tail・不確実性を持つ？

Candidate Advancement
= 今Trade Thesis形成へ進めるだけの根拠がある？

R4
= 今のCapital / Portfolioで実際に資金を出してよい？
~~~

---

## 22.3 Evaluation Target / Candidate Version / As-Of

Economic Valueの評価対象は、意味が固定された特定Decision Candidate Version。

~~~text
Economic Evaluation
=
f(
  Decision Candidate Version,
  Economic Evaluation Context
)
~~~

Candidate semantics candidates:

~~~text
Target
Instrument
Exposure Intent
Candidate Objective
Relevant Horizon
Linked Decision Thesis
Preconditions
Invalidation References
Critical Unknowns
Decision Context Reference
~~~

Material semantic change examples:

~~~text
LONG → SHORT
BTC → ETH
PERP → SPOT
15m → 4h
RETURN_SEEKING → HEDGE
~~~

これらは同じCandidateのEconomic微調整ではない。

~~~text
Material Candidate Change
→ New Candidate / Candidate Version
→ New Economic Evaluation
~~~

### Temporal separation

~~~text
Candidate As-Of
!= Market Context As-Of
!= Cost Context As-Of
!= Economic Evaluation As-Of
~~~

全Timestamp一致ではなくTemporal Consistencyを要求する。

~~~text
Fresh Data
!= Time-Consistent Data

Future Information
!= Earlier As-Of Input
~~~

Look-aheadは禁止。

### Candidate Current-Use Validity

~~~text
Immutable Candidate
!= Forever Current Candidate
~~~

Economic Evaluation前にCandidate Current-Use Validityを確認する。

~~~text
Decision Candidate
↓
Current-Use Validity Gate
├─ VALID → Economic Evaluation
└─ STALE / INVALID → Re-decision / rebuild
~~~

---

## 22.4 Economic Evaluation Context

Logical boundary candidates:

~~~text
Economic Evaluation Context
│
├─ Decision Candidate Version Ref
├─ Decision / Thesis Lineage
├─ Candidate Objective
├─ Evaluation Baseline / Reference Context
├─ Candidate As-Of
├─ Evaluation As-Of
├─ Market Context Ref / As-Of
├─ Valuation Basis
├─ Venue / Instrument Context
├─ Fee / Funding / Carry Context
├─ Liquidity / Spread / Slippage Context
├─ Horizon
├─ Critical Unknowns
├─ Economic Model / Distribution Refs
└─ Input Freshness / Integrity Context
~~~

Valuation Basisは、Economic ValueがどのPrice / Bid-Ask / Market Stateを基準に評価したか追跡できる責任。

~~~text
Old Assessment
!= Current Assessment

Same Candidate Version
+
New As-Of / Market Context
=
New Economic Value Assessment
~~~

過去Assessmentを書き換えない。

---

## 22.5 Candidate Objective / Evaluation Baseline

Precision Reviewで追加された重要補強。

Decision CandidateはEconomic Valueの目的を明示できる必要がある。

Candidate Objective candidate examples:

~~~text
RETURN_SEEKING
HEDGE
INSURANCE
RISK_REDUCTION
LIQUIDITY_PROTECTION
~~~

Exact enumは未確定。

### Evaluation Baseline

Economic Valueは「何と比較して価値を測るか」を明示する。

Return-seeking例:

~~~text
No new exposure
vs
Candidate exposure
~~~

Hedge例:

~~~text
Reference Exposure without Hedge
vs
Reference Exposure + Hedge Candidate
~~~

重要:

~~~text
Standalone Economic Value
!= Objective-relative Economic Value

Negative Standalone EV
!= Economically Useless for Hedge / Insurance
~~~

Hedge / Insurance Candidateでは明示的なReference Exposure Snapshotが必要になり得る。

~~~text
Portfolio-referenced Economic Evaluation
!= Portfolio Capital Permission
~~~

R4のCapital Allocation authorityは維持する。

---

## 22.6 Expected Effect vs Expected Economic Value

### Expected Effect

Working definition:

> 特定Cause / Condition / Scope / Horizonのもとで、Target Market VariableがBaseline / Counterfactualに対してどのような変化を示すと研究上期待されるかを表すEffect semantics / distribution。

Expected EffectはPrice Directionに限定しない。

~~~text
Price
Volatility
Liquidity
Spread
Funding
Basis
OI
Liquidation
Correlation
Flow
Regime transition
~~~

~~~text
Expected Effect
!= Directional Trade Return
~~~

### Research Effect Profile

Logical candidate:

~~~text
Research Effect Profile
│
├─ Target Variable
├─ Scope
├─ Conditions
├─ Horizon
├─ Baseline / Counterfactual
├─ Effect Direction / Semantics
├─ Effect Distribution
├─ Central Tendency
├─ Dispersion / Tail
├─ Evidence / OOS / Replication Context
├─ Uncertainty
├─ Failure Boundary
└─ Research Provenance
~~~

### Current Effect Projection

Working responsibility:

> 既にCurrent-use validと判断されたDecision Thesis / Candidateについて、Research Effect semanticsを今回のEconomic Evaluationに必要なMagnitude / Distribution / Horizon representationへ投影する。

重要境界:

~~~text
Current Effect Projection
!= Applicability

!= Decision Thesis Formation

!= Direction Generator
~~~

Material Context mismatchをEconomic Valueが勝手に修正しない。

~~~text
Material Current Effect Mismatch
→ Applicability / Decision Synthesis
~~~

Arbitrary discountは禁止。

~~~text
Boundary approaching
→ Effect × arbitrary discount
~~~

のような未検証係数をAIが発明しない。

### Monetization Mapping

Working definition:

> Research-derived Market Effectを、特定Decision CandidateのInstrument / Exposure / Horizon / Valuation Basisに対するGross Economic Outcomeへ変換する規則。

~~~text
Market Effect Distribution
↓
Instrument-specific Payoff / Monetization Mapping
↓
Gross Economic Outcome Distribution
~~~

~~~text
Expected Effect
!= Candidate Economic Outcome
~~~

Valid EffectでもCandidate-specific mappingが無ければEVを捏造しない。

~~~text
Valid Market Effect
+
No validated Monetization Mapping
→ Economic Mapping INSUFFICIENT
→ possible Research Gap
~~~

---

## 22.7 Gross vs Net Economic Outcome

Economic ValueはGrossとNetを分離する。

~~~text
Current Effect Projection
↓
Monetization Mapping
↓
Gross Economic Outcome Distribution
↓
Economic Friction & Holding Flow
↓
Net Economic Outcome Distribution
~~~

~~~text
Gross Economic Outcome
!= Net Economic Outcome
~~~

Expected Economic Valueは上位Truthではなく、Net Economic Outcome Distributionから導出されるDerived Metric。

~~~text
Expected Value number
!= Full Economic Value Assessment
~~~

---

## 22.8 Probability / Distribution / Uncertainty

中心分離:

~~~text
Distribution
= どんなOutcomeがどの範囲・形で起こり得るか

Probability
= 特定Outcome / EventへどれだけProbability Massを置くか

Uncertainty
= Distribution / Probability / Mapping自体をどこまで信用できるか
~~~

~~~text
Probability
!= Uncertainty

Distribution
!= Single Probability

Uncertainty
!= 1 - Probability
~~~

### Uncertainty dimensions

少なくとも意味として以下を分離する。

~~~text
Outcome / Aleatoric Uncertainty
Data Uncertainty
Model Uncertainty
Parameter / Estimation Uncertainty
Regime / Context-Match Uncertainty
Mapping Uncertainty
Cost / Execution Uncertainty
Dependency / Structural Uncertainty
~~~

Unknownも別。

~~~text
Unknown
!= Uncertainty

Unknown Probability
!= 50%

Missing Data
!= Neutral Outcome
~~~

### Outcome Distribution vs Distribution Uncertainty

~~~text
Level 1:
Outcome Distribution

Level 2:
Uncertainty About That Distribution
~~~

MeanだけをFull Distributionとしない。

### Probability provenance

ProbabilityはSource / Calibration / Validation / Regime / Sample / Uncertaintyへ追跡可能にする。

~~~text
Outcome Probability
!= Knowledge Truth Probability

Calibration
!= Accuracy
!= Edge
~~~

### Evaluation Mode

Precision Reviewで追加。

~~~text
Economic Value Assessment
│
├─ Probabilistic Evaluation
├─ Empirical Distribution Evaluation
├─ Scenario Evaluation
└─ Stress Evaluation / Context
~~~

Exact enumは未確定。

Strict Expected Economic Valueを使うにはvalid probability semanticsが必要。

~~~text
Scenario Weight
!= Validated Probability

Scenario-weighted Estimate
!= Strict Expected Value

Stress Exposure
!= Expected Value
when Probability is unknown
~~~

---

## 22.9 Economic Friction & Holding Flow Model

Precision Reviewで「Cost Model」より意味を広げる。

Working responsibility:

> Candidateを特定Venue / Instrument / Horizon / Exposure / Market Contextで実行・保有した時に発生し得るEconomic FrictionとSigned Holding Flowを、Size / Market State / Time / Path dependency、Uncertainty、Coverage Boundary、Provenanceを保持して評価する。

本命構造:

~~~text
Entry Friction
├─ Fee / Rebate
├─ Spread
├─ Slippage
└─ Market Impact

Holding Economic Flow
├─ Funding
├─ Carry
└─ Borrow / Financing

Exit Friction
├─ Fee / Rebate
├─ Spread
├─ Slippage
└─ Market Impact
~~~

Opportunity CostはDirect Friction / Flowと分離する。

~~~text
Direct Economic Friction / Holding Flow
!= Relative Opportunity Cost
~~~

Funding / Rebateは正負両方向。

~~~text
Funding
!= Always Cost
~~~

### Cost behavior

~~~text
Fixed / Schedule-based
Size-dependent
Market-State-dependent
Time-dependent
Path-dependent
Relative / Opportunity-dependent
~~~

### Coverage / Double Count Guard

~~~text
Fee
!= Spread
!= Slippage
!= Market Impact
~~~

Modelが別Componentを内包する場合があるためCoverage Boundaryを明示する。

~~~text
Slippage includes Spread
→ do not add Spread again
~~~

FundingがCarryに含まれる場合も二重計上禁止。

### Joint dependency

悪いMarket Outcome時にCostも悪化し得る。

~~~text
Price Down
→ Volatility Up
→ Liquidity Down
→ Spread / Slippage Up
~~~

Known material dependencyを独立仮定へ置き換えない。

~~~text
Marginal Distributions alone
!= Joint Economic Distribution

No known dependency
!= Proven independence
~~~

Expected CostとRealized Costを分離し、RealizedでPast Expected Costを書き換えない。

---

## 22.10 Downside / Tail / Asymmetry

Economic Value側の責任:

> Net Economic Outcome Distributionについて、通常損失、Lower-tail、Extreme Tail、Gain/Loss Asymmetry、Stress Exposure等を記述する。ただしそのRiskを実際にCapitalとして許容するかはR4が決定する。

~~~text
Expected Economic Value
!= Economic Risk Profile

Economic Risk Characterization
!= Capital Risk Permission

Positive EV
!= Acceptable Risk
~~~

### Downside

~~~text
Loss Probability
Loss Magnitude Distribution
Lower Quantiles
Conditional Loss Severity
~~~

Loss ProbabilityだけでDownside Riskを表さない。

### Tail

~~~text
Downside Risk
!= Tail Risk

Tail Severity
!= Tail Probability

Unknown Tail Probability
!= Zero Tail Risk
~~~

Probabilistic TailとStress Tailを分離。

~~~text
Expected Distribution Tail
+
Stress Exposure Context
~~~

Stress Probabilityを勝手に発明しない。

### Asymmetry

Upside / Downside / Tail / Payoff shapeを別々に保持する。

~~~text
Same EV
!= Same Asymmetry
~~~

VaR / Expected Shortfall / Sharpe等は必要ならDerived ViewでありCanonical Economic Truthではない。

### Economic Risk Profile

Logical candidate:

~~~text
Economic Risk Profile
│
├─ Downside Profile
├─ Probabilistic Tail
├─ Tail Severity / Uncertainty
├─ Unknown Tail Context
├─ Asymmetry Profile
├─ Stress Exposure
├─ Liquidity / Exit Fragility
├─ Path Dependency
├─ Cost-tail Dependency
├─ Risk Uncertainty
└─ Provenance / As-Of
~~~

---

## 22.11 Multiple Candidate Comparison

順番:

~~~text
Candidate
↓
Standalone Economic Value Assessment
↓
Comparison Eligibility
↓
Relative Economic Comparison
~~~

Relative ComparisonでStandalone Economic Valueを書き換えない。

~~~text
Candidate coexistence
!= Direct Comparability
~~~

比較前に少なくともObjective / Horizon / Economic Basis / Numeraire / As-Of / Size Region / Venue / Validityを確認する。

Economic Valueはdimension-specific comparisonを出してよい。

~~~text
Expected EV
Median
Cost
Downside
Tail
Asymmetry
Uncertainty
Liquidity / Exit
Stress
Size Region
~~~

ただし、

~~~text
Highest EV
!= Automatic Winner

Lower Risk
!= Automatic Winner

Dimension-specific ordering
!= Overall Candidate Selection
~~~

Global Best Candidate RankingはCanonicalにしない。

### Dominance / Non-Dominated Set

~~~text
Economically Dominated
!= Automatically Rejected

Non-Dominated Set
!= Final Selected Set
~~~

### Cross-Candidate dependency

Precision Reviewで追加。

~~~text
shared market factor
shared liquidity dependency
shared venue
shared funding regime
shared underlying
~~~

等のCross-Candidate Economic DependencyをR4へ渡せるようにする。

---

## 22.12 Opportunity Context

Economic Value側では、

~~~text
Standalone Economic Value
+
Relative Economic Difference
+
Potential Opportunity Context
~~~

を扱える。

しかし本当のOpportunity CostにはCapital scarcity / mutual exclusivity / execution timing / portfolio constraintsが関わる。

~~~text
Potential Opportunity Context
!= Allocative / Realized Opportunity Cost

Economic Alternative
!= Capital Mutually Exclusive
~~~

Portfolio AllocationはR4。

No-Actionも常に0とは固定しない。

~~~text
Economic Value
=
Candidate Outcome
relative to
explicit Evaluation Baseline
~~~

---

## 22.13 Candidate Advancement / WAIT / ABSTAIN

Working definition:

> 特定Decision Candidate VersionとCurrent-use ValidなEconomic Value Assessmentを受け取り、必要に応じRelative Economic Comparison Contextを参照し、Versioned Advancement Criteriaに基づいて、現在Trade Thesisを形成するに足るEconomic / Decision BasisがあるかをCandidate-specificに判定する。

~~~text
Candidate Advancement
!= Best Candidate Selection
!= Capital Permission
!= Position Sizing
!= Portfolio Allocation
!= Execution
~~~

### ADVANCE

~~~text
ADVANCE
=
Trade Thesisを形成してよい

ADVANCE
!= Tradeしてよい
!= Capital Permission
~~~

0 / 1 / multiple Candidatesが同時にADVANCE可能。

### WAIT

~~~text
今は進めない
+
Opportunityはまだ生きている
+
何を待つか / 再評価条件が明示されている
~~~

WAIT requires Re-evaluation Trigger.

~~~text
WAIT Trigger
↓
Candidate Current-Use Validity
↓
New Economic Evaluation Context
↓
New Economic Value Assessment
↓
New Candidate Advancement Record
~~~

WAIT recordを直接ADVANCEへ書き換えない。

### ABSTAIN

~~~text
今回のCandidate Opportunityを終了する
~~~

ただし、

~~~text
ABSTAIN
!= Permanent Ban
!= Knowledge Refutation
!= Thesis Failure
~~~

Positive EVもAutomatic ADVANCEではない。
Negative standalone EVもHedge等ではAutomatic ABSTAINではない。

Advancement thresholdをAIがad hocに発明しない。

---

## 22.14 Candidate Advancement Record

Logical candidate:

~~~text
Candidate Advancement Record
│
├─ Candidate Version Ref
├─ Decision Opportunity Ref
├─ Economic Value Assessment Ref
├─ Relative Comparison Ref [optional]
├─ Disposition: ADVANCE / WAIT / ABSTAIN
├─ Advancement Basis
├─ Critical Economic Findings
├─ Critical Unknowns
├─ Economic Validity Conditions
├─ Policy / Criteria Version
├─ Evaluation As-Of
├─ WAIT Trigger / Expiry
├─ ABSTAIN Reason
└─ Trace / Provenance
~~~

Historical recordはimmutable。

~~~text
Immutable ADVANCE Record
!= Forever Valid Advancement
~~~

Trade Thesis形成前にCurrent-use validityを再確認できるようにする。

---

## 22.15 Economic Value → Trade Thesis Handoff

Economic Value AssessmentからTrade Thesisへ直接飛ばさない。

~~~text
Economic Value Assessment
↓
Candidate Advancement
↓
Candidate Advancement Record
↓
[ADVANCE]
Trade Thesis Formation
~~~

情報を3段階へ分離する。

~~~text
Evaluated Economic Evidence
!= Advancement Basis
!= Trade Thesis Economic Basis
~~~

Trade ThesisへのEconomic handoff候補:

~~~text
Candidate / Decision Lineage
Candidate Objective
Economic Assessment Reference
Advancement Basis
Economic Validity Conditions
Accepted Risks / Unknowns
Evaluation Scope / As-Of
~~~

Trade ThesisへEconomic Value Assessment全文を複製せず、Reference + materially relied-upon economicsを固定する。

### Economic Validity Conditions

> 今回のEconomic Assessmentが経済的意味を保つために必要な条件。

例:

~~~text
Venue
Evaluated size region
Leverage region
Spread / Slippage region
Funding / Carry region
Entry valuation region
Horizon
Execution assumption region
~~~

重要分離:

~~~text
Knowledge Failure Boundary
!= Trade Thesis Invalidation
!= Economic Validity Condition
!= R4 Capital Constraint
~~~

Accepted UnknownはResolved Unknownではない。

---

## 22.16 R4 Economic Contract

Working definition:

> ADVANCEされたDecision Candidate / Trade Thesisについて、どのEconomic Value Assessment、Economic Risk Profile、Economic Validity Conditions、Evaluated Economic Region、Accepted Unknowns等を前提としてR4がCapital Permission / Capital Expressionを判断できるかを固定し、R4が変更可能な範囲と上流再評価境界を定める論理契約。

中心原則:

~~~text
R4 is an Economic Envelope consumer,
not the Economic Envelope author.
~~~

R4へ渡す論理ブロック:

~~~text
Decision / Trade Lineage
Candidate Semantics
Economic Assessment
Joint Economic Envelope
Economic Risk Profile
Accepted Unknowns / Validity Conditions
Current Validity / As-Of
~~~

R4が勝手に変更しない:

~~~text
Target
Material Instrument Semantics
Direction / Exposure Intent
Candidate Objective
Material Horizon
Decision Thesis
Canonical Knowledge
Economic Assessment
Risk Characterization
Accepted Unknown truth state
~~~

R4 Mutable Fields候補:

~~~text
Capital Permission
Approved Exposure Size
Approved Leverage
Capital Reservation
Protection Requirements
Portfolio Allocation
~~~

ただしJoint Economic Envelope内。

---

## 22.17 Joint Economic Envelope

Precision Reviewで強化。

~~~text
Economic Envelope
=
evaluated combinations / joint region
~~~

例えば:

~~~text
(Size, Leverage, Venue, Order Type, Spread, Horizon)
~~~

のJoint Context。

重要:

~~~text
Inside every individual bound
!= Inside evaluated Joint Economic Envelope
~~~

例:

~~~text
0.02 BTC @ 1x evaluated
0.005 BTC @ 2x evaluated

does not imply

0.02 BTC @ 2x evaluated
~~~

Joint Economic Envelope外ならEconomic Re-evaluation required。

---

## 22.18 R4 Change Classification / Return Router

R4で変更が必要になった時、全部Economic Valueへ返さない。

### Type A — Capital-only Change

~~~text
Evaluated Joint Envelope内のSize selection
Capital reservation
Portfolio exposure limitation
BLOCK
~~~

→ R4内。

### Type B — Economic Change

~~~text
Size outside envelope
Leverage outside envelope
Unevaluated Venue
Material entry valuation change
Spread / Slippage regime change
Funding / Carry change
Material execution-method change
Economically material protection change
~~~

→ Economic Re-evaluation。

### Type C — Candidate Semantic / Composite Change

~~~text
Long → Short
BTC → ETH
RETURN_SEEKING → HEDGE
15m → 4h
new instrument leg
new composite payoff
~~~

→ Decision Candidate Formation。

### Type D — Thesis / Knowledge Validity Change

~~~text
Trade Thesis invalidation
Core Knowledge SUSPENDED
Critical Applicability change
Failure Boundary breached
Material contradiction
~~~

→ Applicability / Decision Synthesis。

---

## 22.19 R4 Protection Refinement

Protectionを3種類へ分ける。

~~~text
Protection A
=
already inside evaluated Economic Envelope
→ R4

Protection B
=
same Candidate semantics,
but materially changes Economic Profile
→ Economic Re-evaluation

Protection C
=
new instrument leg / new objective / new payoff structure
→ New / Composite Decision Candidate
~~~

~~~text
Safer-looking change
!= Economically neutral change

New economic leg
!= mere parameter adjustment
~~~

---

## 22.20 Economic Re-evaluation Lineage

R4 ↔ EVを上書きLoopにしない。

Logical candidate:

~~~text
Economic Re-evaluation Request
│
├─ Source R4 Decision Ref
├─ Current Economic Assessment Ref
├─ Requested Change
├─ Change Classification
├─ Reason
├─ Requested Evaluation Context
└─ As-Of
~~~

Lineage:

~~~text
EVA-101
↓
R4 Re-evaluation Request
↓
EVA-102
↓
New Candidate Advancement Record
↓
New / updated Trade Thesis lineage
↓
New R4 Economic Contract
↓
R4
~~~

Past Economic Assessmentを上書きしない。

---

## 22.21 Precision Review / Destruction Test

代表ケース:

- Research Effect +0.8% / Long Candidate
- 同じEffect / Short Candidate
- Volatility Effect / Spot Long mapping unavailable
- Research Horizon 24h / Candidate 15m
- Candidate作成後Market急変
- Past EV +0.5 / Current EV -0.1
- Uncalibrated P(up)=65%
- Stress -20% / probability unknown
- Mean only / no full distribution
- Slippage missing
- Spread already inside Slippage model
- Funding benefit
- Bad market outcome + bad cost dependence
- Positive EV + severe Tail
- Hedge negative standalone EV
- Multiple positive candidates
- Return vs Hedge comparison
- Multiple ADVANCE
- WAIT + information update
- ADVANCE becomes stale
- R4 size inside envelope
- R4 size outside envelope
- R4 Long → Short
- R4 Venue change
- R4 Stop change
- R4 adds new Hedge leg
- Knowledge SUSPENDED during R4
- Old EV used later
- R4 → EV → R4 repeated re-evaluation
- individual bounds inside but joint combination untested
- Economic Value attempts to re-decide Bull / Bear
- Research correct but monetization / cost failed
- Trade profitable but original research wrong

Result:

~~~text
① Economic Value Formal Responsibility
= SURVIVED

② Evaluation Target / As-Of
= SURVIVED / STRENGTHENED

③ Expected Effect → Economic Value
= SURVIVED / CURRENT EFFECT AUTHORITY REFINED

④ Probability / Uncertainty / Distribution
= SURVIVED / EVALUATION MODE REFINED

⑤ Cost Model
= SURVIVED / FRICTION + SIGNED FLOW REFINED

⑥ Downside / Tail / Asymmetry vs R4
= SURVIVED / HEDGE BASELINE REFINED

⑦ Multiple Candidate Comparison
= SURVIVED / CROSS-CANDIDATE DEPENDENCY STRENGTHENED

⑧ Candidate Advancement / Trade Thesis Handoff
= SURVIVED

⑨ R4 Economic Contract
= SURVIVED / JOINT ENVELOPE + COMPOSITE PROTECTION + RETURN ROUTER REFINED
~~~

Precision Gate:

~~~text
PASS AS WORKING CANDIDATE
after current refinements
~~~

---

## 22.22 Key Precision Review Refinements

A. Hedge / Insurance requires explicit Objective-relative Baseline / Reference Exposure when needed.

B. Economic Envelope is Joint, not independent per-field bounds.

C. Strict Expected Value requires valid probability semantics.

D. Direct Cost wording is widened to Economic Friction & Signed Holding Flow.

E. Current Effect Projection cannot re-decide Applicability or Direction.

F. New R4 protection leg is Composite Candidate formation, not mere EV parameter tweak.

G. R4 ↔ EV re-evaluation must form immutable lineage.

H. Potential Opportunity Context remains distinct from Allocative / Realized Opportunity Cost.

I. Cross-Candidate dependency should remain visible to R4.

J. No-Action semantics depend on Objective / Evaluation Baseline.

---

## 22.23 Key Precision Invariants

~~~text
EVP-01 Economic Value evaluates a specific Decision Candidate Version.
EVP-02 Candidate semantics must not mutate inside Economic Evaluation.
EVP-03 Candidate As-Of != Evaluation As-Of.
EVP-04 Immutable Candidate != Forever Current Candidate.
EVP-05 Economic Value Assessment is Context-bound / As-Of-bound.
EVP-06 Past Economic Assessment must not be overwritten by later Assessment.
EVP-07 Candidate Objective must be explicit enough to interpret value.
EVP-08 Evaluation Baseline / Reference Context must be explicit.
EVP-09 Standalone EV != Objective-relative Economic Value.
EVP-10 Expected Effect != Expected Economic Value.
EVP-11 Market Effect != Candidate P&L.
EVP-12 Valid Effect != Monetizable by every Candidate.
EVP-13 Current Effect Projection != Applicability.
EVP-14 Current Effect Projection != Direction Generator.
EVP-15 Missing Monetization Mapping != Zero EV.
EVP-16 Gross Economic Outcome != Net Economic Outcome.
EVP-17 Probability != Uncertainty.
EVP-18 Unknown Probability != 50%.
EVP-19 Scenario Weight != Validated Probability.
EVP-20 Scenario-weighted Estimate != Strict Expected Value.
EVP-21 Stress Probability must not be invented.
EVP-22 Mean Outcome != Full Outcome Distribution.
EVP-23 Outcome Distribution != Uncertainty about Distribution.
EVP-24 Funding / Rebate may be signed Benefit or Cost.
EVP-25 Fee != Spread != Slippage != Market Impact.
EVP-26 Cost Coverage boundaries must prevent double counting.
EVP-27 Expected Cost != Realized Cost.
EVP-28 Known material outcome/cost dependency must not be silently treated independent.
EVP-29 Expected Economic Value != Economic Risk Profile.
EVP-30 Positive EV != Acceptable Capital Risk.
EVP-31 Downside Risk != Tail Risk.
EVP-32 Unknown Tail Probability != Zero Tail Risk.
EVP-33 Same EV != Same Asymmetry.
EVP-34 Candidate Economic Risk != Portfolio Risk.
EVP-35 Candidate coexistence != Direct Comparability.
EVP-36 Highest EV != Automatic Winner.
EVP-37 Global Best Candidate Ranking is not Canonical Economic Output.
EVP-38 Economic Alternative != Capital Mutually Exclusive.
EVP-39 Potential Opportunity Context != Allocative Opportunity Cost.
EVP-40 Economic Value Assessment != Candidate Advancement.
EVP-41 ADVANCE != Trade Permission.
EVP-42 Multiple Candidates may ADVANCE.
EVP-43 WAIT requires identifiable Re-evaluation Trigger.
EVP-44 WAIT Trigger → New Assessment / New Advancement, not direct ADVANCE.
EVP-45 ABSTAIN != Knowledge Refutation.
EVP-46 Positive EV != Automatic ADVANCE.
EVP-47 Negative Standalone EV != Automatic ABSTAIN for Hedge / Insurance.
EVP-48 Advancement Criteria must be explicit / versioned.
EVP-49 Trade Thesis must reference exact EVA / Advancement record.
EVP-50 Accepted Unknown != Resolved Unknown.
EVP-51 Knowledge Failure Boundary != Economic Validity Condition.
EVP-52 Economic Validity Condition != R4 Capital Constraint.
EVP-53 R4 is an Economic Envelope consumer, not author.
EVP-54 Economic Envelope is a Joint evaluated region.
EVP-55 Inside individual bounds != inside Joint Economic Envelope.
EVP-56 R4 must not rewrite Direction / Target / Objective / Thesis.
EVP-57 R4 must not rewrite Economic Value / Risk characterization.
EVP-58 R4 may BLOCK a valid positive-EV Candidate.
EVP-59 R4 BLOCK != Economic invalidity.
EVP-60 Outside Joint Economic Envelope → Economic Re-evaluation.
EVP-61 New instrument leg / composite payoff → Candidate Formation.
EVP-62 Thesis / Knowledge validity change != mere Economic re-evaluation.
EVP-63 R4 → EV Re-evaluation creates new immutable lineage.
EVP-64 Capital Permission != Forever-valid Execution Permission.
EVP-65 Execution must remain within authorized Economic / Capital conditions.
~~~

---

## 22.24 Human View

Human-level definition:

> Economic Valueとは、市場理解から作られた具体的な行動候補について、「この条件なら、実際にどんな利益・損失分布になり、どんなCost・Tail Risk・不確実性を持つのか」を調べる仕組み。その候補を次へ進めるかはCandidate Advancement、実際に資金を出すかはR4が決める。

全体:

~~~text
市場研究
↓
今使えるKnowledge
↓
Decision Thesis
↓
Decision Candidate
↓
何を目的にやる？
↓
何と比較して価値を測る？
↓
市場の動きをこのCandidateでどうP&Lへ変える？
↓
Fee / Spread / Slippage / Funding / Carry等を反映
↓
Net Outcome Distribution
↓
EV / Downside / Tail / Asymmetry / Unknown
↓
他CandidateとのEconomic difference
↓
Trade Thesisへ進める？
├─ ADVANCE
├─ WAIT
└─ ABSTAIN
↓
ADVANCE
↓
Trade Thesis
↓
R4
↓
Current Portfolio / Capitalで本当に資金を出せる？
~~~

Human key definitions:

~~~text
Expected Effect
= 市場がどう動く？

Monetization Mapping
= その動きをこのCandidateではどうP&Lへ変える？

Economic Value
= Costまで入れるとどんな利益・損失構造？

Distribution
= 何が起こり得る？

Probability
= どれくらい起こりそう？

Uncertainty
= その推定自体をどこまで信用できる？

Downside
= 負ける側はどう？

Tail
= 最悪側ではどこまで壊れる？

ADVANCE
= Trade Thesisを作る段階へ進める

WAIT
= 再評価条件付きで待つ

ABSTAIN
= 今回のOpportunityは見送る

R4
= 現在の口座で実際にどれだけRisk / Capitalを許可する？
~~~

Economic Envelope Human View:

> Economic Valueが「ちゃんと評価済み」の条件組み合わせ。

~~~text
各条件が個別に範囲内
!=
その組み合わせも評価済み
~~~

Hedge Human View:

~~~text
Return Candidate
= これ単体でどんな経済性？

Hedge Candidate
= Reference Exposureへ追加した時、
  Loss Distributionがどう改善する？
~~~

Return Router Human View:

~~~text
資金量だけ / 評価済みEnvelope内
→ R4

Fee / Size / Venue / Slippage等のEconomic条件
→ Economic Value

Long→Short / BTC→ETH / new Hedge leg等
→ Decision Candidate

市場判断が崩れた
→ Decision Synthesis

Knowledgeが使えなくなった
→ Applicability
~~~

---

## 22.25 Human Review Result

Daisuke review:

> 問題はなそうやな

Interpretation:

~~~text
Major conceptual issue:
NONE FOUND

Human View:
ACCEPTABLE

Precision Design / Human View mismatch:
NO MAJOR ISSUE FOUND

Working Candidate:
READY TO SAVE
~~~

これはFormal Current Architecture adoptionを意味しない。

---

## 22.26 Save / Adoption Boundary

今回保存:

~~~text
98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
00_AI/AI_HANDOFF.md
~~~

今回変更しない:

~~~text
00_AI/AI_CONTEXT.md
00_HUMAN/HUMAN_MAP.md
02_ARCHITECTURE/
~~~

Human Viewは現時点ではWorking Study内のReview Projection。

正式採用後、必要ならFormal Precision ArchitectureとOfficial Human Projectionへ圧縮・反映する。

---

## 22.27 R3 Integration Review Boundary

Economic Valueまでで、R3 detailed recoveryの主要連鎖は次まで揃った。

~~~text
Knowledge Admission
→ Knowledge Record
→ Knowledge Relationship
→ Knowledge Graph
→ Version Lineage
→ Knowledge Lifecycle
→ Knowledge Applicability
→ Decision Synthesis
→ Economic Value
~~~

Admission / Record / Relationship / Graph / Versionの一部はPrecision-First導入前に作成された。

次工程:

~~~text
R3 Integration Precision Review
~~~

Review target:

~~~text
Admission
→ Record
→ Relationship
→ Graph
→ Version
→ Lifecycle
→ Applicability
→ Decision Synthesis
→ Economic Value
~~~

責任重複、用語ズレ、Object境界、Version / As-Of、Unknown handling、Authority、Return Route、Human View consistencyを横断確認し、生き残った不足だけを修正する。

その後Phase 6 Destruction Reviewへ進む。

---

## 22.28 Checkpoint Result

Checkpoint 015:

~~~text
R3 Detailed Refinement
Economic Value / Opportunity Evaluation
= SAVED WORKING CANDIDATE

Precision Review
= PASS AFTER REFINEMENTS

Human View
= REVIEWED

Human Review
= NO MAJOR CONCEPTUAL ISSUE FOUND

Formal Current Architecture
= UNCHANGED
~~~

---

# 23. Checkpoint 016 — R3 Integration Precision Review / Issue Consolidation & Repair Plan

**Date:** 2026-10-03  
**State:** SAVED / WORKING REVIEW CHECKPOINT  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction — R3 Integration Precision Review  
**Save Role:** Checkpoint 015までに復元したR3をAdmission〜Economic Valueまで横断し、STEP 1〜7で発見したFindingをRoot Issueへ統合し、Integration Repair前の基準点として保存する。  
**Repair Applied In This Checkpoint:** NO  
**Next:** Repair Package A — Knowledge Foundation から開始する。

## 23.1 Review Target

今回の横断対象:

~~~text
Knowledge Admission
→ Knowledge Record
→ Knowledge Relationship
→ Knowledge Graph
→ Version Lineage
→ Knowledge Lifecycle
→ Knowledge Applicability
→ Decision Material Snapshot
→ Decision Synthesis
→ Decision Thesis
→ Decision Candidate
→ Economic Value
→ Candidate Advancement
→ Trade Thesis
→ R4 Economic Contract boundary
~~~

目的:

> 各Componentが単体で成立しているかではなく、1本のR3 Systemとして接続した時に、責任・Authority・Object Truth・Version / As-Of・Unknown・Dependency・Return Routeが壊れていないかを確認し、生き残った問題だけをRepair対象へする。

中心Review Questions:

~~~text
上流は何を保証する？
何を渡す？
下流は何を信じてよい？
下流は何を変更してはいけない？
問題時はどのSemantic Ownerへ戻す？
~~~

---

## 23.2 STEP 1 — Canonical Vocabulary Review

Result:

~~~text
PASS WITH INTEGRATION ISSUES
~~~

主要Vocabulary統合方向:

~~~text
Lifecycle State
→ Precisionでは Lifecycle Disposition を優先

Decision Thesis Candidate
→ Decision Thesis へ統一方向

PROCEED
→ ADVANCE へ統一方向

Decision Disposition
→ Candidate Disposition へ寄せる

Economic Value / Opportunity Evaluation
→ Economic Value Evaluation を責任名候補

Economic Envelope
→ Joint Economic Envelope を精密名として優先

Economic Cost Model
→ Economic Friction & Holding Flow Model
~~~

Generic単語の単独使用は避ける方向:

~~~text
Current
Valid
State
Unknown
Blocked
Boundary
Constraint
Candidate
Version
Confidence
EV
~~~

必ず対象軸を明示する。

重要分離:

~~~text
Failure Boundary
!= Knowledge-Use Constraint
!= Trade Thesis Invalidation Condition
!= Economic Validity Condition
!= R4 Capital Constraint
~~~

---

## 23.3 STEP 2 — Responsibility / Authority Matrix

Result:

~~~text
PASS WITH AUTHORITY GAPS
~~~

R3共通Authority分離候補:

~~~text
Generate / Detect
!= Assess
!= Decide / Authorize
!= Canonical Write
~~~

特にKnowledge Lifecycleは既に強い基準形:

~~~text
Trigger
↓
Lifecycle Assessment
↓
Transition Proposal
↓
Lifecycle Governance
↓
Authorized Decision
↓
Single Writer
↓
Canonical Lifecycle State
~~~

確認されたAuthority Gap:

~~~text
A. Knowledge Admission Decision / Canonical Record Writer
B. Canonical Knowledge Relationship Approval / Writer
C. Knowledge Version Approval / Version Lineage Writer
D. Knowledge-Use Constraint Authorization
E. Decision Material Eligibility / Snapshot sealing authority
F. Decision Candidate Formation authority
G. Candidate Advancement Policy Governance
H. Trade Thesis Adoption / Canonical Writer
I. R4 Economic Contract creation / version owner
~~~

横断原則:

> 下流は上流の結果を利用できるが、上流の意味を再定義してはいけない。問題を見つけたら、その意味を所有するAuthorityへ返す。

---

## 23.4 STEP 3 — Object Boundary Review

Result:

~~~text
PASS WITH 6 BOUNDARY REFINEMENTS
~~~

Object分類:

~~~text
Canonical Semantic Object
Assessment Object
Snapshot / Historical Object
Derived View
~~~

中心原則:

~~~text
Canonical semantic fact
=
one canonical owner

Downstream reference
!= duplicated canonical truth
~~~

主要Boundary Finding:

~~~text
1. Knowledge Record Known Contradictions
   vs Canonical Knowledge Relationship

2. Knowledge Record
   vs Knowledge Version

3. Decision Synthesis Result
   vs Decision Thesis

4. EVA
   vs Risk / Cost / Envelope sub-object ownership

5. Critical / Accepted Unknown
   source identity / downstream treatment

6. Failure Boundary definition
   vs downstream Boundary status / usage
~~~

重要:

~~~text
Logical Object count
!= Database Table count
!= Python Class count
~~~

現段階では意味所有権だけを確定し、Physical implementationへ降ろさない。

---

## 23.5 STEP 4 — Forward Handoff Review

Result:

~~~text
PASS WITH 5 CONFIRMED INTEGRATION FINDINGS
~~~

Finding:

~~~text
FH-001
Decision Material Snapshot must pin
Decision Target / Scope / Horizon.

FH-002
Decision Snapshot must not consume
floating Knowledge Relationships.

FH-003
Decision Thesis Candidate
should converge toward Decision Thesis
unless a real promotion boundary is found.

FH-004
Decision Candidate contract is older than
Economic Value requirements.

FH-005
Economic Value Assessment needs
an explicit Evaluation Availability / Sufficiency axis.
~~~

特にFH-004 / FH-005はRepair必須。

Forward principle:

~~~text
Meaning Preservation
Progressive Narrowing
Reference over Copy
~~~

---

## 23.6 STEP 5 — Version / As-Of / Lineage Review

Result:

~~~text
PASS WITH 8 TEMPORAL INTEGRATION FINDINGS
~~~

Finding:

~~~text
VT-001
Knowledge Version needs explicit temporal identity.

VT-002
Event / Source Time
!= Information Availability Time
!= Assessment / Decision Time.

VT-003
New Knowledge Version must not silently inherit
old Applicability / Relationship / Lifecycle assumptions.

VT-004
Relationship requires Version + historical availability semantics.

VT-005
Knowledge-Use Constraint requires revision / effective-time semantics.

VT-006
Decision Thesis should be immutable per synthesis context.

VT-007
Trade Thesis re-evaluation must create a new immutable revision / record,
not in-place overwrite.

VT-008
Historical replay requires exact refs,
policy / model versions,
and temporal semantics.
~~~

R3共通Temporal原則候補:

~~~text
Semantic Change
→ New Version

Context Change
→ New Assessment

Later Information
!= Past Decision Context

Immutable Historical Record
!= Forever Current-Use Valid

Event Time
!= Information Availability Time
!= Assessment / Decision Time
~~~

Historical Decision Reconstruction ChainをLineage横断概念として維持する。

---

## 23.7 STEP 6 — Unknown / Conflict / Dependency Review

Result:

~~~text
PASS WITH 15 INTEGRATION FINDINGS
~~~

Unknown:

~~~text
UNKNOWN != FALSE
Missing != Mismatch
Unknown != Uncertainty
Unknown existence != Criticality
Accepted Unknown != Resolved Unknown
~~~

Unknownはsource identityを保持し、下流はLayer-specific treatmentだけを追加する方向。

Conflict:

~~~text
Canonical Contradiction
!= Decision-time Competition
!= Unresolved Conflict

Opposite Direction
!= Contradiction

Conflict
!= Uncertainty
~~~

Dependency:

~~~text
Knowledge Count
!= Evidence Count

Different Knowledge ID
!= Independent Evidence

No known dependency
!= Proven independence

Unavailable dependency information
!= No dependency

Independent Convergence
requires an explicit independence basis.
~~~

Semantic RelationshipとEvidence / Research Dependencyは別。

新しい巨大Dependency Layer / Unknown Layerは現段階で追加しない。

---

## 23.8 STEP 7 — Backward Return Router Review

Result:

~~~text
PASS WITH 13 INTEGRATION FINDINGS
~~~

中心原則:

~~~text
Detection location
!= Semantic Authority
~~~

Return routingはRaw Event Typeではなく、何の意味が変わったかで決める。

統合Return:

~~~text
Research / Knowledge semantics changed
→ R2 Research / Knowledge Admission

Knowledge operational trust changed
→ Knowledge Lifecycle

Current applicability changed
→ Knowledge Applicability

Semantic relationship changed
→ Knowledge Relationship

Decision meaning changed
→ Decision Synthesis

Candidate semantics changed
→ Decision Candidate Formation

Economic context changed
→ Economic Value Re-evaluation

Capital / Portfolio only
→ R4
~~~

重要:

~~~text
Return
!= history rewind

Backward Routing
→ Forward Rebuild
~~~

過去Objectは削除・上書きせず、Current-use validityを失わせ、必要な依存Chainだけ新しく再構築する。

One Findingは複数Consumerへfan-out可能だが、Primary Semantic Ownerは1つ。

Two-Speed:

~~~text
Fast R4 Safety
!= Slow Research / Knowledge conclusion
~~~

---

## 23.9 Consolidated R3 Integration Issue List v0.1

STEP 1〜7のFindingをRoot Cause単位へ統合した。

### Priority Definition

| Priority | Meaning |
|---|---|
| CRITICAL | STEP 8 End-to-End Destruction Test前にRepair必須 |
| HIGH | Flowは動くがAuthority / Truth / Reproducibilityを壊し得るため同Repair cycleで修正 |
| MEDIUM | Semantic Coreは成立。Formal Architecture前に整理 |
| LATER | DB / Python / Physical implementationで確定可能 |

### Root Issues

| ID | Root Issue | Priority |
|---|---|---|
| R3-INT-001 | Knowledge Record / Version / Identity の正本境界 | CRITICAL |
| R3-INT-002 | R3共通Temporal Contract / Look-Ahead防止 | CRITICAL |
| R3-INT-003 | Decision Material Snapshot Contract不足 | CRITICAL |
| R3-INT-004 | Decision Candidate Contract Backfill | CRITICAL |
| R3-INT-005 | Economic Value Assessment Evaluation Availability / Sufficiency不足 | CRITICAL |
| R3-INT-006 | Knowledge Admissionの意味軸 / Authority混在 | HIGH |
| R3-INT-007 | Knowledge Relationship Canonical Ownership / Version / Temporal Contract | HIGH |
| R3-INT-008 | Unknown Identity / Treatment Model | HIGH |
| R3-INT-009 | Dependency / Independence Provenance | HIGH |
| R3-INT-010 | Decision Synthesis Result / Decision Thesis境界 | HIGH |
| R3-INT-011 | Candidate Advancement Governance / Disposition語彙 | HIGH |
| R3-INT-012 | Trade Thesis Revision / Canonical Write Boundary | HIGH |
| R3-INT-013 | Knowledge-Use Constraint Authority / Time | HIGH |
| R3-INT-014 | Backward Return RouterのR3共通Rule化 | MEDIUM |

Count:

~~~text
CRITICAL = 5
HIGH     = 8
MEDIUM   = 1
TOTAL    = 14
~~~

---

## 23.10 R3-INT-001 — Knowledge Record / Version / Identity

Repair Direction:

~~~text
Knowledge Identity
=
Knowledge系列Identity

Knowledge Record
=
特定VersionのCanonical Semantic Record

Knowledge Version
=
Knowledge RecordをVersion単位で指すLogical Identity

Version Lineage
=
Version間の履歴 / 関係
~~~

禁止:

~~~text
Knowledge Record全文
+
Knowledge Version全文
=
duplicate semantic truth
~~~

Repair Package Aの先頭で閉じる。

---

## 23.11 R3-INT-002 — Temporal Contract

Repair Direction:

~~~text
Event / Source Time
!= Information Available / Known Time
!= Assessment / Decision Time
!= Effective Time
~~~

Historical Decisionへ使用可能なのは、原則としてDecision As-Of以前にSystemが利用可能だった情報だけ。

Semantic Change / Context Change分離も共通化する。

---

## 23.12 R3-INT-003 — Decision Material Snapshot

Repair Direction:

~~~text
Decision Context
├─ Target
├─ Scope
├─ Relevant Horizon
└─ Decision As-Of
~~~

Snapshotはexact immutable refs / revisionsを固定し、floating Current参照を避ける。

---

## 23.13 R3-INT-004 — Decision Candidate Contract

Economic Value要求を上流へBackfillする。

最低意味候補:

~~~text
Decision Candidate Version
├─ Decision Thesis Ref
├─ Target
├─ Instrument
├─ Exposure Intent
├─ Candidate Objective
├─ Relevant Horizon
├─ Evaluation Baseline / Reference
├─ Preconditions
├─ Candidate-specific Invalidation Refs
├─ Critical Unknown Refs
├─ Decision Context Ref
└─ Candidate As-Of
~~~

---

## 23.14 R3-INT-005 — Evaluation Availability / Sufficiency

Economic Value Assessmentに、

~~~text
Economic Direction / Attractiveness
!= Evaluation Availability / Sufficiency
~~~

を導入する方向。

例:

~~~text
potentially positive economics
+
critical slippage unknown
=
not automatically sufficient for advancement
~~~

Exact enumはRepair時に検討し、現時点では固定しない。

---

## 23.15 R3-INT-006 — Admission Axis / Authority

現行候補:

~~~text
ADMIT
ADMIT_WITH_BOUNDARY
NEGATIVE
UNKNOWN
MERGE
SUPERSEDE_CANDIDATE
RESEARCH_REQUIRED
DEFER
REJECT
~~~

は1軸にしない。

Repair方向:

~~~text
Research Result Classification
Admission Disposition
Duplicate Handling
Relationship / Version Handling
~~~

へ分離。

Admission Assessment / Decision Authority / Canonical Knowledge Writerの境界も補強する。

---

## 23.16 R3-INT-007 — Relationship Canonical Ownership

Repair方向:

~~~text
Canonical CONTRADICTS truth
=
Knowledge Relationship owner

Knowledge Record
!= contradiction truth owner
~~~

RelationshipはExact Knowledge VersionとHistorical availabilityを追跡可能にする。

Relationship Candidate → Assessment → Canonicalization Decision → WriterのAuthority境界も検討する。

---

## 23.17 R3-INT-008 — Unknown Identity / Treatment

Unknown Source / Findingを追跡し、下流はTreatmentを追加する。

~~~text
Unknown existence
!= Criticality

Economic Value identifies unknown
↓
Candidate Advancement
accepts / waits / blocks
↓
Trade Thesis
records Accepted Unknown
~~~

Unknown Reason / Causeも意味上区別する。

---

## 23.18 R3-INT-009 — Dependency / Independence

Repair方向:

~~~text
Dependency Context
├─ Dependency Type
├─ Source Refs
├─ Materiality
├─ Known / Unknown
├─ Independence Basis [when claimed]
└─ Provenance
~~~

Independent Convergenceを名乗る場合はIndependence Basis必須。

新専用Layerの追加は保留。

---

## 23.19 R3-INT-010 — Synthesis Result / Decision Thesis

Repair方向:

~~~text
Decision Synthesis Result
↓
Decision Thesis
↓
Decision Candidate
~~~

Decision Thesis Candidateは統一候補として廃止方向。

Synthesis Resultは全体結果、Decision Thesisは個別Market Judgment。

Thesisを別Canonical Objectとして保持する場合、ResultはThesis全文複製ではなくRefを持つ。

---

## 23.20 R3-INT-011 — Candidate Advancement

Repair方向:

~~~text
PROCEED
→ Deprecated方向

ADVANCE
→ Candidate-specific advancement term

Candidate Disposition
=
ADVANCE / WAIT / ABSTAIN
~~~

Advancement Policy / Criteriaは明示・Versioned。

Candidate Advancement logicはPolicy Consumerであり、ad hoc Policy Authorではない。

---

## 23.21 R3-INT-012 — Trade Thesis Revision

Trade Thesisはimmutable reasoning record方向。

~~~text
TT-101
↓
Economic Re-evaluation
↓
TT-102
predecessor = TT-101
~~~

in-place overwriteは禁止。

Trade Thesis Formation / Adoption / Writer責任も後のRepairで明示する。

---

## 23.22 R3-INT-013 — Knowledge-Use Constraint

Repair方向:

~~~text
Knowledge-Use Constraint Candidate
↓
Constraint Authorization
↓
Authorized Knowledge-Use Constraint
~~~

最低意味:

~~~text
Target Knowledge Version
Revision
Effective Time
Expiry / Release
Authority
Provenance
~~~

Emergency Knowledge-Use Blockも同じTemporal vocabularyへ接続する。

---

## 23.23 R3-INT-014 — Return Router Common Rule

新しい万能Router Layerは追加しない。

既存Return semanticsをR3共通Ruleへ圧縮する。

~~~text
Backward Routing
→ Forward Rebuild

Detection Location
!= Semantic Authority

Historical Record
!= Mutable Current State
~~~

Upstream changeはMaterially dependentな下流だけ再構築する。

Fast Safety pathはSlow semantic reviewを待たない。

---

## 23.24 Repair Packages

14 Issueを個別にバラバラ修正せず、4 Packageへまとめる。

### Repair Package A — Knowledge Foundation

~~~text
R3-INT-001
R3-INT-006
R3-INT-007
R3-INT-013
~~~

対象:

~~~text
Admission
Knowledge Identity
Knowledge Record
Knowledge Version
Version Lineage
Knowledge Relationship
Knowledge-Use Constraint
~~~

### Repair Package B — Temporal / Reproducibility

~~~text
R3-INT-002
R3-INT-003
~~~

対象:

~~~text
Temporal vocabulary
Look-Ahead protection
Applicability
Snapshot
Historical Replay
exact refs / revisions
~~~

### Repair Package C — Decision Contract

~~~text
R3-INT-004
R3-INT-008
R3-INT-009
R3-INT-010
R3-INT-011
~~~

対象:

~~~text
Decision Synthesis
Decision Thesis
Decision Candidate
Unknown
Dependency
Candidate Advancement
~~~

### Repair Package D — Economic / Trade Exit

~~~text
R3-INT-005
R3-INT-012
R3-INT-014
~~~

対象:

~~~text
Economic Value Assessment
Evaluation Availability / Sufficiency
Trade Thesis revision
Return Router common rule
~~~

Repair order:

~~~text
Package A
↓
Package B
↓
Package C
↓
Package D
↓
Adjacent Contract Re-check
↓
STEP 8 End-to-End Destruction Test
~~~

---

## 23.25 Explicit Non-Goals

Checkpoint 016 / Integration Repairでは以下を作らない。

~~~text
New giant Dependency Layer
New Unknown architecture layer
Universal Return Router Service
DB table design
Python class design
API implementation contract
Exact enum finalization for every axis
Physical process/server separation
~~~

現在閉じる範囲:

~~~text
Meaning
Ownership
Authority
Input / Output Contract
Version
As-Of
Reference
Lineage
Current-use validity
~~~

---

## 23.26 Repair Success Gate

STEP 8へ進む前に最低限:

~~~text
1. Knowledge semantic truth has one canonical owner.

2. Version / As-Of / Information Availability are historically reproducible.

3. Decision Material Snapshot pins exact decision context and exact revisions.

4. Decision Candidate supplies all semantics Economic Value requires.

5. Economic Value separates economic attractiveness from evaluation sufficiency.

6. Unknown is never silently converted to FALSE / ZERO / 50%.

7. Dependency unknown is never silently promoted to independence.

8. Decision Synthesis Result / Decision Thesis ownership is not duplicated.

9. Trade Thesis re-evaluation never overwrites historical reasoning.

10. Return routing never rewrites history; it routes upstream and rebuilds forward.
~~~

---

## 23.27 Save / Adoption Boundary

Checkpoint 016として保存するWorking Study:

~~~text
STEP 1 Canonical Vocabulary Review
STEP 2 Responsibility / Authority Matrix
STEP 3 Object Boundary Review
STEP 4 Forward Handoff Review
STEP 5 Version / As-Of / Lineage Review
STEP 6 Unknown / Conflict / Dependency Review
STEP 7 Backward Return Router Review
R3 Integration Issue List v0.1
Repair Package A-D
Repair Success Gate
~~~

今回Formal Currentへ昇格しない。

変更しない:

~~~text
00_AI/AI_CONTEXT.md
00_HUMAN/HUMAN_MAP.md
02_ARCHITECTURE/
~~~

---

## 23.28 Checkpoint Result

Checkpoint 016:

~~~text
R3 Integration Precision Review
STEP 1-7
= COMPLETE

Root Issue Consolidation
= COMPLETE

Integration Issues
= 14

CRITICAL
= 5

HIGH
= 8

MEDIUM
= 1

Integration Repair
= NOT STARTED

Formal Current Architecture
= UNCHANGED

NEXT
=
Repair Package A — Knowledge Foundation
starting with R3-INT-001
Knowledge Identity / Knowledge Record / Knowledge Version / Version Lineage
~~~

---

# 24. Checkpoint 017 — R3 Integration Repair / Package A — Knowledge Foundation

**Date:** 2026-10-04  
**State:** SAVED / WORKING REPAIR CHECKPOINT  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction — R3 Integration Repair  
**Repair Package:** A — Knowledge Foundation  
**Issues Repaired:** R3-INT-001 / R3-INT-006 / R3-INT-007 / R3-INT-013  
**Next:** Repair Package B — Temporal / Reproducibility, starting with R3-INT-002 Temporal / Look-Ahead Contract.

## 24.1 Package A Purpose

Checkpoint 016で確定したR3 Integration Issue Listのうち、Knowledge Foundationを構成する4件を先に修正した。

~~~text
R3-INT-001
Knowledge Record / Version / Identity canonical boundary

R3-INT-006
Knowledge Admission semantic axes / authority

R3-INT-007
Knowledge Relationship canonical ownership / version / time

R3-INT-013
Knowledge-Use Constraint authority / time
~~~

目的:

> Knowledge誕生前から、Version-specific semantic truth、Version continuity、cross-Knowledge relation、operational use restrictionまでを、二重Truth・Authority混在・silent inheritance・history rewriteなしで接続する。

---

## 24.2 R3-INT-001 — Knowledge Identity / Record / Version / Lineage

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Canonical meaning:

~~~text
Knowledge Identity
=
同一Knowledge系列を束ねるStable Identity

Knowledge Record
=
特定Versionの唯一のCanonical Semantic Record

Knowledge Version
=
Knowledge Identity + Version IDで特定されるLogical Version Identity
独立した重複Semantic Bodyではない

Version Lineage
=
同一Knowledge Identity内のVersion continuity / history
~~~

基本形:

~~~text
Knowledge Identity K021
├─ Knowledge Record K021@v1
├─ Knowledge Record K021@v2
└─ Knowledge Record K021@v3
~~~

Knowledge semantic truth owner:

~~~text
Knowledge Record K021@v3
~~~

Knowledge Identity / Version Lineage / Lifecycle / ApplicabilityはKnowledge semantic bodyを重複所有しない。

Current naming refinement:

~~~text
Current Semantic Version
→ Current Canonical Knowledge Version
~~~

重要:

~~~text
Current Canonical Knowledge Version
!= ACTIVE
!= APPLICABLE
~~~

Current Canonical VersionがSUSPENDEDでもPrevious Versionへ自動Fallbackしない。

Version creation:

~~~text
Material Semantic Change
→ New Version REQUIRED

Context Change Only
→ New Assessment, NOT New Version

Evidence Update With Same Meaning
→ Validation History, NOT New Version

Lifecycle Transition
→ NOT New Version

Reactivation After RETIRED
→ Revalidation + Admission + New Version / New Identity
~~~

Version vs Relationship:

~~~text
Old semantics replaced by new semantics
→ Same Identity / New Version

Old and new semantics both independently reusable
→ New Identity + Knowledge Relationship
~~~

Same-Identity succession:

~~~text
Version Lineage
~~~

Cross-Identity formal replacement:

~~~text
SUPERSEDES Relationship
~~~

Historical consumers must pin exact Knowledge Version refs.

---

## 24.3 R3-INT-001 Additional Boundary

Admission-time Evidence TraceとLater Validation Historyを分離する。

~~~text
Knowledge Record
→ Admission Evidence / Research Trace

Later same-semantics validation
→ append-only Validation History / Research Event refs
~~~

追加EvidenceだけでKnowledge Versionを増やさない。

Non-semantic administrative correctionも不要なSemantic Version inflationを起こさない。

---

## 24.4 R3-INT-006 — Knowledge Admission Axes

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

旧Admission Decision候補:

~~~text
ADMIT
ADMIT_WITH_BOUNDARY
NEGATIVE
UNKNOWN
MERGE
SUPERSEDE_CANDIDATE
RESEARCH_REQUIRED
DEFER
REJECT
~~~

は複数意味軸を混在させていたため、次へ分離した。

~~~text
1. Research Result Classification
2. Knowledge Worthiness
3. Canonicalization Need / Identity-Version Assessment
4. Admission Disposition
~~~

重要:

~~~text
Research Result Classification
!= Knowledge Worthiness

Knowledge Worthiness
!= Admission Disposition

NEGATIVE
!= REJECT

UNKNOWN
!= DEFER

Failure Boundary presence
!= Admission Disposition
~~~

ADMIT_WITH_BOUNDARYはCanonical admission stateから外す方向。

~~~text
Admission Disposition = ADMIT
+
Knowledge Semantic Body contains Failure Boundary
~~~

MERGE / SUPERSEDE_CANDIDATEもAdmission Dispositionから外す。

---

## 24.5 Knowledge Worthiness

Knowledge Worthinessの中心問い:

> Validated Research Resultが、別時点・別Decisionでも再利用可能なKnowledgeとして残す価値を持つか。

Conceptual axis:

~~~text
WORTHY
NOT_WORTHY
UNDETERMINED
~~~

Exact enumは後。

SUPPORTEDでもNOT_WORTHYになり得る。

NEGATIVE / UNKNOWN Research ResultでもWORTHYになり得る。

---

## 24.6 Canonicalization Need

Existing Knowledge Comparison後に、何をCanonical化する必要があるかを分ける。

~~~text
NEW_KNOWLEDGE_SEMANTICS
REPLACEMENT_SEMANTICS
VALIDATION_ONLY
UNRESOLVED
~~~

意味:

~~~text
NEW_KNOWLEDGE_SEMANTICS
→ New Knowledge Identity candidate

REPLACEMENT_SEMANTICS
→ Same Identity / New Version candidate

VALIDATION_ONLY
→ Existing exact VersionのValidation Historyへ
   New Knowledge Versionを作らない

UNRESOLVED
→ DEFER / RESEARCH_REQUIRED candidate
~~~

Exact enum名は後。

---

## 24.7 Admission Disposition

Minimal canonical direction:

~~~text
ADMIT
DEFER
RESEARCH_REQUIRED
REJECT
~~~

ADMIT:

~~~text
Canonicalization Pathを承認
!= Canonical Record already exists
~~~

REJECT:

~~~text
このCandidateをCanonical KnowledgeへMaterializeしない
!= Research Result false
!= Research Result delete
~~~

Later reconsiderationはhistorical decision updateではなくNew Admission Assessment / Decision。

---

## 24.8 Admission Authority

Repair後:

~~~text
Validated Research Result
↓
Knowledge Worthiness Assessment
↓
Semantic Extraction
↓
Existing Knowledge Comparison
↓
Canonicalization Need
↓
Identity / Version Proposal
+
Relationship Candidate Detection
↓
Knowledge Candidate
↓
Admission Assessment
↓
Admission Proposal
↓
Knowledge Admission Governance
↓
Authorized Admission Decision
↓
Knowledge Admission Writer
↓
Canonical Knowledge Identity / Record / Version Lineage
~~~

Authority split:

~~~text
Assessment
!= Decision
!= Canonical Write
~~~

Knowledge Admission GovernanceはCanonical KnowledgeとしてMaterializeするかを決定する。

Knowledge Admission WriterはAuthorized DecisionだけをMaterializeする。

Writerはstale preconditionを勝手に補正しない。

~~~text
Expected parent / previous state mismatch
→ WRITE REJECTED
→ Re-assessment
~~~

Authorized ADMIT
!= Canonical Record Exists.

---

## 24.9 Knowledge Candidate Boundary

Knowledge CandidateはCanonical前のProposed Semantic Package。

持てる:

~~~text
Source Validated Research Result Ref
Proposed Claim / Type / Scope / Conditions / Horizon
Proposed Effect / Failure Boundary / Constraint Semantics
Evidence / Research refs
Proposed Uncertainty
Worthiness Assessment Ref
Existing Knowledge Comparison Ref
Identity / Version Proposal
Relationship Candidate refs
Provenance
~~~

持たない:

~~~text
Canonical Knowledge ID assignment
Canonical Version assignment
Canonical Relationship truth
Lifecycle Disposition
Applicability
Economic Value
Trade Direction
~~~

---

## 24.10 R3-INT-007 — Knowledge Relationship Canonical Ownership

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Canonical semantic relation truthのsole owner:

~~~text
Canonical Knowledge Relationship
~~~

Knowledge Recordの:

~~~text
Known Contradictions
~~~

はCanonical-owned fieldとして廃止方向。

UI / Searchでのcontradiction一覧はDerived Relationship Viewとして生成する。

---

## 24.11 Exact-Version Relationship

Canonical Knowledge Relationshipは原則Exact Knowledge Versions間で定義する。

~~~text
K021@v3
CONTRADICTS
K044@v2
~~~

Identity-level:

~~~text
K021 CONTRADICTS K044
~~~

はCanonical source truthではなくDerived / Summary View。

New Knowledge VersionへOld Relationshipを自動継承しない。

~~~text
K021@v2 CONTRADICTS K044@v1
+
K021@v3 admitted

!=
K021@v3 automatically CONTRADICTS K044@v1
~~~

New Relationship Candidate / Assessmentが必要。

---

## 24.12 Canonical Relationship Set Refinement

Working canonical relation direction:

~~~text
EQUIVALENT
SPECIALIZES
REFINES
EXTENDS
CONTRADICTS
SUPERSEDES
~~~

DUPLICATE_CANDIDATEはCanonical Relationship Typeから外す。

~~~text
Duplicate suspicion
!= Canonical EQUIVALENT
~~~

DUPLICATE_CANDIDATE等はCandidate / Finding側。

Same-Identity successionにはSUPERSEDESを使わずVersion Lineageを使う。

---

## 24.13 Relationship Authority

Repair後:

~~~text
Candidate Generation
↓
Relationship Candidate
↓
Relationship Assessment
↓
Relationship Proposal
↓
Knowledge Relationship Governance
↓
Authorized Relationship Decision
↓
Knowledge Relationship Writer
↓
Canonical Knowledge Relationship
~~~

Candidate generator can include:

~~~text
Admission
R2
AI
Python rule
Similarity Search
Applicability Finding
Lifecycle Assessment
Human Review
~~~

しかし:

~~~text
Candidate Generator
!= Canonical Relationship Authority
~~~

Canonical CONTRADICTS:

~~~text
!= Truth Winner
!= Lifecycle Transition
!= Decision-time Winner
~~~

---

## 24.14 Relationship Temporal / Historical Boundary

Relationship-specific temporal rule:

~~~text
Relationship Record Creation Time
!= Relationship Availability To Decision
~~~

Past Decision Contextへ、Later Canonical Relationshipを逆流させない。

~~~text
09:10 Snapshot S1
09:30 Relationship becomes canonically available

→ S1 does not contain later Relationship
~~~

Decision Material Snapshotはfloating relationship summaryではなくExact Relationship Refをpinする。

Relationship correctionもhistorical in-place mutationしない。

~~~text
Old canonical assertion
↓
new assessment / decision
↓
new current-use relationship assertion / correction lineage
~~~

Exact temporal vocabulary / field namesはR3-INT-002で統合する。

---

## 24.15 Relationship Boundary vs Other Domains

~~~text
Knowledge Relationship
!= Knowledge Record

Knowledge Relationship
!= Version Lineage

Knowledge Relationship
!= Knowledge Graph

Knowledge Relationship
!= Evidence / Research Dependency

Knowledge Relationship
!= Lifecycle Authority
~~~

Knowledge GraphはDerived / rebuildable。

Canonical CONTRADICTSはResearch / Lifecycle Trigger候補を生成できるが、Relationship authority自身がそれらのStateを変更しない。

---

## 24.16 R3-INT-013 — Knowledge-Use Constraint

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Definition:

> 特定のExact Knowledge Versionについて、そのKnowledge semanticsやLifecycle Dispositionを変更することなく、明示されたUsage ScopeにおけるDecision Material利用を制限するAuthorized Operational Restriction。

重要:

~~~text
Knowledge-Use Constraint
!= Knowledge Condition
!= Failure Boundary
!= Lifecycle Disposition
!= Semantic Applicability
!= R4 Capital Constraint
!= Constraint Knowledge
~~~

---

## 24.17 Exact-Version Constraint Target

Canonical Knowledge-Use Constraintは原則Exact Knowledge Versionを対象とする。

~~~text
Target = K021@v3
~~~

Identity-wide concernがある場合でも、historical canonical constraint recordをfloating:

~~~text
K021 current forever
~~~

にしない。

Identity-level policy / findingから必要なExact-Version Constraint Candidateを生成する。

New VersionへOld Constraintを自動継承しない。

---

## 24.18 Usage Scope

Constraintは単なるBLOCKED stateではなく、何の利用を制限するかを追跡可能にする。

例:

~~~text
Live Decision Material use blocked
Research reference allowed
Audit / explanation allowed
~~~

Exact enumは後。

---

## 24.19 Constraint Authority

Repair後:

~~~text
Constraint Finding / Trigger
↓
Knowledge-Use Constraint Candidate
↓
Constraint Assessment
↓
Constraint Proposal
↓
Knowledge-Use Constraint Governance
↓
Authorized Constraint Decision
↓
Knowledge-Use Constraint Writer
↓
Canonical Authorized Knowledge-Use Constraint
~~~

Candidate generator
!= Constraint Authority.

WriterはAuthorized Decisionだけをmaterializeする。

---

## 24.20 Constraint Temporal / Release Boundary

Canonical constraint logical meaning候補:

~~~text
Constraint ID
Target Exact Knowledge Version Ref
Usage Scope
Restriction Semantics
Reason / Finding Refs
Authorization Decision Ref
Revision / Lineage
Decision Time
Effective Time
Optional Expiry
Release / Review Condition
Authority
Provenance
~~~

Exact temporal field namingはR3-INT-002へ送る。

重要:

~~~text
Constraint Decision Time
!= Constraint Effective Time

Constraint Release
!= Historical Constraint Deletion

Later Release
!= Past Decision Context Rewrite

Constraint Release
!= Automatic Applicability Reactivation
~~~

---

## 24.21 Emergency Knowledge-Use Block

既存Fast Safety設計をAuthority付きで補強。

~~~text
Verified Hard Integrity Finding
↓
Pre-authorized Emergency Constraint Policy
↓
Authorized Fast Constraint Activation
↓
New Decision Materialから即時除外
+
parallel
Lifecycle Fast Suspension Path
~~~

重要:

~~~text
Fast
!= Uncontrolled

Emergency Knowledge-Use Block
!= Lifecycle SUSPENDED

Fast Constraint Activation
!= Fast RETIRE

Emergency Block
!= R4 direct EXIT
~~~

---

## 24.22 Constraint vs New Version

~~~text
K021@v3
Constraint C1
↓
K021@v4 admitted
~~~

C1をv4へsilent carry-forwardしない。

必要なら:

~~~text
v4
↓
new Constraint Candidate
↓
new Assessment / Authorization
~~~

重要:

~~~text
Constraint inheritance
!= Constraint re-evaluation
~~~

---

## 24.23 Constraint vs Decision Material

Constraintが有効:

~~~text
Semantic Applicability = APPLICABLE
Knowledge-Use Constraint = EFFECTIVE
Decision Material Eligibility = BLOCKED
~~~

Semantic Applicabilityを書き換えない。

Blocked-but-readable KnowledgeはTRACE ONLYにできるが、Decision SynthesisのACTIVE INPUTとして影響させない。

Constraint Store / Constraint Information unavailableの場合:

~~~text
Unavailable
!= No Constraint
~~~

Materialならeligibility uncertaintyとして扱う。

---

## 24.24 Package A Cross Check — Canonical Truth Ownership

| Truth | Canonical Owner |
|---|---|
| Knowledge系列Identity | Knowledge Identity |
| Exact Version Semantic Body | Knowledge Record K021@v3 |
| Same-Identity Version continuity | Version Lineage |
| Cross-Knowledge Semantic Relation | Knowledge Relationship |
| Knowledge operational treatment | Knowledge Lifecycle |
| Knowledge usage restriction | Knowledge-Use Constraint |
| Current-market semantic usability | Applicability |

Result:

~~~text
Duplicate canonical ownership
= NONE FOUND
~~~

---

## 24.25 Package A Cross Check — Governance Pattern

Package AはLifecycle設計と同じ責任分離へ揃った。

~~~text
Admission:
Candidate / Assessment
→ Governance
→ Writer

Relationship:
Candidate / Assessment
→ Governance
→ Writer

Knowledge-Use Constraint:
Candidate / Assessment
→ Governance
→ Writer

Lifecycle:
Trigger / Assessment
→ Governance
→ Writer
~~~

Common Principle:

~~~text
Generate / Detect
!= Assess
!= Decide / Authorize
!= Canonical Write
~~~

Separate Responsibility
!= Separate Process / Server.

---

## 24.26 Package A Cross Check — Version / Inheritance

Common rule:

~~~text
New Knowledge Version
does NOT automatically inherit:

- Old Lifecycle assumptions
- Old Applicability assessment
- Old Knowledge Relationship
- Old Knowledge-Use Constraint
~~~

Each downstream domain re-evaluates exact new Version as required.

Current Canonical VersionがSUSPENDED / uninitializedでもPrevious Versionへのsilent fallbackは禁止。

---

## 24.27 Package A Adjacent Handoff Clarifications

### PA-HO-001 — Admission → Lifecycle Initialization

Successful Canonical Admission後:

~~~text
Newly Admitted Knowledge Version
↓
Lifecycle Initialization
~~~

Admission WriterがLifecycle Dispositionを勝手に決めない。

Initial Lifecycle Disposition authorityはLifecycle側。

### PA-HO-002 — Current Canonical Version Materialization

NEW_VERSIONをAdmission Governanceが承認した場合:

~~~text
Admission Governance
=
semantic canonicalization decision owner

Knowledge Admission Writer
=
Authorized Decisionに従い
Knowledge Record creation
+
Version Lineage update
+
Current Canonical Knowledge Version Ref update
をmaterialize
~~~

LifecycleはCurrent Canonical Version選択Authorityではない。

---

## 24.28 Package A Destruction Result

以下を破壊確認:

~~~text
Negative Research Result admitted as reusable Knowledge
Unknown Research Result admitted as reusable Knowledge
Failure Boundary付きKnowledge
Validation-only Result
Threshold correction
Specialized reusable Knowledge
Duplicate suspicion
Stale Admission Writer precondition
New Version after old canonical relationship
False contradiction correction
Relationship store unavailable
Same-Identity version succession
Cross-Identity SUPERSEDES
ACTIVE + APPLICABLE but Knowledge-Use blocked
Constraint release
Constraint store outage
Emergency integrity block
Constraint reason becoming semantic discovery
New Version while old Version constrained
~~~

Result:

~~~text
R3-INT-001
= PASS

R3-INT-006
= PASS

R3-INT-007
= PASS

R3-INT-013
= PASS

Package A Cross-Object Ownership
= PASS

Authority Separation
= PASS

Version Boundary
= PASS

Historical Immutability
= PASS

Adjacent Contract
= PASS WITH PA-HO-001 / PA-HO-002 CLARIFIED
~~~

Blocking Issue:

~~~text
NONE
~~~

---

## 24.29 Package A Canonical Invariant Summary

~~~text
A-KF-01
One canonical semantic fact has one canonical owner.

A-KF-02
Knowledge Record is the semantic truth owner for one exact Version.

A-KF-03
Knowledge Version does not duplicate the Knowledge Record semantic body.

A-KF-04
Same-Identity evolution uses Version Lineage.

A-KF-05
Cross-Identity semantics use Knowledge Relationship.

A-KF-06
Knowledge Candidate != Canonical Knowledge Version.

A-KF-07
Admission Assessment != Admission Decision != Canonical Write.

A-KF-08
Relationship Candidate != Canonical Relationship.

A-KF-09
DUPLICATE_CANDIDATE is not a canonical relation type.

A-KF-10
Relationship is exact-Version scoped and not silently inherited.

A-KF-11
Known Contradiction truth is not owned by Knowledge Record.

A-KF-12
Knowledge-Use Constraint is operational permission, not Knowledge semantics.

A-KF-13
Knowledge-Use Constraint targets exact Knowledge Version.

A-KF-14
Constraint release does not rewrite historical Decision Context.

A-KF-15
New Version does not silently inherit old Constraint.

A-KF-16
Current Canonical Version != ACTIVE != APPLICABLE.

A-KF-17
Current Canonical Version failure does not cause automatic previous-Version fallback.

A-KF-18
Historical consumers pin exact Version / Relationship / Constraint refs.

A-KF-19
Fast Safety does not grant fast semantic mutation authority.

A-KF-20
Canonical Writer executes authorized semantics; it does not invent them.
~~~

---

## 24.30 Save / Adoption Boundary

Checkpoint 017 saves Package A as Working Repair only.

Formal Current remains unchanged.

Do not modify:

~~~text
00_AI/AI_CONTEXT.md
00_HUMAN/HUMAN_MAP.md
02_ARCHITECTURE/
~~~

Physical implementation remains out of scope:

~~~text
DB tables
Python classes
API schemas
process/server boundaries
final enum naming
~~~

---

## 24.31 Checkpoint Result

~~~text
Checkpoint 017
R3 Integration Repair
Package A — Knowledge Foundation
= SAVED WORKING REPAIR

R3-INT-001
= REPAIRED / WORKING

R3-INT-006
= REPAIRED / WORKING

R3-INT-007
= REPAIRED / WORKING

R3-INT-013
= REPAIRED / WORKING

Blocking Issue
= NONE

Formal Current Architecture
= UNCHANGED

NEXT
=
Repair Package B — Temporal / Reproducibility

FIRST TARGET
=
R3-INT-002
Temporal / Look-Ahead Contract
~~~

---

# 25. Checkpoint 018 — R3 Integration Repair / Package B — Temporal / Reproducibility

**Date:** 2026-10-04  
**State:** SAVED / WORKING REPAIR CHECKPOINT  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction — R3 Integration Repair  
**Repair Package:** B — Temporal / Reproducibility  
**Issues Repaired:** R3-INT-002 / R3-INT-003  
**Next:** Repair Package C — Decision Contract, starting with R3-INT-004 Decision Candidate Contract Backfill.

## 25.1 Package B Purpose

Checkpoint 016で確定したCRITICAL issueのうち、R3のTemporal IntegrityとDecision Input Boundaryを構成する2件を修正した。

~~~text
R3-INT-002
R3 common Temporal / Look-Ahead Contract

R3-INT-003
Decision Material Snapshot Contract
~~~

目的:

> 後から得た情報を過去Decisionへ逆流させず、「その時点で市場理解OSが何を知ることができ、何をDecision Inputとして固定したか」をExact Version / Revision / Policy / Modelまで含めて再現可能にする。

---

## 25.2 R3-INT-002 — Temporal Contract

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

R3共通Temporal Vocabularyの中心分離:

~~~text
Event / Domain Time
!= Source Available Time
!= System Information Available Time
!= As-Of / Information Cutoff
!= Assessment / Decision Time
!= Effective Time
!= Record / Materialization Time
~~~

各Objectがすべての時刻を持つ必要はない。

ただし、異なる意味の時刻を同じtimestampとして扱わない。

---

## 25.3 Event / Domain Time vs Information Availability

Event / Domain Time:

> 現実世界で出来事・値・状態がいつのものか。

System Information Available Time:

> 市場理解OSがその情報をDecision Inputとして実際に利用可能になった最初の時刻。

Original DecisionのHistorical EligibilityはEvent Timeだけで決めない。

~~~text
Event Time <= Decision As-Of
だけでは不十分

Material Input System Available Time
<= Information Cutoff
が必要
~~~

例:

~~~text
ETF Event Time
09:58

System Available
10:03

Decision / Cutoff
10:00

→ Original Decision Inputとして使用不可
~~~

---

## 25.4 Source Available vs System Available

外部Sourceが公開済みでも、市場理解OSがまだ取得 / 検証できていなければOriginal Decisionには利用できない。

~~~text
Source Available Time
!= System Information Available Time
~~~

Historical Decision Reconstructionでは、原則としてSystem Information Available Timeを基準にする。

---

## 25.5 As-Of / Information Cutoff / Decision Time / Effective Time

As-Of:

> どの時点の世界を評価対象にしているか。

Information Cutoff:

> Assessment / Decisionへ使用可能な情報の最終Availability時刻。

Assessment / Decision Time:

> 評価またはAuthority Decisionが実際に行われた時刻。

Effective Time:

> 承認されたState / Restriction / PolicyがOperationalに効き始める時刻。

重要:

~~~text
Decision Time
!= Effective Time

Retroactive Effective Semantics
!= Retroactive Information Availability
~~~

Later Decisionで「過去からeffectiveだった」と判断しても、Past Original Decisionが当時その情報を知っていたことにはしない。

---

## 25.6 Historical Information Eligibility Rule

Original Decision用のMaterial Inputは原則:

~~~text
input.system_available_at
<= snapshot.information_cutoff
~~~

を満たす。

通常:

~~~text
information_cutoff
<= decision_as_of
~~~

を基本とする。

Event Time aloneではNo-Look-Aheadを保証しない。

---

## 25.7 Derived Information Availability

Derived informationはMaterial dependencyより先にAvailableになれない。

~~~text
derived_available_at
>= max(material_input_available_at)

and

derived_available_at
>= calculation / validation completion
~~~

対象候補:

~~~text
Feature
Market Context
Research Result
Knowledge Candidate
Knowledge Record
Knowledge Relationship
Applicability Assessment
Economic Value Assessment
~~~

Feature label time
!= Feature availability time.

Future-window featureはEarlier Decisionへ使わない。

---

## 25.8 Data Revision / Correction

Later correctionはPast Decisionが当時利用したRevisionを上書きしない。

例:

~~~text
10:03
Revision 1 = 100

10:10
Decision

11:00
Revision 2 = 80
~~~

Historical Original Decision Replay:

~~~text
Revision 1
~~~

Retrospective analysis:

~~~text
Revision 2
may be used
~~~

重要:

~~~text
Corrected Data
!= Data Known Earlier
~~~

---

## 25.9 Historical Reconstruction vs Retrospective Analysis

Historical Decision Reconstruction:

> 当時の市場理解OSが何を知り、どのPolicy / Model / Knowledge / Relationship / Constraintで判断したかを再現する。

Retrospective / Counterfactual Analysis:

> Later Knowledge / corrected data / later Model等を使って、過去を現在の視点で再評価する。

重要:

~~~text
Historical Reconstruction
!= Retrospective Analysis
~~~

Later Knowledgeを使った分析をOriginal Decision Contextとして扱わない。

---

## 25.10 Package A Temporal Handoff

Package Aと時間契約を接続。

Admission:

~~~text
Authorized ADMIT
!= Canonical Knowledge Available

Admission Governance Decision
→ Writer
→ successful canonical materialization
→ Knowledge becomes decision-available
~~~

Relationship:

~~~text
Relationship Decision
!= Relationship Available To Decision
~~~

Constraint:

~~~text
Constraint Decision Time
!= Constraint Effective Time
~~~

Lifecycle:

~~~text
Later Lifecycle Decision
!= Past Decision Context
~~~

Canonical authorizationとdecision-availabilityを混同しない。

---

## 25.11 Model / Policy Temporal Integrity

Historical replayはDataだけでなくModel / Policy Versionも当時利用可能だったものへ固定する。

対象例:

~~~text
Snapshot Assembly Policy
Relationship Assessment Policy
Candidate Advancement Policy
Economic Model
Slippage Model
Risk Policy
~~~

Later Model / PolicyはOriginal Decision Reconstructionへ逆流させない。

---

## 25.12 Temporal Unknown

~~~text
Missing Availability Time
!= Zero-Latency Availability

Temporal Availability Unknown
!= Historically Available
~~~

Availability Timeを推定する場合は推定であることとUncertaintyを保持する。

Clock / source timing integrityが怪しい情報をperfectly alignedとして扱わない。

---

## 25.13 R3-INT-002 Core Invariants

~~~text
TC-01 Event / Domain Time != Information Available Time.
TC-02 Source Available Time != System Information Available Time.
TC-03 As-Of != Assessment / Decision Time.
TC-04 Decision Time != Effective Time.
TC-05 Record / Materialization Time != Domain Event Time.
TC-06 Historical input requires Information Available Time <= Information Cutoff.
TC-07 Event Time <= Decision As-Of alone is insufficient.
TC-08 Later-arriving information must not rewrite past Decision Context.
TC-09 Later correction must not replace the revision originally available.
TC-10 Historical Reconstruction != Retrospective Analysis.
TC-11 Historical Reconstruction uses then-available Data / Knowledge / Relationship / Constraint / Model / Policy.
TC-12 Later Model / Policy must not appear historically available.
TC-13 Derived information cannot be available before material dependencies.
TC-14 Feature label time != Feature availability time.
TC-15 Future-window features cannot influence earlier decisions.
TC-16 Authorized Decision != Canonical Object Available.
TC-17 Canonical availability begins only after successful materialization unless explicitly defined otherwise.
TC-18 Current Canonical Version is resolved relative to explicit time context.
TC-19 Later Knowledge Version must not rewrite historical consumers.
TC-20 Later Relationship must not rewrite Past Decision Context.
TC-21 Later Constraint release must not rewrite Past Decision Context.
TC-22 Later Lifecycle Decision must not rewrite Past Decision Context.
TC-23 Retroactive Effective Time != Retroactive Information Availability.
TC-24 Original Decision Reconstruction uses what the system could know.
TC-25 Missing Availability Time != zero-latency availability.
TC-26 Temporal Availability Unknown remains Unknown.
TC-27 Snapshot requires explicit As-Of / Information Cutoff.
TC-28 Snapshot inputs are exact revisions / versions.
TC-29 Snapshot assembly must not mix moving Current state.
TC-30 Decision Synthesis consumes sealed Snapshot, not moving Current inputs.
TC-31 Candidate As-Of != Economic Evaluation As-Of.
TC-32 Economic Evaluation respects Market / Cost input availability.
TC-33 Historical immutable object != forever current-use valid.
TC-34 Semantic Change → New Version.
TC-35 Context Change → New Assessment.
TC-36 No-Look-Ahead is a cross-cutting integrity rule.
TC-37 Confirmed temporal leakage may trigger fast safety but not historical rewrite.
~~~

---

## 25.14 R3-INT-003 — Decision Material Snapshot Contract

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Definition:

> 特定Decision Contextについて、特定Decision As-Of / Information Cutoffまでに市場理解OSが利用可能だったMarket Context、Exact Knowledge Versions、Lifecycle、Applicability、Knowledge-Use Constraints、Canonical Relationships、Dependency / Unknown Context、ならびに重要なExcluded / Blocked TraceをExact Referenceで固定し、Decision Synthesisへ渡すImmutable Decision Input Boundary。

Decision Material Snapshot:

~~~text
!= Decision Output
!= Knowledge Pool
!= Raw Data Warehouse
!= Trade Thesis
~~~

---

## 25.15 Decision Context

Snapshotより先にDecision Contextを固定する。

最低意味:

~~~text
Decision Context
├─ Target
├─ Scope
├─ Relevant Horizon
├─ Decision As-Of
└─ Decision Purpose / Question Ref
~~~

Decision Context
!= Current Market Context.

Material Target / Scope / Horizon change
→ New Decision Context + New Snapshot.

---

## 25.16 Snapshot Temporal Header

Snapshotは最低意味として:

~~~text
Decision As-Of
Information Cutoff
Snapshot Sealed At
~~~

を持つ。

重要:

~~~text
Decision As-Of
!= Information Cutoff
!= Snapshot Sealed At
~~~

Sealまでに到着した情報全部を入れるのではなく、Information Cutoff以前にAvailableだった情報だけをOriginal Snapshotへ入れる。

---

## 25.17 Snapshot Logical Blocks

Working structure:

~~~text
Decision Material Snapshot
│
├─ A. Snapshot Identity / Decision Context
├─ B. Market Context Boundary
├─ C. ACTIVE Decision Materials
├─ D. Cross-Knowledge Context
├─ E. TRACE ONLY / Excluded / Blocked / Unknown Trace
└─ F. Snapshot Integrity / Seal Trace
~~~

Logical structureでありDB Table数ではない。

---

## 25.18 Block A — Identity / Decision Context

候補:

~~~text
Snapshot ID
Decision Context Ref
Target
Scope
Relevant Horizon
Decision As-Of
Information Cutoff
Snapshot Sealed At
Snapshot Assembly / Eligibility Policy Ref
Optional predecessor Snapshot Ref
Optional rebuild reason
~~~

Historical replayのため、当時のAssembly / Selection Policyを追跡可能にする。

---

## 25.19 Block B — Market Context

SnapshotはMarket Data全文を複製しない。

Exact Context / Observation refs、Data Quality / Freshness / Temporal integrity refsを保持する。

各Material Inputは:

~~~text
available_at <= information_cutoff
~~~

を満たす。

Latest-value collection
!= time-consistent Decision Context.

---

## 25.20 Block C — ACTIVE INPUT

ACTIVE INPUTはDecision Thesisへ実質Influenceしてよい材料のみ。

Logical material:

~~~text
Exact Knowledge Version Ref
Lifecycle Revision / Event Ref
Applicability Assessment Ref
Knowledge-Use Constraint Refs
Decision Material Eligibility Ref / Result
Material Boundary Status Ref
Material Unknown Refs
Input Role = ACTIVE INPUT
~~~

Temporal availabilityだけではACTIVE INPUTにならない。

~~~text
Temporally Available
!= Influence Eligible
~~~

Lifecycle / Applicability / Constraint / Eligibilityを通る。

---

## 25.21 Decision Material Eligibility Authority

Decision Material EligibilityはPre-Decision Knowledge Applicability / Use-Permission pipelineの最終利用可否Assessment。

~~~text
Lifecycle Eligibility
↓
Scope
↓
Condition Match
↓
Failure Boundary
↓
Semantic Applicability
↓
Knowledge-Use Constraint
↓
Decision Material Eligibility
~~~

Snapshot AssemblerはEligibilityを勝手に再判断しない。

~~~text
Snapshot Assembler
!= Decision Material Eligibility Authority
~~~

---

## 25.22 Block D — Cross-Knowledge Context

候補:

~~~text
Exact Canonical Relationship Refs
Scope / Horizon overlap context
Contradiction context
Evidence / Research Dependency refs
Data / Feature Dependency refs
Mechanism Dependency refs
Unknown Dependency refs
Independence Basis refs [when claimed]
~~~

SynthesisがCurrent Relationship / Dependency Storeへsilent re-queryしなくて済むようにSnapshotへ必要Contextを固定する。

---

## 25.23 Block E — ACTIVE INPUT vs TRACE ONLY

ACTIVE INPUT:

> Thesis Support / OppositionへInfluenceしてよい。

TRACE ONLY:

> Audit / Explanation / Sufficiency / Findingでは参照可能だが、Thesis Support / Oppositionの実質Influenceとして使わない。

重要:

~~~text
Readable
!= Influence-Eligible

TRACE ONLY
may affect Synthesis Sufficiency

but

TRACE ONLY
must not become directional support / opposition
~~~

Blocked-but-readable Knowledgeを反対票 / 賛成票にしない。

---

## 25.24 Excluded / Blocked Trace

Materialに関係したが利用しなかったものは理由を残す。

候補:

~~~text
Lifecycle Ineligible
Scope Mismatch
Semantic NOT_APPLICABLE
Semantic Applicability UNDETERMINED
Knowledge-Use Constraint BLOCKED
Decision Material Eligibility UNDETERMINED
Applicability stale
Required data unavailable
Relationship context unavailable
Constraint context unavailable
Temporal eligibility failed
Outside Decision Context
Integrity failure
~~~

ただしEntire Knowledge PoolをSnapshotへ保存しない。

Decision-relevant candidate setのうちMaterialだったものを対象とする。

Retrieval Miss
!= Explicit Exclusion.

---

## 25.25 Epistemic Unknown vs Snapshot Integrity Unknown

Epistemic Unknown:

> Market / Knowledgeについて分からない。

Snapshot Integrity Unknown:

> 何をDecision Inputとして使ったか正しく固定できない。

重要:

~~~text
Epistemic Unknown
!= Snapshot Integrity Failure
~~~

Exact AssessmentとしてUnknownを保持できるならStructurally valid SnapshotはSeal可能。

Exact Version / Constraint revision / temporal eligibility等がMaterialに解決不能ならSnapshot Integrity Problem。

---

## 25.26 Block F — Snapshot Integrity / Seal

最低確認候補:

~~~text
Temporal Eligibility Check
Exact Reference Resolution Check
Knowledge Version Consistency
Lifecycle Revision Resolution
Constraint Resolution
Relationship Context Availability
Market Context Time Consistency
Selection / Coverage Integrity
No-Look-Ahead Check
Assembly Policy Ref
Seal Result / Reason Trace
~~~

Snapshot SealはSemantic Truth判断ではない。

---

## 25.27 Snapshot Assembler / Sealer Authority

Logical responsibilities:

~~~text
Decision Material Snapshot Assembler
=
Decision Context + authoritative upstream assessmentsから
exact refsを収集しSnapshot Candidateを構成

Snapshot Integrity Gate / Sealer
=
Temporal integrity / exact refs / no-look-ahead /
required block completenessを確認しImmutable SnapshotをSeal
~~~

重要:

~~~text
Snapshot Sealer
=
Integrity Authority

Snapshot Sealer
!= Knowledge / Relationship / Lifecycle / Applicability Authority
~~~

Separate logical responsibility
!= Separate process / server.

---

## 25.28 Snapshot Seal vs Decision Sufficiency

Package B cross-checkで明示。

~~~text
PB-HO-001
Snapshot Seal Success
!= Decision Sufficiency
~~~

Seal成功はInput BoundaryがStructurally validという意味。

Critical Unknownや重要Material unavailableによりDecision SynthesisがINCONCLUSIVEになることは可能。

---

## 25.29 Snapshot Immutability / Current-Use Validity

Sealed SnapshotはImmutable。

~~~text
Sealed Snapshot
→ no in-place Current update
~~~

Later:

~~~text
Lifecycle change
Constraint activation / release
Knowledge Version change
Material Relationship change
Market shock
Context freshness expiry
Integrity finding
~~~

があってもSnapshot本文を書き換えない。

重要:

~~~text
Snapshot Historical Integrity
!= Snapshot Current-Use Validity
~~~

Current-use validityは別Assessmentとして扱う方向。

Materially staleなら:

~~~text
Old Snapshot remains Historical
↓
REBUILD_REQUIRED
↓
New Snapshot
~~~

Any update
!= automatic rebuild.

Material dependencyを確認する。

---

## 25.30 Decision Synthesis Handoff

~~~text
Sealed Decision Material Snapshot
↓
Current-Use Validity Gate
↓
Decision Synthesis
~~~

Decision SynthesisはSnapshotをDecision Input Boundaryとして使い、Current Knowledge / Relationship / Constraint / Market stateをsilent re-queryしてDecision Influenceへ混ぜない。

Synthesis途中でMaterial invalidationが起きた場合:

~~~text
Historical Snapshot mutation
= NO

Current synthesis continuation
= validity handling

Materially stale
→ New Snapshot
→ New Synthesis
~~~

Decision Synthesis ResultはExact Snapshot Refを持つ。

---

## 25.31 Original Snapshot Replay vs Historical Reconstruction

Package B cross-checkで明示。

~~~text
PB-HO-002
Original Snapshot Replay
!= Historical Snapshot Reconstruction
~~~

Original Snapshot Replay:

> 当時実際にSealされたSnapshotを読む。

Historical Reconstruction:

> Original Snapshotが存在しない場合、当時利用可能だったimmutable revisions / policy / cutoffから後で再構成する。

Reconstructed objectをOriginal Snapshotと偽らない。

Retrospective Analysisはさらに別。

---

## 25.32 Exact Reference Requirement

Package B cross-checkで強化。

~~~text
PB-HO-003
Exact Reference
must resolve to
immutable / historically reconstructable revision.
~~~

対象:

~~~text
Knowledge Version
Relationship
Lifecycle Event / Revision
Constraint
Applicability Assessment
Market Context
Policy
Model
~~~

Mutable pointer:

~~~text
current_btc_context
current_K021
~~~

はHistorical Exact Refではない。

---

## 25.33 Package B End-to-End Flow

~~~text
Event / Information
↓
System Information Availability
↓
Temporal Eligibility
available_at <= cutoff
↓
Exact Version / Revision Resolution
↓
Lifecycle / Applicability / Constraint / Relationship
↓
Decision Material Eligibility
↓
Snapshot Assembly
↓
Integrity / No-Look-Ahead Validation
↓
Snapshot Seal
↓
Current-Use Validity Gate
↓
Decision Synthesis
↓
Decision Synthesis Result
references exact Snapshot
↓
Historical storage
~~~

Later audit:

~~~text
Original Snapshot exists?
├─ YES
│   → Original Snapshot Replay
│
└─ NO
    → Historical Reconstruction
       from then-available immutable revisions
       + original policy / cutoff
~~~

Separate branch:

~~~text
Retrospective Analysis
→ may use later Knowledge / Model / corrected data
→ must not be represented as Original Decision Context
~~~

---

## 25.34 Package B Destruction Review

Cases checked:

~~~text
Delayed ETF information
Future-window feature
Later data correction
Later Model / Policy
Later Relationship
Retroactive Lifecycle decision
Constraint release
Knowledge Version arriving during Snapshot assembly
Constraint activation after seal
Legitimate epistemic UNKNOWN
Structural exact-ref UNKNOWN
Relationship Store unavailable
Constraint Store unavailable
Target / Horizon change
Retrieval miss
Synthesis silently re-querying Current store
Snapshot becoming stale after seal
~~~

Result:

~~~text
Temporal Eligibility
= PASS

Exact Revision Resolution
= PASS

Snapshot Assembly
= PASS

Snapshot Seal
= PASS

Current-Use Validity
= PASS

Historical Reconstruction
= PASS

Look-Ahead Protection
= PASS

Package A Compatibility
= PASS

Decision Synthesis Handoff
= PASS

Blocking Issue
= NONE
~~~

---

## 25.35 Package B Core Invariants

~~~text
PB-01 What happened != When the system knew it.
PB-02 Historical eligibility is determined by Information Availability, not Event Time alone.
PB-03 Original Decision uses only information available by its Information Cutoff.
PB-04 Snapshot pins exact historically reproducible revisions.
PB-05 Snapshot Seal means input integrity, not decision sufficiency.
PB-06 Sealed Snapshot is immutable.
PB-07 Historical Integrity != Current-Use Validity.
PB-08 Material invalidation → New Snapshot, not old Snapshot mutation.
PB-09 Original Snapshot Replay != Historical Reconstruction != Retrospective Analysis.
PB-10 Later information never becomes information that the past system had.
~~~

---

## 25.36 Save / Adoption Boundary

Checkpoint 018 saves Package B as Working Repair only.

Formal Current remains unchanged.

Do not modify:

~~~text
00_AI/AI_CONTEXT.md
00_HUMAN/HUMAN_MAP.md
02_ARCHITECTURE/
~~~

Still not decided here:

~~~text
DB tables
Python classes
storage engine
physical snapshot format
final enum names
exact fail-open / fail-closed implementation
~~~

---

## 25.37 Checkpoint Result

~~~text
Checkpoint 018
R3 Integration Repair
Package B — Temporal / Reproducibility
= SAVED WORKING REPAIR

R3-INT-002
= REPAIRED / WORKING

R3-INT-003
= REPAIRED / WORKING

PB-HO-001
Snapshot Seal Success != Decision Sufficiency
= CLARIFIED

PB-HO-002
Original Snapshot Replay != Historical Reconstruction
= CLARIFIED

PB-HO-003
Exact Ref must resolve to immutable / historically reconstructable revision
= CLARIFIED

Blocking Issue
= NONE

Formal Current Architecture
= UNCHANGED

NEXT
=
Repair Package C — Decision Contract

FIRST TARGET
=
R3-INT-004
Decision Candidate Contract Backfill
~~~

---

# 26. Checkpoint 019 — R3 Integration Repair / Package C — Decision Contract & Decision Lineage

**Date:** 2026-10-04  
**State:** SAVED / WORKING REPAIR CHECKPOINT  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction — R3 Integration Repair  
**Repair Package:** C — Decision Contract  
**Issues Repaired:** R3-INT-004 / R3-INT-008 / R3-INT-009 / R3-INT-010 / R3-INT-011  
**Cross-Cutting Addition:** Decision Lineage Contract  
**Next:** Repair Package D — Economic / Trade Exit, starting with R3-INT-005 Evaluation Availability / Sufficiency.

## 26.1 Package C Purpose

Package Cの目的は、Decision Material SnapshotからTrade Thesis Formation直前までを、Object責任、Unknown、Dependency、Economic Evaluation、Advancement Authority、History / Lineageを混線させず一本のDecision Contractとして閉じること。

Core flow:

~~~text
Decision Material Snapshot
↓
Decision Synthesis Result
↓
Decision Thesis
↓
Decision Candidate
↓
Economic Value Assessment
↓
Candidate Advancement Record
↓
Trade Thesis Formation
~~~

このFlowは一対一の一本道ではない。

~~~text
1 Snapshot
→ 0 / 1 / multiple Decision Theses

1 Decision Thesis
→ 0 / 1 / multiple Decision Candidates

1 Decision Candidate
→ multiple Economic Value Assessments over time

1 Candidate
→ multiple immutable Advancement Records over time

multiple Candidates
→ multiple ADVANCE branches may coexist
~~~

したがってPackage Cは、

> 一本のDecision Lineage Spine + 分岐可能なImmutable DAG

として扱う。

---

## 26.2 R3-INT-004 — Decision Candidate Contract Backfill

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Definition:

> Decision Candidateとは、Current-use validなDecision Thesisから導出された、Economic Value評価対象となる具体的かつ意味固定されたAction Option。何を対象に、どのInstrumentで、どのExposure Intent / Objective / Horizonとして評価するかを明示するが、そのEconomic Value、採用、資金量、Executionを決定しない。

Boundary:

~~~text
Decision Thesis
= 今の市場について何が言える？

Decision Candidate
= その市場理解から何をAction Optionとして評価する？

Economic Value
= そのAction Optionはどんな経済性を持つ？
~~~

Decision Candidate:

~~~text
!= Trade Thesis
!= Candidate Advancement
!= Capital Permission
!= Position Size
!= Order
!= Execution
~~~

---

## 26.3 Decision Candidate Logical Contract

Working semantic contract:

~~~text
Decision Candidate
│
├─ Candidate Identity
├─ Candidate Version
│
├─ Decision Thesis Ref(s)
├─ Decision Context Ref
│
├─ Target
├─ Instrument
├─ Exposure Intent
├─ Candidate Objective
├─ Relevant Horizon
│
├─ Evaluation Baseline Specification
│
├─ Preconditions
├─ Candidate-specific Invalidation Refs / Conditions
├─ Critical Unknown Refs
│
├─ Candidate As-Of
├─ Candidate Available / Materialized At
│
└─ Formation / Provenance Trace
~~~

DB schemaではない。

---

## 26.4 Candidate Identity / Version

Independently coexisting / evaluable Action Options:

~~~text
→ separate Candidate Identities
~~~

Same Action Option semantic correction / replacement:

~~~text
→ same Candidate Identity + new Candidate Version
~~~

Examples:

~~~text
Spot Long
Perp Long
Long
Short
RETURN_SEEKING
HEDGE
~~~

は、同時比較可能・独立Action Optionなら別Candidate Identity。

Material semantic changes:

~~~text
LONG → SHORT
BTC → ETH
PERP → SPOT
15m → 4h
RETURN_SEEKING → HEDGE
new instrument leg
new composite payoff
~~~

はEconomic Value側で修正しない。

---

## 26.5 Candidate-owned Semantics vs Economic Evaluation Context

Candidate-owned:

~~~text
Target
Instrument
Exposure Intent
Candidate Objective
Relevant Horizon
Evaluation Baseline Specification
Preconditions
Candidate Invalidation
Source Thesis lineage
Candidate-specific Unknown treatment
~~~

Economic Evaluation Context-owned:

~~~text
Actual Reference Exposure Snapshot
Venue context
Valuation Basis
Fee
Funding
Carry
Spread
Slippage
Liquidity
Exact Size / Size Region
Leverage
Current Market / Cost Context
~~~

Important:

~~~text
Evaluation Baseline Specification
!= Actual Evaluation Baseline Context Snapshot
~~~

Candidate semantic is immutable before Economic Evaluation.

---

## 26.6 Candidate Formation Authority

Logical responsibility:

> Decision Candidate Formationは、Current-use validなDecision Thesis / Decision Contextを基に、Economic Valueへ渡すAction Option semanticsを形成・固定する。

Candidate Formation owns Action Option semantics.

It does not own:

~~~text
Knowledge Truth
Decision Thesis Truth
Economic Value
Economic Risk Profile
ADVANCE / WAIT / ABSTAIN
Capital Permission
Position Size
Execution
~~~

Candidate Formation must not silently widen Target / Scope / Horizon beyond source Thesis support.

One Thesis may form zero / one / multiple Candidates.

No viable Action Option:

~~~text
!= Fake Candidate required
~~~

---

## 26.7 R3-INT-004 Core Invariants

~~~text
DC-01 Decision Thesis != Decision Candidate.
DC-02 Decision Candidate is an Economic Evaluation target, not Trade Permission.
DC-03 Candidate semantics must be fixed before Economic Evaluation.
DC-04 Economic Value must not invent missing Candidate semantics.
DC-05 Candidate must reference exact Decision Thesis lineage.
DC-06 Candidate Formation must not silently widen Target / Scope / Horizon.
DC-07 Target != Instrument.
DC-08 Exposure Intent != Position Size.
DC-09 Candidate Objective is Candidate semantics.
DC-10 Different Objective normally implies a different Candidate.
DC-11 Evaluation Baseline semantics must be explicit.
DC-12 Baseline Specification != Actual Baseline Context Snapshot.
DC-13 Mutable Reference Exposure belongs to EVA Context.
DC-14 Candidate Preconditions != Economic Validity Conditions.
DC-15 Candidate Invalidation != Knowledge Failure Boundary.
DC-16 Candidate Invalidation != Trade Thesis Invalidation.
DC-17 Candidate Invalidation != Economic Validity Condition.
DC-18 Candidate Critical Unknowns preserve source identity.
DC-19 Candidate As-Of != Candidate Available At != EVA As-Of.
DC-20 Immutable Candidate != Forever Current Candidate.
DC-21 Current-use validity changes must not mutate Candidate semantics.
DC-22 Economic context change only → New EVA, not Candidate mutation.
DC-23 Material Action semantic change → New Candidate or New Candidate Version.
DC-24 Independently evaluable Action Options should be separate Candidate Identities.
DC-25 Same Action semantic correction may use a new Candidate Version.
DC-26 One Thesis may form zero / one / multiple Candidates.
DC-27 No viable Action Option != Fake Candidate required.
DC-28 INCONCLUSIVE must not silently produce directional Candidate.
DC-29 Candidate Formation != Economic Value.
DC-30 Candidate Formation != Candidate Advancement.
DC-31 Candidate Formation != Capital Permission.
DC-32 Negative EV != Inverted Candidate.
DC-33 Positive EV does not authorize Candidate semantic mutation.
DC-34 Venue change requires New Candidate only if material instrument semantics change.
DC-35 Size / Leverage / Fee / Funding / Spread / Slippage are normally EVA Context.
DC-36 New instrument leg / composite payoff requires Candidate Formation.
DC-37 Economic Value consumes exact Candidate Version.
DC-38 Incomplete Candidate Contract routes back to Candidate Formation.
DC-39 Historical Candidate Versions remain immutable.
DC-40 Candidate Formation / Provenance remains traceable.
~~~

---

## 26.8 R3-INT-008 — Unknown Identity / Treatment

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Core model:

~~~text
Unknown Source / Finding
+
Layer-specific Treatment
~~~

Unknown itself
!= downstream treatment.

Logical Unknown identity:

~~~text
Unknown
│
├─ Unknown Question / Subject
├─ Origin Object Ref
├─ Source Domain / Layer
├─ Scope
├─ Relevant Horizon
├─ Unknown Reason
├─ As-Of / Availability Context
└─ Provenance
~~~

A central new Unknown architecture layer is not required.

---

## 26.9 Unknown Existence vs Criticality

~~~text
Unknown Existence
!= Unknown Criticality
~~~

The same unresolved question can be:

~~~text
Critical in one Thesis
Non-material in another Candidate
Economically material in an EVA
Accepted under an Advancement Policy
~~~

Criticality / materiality / acceptance are context-specific Treatments.

Downstream objects should reference the same Unknown source identity rather than copy / redefine the Unknown.

---

## 26.10 Unknown Reasons

Unknown Reason and semantic UNKNOWN are separated.

Candidate reasons may include:

~~~text
Missing Data
Stale Data
Source Conflict
Insufficient Evidence
Undefined Semantics
Model Unavailable
Probability Not Estimable
Dependency Unresolved
Temporal Availability Unknown
~~~

Exact enum is later work.

Important:

~~~text
Missing Data
!= semantic UNKNOWN itself

Missing Data
may cause
Condition = UNKNOWN
~~~

---

## 26.11 Unknown Acceptance / Resolution

Economic Value:

~~~text
identifies economic relevance of Unknown
~~~

Candidate Advancement:

~~~text
under explicit Policy,
decides whether an Unknown may be accepted for advancement
~~~

Trade Thesis:

~~~text
preserves Accepted Unknown refs historically
~~~

Important:

~~~text
Accepted Unknown
!= Resolved Unknown
!= Ignored Unknown
!= Low-Risk Truth
!= Assumed False
~~~

Later resolution does not rewrite historical Snapshot / Thesis / Advancement / Trade Thesis.

---

## 26.12 R3-INT-008 Core Invariants

~~~text
UK-01 UNKNOWN != FALSE.
UK-02 UNKNOWN != ZERO.
UK-03 UNKNOWN != 50% probability.
UK-04 Unknown != Uncertainty.
UK-05 Unknown != Conflict.
UK-06 Unknown != BLOCKED.
UK-07 Missing Data != Condition Mismatch.
UK-08 Unknown Reason != one generic Unknown semantic.
UK-09 Unknown existence != Criticality.
UK-10 Criticality is context-relative.
UK-11 Same unresolved question preserves traceable source identity downstream.
UK-12 Downstream adds Treatment; it does not redefine source Unknown.
UK-13 Thesis Critical Unknown is context treatment.
UK-14 Candidate Critical Unknown is Candidate-specific.
UK-15 Economic Value evaluates relevance but does not authorize acceptance.
UK-16 Candidate Advancement owns ADVANCE / WAIT / ABSTAIN treatment under Policy.
UK-17 Accepted Unknown != Resolved Unknown.
UK-18 Accepted Unknown != Ignored Unknown.
UK-19 Trade Thesis preserves Accepted Unknown refs historically.
UK-20 Later resolution must not rewrite historical Unknown treatment.
UK-21 Resolution may trigger new Assessment / Snapshot / EVA / Advancement.
UK-22 WAIT record must not be mutated after Unknown resolution.
UK-23 Epistemic Unknown != Snapshot Integrity Unknown.
UK-24 Legitimate epistemic Unknown may exist in valid Snapshot.
UK-25 Material snapshot integrity unknown may block sealing / use.
UK-26 Unknown Constraint State != No Constraint.
UK-27 Unknown Dependency != Independence.
UK-28 Logical Unknown Identity does not require a new central architecture layer.
UK-29 Unknown ownership remains with the domain defining the unresolved question.
UK-30 Historical Unknown remains historically true after later resolution.
~~~

---

## 26.13 R3-INT-009 — Dependency / Independence Provenance

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Core separation:

~~~text
Semantic Knowledge Relationship
!= Dependency
~~~

Canonical provenance / lineage is the source basis.

~~~text
Provenance Fact
!= Dependency Assessment
~~~

Example:

~~~text
R1 uses D1
R2 uses D1
K1 derived from R1
K2 derived from R2
~~~

are provenance facts.

Assessment:

~~~text
K1 / K2 have a material shared-data dependency
in this Decision Context
~~~

is contextual.

---

## 26.14 Dependency Dimensions / Scoped Independence

Candidate dimensions include:

~~~text
Evidence Dependency
Research / Experiment Lineage Dependency
Dataset Dependency
Feature Dependency
Mechanism Dependency
Event Dependency
Model Dependency
Economic Dependency
~~~

Exact enum is later work.

Important:

~~~text
Dependency Existence
!= Dependency Materiality

Different Dataset
!= Absolute Independence

No known dependency
!= Proven independence

No dependency identified
!= Independence supported
~~~

Independence must be dimension-scoped.

Independent Convergence requires explicit Independence Basis.

---

## 26.15 Dependency Assessment Contract

Logical candidate:

~~~text
Dependency Assessment
│
├─ Assessment ID
├─ Context Ref
├─ Subject Material Refs
├─ Dependency Dimensions
├─ Shared Source / Lineage Refs
├─ Dependency Findings
├─ Materiality
├─ Unresolved Dependency Refs
├─ Independence Basis [if claimed]
├─ Assessment Policy / Method Ref
├─ As-Of / Information Cutoff
└─ Provenance
~~~

Dependency Assessment does not rewrite canonical provenance.

AI-generated possible dependency
!= canonical provenance fact.

No giant new Dependency architecture layer is required.

---

## 26.16 Decision Dependency vs Economic Dependency

Decision reasoning dependency:

~~~text
shared Evidence
shared Dataset
shared Research lineage
shared Feature lineage
shared Mechanism
shared Event
~~~

Cross-Candidate Economic Dependency:

~~~text
shared underlying
shared venue
shared liquidity
shared funding regime
shared macro factor
~~~

Important:

~~~text
Decision Dependency Context
!= Cross-Candidate Economic Dependency Context
~~~

Both remain traceable.

---

## 26.17 R3-INT-009 Core Invariants

~~~text
DP-01 Semantic Relationship != Dependency.
DP-02 Canonical provenance is the source basis for dependency assessment.
DP-03 Dependency Context must not become duplicate universal truth storage.
DP-04 Provenance Fact != Dependency Assessment.
DP-05 Dependency Existence != Dependency Materiality.
DP-06 Dependency preserves type / source / materiality / provenance.
DP-07 Different Knowledge ID != Independent Evidence.
DP-08 Different Research ID != Independent Research.
DP-09 Different Feature Name != Independent Information.
DP-10 Different Dataset != Absolute Independence.
DP-11 Multiple observations of one event != multiple independent events.
DP-12 Shared Dataset != Complete Semantic Duplicate.
DP-13 Duplicate Knowledge != Duplicate Influence.
DP-14 Influence Deduplication != Knowledge deletion / merge.
DP-15 Knowledge Count != Vote Count.
DP-16 Knowledge Count != Evidence Count.
DP-17 No known dependency != Proven independence.
DP-18 No dependency identified != Independence supported.
DP-19 Dependency unavailable != No Dependency.
DP-20 Incomplete provenance must not be interpreted as independence.
DP-21 Independence must be dimension-scoped.
DP-22 Independence claim requires explicit Independence Basis.
DP-23 Independence in one dimension != independence in all dimensions.
DP-24 Independent Convergence != Vote Count.
DP-25 Independent Convergence != Truth Probability.
DP-26 Independent Convergence != automatic winner.
DP-27 Dependency Unknown remains Unknown.
DP-28 Assessment must not rewrite canonical provenance.
DP-29 AI possible dependency != canonical provenance fact.
DP-30 Snapshot pins dependency context available at its cutoff.
DP-31 Later dependency discovery must not rewrite Past Decision Context.
DP-32 Synthesis preserves shared dependency instead of independent double count.
DP-33 Semantic materials may remain separate despite dependent influence.
DP-34 Thesis may reference Dependency Context without copying full lineage.
DP-35 Decision Dependency != Cross-Candidate Economic Dependency.
DP-36 Candidate coexistence != Portfolio independence.
DP-37 Individual positive EV != independent combined economic value.
DP-38 Material economic dependency may require Joint Economic Envelope treatment.
DP-39 Dependency Assessment does not own Advancement / Capital Permission.
DP-40 Dependency correction creates a new Assessment, not historical mutation.
~~~

---

## 26.18 R3-INT-010 — Decision Synthesis Result / Decision Thesis Boundary

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Canonical flow:

~~~text
Sealed Decision Material Snapshot
↓
Current-Use Validity Gate
↓
Decision Synthesis
↓
Decision Synthesis Result
│
├─ Decision Thesis DT-...
├─ Decision Thesis DT-...
└─ Synthesis-wide Findings
↓
Decision Candidate Formation
~~~

Decision Thesis Candidate is deprecated unless a real promotion boundary is introduced later.

~~~text
Decision Thesis Candidate
→ deprecated alias / legacy wording
~~~

---

## 26.19 Decision Synthesis Result

Definition:

> 1つのExact Decision Material SnapshotをDecision Synthesisした一回のImmutableな結果全体。形成されたDecision Thesis群、Synthesis Outcome、Thesis Set Structure、Synthesis-wide Conflict / Unknown / Dependency context、Traceを保持する。

Logical contract:

~~~text
Decision Synthesis Result
│
├─ Result ID
├─ Exact Decision Material Snapshot Ref
├─ Decision Context Ref
│
├─ Synthesis Outcome
├─ Thesis Set Structure [if formed]
├─ Decision Thesis Refs[]
│
├─ Synthesis-wide Conflict Refs
├─ Synthesis-wide Critical Unknown Refs
├─ Synthesis-wide Dependency Context Refs
├─ Synthesis Findings / Sufficiency Findings
│
├─ Synthesis As-Of
├─ Synthesis Available At
├─ Synthesis Policy / Model Ref
└─ Provenance
~~~

Synthesis Result owns the whole synthesis event.

Decision Thesis owns one Market Judgment.

Do not duplicate Thesis semantic body inside Synthesis Result.

---

## 26.20 Synthesis Outcome / Thesis Set Structure

Two axes remain separate.

~~~text
Synthesis Outcome:
THESIS_FORMED
INCONCLUSIVE
~~~

When THESIS_FORMED:

~~~text
Thesis Set Structure:
SINGLE
MULTIPLE_COMPATIBLE
MULTIPLE_COMPETING
~~~

Contract:

~~~text
THESIS_FORMED
→ one or more Formal Decision Theses

INCONCLUSIVE
→ zero Formal Decision Theses
~~~

INCONCLUSIVE is not a fourth Thesis Set Structure.

---

## 26.21 Decision Thesis

Definition:

> 特定Decision Synthesis Result / Snapshot / Decision Contextに基づき、Target / Scope / Relevant Horizonについて形成されたImmutableなCurrent-market Judgment。Supporting / Opposing Material、Boundary、Conflict、Critical Unknown、Dependency、Uncertainty、Source Traceを保持するが、Action、Economic Value、Capital、Executionを決めない。

Logical contract:

~~~text
Decision Thesis
│
├─ Thesis ID
├─ Decision Synthesis Result Ref
├─ Decision Material Snapshot Ref
├─ Decision Context Ref
│
├─ Target
├─ Scope
├─ Relevant Horizon
├─ Market Judgment
│
├─ Supporting Material Refs
├─ Opposing Material Refs
├─ Material Boundary Refs
├─ Conflict Context Refs
├─ Critical Unknown Refs
├─ Dependency Context Refs
├─ Uncertainty Context
│
├─ Thesis As-Of
├─ Thesis Available At
├─ Synthesis Policy / Model Ref
└─ Provenance / Trace
~~~

Decision Thesis:

~~~text
!= Directional Signal
!= Decision Candidate
!= Trade Thesis
~~~

Non-directional Thesis is allowed.

---

## 26.22 Decision Thesis Immutability

Decision Thesis is a Snapshot-bound artifact.

Material re-synthesis:

~~~text
New Snapshot
↓
New Synthesis Result
↓
New Decision Thesis
~~~

Do not mutate old Thesis.

Thesis current-use validity is separate from historical integrity.

Supporting / Opposing Material must be ACTIVE INPUT.

TRACE ONLY:

~~~text
must not provide directional support / opposition
may affect sufficiency / audit
~~~

Dependency / Unknown / Conflict treatment remains explicit.

---

## 26.23 R3-INT-010 Core Invariants

~~~text
DST-01 Decision Synthesis Result != Decision Thesis.
DST-02 Result owns whole synthesis event; Thesis owns one Market Judgment.
DST-03 Result references, not duplicates, Thesis bodies.
DST-04 Decision Thesis Candidate is deprecated without a real promotion boundary.
DST-05 Decision Synthesis != Canonical Knowledge creation.
DST-06 Decision Synthesis != Economic Value.
DST-07 Synthesis Outcome != Thesis Set Structure.
DST-08 THESIS_FORMED requires at least one Formal Thesis.
DST-09 INCONCLUSIVE produces no Formal Thesis.
DST-10 Thesis Set Structure applies only when THESIS_FORMED.
DST-11 SINGLE / MULTIPLE_COMPATIBLE / MULTIPLE_COMPETING are separate from Outcome.
DST-12 MULTIPLE_COMPETING != Canonical CONTRADICTS.
DST-13 CONTRADICTS does not force truth winner.
DST-14 Decision Thesis is a Snapshot-bound Market Judgment.
DST-15 Decision Thesis != Directional Signal.
DST-16 Decision Thesis may be non-directional.
DST-17 Only ACTIVE INPUT provides formal Thesis support / opposition.
DST-18 TRACE ONLY must not become directional influence.
DST-19 TRACE ONLY may affect sufficiency / audit.
DST-20 Support Count != Vote Count.
DST-21 Support / Opposition role is Thesis-context-specific.
DST-22 Dependency Context remains visible in Thesis lineage.
DST-23 Critical Unknown is context treatment.
DST-24 Decision Thesis must be source-traceable.
DST-25 Novel unsupported causal inference must not become Canonical Knowledge via Synthesis.
DST-26 Novel research-worthy inference routes to R2.
DST-27 Decision Thesis is immutable.
DST-28 Material re-synthesis creates a new Thesis.
DST-29 Thesis As-Of != Thesis Available At.
DST-30 Later information must not be injected into existing Thesis.
DST-31 Historical Thesis integrity != current-use validity.
DST-32 Decision Thesis != Decision Candidate.
DST-33 Thesis must not own Instrument / Objective / Baseline / Position Size / EV.
DST-34 One Thesis may form zero / one / multiple Candidates.
DST-35 Competing Theses must not be silently collapsed into one directional Candidate.
DST-36 Decision Thesis != Trade Thesis.
DST-37 Trade Thesis must reference, not rewrite, Decision Thesis.
DST-38 Synthesis Result pins exact Snapshot / Policy / Model.
DST-39 Synthesis integrity failure must not appear as valid THESIS_FORMED.
DST-40 Structurally valid Snapshot may still yield INCONCLUSIVE.
~~~

---

## 26.24 R3-INT-011 — Candidate Advancement Governance / Terminology

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Precision terminology:

~~~text
PROCEED
→ deprecated legacy wording

ADVANCE
→ preferred precision term

Decision Disposition
→ deprecated ambiguous wording

Candidate Advancement Disposition
→ ADVANCE / WAIT / ABSTAIN
~~~

Disposition belongs to an immutable Candidate Advancement Record, not mutable Candidate state.

---

## 26.25 Candidate Advancement Responsibility

Definition:

> 特定のExact Decision Candidate Versionと、そのCandidateに対するCurrent-use validなEconomic Value Assessmentを、明示的かつVersionedなCandidate Advancement Policyの下で評価し、「Trade Thesis Formationへ進める」「条件変化・情報更新を待つ」「今回のCandidate Opportunityを終了する」のいずれかをCandidate-specificに判定する責任。

Core boundary:

~~~text
Economic Value Assessment
!= Candidate Advancement

Candidate Advancement
!= Trade Thesis Formation

ADVANCE
!= Trade Permission

ADVANCE
!= Capital Permission

Capital Permission
!= Execution Permission
~~~

---

## 26.26 Candidate Advancement Policy Governance

Logical authority:

~~~text
Candidate Advancement Policy Governance
↓
Versioned Candidate Advancement Policy
↓
Candidate Advancement Assessment
↓
Candidate Advancement Decision
↓
Immutable Candidate Advancement Record
~~~

Policy Governance owns criteria / threshold / Unknown acceptance rules / objective-specific rules.

Advancement logic is a Policy Consumer, not an ad hoc Policy Author.

AI may propose Policy changes but cannot silently activate them.

Policy Version is subject to Package B temporal / historical rules.

---

## 26.27 Advancement Input Contract

Logical inputs:

~~~text
Exact Decision Candidate Version Ref
Candidate Current-Use Validity Ref
Exact Economic Value Assessment Ref
EVA Current-Use Validity Ref
Evaluation Availability / Sufficiency Ref
Optional Relative Economic Comparison Ref
Candidate Objective
Critical Unknown Refs / Treatments
Economic Validity Condition Refs
Joint Economic Envelope Ref [if material]
Candidate Advancement Policy Ref
Advancement As-Of
Information Cutoff
Provenance
~~~

Candidate Advancement must not:

~~~text
repair missing Candidate semantics
author Economic Value
invent probability
rewrite EVA
silently invent advancement thresholds
~~~

---

## 26.28 ADVANCE / WAIT / ABSTAIN

ADVANCE:

> Current Candidate / EVA / Policy basis permits progression to Trade Thesis Formation.

~~~text
ADVANCE
!= Trade permission
!= Global Candidate winner
~~~

0 / 1 / multiple Candidates may ADVANCE.

WAIT:

> Opportunity remains live, but current conditions do not support advancement; a specific future change / information should trigger re-evaluation.

WAIT requires:

~~~text
Re-evaluation Trigger
Re-evaluation Route
and when needed
Expiry / Deadline relative to Candidate Horizon
~~~

WAIT:

~~~text
!= generic Error Bucket
!= R4 HOLD
!= Candidate invalidation
~~~

ABSTAIN:

> Current Candidate Opportunity is closed under the present Candidate / EVA / Policy context.

ABSTAIN:

~~~text
!= Knowledge Refutation
!= Decision Thesis Refutation
!= Candidate Deletion
!= Candidate Invalidation
!= Permanent Ban
~~~

NO-TRADE remains a derived human outcome, not a canonical Advancement state.

---

## 26.29 Unknown Acceptance in Advancement

Economic Value:

~~~text
identifies economic relevance of Unknown
~~~

Candidate Advancement:

~~~text
under explicit Policy,
decides advancement-scope acceptance
~~~

Trade Thesis:

~~~text
preserves Accepted Unknown refs
~~~

Accepted Unknown:

~~~text
!= Resolved Unknown
~~~

Accepted Unknown does not bind R4 to grant Capital Permission.

---

## 26.30 Candidate Advancement Record

Logical contract:

~~~text
Candidate Advancement Record
│
├─ Advancement Record ID
├─ Exact Decision Candidate Version Ref
├─ Candidate Current-Use Validity Ref
│
├─ Exact Economic Value Assessment Ref
├─ EVA Current-Use Validity Ref
├─ Evaluation Availability / Sufficiency Ref
├─ Optional Relative Economic Comparison Ref
│
├─ Candidate Advancement Policy Ref
├─ Candidate Advancement Disposition
│   ├─ ADVANCE
│   ├─ WAIT
│   └─ ABSTAIN
│
├─ Advancement Basis Refs
├─ Critical Unknown Treatment Refs
├─ Accepted Unknown Refs [ADVANCE]
├─ Economic Validity Condition Refs
│
├─ Advancement As-Of
├─ Information Cutoff
├─ Record Available At
│
├─ WAIT Trigger / Route / Expiry [WAIT]
├─ ABSTAIN Reason / Closure Scope [ABSTAIN]
├─ Predecessor / Related Advancement Ref [if re-evaluated]
└─ Provenance
~~~

Record is immutable.

Immutable ADVANCE Record
!= forever-current Advancement.

Trade Thesis Formation rechecks current-use validity.

---

## 26.31 R3-INT-011 Core Invariants

~~~text
CA-01 Economic Value Assessment != Candidate Advancement.
CA-02 Candidate Advancement != Trade Thesis Formation.
CA-03 ADVANCE != Trade Permission.
CA-04 ADVANCE != Capital Permission.
CA-05 Capital Permission != Execution Permission.
CA-06 PROCEED is deprecated; ADVANCE is preferred.
CA-07 Decision Disposition is deprecated as ambiguous.
CA-08 Candidate Advancement Disposition = ADVANCE / WAIT / ABSTAIN.
CA-09 Disposition belongs to immutable Advancement Record.
CA-10 Positive EV != Automatic ADVANCE.
CA-11 Negative Standalone EV != Automatic ABSTAIN for Hedge / Insurance.
CA-12 Advancement Policy must be explicit / versioned.
CA-13 Advancement logic is a Policy Consumer, not ad hoc Policy Author.
CA-14 AI may propose but not silently activate Policy changes.
CA-15 Objective may require objective-specific criteria.
CA-16 Advancement consumes exact Candidate Version.
CA-17 Advancement consumes exact current-use valid EVA.
CA-18 Advancement must not repair Candidate semantics.
CA-19 Advancement must not author Economic estimates.
CA-20 Candidate Contract Failure != WAIT.
CA-21 EVA Integrity Failure != WAIT.
CA-22 WAIT != Error Bucket.
CA-23 ADVANCE authorizes Trade Thesis Formation only.
CA-24 Multiple Candidates may simultaneously ADVANCE.
CA-25 ADVANCE != Global Winner.
CA-26 WAIT is a live but temporarily non-advancing Opportunity.
CA-27 WAIT requires identifiable Trigger.
CA-28 WAIT preserves an appropriate Re-evaluation Route.
CA-29 WAIT may require Expiry relative to Candidate Horizon.
CA-30 WAIT Record must not be mutated into ADVANCE.
CA-31 WAIT Trigger creates new evaluation / advancement lineage.
CA-32 WAIT != R4 HOLD.
CA-33 ABSTAIN closes current Opportunity, not Knowledge / Candidate identity.
CA-34 ABSTAIN != Knowledge Refutation.
CA-35 ABSTAIN != Decision Thesis Refutation.
CA-36 ABSTAIN != Candidate Deletion.
CA-37 ABSTAIN != Permanent Ban.
CA-38 ABSTAIN != Candidate Invalidation.
CA-39 NO-TRADE is derived, not canonical Advancement state.
CA-40 Unknown Identification != Unknown Acceptance.
CA-41 Candidate Advancement owns advancement-scope acceptance under Policy.
CA-42 Accepted Unknown != Resolved Unknown.
CA-43 Accepted Unknown does not bind R4.
CA-44 Advancement Record pins exact Policy Version.
CA-45 Later Policy must not rewrite historical Advancement.
CA-46 Advancement Basis references upstream findings; it does not duplicate truth.
CA-47 Advancement Record is immutable.
CA-48 Immutable ADVANCE != forever-current Advancement.
CA-49 Current-use loss must not mutate historical Disposition.
CA-50 Post-ADVANCE material change routes to new Assessment / Evaluation.
CA-51 Trade Thesis Formation references exact Advancement Record.
CA-52 Trade Thesis Formation does not re-decide Advancement.
CA-53 R4 BLOCK != Candidate Advancement Failure.
CA-54 R4 BLOCK != Economic Invalidity.
CA-55 Relative Comparison informs Advancement only under explicit Policy.
CA-56 Relative Comparison does not create universal Global Ranking.
CA-57 Candidate coexistence != Independent Opportunity.
CA-58 Dependency Context remains visible downstream.
CA-59 Evaluation Availability / Sufficiency is explicit input.
CA-60 Evaluation insufficiency != Automatic WAIT.
CA-61 Invalid Advancement Input Contract must not be forced into a Disposition.
CA-62 Advancement Integrity Failure != Advancement Disposition.
CA-63 Policy Governance != Candidate-specific Decision.
CA-64 Advancement Assessment != Policy Authoring.
CA-65 Advancement Decision remains traceable to Candidate / EVA / Policy / As-Of.
CA-66 Historical Advancement reasoning remains reproducible.
~~~

---

## 26.32 Decision Lineage Contract

Decision Lineage is a cross-cutting trace contract, not a new architecture layer.

Definition:

> Decision Lineageとは、1つのDecision Contextから派生したDecision Material Snapshot、Decision Synthesis Result、Decision Thesis、Decision Candidate、Economic Value Assessment、Candidate Advancement Record、Trade Thesisへ至るReason / Evidence / Evaluationの系譜を、各Immutable ArtifactのExact Referenceによって追跡可能にした横断Lineage。

Decision Lineage:

~~~text
!= Canonical Truth Owner
!= New Decision Engine
!= Governance Authority
!= New R3 Layer
~~~

---

## 26.33 Decision Lineage Root / Branching

Root:

~~~text
Decision Context
~~~

Example:

~~~text
Decision Lineage DL-001
│
├─ Decision Context DCX-001
├─ Snapshot S-001
├─ Synthesis Result SR-001
├─ Thesis
│   ├─ DT-001
│   └─ DT-002
├─ Candidate
│   ├─ CAN-001@v1
│   ├─ CAN-002@v1
│   └─ CAN-003@v1
├─ EVA
│   ├─ EVA-001
│   ├─ EVA-002
│   └─ EVA-003
├─ Advancement
│   ├─ AR-001 ADVANCE
│   ├─ AR-002 WAIT
│   └─ AR-003 ABSTAIN
└─ Trade Thesis
    └─ TT-001
~~~

Branching is normal.

Branch count
!= Vote Count.

---

## 26.34 Exact Artifact References vs Decision Lineage ID

Canonical lineage truth is established by exact artifact references.

~~~text
Exact Parent / Source Refs
=
canonical lineage basis
~~~

A Decision Lineage ID may be used as a correlation / traversal key.

~~~text
Decision Lineage ID
!= sole source of lineage truth
!= authority
~~~

Lineage ID alone is insufficient to know which Thesis / Candidate / EVA materially caused a downstream artifact.

---

## 26.35 Forward Contract Pattern

Each R3 stage should expose:

~~~text
INPUT
PROCESS
OUTPUT
GATE
RETURN
~~~

Example:

Decision Candidate:

~~~text
INPUT
Decision Thesis

PROCESS
Action Option Formation

OUTPUT
Decision Candidate

GATE
Candidate Contract Completeness

RETURN
Thesis support insufficient
→ Decision Synthesis
~~~

Economic Value:

~~~text
INPUT
Exact Decision Candidate Version

PROCESS
Economic Evaluation

OUTPUT
Economic Value Assessment

GATE
Evaluation Availability / Sufficiency

RETURN
Candidate semantics incomplete
→ Candidate Formation
~~~

This pattern supports explicit Return Router design later.

---

## 26.36 Unknown Carry-Forward Rule

Package C cross-check clarification:

~~~text
PC-HO-001
Material Unknown must be carried forward
by exact reference
or explicitly treated as non-material
for the downstream artifact.
~~~

Unknown must not silently disappear between Thesis / Candidate / EVA / Advancement / Trade Thesis.

---

## 26.37 Candidate Branch Termination

Package C cross-check clarification:

~~~text
PC-HO-002
Candidate-branch termination
!= Decision-Lineage termination.
~~~

ABSTAIN of one Candidate does not end sibling Candidate branches.

INCONCLUSIVE may end the lineage before Candidate Formation.

No Candidate is also a valid stopping point.

---

## 26.38 Canonical Lineage Basis

Package C cross-check clarification:

~~~text
PC-HO-003
Exact Artifact Refs are the canonical lineage basis.

Decision Lineage ID
is a correlation / traversal aid.
~~~

---

## 26.39 Artifact-specific Current-Use Validity

Package C cross-check clarification:

~~~text
PC-HO-004
Decision Lineage has no single universal Current-Use Validity state.
~~~

Validity may differ for:

~~~text
Snapshot
Decision Thesis
Decision Candidate
Economic Value Assessment
Candidate Advancement
Trade Thesis
~~~

Lineage-level VALID / STALE shown in UI may be derived only.

---

## 26.40 Temporal Integrity of Lineage Edges

Package C cross-check clarification:

~~~text
PC-HO-005
For every material lineage edge:

required upstream artifact
must be available
before downstream use / evaluation cutoff.
~~~

Example:

~~~text
Candidate Available At = 10:00:06

EVA cannot validly use that Candidate
at 10:00:04.
~~~

Downstream cannot use a future upstream artifact.

---

## 26.41 Original Decision Lineage vs Retrospective Analysis

Package C cross-check clarification:

~~~text
PC-HO-006
Retrospective / Counterfactual artifacts
must not masquerade as descendants
of the Original Decision Lineage.
~~~

Original lineage uses then-available Data / Policy / Model / Knowledge.

Later retrospective analysis remains a separate analysis lineage / explicitly retrospective branch.

---

## 26.42 Decision Lineage Common Invariants

~~~text
PC-01 Every downstream artifact references exact upstream artifact(s) materially relied upon.
PC-02 Downstream does not redefine upstream canonical truth.
PC-03 Decision Lineage may branch.
PC-04 Branch count != Vote Count.
PC-05 One Thesis may produce zero / one / multiple Candidates.
PC-06 One Candidate may have multiple EVA / Advancement descendants over time.
PC-07 WAIT re-evaluation creates new descendant lineage, not mutable disposition.
PC-08 ABSTAIN closes one Candidate branch, not whole Decision Lineage.
PC-09 Multiple ADVANCE branches may coexist.
PC-10 Unknown source identity remains traceable until later resolution.
PC-11 Material Unknown must not silently disappear between stages.
PC-12 Dependency remains visible; dependent support must not become independent influence.
PC-13 Decision Dependency != Economic Dependency.
PC-14 Candidate semantics are fixed before EVA.
PC-15 Economic Value must not mutate Candidate semantics.
PC-16 Candidate Advancement must not mutate Economic Assessment.
PC-17 Trade Thesis Formation must not re-decide Candidate Advancement.
PC-18 Each material artifact preserves As-Of / Available-At semantics.
PC-19 Downstream artifact cannot precede availability of required upstream artifact.
PC-20 Historical artifacts are immutable.
PC-21 Material upstream change creates new descendant artifacts / branches.
PC-22 Current-Use Validity is artifact-specific, not one Lineage state.
PC-23 Decision Lineage ID is not a truth owner.
PC-24 Exact Parent / Source refs define canonical lineage.
PC-25 Original Decision Lineage != Retrospective Analysis Lineage.
PC-26 Normal termination before Trade Thesis is valid.
PC-27 NO-TRADE is a derived human outcome, not canonical lineage state.
PC-28 Every Trade Thesis must trace back to an exact Decision Material Snapshot.
~~~

---

## 26.43 Package C End-to-End Contract

~~~text
Decision Context
↓
Decision Material Snapshot
  - exact decision input boundary
  - temporal / no-look-ahead integrity
↓
Current-Use Validity Gate
↓
Decision Synthesis
↓
Decision Synthesis Result
  - synthesis-wide outcome / structure
↓
Decision Thesis
  - immutable Market Judgment
↓
Decision Candidate Formation
↓
Decision Candidate
  - immutable Action Option semantics
↓
Candidate Current-Use Validity Gate
↓
Economic Value Assessment
  - candidate-specific economics
↓
Evaluation Availability / Sufficiency
↓
Candidate Advancement
  - policy-governed ADVANCE / WAIT / ABSTAIN
↓
ADVANCE only
Trade Thesis Formation
~~~

Trade Thesis Formation details are completed in Package D.

---

## 26.44 Package C Cross Check

Cross-check dimensions:

~~~text
Object Ownership
Unknown Continuity
Dependency Continuity
Decision Thesis / Candidate Boundary
Candidate / EVA Boundary
EVA / Advancement Boundary
Advancement / Trade Thesis Formation Boundary
Branching Model
Temporal / Availability Integrity
Historical Immutability
Decision Lineage Traceability
~~~

Result:

~~~text
Object Ownership
= PASS

Unknown Continuity
= PASS

Dependency Continuity
= PASS

Decision Thesis / Candidate Boundary
= PASS

Candidate / EVA Boundary
= PASS

EVA / Advancement Boundary
= PASS

Advancement / Trade Thesis Formation Boundary
= PASS

Branching Model
= PASS

Temporal / Availability Integrity
= PASS

Historical Immutability
= PASS

Decision Lineage Traceability
= PASS

Blocking Issue
= NONE
~~~

---

## 26.45 Package D Cross-Package Dependencies

Package C is closed, but three repair items remain intentionally in Package D.

### CPD-001 — R3-INT-005

~~~text
Economic Value Assessment
→ Evaluation Availability / Sufficiency
~~~

Candidate Advancement consumes this as explicit input.

Detailed semantics remain Package D work.

Non-blocking for Package C.

### CPD-002 — R3-INT-012

~~~text
ADVANCE
→ Trade Thesis Formation
→ immutable Trade Thesis revision / adoption
~~~

Package C closes the handoff to Trade Thesis Formation.

Trade Thesis revision / adoption / writer semantics remain Package D.

Non-blocking for Package C.

### CPD-003 — R3-INT-014

~~~text
Backward Return Router Common Rule
~~~

Package C defines stage-specific Return expectations.

The shared common router / loop rule remains Package D.

Non-blocking for Package C.

---

## 26.46 Save / Adoption Boundary

Checkpoint 019 saves Package C and Decision Lineage Contract as Working Repair only.

Formal Current remains unchanged.

Do not modify:

~~~text
00_AI/AI_CONTEXT.md
00_HUMAN/HUMAN_MAP.md
02_ARCHITECTURE/
~~~

Still not decided here:

~~~text
DB tables
Python classes
physical Decision Lineage storage
central vs distributed lineage index
final enum names
final exact field names
runtime process topology
final fail-open / fail-closed implementation
~~~

---

## 26.47 Checkpoint Result

~~~text
Checkpoint 019
R3 Integration Repair
Package C — Decision Contract
= SAVED WORKING REPAIR

R3-INT-004
Decision Candidate Contract
= REPAIRED / WORKING

R3-INT-008
Unknown Identity / Treatment
= REPAIRED / WORKING

R3-INT-009
Dependency / Independence Provenance
= REPAIRED / WORKING

R3-INT-010
Decision Synthesis Result / Decision Thesis Boundary
= REPAIRED / WORKING

R3-INT-011
Candidate Advancement Governance / Terminology
= REPAIRED / WORKING

Decision Lineage Contract
= ADDED / WORKING

Package C Cross Check
= PASS

PC-HO-001
Material Unknown carry-forward or explicit non-material treatment
= CLARIFIED

PC-HO-002
Candidate branch termination != Decision Lineage termination
= CLARIFIED

PC-HO-003
Exact Artifact Refs are canonical lineage basis
= CLARIFIED

PC-HO-004
Current-Use Validity is artifact-specific
= CLARIFIED

PC-HO-005
Downstream cannot use future upstream artifact
= CLARIFIED

PC-HO-006
Retrospective artifacts != Original Decision Lineage descendants
= CLARIFIED

Blocking Issue
= NONE

Formal Current Architecture
= UNCHANGED

NEXT
=
Repair Package D — Economic / Trade Exit

FIRST TARGET
=
R3-INT-005
Evaluation Availability / Sufficiency
~~~

---

# 27. Checkpoint 020 — R3 Integration Repair / Package D — Economic / Trade Exit & Backward Return Router

**Date:** 2026-10-04  
**State:** SAVED / WORKING REPAIR CHECKPOINT  
**Formal Current Architecture Changed:** NO  
**Phase:** 5 Reconstruction — R3 Integration Repair  
**Repair Package:** D — Economic / Trade Exit  
**Issues Repaired:** R3-INT-005 / R3-INT-012 / R3-INT-014  
**Next:** Adjacent Contract Recheck → STEP 8 Destruction Test / R3 Integration Final Review.

## 27.1 Package D Purpose

Package D closes the final R3 integration gap between Economic Value, Evaluation Availability / Sufficiency, Candidate Advancement, Trade Thesis Formation / Adoption, R4 handoff, and backward routing from R4 / Runtime / downstream findings.

Core forward flow:

~~~text
Decision Candidate
↓
Economic Value Assessment
↓
Evaluation Availability / Sufficiency Assessment
↓
Candidate Advancement
↓
ADVANCE
↓
Trade Thesis Formation
↓
Trade Thesis Adoption
↓
Immutable Trade Thesis
↓
R4 Economic / Capital Decision
~~~

Core backward rule:

> A downstream finding must return to the nearest upstream semantic owner of the meaning that actually changed, then rebuild forward only through materially dependent descendants. Historical artifacts are never rewritten.

---

## 27.2 R3-INT-005 — Evaluation Availability / Sufficiency

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Economic evaluation is separated into distinct axes:

~~~text
Evaluation Integrity
!= Evaluation Availability
!= Evaluation Coverage
!= Evaluation Sufficiency
!= Economic Attractiveness
!= Candidate Advancement
~~~

Economic Value Assessment existence:

~~~text
!= Strict Expected EV availability
~~~

A valid partial EVA is allowed.

~~~text
Valid Partial Evaluation
!= Invalid Evaluation
~~~

---

## 27.3 Evaluation Integrity

Evaluation Integrity asks whether the EVA is structurally / temporally valid as an economic assessment artifact.

Minimum semantic checks include:

~~~text
Exact Candidate Version resolved
Economic Evaluation Context resolved
Candidate semantics complete
Temporal eligibility / No-Look-Ahead pass
Model / Mapping refs resolved
Required provenance traceable
No silent Candidate mutation
No material double counting
~~~

Integrity failure:

~~~text
!= Negative EV
!= Evaluation Insufficiency
!= WAIT
!= ABSTAIN
~~~

It routes to the owner of the defect.

---

## 27.4 Evaluation Availability

Evaluation Availability is component / capability specific.

A single EVA.available boolean is insufficient.

Example:

~~~text
Gross Outcome
= AVAILABLE

Net Outcome
= LIMITED

Strict Expected EV
= UNAVAILABLE

Scenario Evaluation
= AVAILABLE

Stress Evaluation
= AVAILABLE

Probabilistic Tail
= UNAVAILABLE

Tail Severity
= AVAILABLE
~~~

Exact enum is later work.

Important:

~~~text
Numeric Output Exists
!= Metric Validly Available
~~~

---

## 27.5 Evaluation Mode / Probability Boundary

Strict Expected Value requires valid probability semantics.

~~~text
Unknown Probability
!= 50%

Scenario Weight
!= Validated Probability

Scenario-weighted Estimate
!= Strict Expected Value

Stress Exposure
!= Expected Loss without valid probability semantics
~~~

When probabilities are unknown:

~~~text
Strict Expected EV
= unavailable

Scenario / Stress evaluation
= may remain valid
~~~

Unsupported mode fallback must remain explicit.

---

## 27.6 Gross / Net / Cost Coverage

~~~text
Gross Economic Availability
!= Net Economic Availability
~~~

Missing material Slippage / Funding / Spread / Carry must not silently become zero.

Model Coverage Boundary must prevent:

~~~text
false missingness
double counting
~~~

Example:

~~~text
Slippage model includes Spread
→ do not separately count Spread again
~~~

Raw Data Availability:

~~~text
!= Economic Metric Availability
~~~

Data + Model + Mapping + Context / Coverage may all be required.

---

## 27.7 Evaluation Coverage

Coverage describes which required / optional economic dimensions were evaluated.

Coverage count / percentage is not sufficiency.

~~~text
Coverage Count
!= Evaluation Sufficiency

Complete Coverage
!= Automatic Sufficiency

Partial Coverage
!= Automatic Insufficiency
~~~

A single missing required component can be material even if most components are available.

---

## 27.8 Evaluation Requirement Profile

Sufficiency is evaluated relative to an explicit Versioned Evaluation Requirement Profile.

Logical candidate:

~~~text
Evaluation Requirement Profile
│
├─ Profile ID / Version
├─ Applicable Candidate Objective
├─ Instrument / Exposure Context
├─ Horizon / Evaluation Purpose
├─ Required Evaluation Modes
├─ Required Economic Components
├─ Conditional Requirements
├─ Optional / Diagnostic Components
├─ Required Probability Semantics
├─ Cost Coverage Requirements
├─ Tail / Stress Requirements
├─ Dependency Requirements
├─ Freshness / Temporal Requirements
├─ Model Coverage Requirements
└─ Provenance
~~~

Component roles may include semantic equivalents of:

~~~text
REQUIRED
CONDITIONAL
OPTIONAL
DIAGNOSTIC
~~~

Exact enum is later work.

Candidate Objective / Instrument / Horizon may activate different requirements.

---

## 27.9 Evaluation Sufficiency

Definition:

> Evaluation Sufficiency is the assessment of whether an exact Economic Value Assessment satisfies the applicable Versioned Evaluation Requirement Profile for the intended evaluation purpose.

Working result semantics may include:

~~~text
SUFFICIENT
INSUFFICIENT
UNDETERMINED
~~~

Exact enum is later work.

Important:

~~~text
Unknown existence
!= Automatic Insufficiency

Evaluation Sufficiency
!= Confidence Score

Evaluation Sufficiency
!= Coverage Percentage

Sufficient Evaluation
!= ADVANCE

Insufficient Evaluation
!= Automatic WAIT

Insufficient Evaluation
!= Automatic ABSTAIN
~~~

---

## 27.10 Evaluation Availability / Sufficiency Assessment

Logical contract:

~~~text
Evaluation Availability / Sufficiency Assessment
│
├─ Assessment ID
├─ Exact Economic Value Assessment Ref
├─ Exact Decision Candidate Version Ref
├─ Economic Evaluation Context Ref
├─ Evaluation Requirement Profile Ref
├─ Evaluation Mode / Capability Profile
├─ Component Availability Profile
├─ Coverage Profile
├─ Required Component Gap Refs
├─ Critical Unknown Refs
├─ Uncertainty / Quality Findings
├─ Temporal / Freshness Findings
├─ Model / Mapping Coverage Findings
├─ Sufficiency Result
├─ Sufficiency Reason / Limitation Refs
├─ Assessment As-Of
├─ Information Cutoff
├─ Assessment Available At
└─ Provenance
~~~

This assessment does not rewrite EVA and does not own Candidate Advancement.

Later Requirement Profile / Market information does not rewrite historical assessments.

---

## 27.11 R3-INT-005 Core Invariants

~~~text
EAS-01 EVA existence != Strict Expected EV availability.
EAS-02 Valid Partial EVA != Invalid EVA.
EAS-03 Evaluation Integrity != Evaluation Availability.
EAS-04 Evaluation Availability != Evaluation Coverage.
EAS-05 Evaluation Coverage != Evaluation Sufficiency.
EAS-06 Evaluation Sufficiency != Economic Attractiveness.
EAS-07 Economic Attractiveness != Candidate Advancement.
EAS-08 Numeric Output Exists != Metric validly available.
EAS-09 Economic Component availability is component-specific.
EAS-10 Availability respects Data / Model / Mapping / Temporal / Coverage prerequisites.
EAS-11 Missing Metric != Zero Metric.
EAS-12 Missing Monetization Mapping != Zero EV.
EAS-13 Unknown Probability != 50%.
EAS-14 Scenario Weight != Validated Probability.
EAS-15 Scenario-weighted Estimate != Strict Expected Value.
EAS-16 Stress Exposure != Expected Loss without probability semantics.
EAS-17 Unknown Tail Probability != Zero Tail Risk.
EAS-18 Gross Availability != Net Availability.
EAS-19 Missing material Slippage != zero Slippage.
EAS-20 Coverage boundaries prevent double counting / false missingness.
EAS-21 Raw Data Availability != Economic Metric Availability.
EAS-22 Unknown Finding Available != numeric metric available.
EAS-23 Coverage Count != Sufficiency.
EAS-24 Complete Coverage != Automatic Sufficiency.
EAS-25 Partial Coverage != Automatic Insufficiency.
EAS-26 Requirement Profile is explicit / versioned.
EAS-27 Sufficiency is relative to applicable Requirement Profile.
EAS-28 Candidate Objective may require different requirements.
EAS-29 Instrument / Exposure / Horizon may activate conditional requirements.
EAS-30 Unknown existence != Automatic Insufficiency.
EAS-31 Material required Unknown / gap remains explicit.
EAS-32 Sufficiency != Confidence Score.
EAS-33 Sufficiency != Coverage Percentage.
EAS-34 Sufficient Evaluation != ADVANCE.
EAS-35 Insufficient Evaluation != Automatic WAIT.
EAS-36 Insufficient Evaluation != Automatic ABSTAIN.
EAS-37 Integrity Failure must not become Advancement Disposition.
EAS-38 Assessment references exact EVA / Candidate Version.
EAS-39 Assessment references exact Requirement Profile Version.
EAS-40 Assessment does not rewrite Economic Value.
EAS-41 Assessment does not own Candidate Advancement.
EAS-42 Later Requirement Profile does not rewrite historical Sufficiency.
EAS-43 Later market / cost information does not rewrite historical EVA / Sufficiency.
EAS-44 Material new economic information creates new evaluation lineage.
EAS-45 Same current-valid EVA may receive new Sufficiency Assessment under a new Requirement Profile.
EAS-46 Historical Sufficiency != Current-Use Validity.
EAS-47 Standalone Sufficiency != Relative Comparison Sufficiency.
EAS-48 Individual Candidate Sufficiency != Joint Economic Envelope Sufficiency.
EAS-49 Strict Expected Value requires valid probability semantics.
EAS-50 Unsupported mode fallback must not masquerade as requested mode.
EAS-51 Unsupported metrics remain unavailable; numbers must not be fabricated.
EAS-52 Candidate Advancement consumes Availability / Sufficiency; it does not author them ad hoc.
~~~

---

## 27.12 R3-INT-012 — Trade Thesis Revision / Adoption / Immutability

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Definition:

> Trade Thesis is an immutable Trade-specific Reasoning Artifact that fixes why an ADVANCEd exact Decision Candidate is submitted to R4, including exact Decision Thesis, Candidate, EVA, Evaluation Sufficiency, Advancement, Economic Validity Conditions, Accepted Unknowns, Dependencies and Trade-specific Invalidation semantics.

Trade Thesis:

~~~text
!= Knowledge Truth
!= Decision Thesis
!= Decision Candidate
!= Economic Value Assessment
!= Candidate Advancement Decision
!= Capital Permission
!= Position Size
!= Execution Order
!= Actual Exposure
~~~

---

## 27.13 Trade Thesis Formation / Adoption / Writer

Canonical working authority chain:

~~~text
Candidate Advancement Record
Disposition = ADVANCE
↓
Current-Use Validity Gate
↓
Trade Thesis Formation
↓
Trade Thesis Formation Result
↓
Trade Thesis Adoption Assessment
↓
Trade Thesis Adoption Authorization
↓
Trade Thesis Writer
↓
Immutable Trade Thesis
~~~

Key separation:

~~~text
Formation
!= Adoption

Adoption
!= Materialization

Materialization
!= Capital Permission

Capital Permission
!= Exposure Activation
~~~

Adoption checks reasoning-contract integrity; it does not re-run Economic attractiveness or create a second ADVANCE / WAIT / ABSTAIN authority.

---

## 27.14 Trade Thesis Logical Contract

Working semantic contract:

~~~text
Trade Thesis
│
├─ Trade Thesis ID
├─ Decision Lineage Ref
├─ Decision Context Ref
├─ Decision Material Snapshot Ref
├─ Decision Synthesis Result Ref
├─ Decision Thesis Ref(s)
├─ Exact Decision Candidate Version Ref
├─ Exact Economic Value Assessment Ref
├─ Exact Evaluation Availability / Sufficiency Assessment Ref
├─ Exact Candidate Advancement Record Ref
├─ Relied-Upon Knowledge Version Refs
├─ Material Dependency Context Refs
├─ Advancement Basis Refs
├─ Material Economic Basis Refs
├─ Economic Risk / Tail Refs
├─ Economic Validity Condition Refs
├─ Accepted Unknown Refs
├─ Trade-specific Invalidation Conditions
├─ Trade Thesis As-Of
├─ Information Cutoff
├─ Available At
├─ Formation Policy / Method Ref
├─ Adoption Authorization Ref
├─ Predecessor Trade Thesis Ref [if revision]
├─ Revision / Replacement Reason [if applicable]
└─ Provenance
~~~

Only materially relied-upon exact upstream refs are fixed; full upstream truth is not copied.

---

## 27.15 Trade Thesis Revision

Trade Thesis is immutable.

Revision means:

~~~text
new upstream basis
↓
new Formation
↓
new Adoption
↓
new immutable Trade Thesis
~~~

It does not mean in-place mutation.

Preferred lineage:

~~~text
TT-101
↓ predecessor
TT-202
~~~

rather than mutable TT-101@v2 semantics.

Economic Re-evaluation:

~~~text
!= automatic Trade Thesis revision
~~~

A new Trade Thesis is formed only after the new upstream path reaches a valid ADVANCE and Adoption.

---

## 27.16 Revision vs New Branch

Same Candidate branch + new economic basis:

~~~text
may produce successor Trade Thesis
~~~

Material Candidate semantic change:

~~~text
→ Candidate Formation
→ new Candidate branch
→ new Trade Thesis branch
~~~

New Decision Thesis / Decision Context basis:

~~~text
→ new Decision lineage branch
~~~

Do not hide semantic changes as Trade Thesis revision.

---

## 27.17 Trade Thesis Current-Use Validity

Historical Trade Thesis integrity:

~~~text
!= current-use validity
~~~

Current-use assessment may consider:

~~~text
Source Decision Thesis validity
Candidate validity
EVA validity
EAS validity
Advancement validity
Accepted Unknown treatment
Economic Validity Conditions
Trade Thesis Invalidation Conditions
Relevant Horizon
Material Dependency changes
~~~

Later Knowledge / Relationship / Dependency / Unknown resolution never rewrites the historical Trade Thesis.

---

## 27.18 R4 / Runtime Boundary

R4 consumes exact Trade Thesis refs.

~~~text
Trade Thesis
!= R4 Capital Permission
~~~

Capital-only change inside valid economic envelope:

~~~text
→ R4 only
→ no Trade Thesis revision required
~~~

Economic envelope exceeded:

~~~text
→ Economic Re-evaluation
→ EAS
→ Advancement
→ if ADVANCE, new Trade Thesis
~~~

New instrument leg / composite payoff:

~~~text
→ Candidate Formation
~~~

Actual Exposure is required before Runtime Assumption Set activation.

~~~text
Trade Thesis exists
+ R4 ALLOW
+ No Fill
→ Active Runtime Assumption Set = none
~~~

Trade Thesis invalidation while exposed routes to Runtime / R4 authority; it does not directly command EXIT.

---

## 27.19 R3-INT-012 Core Invariants

~~~text
TT-01 Trade Thesis is immutable Trade-specific reasoning.
TT-02 Trade Thesis != Knowledge Truth.
TT-03 Trade Thesis != Decision Thesis.
TT-04 Trade Thesis != Candidate Advancement.
TT-05 Trade Thesis != Capital Permission.
TT-06 Trade Thesis creation != Position Activation.
TT-07 Formation != Adoption.
TT-08 Adoption != R4 Capital Approval.
TT-09 Formation consumes exact current-use valid ADVANCE record.
TT-10 Formation must not re-decide Advancement.
TT-11 Formation must not mutate Candidate semantics.
TT-12 Formation must not author Economic Value.
TT-13 Formation must not add / remove Accepted Unknowns ad hoc.
TT-14 Formation Result != Adopted Trade Thesis.
TT-15 Adoption checks reasoning-contract integrity, not Economic attractiveness.
TT-16 Adoption must not create second Advancement authority.
TT-17 Adoption Authorization != Trade Thesis Available.
TT-18 Downstream use begins only after successful materialization.
TT-19 Writer must not alter authorized semantics.
TT-20 Writer precondition failure must not be ignored.
TT-21 Writer failure != predecessor automatically valid.
TT-22 Trade Thesis pins exact Decision Thesis refs.
TT-23 Trade Thesis pins exact Candidate Version.
TT-24 Trade Thesis pins exact EVA.
TT-25 Trade Thesis pins exact EAS.
TT-26 Trade Thesis pins exact Advancement Record.
TT-27 Trade Thesis preserves relied-upon Knowledge Version refs.
TT-28 Trade Thesis preserves material Dependency Context refs.
TT-29 Trade Thesis preserves Accepted Unknown refs.
TT-30 Accepted Unknown != Resolved Unknown.
TT-31 Trade Thesis preserves Economic Validity Condition refs.
TT-32 Economic Validity Condition != Trade Thesis Invalidation Condition.
TT-33 Trade Thesis Invalidation != R4 Stop / EXIT rule.
TT-34 Trade Thesis Invalidation does not directly command Position Action.
TT-35 Trade Thesis is immutable.
TT-36 Revision means a new immutable Trade Thesis artifact.
TT-37 Revision must not overwrite predecessor reasoning.
TT-38 Same Candidate + new EVA / Advancement + ADVANCE may create successor Trade Thesis.
TT-39 Economic Re-evaluation != automatic Trade Thesis revision.
TT-40 New Candidate semantics creates new branch.
TT-41 New Decision Thesis lineage creates new reasoning branch.
TT-42 Capital-only R4 changes do not require Trade Thesis revision.
TT-43 Change inside valid Economic Envelope does not require Trade Thesis revision.
TT-44 Change outside Economic Envelope routes through Economic Re-evaluation.
TT-45 New instrument leg / composite payoff routes through Candidate Formation.
TT-46 Historical Trade Thesis != forever current-use valid.
TT-47 Current-use validity != historical integrity.
TT-48 Later Unknown resolution does not rewrite history.
TT-49 Later Knowledge Version does not rewrite history.
TT-50 Later Relationship / Dependency does not rewrite history.
TT-51 No single Global Current Trade Thesis is required.
TT-52 R4 consumes exact Trade Thesis refs.
TT-53 Multiple adopted Trade Thesis branches may coexist.
TT-54 R4 BLOCK != Trade Thesis invalidity.
TT-55 R4 BLOCK != Advancement failure.
TT-56 No Fill → no Active Runtime Assumption Set.
TT-57 Actual Exposure is required before Runtime Assumption activation.
TT-58 Runtime Assumption Set references exact Trade Thesis.
TT-59 Runtime monitoring must not mutate Trade Thesis.
TT-60 Invalidation while exposed routes to Runtime / R4, not automatic EXIT.
TT-61 Adoption / Materialization timestamps obey Temporal Contract.
TT-62 R4 cannot use Trade Thesis before Available At.
TT-63 Later Adoption Policy does not rewrite historical adoption.
TT-64 Semantic correction must not silently edit historical Trade Thesis.
TT-65 Correction != Revision reason.
TT-66 Retrospective Trade Thesis != Original Decision Lineage output.
TT-67 Exact artifact refs are canonical reasoning chain.
TT-68 Adoption does not select a global winner.
~~~

---

## 27.20 R3-INT-014 — Backward Return Router Common Rule

Repair Result:

~~~text
PASS AS WORKING REPAIR
~~~

Definition:

> Backward Return Router Common Rule is a cross-cutting routing protocol that classifies a downstream change / finding by the meaning that actually changed, identifies the nearest upstream authority that owns that meaning, routes the finding to that owner, and rebuilds only materially dependent descendants forward without rewriting historical artifacts.

Important:

~~~text
Return Router
!= Universal Router Service
!= Truth Authority
!= Economic Authority
!= Capital Authority
!= History Mutation Mechanism
~~~

A dedicated giant Return Router architecture layer is not required.

---

## 27.21 Core Routing Principle — Nearest Semantic Owner

Routing is based on:

~~~text
What meaning changed?
~~~

not merely:

~~~text
Where was the problem detected?
~~~

Core rule:

~~~text
Downstream Finding
↓
Classify semantic change
↓
Check material dependency / affected exact artifacts
↓
Choose nearest upstream semantic owner
↓
Create immutable Return / Re-evaluation lineage
↓
Rebuild forward only through materially affected descendants
~~~

Do not rewind farther than necessary.

Do not stay downstream if the downstream component does not own the changed meaning.

---

## 27.22 Common Return Classes

### Capital-only / R4-owned Change

Examples:

~~~text
Capital reservation
Portfolio capacity
Position-size reduction
Capital concentration
Risk budget
Protection inside existing authorized semantics
~~~

When Candidate semantics / EVA envelope / Thesis remain valid:

~~~text
→ R4 only
~~~

### Economic Change

Examples:

~~~text
Spread / Slippage regime change
Funding / Carry change
Valuation basis change
Size outside evaluated region
Economic model / cost context update
Joint Economic Envelope insufficiency
~~~

When Thesis / Candidate semantics remain valid:

~~~text
→ Economic Value Re-evaluation
→ EAS
→ Candidate Advancement
→ if ADVANCE, new Trade Thesis
~~~

### Candidate Semantic / Composite Change

Examples:

~~~text
LONG → SHORT
Target change
Instrument semantic change
Objective change
Horizon change beyond source support
New hedge leg
New composite payoff
~~~

Route:

~~~text
→ Decision Candidate Formation
→ Economic Value
→ EAS
→ Advancement
→ Trade Thesis if ADVANCE
~~~

### Decision Input / Thesis Change

Examples:

~~~text
Source Decision Thesis invalidated
Material Market Context changed
Material Relationship / Dependency change
Critical Unknown resolved or changed in a Thesis-material way
Material decision input set changed
~~~

Route:

~~~text
→ new Decision Material Snapshot
→ Decision Synthesis
→ new Decision Thesis / downstream branch
~~~

Do not re-synthesize using a mutated old Snapshot.

### Knowledge Applicability / Use Change

Examples:

~~~text
Knowledge becomes NOT_APPLICABLE
Knowledge-Use Constraint activates
Lifecycle eligibility changes
Constraint / applicability state materially changes
~~~

Route first to the owning Applicability / Constraint / Lifecycle authority, then:

~~~text
→ new Decision Material Snapshot
→ Decision Synthesis
→ rebuild affected descendants
~~~

### Knowledge Validity / Research Change

Examples:

~~~text
Canonical Knowledge validity challenged
Evidence contradiction requires revalidation
Novel causal mechanism discovered
Research hypothesis required
Knowledge truth cannot be resolved at Decision layer
~~~

Route:

~~~text
→ R2 Research / Validation / Lifecycle / Admission path as appropriate
~~~

Then only formally available validated / admitted results may flow forward again.

### Data / Temporal / Integrity Defect

Examples:

~~~text
wrong revision
look-ahead leak
source timing defect
corrupt model ref
unresolvable exact ref
data quality defect
~~~

Route to the owner of the defective data / temporal / assessment contract.

Do not disguise integrity defects as WAIT / ABSTAIN / negative EV.

---

## 27.23 R4 Type A-D Compatibility

The earlier R4-specific classification remains compatible.

~~~text
Type A — Capital-only Change
→ R4

Type B — Economic Change
→ Economic Re-evaluation

Type C — Candidate Semantic / Composite Change
→ Candidate Formation

Type D — Thesis / Knowledge Validity Change
→ Decision / Applicability / Research owner according to actual semantic scope
~~~

Package D refines Type D instead of changing the earlier meaning.

---

## 27.24 Return Routing Assessment

Logical candidate:

~~~text
Return Routing Assessment
│
├─ Routing Assessment ID
├─ Source Event / Finding Ref
├─ Source Artifact Ref
├─ Source Stage
├─ Detection As-Of / Available At
├─ Actual Exposure State Ref [if relevant]
├─ Semantic Change Class
├─ Affected Exact Artifact Refs
├─ Material Dependency / Impact Refs
├─ Current-Use Validity Findings
├─ Primary Upstream Owner / Route
├─ Optional Parallel Safety Route
├─ Re-evaluation / Rebuild Scope
├─ Return Reason
├─ Routing Policy / Method Ref
├─ Predecessor / Related Return Ref
└─ Provenance
~~~

This is a logical trace contract, not a requirement for a central service / DB table.

---

## 27.25 Material Dependency Gate

An upstream change does not automatically rebuild the whole lineage.

~~~text
Upstream changed
↓
Was this exact downstream artifact materially dependent on it?
├─ NO
│   → no rebuild required
└─ YES
    → current-use validity handling
    → rebuild from nearest owner
~~~

Important:

~~~text
Any update
!= Global rebuild
~~~

Relied-upon exact refs / dependency context are used to determine impact.

---

## 27.26 Parallel Fast Safety + Semantic Repair

One downstream event may require more than one route.

Example:

~~~text
Actual Exposure exists
+
Trade Thesis / Knowledge basis materially degrades
~~~

Possible response:

~~~text
Fast Runtime / R4 Safety Route
+
Slow Semantic / Research Return Route
~~~

These are parallel responsibilities.

~~~text
Fast Safety
!= Knowledge Retirement
!= Historical Rewrite
!= automatic Semantic Repair
~~~

Likewise:

~~~text
Research Return
!= immediate Position Action
~~~

This preserves the Two-Speed architecture.

---

## 27.27 Return Record Immutability

A Return / Re-evaluation request is historical.

Do not mutate:

~~~text
old EVA
old EAS
old Advancement Record
old Trade Thesis
old Snapshot
old Decision Thesis
~~~

Instead:

~~~text
Return Event
↓
new upstream assessment / evaluation
↓
new descendant lineage
~~~

Repeated loops create immutable lineage, not overwrite loops.

---

## 27.28 Return Route vs Current-Use Validity

Return routing does not itself rewrite semantic truth.

It may produce / consume Current-Use Validity findings.

Example:

~~~text
TT-101
historically valid artifact

Current-use validity
= LOST

Return Route
= Economic Re-evaluation
~~~

TT-101 remains unchanged.

---

## 27.29 Unknown / Dependency in Return Routing

Unknown resolution does not automatically choose one global route.

Route depends on where the Unknown is material.

Examples:

~~~text
Economic-only Unknown resolved
→ EVA / EAS

Thesis-material Unknown resolved
→ new Snapshot / Synthesis

Research truth Unknown resolved
→ Research / Knowledge path
~~~

Dependency discovery follows the same materiality rule.

~~~text
Decision dependency change
→ Decision / Snapshot path

Cross-Candidate Economic dependency change
→ EVA / Joint Economic Envelope path
~~~

---

## 27.30 Runtime Findings

Runtime detection location does not imply R4 ownership of semantic truth.

Examples:

~~~text
Execution spread worsens
→ Economic / R4 route depending on evaluated envelope

Direction / Candidate semantics need change
→ Candidate Formation

Source Thesis fails
→ Snapshot / Decision Synthesis

Canonical Knowledge challenged
→ Applicability / Lifecycle / Research

Actual capital constraint
→ R4
~~~

Runtime may trigger fast protection in parallel.

---

## 27.31 Error / Integrity Route

Contract / integrity failure is not a business disposition.

~~~text
Integrity Failure
!= WAIT
!= ABSTAIN
!= Negative EV
!= R4 BLOCK
~~~

Route to the owner of the broken contract / artifact.

Only after valid replacement artifacts exist may normal downstream flow resume.

---

## 27.32 R3-INT-014 Core Invariants

~~~text
RR-01 Return routing is based on changed meaning, not detection location.
RR-02 Return Router Common Rule != universal router service.
RR-03 Return routing does not own canonical truth.
RR-04 Return routing does not mutate historical artifacts.
RR-05 Route to the nearest upstream semantic owner.
RR-06 Do not rewind farther than necessary.
RR-07 Do not keep a change downstream when downstream does not own that meaning.
RR-08 Material dependency is checked before rebuilding descendants.
RR-09 Any upstream update != global rebuild.
RR-10 Rebuild only materially affected descendants.
RR-11 Capital-only change stays in R4 when semantic / economic envelope remains valid.
RR-12 Economic change routes to EVA / EAS when Candidate / Thesis remain valid.
RR-13 Candidate semantic change routes to Candidate Formation.
RR-14 Decision-input / Thesis change creates new Snapshot / Synthesis branch.
RR-15 Knowledge applicability / use change routes to Applicability / Constraint / Lifecycle owner first.
RR-16 Knowledge validity / novel causal question routes to Research / Validation authority.
RR-17 Data / Temporal / Integrity defect routes to its owning contract.
RR-18 Integrity Failure != WAIT.
RR-19 Integrity Failure != ABSTAIN.
RR-20 Integrity Failure != negative EV.
RR-21 Type A-D R4 classification remains compatible with common router.
RR-22 Type D is refined by actual Decision / Applicability / Research ownership.
RR-23 Return Routing Assessment is trace, not semantic authority.
RR-24 Return / Re-evaluation records are immutable.
RR-25 Repeated return loops create new lineage, not overwrite loops.
RR-26 Current-use invalidation != historical mutation.
RR-27 Unknown resolution routes according to material scope.
RR-28 Dependency discovery routes according to dependency type / materiality.
RR-29 Decision dependency != Economic dependency.
RR-30 Detection in Runtime != semantic ownership by Runtime.
RR-31 Actual Exposure safety may create a parallel R4 fast route.
RR-32 Fast Safety != Semantic Repair.
RR-33 Fast Safety != Knowledge Retirement.
RR-34 Research Return != immediate Position Action.
RR-35 Trade Thesis Invalidation != automatic EXIT.
RR-36 R4 BLOCK != upstream semantic invalidity.
RR-37 No Fill does not create Runtime Assumption Set.
RR-38 New valid upstream outputs rebuild forward through normal authority boundaries.
RR-39 Downstream must use exact new artifacts; stale floating current refs are prohibited.
RR-40 Historical Replay remains based on the original lineage, not later return outcomes.
~~~

---

## 27.33 Package D End-to-End Contract

Forward:

~~~text
Exact Decision Candidate Version
↓
Economic Value Assessment
↓
Evaluation Availability / Sufficiency Assessment
↓
Candidate Advancement
↓
ADVANCE
↓
Trade Thesis Formation
↓
Adoption Assessment
↓
Adoption Authorization
↓
Trade Thesis Writer
↓
Immutable Trade Thesis
↓
R4 Economic / Capital Decision
↓
Execution
↓
Actual Exposure?
↓
Runtime Assumption Set [only if exposure exists]
~~~

Backward:

~~~text
R4 / Runtime / downstream Finding
↓
Return Routing Assessment
↓
What meaning actually changed?
↓
Material dependency check
↓
Nearest semantic owner
↓
New upstream artifact / assessment
↓
Rebuild forward through exact descendant lineage
~~~

---

## 27.34 Package D Cross Check

Cross-check dimensions:

~~~text
EVA vs Availability / Sufficiency ownership
Availability / Sufficiency vs Advancement authority
Advancement vs Trade Thesis Formation
Formation vs Adoption
Adoption vs Writer
Trade Thesis vs R4 authority
Trade Thesis vs Runtime activation
Current-Use Validity vs Historical integrity
Backward routing semantic ownership
Return routing material dependency
Fast Safety vs Slow Semantic / Research return
Unknown continuity
Dependency continuity
Temporal / Availability integrity
Decision Lineage immutability
~~~

Result:

~~~text
EVA / EAS Boundary
= PASS

EAS / Advancement Boundary
= PASS

Advancement / Trade Thesis Formation Boundary
= PASS

Formation / Adoption Boundary
= PASS

Adoption / Writer Boundary
= PASS

Trade Thesis / R4 Boundary
= PASS

Trade Thesis / Runtime Activation Boundary
= PASS

Historical Immutability
= PASS

Current-Use Validity Separation
= PASS

Backward Routing Ownership
= PASS

Material Dependency Routing
= PASS

Fast Safety / Slow Repair Separation
= PASS

Unknown Continuity
= PASS

Dependency Continuity
= PASS

Temporal / Availability Integrity
= PASS

Decision Lineage Traceability
= PASS

Blocking Issue
= NONE
~~~

---

## 27.35 Package D Clarifications

~~~text
PD-HO-001
Valid Partial EVA
!= Invalid EVA.

PD-HO-002
Evaluation Sufficiency is relative to an explicit Versioned Requirement Profile.

PD-HO-003
Trade Thesis Formation
!= Adoption
!= Materialization.

PD-HO-004
Backward Return routes to the nearest semantic owner,
not automatically to Economic Value.

PD-HO-005
Fast R4 / Runtime safety may run in parallel with
slow semantic / research repair.

PD-HO-006
Return routing invalidates current-use only where material;
it never rewrites historical artifacts.
~~~

---

## 27.36 R3 Integration Repair Status After Package D

~~~text
Package A — Knowledge Foundation
= COMPLETE / CHECKPOINTED

Package B — Temporal / Reproducibility
= COMPLETE / CHECKPOINTED

Package C — Decision Contract / Decision Lineage
= COMPLETE / CHECKPOINTED

Package D — Economic / Trade Exit / Return Router
= COMPLETE / WORKING CHECKPOINT

R3 Integration Repair blocking issue
= NONE
~~~

Remaining planned work:

~~~text
Adjacent Contract Recheck
↓
STEP 8 Destruction Test
↓
R3 Integration Final Review
↓
Formal adoption decision later
~~~

---

## 27.37 Save / Adoption Boundary

Checkpoint 020 saves Package D as Working Repair only.

Formal Current remains unchanged.

Do not modify:

~~~text
00_AI/AI_CONTEXT.md
00_HUMAN/HUMAN_MAP.md
02_ARCHITECTURE/
~~~

Still not decided here:

~~~text
DB table structure
Python classes
physical Return Router implementation
centralized vs distributed routing runtime
final enum names
final exact field names
runtime scheduling / concurrency model
final fail-open / fail-closed implementation
formal adoption into 02_ARCHITECTURE
~~~

---

## 27.38 Checkpoint Result

~~~text
Checkpoint 020
R3 Integration Repair
Package D — Economic / Trade Exit & Backward Return Router
= SAVED WORKING REPAIR

R3-INT-005
Evaluation Availability / Sufficiency
= REPAIRED / WORKING

R3-INT-012
Trade Thesis Revision / Adoption / Immutability
= REPAIRED / WORKING

R3-INT-014
Backward Return Router Common Rule
= REPAIRED / WORKING

Package D Cross Check
= PASS

PD-HO-001
Valid Partial EVA != Invalid EVA
= CLARIFIED

PD-HO-002
Sufficiency is Requirement-Profile relative
= CLARIFIED

PD-HO-003
Formation != Adoption != Materialization
= CLARIFIED

PD-HO-004
Return to nearest semantic owner
= CLARIFIED

PD-HO-005
Fast Safety may run parallel with slow repair
= CLARIFIED

PD-HO-006
Return routing never rewrites history
= CLARIFIED

Blocking Issue
= NONE

Formal Current Architecture
= UNCHANGED

NEXT
=
Adjacent Contract Recheck
→ STEP 8 Destruction Test
→ R3 Integration Final Review
~~~

