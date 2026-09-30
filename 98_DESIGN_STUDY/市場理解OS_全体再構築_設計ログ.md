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
