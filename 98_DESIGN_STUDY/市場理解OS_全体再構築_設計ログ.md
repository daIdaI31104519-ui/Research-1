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
