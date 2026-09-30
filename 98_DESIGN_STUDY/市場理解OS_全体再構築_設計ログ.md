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
