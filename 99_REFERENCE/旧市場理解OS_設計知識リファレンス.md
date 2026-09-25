# 旧市場理解OS — 設計知識リファレンス

**Document Role:** Legacy Knowledge Master Index / Comparison Reference  
**Status:** DRAFT / LEGACY REVIEW IN PROGRESS  
**Structure Review:** REVIEWED  
**Current Design Authority:** NONE  
**Parent Policy:** `99_REFERENCE/README.md`  
**Parent Workflow:** `00_AI/AI_WORKFLOW.md`  
**Legacy Repository:** `daIdaI31104519-ui/-OS-`  

**Purpose:**  
旧市場理解OSに存在する設計思想・Concept・Object・Role・State・Lifecycle・失敗・FIX理由を、Source追跡可能な形で圧縮・索引化し、Current DesignのDefinition / Detailed Design / Contract設計時に安全に検索・比較できるLegacy Knowledge Referenceを作る。

---

# 0. Role / Boundary

この文書は、

> **旧市場理解OSの設計知識を検索・比較するためのMaster Index**

である。

Legacy Knowledgeの扱い方そのものは、

```text
99_REFERENCE/README.md
```

の `LEGACY REVIEW GATE` を正本とする。

この文書では、そのRuleを詳細再定義しない。

基本認識:

```text
このReference
≠ Current Design

このReference
≠ Current Owner

Legacy Definition
≠ Current Definition

Review済み
≠ 採用済み

Recommendation
≠ Decision
```

この文書の責任は、

```text
WHAT WAS THERE
+
WHAT FAILED
+
WHERE IT CAME FROM
+
HOW IT RELATES TO CURRENT
```

を検索可能にすることである。

---

# 1. Legacy Source Snapshot

このReferenceが、旧Repositoryのどの状態を基準にしているかを固定する。

```text
LEGACY_SOURCE_REPOSITORY:
daIdaI31104519-ui/-OS-

LEGACY_SOURCE_REF:
main

LEGACY_SOURCE_COMMIT_SHA:
557d338e30937aebb661aad295a54f75706f90b7

LEGACY_SOURCE_TREE_SHA:
1a8968030720020373ad74562f714491d25d6dc0

SNAPSHOT_CAPTURED_AT:
2026-09-18
```

重要:

```text
Source Snapshot取得済み
≠
Source本文Review済み
```

旧RepoのHEADが後から変更された場合でも、このReferenceが何を基準に作られたか追跡できるようにする。

---

# 2. Legacy Source Inventory

旧RepositoryのSourceを4Groupへ分類する。

## 2.1 Summary / 全体構想

```text
市場理解OS まとめ案 1.md
市場理解OS まとめ案 2.md
市場理解OS まとめ案 3.md
市場理解OS まとめ案 4.md
市場理解OS まとめ案 5.md
市場理解OS まとめ案 6.md
市場理解OS まとめ案 7.md
市場理解OS まとめ案 8.md
市場理解OS まとめ案 9.md
市場理解OS まとめ案 10.md
市場理解OS まとめ案 11.md
```

主用途:

```text
旧OS全体像
Architecture
Research / Production Flow
主要Concept
設計思想
重要責任境界
```

---

## 2.2 Dictionary

```text
01_DICTIONARY/OBJECT_DICTIONARY.md
01_DICTIONARY/ROLE_DICTIONARY.md
01_DICTIONARY/STATE_DICTIONARY.md
01_DICTIONARY/SECURITY_DICTIONARY.md
01_DICTIONARY/CREDENTIAL_DICTIONARY.md
01_DICTIONARY/DATA_CLASSIFICATION_DICTIONARY.md
```

主用途:

```text
Object
Concept
Role
State
Lifecycle
Security
Credential
Data Classification
Authority
Responsibility
```

の旧定義確認。

---

## 2.3 Governance

```text
00_GOVERNANCE/DESIGN_CHANGE_RULES.md
00_GOVERNANCE/GIT_RULES.md
```

主用途:

```text
Legacy Design Governance
Change Rule
Authority
Legacy Git Operation
```

の確認。

Current `AI_WORKFLOW.md` のRuleとは混同しない。

---

## 2.4 FIX / Backup

```text
99_ARCHIVE/BACKUP/
```

確認対象:

```text
FIX-001 Observation
FIX-002 Hypothesis / Production State
FIX-003 Research Plan State
FIX-004 Edge / Knowledge State
FIX-005 Object Naming
FIX-006 Feature / Priority / DNA Cycle
FIX-007 Market Event Responsibility
FIX-008 Production Thesis Builder
FIX-009 Entry / Production Evidence
FIX-010 State Transition Event
FIX-011 Research Plan Two-Axis State
FIX-012 Lifecycle / Aging / Production Separation
FIX-013 State Authority Matrix
FIX-014 Source Metadata / Lifecycle Separation
FIX-015 Approval Decision
FIX-016 Production / Risk Stage Separation
FIX-017 Knowledge Lifecycle
FIX-018A Security / Identity / Authorization
FIX-018B Credential Governance
FIX-018C Data Classification
```

主用途:

> **何を直したかだけでなく、なぜ直す必要があったかを再利用する。**

---

# 3. Source Review Progress

Source Fileをどこまで読んだかは、Concept Review Statusと分離する。

使用するStatus:

```text
SOURCE_REVIEW_STATUS =
NOT_REVIEWED
IN_REVIEW
PARTIAL
REVIEWED
```

重要:

```text
SOURCE_REVIEW_STATUS
≠
LEGACY_REVIEW_STATUS
```

意味:

```text
SOURCE_REVIEW_STATUS
=
元Fileそのものをどこまで確認したか

LEGACY_REVIEW_STATUS
=
特定ConceptをCurrent Designと比較した結果
```

初期状態:

| Source Group | SOURCE_REVIEW_STATUS | Purpose |
|---|---|---|
| まとめ案 1〜11 | REVIEWED | Legacy全体像 / Research Evidence / Production / Governance |
| OBJECT_DICTIONARY | NOT_REVIEWED | Object / Concept |
| ROLE_DICTIONARY | NOT_REVIEWED | Role |
| STATE_DICTIONARY | NOT_REVIEWED | State / Lifecycle |
| SECURITY_DICTIONARY | NOT_REVIEWED | Security |
| CREDENTIAL_DICTIONARY | NOT_REVIEWED | Credential |
| DATA_CLASSIFICATION_DICTIONARY | NOT_REVIEWED | Data Classification |
| DESIGN_CHANGE_RULES | NOT_REVIEWED | Legacy Governance |
| GIT_RULES | NOT_REVIEWED | Legacy Git Governance |
| FIX-001〜018C | NOT_REVIEWED | Failure / Change Reason |

---

# 4. Legacy Whole-System Overview

`市場理解OS まとめ案 1〜11` のReview後に作成する。

旧OS全体を再設計するSectionではなく、

> **旧市場理解OSが何を作ろうとしていたのかを短時間で把握するための圧縮Summary**

とする。

## 4.1 Legacy Mission / Goal

```text
<TODO>
```

## 4.2 Legacy Architecture

```text
<TODO>
```

## 4.3 Legacy Market Understanding Flow

```text
<TODO>
```

## 4.4 Legacy Research Flow

```text
<TODO>
```

## 4.5 Legacy Knowledge Flow

```text
<TODO>
```

## 4.6 Legacy Production / Trading Flow

```text
<TODO>
```

## 4.7 Legacy Feedback / Re-Research Flow

```text
<TODO>
```

## 4.8 Legacy Governance / Authority Model

```text
<TODO>
```

---

# 5. Legacy Concept Index

Legacy Conceptを素早く検索するためのMaster Index。

| Legacy Concept | Category | Primary Legacy Source | LEGACY_REVIEW_STATUS | Current Relation | Detail |
|---|---|---|---|---|---|
| `<Concept>` | `<Category>` | `<Path>` | NOT_REVIEWED | UNKNOWN | `<Section>` |

基本Category:

```text
Observation / Data
Market Understanding
Research
Causal
Evidence
Market DNA
Knowledge
Applicability
Decision
Production
Trade
Risk
State / Lifecycle
Role
Authority
Governance
Security
Credential
Data Classification
Other
```

原則:

> Categoryを増やす前に既存Categoryへ整理できないか確認する。

---

# 6. Legacy → Current Concept Map

旧ConceptとCurrent Research-1の関係を検索するためのIndex。

| Legacy Concept | Current Concept / Owner Candidate | Relationship | Conflict | Recommendation |
|---|---|---|---|---|
| `<Legacy>` | `<Current / UNKNOWN>` | UNKNOWN | UNKNOWN | UNDECIDED |

Relationship候補:

```text
SAME_RESPONSIBILITY
PARTIAL_OVERLAP
RENAMED
SPLIT
MERGED
DIFFERENT_RESPONSIBILITY
NO_CURRENT_EQUIVALENT
UNKNOWN
```

重要:

```text
同じ名前
≠ 同じ責任

違う名前
≠ 違う責任
```

名称ではなくResponsibilityを比較する。

---

# 7. Important Concept Reviews

このSectionには、今後Current Designで再利用価値が高いLegacy Conceptだけ詳細Reviewを置く。

全Legacy Objectを無条件に詳細化しない。

---

## Concept: `<Legacy Concept Name>`

### Legacy Definition

```text
<TODO>
```

旧Sourceが支持している内容だけを書く。

### Legacy Responsibility

```text
<TODO>
```

### Legacy Inputs / Outputs

```text
Inputs:
<TODO>

Outputs:
<TODO>
```

### Legacy Relations

```text
Upstream:
<TODO>

Downstream:
<TODO>

Related Object:
<TODO>

Related Role:
<TODO>

Related State:
<TODO>
```

### Legacy State / Lifecycle

```text
<TODO / NOT_APPLICABLE / UNKNOWN>
```

### Legacy Authority

```text
Research Authority:
<TODO / UNKNOWN>

Production Authority:
<TODO / UNKNOWN>

Risk Authority:
<TODO / UNKNOWN>

State Transition Authority:
<TODO / UNKNOWN>

Approval Authority:
<TODO / UNKNOWN>
```

存在しないAuthorityを推測で追加しない。

### Fix / Failure History

```text
Problem:
<TODO>

Why It Failed / Changed:
<TODO>

Legacy Resolution:
<TODO>
```

### Current Research-1 Relation

```text
<TODO / UNKNOWN>
```

### Current Owner Candidate

```text
<TODO / UNKNOWN>
```

Reference自身をCurrent Ownerにしない。

### Difference

```text
Legacy:
<TODO>

Current:
<TODO>

Important Difference:
<TODO>
```

LegacyとCurrentを自然な文章へ融合しない。

### LEGACY_CONFLICT_STATUS

```text
UNKNOWN
```

候補:

```text
NONE
MINOR
MAJOR
UNKNOWN
```

### LEGACY_REVIEW_STATUS

```text
NOT_REVIEWED
```

候補:

```text
NOT_REVIEWED
REFERENCE_ONLY
ADOPTABLE
PARTIAL_REUSE
REDESIGN_REQUIRED
REJECTED
```

### LEGACY_REUSE_RECOMMENDATION

```text
UNDECIDED
```

候補:

```text
ADOPT
SIMPLIFY
MERGE
REDESIGN
REJECT
REFERENCE_ONLY
UNDECIDED
```

RecommendationはCurrent Design Decisionではない。

### Reuse Value

```text
Definition Value:
<TODO>

Failure Knowledge Value:
<TODO>

Responsibility Separation Value:
<TODO>

State / Lifecycle Value:
<TODO>

Other:
<TODO>
```

### REVIEWED_AGAINST

```text
Current Owner Path:
<TODO>

Current Version / Baseline:
<TODO>

Review Date:
<TODO>
```

### Source Pointer

```text
Primary Legacy Source:
<TODO>

Secondary Legacy Source:
<TODO>

Legacy Commit:
557d338e30937aebb661aad295a54f75706f90b7

Related FIX:
<TODO>

Related Backup:
<TODO>
```

---


## 7.1 Review Batch A — Research Evidence / Knowledge Maintenance

**Review Date:** 2026-09-21  
**Review Scope:** 旧市場理解OSのResearch Evidence系ConceptをCurrent \`03_RESEARCH\` / \`04_KNOWLEDGE_APPLICABILITY\` と比較し、再利用候補を整理する。  
**Current Design Authority:** NONE  
**Current Design Status:** NOT_ADOPTED  

このBatchは、

\`\`\`text
Legacy Source-backed Fact
+
Current Design Relation
+
Derived Reuse Proposal
\`\`\`

を分離して記録する。

重要:

\`\`\`text
このSectionに保存
≠ Current Designへ採用

Formal Definition Candidate
≠ Current正式Definition

Reuse Recommendation
≠ Current Design Decision
\`\`\`

### 7.1.1 Review Summary

| Concept | Legacy Support | Current Relation | Review Result | Reuse Recommendation | Current Status |
|---|---|---|---|---|---|
| Demo Forward | STRONG | Forward Evidence / Validation Channelあり | PARTIAL_REUSE | MERGE / REFINE | NOT_ADOPTED |
| Evidence Channel | STRONG | Current 03に明示 | ADOPTABLE | MERGE | NOT_ADOPTED |
| Evidence Role | PARTIAL | Source / Role分離要求あり | PARTIAL_REUSE | REFINE / MERGE | NOT_ADOPTED |
| Evidence Outcome | WEAK / IMPLICIT | Currentに独立Conceptなし | REDESIGN_REQUIRED | DERIVED PROPOSAL | NOT_ADOPTED |
| Evidence Evaluation Status | NO DIRECT LEGACY OBJECT | Currentに独立Conceptなし | DERIVED | NEW PROPOSAL | NOT_ADOPTED |
| Shared Evidence | STRONG | Current 04に明示 | ADOPTABLE | MERGE | NOT_ADOPTED |
| Evidence Dependency | PARTIAL / STRONG AT HYPOTHESIS LEVEL | Overlap / Derived Relationあり | PARTIAL_REUSE | REFINE / MERGE | NOT_ADOPTED |
| Evidence Strength | STRONG | Current 04でApplicabilityと分離 | ADOPTABLE | MERGE / REFINE | NOT_ADOPTED |
| Evidence Profile | STRONG AS EVIDENCE SEPARATION / PACKAGE | Current 04に明示 | PARTIAL_REUSE | MERGE / OWNERSHIP REFINE | NOT_ADOPTED |
| Hypothesis Assessment | PARTIAL / IMPLICIT | Currentに独立Objectなし | REDESIGN_REQUIRED | DERIVED PROPOSAL | NOT_ADOPTED |
| Research Result | STRONG | Current 03に明示 | ADOPTABLE | MERGE / REFINE | NOT_ADOPTED |
| Validation Gate | PARTIAL / RELATED VALIDATION | Current 03に明示 | PARTIAL_REUSE | CURRENT REFINEMENT | NOT_ADOPTED |
| Validated Research Result | PARTIAL / RELATED VALIDATION | Current 03に明示 | PARTIAL_REUSE | CURRENT REFINEMENT | NOT_ADOPTED |
| Knowledge Admission | PARTIAL | Current 04でAdmission / Promotion一体 | PARTIAL_REUSE | SPLIT / REFINE | NOT_ADOPTED |
| Knowledge Promotion | PARTIAL | Current 04でAdmission / Promotion一体 | PARTIAL_REUSE | SPLIT / REFINE | NOT_ADOPTED |
| Knowledge Record | Knowledge Object思想あり | Current 04にContext候補あり | PARTIAL_REUSE | REFINE / DEFINE | NOT_ADOPTED |
| Knowledge Pool | STRONG | Current 04に明示 | ADOPTABLE | CURRENTを優先 | NOT_ADOPTED |
| Applicability Evaluation | PARTIAL / IMPLICIT | Current 04に明示 | PARTIAL_REUSE | CURRENT REFINEMENT | NOT_ADOPTED |
| Applicability Assessment | NO DIRECT LEGACY OBJECT | Current 04にConcept候補あり | PARTIAL_REUSE | CURRENT REFINEMENT | NOT_ADOPTED |
| Applicable Knowledge Set | PARTIAL / PRODUCTION APPLICABILITY思想 | Current 04に明示 | PARTIAL_REUSE | CURRENT REFINEMENT | NOT_ADOPTED |
| Evaluation Status | NO DIRECT LEGACY OBJECT | Current state候補から分離Proposal | DERIVED | NEW PROPOSAL | NOT_ADOPTED |
| Constraint Gate Status | PARTIAL / Constraint思想あり | Current Constraint Checkを精密化 | DERIVED | NEW PROPOSAL | NOT_ADOPTED |
| Candidate Retrieval Trace | NO DIRECT LEGACY OBJECT | Current Runtime検索責任の精密化 | DERIVED | NEW PROPOSAL | NOT_ADOPTED |
| Legacy 05 Decision Boundary | STRONG Production/Signal思想 | Current 04後段として再配置 | PARTIAL_REUSE | SPLIT / REFINE | NOT_ADOPTED |
| Decision Context Assembly | PARTIAL / Builder Input Assembly | Current 04出力を固定するDerived Concept | DERIVED | NEW PROPOSAL | NOT_ADOPTED |
| Knowledge Integration | STRONG Dependency/Contradiction思想 | Selectionを04へ移し05で再設計 | PARTIAL_REUSE | SPLIT / REFINE | NOT_ADOPTED |
| Trade Thesis Construction | STRONG | Current 05候補 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Trade Thesis | STRONG | Current 05候補 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Decision Evaluation | STRONG Signal Engine思想 | Current 05候補へ再設計 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Decision Result | STRONG SignalDecision思想 | Current 05候補へ再設計 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Decision Scope | NO DIRECT LEGACY OBJECT | 複数Horizon比較問題のDerived Correction | DERIVED | NEW PROPOSAL | NOT_ADOPTED |
| Expected Value Assessment | PARTIAL / expected_value_profile | Trade Thesisとの責任分離Proposal | DERIVED | REFINE | NOT_ADOPTED |
| Defense / Risk Boundary | STRONG Pre-Trade Defense思想 | 05後段Safety Domainとして再配置 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Defense Evaluation | STRONG | Safety Gateへ精密化 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| DefenseDecision | STRONG | ALLOW / REDUCE / BLOCKを維持 | ADOPTABLE | REFINE | NOT_ADOPTED |
| DefenseEvaluationResult | NO DIRECT LEGACY OBJECT | BLOCKとFail-Closed分離のDerived Boundary | DERIVED | NEW PROPOSAL | NOT_ADOPTED |
| RiskState | STRONG | Current Risk Permissionへ限定 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Risk Governance / RiskState Transition | STRONG FIX-013/015/016 | Risk専用Contractへ精密化 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Emergency Fast Path | STRONG | Safety Restrictionのみ高速化 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Recovery Strict Path | STRONG | Permission Expansionを厳格化 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Defense → Execution Contract | STRONG FIX-009境界 | Current Execution Admissionへ再設計 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| EntryThesis | STRONG FIX-009 / OBJ-PRD-010 | Current Entry Snapshotへ再設計 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| OrderIntent | STRONG OBJ-PRD-008 / ROLE-EXEC-001 | Exchange-independent execution intentへ精密化 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| ExecutionRecord | STRONG OBJ-PRD-009 / ROLE-ADP-002 | Requested / Submitted / Actualを分離 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| ProductionEvidence | STRONG OBJ-PRD-013 / FIX-009 | LIVE Research Evidenceへ精密化 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Execution Integrated Flow | STRONG | Defense境界からLive Evidenceまで統合 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| TradeResult / Post-Trade Entry Boundary | STRONG OBJ-PRD-014 | Final Trade FactとAnalysisを分離 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| OutcomeAnalysisResult | STRONG OBJ-POST-001 | Outcome / Opportunity / System Integrityを分離 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| TradeThesisEvaluation | STRONG OBJ-POST-002 | PnL非依存のThesis全体評価 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| HypothesisAttribution | STRONG OBJ-POST-003 | CurrentではThesis Member Attributionへ意味拡張 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| DefenseDecisionEvaluation | STRONG OBJ-POST-004 | Pre-Trade Defense Evaluationとの命名衝突を分離 | PARTIAL_REUSE | RENAME / REFINE | NOT_ADOPTED |
| SupervisorEvaluation | STRONG OBJ-POST-005 | Detection / Timing / Stability / Utilityへ精密化 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| DemoLiveDivergence | STRONG OBJ-POST-006 | Channel比較とComparability Gateへ精密化 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| CounterfactualResult | STRONG OBJ-POST-007 | Hindsight防止 / Minimal Interventionを追加 | ADOPTABLE / PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Post-Trade Integrated Flow | STRONG ROLE-ANL-001 | Trade Fact→Analysis→Research Candidateを統合 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Finding Extractor Common Contract | DERIVED | Analysis→Finding共通Gate | CURRENT_DERIVED | ADD | NOT_ADOPTED |
| Finding Normalizer Common Contract | DERIVED | Draft→Canonical Finding標準化 | CURRENT_DERIVED | ADD | NOT_ADOPTED |
| Finding Type Registry v1.0 | DERIVED | Post-Trade 7系統のCanonical Finding語彙 | CURRENT_DERIVED | ADD | NOT_ADOPTED |
| Analysis→ResearchCandidate Contract | DERIVED + 03_RESEARCH | Finding→Candidate Promotion境界 | CURRENT_DERIVED | ADD | NOT_ADOPTED |
| Research Router / ResearchRoute | STRONG ROLE-RTR-001 + OBJ-POST-008 | Research Domain Routingへ責任補正 | PARTIAL_REUSE | REFINE | NOT_ADOPTED |
| Finding Pipeline Integrated Flow | DERIVED + 03_RESEARCH | Analysis→Finding→Candidate→Intake→Routerを統合 | CURRENT_DERIVED | ADD | NOT_ADOPTED |

---

## 7.2 Demo Forward

### Legacy Source-backed Fact

Legacyでは、Demo Forwardを、

\`\`\`text
Hypothesis / Hypothesis SetをT0で固定
↓
T0以降の新しい市場Dataだけを使用
↓
Forward Trial
↓
Evidence Package
\`\`\`

として扱う案が存在する。

Historical / OOS / Demo Forward / Liveは同質Evidenceとして単純合算しない。

**Primary Legacy Sources:**

\`\`\`text
市場理解OS まとめ案 5.md
市場理解OS まとめ案 10.md
市場理解OS まとめ案 11.md
\`\`\`

### Current Research-1 Relation

Current \`03_RESEARCH\` はすでに、

\`\`\`text
Forward Validation
Forward Evidence
Historical / OOS / Forward / Stress / LiveのChannel分離
\`\`\`

を持つ。

### Derived Reuse Proposal

> **Demo Forward = 特定VersionのResearch Target / HypothesisをT0でFreezeし、T0以降に新しく到着したDataだけを使ってForward Evidenceを生成する03_RESEARCH内のValidation Method候補。**

Responsibility候補:

\`\`\`text
Version Freeze
T0境界
Future-only Validation
Forward Evidence生成
Process FailureとHypothesis Failureの分離
\`\`\`

Does Not Own:

\`\`\`text
Knowledge Promotion
Applicability
Signal
Trade Permission
Live Execution Authority
\`\`\`

禁止候補:

\`\`\`text
T0前後Data Leakage
Outcomeを見た後の同Version書換え
HistoricalとForwardの同質合算
Demo PASSからProductionへ直結
\`\`\`

関係:

\`\`\`text
Demo Forward
= HOW

Forward Evidence
= RESULT

Evidence Channel = FORWARD
= IDENTITY
\`\`\`

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
MERGE / REFINE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.3 Evidence Channel

### Legacy Source-backed Fact

LegacyはHistorical / OOS / Demo Forward / Stress / Live等のEvidence Sourceを分離し、単一件数・単一勝率へ潰さない思想を持つ。

### Current Research-1 Relation

Current \`03_RESEARCH\` に以下が明示済み。

\`\`\`text
Runtime / Observational Evidence
Historical Evidence
OOS Evidence
Forward Evidence
Stress Evidence
Production / Live Evidence
\`\`\`

### Derived Reuse Proposal

> **Evidence Channel = EvidenceがどのValidation / Observation経路から生成されたかというIdentity / Contextを保持する分類責任。**

Evidence Channelは、

\`\`\`text
Hypothesis Verdict
Evidence Strength
Knowledge Promotion
Applicability
Trade Permission
\`\`\`

を決定しない。

Different ChannelであってもIndependent Evidenceとは限らない。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
NONE

LEGACY_REVIEW_STATUS:
ADOPTABLE

LEGACY_REUSE_RECOMMENDATION:
MERGE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.4 Evidence Role

### Legacy Source-backed Fact

LegacyにはSupporting / Conditional / Contradicting等の役割分離思想があり、Current 03にもEvidence Source / Roleを区別する要求が存在する。

### Derived Reuse Proposal

> **Evidence Role = Evidenceが特定Research Targetに対して何を確認する目的で使われるかを表すTarget-relative Relationship Context。**

詳細Taxonomy候補:

\`\`\`text
SUPPORTING
CONTRADICTING
DISCRIMINATING
CONDITIONING
BOUNDARY
CONTEXTUAL
PROCESS_VALIDATION
\`\`\`

重要:

\`\`\`text
Role
≠ Outcome
≠ Strength
≠ Channel
≠ Source
\`\`\`

同一EvidenceがTargetごとに異なるRoleを持つことを許容する。

Taxonomy自体はLegacy原文ではなくDerived Proposal。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
NONE / MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
REFINE / MERGE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.5 Evidence Outcome / Evidence Evaluation Status

### Legacy Source-backed Fact

Legacy / CurrentにはSUPPORTED / REFUTED / INCONCLUSIVE等のResearch Result思想はあるが、Evidence単位の独立したEvidence Outcome Object / Definitionは確認できない。

したがって、以下はLegacy DefinitionではなくDerived Proposal。

### Derived Reuse Proposal — Evidence Outcome

> **Evidence Outcome = Evidenceを特定Research Targetに対して定義されたRoleに沿って評価した際、実際に何を示したかを表すTarget-relative Result Context。**

Outcome候補:

\`\`\`text
SUPPORTIVE
CONTRADICTING
NEUTRAL
MIXED
INCONCLUSIVE
UNKNOWN
\`\`\`

### Important Correction — Evaluation Statusを分離

\`NOT_OBSERVED\` と \`INVALID\` はOutcome Directionと同一Enumへ入れない。

別軸候補:

\`\`\`text
Evidence Evaluation Status
├─ VALID
├─ INVALID
├─ NOT_OBSERVED
├─ NOT_EVALUATED
└─ UNKNOWN
\`\`\`

理由:

\`\`\`text
Outcome
= 何を示したか

Evaluation Status
= そもそも評価可能 / 観測可能だったか
\`\`\`

したがって、

\`\`\`text
INVALID
≠ CONTRADICTING

NOT_OBSERVED
≠ 自動的にCONTRADICTING
\`\`\`

とする。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
REDESIGN_REQUIRED

LEGACY_REUSE_RECOMMENDATION:
DERIVED PROPOSAL

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.6 Shared Evidence / Evidence Dependency

### Shared Evidence — Source-backed Fact

LegacyではHypothesis数をConfidenceとして使わず、

\`\`\`text
shared_evidence_ids
dependency
redundancy
common_cause
mechanism_group
\`\`\`

等を認識する案が存在する。

Current 04にも、

\`\`\`text
Shared Evidence
Shared Cause
Derived Relationship
Duplicate / Overlap
\`\`\`

が存在する。

### Shared Evidence — Derived Definition

> **Shared Evidence = 複数Hypothesis / Research Result / Knowledge等が同一または実質的に重複するEvidence / Observation / Market Event / Source等を共有しているRelationship。**

目的:

> 同じEvidenceを複数の独立支持として二重計上しない。

### Evidence Dependency — Derived Definition

> **Evidence Dependency = Evidenceや評価の意味・成立が、別Evidence / Observation / Source / Market Event / Derived Feature / Research Result等へ依存しているRelationship。**

概念候補:

\`\`\`text
Direct Dependency
Derived Dependency
Common Source Dependency
Common Event Dependency
Common Cause Dependency
Temporal Dependency
Research Dependency
Unknown Dependency
\`\`\`

具体Enumはまだ固定しない。

重要:

\`\`\`text
Shared
≠ Dependency

Dependency
≠ Invalid

Dependency
≠ Causality Proof
\`\`\`

### Review

\`\`\`text
Shared Evidence:
LEGACY_CONFLICT_STATUS = NONE
LEGACY_REVIEW_STATUS = ADOPTABLE
LEGACY_REUSE_RECOMMENDATION = MERGE

Evidence Dependency:
LEGACY_CONFLICT_STATUS = MINOR
LEGACY_REVIEW_STATUS = PARTIAL_REUSE
LEGACY_REUSE_RECOMMENDATION = REFINE / MERGE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.7 Evidence Strength

### Legacy Source-backed Fact

Legacy Causal Engineには \`Evidence Strength\` が研究項目として明示される。

Current 04にも、

\`\`\`text
Evidence Strength
≠ Applicability
\`\`\`

が明示されている。

### Derived Reuse Proposal

> **Evidence Strength = Evidenceが特定Targetに対して割り当てられたEvidence Roleを、どの程度信頼して研究判断へ利用できるかを表すTarget-relative Assessment Context。**

評価Context候補:

\`\`\`text
Data / Source Quality
Reproducibility
Channel Context
Target Relevance
Independence / Dependency
Contradiction Context
Temporal / Version Validity
Sample / Unique Market Event Coverage
Research Process Integrity
Uncertainty
\`\`\`

重要:

\`\`\`text
Strength
≠ Evidence Count
≠ Channel
≠ Outcome
≠ Independence
≠ Applicability
\`\`\`

現段階ではUniversal Score化しない。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
NONE / MINOR

LEGACY_REVIEW_STATUS:
ADOPTABLE

LEGACY_REUSE_RECOMMENDATION:
MERGE / REFINE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.8 Evidence Profile

### Legacy Source-backed Fact

LegacyはEvidence Package / Evidence Source Separationを持ち、Historical / OOS / Demo / Live等を一つの数字へ潰さない。

Current 04にはすでに \`Evidence Profile\` が存在する。

### Derived Reuse Proposal

> **Evidence Profile = 一つのResearch Target / Hypothesisに対する複数Evidenceを、Channel・Role・Outcome・Strength・Source・Time・Version・Quality・Uncertainty・Shared / Dependency Contextを失わず整理し、支持・矛盾・不足・依存関係を確認可能にするEvidence構造。**

### Important Correction — Ownership

推奨Ownership候補:

\`\`\`text
03_RESEARCH
↓
Evidence Profileを生成 / 構成
↓
Research Resultへ保持
↓
Validated Research Result
↓
04_KNOWLEDGE_APPLICABILITY
Evidence Profileを参照
\`\`\`

04が同じEvidence Profileを再生成しない。

これはCurrentへの採用決定ではなくOwnership Refinement Proposal。

Evidence Profileは、

\`\`\`text
Evidence Score
Hypothesis Verdict
Knowledge Promotion
Applicability
Trade Permission
\`\`\`

を所有しない。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
MERGE / OWNERSHIP REFINE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.9 Hypothesis Assessment

### Source Relation

LegacyにはHypothesis Score / Reliability / Lifecycle / SUPPORTED / WEAK / RETIRED等が存在するが、今回の多軸 \`Hypothesis Assessment\` と同一ではない。

Current 03にも独立Objectとしては存在しない。

したがって、これはDerived Reuse Proposal。

### Derived Definition

> **Hypothesis Assessment = 特定VersionのHypothesisに紐付くEvidence Profileを、Role・Outcome・Strength・Channel・Quality・Shared Evidence・Dependency・Contradiction・Alternative Hypothesis・Condition・Failure Boundary・Evidence Gap・Uncertainty・Research Process Integrityを保持したまま解釈し、「このHypothesisについて研究上どこまで言えるか」を整理するResearch評価。**

多軸候補:

\`\`\`text
Conclusion
Scope
Contradiction
Alternative Status
Boundary Status
Evidence Coverage
Dependency Context
Uncertainty
Process Integrity
\`\`\`

禁止:

\`\`\`text
Evidence数 → Hypothesis Result
平均Strength → Hypothesis Result
Supporting多数決 → SUPPORTED
AI判断 → SUPPORTED
\`\`\`

Hypothesis AssessmentはLifecycle変更Authorityを持たない。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
REDESIGN_REQUIRED

LEGACY_REUSE_RECOMMENDATION:
DERIVED PROPOSAL

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.10 Research Result

### Legacy Source-backed Fact

LegacyにはResearch ResultがKnowledge Object / Research Outputとして存在する。

Current 03でも正式なResearch出口候補として明示されている。

### Derived Refinement

> **Research Result = 特定Research Question / Research Planについて得られたEvidence ProfileとHypothesis Assessmentを中心に、Alternative Hypothesis・Contradiction・Condition・Failure Boundary・Constraint Candidate・Reproducibility・Regime Dependency・Uncertainty・Unknown・Research Process状態・Trace / Versionを統合し、そのResearchによって何が分かり、何が分からず、どの条件で成立し、どこで壊れたかを追跡可能に表現するResearch成果。**

重要:

\`\`\`text
Research Result
≠ Hypothesis Assessment
≠ Knowledge
≠ Applicability
≠ Production Approval
\`\`\`

成功だけでなく、

\`\`\`text
REFUTED
INCONCLUSIVE
REGIME DEPENDENT
FAILURE BOUNDARY FOUND
INSUFFICIENT EVIDENCE
UNKNOWN
\`\`\`

もResearch Assetになり得る。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
NONE / MINOR

LEGACY_REVIEW_STATUS:
ADOPTABLE

LEGACY_REUSE_RECOMMENDATION:
MERGE / REFINE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.11 Validation Gate

### Source Relation

LegacyにはValidation / Evidence Package / Approval等の関連思想があるが、Current \`Validation Gate\` と同一Definitionではない。

Current 03にValidation Gateが明示済み。

### Derived Refinement

> **Validation Gate = Research Resultが次のKnowledge領域で再評価・再利用可能な最低限のResearch Integrity / Trace / Version / Evidence Contextを保持しているかを確認する03_RESEARCHの品質境界。**

確認候補:

\`\`\`text
Research Question / Target / Version
Evidence Source / Channel / Role
Contradiction / Alternative
Failure Boundary / Constraint
Uncertainty / Unknown
Research Process FailureとHypothesis Refutationの分離
Trace / Provenance
\`\`\`

### Important Correction — 新Conceptを無条件必須化しない

Evidence Strength / Shared Evidence / Evidence Dependency等は、

> **Research Type上必要な場合に追跡可能であること**

をGate確認候補とする。

全Researchへ空Object生成を強制しない。

\`\`\`text
Required when applicable
≠ Required for every Research
\`\`\`

Validation Gateは、

\`\`\`text
Hypothesis Truth Gate
Knowledge Approval Gate
Production Approval Gate
\`\`\`

ではない。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
CURRENT REFINEMENT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.12 Validated Research Result

### Current Source-backed Fact

Current 03では、

> **Validated = Hypothesisが正しい、ではなく、Research Resultが定義された研究・検証・Trace要件を満たし次のKnowledge領域で評価可能な形になっていること**

と定義されている。

### Derived Refinement

> **Validated Research Result = Validation Gateで必要なResearch Integrity・Evidence Traceability・Version Integrity・Contradiction / Uncertainty保持・Process Integrity等を満たし、SUPPORTED / REFUTED / INCONCLUSIVE等の結論種別に関係なく04が再評価可能になった正式Research Output。**

重要:

\`\`\`text
Validated
≠ Proven
≠ Supported
≠ Knowledge
≠ Applicable
≠ Production Approved
\`\`\`

例:

\`\`\`text
Research Conclusion = REFUTED
Validation Status = VALIDATED

Research Conclusion = INCONCLUSIVE
Validation Status = VALIDATED
\`\`\`

も成立し得る。

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
CURRENT REFINEMENT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.13 Knowledge Admission / Knowledge Promotion

### Legacy / Current Source Relation

LegacyにはEvidence Package → Knowledge Candidate → Approval等の近い思想が存在する。

Current 04には、

\`\`\`text
Validated Research Result
↓
Knowledge Admission / Promotion
↓
Knowledge Record / Knowledge Pool
\`\`\`

が存在するが、AdmissionとPromotionはまだ一体Concept。

今回の二段分離はDerived Proposal。

### Knowledge Admission — Derived Definition

> **Knowledge Admission = Validated Research Resultを将来再利用可能なKnowledgeとして管理する価値があるか、また既存KnowledgeとのRelation上どの扱いが適切かを判断する04 Knowledge Maintenance Pathの入口審査。**

扱い候補:

\`\`\`text
NEW
MERGE
UPDATE_CANDIDATE
LINK
DEFER
REJECT_AS_KNOWLEDGE
\`\`\`

具体Enumは未確定。

Important:

\`\`\`text
Validated
≠ Admission必須

Not Admitted as Knowledge
≠ Research Result Deleted
\`\`\`

### Knowledge Promotion — Derived Definition

> **Knowledge Promotion = AdmissionでKnowledge化価値があると判断されたValidated Research Resultについて、Claim・Condition・Failure Boundary・Constraint・Evidence Profile・Contradiction・Uncertainty・Version・Trace・既存Knowledge Relationを整理し、新規Knowledge Recordまたは既存Knowledge Version / Relationship UpdateとしてKnowledge Poolへ正式反映するMaintenance処理。**

### Important Correction — Naming Collision

Legacyには別責任としてProduction Promotion Ladderが存在する。

したがって必ず、

\`\`\`text
Knowledge Promotion
≠ Production Promotion
\`\`\`

を明記する。

将来のRename候補:

\`\`\`text
Knowledge Registration
Knowledge Materialization
Knowledge Commit
\`\`\`

ただし現時点ではRenameを確定しない。

### Does Not Own

\`\`\`text
Current Applicability
Production Approval
Trade Thesis
Signal
Risk Permission
Execution
\`\`\`

### Review

\`\`\`text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
SPLIT / REFINE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
\`\`\`

---

## 7.14 Knowledge Record / Knowledge Pool

### Source Relation

LegacyにはKnowledge Domain / Knowledge Object / Knowledge Spine思想があり、Current 04にはKnowledge Pool・Knowledge Version・Knowledge Status・条件付きKnowledgeの責任が存在する。

今回のKnowledge Record正式化は、Legacy原文の単純復活ではなくCurrent責任を細分化したDerived Refinement。

### Knowledge Record — Formal Definition Candidate

> **Knowledge Record = Validated Research ResultがKnowledge Admission / Knowledge Promotionを経て、ClaimだけでなくScope・成立条件・Failure Boundary・Constraint Context・Evidence Context・Contradiction・Uncertainty・Version・Validation History・Trace / Provenance・他KnowledgeとのRelationshipを保持し、将来のResearchおよびApplicabilityから再利用可能な形へ整理された正式Knowledge単位候補。**

重要:

~~~text
Research Result
≠ Knowledge Record

Hypothesis
≠ Knowledge Record

Knowledge Record
≠ Current Applicability

Knowledge Record
≠ Trade Permission
~~~

Knowledge Recordは概念上、以下を保持可能にする。

~~~text
Knowledge Identity
Knowledge Type
Claim / Finding
Scope
Condition
Failure Boundary
Constraint Context
Evidence Profile Reference
Contradiction
Uncertainty
Target Asset / Market
Time Horizon
Regime / Market Context
Version
Validation History
Source Research Result
Trace / Provenance
Knowledge Relationships
~~~

具体Field / Schemaは未確定。

### 1:N / N:1を許容

~~~text
1 Research Result
→ 複数Knowledge候補

複数Research Result
→ 1 Knowledge Recordを支持 / 更新
~~~

Research ResultとKnowledge Recordを1:1固定しない。

### Knowledge Version Correction

~~~text
Knowledge Content Version
≠ Validation / Evidence History
~~~

Claim・Scope・Condition・Boundary等の意味変更はKnowledge Version候補。
単なるEvidence追加だけで毎回Knowledge Versionを増やすとは限らない。

旧Versionを無言で上書きしない。

### Constraint Authority Correction

Research側のConstraint CandidateをKnowledge Recordへ移しただけでProduction Hard Constraintへ自動昇格させない。

概念上:

~~~text
Research Constraint Candidate
↓
Knowledge Constraint / Constraint Context
↓
別Authority / Governance
↓
Runtime Authorized Constraint
~~~

の身分差を保持可能にする。

具体State / Authorityは未確定。

### Failure Boundary Authority Correction

Failure Boundaryも、存在するだけで無条件Hard Gateとしない。

Applicabilityでは最低限、

~~~text
Failure Boundary Status
Boundary Evidence Context
Boundary Uncertainty
~~~

を参照可能にする。

強く確立したBoundaryと限定EvidenceしかないBoundaryを同一扱いしない。

### Knowledge Pool — Formal Definition Candidate

> **Knowledge Pool = Knowledge Admission / Promotionを経て正式化されたPositive・Negative・Failure・Constraint・Uncertainty等のKnowledge Recordと、それらのVersion・Relationship・Research / Evidence Traceを、ResearchおよびRuntime Applicabilityから再利用可能な形で参照する04内の論理Knowledge領域。**

重要:

~~~text
Knowledge Pool
≠ Database Table

Knowledge Pool
≠ Trade Rule一覧

Knowledge Pool
≠ Approved Hypothesis一覧

Knowledge Pool
≠ Applicable Knowledge Set
~~~

役割:

~~~text
何が分かったか
どこで成立するか
どこで失敗するか
何が否定されたか
何が制限条件か
何が不明か
~~~

RuntimeからKnowledge Poolを直接書き換えない。

~~~text
Runtime Finding
↓
Research Candidate
↓
03_RESEARCH
↓
Validated Research Result
↓
Knowledge Maintenance
~~~

を基本方向とする。

### Review

~~~text
Knowledge Record:
LEGACY_CONFLICT_STATUS = MINOR
LEGACY_REVIEW_STATUS = PARTIAL_REUSE
LEGACY_REUSE_RECOMMENDATION = REFINE / DEFINE

Knowledge Pool:
LEGACY_CONFLICT_STATUS = NONE / MINOR
LEGACY_REVIEW_STATUS = ADOPTABLE
LEGACY_REUSE_RECOMMENDATION = CURRENT DESIGNを優先

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.15 Applicability Evaluation

### Current Relation

Current 04には既にApplicability Evaluation / State / Failure Boundary Check / Constraint Check / Evidence StrengthとApplicabilityの分離 / Validation Age / Knowledge Conflict・Overlapが存在する。

今回のDefinitionはCurrent Working Baselineの精密化Proposal。

### Formal Definition Candidate

> **Applicability Evaluation = Knowledge Poolから参照したKnowledge RecordのScope・成立条件・Failure Boundary・Constraint Context・Evidence Context・Validation Age・Version・Uncertainty等を、特定時点のCurrent Market Understanding・Market DNA Snapshot・Quality / Freshness・Runtime Contextと照合し、Knowledgeの真偽やTrade方向を変更することなく、現在市場の意思決定材料として利用対象にできるかを評価するRuntime処理。**

中心的な問い:

> **「このKnowledgeは、今この市場条件で利用対象にしてよいか？」**

Does Not Own:

~~~text
Research
Knowledge Validation
Knowledge Lifecycle Update
Expected Value
Trade Thesis
BUY / SELL
Risk Permission
Execution
~~~

### Conceptual Evaluation

~~~text
Candidate Retrieval
↓
Knowledge Eligibility
↓
Scope / Target Match
↓
Condition Match
↓
Failure Boundary Check
↓
Constraint Check
↓
Evidence Context
↓
Validation Age / Version
↓
Current Quality / Freshness
↓
Contradiction
↓
Uncertainty
↓
Relationship / Overlap
↓
Applicability Assessment
~~~

これは責任整理の概念順であり、Python実装順を固定しない。

### Condition Context

~~~text
MATCHED
MISSING
MISMATCHED
UNKNOWN
~~~

の違いを表現可能にする。

重要:

~~~text
MISSING
≠ MISMATCHED
~~~

UNKNOWNを自動MATCH扱いしない。

### Applicability State Correction — MUST

従来候補のApplicability Stateは意味の異なるStateを混在させるため、Derived Proposalでは三軸へ分離する。

#### Applicability State

~~~text
APPLICABLE
PARTIALLY_APPLICABLE
NOT_APPLICABLE
UNCERTAIN
~~~

#### Evaluation Status

~~~text
COMPLETED
NOT_EVALUATED
INCOMPLETE
FAILED
~~~

#### Constraint Gate Status

~~~text
CLEAR
LIMITED
BLOCKED
UNKNOWN
~~~

正式Enumは未確定。

例:

~~~text
Applicability State = APPLICABLE
Evaluation Status = COMPLETED
Constraint Gate Status = BLOCKED
~~~

は成立し得る。

これにより「KnowledgeはCurrent Marketに適合していたが、Runtime利用は禁止された」という情報を失わない。

### PARTIALLY_APPLICABLE Correction — SHOULD

PARTIALLY_APPLICABLEは主にScope / Conditionが部分一致している状態へ意味を寄せる。

~~~text
Condition完全一致
BUT
Evidence古い / Uncertainty高い
~~~

だけを理由にPARTIALへ潰さない。

その場合は、

~~~text
Applicability State = APPLICABLE
+
Uncertainty / Validation Age Context
~~~

または必要に応じてUNCERTAINとする方向を残す。

### Current Context ≠ New Knowledge

Runtime ObservationはApplicability Contextとして使えるが、新Knowledgeへ即昇格させない。
新しい矛盾・未知はResearch Candidateへ戻す。

### Review

~~~text
LEGACY_CONFLICT_STATUS:
NONE / MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
CURRENT REFINEMENT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.16 Applicability Assessment

### Formal Definition Candidate

> **Applicability Assessment = 特定VersionのKnowledge Recordを、特定Evaluation Contextに対してApplicability Evaluationした結果を、Applicability StateだけでなくEvaluation Status・Constraint Gate Status・Matched / Missing / Mismatched / Unknown Conditions・Failure Boundary・Evidence Context・Validation Age・Current Data Quality / Freshness・Contradiction・Uncertainty・Relationship / Overlap・Evaluation Reason / Limitationとともに保持する、説明可能なRuntime評価結果Object候補。**

重要:

~~~text
Applicability Evaluation
= 評価処理

Applicability Assessment
= 評価結果Object

Knowledge Record
≠ Applicability Assessment
~~~

AssessmentはKnowledgeの永久属性ではなくRuntime Snapshot。

~~~text
09:00 K-101 = APPLICABLE
12:00 K-101 = NOT_APPLICABLE
18:00 K-101 = UNCERTAIN
~~~

は正常。

### Target / Context Binding

必ず概念上、

~~~text
Knowledge ID
Knowledge Version
Evaluation Context
Evaluation Time
Applicability Logic / Assessment Version
~~~

へ紐付け可能にする。

Evaluation Context候補:

~~~text
Market / Asset
Current Market Understanding Ref
Market DNA Snapshot Ref
Quality Context
Freshness Context
Runtime Event / Session Context
~~~

### Assessment Context

~~~text
Applicability State
Evaluation Status
Constraint Gate Status
Matched Conditions
Missing Conditions
Mismatched Conditions
Unknown Conditions
Failure Boundary Status
Boundary Evidence / Uncertainty
Evidence Context
Validation Age Context
Current Quality / Freshness
Known Research Contradiction
Current Applicability Contradiction
Uncertainty
Relationship / Shared Evidence / Dependency / Overlap Context
Evaluation Reasons
Evaluation Limitations
~~~

具体Schemaは未確定。

### Excluded Assessmentも保持

~~~text
NOT_APPLICABLE
UNCERTAIN
Constraint Gate BLOCKED
Evaluation INCOMPLETE / FAILED
~~~

もTrace対象とする。

Runtimeで見つかった新しい矛盾はResearch Candidateへ返し、AssessmentがKnowledge Lifecycleを直接更新しない。

### Review

~~~text
LEGACY_CONFLICT_STATUS:
NONE / MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
CURRENT REFINEMENT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.17 Applicable Knowledge Set

### Formal Definition Candidate

> **Applicable Knowledge Set = 特定Evaluation Contextに対して評価されたKnowledge Record群から、05_DECISIONが現在の意思決定材料として利用可能なものをApplicability Assessment付きで選別し、各KnowledgeのCondition・Failure Boundary・Constraint・Evidence・Uncertaintyを保持するとともに、Knowledge間のConflict・Shared Evidence・Dependency・Overlap等のRelationship Contextを解決せず引き継ぐ、04の正式Downstream Boundary Object候補。**

重要:

~~~text
Applicable Knowledge Set
≠ Knowledge Pool
≠ Knowledge ID一覧
≠ Trade Thesis
≠ BUY / SELL
≠ Trade Permission
~~~

### Member Selection Direction

概念上:

~~~text
APPLICABLE
→ Active Member候補

PARTIALLY_APPLICABLE
→ Conditional / Partial Member候補

NOT_APPLICABLE
→ Evaluated Exclusion Trace

UNCERTAIN
→ Active Setから通常除外 + Uncertainty Trace

Constraint Gate = BLOCKED
→ Active Setから除外 + Block Trace

Evaluation Status ≠ COMPLETED
→ Active Setから除外 + Process Trace
~~~

正式Selection Ruleは未確定。

PARTIALをSetへ含める場合もPARTIALLY_APPLICABLEの身分を保持し、APPLICABLEへ昇格させない。
単純な0.5票として扱わない。

### Conflict / Shared Evidence

04では、

~~~text
Conflict Exists
Shared Evidence Exists
Dependency Exists
Overlap Exists
~~~

まで認識する。

~~~text
Conflict Winner
Knowledge Weight
Direction
~~~

は05の責任。

したがって、

~~~text
3 Knowledge
≠ 3 Independent Reasons
~~~

を05が理解できるRelationship Contextを保持する。

### Empty Set

~~~text
Applicable Knowledge Set = EMPTY
~~~

を正常状態として許容する。

重要:

~~~text
EMPTY
≠ Evaluation Failure
EMPTY
≠ NO_TRADE Decision
~~~

### Review

~~~text
LEGACY_CONFLICT_STATUS:
NONE / MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
CURRENT REFINEMENT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.18 Runtime Applicability Review Corrections

Knowledge Record → Applicable Knowledge Set全体Reviewで、保存前に以下6点をCorrectionとして反映する。

### CORRECTION-01 — Applicability / Process / Constraint State Separation

~~~text
Applicability State
Evaluation Status
Constraint Gate Status
~~~

を分離する。

理由:

> 「市場に適合するか」「評価処理が完了したか」「利用禁止Gateに掛かったか」は別問題。

### CORRECTION-02 — Constraint Candidate ≠ Runtime Hard Constraint

~~~text
Research Constraint Candidate
≠ Knowledge Constraint / Constraint Context
≠ Runtime Authorized Hard Constraint
~~~

Authority昇格を暗黙化しない。

### CORRECTION-03 — Evaluation Context Binding

同一Applicable Knowledge Set内のAssessmentは原則、同一または互換性を確認できるEvaluation Contextへ紐付ける。

Evaluation Context候補:

~~~text
Evaluation Cycle / Time Window
Current Market Understanding Ref
Market DNA Snapshot Ref
Quality Context
Freshness Context
~~~

暴落前Assessmentと暴落後Assessmentを無条件に同一Setへ混ぜない。

### CORRECTION-04 — Candidate Retrieval TraceとEvaluated Exclusion Traceを分離

~~~text
Knowledge Pool
↓
Candidate Retrieval
├ Retrieved
└ Not Retrieved
       ↓
Retrieved Candidate
↓
Applicability Evaluation
├ Included
└ Evaluated but Excluded
~~~

重要:

~~~text
Not Retrieved
≠ NOT_APPLICABLE
~~~

### CORRECTION-05 — PARTIALLY_APPLICABLE Meaning

PARTIALは主にScope / Conditionの部分一致を示す。

Evidence Age / Evidence Weakness / UncertaintyだけをPARTIALへ押し込まない。

### CORRECTION-06 — Failure Boundary Authority / Uncertainty

Failure Boundaryが存在するだけで無条件Hard Gateとしない。

最低限、

~~~text
Boundary Status
Boundary Evidence Context
Boundary Uncertainty
~~~

を保持可能にし、Boundaryの確立度を失わない。

---

## 7.19 Runtime Applicability Trace Separation

### Candidate Retrieval Trace

> **どのKnowledgeが今回Applicability Evaluation候補として取得された / されなかったか、その検索Contextと理由を追跡するTrace候補。**

用途:

~~~text
なぜK-999は今回評価対象に入らなかったか？
~~~

を説明する。

### Evaluated Exclusion Trace

> **Applicability EvaluationされたKnowledgeが、なぜApplicable Knowledge Setへ入らなかったかを追跡するTrace候補。**

例:

~~~text
NOT_APPLICABLE
UNCERTAIN
Constraint Gate BLOCKED
Evaluation INCOMPLETE
Evaluation FAILED
PARTIAL but not selected
~~~

重要:

~~~text
Candidate Retrieval Trace
≠ Evaluated Exclusion Trace
~~~

---

## 7.20 Runtime Applicability — Final Boundary

今回のRefinement後の概念Flow:

~~~text
Knowledge Pool
↓
Candidate Retrieval
↓
Candidate Retrieval Trace
↓
Knowledge Candidates
        +
Evaluation Context
        ↓
Applicability Evaluation
        ↓
Applicability Assessment
├ Applicability State
├ Evaluation Status
├ Constraint Gate Status
├ Condition Match
├ Failure Boundary Context
├ Evidence Context
├ Validation Age
├ Quality / Freshness
├ Contradiction
├ Uncertainty
└ Relationship Context
        ↓
Set Construction
├ Applicable Members
├ Conditional / Partial Members
└ Evaluated Exclusion Trace
        ↓
Applicable Knowledge Set
+
Conflict / Shared Evidence /
Dependency / Overlap Context
        ↓
05_DECISION
~~~

Responsibility Boundary:

~~~text
04
= Knowledgeの現在利用資格を評価・選別し、
  理由とRelationshipを保持して05へ渡す

05
= Applicable Knowledgeを統合し、
  Conflictを扱い、
  Decision / Trade Thesisを作る
~~~

絶対境界:

~~~text
Knowledge Record
≠ Applicability Assessment

Knowledge Pool
≠ Applicable Knowledge Set

Applicable Knowledge
≠ Positive Expected Value

Conflict Detection
≠ Conflict Resolution

Applicable Knowledge Set
≠ Trade Permission
~~~

このRuntime Flow全体は、Current 04 Working Baseline + Legacy Referenceを比較して作ったDerived Reuse / Current Refinement Proposalであり、Current Design採用済みではない。

~~~text
CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---


## 7.21 Legacy 05_DECISION Equivalent — Reference Extraction

### Source-backed Legacy Flow

Legacy Production / Trading Domainでは概ね以下の責任が存在した。

~~~text
Approved Hypothesis / Edge Pool
+ Current Market Context
+ Market DNA
↓
Applicable Hypothesis Set
↓
Trade Thesis
↓
External AI Review (optional)
↓
Signal Engine
↓
Pre-Trade Defense
↓
Execution Logic
↓
EntryThesis
↓
OrderIntent
~~~

Current 04ではすでにKnowledgeのApplicability Selectionを担当するため、Legacy Production全体を05へそのまま移植しない。

### Responsibility Redistribution

~~~text
Legacy ApplicableHypothesisSet
→ Current 04 Applicable Knowledge Setへ吸収 / 再設計

Legacy Production Thesis Builder Selection
→ Current 04

Legacy Production Thesis Builder Composition
→ Current 05

Legacy TradeThesis
→ Current 05候補

Legacy Signal Engine / SignalDecision
→ Current 05 Decision Evaluation / Decision Result候補

Legacy Pre-Trade Defense
→ 05外のDefense / Risk

Legacy EntryThesis / OrderIntent
→ Execution
~~~

中心境界:

~~~text
04
= Selection / Applicability

05
= Integration / Thesis / Decision

Defense
= Current Safety / Risk Permission

Execution
= Order / Entry / Fill
~~~

### Legacy Review

~~~text
LEGACY_CONFLICT_STATUS:
MINOR / RESPONSIBILITY REDISTRIBUTION REQUIRED

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

LEGACY_REUSE_RECOMMENDATION:
SPLIT / REFINE / MERGE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.22 05_DECISION — Core Responsibility Boundary

### Formal Definition Candidate

> **05_DECISION = 04_KNOWLEDGE_APPLICABILITYから受け取ったApplicable Knowledge Setを、Conflict・Shared Evidence・Dependency・Overlap・Contradiction・Uncertaintyを失わず意思決定目的で統合し、現在市場についてのTrade Thesisを構成し、そのThesisにRiskを取りたいだけの合理性・期待価値があるかを評価してDecision Resultを生成する意思決定領域候補。**

### Formal Input Candidate

~~~text
Applicable Knowledge Set
Applicability Assessments
Evaluation Context
Conflict Context
Shared Evidence
Dependency / Overlap
Failure Boundary Context
Constraint Context
Evidence Context
Quality / Freshness
Uncertainty
~~~

### Formal Output Candidate

~~~text
Trade Thesis 0..N
Decision Evaluation Status
Decision Result
Decision Trace
Diagnostics
Research Feedback Candidate
~~~

### Does Not Own

~~~text
Research
Knowledge Promotion
Applicability Re-evaluation
Knowledge Lifecycle Update
Constraint Authority Update
Production Promotion
Risk State Update
Defense
EntryThesis
OrderIntent
Execution
~~~

### Absolute Boundaries

~~~text
Applicable Knowledge
≠ Trade Thesis

Trade Thesis
≠ Decision Result

Decision Result
≠ Defense Decision

Decision Result
≠ Execution Permission
~~~

### Review

~~~text
LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

REUSE_RECOMMENDATION:
SPLIT / REFINE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.23 Decision Context Assembly

### Formal Definition Candidate

> **Decision Context Assembly = 04から渡されたApplicable Knowledge Setと、そのEvaluation Context・Applicability Assessment・Relationship・Constraint・Failure Boundary・Evidence・Quality / Freshness・Uncertaintyを、身分・Version・時間的一貫性を変更せず検証・束ね、特定Decision Cycleで後続05処理が同一入力状態を再現可能に利用できるDecision Context Snapshotへ固定する05内部の入口責任候補。**

### Core Responsibility

~~~text
Applicable Knowledge Set
+
Evaluation Context
+
Assessment / Relationship Context
↓
Identity / Version / Temporal Compatibility Check
↓
Decision Context Snapshot
~~~

### Important Boundary

Decision Context Assemblyは以下を行わない。

~~~text
Knowledge再検索
Applicability再判定
Knowledge昇格 / 降格
Knowledge Version差替え
Conflict Resolution
Knowledge Weighting
Thesis Role Assignment
Expected Value Evaluation
Direction生成
Trade Thesis生成
BUY / SELL / NO_TRADE
Defense
Execution
~~~

### Evaluation Context vs Decision Context

~~~text
Evaluation Context
= 04がApplicabilityを評価した市場Context

Decision Context
= そのEvaluation結果を今回のDecision Cycleで使用するため固定したInput Context
~~~

05が新しいMarket DNAへ勝手に差し替え、旧Assessmentを再利用しない。

### Decision Context Snapshot Candidate

概念上:

~~~text
Decision Cycle ID / Context ID
Evaluation Context Ref
Applicable Knowledge Set Ref
Knowledge IDs / Versions
Assessment Refs / Versions
Relationship Context
Constraint / Boundary Context
Quality / Freshness
Uncertainty
Assembly Logic Version
Assembled At
Trace
~~~

正式Persistent Object化は未確定。

### Assembly Process Status

候補:

~~~text
READY
INCOMPLETE
INCONSISTENT
FAILED
~~~

正式Enumは未確定。

重要:

~~~text
Assembly FAILED
≠ NO_TRADE

Applicable Knowledge Set EMPTY
≠ Assembly Failure
~~~

### Trace

~~~text
Decision Context
→ Applicable Knowledge Set
→ Applicability Assessment
→ Knowledge Record

Decision Context
→ Evaluation Context
→ Current Market Understanding / Market DNA
~~~

### Review

~~~text
LEGACY_SOURCE_RELATION:
Production Thesis Builder Input Assembly

LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

REUSE_RECOMMENDATION:
SPLIT / REFINE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.24 Knowledge Integration

### Formal Definition Candidate

> **Knowledge Integration = Decision Context Snapshotに固定されたApplicable Knowledge群の意味・方向・条件・独立性・Shared Evidence・Dependency・Overlap・Common Cause・Conflict・Failure Boundary・Constraint・Uncertaintyを、元Knowledgeを変更せず意思決定用に構造化し、重複根拠の二重計上やKnowledge多数決を防ぎながらTrade Thesis Constructionへ渡せるIntegrated Knowledge Contextを生成する05内部責任候補。**

### Core Flow

~~~text
Decision Context Snapshot
↓
Semantic / Horizon Alignment
↓
Effect / Direction Context
↓
Shared Evidence / Independence
↓
Dependency / Common Cause
↓
Overlap / Redundancy
↓
Conflict Structure
↓
Condition / Failure Boundary / Constraint
↓
Uncertainty Structure
↓
Integrated Knowledge Context
~~~

### Critical Correction — Thesis Roleをまだ確定しない

Knowledge Integrationでは、

~~~text
PRIMARY
SUPPORTING
CONDITIONAL
CONTRADICTING
~~~

をCanonical Roleとして確定しない。

理由:

> Thesis RoleはTrade Thesisに対するTarget-relative Roleであり、Trade Thesisが未構築の段階では確定できない。

IntegrationではThesis非依存の、

~~~text
Effect Group
Mechanism Group
Shared Evidence Group
Dependency Group
Conflict Group
Conditional Context
Uncertainty Context
~~~

等へ整理する。

### Independence Rule

~~~text
3 Knowledge
≠ 3 Independent Reasons
~~~

Shared Evidence / Same Market Event / Dependency / Common Cause / Redundancyを独立票として数えない。

### Conflict

~~~text
Conflict Detection
→ 04

Conflict Structure / Meaning
→ Knowledge Integration

Conflict Resolution / Thesis handling
→ 後続05
~~~

Integration段階でWinnerを決定しない。

### Runtime Integration ≠ Knowledge Merge

~~~text
05 Runtime Integration
≠ Knowledge Record Merge
~~~

Duplicate / Overlapを発見してもKnowledge Poolを直接修正しない。
必要ならKnowledge Maintenance / Research CandidateへFeedbackする。

### Integrated Knowledge Context Candidate

~~~text
Knowledge Members
Semantic / Effect Relations
Evidence Independence Structure
Shared Evidence
Dependency
Common Cause
Overlap / Redundancy
Conflict Structure
Condition Structure
Failure Boundary Context
Constraint Context
Uncertainty Context
Trace
Integration Logic Version
~~~

正式Object化は未確定。

### Process Status Candidate

~~~text
INTEGRATED
PARTIALLY_INTEGRATED
UNRESOLVED
FAILED
~~~

重要:

~~~text
UNRESOLVED
≠ NO_TRADE

FAILED
≠ NO_TRADE
~~~

### Does Not Own

~~~text
Applicability Re-evaluation
Knowledge Promotion / Merge / Delete
Lifecycle Update
Constraint Override
Final Thesis Role
Expected Value Assessment
Final Direction
BUY / SELL / NO_TRADE
Defense
Execution
~~~

### Review

~~~text
LEGACY_SOURCE_RELATION:
FIX-008 Dependency / Redundancy Checker
+ Contradiction Integrator

LEGACY_CONFLICT_STATUS:
MINOR

MAIN REDESIGN:
Hypothesis → Knowledge
Selection → 04
Final Thesis Role → Trade Thesis Construction

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.25 Trade Thesis Construction / Trade Thesis

### Trade Thesis Construction — Formal Definition Candidate

> **Trade Thesis Construction = Integrated Knowledge Contextに整理されたApplicable Knowledge群から、Shared Evidence・Dependency・Conflict・Condition・Failure Boundary・Constraint・Uncertaintyを失わず、KnowledgeへThesis-relativeなPRIMARY / SUPPORTING / CONDITIONAL / CONTRADICTING Roleを割り当て、Expected Direction・Effect・Horizon・成立条件・反証・Invalidationを持つ0個以上の一貫したTrade Thesisを構成する05内部責任候補。**

### Trade Thesis — Formal Definition Candidate

> **Trade Thesis = 特定Decision ContextにおいてApplicable Knowledge群を一つの市場論拠として構成し、何を・なぜ・どのHorizonで期待するか、どのKnowledgeが中心・支持・条件・反証を担うか、何が論拠を弱化・無効化するか、どの不確実性を抱えるかをVersion / Trace付きで固定したImmutable Decision-Reasoning Snapshot候補であり、BUY / SELL / NO_TRADEやExecution Permissionそのものではない。**

### 0..N Thesis

Current Refinementでは、

~~~text
Integrated Knowledge Context
→ Trade Thesis 0..N
~~~

を許容する。

Conflictがある場合にConstructionが無理に一つへ決着させない。

例:

~~~text
T-A = Downside Deleveraging Thesis
T-B = Spot-led Continuation Thesis
~~~

両方が成立可能なら両方を後段へ渡せる。

### Thesis-relative Roles

ここで初めて、

~~~text
PRIMARY
SUPPORTING
CONDITIONAL
CONTRADICTING
~~~

をTrade Thesisに対する相対Roleとして確定する。

~~~text
Thesis Role
≠ Knowledge永久属性
~~~

### Expected Value Ownership Correction

Legacy TradeThesisには expected_value_profile が存在したが、Current Proposalでは責任を分離する。

Trade Thesisが保持する候補:

~~~text
Expected Value Input Context
Research-derived Return / Loss Profile Refs
Cost Estimate Inputs
Probability / Frequency Context
Tail Risk Context
Uncertainty
~~~

Trade Thesis自身は、

~~~text
Final Expected Value Assessment
Trade-worthy Verdict
~~~

を所有しない。

それらはDecision Evaluationの責任。

### Thesis Context Candidate

~~~text
Identity / Version
Decision Context Ref
Integrated Knowledge Context Ref
Expected Direction
Expected Effect
Expected Horizon
Primary Knowledge
Supporting Knowledge
Conditional Knowledge
Contradicting Knowledge
Shared Evidence / Dependency / Redundancy / Common Cause
Required / Weakening Conditions
Failure Boundary Context
Invalidation Conditions
Main Market Risks / Counter-mechanisms
Expected Value Input Context
Quality
Uncertainty
Construction Logic Version
Created At / Validity
Trace
~~~

### Failure Boundary ≠ Invalidation

~~~text
Failure Boundary
= Research上Knownな成立限界

Thesis Invalidation
= 今回のThesisを維持できなくなる条件
~~~

関連するが同一ではない。

### Invalidation ≠ Stop Loss

~~~text
Thesis Invalidation
≠ Execution Stop Loss
~~~

### Construction Status Candidate

~~~text
BUILDABLE
PARTIAL
NOT_BUILDABLE
FAILED
~~~

重要:

~~~text
THESIS_NOT_BUILDABLE
≠ Decision NO_TRADE

NOT_BUILDABLE
≠ FAILED
~~~

### AI

AIは説明・矛盾・Missing Alternative等のAdvisoryに利用可能。
不足KnowledgeをAI一般知識で補ってThesisを捏造しない。
新しいIdeaはResearch Candidateへ送る。

### Does Not Own

~~~text
Applicability変更
Knowledge Lifecycle
Knowledge Merge
Final Expected Value Assessment
BUY / SELL / NO_TRADE
Defense
Risk State
EntryThesis
OrderIntent
Execution
~~~

### Review

~~~text
LEGACY_SOURCE_RELATION:
OBJ-PRD-003 TradeThesis
FIX-008 Thesis Composer

LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
ADOPTABLE / PARTIAL_REUSE

CURRENT REDESIGN:
Hypothesis → Knowledge
Selection → 04
Trade Thesis 1 → 0..N
Final EV Assessment → Decision Evaluation

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.26 Decision Evaluation / Decision Result

### Decision Scope — Important Correction

複数Trade Thesisを比較する前に、比較可能なDecision ScopeへBindingする。

> **Decision Scope = 一つのDecision Resultが責任を持つ比較可能なMarket / Asset / Instrument / Horizon / Evaluation Window等の意思決定対象Context候補。**

原則:

~~~text
同一 / Compatible Decision Scope
→ Cross-Thesis Comparison可能

Incompatible Horizon / Instrument / Context
→ 無理に一つのWinnerを選ばない
→ 別Decision ResultまたはContext扱い
~~~

例:

~~~text
BTC 5m Downside Thesis
≠ BTC 1d Upside Thesisを単純Winner比較
~~~

Decision Cycleは複数Decision Scopeを含み得る。

### Decision Evaluation — Formal Definition Candidate

> **Decision Evaluation = 同一または互換性のあるDecision Scopeに属する有効Trade Thesis群を、Expected Value・損益非対称性・Evidence Independence・Contradiction・Invalidation・Quality・Uncertainty・相互競合の観点から評価・比較し、Knowledge数やThesis数の多数決に頼らず、現在のDecision ContextでRiskを取りたい合理性があるかを判断する05の最終評価処理候補。**

### Decision Result — Formal Definition Candidate

> **Decision Result = 正常に評価されたTrade Thesis群について、どのThesisを根拠にどの方向のRiskを取りたいか、またはRiskを取らないかを、Expected Value Assessment・比較結果・Contradiction・Uncertainty・Reason・Version / Trace付きで固定した05のImmutable Decision Object候補であり、Defense Approval・Execution Permission・Orderそのものではない。**

### Expected Value Assessment — Ownership

Decision Evaluationが正式に所有する候補:

~~~text
Expected Value Assessment
Expected Return / Loss Asymmetry
Probability / Frequency Context
Tail Risk Context
Estimated Cost Context
Expected Value Uncertainty
Trade-worthiness Context
~~~

重要:

~~~text
Expected Value Assessment
≠ Evidence Strength

Expected Value Assessment
≠ Applicability

Expected Value Assessment
≠ Confidence
~~~

具体Formula / Thresholdは未確定。

### Estimated Cost vs Actual Execution Cost

Decision時:

~~~text
Estimated Fee
Estimated Spread
Estimated Slippage
Funding / Financing Estimate
~~~

Execution後:

~~~text
Actual Fill
Actual Fee
Actual Slippage
Actual Latency
~~~

を分離する。

同じLiquidity / Spread情報がDecisionとDefense双方で参照されても、責任は異なる。

~~~text
Decision Evaluation
= EV / Trade-worthinessへの影響

Defense
= 今安全に実行可能か
~~~

### Evaluation Process Status

市場Decisionと処理状態を分ける。

候補:

~~~text
COMPLETED
INCOMPLETE
FAILED
STALE
NOT_EVALUATED
~~~

正式Enumは未確定。

重要:

~~~text
Evaluation FAILED
≠ NO_TRADE

Decision STALE
≠ NO_TRADE
~~~

### Thesis Evaluation / Cross-Thesis Comparison

概念上:

~~~text
Trade Thesis T-A
→ Thesis Evaluation A

Trade Thesis T-B
→ Thesis Evaluation B

Compatible Decision Scope
↓
Cross-Thesis Comparison
↓
Decision Result
~~~

Thesis数による多数決は禁止。

比較Context候補:

~~~text
Expected Value Assessment
Expected Horizon
Mechanism Independence
Evidence Independence
Contradiction
Applicability Quality
Uncertainty
Invalidation Risk
Overlap
Mutual Exclusivity
Context Compatibility
~~~

### Decision Outcome

Legacy候補:

~~~text
BUY
SELL
NO_TRADE
~~~

ただしBUY / SELLはExecution Orderと誤認しやすいため、意味上は、

~~~text
TAKE_LONG_RISK
TAKE_SHORT_RISK
NO_TRADE
~~~

相当として扱う方向をDerived Recommendationとする。

正式Renameは未確定。

### NO_TRADE — Formal Meaning

> **NO_TRADE = 有効Trade Thesisを正常に評価した結果、Expected Value・Conflict・Uncertainty・Invalidation等を考慮して現在Riskを取る合理性が十分でないと判断した正常なDecision Outcome候補。**

重要:

~~~text
THESIS_NOT_BUILDABLE
= 論拠が成立しない

Decision Evaluation FAILED
= 評価処理失敗

NO_TRADE
= 正常評価した結果、Riskを取らない

TAKE_LONG_RISK / TAKE_SHORT_RISK
= Riskを取りたい方向
  ただしExecution Permissionではない
~~~

### Decision Result Candidate

~~~text
Decision Result ID / Version
Decision Context Ref
Decision Scope Ref
Evaluation Status
Evaluated Thesis Refs
Selected Thesis Ref
Non-selected Thesis Refs / Reasons
Decision Outcome
Expected Value Assessment
Contradiction / Alternative Context
Invalidation Context
Uncertainty
Decision Reasons
Limitations
Evaluation Logic Version
Expected Value Logic Version
Created At / Validity
Trace
~~~

### Defense Boundary

~~~text
Decision Evaluation
= Riskを取りたいか

Defense
= 今そのRiskを取って安全か
~~~

したがって、

~~~text
TAKE_LONG_RISK / TAKE_SHORT_RISK
≠ Execution Permission
~~~

### AI Review

AI ReviewはAdvisory。
AI多数決をDecision Authorityにしない。
AI新案はResearch Candidateへ送る。

### Immutable / Trace

結果を見てDecision Resultを書き換えない。

~~~text
Decision Result
→ Trade Thesis
→ Integrated Knowledge Context
→ Decision Context
→ Applicable Knowledge Set
→ Applicability Assessment
→ Knowledge Record
→ Research Result
→ Evidence
~~~

へ戻れる構造を候補とする。

### Does Not Own

~~~text
Research
Knowledge Promotion
Applicability Evaluation
Trade Thesis Construction
Knowledge Lifecycle
Constraint Authority
Production Promotion
Risk State Update
Defense
Position Size
Leverage
Entry / Stop / Take Profit
OrderIntent
Execution
~~~

### Review

~~~text
LEGACY_SOURCE_RELATION:
ROLE-SIG-001 Signal Engine
OBJ-PRD-005 SignalDecision
FIX-008 Signal Boundary

LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
ADOPTABLE / PARTIAL_REUSE

CURRENT REDESIGN:
Single Thesis → 0..N Thesis
Decision Scope Binding added
Expected Value Assessment ownership clarified
Process Status separated from Decision Outcome
BUY / SELL retained only as Legacy-compatible naming candidate

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.27 05_DECISION — Integrated Review / Final Candidate Flow

### Review Result

今回、05内部候補を全体Reviewした結果、Architectureを作り直す必要がある重大矛盾は確認されなかった。

保存前に以下3点をCorrectionとして反映した。

### CORRECTION-05-01 — Decision Scope Binding

~~~text
Incompatible Horizon / Instrument / Context
≠ Direct Cross-Thesis Winner Comparison
~~~

比較可能なDecision Scope単位でDecision Resultを生成する方向へ修正。

### CORRECTION-05-02 — Expected Value Ownership Separation

~~~text
Trade Thesis
= EV Input / Context

Decision Evaluation
= Expected Value Assessment / Trade-worthiness
~~~

へ分離。

### CORRECTION-05-03 — Thesis Role Timing

~~~text
Knowledge Integration
= Thesis-independent Relationship / Effect / Mechanism Structure

Trade Thesis Construction
= PRIMARY / SUPPORTING / CONDITIONAL / CONTRADICTING
  をThesis-relativeに確定
~~~

へ修正。

### Final Candidate Flow

~~~text
04_KNOWLEDGE_APPLICABILITY
↓
Applicable Knowledge Set

────────────────────────────
05_DECISION
────────────────────────────

Decision Context Assembly
↓
Decision Context Snapshot
↓
Knowledge Integration
↓
Integrated Knowledge Context
↓
Trade Thesis Construction
↓
Trade Thesis 0..N
↓
Optional AI Review
↓
Decision Scope Binding
↓
Individual Thesis Evaluation
↓
Expected Value Assessment
↓
Cross-Thesis Comparison
↓
Decision Result

────────────────────────────
05 Boundary
────────────────────────────

↓
Defense / Risk
↓
Execution
~~~

### Absolute Semantic Boundaries

~~~text
Applicable Knowledge
≠ Trade Thesis

Knowledge Integration
≠ Knowledge Merge

Trade Thesis
≠ Expected Value Assessment

Trade Thesis
≠ Decision Result

THESIS_NOT_BUILDABLE
≠ NO_TRADE

Evaluation FAILED
≠ NO_TRADE

Decision Result
≠ Defense Decision

Decision Result
≠ Execution Permission

WIN
≠ Correct Understanding

LOSS
≠ Wrong Understanding
~~~

### Status

この05全体は、

> **Legacy Production / Signal Concept + Current 04 Boundary + Derived Refinementを比較して作ったReference Proposalであり、Current正式設計ではない。**

~~~text
CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---


## 7.28 Defense / Risk — Integrated Boundary

### Formal Domain Candidate

> **Defense / Risk = 05_DECISIONが生成したRisk-taking Decision Resultについて、市場論拠やExpected Valueを再評価せず、Current RiskState・Authorized Runtime Constraint・Liquidity / Exposure / Drawdown / Exchange Health等のSafety Contextから、現在そのRiskをExecutionへ通してよいかをGateするRuntime Safety Domain候補。**

中心境界:

~~~text
05 Decision Evaluation
= Riskを取りたいか

Defense Evaluation
= 今そのRiskをExecutionへ通して安全か

RiskState
= Scope全体として現在どこまでRiskを許すか

Risk Governance
= RiskStateを誰がどう変更できるか

Execution
= 許可Envelopeを具体的なEntry / Orderへ変換
~~~

Absolute Boundaries:

~~~text
Decision Result
≠ DefenseDecision

DefenseDecision
≠ RiskState

RiskState
≠ Production Promotion

BLOCK
≠ Decision Wrong

Fail-Closed
≠ BLOCK

ALLOW
≠ Order Sent

REDUCE
≠ Exact Position Size
~~~

### Legacy Relation

~~~text
Legacy Pre-Trade Defense
→ Current Defense Evaluation

Legacy DefenseDecision
→ Current DefenseDecision

Legacy RiskState
→ Current RiskState

FIX-013 / FIX-015
→ Current Risk Governance / Transition

FIX-009 Defense → Entry boundary
→ Current Defense → Execution Contract
~~~

### Status

~~~text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.29 Defense Evaluation

### Formal Definition Candidate

> **Defense Evaluation = 正常なRisk-taking Decision Resultについて、そのDirection / Trade Thesis / Expected Valueを再評価せず、Current RiskState・Authorized Runtime Constraint・Liquidity / Spread / Slippage Risk・Exposure・Drawdown / Loss Context・Data / Runtime Quality・Exchange / API Health・Abnormal Event・Global Risk Limit等を独立Safety Gateとして評価し、そのDecisionをExecutionへALLOW・制限付きREDUCE・またはBLOCKできるかを判断するRuntime Safety処理候補。**

### Gate Candidate

~~~text
Decision Validity Gate
RiskState Gate
Constraint Gate
Liquidity Gate
Exposure Gate
Drawdown Gate
Data Quality Gate
Exchange / API Health Gate
Abnormal Event Gate
~~~

各Gateを万能総合Scoreへ潰さない。

候補状態:

~~~text
CLEAR
RESTRICT
BLOCK
UNKNOWN
NOT_EVALUATED
~~~

正式Enumは未確定。

### Safety Meaning

~~~text
Liquidity
= 約定 / Exit可能性を含む市場実行安全性

Exposure
= 既存Riskとの合成安全性

Drawdown
= 追加Riskを許容できる資本安全性

Exchange / API Health
= 注文・約定・Positionを安全に管理できるInfrastructure安全性

Constraint
= RuntimeでEnforcement権限を持つAuthorized Constraint
~~~

### Hard Gate Principle

~~~text
Authorized Hard Constraint violation
Critical Exchange Failure
Position State Unknown
NO_NEW_ENTRY
Global hard DD breach
~~~

等を単なる減点として相殺しない。

### Evaluation Status vs Outcome

~~~text
Defense Evaluation Status
≠ Defense Outcome
~~~

候補:

~~~text
COMPLETED
NOT_REQUIRED
INCOMPLETE
FAILED
STALE
NOT_EVALUATED
~~~

正常完了時のみ:

~~~text
ALLOW
REDUCE
BLOCK
~~~

を生成する。

### Fail-Closed

~~~text
Evaluation FAILED / INCOMPLETE / Critical UNKNOWN
↓
DefenseDecisionを捏造しない
↓
Safety PolicyによりExecution DENY
~~~

重要:

~~~text
BLOCK
= 正常Safety判断による禁止

Fail-Closed
= 正常Safety判断を作れなかったためのSafety停止
~~~

### Does Not Own

~~~text
Trade Thesis
Expected Value Assessment
Trade Direction
Knowledge Applicability
RiskState Apply
Constraint Authorization
Exact Position Size
Order Planning
~~~

### Review

~~~text
LEGACY_SOURCE_RELATION:
ROLE-DEF-001 Pre-Trade Defense

LEGACY_REVIEW_STATUS:
ADOPTABLE / PARTIAL_REUSE

CURRENT_REFINEMENT:
Independent Safety Gates
Evaluation Status / Outcome separation
Fail-Closed separation
Authorized Constraint boundary

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.30 DefenseDecision / DefenseEvaluationResult

### DefenseDecision — Formal Definition Candidate

> **DefenseDecision = 正常に完了したDefense Evaluationの結果として、特定Decision Resultを現在Safety Context上Executionへ通常条件で通すか、Risk制限付きで通すか、または通さないかをALLOW / REDUCE / BLOCKとしてReason・Restriction・RiskState / Constraint / Safety Context Reference・Version / Validity / Trace付きで固定したImmutable Runtime Safety Decision Object候補。**

Outcome:

~~~text
ALLOW
REDUCE
BLOCK
~~~

### ALLOW

~~~text
Defense Gate passed
→ Execution Planning Candidate
~~~

ただしOrder送信ではない。

### REDUCE

~~~text
Decision / Directionは維持
+
通常Risk量は禁止
+
Restriction Context内だけExecution可能
~~~

Exact Position SizeはExecution側。

### BLOCK

~~~text
Defense Evaluation completed
+
Current Safety Context上Execution禁止
~~~

Trade Thesisの誤りを意味しない。

### DefenseEvaluationResult — Derived Boundary Candidate

> **DefenseEvaluationResult = Defense Evaluation自体のProcessing Status、正常完了時のDefenseDecision Reference、正常完了できなかった場合のFail-Closed適用、Diagnostics、Validity / Traceを束ね、ExecutionがBLOCKとEvaluation Failureを混同しないためのDefense→Execution境界Context候補。**

概念:

~~~text
DefenseEvaluationResult

evaluation_status
defense_decision_ref
fail_closed_applied
execution_disposition
failure_reason
policy_ref
validity
trace
~~~

### CORRECTION-DR-01 — execution_dispositionは第二のDecisionではない

保存前Reviewで次を明確化する。

~~~text
execution_disposition
= DefenseEvaluationResultから決定論的に導出されるExecution Boundary Projection

execution_disposition
≠ 独立Decision Authority
~~~

候補Mapping:

~~~text
COMPLETED + ALLOW
→ PROCEED

COMPLETED + REDUCE
→ PROCEED_RESTRICTED

COMPLETED + BLOCK
→ DENY

FAILED / INCOMPLETE / STALE + Fail-Closed
→ DENY
~~~

矛盾Combinationを許さない。

### Invariants

~~~text
DefenseDecision exists
⇒ Evaluation COMPLETED

Evaluation failed
⇒ No DefenseDecision

BLOCK
≠ Fail-Closed

REDUCE
≠ Exact Position Size

Missing Defense
≠ ALLOW
~~~

### Status

~~~text
LEGACY_SOURCE_RELATION:
OBJ-PRD-006 DefenseDecision

DefenseEvaluationResult:
DERIVED CURRENT PROPOSAL

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.31 RiskState

### Formal Definition Candidate

> **RiskState = 明示されたRisk Scopeについて、市場理解OSが現在どこまで新規Risk / Exposureを許容するかを表すCross-Cutting Runtime Permission State候補であり、Research Maturity・Knowledge Health・Production Promotion・DefenseDecisionとは独立する。**

Legacy Candidate States:

~~~text
NORMAL
CAUTION
RISK_REDUCED
MICRO_ONLY
NO_NEW_ENTRY
EMERGENCY
~~~

### State Meaning

~~~text
NORMAL
= 通常Risk Envelope

CAUTION
= 警戒。必ずしも縮小ではない

RISK_REDUCED
= 通常より縮小されたRisk Envelope

MICRO_ONLY
= 最小級Riskのみ許可

NO_NEW_ENTRY
= 新規Risk追加禁止。既存Position安全管理は継続

EMERGENCY
= 重大Safety Event。通常Risk-takingよりContainment / Recovery優先
~~~

### Scope Candidate

Source-backed中心:

~~~text
OS
Account
Portfolio
Market Instance
~~~

Derived候補:

~~~text
Venue / Exchange
Asset
~~~

各RiskStateは明示ScopeへBindingする。

### Multiple Scope

~~~text
Global NORMAL
Portfolio RISK_REDUCED
BTC Market Instance NO_NEW_ENTRY
~~~

等を許容可能。

単純平均・万能Severity Scoreへ潰さない。

Defenseは対象DecisionへApplicableなScope群からEffective Risk Permission Contextを評価する。

### CORRECTION-DR-02 — allowed_exposureとDefense Restrictionを分離

~~~text
RiskState.allowed_exposure
= Scope-level Risk Policyが許すBaseline / Ceiling

Defense Restriction Context
= 今回1 Decisionに対するPer-Decision Effective Restriction
~~~

同一ではない。

DefenseはRiskStateのBaselineを参照し、Liquidity / Exposure / DD等を合わせて今回のRestrictionをより厳しくできる。

DefenseがRiskState.allowed_exposure自体を書き換えない。

### Legacy Health Field Refinement

Legacy RiskState内の、

~~~text
money_dd_state
knowledge_health_state
execution_health_state
data_health_state
market_novelty_state
~~~

はCurrentでは第二の正本として複製せず、

~~~text
trigger_refs
basis_refs
risk_context_refs
~~~

としてSource Stateへ参照する方向が安全。

### Absolute Separation

~~~text
RiskState
≠ Production Promotion

RiskState
≠ Knowledge Health

RiskState
≠ Runtime State

RiskState
≠ DefenseDecision

RiskState
≠ Command
~~~

### Status

~~~text
LEGACY_SOURCE_RELATION:
OBJ-PRD-007 RiskState
STATE-RISK-001

LEGACY_REVIEW_STATUS:
ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.32 Risk Governance / RiskState Transition

### Formal Definition Candidate

> **Risk Governance = RiskStateを変更する必要性の発生からCurrent RiskStateへの実適用までをREQUEST / RECOMMEND / APPROVE / APPLYの独立Authority責任として統治し、Safety Restrictionでは明示Policyに基づくEmergency Fast Pathを許容しつつ、Recovery / Permission ExpansionではStrict Approval / Revalidationを要求し、成功State変更だけをImmutable StateTransitionEventとして記録するCross-Cutting Governance責任候補。**

### Canonical Authority Flow

~~~text
Trigger / Finding
↓
REQUEST
↓
RECOMMEND
↓
APPROVE
↓
ApprovalDecision
↓
APPLY Validation
↓
Atomic State Apply
↓
StateTransitionEvent
↓
Current RiskState Projection
~~~

### Authority Meaning

~~~text
REQUEST
= State変更検討を正式要求

RECOMMEND
= どのTransitionが妥当か専門推奨

APPROVE
= Policy / Authority上Applyしてよいか判断

APPLY
= Current State / Approval / Ruleを再検証し実際にWrite
~~~

絶対原則:

~~~text
REQUEST
≠ RECOMMEND
≠ APPROVE
≠ APPLY

APPROVE
≠ APPLIED
~~~

### Single Writer

~~~text
1 RiskState Machine
= 原則1 Apply Authority
~~~

Defense / AI / Logger / Telegram / Post-Trade等がCurrent RiskStateへ無制限に直接Writeしない。

### ApprovalDecision

Legacy FIX-015のSource-backed Objectを再利用候補とする。

Decision:

~~~text
APPROVE
REJECT
HOLD
~~~

Binding候補:

~~~text
Target
Target Version
State Machine
State Machine Version
expected_from_state
requested_to_state
Scope
Validity
Approval Policy
Authority Policy
~~~

### Apply Validation

Apply直前に少なくとも概念上:

~~~text
Required Approval Set
Target / Version
Scope
Expiry
Supersession
Single-use
Current State
expected_previous_state
Transition Legality
Current Constraint / Policy
Authority
~~~

を再検証する。

### Concurrent / Stale Write

~~~text
expected_previous_state
≠ actual current_state
→ Apply reject
~~~

### StateTransitionEvent

成功ApplyだけをImmutable Historical Factとして保存。

候補:

~~~text
target_ref
state_machine_id / version
from_state
to_state
expected_previous_state
transition_sequence
trigger_refs
reason_codes
requested_by_role
recommended_by_role
recommendation_ref
approval_decision_refs
applied_by_role
transitioned_at
effective_at
previous_transition_event_ref
trace_id
~~~

Rejected / Failed AttemptはStateTransitionEventではない。

### Current Projection

~~~text
Current RiskState
= 高速参照Projection

StateTransitionEvent
= Historical Fact
~~~

HistoryからProjectionを再構築可能な方向を維持する。

### Status

~~~text
LEGACY_SOURCE_RELATION:
FIX-013
FIX-015
FIX-016
STATE_DICTIONARY
OBJECT_DICTIONARY

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.33 Emergency Fast Path / Recovery Strict Path

### Emergency Fast Path — Formal Candidate

> **Emergency Fast Path = Critical Safety Trigger時にRisk Restrictionを低LatencyでApplyするため、明示Emergency Authority Policyのもとで通常Governance Pathを高速化する仕組みであり、Governanceを省略する仕組みではない。**

Restrictive例:

~~~text
NORMAL → EMERGENCY
NORMAL → NO_NEW_ENTRY
~~~

中間Stateを飛ばせる。

### CORRECTION-DR-03 — Fast PathのAuthority意味

保存前Reviewで以下を明確化する。

~~~text
Emergency Fast Path
≠ No Approval
≠ No Authority
≠ Direct DB Write
~~~

Fast Pathでは、

~~~text
pre-authorized emergency policy
designated emergency authority
pre-validated restrictive transition class
~~~

等によりLatencyを減らせる候補がある。

ただし必ず、

~~~text
Authority provenance
Policy reference
Scope
Current State check
Transition legality
Apply provenance
StateTransitionEvent
Audit / Trace
~~~

を残す。

具体Emergency IAM / Approval実装は未確定。

### Recovery — Formal Candidate

> **Recovery = Restrictive RiskStateからRisk Permissionを再拡張するTransition系列であり、Restrictive Authorityによる自動復帰を禁止し、Root Cause Resolution・Data / Execution Reconciliation・必要Cooldown・Revalidation・Strict Approvalを検証した後にApplyする。**

候補:

~~~text
EMERGENCY
→ NO_NEW_ENTRY
→ MICRO_ONLY
→ RISK_REDUCED
→ CAUTION
→ NORMAL
~~~

原則段階的。

飛び越しは明示Policy時のみ。

### Safety Asymmetry

~~~text
Restriction
= Fast Path allowed candidate

Recovery / Risk Expansion
= Strict Path
~~~

一回のAPI成功等をRecovery証明にしない。

### Status

~~~text
LEGACY_SOURCE_RELATION:
FIX-013 Safety Asymmetry
FIX-015 Approval Provenance
STATE-RISK-001 Recovery

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.34 Defense → Execution Contract

### Formal Definition Candidate

> **Defense → Execution Contract = 有効Risk-taking Decision ResultについてDefense Evaluation完了後、Execution DomainがRiskをEntry / Orderへ変換してよいかをDefenseEvaluationResult・DefenseDecision・RiskState Reference・Authorized Constraint・Restriction Context・Validity / Version / Traceによって明示するRuntime境界Contract候補。**

### Boundary Flow

~~~text
Decision Result
↓
Defense Evaluation
↓
DefenseEvaluationResult
│
├ COMPLETED + ALLOW
│   → PROCEED
│
├ COMPLETED + REDUCE
│   → PROCEED_RESTRICTED
│
├ COMPLETED + BLOCK
│   → DENY
│
└ FAILED / INCOMPLETE / STALE
    + Fail-Closed
    → DENY

↓
Execution Admission
↓
RiskState / Constraint / Validity Recheck
↓
Entry Snapshot Builder
↓
EntryThesis
↓
OrderIntent
~~~

### Execution Admission Candidate

Executionへ進める条件候補:

~~~text
Valid Risk-taking Decision Result
DefenseEvaluationResult exists
Evaluation COMPLETED
DefenseDecision exists
Outcome ALLOW or REDUCE
Disposition consistent
Decision / Defense not stale
RiskState ref valid
Authorized Constraint refs resolvable
Restriction Context present when REDUCE
~~~

### REDUCE Contract

~~~text
Defense
= Maximum Safety Envelope

Execution
= Envelope内で実際のPosition Size / Leverage / Order Planを構成
~~~

ExecutionはDefense Restrictionを緩和しない。
より厳しくすることは可能。

### BLOCK / Fail-Closed

~~~text
BLOCK
→ No EntryThesis
→ No OrderIntent

Fail-Closed
→ No EntryThesis
→ No OrderIntent
~~~

意味は別なのでTraceを分ける。

### RiskState / Constraint Change

Defense後にRiskStateがよりRestrictiveになった場合:

~~~text
Old ALLOW / REDUCE
→ blindly reuse禁止
→ New Defense / Admission evaluation candidate
~~~

RiskStateが緩和しても旧REDUCE / BLOCKを自動昇格しない。

Constraint変更も同様。

### Entry Snapshot Boundary

Legacy FIX-009の強い原則を維持:

~~~text
Defense passed
↓
Entry Snapshot Builder
↓
EntryThesis
↓
OrderIntent
~~~

EntryThesis生成失敗:

~~~text
ENTRY_SNAPSHOT_NOT_BUILDABLE
→ No OrderIntent
~~~

これはDefense BLOCK / NO_TRADEとは別。

### Generator Boundary

~~~text
DefenseDecision Generator
= Defense Domain

EntryThesis Generator
= Execution / Entry Snapshot Builder

OrderIntent Generator
= Execution / Order Planning

Logger
= Custodian

Post-Trade
= Analyzer
~~~

### Absolute Invariants

~~~text
ALLOW
≠ Order Sent

REDUCE
≠ Exact Position Size

BLOCK
≠ Decision Wrong

Fail-Closed
≠ BLOCK

Missing Defense
≠ ALLOW

Expired Defense
≠ ALLOW

DefenseDecision
≠ EntryThesis

No EntryThesis
→ No OrderIntent

Execution
must not override Defense

Execution
must not rewrite Decision / Thesis / Defense
~~~

### Status

~~~text
LEGACY_SOURCE_RELATION:
ROLE-EXEC-001
OBJ-PRD-008 OrderIntent
OBJ-PRD-010 EntryThesis
FIX-009

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.35 Defense / Risk — Integrated Review / Final Candidate Flow

### Review Result

05保存済みReferenceと今回のDefense / Risk候補を再照合した結果、Architectureを作り直す必要がある重大矛盾は確認されなかった。

保存前に以下3点を補強した。

### CORRECTION-DR-01

~~~text
execution_disposition
= Defense結果からの決定論的Boundary Projection
≠ 第二のDecision Authority
~~~

### CORRECTION-DR-02

~~~text
RiskState.allowed_exposure
= Scope-level Baseline / Ceiling

Defense Restriction Context
= Per-Decision Effective Restriction
~~~

### CORRECTION-DR-03

~~~text
Emergency Fast Path
= Restriction Governance高速化

Emergency Fast Path
≠ Authority / Approval / Provenance省略
~~~

### Final Candidate Flow

~~~text
05_DECISION
↓
Decision Result

────────────────────────
Defense / Risk
────────────────────────

Defense Evaluation
├ Decision Validity
├ RiskState
├ Authorized Constraint
├ Liquidity
├ Exposure
├ Drawdown
├ Data Quality
└ Exchange / API Health
↓
DefenseEvaluationResult
↓
DefenseDecision
├ ALLOW
├ REDUCE
└ BLOCK

別系統:

Risk Trigger / Finding
↓
REQUEST
↓
RECOMMEND
↓
APPROVE
↓
ApprovalDecision
↓
APPLY
↓
StateTransitionEvent
↓
Current RiskState

Restriction:
Emergency Fast Path candidate

Recovery:
Strict Path

────────────────────────
Defense → Execution
────────────────────────

ALLOW
→ PROCEED

REDUCE
→ PROCEED_RESTRICTED

BLOCK
→ DENY

Evaluation Fai
## 7.36 EntryThesis

### Formal Definition Candidate

> **EntryThesis = 有効なRisk-taking DecisionがDefense / Risk Gateを通過した後、OrderIntent生成直前のTrade Thesis・Decision Result・DefenseEvaluationResult・DefenseDecision・Risk Permission・Authorized Constraint・Restriction Context・Market Context・Version / Quality / Uncertaintyを、時間的に一貫した状態で固定するImmutable Entry Snapshot候補。**

中心意味:

~~~text
Trade Thesis
= なぜRiskを取りたいか

Decision Result
= Riskを取りたいか

DefenseDecision
= 今そのRiskを取って安全か

EntryThesis
= 実際にEntryへ進む直前、
  何を根拠・条件としていたか
~~~

### Canonical Flow

~~~text
Trade Thesis
↓
Decision Result
↓
DefenseEvaluationResult
↓
DefenseDecision
↓
Execution Admission
↓
RiskState / Constraint / Validity Recheck
↓
Entry Snapshot Builder
↓
EntryThesis
↓
Order Planning
↓
OrderIntent
~~~

### Generator Boundary

~~~text
Generator
= Execution Logic / Entry Snapshot Builder

Custodian
= Logger / Storage

Analyzer
= Post-Trade Analysis
~~~

FIX-009の、

~~~text
Generator
≠ Custodian
≠ Analyzer
~~~

を維持。

### Current Refinement

Legacy:

~~~text
SignalDecision
ApplicableHypothesisSet
~~~

Current候補:

~~~text
Decision Result
Applicable Knowledge / Trade Thesis Trace
~~~

へ読み替える。

### Snapshot Principle

EntryThesisは上流Object全文をDeep Copyする巨大Objectではない。

~~~text
必要なEntry時点Runtime Facts
+
Immutable / Versioned References
~~~

を固定する。

候補Trace:

~~~text
trade_thesis_ref
decision_result_ref
defense_evaluation_result_ref
defense_decision_ref
risk_state_ref
authorized_constraint_refs
entry_market_context_ref
entry_market_dna_ref
quality_ref
uncertainty
entry_snapshot_at
snapshot_builder_version
trace_id
~~~

### Recheck ≠ Re-evaluate

Entry Snapshot Builderは、

~~~text
Current RiskState
Constraint
Decision validity
Defense validity
Market Context compatibility
Version consistency
~~~

をRecheckできる。

しかし、

~~~text
Direction変更
Expected Value再計算
Trade Thesis再構成
Defense Outcome変更
~~~

を行わない。

必要ならNew Decision / Defense Cycleへ戻す。

### Failure

~~~text
ENTRY_SNAPSHOT_NOT_BUILDABLE
~~~

候補を維持。

意味:

> Defense→Execution Admissionまでは到達したが、必須ContextをEntry時点で時間的・意味的に一貫したSnapshotとして固定できない。

これは、

~~~text
Defense BLOCK
≠ ENTRY_SNAPSHOT_NOT_BUILDABLE
≠ NO_TRADE
≠ Processing FAILED
~~~

。

### Invariants

~~~text
No valid Defense
→ No EntryThesis

BLOCK / Fail-Closed
→ No EntryThesis

ENTRY_SNAPSHOT_NOT_BUILDABLE
→ No OrderIntent

EntryThesis BUILT
≠ OrderIntent guaranteed

EntryThesis
= Immutable after creation

Outcome
must not rewrite EntryThesis
~~~

### Status

~~~text
LEGACY_SOURCE_RELATION:
OBJ-PRD-010
ROLE-EXEC-001
FIX-009

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.37 OrderIntent

### Formal Definition Candidate

> **OrderIntent = 正常なEntryThesisを基準として、許可Risk Envelope内でPosition Size・Leverage・Order Style・Price Condition・Split Execution・Protection Intent・Slippage / Liquidity Constraint等を、取引所APIに依存しない形で固定するImmutable Execution Intent候補。**

中心境界:

~~~text
EntryThesis
= WHY / UNDER WHAT CONDITIONS

OrderIntent
= HOW / HOW MUCH / UNDER WHAT EXECUTION LIMITS

Exchange Adapter
= HOW ON THIS VENUE
~~~

### Order Planning Responsibility

Source-backed:

~~~text
Position Size
Leverage
Market / Limit
Split Order
Stop / Take Profit
Slippage tolerance
Liquidity requirement
~~~

Currentでは次へ整理候補:

~~~text
Sizing Intent
Leverage Intent
Entry Order Style
Price Condition
Split Execution Plan
Protection Intent
Slippage / Price Protection
Liquidity Requirement
Execution Constraints
~~~

### Sizing Boundary

~~~text
Defense / Risk
= Maximum Safety Envelope

Execution
= Actual Requested Size
~~~

必ず概念上:

~~~text
requested risk
≤ Defense Restriction
≤ Effective Risk Permission
~~~

。

Size Unitを暗黙化しない。

~~~text
BASE_QUANTITY
QUOTE_NOTIONAL
CONTRACT_QUANTITY
~~~

等のExplicit Quantity Semanticsが必要候補。

### Leverage

Leverage対応Instrumentのみ。

~~~text
Leverage Intent
≠ Risk Permission
~~~

RiskStateがExact Leverageを直接決めない。

### Order Style

Legacyで強く支持されるのは:

~~~text
MARKET
LIMIT
~~~

。

Exchange-specific enumをCoreへ持ち込まない。

~~~text
MARKET
≠ Unlimited Slippage
~~~

。

### Split

候補:

~~~text
1 EntryThesis
→ 1 OrderIntent
→ N Execution Slices
~~~

長時間Split時の再ValidationはExecution Lifecycleへ後送り。

### CORRECTION-EX-01 — Protection IntentとExit Authority

保存前Reviewで以下を明確化。

~~~text
OrderIntent Stop / TP
= Entry時点のInitial Protection Intent

Position Supervisor
= Thesis健全性監督

In-Trade Defense
= Hard Safety

Exit Engine
= 継続中の通常Exit Authority
~~~

したがって、

~~~text
Initial Stop / TP Intent
≠ 永続的なExit Decision Authority
~~~

。

Entry後の状態変化でExit判断が変わる場合、OrderIntentを書き換えず、Exit / Position側の新しいDecision / Actionとして扱う。

### Exchange Adapter Boundary

Adapter owns:

~~~text
Symbol mapping
Tick size
Minimum order
Venue enum
Authentication interface
Request / Response conversion
~~~

AdapterはOrderIntentのEconomic / Risk Meaningを拡張してはならない。

Safe conversion不能ならSubmitしない。

### Build Failure

~~~text
ORDER_INTENT_NOT_BUILDABLE
≠ Defense BLOCK
≠ Planner FAILED
~~~

例:

~~~text
safe size < minimum tradable size
required leverage unsupported
required protection unsupported
liquidity / slippage condition cannot be satisfied
~~~

### Invariants

~~~text
No EntryThesis
→ No OrderIntent

OrderIntent
≠ Exchange Order

REDUCE Restriction
must not be relaxed

OrderIntent BUILT
≠ Exchange accepted

OrderIntent
= Immutable
~~~

### Status

~~~text
LEGACY_SOURCE_RELATION:
OBJ-PRD-008
ROLE-EXEC-001
ROLE-ADP-002

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.38 ExecutionRecord

### Formal Definition Candidate

> **ExecutionRecord = 特定OrderIntentがExchange Adapterを通じて取引所へ実際にどのような注文として送信され、どのように受理・拒否・約定・部分約定・取消・失効・不明状態となったかを、Submission / Acknowledgement / Fill / Price / Size / Fee / Slippage / Latency / Exchange Status / Diagnostics付きで固定するPrimary Execution Fact候補。**

中心境界:

~~~text
OrderIntent
= What we intended

ExecutionRecord
= What actually happened at venue
~~~

### Requested / Submitted / Actual

保存前ReviewでCurrent Refinementとして3段階を維持。

~~~text
INTENDED
= OrderIntent values

SUBMITTED
= AdapterがVenue仕様へ正規化し実際に送った値

ACTUAL
= Exchangeで起きたFill / Fee / Status
~~~

例:

~~~text
requested size:
0.01037 BTC

submitted size:
0.010 BTC

filled size:
0.008 BTC
~~~

これにより、

~~~text
Planning
Adapter Conversion
Exchange Execution
~~~

を分離可能。

### Generator

~~~text
Exchange Adapter
= Canonical Generator

Logger
= Custodian

Post-Trade
= Analyzer
~~~

### Execution Fact

候補:

~~~text
order_intent_ref
submission_attempt_id
exchange_order_id
submitted_at
acknowledged_at
submitted_quantity
submitted_price
fills[]
filled_quantity
remaining_quantity
average_fill_price
partial_fill_state
fees
actual_slippage
exchange_order_state
diagnostics_ref
adapter_version
trace_id
~~~

### Fill Preservation

平均値だけに潰さず、

~~~text
fill_id
filled_at
fill_price
fill_quantity
fee
exchange_trade_id
~~~

等の個別Fill Factを保持可能にする。

### UNKNOWN ≠ REJECTED

~~~text
REJECTED
= Exchange拒否確認済み

UNKNOWN
= Orderが存在するか確定不能
~~~

UNKNOWNをFILLED / REJECTEDへ推測変換しない。
Reconciliation候補へ送る。

### Cardinality

Split / Retryを踏まえ、

~~~text
1 OrderIntent
→ 1..N ExecutionRecords
~~~

を許容候補とする。

原則、

> 1 ExecutionRecord = 1 Venue Submission Attempt / Venue Order Lifecycle候補。

### CORRECTION-EX-02 — Runtime Order StateとCanonical Record

Orderは、

~~~text
OPEN
→ PARTIAL
→ FILLED
~~~

のように時間変化する。

したがってCurrent候補では、

~~~text
Runtime Open Order State
≠ Canonical Immutable ExecutionRecord
~~~

を明確化する。

第一候補:

> Terminal / Reconciled boundaryまで確定したSubmission AttemptをCanonical ExecutionRecordとしてImmutable固定する。

Open中の詳細追跡方式:

~~~text
Runtime State
Exchange Events
Versioned Snapshot
Append-only Event
~~~

のどれを採るかは後続Execution Lifecycle Contractで決める。

現段階では新Objectを自動追加しない。

### Strategy vs Execution

~~~text
Strategy Outcome
≠ Execution Outcome
~~~

を維持。

ExecutionRecordだけでWIN / LOSSやHypothesis correctnessを決めない。

### Status

~~~text
LEGACY_SOURCE_RELATION:
OBJ-PRD-009
ROLE-ADP-002

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.39 ProductionEvidence

### Formal Definition Candidate

> **ProductionEvidence = Live Productionで生成されたExecutionRecordを、同時間帯のEntry / Market / Liquidity / Fee / Funding / Market Event / Quality Contextと結合し、Actual Slippage・Fee・Partial Fill・Latency・Liquidity Impact等をLIVE Channelの研究再利用可能なEvidenceへ構造化したImmutable Object候補。**

### Canonical Flow

~~~text
ExecutionRecord 1..N
+
EntryThesis
TradeThesis
Live Market Context
Liquidity
Fee / Funding
Market Events
Quality / Diagnostics
↓
Live Evidence Collector
↓
ProductionEvidence
channel = LIVE
↓
Post-Trade / Research
~~~

### Generator Boundary

~~~text
Live Evidence Collector
= Generator

Exchange Adapter
≠ Semantic Generator

Logger
= Custodian

Post-Trade
= Analyzer
~~~

### LIVE Identity

~~~text
evidence_source_channel = LIVE
~~~

を維持。

~~~text
Historical
≠ Demo
≠ Forward
≠ LIVE
~~~

を無言で単純合算しない。

### Evidence Groups

候補:

~~~text
Fill Metrics
Actual Slippage
Actual Fee
Funding Context
Partial Fill
Latency Components
Liquidity Impact
Market Context
Market Event Refs
Quality
Completeness
Uncertainty
Diagnostics
~~~

### Source Fact vs Derived Measurement

~~~text
ExecutionRecord fill_price
= Source Fact

ProductionEvidence actual_slippage
= Derived Measurement
~~~

Derived MeasurementはFormula / VersionへTrace可能にする方向。

### Completeness / Quality / Uncertainty

分離:

~~~text
Completeness
= 必要Observationがどこまで取得できたか

Quality
= 取得Dataをどこまで信用できるか

Uncertainty
= 測定 / Attributionにどの程度不確実性があるか
~~~

一つの万能Statusへ潰さない。

Incompleteでも残存Evidenceに価値があれば保存する。

Missing値を推測補完しない。

### CORRECTION-EX-03 — LIVE EvidenceとDemo比較を分離

~~~text
ProductionEvidence
= LIVE side facts / measurements

Demo Evidence
= DEMO side

DemoLiveDivergence
= Post-Trade comparison result
~~~

ProductionEvidence自身が、

~~~text
Demoより悪い
Execution Model failed
Hypothesis failed
~~~

等の比較結論を持たない。

Comparison-readyにするため、

~~~text
Metric Identity
Unit
Formula Version
Time Context
Market Context
~~~

を保持する。

### Research Boundary

~~~text
ProductionEvidence
→ Post-Trade / Research Router
→ Research Candidate
→ 03_RESEARCH
~~~

直接、

~~~text
Knowledge update
Trainer immediate update
Production Rule update
~~~

へ接続しない。

### Invariants

~~~text
ExecutionRecord
≠ ProductionEvidence

ProductionEvidence
≠ TradeResult

ProductionEvidence
≠ DemoLiveDivergence

ProductionEvidence
≠ Research Result

ProductionEvidence
≠ Knowledge

LIVE
must remain LIVE

Incomplete Evidence
must not be fabricated

Market Event association
≠ Causal proof

Live failure
≠ Hypothesis failure
~~~

### Status

~~~text
LEGACY_SOURCE_RELATION:
OBJ-PRD-013
ROLE-EXEC-001 Live Evidence Collector
FIX-009
OBJ-POST-006 DemoLiveDivergence

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.40 Execution — Integrated Review / Final Candidate Flow

### Review Result

Defense→Execution Contractと今回の4Objectを横断Reviewした結果、Architectureを作り直す必要がある重大矛盾は確認されなかった。

以下4点を保存前Correctionとして反映。

### CORRECTION-EX-01 — Protection Intent / Exit Authority Separation

~~~text
OrderIntent Stop / TP
= Initial Protection Intent

Exit Engine / In-Trade Defense
= Ongoing Exit Authority
~~~

Entry後にOrderIntentを書き換えてExit Policyを更新しない。

### CORRECTION-EX-02 — Runtime Order State / Immutable ExecutionRecord Separation

~~~text
Open Order Runtime State
≠ Canonical immutable ExecutionRecord
~~~

Canonical recordのTerminal / Reconciled boundaryは候補として維持し、詳細Event Modelは後続Execution Lifecycleへ。

### CORRECTION-EX-03 — LIVE Evidence / Comparative Analysis Separation

~~~text
ProductionEvidence
= LIVE Evidence

DemoLiveDivergence
= Post-Trade comparative analysis
~~~

### CORRECTION-EX-04 — Pre-submit Runtime Safety Recheck

OrderIntent生成後でも、

~~~text
RiskState
Authorized Constraint
OrderIntent expiry
EntryThesis expiry
Emergency / Runtime Safety
~~~

が変化し得る。

したがって、

~~~text
OrderIntent BUILT
≠ unconditional Submit Permission
~~~

。

Exchange Adapterへ実Submissionする直前に、Execution Controller / Submission Gate相当のRuntime Safety Recheck責任が必要候補。

重要:

~~~text
Submission Gate
≠ New Market Decision
≠ New Defense Decision

Submission Gate
= 既存Permission / Validity / Emergency状態が
  submit時点でも成立しているか確認するProcessing Responsibility
~~~

新Top-Level RoleやPersistent Objectの追加は現段階では行わない。

### Responsibility Review

~~~text
Defense / Risk
= 今Riskを取って安全か

Entry Snapshot Builder
= Entry直前の根拠を固定

Order Planning
= どう注文するか

Exchange Adapter
= Venue仕様へ変換し実Execution Factを回収

Live Evidence Collector
= Execution FactをLIVE Evidenceへ構造化

Position Supervisor
= Entry後のThesis健全性監視

In-Trade Defense
= Position中Hard Safety

Exit Engine
= Ongoing Exit Decision

Post-Trade
= 結果の意味を分析
~~~

責任重複は許容範囲内で分離可能。

### Trace Review

最低限のCanonical Trace:

~~~text
ProductionEvidence
↓
ExecutionRecord[]
↓
OrderIntent
↓
EntryThesis
↓
DefenseEvaluationResult / DefenseDecision
↓
Decision Result
↓
Trade Thesis
↓
Applicable Knowledge / Research
~~~

Risk side:

~~~text
OrderIntent / EntryThesis
↓
Defense Restriction
↓
RiskState
↓
StateTransitionEvent
↓
ApprovalDecision / Trigger
~~~

Trace断絶はCurrent候補上確認されなかった。

### Failure Separation

~~~text
THESIS_NOT_BUILDABLE
≠ NO_TRADE

Defense BLOCK
≠ Fail-Closed

ENTRY_SNAPSHOT_NOT_BUILDABLE
≠ Defense BLOCK

ORDER_INTENT_NOT_BUILDABLE
≠ Planner FAILED

Adapter Conversion Failure
≠ Exchange REJECTED

Exchange REJECTED
≠ Submission UNKNOWN

ExecutionRecord INCOMPLETE
≠ ProductionEvidence INCOMPLETE

ProductionEvidence INCOMPLETE
≠ Research Failure
~~~

### Deferred but Required Execution Work

Execution主要4Objectは揃ったが、次の詳細は後続Contractとして未確定。

~~~text
Execution Submission Gate
Open Order Runtime Lifecycle
Retry / Idempotency / Reconciliation
Split Execution Lifecycle
Position creation / Position identity
Exit-side OrderIntent / ExecutionRecord reuse
Protection order lifecycle
Venue routing / multi-exchange policy
~~~

これらは重大矛盾ではなく、Object定義後に処理Contractとして詰める項目。

### Final Candidate Flow

~~~text
05_DECISION
↓
Decision Result
↓
Defense Evaluation
↓
DefenseEvaluationResult
↓
DefenseDecision
↓
Defense → Execution Admission
↓
Entry Snapshot Builder
↓
EntryThesis
↓
Order Planning
↓
OrderIntent
↓
Submission Safety Recheck candidate
↓
Exchange Adapter
↓
ExecutionRecord 1..N
↓
Live Evidence Collector
↓
ProductionEvidence [LIVE]
↓
Logger / Immutable Storage
↓
Post-Trade Analysis
↓
Research Router
↓
03_RESEARCH
~~~

### Absolute Semantic Boundaries

~~~text
EntryThesis
≠ OrderIntent

OrderIntent
≠ Exchange Order

OrderIntent BUILT
≠ Submitted

ExecutionRecord
≠ ProductionEvidence

ProductionEvidence
≠ Post-Trade Analysis

ProductionEv
## 7.41 TradeResult / Post-Trade Entry Boundary

### Boundary Definition Candidate

> **TradeResult = 一つのTradeがTerminal Conditionへ到達した時点で、Entry / Exit・Exposure・ExecutionRecord・ProductionEvidence・Fee / Funding・Slippage・PnL・MAE / MFE・Exit Reason・Quality / Provenanceを、意味評価を加えず固定するFinal Trade Outcome Fact候補。**

Post-TradeはTradeResultを分析Inputとして扱い、Source Factを書き換えない。

~~~text
ExecutionRecord
= 個々の注文で何が起きたか

ProductionEvidence
= LIVEで何が観測されたか

TradeResult
= Trade全体として何が起きたか

Post-Trade Analysis
= それをどう解釈するか
~~~

### Ownership Correction

LegacyではLogger / Post-TradeがTradeResult Owner候補だが、Currentでは、

~~~text
Trade Finalization / Outcome Assembly
= Generator responsibility

Logger
= Custodian

Post-Trade
= Analyzer
~~~

とする方が既存原則と整合する。

### Critical Invariants

~~~text
TradeResult
≠ OutcomeAnalysisResult

TradeResult
≠ Hypothesis Result

Positive PnL
≠ Thesis correct

Negative PnL
≠ Thesis wrong

Gross PnL
≠ Net PnL

Slippage metric
must not be double-counted in PnL
~~~

~~~text
LEGACY_SOURCE_RELATION:
OBJ-PRD-014 TradeResult

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE / OWNER BOUNDARY REDESIGN

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.42 OutcomeAnalysisResult

### Formal Definition Candidate

> **OutcomeAnalysisResult = TradeResultを、事前Expectationとの整合性・Horizon・MAE / MFE・Exit Timing・Execution Cost / Slippage・Risk-adjusted Outcome・Opportunity・System Integrityへ分解するVersioned Immutable Post-Trade Analysis候補。**

### CORRECTION-PT-01 — Legacy 6分類を3軸へ分離

Legacy:

~~~text
EXPECTED_SUCCESS
UNEXPECTED_SUCCESS
EXPECTED_FAILURE
UNEXPECTED_FAILURE
MISSED_OPPORTUNITY
SYSTEM_FAILURE
~~~

Current:

~~~text
Axis A:
Economic Outcome / Expectation Alignment

Axis B:
Opportunity

Axis C:
System Integrity
~~~

Derived Outcome Classification候補:

~~~text
EXPECTED_SUCCESS
UNEXPECTED_SUCCESS
EXPECTED_FAILURE
UNEXPECTED_FAILURE
~~~

重要:

~~~text
EXPECTED_FAILURE
≠ System Failure

UNEXPECTED_SUCCESS
≠ Thesis proven

SYSTEM_FAILURE
can coexist with Profit

MISSED_OPPORTUNITY
can coexist with Profit or Loss
~~~

OutcomeAnalysisResultはPost-Trade分析の入口であり、Root Causeを確定しない。

~~~text
LEGACY_SOURCE_RELATION:
OBJ-POST-001
ROLE-ANL-001

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.43 TradeThesisEvaluation

### Formal Definition Candidate

> **TradeThesisEvaluation = TradeのPnLとは独立して、Entry時に固定されたTrade ThesisのDirection・Expected Effect・Magnitude / Sequence / Persistence・Horizon・Invalidation・Contradiction・Applicability・Uncertaintyが実市場Behavior / Evidenceとどの程度整合したかを評価するVersioned Immutable Analysis候補。**

### Main Axes

~~~text
Direction Match
Expected Effect Match
Magnitude / Sequence / Persistence
Horizon Match
Invalidation Evaluation
Contradiction Handling
Applicability Evaluation
Uncertainty Calibration
Dependency / Redundancy Context
Risk Coverage
~~~

Overall Outcome候補:

~~~text
MATCHED
PARTIALLY_MATCHED
MISMATCHED
INVALIDATED
INDETERMINATE
~~~

多数決で決めない。

### Critical Boundaries

~~~text
Profit
≠ Thesis correct

Loss
≠ Thesis wrong

Direction Match
≠ Thesis proven

Expected Effect observed
≠ Cause proven

Invalidation triggered
≠ Hypothesis retired

Applicability mistake
≠ Knowledge invalid
~~~

~~~text
LEGACY_SOURCE_RELATION:
OBJ-POST-002
ROLE-ANL-001

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.44 HypothesisAttribution / Thesis Member Attribution

### Formal Definition Candidate

> **HypothesisAttribution = Trade Thesisを構成した各Memberについて、Entry時Role・Expected Effect・Horizon・Evidence Validity・Applicability・Contradiction・Shared Evidence・Dependency・Redundancy・Common Causeを個別評価し、そのMemberがThesis全体へどの程度の独立した説明価値を持ったかを記録するVersioned Immutable Analysis候補。**

### CORRECTION-PT-02 — Current Target Refinement

LegacyはHypothesis-centric。

Current 05では、

~~~text
Applicable Knowledge
↓
Trade Thesis Construction
↓
Thesis-relative Role
~~~

なので、Current意味は:

~~~text
thesis_member_ref
↓
source_knowledge_ref
↓
source_hypothesis_ref / research provenance
~~~

が自然。

PRIMARY / SUPPORTING / CONDITIONAL / CONTRADICTING はKnowledgeの永久属性ではなく、特定Trade Thesis内の相対Role。

### Raw Match ≠ Independent Contribution

~~~text
Member Match
≠ Causal Proof

Member Count
≠ Independent Evidence Count

Shared Evidence
≠ Independent Support

Dependency
≠ Invalidity

Redundancy
≠ Additional Support

Common Cause
≠ Multiple Independent Causes
~~~

CONDITIONALは弱いSUPPORTINGではなく、When / Under What Conditionsを担う。

Current正式名は将来 ThesisMemberAttribution 等へ改名候補だが、現段階ではLegacy対応上HypothesisAttributionを作業名として保持する。

~~~text
LEGACY_SOURCE_RELATION:
OBJ-POST-003
ROLE-ANL-001

LEGACY_REVIEW_STATUS:
PARTIAL_REUSE / TARGET REFINEMENT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.45 DefenseDecisionEvaluation

### Formal Definition Candidate

> **DefenseDecisionEvaluation = 過去のALLOW / REDUCE / BLOCKについて、当時のRiskState・Authorized Constraint・Liquidity・Exposure・Drawdown・Data / Exchange Health等と、その後のActual / Shadow / Counterfactual Outcomeを比較し、Safety判断がRisk抑制・損失回避・過剰制限・機会損失等へどう作用した可能性があるかを評価するVersioned Immutable Post-Trade Analysis候補。**

### CORRECTION-PT-03 — Naming Collision

Currentには既にPre-Trade:

~~~text
Defense Evaluation
→ DefenseDecision
~~~

が存在する。

Post-Trade Legacy DefenseEvaluation はCurrentでは:

~~~text
DefenseDecisionEvaluation
~~~

と呼ぶ方が安全。

### Evaluation Axes

~~~text
Decision Appropriateness
Safety Benefit
Restriction Cost
Gate Effectiveness
Constraint Effectiveness
Counterfactual Confidence
~~~

Outcome-specific Candidate:

~~~text
ALLOW
→ False Allow Candidate

REDUCE
→ Over / Under Restriction Candidate

BLOCK
→ False Block Candidate
~~~

ただし全てCandidate。

~~~text
avoided_loss
→ estimated_avoided_loss

missed_profit
→ estimated_missed_profit
~~~

Actual Factとして扱わない。

Hard Safetyについて:

~~~text
Would-have-profited
≠ Hard Block was wrong
~~~

~~~text
LEGACY_SOURCE_RELATION:
OBJ-POST-004

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / NAME + COUNTERFACTUAL REFINEMENT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.46 SupervisorEvaluation

### Formal Definition Candidate

> **SupervisorEvaluation = Position保有中にPosition Supervisorが生成したThesis Health State / Warningについて、実際のThesis deterioration・Invalidation・Recoveryとの整合性、検知Timing・Severity・Persistence・State Stability・Exit EngineへのAdvisory Utilityを評価するVersioned Immutable Post-Trade Analysis候補。**

### Main Axes

~~~text
Detection Accuracy
Detection Timing
Severity Calibration
State Transition Quality
Persistence / Stability
Action Utility
False Alarm
Late Warning
Missed Warning
Recovery Detection
~~~

### Temporal Boundary

~~~text
Pre-Entry Safety
= Defense

Post-Entry Thesis Monitoring
= Supervisor

Hard Safety During Position
= In-Trade Defense

Normal Exit Authority
= Exit Engine
~~~

### Important Separation

~~~text
Warning
≠ Exit Command

Action Followed
≠ Supervisor correct

Action Not Followed
≠ Supervisor wrong

Trade Loss
≠ Supervisor Failure
~~~

Legacy Hypothesis-centric health fieldsはCurrentではThesis Member Healthへ意味上読み替える候補。

Hysteresisでは、

~~~text
Noise reduction
vs
Detection latency
~~~

を研究対象にする。

~~~text
LEGACY_SOURCE_RELATION:
OBJ-POST-005
ROLE-SUP-001

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.47 DemoLiveDivergence

### Formal Definition Candidate

> **DemoLiveDivergence = Historical / OOS / Demo Forward等のReference ProfileとLIVE ProductionEvidenceを、Target Version・Market / Regime・Scale・Execution / Measurement条件の比較可能性を確認した上で比較し、Market Behavior・Execution・Cost・Liquidity・Regime・Data Quality・Simulation AssumptionのどこにMaterialな差が生じたかを原因候補と分離して保存するVersioned Immutable Comparative Analysis候補。**

### CORRECTION-PT-04 — Comparability Gate

比較前に:

~~~text
COMPARABLE
PARTIALLY_COMPARABLE
NOT_COMPARABLE
INDETERMINATE
~~~

を評価する。

比較Context候補:

~~~text
Instrument
Venue
Direction
Horizon
Position Scale
Market DNA / Regime
Trade Thesis Version
Execution Policy Version
Fee Structure
Liquidity Context
Metric Identity / Formula Version
Data Quality
~~~

### Divergence Dimensions

~~~text
Market Behavior
Execution
Slippage / Fee / Funding
Liquidity
Regime / Market DNA
Scale / Venue
Data Quality
Measurement Definition
Simulation Assumption
~~~

### Critical Boundary

~~~text
NOT_COMPARABLE
≠ NO_DIVERGENCE

Observed Divergence
≠ Proven Cause

Live Failure
≠ Hypothesis Failure

Live Failure
≠ Knowledge Invalid

Model Error Candidate
≠ Model Error Confirmed
~~~

Channelを消して単純合算しない。

~~~text
LEGACY_SOURCE_RELATION:
OBJ-POST-006
ProductionEvidence
Evidence Channel definition

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.48 CounterfactualResult

### Formal Definition Candidate

> **CounterfactualResult = 過去のDecision Pointとその時点で利用可能だったInformation Setを固定し、Actual Actionの代わりに明示されたAlternative Actionを選択していた場合のOutcomeを、Model Assumption・Execution Realism・Feasibility・Uncertainty・Limitations付きでSimulationし、COUNTERFACTUAL Channelの研究補助結果として保存するVersioned Immutable Object候補。**

### CORRECTION-PT-05 — Hindsight Leakage Prevention

~~~text
Decision-time Information Set
≠ Evaluation-time Data Set
~~~

Future DataはAlternative Actionを正当化するために使用しない。
Future DataはT0で固定したAlternative Outcomeを評価するためには利用可能。

### Minimal Intervention

原則:

~~~text
1 Counterfactual
≈ 1 Main Intervention
~~~

変更点を明示する。

### Feasibility

候補:

~~~text
POLICY_COMPLIANT
POLICY_VIOLATING_RESEARCH_SCENARIO
TECHNICALLY_INFEASIBLE
CONDITIONALLY_FEASIBLE
UNKNOWN
~~~

Hard Safetyを無視したScenarioも研究可能だが、Productionで取るべきだった機会として扱わない。

### Execution Realism

~~~text
Large Size Change
≠ Naive Linear PnL Scaling
~~~

必要に応じてFill / Slippage / Liquidity / Market Impact / Latency / Fee / Funding Modelを使う。

### Channel Separation

~~~text
LIVE
≠ SHADOW
≠ DEMO_FORWARD
≠ COUNTERFACTUAL
~~~

Best hindsight action ≠ actionable policy。

~~~text
LEGACY_SOURCE_RELATION:
OBJ-POST-007
Evidence Channel definition

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / MAJOR PRECISION EXPANSION

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.49 Post-Trade — Integrated Review / Final Candidate Flow

### Review Result

Legacy ROLE-ANL-001 Post-Trade Analysis と7つのPost-Trade Objectを、Current Decision / Defense / Execution / Research境界へ照合した結果、Architectureを作り直す必要がある重大矛盾は確認されなかった。

保存前に以下を正式補正した。

### CORRECTION-PT-01 — Outcome分類の多軸化

~~~text
Outcome Alignment
≠ Opportunity
≠ System Integrity
~~~

### CORRECTION-PT-02 — Whole / Parts分離

~~~text
TradeThesisEvaluation
= Thesis全体

HypothesisAttribution
= Thesis Member個別
~~~

### CORRECTION-PT-03 — Defense命名衝突解消

~~~text
Pre-Trade:
Defense Evaluation

Post-Trade:
DefenseDecisionEvaluation
~~~

### CORRECTION-PT-04 — Demo/LIVE比較前のComparability

~~~text
Comparison Conditions
↓
Comparability
↓
Difference Measurement
~~~

NOT_COMPARABLEを差なしへ変換しない。

### CORRECTION-PT-05 — Actual / Counterfactual分離

~~~text
Actual Fact
≠ Shadow
≠ Demo
≠ Counterfactual
~~~

### CORRECTION-PT-06 — Post-Trade Has No Apply Authority

~~~text
Post-Trade Analysis
may create:
Analysis
Candidate
Request / Recommendation material

Post-Trade Analysis
must not directly APPLY:
Hypothesis State
Knowledge State
RiskState
Defense Rule
Supervisor Threshold
Production Rule
Trainer Update
~~~

### Responsibility Matrix

~~~text
OutcomeAnalysisResult
= Trade結果の全体的な意味

TradeThesisEvaluation
= 市場Thesis全体の整合性

HypothesisAttribution
= Thesis Member個別の説明貢献

DefenseDecisionEvaluation
= Entry前Safety判断の有効性

SupervisorEvaluation
= Entry後Thesis監視の有効性

DemoLiveDivergence
= Validation ChannelとLIVE Realityの差

CounterfactualResult
= Alternative ActionのSimulation結果
~~~

### No Overwrite Principle

すべての分析ObjectはSource Objectを改変しない。

~~~text
TradeResult
ProductionEvidence
ExecutionRecord
EntryThesis
TradeThesis
DefenseDecision
PositionThesisState History
~~~

はSource / Snapshotとして保持する。

分析Logic改善時は新Versionを生成する。

### Research Feedback Boundary

~~~text
Post-Trade Analysis Objects
↓
ResearchCandidate(s)
↓
Research Router
↓
ResearchRoute
↓
03_RESEARCH
~~~

Post-Trade Analysis Object自体はRouting Authorityではない。

### Canonical Integrated Flow

~~~text
Trade / Position Terminal
↓
TradeResult
+
ProductionEvidence
+
Entry / Decision / Defense / Execution / Position / Exit Trace
↓
OutcomeAnalysisResult
↓
├ TradeThesisEvaluation
│   ↓
│ HypothesisAttribution
│
├ DefenseDecisionEvaluation
│
├ SupervisorEvaluation
│
├ DemoLiveDivergence
│
└ CounterfactualResult
↓
ResearchCandidate(s)
↓
Research Router
↓
ResearchRoute
↓
03_RESEARCH
↓
Research Plan / Validation
↓
Validated Research Result
↓
04_KNOWLEDGE_APPLICABILITY
↓
05_DECISION
↓
Production
↓
Post-Trade
~~~

### Failure / Meaning Separation

~~~text
Trade LOSS
≠ Thesis Failure

Thesis MISMATCH
≠ Hypothesis Retired

Member mismatch
≠ Knowledge invalid

False Block Candidate
≠ Defense Rule invalid

Late Warning Candidate
≠ Supervisor Rule invalid

Demo/LIVE divergence
≠ Model failure confirmed

Counterfactual Better Outcome
≠ Production should have chosen it
~~~

### Deferred but Required Work

~~~text
Research Router / ResearchRoute

ExitDecision / Exit-side Evaluation refinement

In-Trade Defense post-trade evaluation

Position identity / lifecycle contract

Post-Trade analysis orchestration order

Cross-analysis conflict handling

Analysis-to-ResearchCandidate contract
~~~

直近Owner:

~~~text
Research Router / ResearchRoute
~~~

### Integrated Status

> **Post-Trade 7系統は、Trade Outcomeを単一WIN / LOSSへ潰さず、市場理解・Thesis構成・Safety・Position監視・Demo/LIVE差・Alternative Actionを独立評価してResearchへ戻すCurrent Reference Proposalとして整合した。重大な責任重複はなく、残る主な未設計境界はResearch Router / ResearchRouteである。**

~~~text
LEGACY_CONFLICT_STATUS:
MINOR / MODERATE NAMING

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

idence
≠ DemoLiveDivergence

Initial Stop / TP Intent
≠ Ongoing Exit Authority

Execution Outcome
≠ Strategy Outcome

Live Failure
≠ Hypothesis Failure

Generator
≠ Custodian
≠ Analyzer
~~~

### Integrated Status

> **Execution主要4ObjectとDefense→Execution境界は、Legacy Execution / FIX-009をCurrent 05 / Defense設計へ接続するReference Proposalとして整合し、重大な責任衝突は確認されなかった。ただしSubmission Lifecycle / Position / Exitの詳細Contractは未設計。**

~~~text
LEGACY_CONFLICT_STATUS:
MINOR

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / PARTIAL_REUSE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

lure
→ Fail-Closed
→ DENY

↓
Execution Admission
↓
Entry Snapshot Builder
↓
EntryThesis
↓
OrderIntent
~~~

### Absolute Semantic Boundaries

~~~text
Decision Result
≠ DefenseDecision

DefenseDecision
≠ RiskState

RiskState
≠ Production Promotion

RiskState
≠ Knowledge Health

BLOCK
≠ Fail-Closed

APPROVE
≠ APPLIED

Emergency Fast Path
≠ Governance Bypass

ALLOW
≠ Order Sent

REDUCE
≠ Exact Position Size

No EntryThesis
→ No OrderIntent
~~~

### Status

> **このDefense / Risk全体はLegacy Defense / State Authority / Approval / Risk Separation / Entry Boundaryを比較して作ったReference Proposalであり、Current正式設計ではない。**

~~~text
CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---


## 7.50 Finding Pipeline — Integrated Cross-Review

### Review Target

本Sectionは以下5責任を横断ReviewしたCurrent Reference Proposalである。

~~~text
Finding Extractor
Finding Normalizer
Finding Type Registry / Normalization Mapping
Candidate Promotion
Research Router / ResearchRoute
~~~

Source-backed Authority:

~~~text
03_RESEARCH
ROLE-ANL-001 Post-Trade Analysis
ROLE-RTR-001 Research Router
OBJ-POST-001..008
~~~

ただしFinding Extractor / Normalizer / Registry / Candidate Promotionの詳細ContractはLegacyに明示されていないためCurrent Derived Proposalである。

### Review Result

重大なArchitecture破綻は確認されなかった。

ただし責任重複・抜けを避けるため、以下8補正を固定候補とする。

### CORRECTION-FP-01 — Post-Trade→ResearchCandidate直結を廃止候補

7.49のReference Flowは概念上、

~~~text
Post-Trade Analysis
→ ResearchCandidate
~~~

と短縮されていた。

Current Detailed Candidate Flowではこれを以下へ展開する。

~~~text
Post-Trade Analysis
↓
Finding Extractor
↓
ExtractedFindingDraft
↓
Finding Normalizer
↓
Canonical Finding
↓
Candidate Promotion
↓
ResearchCandidate
↓
Research Intake
~~~

Analysis Object自身をそのままResearchCandidateにしない。

### CORRECTION-FP-02 — Materiality / Research Value Authority分離

三つの段階を混同しない。

~~~text
Finding Extractor:
Findingとして非自明なSemantic Deltaか？

Candidate Promotion:
Research Intakeへ提示するResearch Problem Seedになり得るか？

Research Intake:
実際に研究対象として受理 / 保留 / 統合 / Rejectするか？
~~~

ExtractorはFinal Research Valueを決めない。

Candidate PromotionはResearch Resource Allocationを決めない。

### CORRECTION-FP-03 — Duplicate / Merge Authority分離

~~~text
Normalizer:
Semantic Fingerprintを生成可能
ただしMergeしない

Candidate Promotion:
同一Underlying FindingをCandidate単位へ集約可能
ただし既存Researchとの正式Mergeはしない

Research Intake:
既存Candidate / Researchとの正式MERGE Authority
~~~

同一Trade / Market Event由来の複数Analysisを独立Evidenceとして水増ししない。

### CORRECTION-FP-04 — Research Routerと03 Routingを二段階化

Legacy Research RouterとCurrent 03 Routing / Prioritizationの責任重複を解消する。

~~~text
Research Router
= Research Ingress Domain Routing
  どの研究領域がOwnerか？

03_RESEARCH Routing
= Research Method / Validation Routing
  どう研究するか？
~~~

Research RouterはHistorical / OOS / Stress等を直接起動しない。

### CORRECTION-FP-05 — RouterはResearch Intake ACCEPT後

~~~text
Canonical Finding
↓
Candidate Promotion
↓
ResearchCandidate
↓
Research Intake
↓
ACCEPT
↓
Research Router
~~~

DEFER / MERGE / REJECT / NEED_MORE_CONTEXT状態のCandidateを自動Routingしない。

### CORRECTION-FP-06 — CROSS_ANALYSIS Finding補完

7系統単体Analysisだけでは検出できない以下をCross-Analysis Reviewで補う。

~~~text
FND.CROSS_ANALYSIS.ANALYSIS_CONFLICT
FND.CROSS_ANALYSIS.SHARED_ORIGIN_OVERCOUNT_RISK
FND.CROSS_ANALYSIS.TRACE_GAP
FND.CROSS_ANALYSIS.VERSION_MISMATCH
FND.CROSS_ANALYSIS.RESPONSIBILITY_AMBIGUITY
~~~

Cross-Analysisは単一Analysis Extractorの責任ではない。

### CORRECTION-FP-07 — UNMAPPABLEとUNKNOWN_STRUCTUREを分離

~~~text
UNMAPPABLE
= Normalizerが既存TaxonomyへMappingできない

FND.DISCOVERY.UNKNOWN_STRUCTURE
= 市場 / System上の未知構造そのものがFinding
~~~

Taxonomy不足を市場の未知構造と誤認しない。

### CORRECTION-FP-08 — Stage-local NEED_MORE_CONTEXT

各StageのNEED_MORE_CONTEXTは意味が異なる。

~~~text
Extractor NEED_MORE_CONTEXT
= Finding成立判定に必要なContext不足

Normalizer NEED_MORE_CONTEXT
= Canonical Mappingに必要なContext不足

Candidate Promotion NEED_MORE_CONTEXT
= Candidate形成に必要なResearch Value Context不足

Research Intake NEED_MORE_CONTEXT
= Research受理判断に必要なContext不足

Router NEED_MORE_CONTEXT
= Domain Routingに必要なContext不足
~~~

一つの共通Stateへ潰さず、origin_stageを保持する。

### Final Responsibility Chain

~~~text
Post-Trade Analysis
= Meaning Analysis

Finding Extractor
= What semantic issue exists?

Finding Normalizer
= What canonical language represents it?

Finding Type Registry
= Which canonical vocabulary is allowed?

Candidate Promotion
= Is this worth presenting to Research Intake?

Research Intake
= Should Research accept it?

Research Router
= Which Research Domain owns it?

03 Routing / Prioritization
= How and when should it be studied?

Research Plan
= What exact validation plan will be executed?
~~~

### Cross-Review Status

~~~text
MAJOR_RESPONSIBILITY_CONFLICT:
NONE after corrections

KNOWN_GAPS:
- Taxonomy Governance detailed approval process
- Cross-Analysis extraction detailed rules
- Candidate aggregation detailed algorithm
- Research Intake formal state contract
- Research Domain Registry
- Research Method Routing detailed contract

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.51 Finding Extractor Common Contract

### Formal Definition Candidate

> **Finding Extractor = Post-Trade Analysis Result内の状態・差分・異常・矛盾・未知・限界・Opportunity候補等について、Source Identity・Traceability・Evaluability・Temporal Validity・Comparison Validity・Semantic Significance・Quality・Dependency・Scope・Claim Boundaryを共通Gateで確認し、Findingとして表現可能な意味単位だけを抽出するProcessing Responsibility候補。**

### Responsibility

~~~text
Analysis
= What does the result mean?

Finding Extractor
= Is there a semantic Finding we are allowed to state?
~~~

Does Not Own:

~~~text
Canonical Finding Code
ResearchCandidate
Research Admission
Research Route
Root Cause
Production Action
~~~

### Common Gate Order

~~~text
G0 Source Contract
↓
G1 Identity / Version Binding
↓
G2 Traceability
↓
G3 Evaluability
↓
G4 Temporal Validity
↓
G5 Reference / Comparability Validity
↓
G6 Semantic Delta
↓
G7 Finding Significance
↓
G8 Quality / Completeness
↓
G9 Shared Origin / Dependency
↓
G10 Responsibility / Scope
↓
G11 Claim Boundary / Non-Causality
↓
G12 Finding Atomicity
↓
G13 Normal-State Suppression
↓
Extraction Decision
~~~

### Hard Gate Candidates

~~~text
G0 Source Contract
G1 Identity / Version
G2 Minimum Traceability
G3 Evaluability
G4 Temporal Validity when required
G5 Comparability when required
G10 Responsibility / Scope
G11 Claim Boundary
~~~

### Contextual Gate Candidates

~~~text
G6 Semantic Delta
G7 Finding Significance
G8 Quality / Completeness
G9 Shared Origin / Dependency
G12 Atomicity
G13 Normal-State Suppression
~~~

### Extraction Decisions

~~~text
EXTRACT
NO_FINDING
NEED_MORE_CONTEXT
EXTRACTION_FAILED
~~~

Meaning:

~~~text
EXTRACT
= Finding Draft生成可能

NO_FINDING
= Findingなしと評価できた正常結果

NEED_MORE_CONTEXT
= Finding有無をまだ評価できない

EXTRACTION_FAILED
= Extractor処理自体のFailure
~~~

### Critical Semantics

~~~text
NOT_EVALUABLE
≠ MISMATCH

UNKNOWN
≠ FAILURE

NOT_COMPARABLE
≠ NO_DIVERGENCE

Difference
≠ Finding automatically

Loss
≠ Failure Finding automatically

Profit
≠ No Finding automatically
~~~

### Input Candidate

~~~text
Versioned Post-Trade Analysis Result
Source Facts / Evidence
Time Context
Reference / Expected Context
Quality Context
Dependency Context
Analysis-specific Extraction Policy
~~~

### Output Candidate

~~~text
0..N ExtractedFindingDraft
+
Extraction diagnostics / unresolved context
~~~

Conceptual Draft:

~~~text
ExtractedFindingDraft
├ source_analysis_ref
├ raw_finding_kind
├ subject_refs
├ observed_state
├ reference_state
├ difference_context
├ significance_context
├ quality_context
├ uncertainty
├ origin_fact_refs
├ dependency_context
├ statement_seed
└ limitations
~~~

### Invariants

~~~text
Finding Extractor
≠ Analyzer

Finding Extractor
≠ Normalizer

Finding Extractor
≠ Candidate Promotion

Finding Extractor
must not invent Cause

Finding Extractor
must not create ResearchRoute

Finding Statement Seed
must not exceed Source Analysis

Shared Origin
must remain visible
~~~

### Status

~~~text
SOURCE_STATUS:
CURRENT_DERIVED

CURRENT_03_CONFLICT_STATUS:
NONE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.52 Finding Normalizer Common Contract

### Formal Definition Candidate

> **Finding Normalizer = Finding Extractorによって成立済みとされたExtractedFindingDraftについて、その意味を新たに解釈・拡張せず、Canonical Finding Domain・Class・Code・Standard Statement・Subject / Trace / Quality / Uncertainty / Dependency Contextを共通規則へ正規化し、市場理解OS全体で参照可能なCanonical Findingを生成するProcessing Responsibility候補。**

### Fixed Flow

~~~text
ExtractedFindingDraft
↓
N0 Draft Contract Validation
↓
N1 Domain Resolution
↓
N2 Class Resolution
↓
N3 Canonical Code Resolution
↓
N4 Taxonomy Registry Validation
↓
N5 Subject / Scope Binding
↓
N6 Trace / Provenance Binding
↓
N7 Standard Statement Generation
↓
N8 Quality / Uncertainty Preservation
↓
N9 Shared-Origin / Dependency Preservation
↓
N10 Semantic Fingerprint
↓
N11 Semantic Integrity Check
↓
Canonical Finding
~~~

### Normalization Decisions

~~~text
NORMALIZED
NEED_MORE_CONTEXT
UNMAPPABLE
NORMALIZATION_FAILED
~~~

NO_FINDINGはNormalizerのStateではない。

### Critical Separation

~~~text
Extraction Policy
= Findingが存在する条件

Normalization Policy
= Findingを何と呼ぶか

Finding Type Registry
= どのCanonical語彙が存在可能か
~~~

### Canonical Structured Fields are Source

~~~text
Structured Finding Data
= Semantic Source

Standard Statement
= Human-readable Projection
~~~

StatementだけからFindingを再構築しない。

### Semantic Fingerprint

候補:

~~~text
finding_code
subject_ref
scope
origin key
observation window
~~~

等からDuplicate Detection Hintを作れる。

重要:

~~~text
Fingerprint
≠ Merge Authority

finding_id
≠ semantic_fingerprint
~~~

### Invariants

~~~text
Normalizer
must not add Cause

Normalizer
must not change Research Value

Normalizer
must not change Quality upward

Normalizer
must preserve Uncertainty

Normalizer
must preserve Candidate semantics

Normalizer
must preserve Dependency

Domain
≠ Root Cause

Domain
≠ Research Domain

Class
≠ Severity

Finding Code
≠ Research Route
~~~

### Status

~~~text
SOURCE_STATUS:
CURRENT_DERIVED

CURRENT_03_CONFLICT_STATUS:
NONE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.53 Finding Type Registry v1.0 / Normalization Mapping

### Registry Identity

~~~text
taxonomy_version:
FINDING_TAXONOMY_v1.0

normalization_policy_version:
FINDING_NORMALIZATION_v1.0
~~~

### Canonical Code Format

~~~text
FND.<DOMAIN>.<SPECIFIC_CODE>
~~~

VersionをCode名へ埋め込まない。

### Fixed Domains

~~~text
OUTCOME
THESIS
THESIS_MEMBER
DEFENSE
SUPERVISOR
DEMO_LIVE
COUNTERFACTUAL
CROSS_ANALYSIS
DISCOVERY
~~~

### Fixed Classes

~~~text
DEVIATION
ANOMALY
CONTRADICTION
FAILURE_CANDIDATE
SYSTEM_GAP
BOUNDARY
SAFETY_GAP
MONITORING_GAP
VALIDATION_DIVERGENCE
MODEL_GAP
OPPORTUNITY
QUALITY_GAP
UNKNOWN_STRUCTURE
POSITIVE_DISCOVERY
ANALYSIS_CONFLICT
~~~

### Source Analysis → Domain

~~~text
OutcomeAnalysisResult
→ OUTCOME

TradeThesisEvaluation
→ THESIS

HypothesisAttribution / ThesisMemberAttribution
→ THESIS_MEMBER

DefenseDecisionEvaluation
→ DEFENSE

SupervisorEvaluation
→ SUPERVISOR

DemoLiveDivergence
→ DEMO_LIVE

CounterfactualResult
→ COUNTERFACTUAL

Cross-Analysis Review
→ CROSS_ANALYSIS
~~~

### OUTCOME Mapping

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| EXPECTATION_MISMATCH | DEVIATION | FND.OUTCOME.EXPECTATION_MISMATCH |
| UNEXPECTED_SUCCESS | POSITIVE_DISCOVERY | FND.OUTCOME.UNEXPECTED_SUCCESS |
| UNEXPECTED_FAILURE | FAILURE_CANDIDATE | FND.OUTCOME.UNEXPECTED_FAILURE |
| OUTCOME_HORIZON_MISMATCH | DEVIATION | FND.OUTCOME.OUTCOME_HORIZON_MISMATCH |
| EXIT_TIMING_OPPORTUNITY | OPPORTUNITY | FND.OUTCOME.EXIT_TIMING_OPPORTUNITY |
| RISK_ADJUSTED_OUTCOME_ANOMALY | ANOMALY | FND.OUTCOME.RISK_ADJUSTED_OUTCOME_ANOMALY |
| EXECUTION_COST_IMPACT | DEVIATION | FND.OUTCOME.EXECUTION_COST_IMPACT |
| SYSTEM_INTEGRITY_DEGRADED | SYSTEM_GAP | FND.OUTCOME.SYSTEM_INTEGRITY_DEGRADED |

### THESIS Mapping

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| DIRECTION_MISMATCH | DEVIATION | FND.THESIS.DIRECTION_MISMATCH |
| EFFECT_NOT_OBSERVED | FAILURE_CANDIDATE | FND.THESIS.EFFECT_NOT_OBSERVED |
| EFFECT_PARTIAL | DEVIATION | FND.THESIS.EFFECT_PARTIAL |
| EFFECT_MAGNITUDE_MISMATCH | DEVIATION | FND.THESIS.EFFECT_MAGNITUDE_MISMATCH |
| EFFECT_SEQUENCE_MISMATCH | DEVIATION | FND.THESIS.EFFECT_SEQUENCE_MISMATCH |
| EFFECT_PERSISTENCE_MISMATCH | DEVIATION | FND.THESIS.EFFECT_PERSISTENCE_MISMATCH |
| EFFECT_HORIZON_MISMATCH | DEVIATION | FND.THESIS.EFFECT_HORIZON_MISMATCH |
| INVALIDATION_RULE_ISSUE | BOUNDARY | FND.THESIS.INVALIDATION_RULE_ISSUE |
| CONTRADICTION_UNDERWEIGHTED | CONTRADICTION | FND.THESIS.CONTRADICTION_UNDERWEIGHTED |
| CONTRADICTION_OVERWEIGHTED | CONTRADICTION | FND.THESIS.CONTRADICTION_OVERWEIGHTED |
| APPLICABILITY_MISMATCH | DEVIATION | FND.THESIS.APPLICABILITY_MISMATCH |
| UNCERTAINTY_UNDERSTATED | ANOMALY | FND.THESIS.UNCERTAINTY_UNDERSTATED |
| UNCERTAINTY_OVERSTATED | ANOMALY | FND.THESIS.UNCERTAINTY_OVERSTATED |
| RISK_COVERAGE_GAP | BOUNDARY | FND.THESIS.RISK_COVERAGE_GAP |

### THESIS_MEMBER Mapping

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| PRIMARY_EFFECT_NOT_OBSERVED | FAILURE_CANDIDATE | FND.THESIS_MEMBER.PRIMARY_EFFECT_NOT_OBSERVED |
| PRIMARY_HORIZON_MISMATCH | DEVIATION | FND.THESIS_MEMBER.PRIMARY_HORIZON_MISMATCH |
| SUPPORT_NOT_INDEPENDENT | ANOMALY | FND.THESIS_MEMBER.SUPPORT_NOT_INDEPENDENT |
| SHARED_EVIDENCE_OVERCOUNT | ANOMALY | FND.THESIS_MEMBER.SHARED_EVIDENCE_OVERCOUNT |
| STRONG_MEMBER_DEPENDENCY | ANOMALY | FND.THESIS_MEMBER.STRONG_MEMBER_DEPENDENCY |
| REDUNDANCY_OVERCOUNT | ANOMALY | FND.THESIS_MEMBER.REDUNDANCY_OVERCOUNT |
| COMMON_CAUSE_OVERCOUNT | ANOMALY | FND.THESIS_MEMBER.COMMON_CAUSE_OVERCOUNT |
| CONDITIONAL_CONTEXT_MISCLASSIFIED | DEVIATION | FND.THESIS_MEMBER.CONDITIONAL_CONTEXT_MISCLASSIFIED |
| CONDITION_BROKEN | BOUNDARY | FND.THESIS_MEMBER.CONDITION_BROKEN |
| CONTRADICTION_UNDERWEIGHTED | CONTRADICTION | FND.THESIS_MEMBER.CONTRADICTION_UNDERWEIGHTED |
| CONTRADICTION_OVERWEIGHTED | CONTRADICTION | FND.THESIS_MEMBER.CONTRADICTION_OVERWEIGHTED |
| MEMBER_MISAPPLIED | DEVIATION | FND.THESIS_MEMBER.MEMBER_MISAPPLIED |
| EVIDENCE_DECAY | QUALITY_GAP | FND.THESIS_MEMBER.EVIDENCE_DECAY |
| ALTERNATIVE_EXPLANATION_UNRESOLVED | CONTRADICTION | FND.THESIS_MEMBER.ALTERNATIVE_EXPLANATION_UNRESOLVED |

### DEFENSE Mapping

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| FALSE_ALLOW_CANDIDATE | SAFETY_GAP | FND.DEFENSE.FALSE_ALLOW_CANDIDATE |
| FALSE_BLOCK_CANDIDATE | SAFETY_GAP | FND.DEFENSE.FALSE_BLOCK_CANDIDATE |
| OVER_RESTRICTION_CANDIDATE | SAFETY_GAP | FND.DEFENSE.OVER_RESTRICTION_CANDIDATE |
| UNDER_RESTRICTION_CANDIDATE | SAFETY_GAP | FND.DEFENSE.UNDER_RESTRICTION_CANDIDATE |
| RISK_STATE_GATE_INEFFECTIVE | SAFETY_GAP | FND.DEFENSE.RISK_STATE_GATE_INEFFECTIVE |
| CONSTRAINT_GATE_INEFFECTIVE | SAFETY_GAP | FND.DEFENSE.CONSTRAINT_GATE_INEFFECTIVE |
| LIQUIDITY_GATE_OVER_SENSITIVE | SAFETY_GAP | FND.DEFENSE.LIQUIDITY_GATE_OVER_SENSITIVE |
| LIQUIDITY_GATE_UNDER_SENSITIVE | SAFETY_GAP | FND.DEFENSE.LIQUIDITY_GATE_UNDER_SENSITIVE |
| EXPOSURE_GATE_TOO_PERMISSIVE | SAFETY_GAP | FND.DEFENSE.EXPOSURE_GATE_TOO_PERMISSIVE |
| DRAWDOWN_GATE_LATE | SAFETY_GAP | FND.DEFENSE.DRAWDOWN_GATE_LATE |
| EXCHANGE_HEALTH_GATE_MISSED | SYSTEM_GAP | FND.DEFENSE.EXCHANGE_HEALTH_GATE_MISSED |
| HARD_SAFETY_BLIND_SPOT | SAFETY_GAP | FND.DEFENSE.HARD_SAFETY_BLIND_SPOT |

### SUPERVISOR Mapping

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| LATE_WARNING | MONITORING_GAP | FND.SUPERVISOR.LATE_WARNING |
| MISSED_WARNING | MONITORING_GAP | FND.SUPERVISOR.MISSED_WARNING |
| FALSE_ALARM_CANDIDATE | MONITORING_GAP | FND.SUPERVISOR.FALSE_ALARM_CANDIDATE |
| OVER_ESCALATION | MONITORING_GAP | FND.SUPERVISOR.OVER_ESCALATION |
| UNDER_ESCALATION | MONITORING_GAP | FND.SUPERVISOR.UNDER_ESCALATION |
| STATE_OSCILLATION | MONITORING_GAP | FND.SUPERVISOR.STATE_OSCILLATION |
| HYSTERESIS_TOO_WEAK_CANDIDATE | MONITORING_GAP | FND.SUPERVISOR.HYSTERESIS_TOO_WEAK_CANDIDATE |
| HYSTERESIS_TOO_STRONG_CANDIDATE | MONITORING_GAP | FND.SUPERVISOR.HYSTERESIS_TOO_STRONG_CANDIDATE |
| RECOVERY_MISSED | MONITORING_GAP | FND.SUPERVISOR.RECOVERY_MISSED |
| FALSE_RECOVERY_CANDIDATE | MONITORING_GAP | FND.SUPERVISOR.FALSE_RECOVERY_CANDIDATE |
| EXPECTED_EFFECT_PROGRESS_MISREAD | MONITORING_GAP | FND.SUPERVISOR.EXPECTED_EFFECT_PROGRESS_MISREAD |
| CONDITIONAL_CONTEXT_MISSED | MONITORING_GAP | FND.SUPERVISOR.CONDITIONAL_CONTEXT_MISSED |
| CONTRADICTION_STRENGTH_MISREAD | MONITORING_GAP | FND.SUPERVISOR.CONTRADICTION_STRENGTH_MISREAD |

### DEMO_LIVE Mapping

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| EXECUTION_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.EXECUTION_DIVERGENCE |
| FILL_RATIO_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.FILL_RATIO_DIVERGENCE |
| PARTIAL_FILL_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.PARTIAL_FILL_DIVERGENCE |
| SLIPPAGE_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.SLIPPAGE_DIVERGENCE |
| FEE_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.FEE_DIVERGENCE |
| FUNDING_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.FUNDING_DIVERGENCE |
| LIQUIDITY_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.LIQUIDITY_DIVERGENCE |
| LATENCY_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.LATENCY_DIVERGENCE |
| REGIME_DIVERGENCE | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.REGIME_DIVERGENCE |
| DATA_QUALITY_DIVERGENCE | QUALITY_GAP | FND.DEMO_LIVE.DATA_QUALITY_DIVERGENCE |
| VENUE_MICROSTRUCTURE_GAP | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.VENUE_MICROSTRUCTURE_GAP |
| POSITION_SCALE_GAP | VALIDATION_DIVERGENCE | FND.DEMO_LIVE.POSITION_SCALE_GAP |
| MEASUREMENT_DEFINITION_MISMATCH | QUALITY_GAP | FND.DEMO_LIVE.MEASUREMENT_DEFINITION_MISMATCH |
| SIMULATION_ASSUMPTION_GAP | MODEL_GAP | FND.DEMO_LIVE.SIMULATION_ASSUMPTION_GAP |
| COMPARABILITY_GAP | QUALITY_GAP | FND.DEMO_LIVE.COMPARABILITY_GAP |

### COUNTERFACTUAL Mapping

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| DEFENSE_POLICY_ALTERNATIVE | OPPORTUNITY | FND.COUNTERFACTUAL.DEFENSE_POLICY_ALTERNATIVE |
| SUPERVISOR_ACTION_ALTERNATIVE | OPPORTUNITY | FND.COUNTERFACTUAL.SUPERVISOR_ACTION_ALTERNATIVE |
| EXIT_TIMING_ALTERNATIVE | OPPORTUNITY | FND.COUNTERFACTUAL.EXIT_TIMING_ALTERNATIVE |
| POSITION_SIZE_ALTERNATIVE | OPPORTUNITY | FND.COUNTERFACTUAL.POSITION_SIZE_ALTERNATIVE |
| ORDER_STYLE_ALTERNATIVE | OPPORTUNITY | FND.COUNTERFACTUAL.ORDER_STYLE_ALTERNATIVE |
| RISK_POLICY_ALTERNATIVE | OPPORTUNITY | FND.COUNTERFACTUAL.RISK_POLICY_ALTERNATIVE |
| MATERIAL_IMPROVEMENT_CANDIDATE | OPPORTUNITY | FND.COUNTERFACTUAL.MATERIAL_IMPROVEMENT_CANDIDATE |
| MATERIAL_RISK_REDUCTION_CANDIDATE | OPPORTUNITY | FND.COUNTERFACTUAL.MATERIAL_RISK_REDUCTION_CANDIDATE |
| MATERIAL_RISK_INCREASE_CANDIDATE | DEVIATION | FND.COUNTERFACTUAL.MATERIAL_RISK_INCREASE_CANDIDATE |
| MODEL_UNCERTAINTY_HIGH | MODEL_GAP | FND.COUNTERFACTUAL.MODEL_UNCERTAINTY_HIGH |
| FEASIBILITY_LIMITATION | BOUNDARY | FND.COUNTERFACTUAL.FEASIBILITY_LIMITATION |
| HINDSIGHT_LEAKAGE_RISK | QUALITY_GAP | FND.COUNTERFACTUAL.HINDSIGHT_LEAKAGE_RISK |

### CROSS_ANALYSIS Mapping

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| ANALYSIS_CONFLICT | ANALYSIS_CONFLICT | FND.CROSS_ANALYSIS.ANALYSIS_CONFLICT |
| SHARED_ORIGIN_OVERCOUNT_RISK | ANOMALY | FND.CROSS_ANALYSIS.SHARED_ORIGIN_OVERCOUNT_RISK |
| TRACE_GAP | QUALITY_GAP | FND.CROSS_ANALYSIS.TRACE_GAP |
| VERSION_MISMATCH | QUALITY_GAP | FND.CROSS_ANALYSIS.VERSION_MISMATCH |
| RESPONSIBILITY_AMBIGUITY | ANALYSIS_CONFLICT | FND.CROSS_ANALYSIS.RESPONSIBILITY_AMBIGUITY |

### Standard Statement Rules

Statementは原則、

~~~text
Subject
+
Observed State
+
Reference / Expected State if needed
+
Material Difference
+
Context
+
Uncertainty qualifier when needed
~~~

Structured FieldsがSemantic Sourceであり、StatementはHuman-readable Projection。

### Candidate Semantics Preservation

以下の_CANDIDATEを確定表現へ変えない。

~~~text
FALSE_ALLOW_CANDIDATE
FALSE_BLOCK_CANDIDATE
OVER_RESTRICTION_CANDIDATE
UNDER_RESTRICTION_CANDIDATE
FALSE_ALARM_CANDIDATE
HYSTERESIS_TOO_WEAK_CANDIDATE
HYSTERESIS_TOO_STRONG_CANDIDATE
FALSE_RECOVERY_CANDIDATE
MATERIAL_IMPROVEMENT_CANDIDATE
MATERIAL_RISK_REDUCTION_CANDIDATE
MATERIAL_RISK_INCREASE_CANDIDATE
~~~

### Registry Record Candidate

~~~text
finding_code
domain
class
canonical_label
meaning
allowed_source_analysis
allowed_raw_finding_kinds
required_context
allowed_subject_types
statement_template_ref
taxonomy_version
status
replacement_code
~~~

Registry Status候補:

~~~text
ACTIVE
DEPRECATED
RESERVED
REMOVED
~~~

Historical Findingを無言でMigrationしない。

### Status

~~~text
SOURCE_STATUS:
CURRENT_DERIVED

LEGACY_CONFLICT_STATUS:
NONE

CURRENT_03_CONFLICT_STATUS:
NONE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.54 Analysis → ResearchCandidate / Candidate Promotion Contract

### Formal Definition Candidate

> **Candidate Promotion = Canonical Findingについて、そのFindingが研究可能な問題として最低限のIdentity・Trace・Contextを持ち、Research IntakeへResearchCandidateとして提示するだけのResearch Value Signalがあるかを評価する境界責任候補。Research採用そのものは決定しない。**

### Input

~~~text
Canonical Finding
Related Canonical Findings
Source Trace
Market Context / DNA
Quality / Uncertainty
Shared Origin / Dependency
Existing Research relation hints
~~~

### Eligibility Axes

~~~text
Finding Clarity
Traceability
Researchability
Finding Significance Context
Recurrence / Pattern
Novelty / Unknown
Contradiction
Production Relevance
Risk / Safety Relevance
Evidence / Quality Sufficiency
Uncertainty
Possible Existing Research Relation
~~~

重要:

~~~text
Promotion
≠ Final Research Value Decision

Promotion
≠ Research Admission
~~~

### Promotion Decisions

~~~text
CREATE_CANDIDATE
ACCUMULATE
RECORD_ONLY
NEED_MORE_CONTEXT
~~~

Meaning:

~~~text
CREATE_CANDIDATE
= Research IntakeへResearchCandidateとして提示可能

ACCUMULATE
= 単独Candidate化はまだ弱いがPattern蓄積対象

RECORD_ONLY
= Analysis / Finding historyとして保存しCandidate化しない

NEED_MORE_CONTEXT
= Candidate形成に必要なContext不足
~~~

REJECTはResearch Intakeの責任なのでCandidate Promotionでは使わない。

### Minimum Candidate Formation

概念上最低限:

~~~text
Finding identifiable
+
Source Trace sufficient
+
Research Question Seedを作れる

AND

少なくとも一つのPromotion Basis:
- MATERIAL_ANOMALY
- REPEATED_PATTERN
- NOVEL_BEHAVIOR
- CONTRADICTION
- BOUNDARY_DISCOVERY
- PRODUCTION_RELEVANCE
- RISK_RELEVANCE
- VALIDATION_DIVERGENCE
- MODEL_GAP
- EXPLANATORY_GAP
- OPPORTUNITY_CANDIDATE
- UNKNOWN_STRUCTURE
~~~

全部をAND必須にはしない。

重大な単発Safety / Unknown Failureを逃さないため。

### Atomic Finding → Research Problem Aggregation

FindingはAtomic。

ResearchCandidateはResearch Problem単位。

~~~text
Atomic Findings
↓
Shared Origin / Dependency Review
↓
Candidate Aggregation
↓
One Research Problem Candidate
~~~

例:

~~~text
FND.OUTCOME.UNEXPECTED_FAILURE
+
FND.DEMO_LIVE.SLIPPAGE_DIVERGENCE
+
FND.DEMO_LIVE.PARTIAL_FILL_DIVERGENCE
↓
one candidate:
Comparable LIVE conditionsでExecution Realityが
Reference assumptionをMaterialに下回る可能性
~~~

### Duplicate Boundary

Candidate Promotionは、

~~~text
possible_duplicate_refs
related_research_refs
~~~

を付けられる。

正式MERGEはResearch Intake責任。

### Counterfactual Promotion Strictness

~~~text
Alternative Outcome > Actual
≠ Automatic Candidate
~~~

最低候補:

~~~text
Decision-time information fixed
Predefined / explicit alternative
Feasibility acceptable
No obvious hindsight leakage
Model quality suitable
Difference material
Uncertainty preserved
~~~

### Positive Discovery

Failureだけでなく、

~~~text
Unexpected Success
New Stable Pattern
New Applicability Region
Potential Edge Strengthening
~~~

もCandidate Sourceになり得る。

### ResearchCandidate Conceptual Structure

~~~text
ResearchCandidate
├ identity
├ origin_finding_refs
├ finding_statement
├ candidate_type
├ promotion_basis
├ research_question_seed
├ materiality / recurrence / novelty context
├ production / risk relevance
├ market context / DNA
├ evidence / quality / uncertainty
├ shared-origin / dependency
├ related research / hypothesis / knowledge hints
└ limitations
~~~

### Invariants

~~~text
Finding
≠ ResearchCandidate

CREATE_CANDIDATE
≠ Intake ACCEPT

Trade Loss
≠ Automatic Candidate

Trade Profit
≠ No Candidate

Repeated Trades
≠ Independent Cases

Multiple Findings
≠ Independent Evidence

Counterfactual Better
≠ Automatic Candidate

Candidate Promotion
must not set Root Cause

Candidate Promotion
must not set Research Priority

Candidate Promotion
must not change Production
~~~

### Status

~~~text
SOURCE_STATUS:
CURRENT_DERIVED + 03_RESEARCH BOUNDARY

CURRENT_03_CONFLICT_STATUS:
NONE after admission separation

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.55 Research Router / ResearchRoute

### Research Router — Formal Definition Candidate

> **Research Router = Research Intakeで受理されたResearch Candidateについて、その原因を確定せず、Origin・Finding Type・Affected Responsibility・Evidence / Contextを基に、一つ以上の適切なResearch Domainを選び、その理由・Basis・UncertaintyをResearchRouteへ固定するResearch Ingress Domain Routing Responsibility候補。**

### ResearchRoute — Formal Definition Candidate

> **ResearchRoute = 一つのAccepted Research CandidateをどのResearch Domainへなぜ送ると判断したかを、Route Target・Reason・Basis・Uncertainty・Routing Policy Version・Trace付きで固定するVersioned Immutable Routing Decision Object候補。Research Plan・Root Cause・Final Priority・Research Resultではない。**

### Input Boundary

~~~text
Research Intake
↓
ACCEPTED ResearchCandidate
↓
Research Router
~~~

RouterはRaw Finding / Raw Analysisを直接受け取らない。

### Two-Stage Routing

~~~text
Stage 1:
Research Router
= Domain Routing

Stage 2:
03_RESEARCH Routing / Prioritization
= Method / Validation Routing + Research scheduling priority
~~~

### Domain Candidate Registry

Legacy Source-backed中心:

~~~text
Data Quality Research
Event Detection Research
Formula Research
Feature Research
Market Intelligence Research
Causal Research
Hypothesis Set / Thesis Composition Research
Market DNA Research
Execution Research
Live Evidence Research
Supervisor Research
~~~

Current Derived追加候補:

~~~text
Applicability Research
Defense / Risk Research
Exit / Position Research
Demo / Simulation Model Research
Counterfactual Model Research
Research Structure / Evidence Dependency Research
~~~

正式ResearchDomainRegistryは後続。

### Multi-Route

1 Candidateから複数Domainを許容する。

~~~text
PRIMARY
SECONDARY
CROSS_CUTTING
DEPENDENCY
~~~

はRoute Role候補。

Multi-routeは複数Causeが証明されたことを意味しない。

### Routing Status

~~~text
COMPLETED
AMBIGUOUS
NEED_MORE_CONTEXT
UNROUTABLE
ROUTING_FAILED
~~~

Meaning:

~~~text
AMBIGUOUS
= 複数Domainが妥当で一意化不要 / 不可能

NEED_MORE_CONTEXT
= Routing Context不足

UNROUTABLE
= 現行Domain Registryに適切なOwnerがない

ROUTING_FAILED
= Router処理障害
~~~

### Priority Boundary

Legacy ResearchRouteのpriorityはCurrent 03 PrioritizationとAuthority衝突する。

Routerでは以下へ弱める。

~~~text
urgency_hint
production_impact_hint
risk_relevance_hint
~~~

Final Priorityは03_RESEARCH Prioritization責任。

### ResearchRoute Conceptual Structure

~~~text
ResearchRoute
├ research_route_id
├ research_candidate_ref
├ routing_version
├ routed_at
├ trace_id
├ routing_status
├ route_targets[]
│  ├ target_research_domain
│  ├ route_role
│  ├ reason_codes
│  ├ basis_refs
│  └ target_specific_uncertainty
├ dependency_refs
├ related_research_refs
├ market_context_refs
├ market_dna_refs
├ urgency_hint
├ production_impact_hint
├ risk_relevance_hint
├ routing_policy_ref
├ routing_policy_version
├ routing_uncertainty
├ limitations
└ diagnostics_ref
~~~

### Immutable / Re-route

新ContextでRouteが変わる場合、旧Routeを無言で書き換えない。

~~~text
ResearchRoute v1
↓
New Context
↓
ResearchRoute v2
or
superseding route
~~~

### Invariants

~~~text
ResearchCandidate
≠ ResearchRoute

ResearchRoute
≠ ResearchPlan

Routing
≠ Root Cause

Routing
≠ Final Priority

Routing
≠ Validation Method execution

Target Domain
≠ Cause Confirmed

Multiple Routes
≠ Multiple Causes Proven

ResearchRoute created
≠ Research started

AI suggestion
≠ Routing Authority

Router
must not directly change Production
~~~

### Legacy Review

~~~text
LEGACY_SOURCE_RELATION:
ROLE-RTR-001 Research Router
OBJ-POST-008 ResearchRoute

LEGACY_CONFLICT_STATUS:
MODERATE RESPONSIBILITY OVERLAP
resolved by two-stage routing separation

LEGACY_REVIEW_STATUS:
STRONGLY ADOPTABLE / RESPONSIBILITY REFINEMENT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---

## 7.56 Finding → Research — Integrated Candidate Flow

### Canonical Detailed Flow

~~~text
Trade / Position Terminal
↓
Post-Trade Analysis

├ OutcomeAnalysisResult
├ TradeThesisEvaluation
├ HypothesisAttribution / ThesisMemberAttribution
├ DefenseDecisionEvaluation
├ SupervisorEvaluation
├ DemoLiveDivergence
└ CounterfactualResult

↓
Finding Extractor
↓
Common Extraction Gates
↓
0..N ExtractedFindingDraft

↓
Finding Normalizer
↓
Finding Type Registry v1.0
↓
Canonical Finding

↓
Cross-Analysis Review
├ ANALYSIS_CONFLICT
├ SHARED_ORIGIN_OVERCOUNT_RISK
├ TRACE_GAP
├ VERSION_MISMATCH
└ RESPONSIBILITY_AMBIGUITY

↓
Canonical Finding Set
↓
Candidate Promotion

├ CREATE_CANDIDATE
├ ACCUMULATE
├ RECORD_ONLY
└ NEED_MORE_CONTEXT

↓ when CREATE_CANDIDATE
ResearchCandidate
↓
Research Intake

├ ACCEPT
├ DEFER
├ MERGE
├ REJECT
└ NEED_MORE_CONTEXT

↓ only ACCEPT
Research Router
↓
ResearchRoute / Domain Routing

↓
03_RESEARCH Routing / Prioritization
↓
Research Plan
↓
Research Question / Hypothesis
↓
Validation Channels
↓
Research Result
↓
Validation Gate
↓
Validated Research Result
↓
04_KNOWLEDGE_APPLICABILITY
~~~

### No Direct Bypass

禁止候補:

~~~text
Analysis
→ Router

Analysis
→ Stress Lab

Finding
→ Hypothesis

Finding
→ Trainer

Canonical Finding
→ Production Rule

ResearchCandidate
→ Historical Test directly

ResearchRoute
→ Live change
~~~

### Authority Matrix

| Stage | Owns | Does Not Own |
|---|---|---|
| Post-Trade Analysis | Meaning analysis | Finding taxonomy / Research admission |
| Finding Extractor | Finding existence / semantic extraction | Canonical naming / Research value |
| Finding Normalizer | Canonical representation | New analysis / promotion |
| Finding Registry | Allowed vocabulary | Detection / Research routing |
| Candidate Promotion | Candidate formation | Research admission / formal merge |
| Research Intake | Admission / defer / merge / reject | Root cause / validation result |
| Research Router | Research Domain routing | Method execution / final priority |
| 03 Routing / Prioritization | Research method mix / priority | Research result |
| Research Plan | Executable validation plan | Knowledge promotion |

### Pipeline Failure Separation

~~~text
Analysis INDETERMINATE
≠ Finding NO_FINDING

Extractor NEED_MORE_CONTEXT
≠ Normalizer UNMAPPABLE

Normalizer UNMAPPABLE
≠ UNKNOWN_STRUCTURE

Candidate RECORD_ONLY
≠ Intake REJECT

Intake DEFER
≠ Router UNROUTABLE

Router ROUTING_FAILED
≠ Research Result failure
~~~

### Final Invariants

~~~text
Analysis Result
≠ Finding

Finding
≠ ResearchCandidate

ResearchCandidate
≠ Accepted Research

ResearchRoute
≠ ResearchPlan

Finding Code
≠ Root Cause

Finding Domain
≠ Research Domain

Finding Count
≠ Evidence Count

Route Count
≠ Cause Count

Finding Standardization
≠ Confidence Upgrade

Promotion
≠ Admission

Routing
≠ Validation

Post-Trade Feedback
must return through Research Governance
before Knowledge / Production changes
~~~

### Integrated Review Status

> **Finding Extractor → Normalizer → Registry → Candidate Promotion → Research Intake → Research Routerの責任境界は、03_RESEARCHと既存Post-Trade Referenceへ接続可能な形で整合した。最大の重複であったMateriality / Admission判断、Duplicate Merge、Research Routingの二重Authorityは分離された。Current Design本体へはまだAdoptしていない。**

~~~text
SOURCE_STATUS:
MIXED
- 03_RESEARCH source-backed boundaries
- Legacy Research Router / ResearchRoute reuse
- Finding pipeline detailed semantics are Current Derived

LEGACY_CONFLICT_STATUS:
MINOR / MODERATE responsibility overlap resolved

CURRENT_03_CONFLICT_STATUS:
NONE after corrections

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

---


---

## 7.57 Unsaved Detailed Design — Intermediate Checkpoint / Cross-Review

### Checkpoint Purpose

This section consolidates the detailed design work created after 7.56 and before completion of 05_DECISION.

It is an intermediate Reference checkpoint only.

~~~text
REVIEW_STAGE:
INTERMEDIATE_CHECKPOINT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED

PRODUCTION_STATUS:
NOT_A_PRODUCTION_SPEC

CURRENT_ADOPTION:
REQUIRES_SEPARATE_REVIEW
~~~

The checkpoint covers:

~~~text
Research Intake
Research Domain Registry
Research Method Registry
Research Method Routing
Research Plan
Plan Validation Gate
Research Execution
Research Result Synthesis
Result Validation Gate
Knowledge Admission / Promotion
Knowledge Type Registry
Knowledge Record Common Contract
Knowledge Relationship Registry / Contract
Knowledge Relationship Integrity Gate
Knowledge Lifecycle / Aging Governance
Applicability Evaluation
Applicable Knowledge Set
Decision Context Assembly
Knowledge Integration
Trade Thesis Construction
Decision Scope Binding
~~~

The following are intentionally NOT completed in this checkpoint:

~~~text
Individual Thesis Evaluation
Expected Value Assessment
Cross-Thesis Comparison
Decision Result Finalization / Integrity
Decision Result
05 → Defense Handoff
05_DECISION Final Integrated Review
~~~

### Cross-Review Result

No architecture-breaking contradiction was found.

The reviewed flow remains connectable as:

~~~text
Finding / Candidate
↓
Research Intake
↓
Research Domain Routing
↓
Research Method Routing
↓
Research Plan
↓
Plan Validation
↓
Research Trial / ResearchResult
↓
Research Synthesis
↓
Result Validation
↓
Knowledge Admission / Promotion
↓
Knowledge Record / Relationship / Lifecycle
↓
Runtime Applicability
↓
Applicable Knowledge Set
↓
Decision Context
↓
Knowledge Integration
↓
Trade Thesis 0..N
↓
Decision Scope Binding
↓
[05 remaining evaluation chain]
~~~

### Corrections Applied Before Checkpoint

#### CHECKPOINT-CORRECTION-01 — ResearchPlan Lifecycle vs Plan Validation

Earlier draft language allowed VALIDATED to appear as a ResearchPlan lifecycle state.

That is rejected.

Legacy FIX-011 remains authoritative for the plan state separation:

~~~text
ResearchPlan Lifecycle:
DRAFT
READY
ACTIVE
COMPLETED
SUPERSEDED
CANCELLED

ResearchPlan Lock:
EDITABLE
PRE_REGISTERED
FROZEN

Plan Validation:
separate PlanValidationResult
~~~

Therefore:

~~~text
PlanValidation READY
≠ ResearchPlan lifecycle VALIDATED
~~~

No new VALIDATED lifecycle state is introduced.

#### CHECKPOINT-CORRECTION-02 — Knowledge Type Naming

The earlier candidate primary family:

~~~text
KT.RELATIONSHIP
~~~

is renamed in this checkpoint to:

~~~text
KT.MARKET_RELATIONSHIP
~~~

Reason:

~~~text
KT.MARKET_RELATIONSHIP
= reusable market relationship / pattern / mechanism Knowledge

KnowledgeRelationship
= canonical graph edge between Knowledge Objects
~~~

This avoids type/object name collision.

#### CHECKPOINT-CORRECTION-03 — Relationship Integrity Idempotency

Existing exact or reverse-equivalent symmetric edge is not automatically a semantic integrity failure.

Relationship Integrity outcomes therefore include:

~~~text
WRITE_ALLOWED
WRITE_ALLOWED_WITH_LIMITATIONS
NO_WRITE_REQUIRED
NEEDS_CORRECTION
BLOCKED
INTEGRITY_GATE_FAILED
~~~

Examples:

~~~text
exact edge already exists
→ NO_WRITE_REQUIRED

A CONTRADICTS B exists
candidate B CONTRADICTS A
→ NO_WRITE_REQUIRED with existing relationship ref

SUPERSEDES cycle
→ BLOCKED
~~~

#### CHECKPOINT-CORRECTION-04 — Validated Research Result Boundary

Do not create another full duplicate result object.

Canonical research-level objects remain:

~~~text
ResearchResult
= trial-level result

ResearchSynthesisAssessment
= research-question-level synthesis

ResultValidationDecision
= post-synthesis validation decision
~~~

The downstream expression:

~~~text
Validated Research Result
~~~

is treated as a logical qualified boundary/view:

~~~text
ResearchSynthesisAssessmentRef
+
ResultValidationDecisionRef
~~~

not as a copied evidence/result database.

#### CHECKPOINT-CORRECTION-05 — Contradiction vs Applicability

Current 04 has a minor semantic tension:

~~~text
APPLICABLE description
mentions absence of major contradiction

while later sections allow
multiple contradictory Knowledge
to be simultaneously Applicable
and passed to 05.
~~~

Detailed resolution:

~~~text
Contradiction exists
≠ automatically NOT_APPLICABLE

Contradiction that prevents responsible
applicability determination
→ UNCERTAIN candidate

Both Knowledge can remain APPLICABLE
when each independently matches current conditions,
with contradiction context preserved for 05.
~~~

04 does not resolve the conflict winner.

#### CHECKPOINT-CORRECTION-06 — Common Knowledge Contract Is Not a Duplicate Wrapper

~~~text
Knowledge Record Common Contract
= logical interface / semantic contract
~~~

It does NOT require duplicate physical storage for specialized canonical objects.

Examples:

~~~text
FeatureKnowledge
FormulaKnowledge
Failure
FailureBoundary
Constraint
NegativeKnowledge specialization
~~~

remain specialized canonical objects while satisfying the common Knowledge contract where applicable.

#### CHECKPOINT-CORRECTION-07 — Decision Scope Specification vs Binding

~~~text
Decision Scope Specification
= pre-Thesis requested decision domain

Decision Scope Binding
= post-Thesis comparison-group binding
~~~

They are separate responsibilities.

#### CHECKPOINT-CORRECTION-08 — Scope Does Not Contain Direction / EV

The following MUST NOT define Decision Scope identity:

~~~text
Expected Direction
Mechanism
Expected Value
Evidence Strength
Thesis Quality
Trade-worthiness
~~~

Otherwise opposing Long/Short theses could not be compared inside one scope.

#### CHECKPOINT-CORRECTION-09 — Common Cause Is Not Causal Proof

Knowledge Integration may create:

~~~text
CommonCauseGroup
Common Cause Candidate
Shared Event Group
~~~

but:

~~~text
Common Cause Candidate
≠ causal proof
~~~

Any new causal claim must return through Research.

---

## 7.58 Research Intake — Formal Contract Checkpoint

### Responsibility

~~~text
Candidate Promotion
↓
ResearchCandidate
↓
Research Intake
↓
ACCEPT only
↓
Research Router
~~~

Research Intake is the formal admission boundary.

It answers:

> Is this candidate sufficiently identified, traceable, researchable and valuable to enter the formal research system now?

It does NOT answer:

~~~text
What is the root cause?
Which method proves it?
Which domain is the cause?
What is the final research priority?
Is the hypothesis true?
~~~

### Intake Gates

~~~text
I0 Identity
I1 Origin / Trace
I2 Minimum Context
I3 Researchability
I4 Duplicate / Merge
I5 Existing Research / Hypothesis / Knowledge relation
I6 Evidence / Quality / Uncertainty sufficiency for admission
I7 Research Value
I8 Production / Risk relevance
I9 Admission Conflict / Dependency
I10 Final Admission Decision
~~~

### Intake Outcomes

~~~text
ACCEPT
DEFER
MERGE
REJECT
NEED_MORE_CONTEXT
~~~

Meaning:

~~~text
ACCEPT
= formally admitted
≠ research started
≠ high priority
≠ true

DEFER
= worthwhile but not now

MERGE
= same central research problem;
  preserve origin history

REJECT
= not admissible under current rules
≠ Finding false

NEED_MORE_CONTEXT
= admission cannot responsibly be decided
~~~

### Output Candidate

~~~text
ResearchIntakeDecision
- candidate ref
- intake policy version
- decision
- reason codes
- duplicate / merge refs
- related research refs
- missing context
- production / risk relevance
- uncertainty
- evaluated_at
- trace
~~~

Decision history is immutable. Re-evaluation creates a new decision/version rather than deleting the previous admission history.

### Current 03 Compatibility

Current 03 already contains:

~~~text
ACCEPT
DEFER
MERGE
REJECT
NEED_MORE_CONTEXT
~~~

and the same admission responsibilities.

No material conflict found.

---

## 7.59 Research Domain Registry v1.0 — Checkpoint

### Purpose

Research Domain answers:

> WHERE / WHO owns the research problem?

It does NOT answer:

~~~text
how to test it
which evidence channel to use
which cause is true
what priority it has
~~~

### Two-Stage Routing

~~~text
Research Intake ACCEPT
↓
Research Router
↓
Research Domain Registry
↓
ResearchRoute
= WHERE / WHO

↓
03 Research Routing / Prioritization
↓
Method / Validation Routing
= HOW
~~~

### Canonical Domain IDs

Legacy-backed core:

~~~text
RD.DATA_QUALITY
RD.EVENT_DETECTION
RD.FORMULA
RD.FEATURE
RD.MARKET_INTELLIGENCE
RD.CAUSAL
RD.THESIS_COMPOSITION
RD.MARKET_DNA
RD.SUPERVISOR
RD.EXECUTION
RD.LIVE_EVIDENCE
~~~

Current-derived additions:

~~~text
RD.APPLICABILITY
RD.DEFENSE_RISK
RD.EXIT_POSITION
RD.DEMO_SIMULATION_MODEL
RD.COUNTERFACTUAL_MODEL
RD.RESEARCH_STRUCTURE
~~~

### Boundary Notes

~~~text
RD.DATA_QUALITY
= can the data be trusted?

RD.EVENT_DETECTION
= what event occurred?

RD.FORMULA
= is the calculation / formula valid?

RD.FEATURE
= is the representation useful / stable?

RD.MARKET_INTELLIGENCE
= what is happening?

RD.CAUSAL
= why might it happen?

RD.THESIS_COMPOSITION
= how knowledge/evidence is composed into production reasoning

RD.MARKET_DNA
= how market state is represented / compared

RD.APPLICABILITY
= where knowledge is usable

RD.DEFENSE_RISK
= safety-gate / risk-governance research

RD.SUPERVISOR
= post-entry thesis-health detection research

RD.EXECUTION
= live order / fill / venue mechanics

RD.LIVE_EVIDENCE
= research usability and integrity of live evidence

RD.EXIT_POSITION
= position / exit lifecycle research

RD.DEMO_SIMULATION_MODEL
= simulation-to-reality model research

RD.COUNTERFACTUAL_MODEL
= alternative-action model validity

RD.RESEARCH_STRUCTURE
= evidence dependency / research-system meta structure
~~~

Important:

~~~text
UNROUTABLE
≠ RD.RESEARCH_STRUCTURE
~~~

If the registry has no responsible domain, preserve UNROUTABLE rather than hiding vocabulary gaps.

### Route Roles

~~~text
PRIMARY
SECONDARY
DEPENDENCY
CROSS_CUTTING
~~~

Multiple routes do not prove multiple causes.

### Registry Lifecycle

~~~text
ACTIVE
DEPRECATED
RESERVED
REMOVED
~~~

No silent migration of historical routes.

### Current 03 Reconciliation Note

Current 03 uses the broad phrase Routing / Prioritization.

Future Current adoption must explicitly rename or document:

~~~text
Research Router
= domain routing

03 Routing / Prioritization
= method / validation routing + scheduling priority
~~~

This is a terminology reconciliation, not an architecture conflict.

---

## 7.60 Research Method Registry v1.0 — Checkpoint

### Purpose

Research Method answers:

> HOW will this research question be studied?

Method is separate from Evidence Channel and Experiment Mode.

### Method Families and IDs

~~~text
INFERENCE
- RM.CAUSAL_RESEARCH
- RM.EMPIRICAL_RESEARCH

COMPARISON
- RM.CASE_COMPARISON
- RM.MARKET_DNA_COMPARISON

VALIDATION
- RM.HISTORICAL_VALIDATION
- RM.OOS_VALIDATION
- RM.FORWARD_VALIDATION

ROBUSTNESS
- RM.STRESS_TEST
- RM.REGIME_STABILITY

DIAGNOSTIC_REFUTATION
- RM.FAILURE_ANALYSIS
- RM.CONTRADICTION_ANALYSIS
- RM.ALTERNATIVE_HYPOTHESIS
~~~

### Evidence Channels Remain Separate

Current 03 channels:

~~~text
RUNTIME_OBSERVATIONAL
HISTORICAL
OOS
FORWARD
STRESS
PRODUCTION_LIVE
~~~

Invariants:

~~~text
Method
≠ Evidence Channel

Method
≠ Experiment Mode

different methods
≠ independent evidence

Process Failure
≠ Hypothesis failure
~~~

### Core Method Semantics

~~~text
CAUSAL_RESEARCH
= temporal / lag / confounder / mechanism reasoning
  correlation ≠ cause

EMPIRICAL_RESEARCH
= reproducible conditional relationship
  pattern ≠ cause

CASE_COMPARISON
= compare case structure
  similarity ≠ same cause/outcome

MARKET_DNA_COMPARISON
= compare fixed DNA definition/axes
  similarity ≠ applicability proof

HISTORICAL_VALIDATION
= historical reproduction
  success ≠ future guarantee

OOS_VALIDATION
= untouched holdout
  do not tune on OOS

FORWARD_VALIDATION
= T0-frozen future-only evaluation
  no hindsight rewrite

STRESS_TEST
= predefined stress / failure criteria
  survival ≠ absolute safety

REGIME_STABILITY
= behavior across explicit regimes
  coverage required

FAILURE_ANALYSIS
= expected vs observed failure structure
  loss ≠ failure/root cause

CONTRADICTION_ANALYSIS
= actively examine contradicting evidence
  no contradiction ≠ proof

ALTERNATIVE_HYPOTHESIS
= generate / compare competing explanations
  alternative hypothesis ≠ evidence
~~~

---

## 7.61 Research Method Routing Contract — Checkpoint

### Position

~~~text
Accepted Research Candidate
↓
ResearchRoute / Domain
↓
Research Method Routing
↓
ResearchMethodSelection
↓
Research Plan
~~~

### Routing Gates

~~~text
MR0 Input Integrity
MR1 Research Intent
MR2 Domain / Method Compatibility
MR3 Prerequisite
MR4 Evidence / Data Availability
MR5 PRIMARY Method selection
MR6 Validation Coverage
MR7 Refutation Coverage
MR8 Robustness / Boundary Coverage
MR9 Diagnostic Need
MR10 Dependency / Leakage / Redundancy
MR11 Feasibility / Cost / Urgency Context
MR12 Role Assignment
MR13 Method Set Integrity
~~~

### Research Intent Candidates

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
~~~

### Method Roles

Target-relative:

~~~text
PRIMARY
SUPPORTING
VALIDATION
REFUTATION
ROBUSTNESS
DIAGNOSTIC
~~~

### Eligibility

~~~text
SELECTED
SELECTED_CONDITIONAL
RECOMMENDED_NOT_READY
NOT_SELECTED
BLOCKED_PREREQUISITE
UNAVAILABLE_EVIDENCE
NOT_APPLICABLE
~~~

### Overall Routing Status

~~~text
ROUTED
ROUTED_WITH_LIMITATIONS
NEED_MORE_CONTEXT
METHOD_SET_AMBIGUOUS
NO_FEASIBLE_METHOD
ROUTING_FAILED
~~~

Considered-but-not-selected methods remain auditable.

Do not select all methods by default.

Causal claims must at least consider meaningful refutation / alternative-explanation coverage according to research maturity.

Safety-critical / production-relevant research should strongly consider robustness / failure-boundary coverage.

---

## 7.62 Research Plan / Plan Validation — Checkpoint

### ResearchPlan Responsibility

~~~text
ResearchMethodSelection
↓
ResearchPlan
~~~

A ResearchPlan converts a method selection into a reproducible execution specification.

One plan normally represents one central Research Question.

### Plan Structure

~~~text
Identity
Research Target
Research Question
Hypothesis / Claim Set
Frozen Context
Method Work Items
Evidence Plan
Data Plan
Comparison Plan
Evaluation Plan
Refutation Plan
Robustness Plan
Dependency Plan
Integrity / Leakage Controls
Execution Preconditions
Version / Governance
~~~

### Frozen References

Where material, freeze:

~~~text
target version
formula version
feature version
Market DNA definition version
method registry version
data schema version
evaluation rule version
model version
~~~

### Dataset Roles

~~~text
DEVELOPMENT
IN_SAMPLE
HISTORICAL_VALIDATION
OOS
FORWARD
STRESS_INPUT
LIVE_REFERENCE
~~~

Core leakage rules:

~~~text
development ≠ OOS

pre-T0 inputs
≠ post-T0 outcome knowledge

future outcome
must not enter decision-time input
~~~

### MethodWorkItem Candidate

~~~text
method_id
method_role
research question
prerequisites
inputs
evidence channel
procedure
metrics
comparison
evaluation rules
refutation rules
process-failure rules
dependencies
limitations
~~~

### Process vs Research Outcome

~~~text
Research process succeeded
≠ hypothesis supported

Research process failed
≠ hypothesis refuted
~~~

### ResearchPlan State Correction

Canonical state separation remains Legacy FIX-011:

~~~text
Lifecycle:
DRAFT / READY / ACTIVE / COMPLETED / SUPERSEDED / CANCELLED

Lock:
EDITABLE / PRE_REGISTERED / FROZEN
~~~

Do not add VALIDATED as a Plan Lifecycle state.

### Plan Validation Gate

Pre-research gate:

~~~text
PV0 Identity
PV1 Trace / Lineage
PV2 Question / Scope
PV3 Target / Version Freeze
PV4 Method Selection Integrity
PV5 Method Prerequisites
PV6 Data / Dataset Role
PV7 Temporal Boundary / Leakage
PV8 Comparison / Baseline
PV9 Metric / Evaluation
PV10 Refutation / Alternative
PV11 Failure / Inconclusive
PV12 Dependency / Independence
PV13 Execution Feasibility
PV14 Reproducibility / Auditability
~~~

Outcomes:

~~~text
READY
READY_WITH_LIMITATIONS
NEED_REVISION
BLOCKED
PLAN_VALIDATION_FAILED
~~~

Per-gate candidate status:

~~~text
PASS
PASS_WITH_LIMITATION
FAIL
BLOCKED_DEPENDENCY
NOT_APPLICABLE
UNKNOWN
~~~

Severity:

~~~text
HARD
CONDITIONAL
ADVISORY
~~~

A HARD failure is not majority-voted away.

UNKNOWN critical leakage condition should fail closed.

Output candidate:

~~~text
PlanValidationResult
~~~

The validator does not silently rewrite the plan.

Execution must bind the exact validated Plan Version.

---

## 7.63 Research Execution Contract — Checkpoint

### Position

~~~text
ResearchPlan
+
PlanValidationResult READY
↓
Research Execution
↓
ResearchTrial 1..N
↓
ResearchResult 1..N
~~~

### Legacy Objects Preserved

~~~text
OBJ-RSCH-002 ResearchPlan
OBJ-RSCH-003 ResearchTrial
OBJ-RSCH-004 ResearchResult
OBJ-RSCH-008 ResearchBudget
~~~

### Method / Mode / Channel Separation

~~~text
Research Method
≠ Experiment Mode
≠ Evidence Source Channel
~~~

Experiment Mode candidates:

~~~text
RANDOM_BASELINE
HISTORICAL
REPLAY
PAPER
DEMO_FORWARD
SHADOW
COUNTERFACTUAL
STRESS
~~~

STRESS is a current candidate extension; specialist StressResult may coexist with canonical ResearchResult.

### Trial Binding

Each Trial binds exact:

~~~text
ResearchPlan ref/version
PlanValidationResult
Method Selection / Method Work Item
Method ID / Role
Experiment Mode
Evidence Source Channel
Dataset / dataset role
T0 when applicable
target versions
formula / feature / DNA / model versions
seed where applicable
Plan lifecycle / lock state at start
~~~

### Trial Lifecycle Candidate

~~~text
CREATED
QUEUED
RUNNING
COMPLETED
PARTIAL
FAILED_PROCESS
TIMED_OUT
CANCELLED
~~~

### Execution Stages

~~~text
TE0 Admission
TE1 Materialize
TE2 Input Freeze
TE3 Execute
TE4 Measure
TE5 Integrity
TE6 Evidence Construct
TE7 Evidence Evaluate
TE8 Trial Complete
TE9 ResearchResult
~~~

### Measurement vs Evidence

~~~text
Measurement
≠ Evidence

Evidence
= measurement
+ provenance
+ trial
+ channel
+ role
+ target
+ quality
+ uncertainty
+ dependency
~~~

### Evidence Roles

Candidate:

~~~text
SUPPORTING
CONTRADICTING
DISCRIMINATING
CONDITIONING
BOUNDARY
CONTEXTUAL
PROCESS_VALIDATION
~~~

Evidence outcome candidate:

~~~text
SUPPORTIVE
CONTRADICTING
NEUTRAL
MIXED
INCONCLUSIVE
UNKNOWN
~~~

Evidence evaluation status:

~~~text
VALID
INVALID
NOT_OBSERVED
NOT_EVALUATED
UNKNOWN
~~~

Important:

~~~text
INVALID evidence
≠ contradicting evidence
~~~

### Process Axis

~~~text
SUCCESS
SUCCESS_WITH_LIMITATIONS
PARTIAL
FAILED
TIMED_OUT
CANCELLED
INVALIDATED
~~~

### Research Outcome Candidate

~~~text
SUPPORTIVE
WEAK_SUPPORT
CONTRADICTING
REFUTING_CANDIDATE
MIXED
INCONCLUSIVE
INSUFFICIENT_EVIDENCE
REGIME_DEPENDENT
DATA_LIMITED
UNKNOWN
NOT_EVALUABLE
~~~

Process failure normally yields NOT_EVALUABLE rather than a research refutation.

### Retry Boundary

Operational retry with unchanged frozen semantics may remain the same Trial attempt lineage.

Material change to:

~~~text
input
seed
dataset
parameters
model
metric
time boundary
~~~

creates a new Trial / Plan Version as appropriate.

No result-driven retry cherry-picking.

### Canonical Result Rule

Do not create:

~~~text
HistoricalValidationResult
OOSResult
ForwardResult
...
~~~

as separate canonical general result objects.

Use ResearchResult + Trial mode/channel.

ResearchResult is trial-level.

Question-level integration belongs to ResearchSynthesisAssessment.

---

## 7.64 Research Result Synthesis / Result Validation — Checkpoint

### ResearchSynthesisAssessment Responsibility

~~~text
ResearchResult[]
↓
Research Result Synthesis
↓
ResearchSynthesisAssessment
~~~

It integrates evidence without simple vote / case count.

### Synthesis Stages

~~~text
S0 Eligibility
S1 Process Integrity
S2 Evidence Identity / Provenance
S3 Channel Partition
S4 Evidence Role Partition
S5 Independence / Dependency Graph
S6 Quality / Uncertainty
S7 Coverage / Comparability
S8 Within-Channel Assessment
S9 Contradiction Preservation
S10 Failure-Boundary Integration
S11 Cross-Channel Synthesis
S12 Alternative Explanation
S13 Conclusion
S14 Limitations / Unknowns
~~~

### Channel Separation

Keep separate:

~~~text
RUNTIME_OBSERVATIONAL
HISTORICAL
OOS
FORWARD
STRESS
PRODUCTION_LIVE
~~~

Do not sum them as homogeneous cases.

### Channel Profile Candidate

~~~text
evidence_count
unique_event_count
independent_cluster_count
quality
outcome
contradiction
coverage
uncertainty
limitations
~~~

### Evidence Dependency Relations

Candidate:

~~~text
INDEPENDENT
PARTIALLY_DEPENDENT
SHARED_DATASET
SHARED_EVENT
SHARED_SOURCE
DERIVED_FROM
REDUNDANT
COMMON_CAUSE
UNKNOWN_DEPENDENCY
~~~

Unknown dependency must not be assumed independent.

### Coverage

Track what was and was not tested across:

~~~text
market
instrument
venue
time
horizon
DNA / regime
volatility
liquidity
leverage
session
macro context
~~~

Untested ≠ failed.

### Within-Channel Outcomes

~~~text
CONSISTENT_SUPPORT
MIXED_SUPPORT
CONSISTENT_CONTRADICTION
INSUFFICIENT
INCONCLUSIVE
BOUNDARY_DETECTED
NOT_EVALUABLE
~~~

### Synthesis Outcomes

Candidate:

~~~text
SUPPORTED
SUPPORTED_WITH_BOUNDARY
WEAK_SUPPORT
MIXED
CONTRADICTED
REFUTED
REGIME_DEPENDENT
INCONCLUSIVE
INSUFFICIENT_EVIDENCE
DATA_LIMITED
PROCESS_LIMITED
UNKNOWN
~~~

Empirical support can coexist with causal inconclusiveness.

No universal scalar weighting is fixed here.

### Synthesis Process Status

~~~text
SYNTHESIZED
SYNTHESIZED_WITH_LIMITATIONS
INCOMPLETE_INPUT
SYNTHESIS_BLOCKED
SYNTHESIS_FAILED
~~~

### Result Validation Gate

Post-research quality/trace gate:

~~~text
RV0 Identity / Version
RV1 Lineage / Trace
RV2 Question / Target Binding
RV3 Synthesis Process Integrity
RV4 Trial / Result Completeness
RV5 Evidence Provenance
RV6 Channel / Role Preservation
RV7 Independence / Dependency Preservation
RV8 Quality / Uncertainty
RV9 Contradiction / Refutation Preservation
RV10 FailureBoundary / Constraint Preservation
RV11 Coverage / Tested-vs-Untested
RV12 Alternative Explanation / Unknown
RV13 Conclusion / Scope Consistency
RV14 Reproducibility / Auditability
RV15 Downstream Authority Boundary
~~~

Outcomes:

~~~text
VALIDATED
VALIDATED_WITH_LIMITATIONS
NEEDS_CORRECTION
BLOCKED
RESULT_VALIDATION_FAILED
~~~

A SUPPORTED synthesis can be BLOCKED for broken trace/provenance.

A REFUTED or INCONCLUSIVE synthesis can be VALIDATED as a valid research artifact.

The gate does not re-synthesize.

Correction produces a new synthesis version.

### Validated Research Result Boundary Correction

Treat:

~~~text
Validated Research Result
~~~

as a logical qualified downstream boundary:

~~~text
ResearchSynthesisAssessmentRef
+
ResultValidationDecisionRef
~~~

not a duplicated full result store.

---

## 7.65 Knowledge Admission / Promotion — Checkpoint

### Position

~~~text
Validated Research Result boundary
↓
Knowledge Admission
↓
AdmittedKnowledgeCandidate
↓
Knowledge Promotion
↓
Canonical Knowledge / Relationships
↓
Knowledge Pool
~~~

### Knowledge Admission

Question:

> Does this validated research artifact contain reusable knowledge meaning worth entering the Knowledge system?

Checks:

~~~text
KA0 Validation Identity
KA1 Trace
KA2 Reusable Meaning
KA3 Claim / Scope
KA4 Conditions / Context
KA5 FailureBoundary / Exclusion
KA6 Evidence / Quality / Uncertainty
KA7 Existing Knowledge Retrieval
KA8 Duplicate / Overlap
KA9 Contradiction / Support Relation
KA10 Knowledge Value
KA11 Integrity
~~~

Outcomes:

~~~text
ADMIT
ADMIT_WITH_LIMITATIONS
HOLD
REJECT
NEED_MORE_CONTEXT
ADMISSION_FAILED
~~~

REJECT does not mean bad research.

SUPPORTED is not automatic ADMIT.

REFUTED / INCONCLUSIVE research can generate reusable Negative / Unknown / Boundary / Failure knowledge.

### AdmittedKnowledgeCandidate

Candidate structure:

~~~text
source validated research refs
subject
candidate knowledge type
claim / effect
conditions
exclusions
failure-boundary candidates
constraint candidates
scope / horizon
evidence / uncertainty
existing knowledge relations
limitations
~~~

It is not yet Canonical Knowledge.

### Knowledge Promotion

Checks:

~~~text
KP0 Candidate Identity
KP1 Semantic Identity
KP2 Knowledge Type
KP3 Existing Knowledge Relationship
KP4 New vs Update vs Relation
KP5 Scope / Condition Binding
KP6 Boundary / Constraint Binding
KP7 Evidence / Provenance Binding
KP8 Contradiction Preservation
KP9 Version
KP10 Relationship Construction
KP11 Integrity
KP12 Promotion Decision
~~~

Actions:

~~~text
CREATE_NEW
CREATE_NEW_VERSION
RELATION_ONLY
NO_CHANGE
DEFER_PROMOTION
PROMOTION_BLOCKED
PROMOTION_FAILED
~~~

Old Knowledge Versions remain immutable.

Material semantic change creates a new version.

Additional evidence without semantic change may create/update relationship/evidence linkage rather than a new semantic version.

Promotion does NOT directly mutate Knowledge Aging State.

New contradiction should trigger Knowledge Aging review through its own governance.

---

## 7.66 Knowledge Type Registry v1.0 — Corrected Checkpoint

### Two-Axis Design

Do not place Positive / Negative / Conditional at the same primary level as Feature / Formula / Failure.

Reason:

~~~text
Feature can be negative
Feature can be conditional
Formula can be negative
Market relationship can be positive + conditional
~~~

### Axis A — Primary Knowledge Family

Corrected IDs:

~~~text
KT.MARKET_RELATIONSHIP
KT.FEATURE
KT.FORMULA
KT.FAILURE
KT.FAILURE_BOUNDARY
KT.CONSTRAINT
KT.CONTEXT
KT.UNKNOWN
~~~

Meaning:

~~~text
KT.MARKET_RELATIONSHIP
= reusable market relation / pattern / mechanism knowledge

KT.FEATURE
= feature usefulness / failure / stability knowledge

KT.FORMULA
= formula validity / sensitivity / stability knowledge

KT.FAILURE
= reusable failure mode

KT.FAILURE_BOUNDARY
= where target transitions safe / weak / unsafe / unknown

KT.CONSTRAINT
= governed require / exclude / modify / allow safety knowledge

KT.CONTEXT
= reusable market/context structure

KT.UNKNOWN
= reusable unresolved region / evidence gap / unknown
~~~

### Axis B — Semantic Qualifier

Zero or more:

~~~text
KS.POSITIVE
KS.NEGATIVE
KS.CONDITIONAL
~~~

Example:

~~~text
KT.FEATURE
+
KS.NEGATIVE
+
KS.CONDITIONAL
~~~

rather than three separate primary Knowledge objects.

### Important Boundaries

~~~text
KT.MARKET_RELATIONSHIP
≠ KnowledgeRelationship graph edge

KT.UNKNOWN
≠ KnowledgeLifecycleProfile.UNKNOWN

UNMAPPABLE
≠ KT.UNKNOWN

KS.POSITIVE
≠ profitable
≠ positive EV
≠ production approved

KS.NEGATIVE
≠ failed process

KS.CONDITIONAL
≠ weak knowledge
~~~

### Edge

Legacy Edge remains a specialized maturity / promotion artifact:

~~~text
CAUSAL_EDGE
EMPIRICAL_EDGE
~~~

It is NOT a primary Knowledge Family.

Causal strength ≠ positive EV.

### Type Resolution

~~~text
KTR0 Subject
KTR1 Reusable Meaning
KTR2 Primary Family
KTR3 Semantic Qualifier
KTR4 Specialized Promotion Target
KTR5 Relationship / Boundary
KTR6 Integrity
↓
KnowledgeTypeResolution
~~~

Resolution state:

~~~text
RESOLVED
RESOLVED_WITH_LIMITATIONS
AMBIGUOUS
NEED_MORE_CONTEXT
UNMAPPABLE
TYPE_RESOLUTION_FAILED
~~~

Registry version:

~~~text
KNOWLEDGE_TYPE_REGISTRY_v1.0
~~~

Registry status:

~~~text
ACTIVE
DEPRECATED
RESERVED
REMOVED
~~~

---

## 7.67 Knowledge Record Common Contract — Checkpoint

### Principle

~~~text
Knowledge Record Common Contract
≠ giant universal Knowledge object
~~~

Use:

~~~text
Common semantic contract
+
Family-specific extension
~~~

Specialized canonical objects remain specialized.

Do not duplicate them into a second generic Knowledge table solely because of this contract.

### Common Contract

Every canonical Knowledge family should be able to expose:

~~~text
KR0 Identity
KR1 Type / Semantic Classification
KR2 Subject / Claim
KR3 Scope
KR4 Conditions
KR5 Boundary / Exclusion
KR6 Evidence / Provenance
KR7 Uncertainty / Limitations
KR8 Version / Lineage
KR9 Relationships
KR10 Lifecycle Reference
KR11 Integrity / Audit
~~~

### Common Semantic Shape

~~~text
Identity
- knowledge id
- knowledge version
- created at
- trace

Classification
- primary family
- semantic qualifiers
- type registry version

Semantics
- subject refs
- canonical claim
- effect / behavior

Scope
- asset / market / instrument / venue
- horizon / session
- regime / DNA scope

Conditions
- required
- supporting
- weakening
- context

Boundary
- known exclusions
- failure-boundary refs
- constraint refs
- unknown-region refs

Evidence
- validated research boundary refs
- synthesis refs
- evidence package refs
- provenance refs

Uncertainty
- uncertainty
- limitations
- evidence gaps
- unresolved questions

Version
- previous version
- supersession / lineage refs
- promotion / admission refs
- version reason

Relationships
- KnowledgeRelationship refs

Lifecycle
- KnowledgeLifecycleProfile ref

Integrity
- contract version
- type registry version
- trace status
- diagnostics
~~~

### Requiredness

Use:

~~~text
REQUIRED
REQUIRED_WHEN_APPLICABLE
OPTIONAL
~~~

Do not require fields that are semantically impossible for a family.

### Family Extensions

Examples:

~~~text
KT.FEATURE
- feature definition ref
- known strengths
- known failures
- redundancy refs

KT.FORMULA
- formula ref
- sensitivity / regime / stress profile
- known failures

KT.FAILURE
- failure type
- origin domain
- observed effect
- root-cause state
- known causes / unknowns
- reproduction refs

KT.FAILURE_BOUNDARY
- target ref
- boundary variables
- safe / weak / unsafe / unknown regions

KT.CONSTRAINT
- target scope
- constraint type
- condition
- action/effect
- source boundary refs

KT.CONTEXT
- context dimensions
- market/regime characteristics

KT.UNKNOWN
- unknown subject
- known context
- missing evidence
- reopen conditions
~~~

### Source-of-Truth Separation

~~~text
Knowledge semantics
→ Canonical Knowledge

Evidence
→ Research / Evidence objects

Knowledge relationship
→ KnowledgeRelationship

Freshness / health
→ KnowledgeLifecycleProfile

Runtime applicability
→ ApplicabilityAssessment

Production permission
→ downstream governance
~~~

---

## 7.68 Knowledge Relationship Registry / Contract v1.0 — Checkpoint

### Formal Role

~~~text
KnowledgeRecord
= Node

KnowledgeRelationship
= canonical semantic Edge

KnowledgeGraph
= View over Nodes + Edges
~~~

Graph does not duplicate Knowledge.

### Registry Types

~~~text
KR.SUPPORTS
KR.CONTRADICTS
KR.DEPENDS_ON
KR.DERIVED_FROM
KR.APPLIES_TO
KR.FAILS_UNDER
KR.SUPERSEDES
KR.DUPLICATES
KR.RELATED_TO
~~~

### Directionality

Directed:

~~~text
SUPPORTS
DEPENDS_ON
DERIVED_FROM
APPLIES_TO
FAILS_UNDER
SUPERSEDES
~~~

Semantic symmetric:

~~~text
CONTRADICTS
DUPLICATES
RELATED_TO
~~~

Do not double-store reverse symmetric edges.

### Meaning

~~~text
SUPPORTS
= Source materially supports Target
  ≠ independent evidence
  ≠ truth propagation

CONTRADICTS
= materially incompatible claims under overlapping scope
  ≠ automatic refutation

DEPENDS_ON
= Source current interpretation/validity materially relies on Target

DERIVED_FROM
= Source provenance originates from Target
  ≠ current dependency
  ≠ support

APPLIES_TO
= static reusable context relation
  ≠ runtime Applicability

FAILS_UNDER
= Source weakens/fails under Target boundary/context
  ≠ Constraint
  ≠ production block

SUPERSEDES
= Source is semantic successor of Target
  ≠ delete old Knowledge

DUPLICATES
= materially redundant semantic meaning
  ≠ automatic merge

RELATED_TO
= meaningful association when stronger registered relation is not justified
  no causal/support inference
~~~

### Version Binding

Relationships should bind exact Knowledge Versions.

New Knowledge Version does not silently inherit old relationships.

### Non-Transitivity

Do not automatically materialize transitive canonical edges.

Examples:

~~~text
A SUPPORTS B
B SUPPORTS C
≠ auto A SUPPORTS C

A DEPENDS_ON B
B DEPENDS_ON C
≠ auto canonical A DEPENDS_ON C
~~~

Traversal views may expose paths without writing new edges.

---

## 7.69 Knowledge Relationship Integrity Gate — Corrected Checkpoint

### Position

~~~text
KnowledgeRelationshipCandidate
↓
Relationship Resolution
↓
Knowledge Relationship Integrity Gate
↓
RelationshipIntegrityDecision
↓
Canonical Graph Writer
↓
KnowledgeRelationship
~~~

Gate ≠ Writer.

Gate does not silently rewrite relation type or endpoints.

### Gates

~~~text
RI0 Candidate Identity
RI1 Registry Membership
RI2 Endpoint Existence
RI3 Exact Version Binding
RI4 Self Relation
RI5 Direction / Symmetry
RI6 Family Compatibility
RI7 Scope / Condition Compatibility
RI8 Evidence / Basis Integrity
RI9 Existing Edge Check
RI10 Reverse Symmetric Duplicate Check
RI11 SUPERSEDES Cycle
RI12 DERIVED_FROM Cycle
RI13 DEPENDS_ON Cycle Review
RI14 Temporal / Validity Consistency
RI15 Authority Boundary
RI16 Graph Snapshot / Concurrency
RI17 Final Write Integrity
~~~

### Critical Rules

~~~text
Dangling edge
→ BLOCKED

Self relation
→ BLOCKED

SUPERSEDES cycle
→ BLOCKED

DERIVED_FROM cycle
→ BLOCKED

DEPENDS_ON cycle
→ review;
  block only when it creates invalid circular justification

invalid CONTRADICTS with insufficient scope overlap
→ NEEDS_CORRECTION

exact existing edge
→ NO_WRITE_REQUIRED

reverse-equivalent symmetric existing edge
→ NO_WRITE_REQUIRED
~~~

### Outcomes

~~~text
WRITE_ALLOWED
WRITE_ALLOWED_WITH_LIMITATIONS
NO_WRITE_REQUIRED
NEEDS_CORRECTION
BLOCKED
INTEGRITY_GATE_FAILED
~~~

### Concurrency

Decision binds:

~~~text
candidate version
candidate digest
source exact version
target exact version
graph snapshot/revision
registry version
~~~

Graph Writer must revalidate when the graph revision changed after the gate check.

This prevents TOCTOU cycle/duplicate creation.

### Authority Boundaries

~~~text
CONTRADICTS
≠ RETIRE

FAILS_UNDER
≠ Production BLOCK

APPLIES_TO
≠ Runtime APPLICABLE

SUPERSEDES
≠ delete

DUPLICATES
≠ automatic merge
~~~

---

## 7.70 Knowledge Lifecycle / Aging Governance — Checkpoint

### Canonical Meaning

Legacy FIX-017 remains the semantic anchor:

~~~text
KnowledgeLifecycleProfile
= Current freshness / health / revalidation projection

Evidence history
= Research / Evidence objects

Research maturity
= Hypothesis / Edge lifecycle

Production permission
= Production Promotion

Risk permission
= RiskState

Storage / archive
= Storage lifecycle
~~~

### States

~~~text
FRESH
CURRENT
AGING
STALE
DEGRADED
UNKNOWN
~~~

Meaning:

~~~text
FRESH
= recently formally validated and freshness basis is clear

CURRENT
= no longer newly validated but still current enough

AGING
= not invalid, but revalidation is approaching / evidence is aging

STALE
= freshness / revalidation requirement exceeded
  ≠ wrong
  ≠ retired

DEGRADED
= material health deterioration from new evidence,
  contradiction, demo-live divergence, etc.
  ≠ retired
  ≠ production paused

UNKNOWN
= health/freshness cannot responsibly be determined
  ≠ KT.UNKNOWN
~~~

### Normal Time-Aging Path

~~~text
FRESH
→ CURRENT
→ AGING
→ STALE
~~~

DEGRADED and UNKNOWN are not simple lower rankings in the same linear scale.

### Evaluation Inputs

~~~text
exact Knowledge Version
last validation
revalidation due
freshness basis
new validated research
production evidence
contradiction
demo-live divergence
failure-boundary changes
relationship / dependency context
aging policy
~~~

### Assessment / Apply Separation

~~~text
KnowledgeLifecycleAssessment
= what state appears justified

Transition Decision / Apply
= what state is actually changed to

StateTransitionEvent
= immutable transition fact

KnowledgeLifecycleProfile
= current projection
~~~

Evaluator does not directly mutate the projection.

### Review Triggers

~~~text
REVALIDATION_DUE
NEW_VALIDATED_RESEARCH
NEW_MATERIAL_CONTRADICTION
NEW_PRODUCTION_EVIDENCE
DEMO_LIVE_DIVERGENCE
FAILURE_BOUNDARY_CHANGE
DEPENDENCY_HEALTH_CHANGE
KNOWLEDGE_VERSION_CHANGE
AGING_POLICY_CHANGE
MIGRATION_UNCERTAINTY
~~~

Trigger ≠ transition.

### Important Current 04 Separation

Current 04 also mentions possible:

~~~text
ACTIVE
WEAK
RETIRED
UNDER_REVIEW
SUPERSEDED
~~~

These MUST NOT be merged into Knowledge Aging State.

Their exact future owner / semantics remain unresolved for Current adoption.

---

## 7.71 Applicability Evaluation Formal Contract — Corrected Checkpoint

### Question

Applicability asks:

> Can this exact Knowledge Version be used as decision material in this exact current market context?

It does NOT ask whether the Knowledge is universally true.

### Inputs

~~~text
Knowledge Record
KnowledgeLifecycleProfile
Current Market Understanding
Market DNA Snapshot
Runtime Quality Context
Runtime Freshness Context
Current Event Context
FailureBoundary
Constraint
KnowledgeRelationship
Evidence / Validation Context
~~~

### Evaluation Flow

~~~text
AE0 Evaluation Identity
AE1 Knowledge Integrity
AE2 Runtime Context Integrity
AE3 Scope Compatibility
AE4 Required Condition Match
AE5 Supporting / Weakening Conditions
AE6 Market DNA / Regime Compatibility
AE7 Lifecycle / Aging Context
AE8 Failure Boundary Check
AE9 Constraint Check
AE10 Contradiction / Relationship Review
AE11 Evidence / Uncertainty Context
AE12 Data Quality / Freshness
AE13 State Resolution
~~~

### States

~~~text
APPLICABLE
PARTIALLY_APPLICABLE
NOT_APPLICABLE
UNCERTAIN
BLOCKED_BY_CONSTRAINT
NOT_EVALUATED
~~~

### State Meaning

~~~text
APPLICABLE
= required scope/conditions sufficiently match,
  safe known boundary context,
  no effective hard blocking constraint,
  quality/context sufficient for decision-material use

PARTIALLY_APPLICABLE
= core conditions broadly match but material weakening,
  partial mismatch, weak boundary, aging/limitation, etc.

NOT_APPLICABLE
= evaluation succeeded and major scope/required conditions
  do not match, or current state is in an unsafe research boundary

UNCERTAIN
= evaluation occurred but critical information/conflict/unknown
  prevents responsible applicable/not-applicable conclusion

BLOCKED_BY_CONSTRAINT
= an effective/authorized hard Constraint prevents use

NOT_EVALUATED
= applicability evaluation did not meaningfully complete
~~~

### Important Correction — Contradiction

~~~text
Contradiction exists
≠ NOT_APPLICABLE automatically
~~~

Two individually applicable Knowledge objects may contradict and both pass to 05.

If contradiction destroys the ability to determine one Knowledge's applicability itself:

~~~text
→ UNCERTAIN candidate
~~~

04 still does not choose the conflict winner.

### FailureBoundary vs Constraint

~~~text
FailureBoundary UNSAFE
→ NOT_APPLICABLE candidate

Authorized hard Constraint violation
→ BLOCKED_BY_CONSTRAINT
~~~

Do not turn every research boundary directly into a Constraint.

### Lifecycle

No fixed mapping such as:

~~~text
FRESH → APPLICABLE
STALE → NOT_APPLICABLE
DEGRADED → BLOCKED
~~~

Lifecycle is context for Applicability, not Applicability itself.

### Market DNA

~~~text
DNA similarity
≠ Applicability proof
~~~

Critical DNA-axis mismatch must not be hidden by an average similarity score.

### Processing Status

Separate from applicability state:

~~~text
EVALUATED
EVALUATED_WITH_LIMITATIONS
NEED_MORE_CONTEXT
EVALUATION_BLOCKED
EVALUATION_FAILED
~~~

### Output

~~~text
ApplicabilityAssessment
~~~

Immutable to:

~~~text
exact Knowledge Version
exact Evaluation Cycle
exact Current Market Context
policy version
boundary / constraint context
uncertainty
trace
~~~

---

## 7.72 Applicable Knowledge Set Common Contract — Checkpoint

### Three-Layer Boundary

~~~text
ApplicableKnowledgeEntry
= one Knowledge transfer unit

ApplicableKnowledgeSet
= current decision-material collection

ExcludedApplicabilityTrace
= evaluated but excluded Knowledge audit
~~~

### Main Set Includes

~~~text
APPLICABLE
PARTIALLY_APPLICABLE
~~~

Only.

Excluded trace includes:

~~~text
NOT_APPLICABLE
UNCERTAIN
BLOCKED_BY_CONSTRAINT
NOT_EVALUATED
~~~

### ApplicableKnowledgeEntry

Must bind at least:

~~~text
Knowledge ref/version
ApplicabilityAssessment ref
Applicability State
condition summary
failure-boundary context
constraint context
relationship context
lifecycle context
evidence context
uncertainty / limitations
trace
~~~

PARTIALLY_APPLICABLE must preserve explicit limitation/restriction context.

### Set-Level Context

~~~text
same Evaluation Cycle
Current Market Context refs
Applicable entries
Partially-applicable entries

Contradiction groups
Dependency context
Duplicate / overlap clusters
Shared-evidence groups
Shared-cause groups

Boundary context
Constraint context
Set uncertainty

Excluded trace
Integrity status
~~~

### No Vote / Double Counting

~~~text
Knowledge count
≠ independent evidence count

Shared Evidence
≠ separate votes

Dependency chain
≠ extra reasons

Duplicate Knowledge
≠ extra support
~~~

### Set Integrity

Candidate status:

~~~text
COMPLETE
COMPLETE_WITH_LIMITATIONS
INCOMPLETE
BLOCKED
ASSEMBLY_FAILED
~~~

### Empty Set

~~~text
ApplicableKnowledgeSet entries = []
~~~

is valid.

Important:

~~~text
EMPTY
≠ NO_TRADE
~~~

04 reports absence of usable Knowledge.

05 owns the decision outcome.

---

## 7.73 Decision Context Assembly Formal Contract — Checkpoint

### Position

~~~text
ApplicableKnowledgeSet
+
Current Market Understanding
+
Market DNA Snapshot
+
Decision Scope Specification
↓
Decision Context Assembly
↓
DecisionContextSnapshot
~~~

### Responsibility

~~~text
VERIFY
BIND
FREEZE
TRACE
~~~

It does NOT:

~~~text
re-search Knowledge
re-evaluate Applicability
replace Knowledge Versions
recalculate Market DNA
resolve conflicts
weight Knowledge
assign Thesis Roles
calculate EV
produce Trade direction
produce NO_TRADE
~~~

### Decision Scope Specification

Pre-Thesis input:

~~~text
asset
market
instrument
venue scope
decision horizon
evaluation window
target context
scope policy version
~~~

Direction-neutral.

### Decision Scope Binding Is Different

~~~text
Decision Scope Specification
= requested domain before Thesis

Decision Scope Binding
= actual Thesis comparison grouping after Thesis construction
~~~

### Assembly Gates

~~~text
DC0 Assembly Identity
DC1 Applicable Set Integrity
DC2 Evaluation Cycle Compatibility
DC3 Market Understanding Binding
DC4 Market DNA Binding
DC5 Temporal Consistency
DC6 Decision Scope Compatibility
DC7 Knowledge Version Binding
DC8 Applicability Assessment Binding
DC9 Relationship Context Binding
DC10 Boundary / Constraint Binding
DC11 Quality / Freshness Binding
DC12 Uncertainty / Exclusion Binding
DC13 Snapshot Freshness
DC14 Authority Boundary
DC15 Final Snapshot Integrity
~~~

### Status

~~~text
READY
READY_WITH_LIMITATIONS
INCOMPLETE
INCONSISTENT
STALE
ASSEMBLY_FAILED
~~~

Status ≠ Decision Outcome.

### Immutable Snapshot

DecisionContextSnapshot binds exact:

~~~text
ApplicableKnowledgeSet
Knowledge Versions
Applicability Assessments
Current Market Understanding
Market DNA Snapshot
Quality / Freshness / Event Context
Decision Scope Specification
Relationship / Boundary / Constraint context
Excluded Trace
Uncertainty
assembly policy/version
~~~

New market context requires a new applicability/set/context cycle.

Do not mix new DNA with old ApplicabilityAssessment.

---

## 7.74 Knowledge Integration Formal Contract — Checkpoint

### Position

~~~text
DecisionContextSnapshot
↓
Knowledge Integration
↓
IntegratedKnowledgeContext
↓
Trade Thesis Construction
~~~

Only DecisionContextSnapshot contents may be used.

No new Knowledge search or excluded-Knowledge restoration.

### Integration Flow

~~~text
KI0 Input Integrity
KI1 Knowledge Member Normalization
KI2 Semantic / Horizon Alignment
KI3 Effect Structure
KI4 Mechanism Structure
KI5 Shared Evidence Structure
KI6 Independence Assessment
KI7 Dependency Structure
KI8 Common Cause Structure
KI9 Overlap / Redundancy Structure
KI10 Conflict Structure
KI11 Condition Structure
KI12 Failure Boundary Structure
KI13 Constraint Context
KI14 Uncertainty Structure
KI15 Integrated Context Integrity
~~~

### Core Structures

~~~text
EffectGroup
MechanismGroup
SharedEvidenceGroup
IndependenceCluster
DependencyGroup
CommonCauseGroup
OverlapGroup
ConflictGroup
ConditionGroup
BoundaryGroup
ConstraintGroup
UncertaintyGroup
~~~

### Semantics

~~~text
Effect
≠ Trade Action

Mechanism
≠ Causal proof

Shared Evidence
≠ Independent Evidence

Knowledge count
≠ Independent Reason count

Common Cause Candidate
≠ Proven Cause

Overlap
≠ Merge

Conflict
≠ Winner

Different Horizon
≠ Contradiction automatically

Failure Boundary
≠ Thesis Invalidation
~~~

### Thesis-Relative Roles Are NOT Assigned Here

Do not assign:

~~~text
PRIMARY
SUPPORTING
CONDITIONAL
CONTRADICTING
~~~

during Knowledge Integration.

Those roles belong to Trade Thesis Construction.

### Status

~~~text
INTEGRATED
PARTIALLY_INTEGRATED
UNRESOLVED
FAILED
~~~

Known unresolved market conflict can still be INTEGRATED if the conflict is correctly represented.

Empty input can produce an empty INTEGRATED context.

### Output

~~~text
IntegratedKnowledgeContext
~~~

Immutable and versioned by integration logic.

---

## 7.75 Trade Thesis Construction / Trade Thesis — Checkpoint

### Position

~~~text
IntegratedKnowledgeContext
↓
Trade Thesis Construction
↓
TradeThesis 0..N
↓
Decision Scope Binding
~~~

### Construction Flow

~~~text
TTC0 Input Integrity
TTC1 Thesis Candidate Discovery
TTC2 Effect / Horizon Coherence
TTC3 Mechanism Composition
TTC4 Thesis Member Selection
TTC5 Thesis-relative Role Assignment
TTC6 Shared Evidence / Independence Binding
TTC7 Dependency / Common Cause Binding
TTC8 Conflict / Contradiction Binding
TTC9 Required / Weakening Conditions
TTC10 Failure Boundary Translation
TTC11 Invalidation Construction
TTC12 Counter-mechanism Construction
TTC13 EV Input Context Assembly
TTC14 Uncertainty / Quality Assembly
TTC15 Thesis Coherence / Integrity
~~~

### 0..N Thesis

~~~text
0 Thesis
= valid construction result
≠ NO_TRADE

Multiple Thesis
= valid
~~~

Do not force one thesis from conflicting knowledge.

### Thesis-Relative Roles

Assigned here for the first time:

~~~text
PRIMARY
SUPPORTING
CONDITIONAL
CONTRADICTING
~~~

Meaning:

~~~text
PRIMARY
= central knowledge whose material collapse requires thesis re-evaluation

SUPPORTING
= additional compatible support
  ≠ extra vote

CONDITIONAL
= activation / regime / amplification / weakening context
  ≠ weak SUPPORTING

CONTRADICTING
= applicable knowledge materially opposing/weakening the thesis
  must not be hidden
~~~

Role is a Thesis-relative property, not a permanent Knowledge attribute.

### TradeThesis Core Semantics

~~~text
Expected Direction
Expected Effect
Expected Horizon

Required Conditions
Weakening Conditions

Main / Secondary Mechanism
Contradicting Members
Counter-mechanism

Shared Evidence
Independence
Dependency
Common Cause / overlap

Failure Boundary Context
Invalidation Conditions
Constraint Context

EV Input Context
Quality / Uncertainty
Trace
~~~

### Expected Direction

Candidate semantics:

~~~text
UPWARD
DOWNWARD
NON_DIRECTIONAL
TWO_SIDED
UNRESOLVED
~~~

Expected Direction is market expectation, not trade action.

~~~text
DOWNWARD
≠ TAKE_SHORT_RISK
~~~

### Failure Boundary / Invalidation / Stop Loss

Strict separation:

~~~text
Failure Boundary
= reusable research-level known limit

Thesis Invalidation
= current Thesis premise no longer holds

Stop Loss
= later execution / risk protection
~~~

### Counter-mechanism

Represents market process that may offset/reverse/delay the main mechanism.

It is not an automatic opposite trade.

### EV Ownership Correction

~~~text
Trade Thesis
= Expected Value Input Context

Decision Evaluation
= final Expected Value Assessment
~~~

Trade Thesis must not own:

~~~text
final expected value
trade_worthy
accept trade
position size
risk budget
~~~

### Expected Magnitude / Sequence / Persistence

Required when supported by research:

~~~text
expected magnitude
expected sequence
expected persistence
~~~

This is needed for future Post-Trade TradeThesisEvaluation compatibility.

Do not invent them if evidence does not support them.

### Construction Status

~~~text
BUILDABLE
PARTIAL
NOT_BUILDABLE
FAILED
~~~

Important:

~~~text
NOT_BUILDABLE
≠ FAILED

NOT_BUILDABLE
≠ NO_TRADE
~~~

### TradeThesisMember Candidate

A Thesis-relative member projection may preserve:

~~~text
Knowledge ref/version
Thesis role
Applicability state
Effect / Mechanism group refs
Shared Evidence
Dependency / Common Cause
Conditions
Contradictions
Uncertainty / limitations
~~~

Useful for Post-Trade member attribution.

---

## 7.76 Decision Scope Binding Formal Contract — Checkpoint

### Position

~~~text
TradeThesis 0..N
↓
Optional AI Review
↓
Decision Scope Binding
↓
DecisionScope 0..N
↓
Individual Thesis Evaluation
~~~

### Question

> Which Trade Theses can be meaningfully evaluated and compared under one Decision Result boundary?

It does NOT rank or evaluate thesis quality.

### Binding Flow

~~~text
DSB0 Input Integrity
DSB1 Thesis Validity
DSB2 Asset Compatibility
DSB3 Market Compatibility
DSB4 Instrument Compatibility
DSB5 Venue / Execution Target Compatibility
DSB6 Horizon Compatibility
DSB7 Evaluation Window Compatibility
DSB8 Decision Context Compatibility
DSB9 Runtime Context Compatibility
DSB10 Constraint / Boundary Compatibility
DSB11 Mutual Comparability
DSB12 Scope Partitioning
DSB13 Scope Integrity
~~~

### Hard / Main Dimensions

Candidate hard dimensions:

~~~text
same/compatible Decision Context
same Asset
same/compatible decision-target Instrument
~~~

Conditional compatibility dimensions:

~~~text
Venue
Expected Horizon
Evaluation Window
Context Conditions
~~~

### Not Scope Dimensions

Do NOT define scope by:

~~~text
Expected Direction
Expected Effect direction
Mechanism
Expected Value
Evidence Strength
Thesis Quality
Confidence
Trade-worthiness
~~~

Reason:

Opposing Long/Short theses must be able to compete inside the same Decision Scope.

### Horizon Compatibility

Candidate:

~~~text
EXACT
COMPATIBLE_OVERLAP
COMPATIBLE_NESTED
PARTIALLY_COMPATIBLE
INCOMPATIBLE
UNKNOWN
~~~

Do not rewrite original Thesis horizons to the scope comparison window.

Example:

~~~text
T-A = 20–40m
T-B = 30–60m

Decision Scope comparison window
may be 30–40m

but original Thesis horizons remain unchanged.
~~~

### Decision Target vs Evidence Market

~~~text
Evidence Market
≠ Decision-target Market/Instrument
~~~

A spot-flow thesis and derivatives thesis may still compete if both make expectations about the same decision-target instrument.

### Compatibility Assessment

Candidate:

~~~text
COMPARABLE
COMPARABLE_WITH_LIMITATIONS
NOT_COMPARABLE
NEED_MORE_CONTEXT
~~~

### DecisionScope

Immutable comparison boundary containing:

~~~text
Decision Context
Asset / Market
Decision-target Instrument
Venue Scope
Decision Horizon
Evaluation Window
Trade Thesis refs/versions
Compatibility assessments
Binding policy/version
Trace
~~~

### Unbound Thesis

Preserve:

~~~text
UnboundThesisTrace
~~~

Reasons may include:

~~~text
HORIZON_INCOMPATIBLE
INSTRUMENT_INCOMPATIBLE
CONTEXT_INCOMPATIBLE
EVALUATION_WINDOW_MISMATCH
SCOPE_AMBIGUOUS
MISSING_SCOPE_CONTEXT
STALE_THESIS
INVALID_CONTEXT_BINDING
~~~

Unbound ≠ invalid Thesis.

If possible, create a separate Decision Scope rather than silently discard it.

### Single / Zero Scope

~~~text
single-Thesis Decision Scope
= valid

0 Trade Thesis
→ 0 Decision Scope
= valid process result
≠ NO_TRADE
~~~

### Binding Status

~~~text
BOUND
PARTIALLY_BOUND
NO_BINDABLE_THESIS
INCOMPLETE
INCONSISTENT
STALE
BINDING_FAILED
~~~

Binding failure/status ≠ Decision Outcome.

---

## 7.77 Intermediate Checkpoint — Integrated Responsibility Review

### No Major Responsibility Collision Found

After correction, the core responsibilities separate as:

~~~text
Candidate Promotion
= worth presenting to Research Intake

Research Intake
= worth formally admitting

Research Router
= which research domain owns it

Research Method Routing
= how to study it

Research Plan
= reproducible execution specification

Plan Validation
= may this plan start research?

Research Execution
= run frozen Trials and create ResearchResult

Research Synthesis
= integrate trial evidence

Result Validation
= is synthesis a transferable research artifact?

Knowledge Admission
= is there reusable knowledge meaning?

Knowledge Promotion
= how is it canonicalized/versioned/related?

Knowledge Type
= what kind of reusable knowledge is it?

Knowledge Record
= canonical semantic knowledge

KnowledgeRelationship
= graph relation between knowledge versions

Knowledge Lifecycle
= current freshness / health

Applicability
= may this knowledge be used now?

Applicable Knowledge Set
= 04→05 usable-knowledge boundary

Decision Context
= freeze this decision cycle's inputs

Knowledge Integration
= structure meaning, dependencies, overlap and conflict

Trade Thesis
= compose one market reasoning hypothesis

Decision Scope Binding
= define which theses are directly comparable
~~~

### Important Non-Equivalences

~~~text
Research Candidate
≠ Accepted Research

Research Plan
≠ PlanValidationResult

ResearchResult
≠ ResearchSynthesisAssessment

Validated Research Result
≠ duplicated result store

Research Outcome
≠ Process Status

Knowledge
≠ Evidence

KT.MARKET_RELATIONSHIP
≠ KnowledgeRelationship

Knowledge Aging
≠ Knowledge Status / Research maturity

Knowledge
≠ Applicable Knowledge

Applicability
≠ Evidence Strength

Applicable Knowledge Set
≠ Vote

Decision Context
≠ Integrated Knowledge Context

Knowledge Integration
≠ Knowledge Merge

Trade Thesis
≠ Expected Value Assessment

Expected Direction
≠ Trade Action

Failure Boundary
≠ Thesis Invalidation

Thesis Invalidation
≠ Stop Loss

Decision Scope
≠ Trade Thesis

Direction / Mechanism / EV
≠ Decision Scope identity

THESIS_NOT_BUILDABLE
≠ NO_TRADE
~~~

### Trace Continuity Review

The intended trace remains continuous:

~~~text
Trade Thesis
→ IntegratedKnowledgeContext
→ DecisionContextSnapshot
→ ApplicableKnowledgeSet
→ ApplicableKnowledgeEntry
→ ApplicabilityAssessment
→ KnowledgeRecord
→ Knowledge Admission / Promotion
→ Validated Research Result boundary
→ ResearchSynthesisAssessment
→ ResearchResult
→ ResearchTrial
→ ResearchPlan
→ ResearchCandidate
→ Finding / Source
~~~

No intended silent evidence copy is required.

### Remaining Current-Reconciliation Items

These are intentionally unresolved, not silently fixed:

1. Current 03 broad Routing / Prioritization terminology must be reconciled with the new two-stage:
   Domain Routing vs Method/Prioritization Routing.

2. Current 04 candidate Knowledge Status:
   ACTIVE / WEAK / RETIRED / UNDER_REVIEW / SUPERSEDED
   needs a separate owner/state contract and must not be merged into Knowledge Aging.

3. Applicability thresholds / DNA distance / confidence formulas remain undefined by design.

4. Knowledge Family-specific required fields remain a later contract/schema task.

5. Constraint authorization/effective-state governance remains separate from the Applicability contract.

6. Trade Thesis Expected Direction supports NON_DIRECTIONAL / TWO_SIDED conceptually, but the v1 Production Decision outcome vocabulary has not yet been formally closed.

7. 05 Decision is NOT complete until:
   Individual Thesis Evaluation,
   Expected Value Assessment,
   Cross-Thesis Comparison,
   Decision Result Finalization,
   Decision Result,
   and 05→Defense Handoff are formalized.

### Final Checkpoint Flow

~~~text
03_RESEARCH
↓
Validated Research Result boundary

04_KNOWLEDGE_APPLICABILITY — Maintenance
↓
Knowledge Admission
↓
Knowledge Promotion
↓
Knowledge Type Resolution
↓
Knowledge Record
↓
Knowledge Relationship
↓
Knowledge Lifecycle

04_KNOWLEDGE_APPLICABILITY — Runtime
↓
Applicability Evaluation
↓
Applicable Knowledge Set

05_DECISION
↓
Decision Context Assembly
↓
DecisionContextSnapshot
↓
Knowledge Integration
↓
IntegratedKnowledgeContext
↓
Trade Thesis Construction
↓
TradeThesis 0..N
↓
Decision Scope Binding
↓
DecisionScope 0..N

[CHECKPOINT ENDS HERE]

Next:
Individual Thesis Evaluation
↓
Expected Value Assessment
↓
Cross-Thesis Comparison
↓
Decision Result Finalization
↓
Decision Result
↓
05→Defense Handoff
~~~

### Checkpoint Status

~~~text
SOURCE_STATUS:
MIXED

SOURCE_BACKED:
- Current 03 Research boundaries
- Current 04 Knowledge / Applicability boundaries
- Legacy ResearchPlan / ResearchTrial / ResearchResult
- Legacy FeatureKnowledge / FormulaKnowledge / Failure / FailureBoundary / Constraint
- Legacy KnowledgeRelationship
- Legacy KnowledgeLifecycleProfile
- Legacy TradeThesis / SignalDecision concepts

CURRENT_DERIVED:
- detailed Intake / Registry / Method contracts
- Research Synthesis / Result Validation refinement
- two-axis Knowledge Type registry
- Knowledge Common Contract
- Relationship semantic/integrity contracts
- detailed Lifecycle Governance
- detailed Applicability contract
- Applicable Knowledge Set transfer contract
- Decision Context / Integration / 0..N Thesis / Scope Binding

CURRENT_03_CONFLICT_STATUS:
MINOR TERMINOLOGY RECONCILIATION REQUIRED

CURRENT_04_CONFLICT_STATUS:
MINOR SEMANTIC REFINEMENT APPLIED
- contradiction vs applicability clarified
- aging vs candidate Knowledge Status separated

LEGACY_CONFLICT_STATUS:
MINOR / MODERATE RESPONSIBILITY REFINEMENT
NO ARCHITECTURE-BREAKING CONFLICT FOUND

REVIEW_STAGE:
INTERMEDIATE_CHECKPOINT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~



---

## 7.78 05_DECISION — Final Checkpoint Scope

### Purpose

This checkpoint closes the detailed Reference design of 05_DECISION after the Intermediate Checkpoint in 7.57–7.77.

It consolidates the post-checkpoint contracts:

~~~text
Individual Thesis Evaluation
Expected Value Assessment
Cross-Thesis Comparison
Decision Candidate Resolution
Decision Result Finalization / Integrity Gate
Decision Result
DecisionCycleProcessingResult
05 → Defense Handoff
05_DECISION Integrated Final Review
~~~

This is still Reference material.

~~~text
REVIEW_STAGE:
FINAL_CHECKPOINT

05_REFERENCE_SEMANTIC_STATUS:
CLOSED_CANDIDATE

CURRENT_DESIGN_STATUS:
NOT_ADOPTED

PRODUCTION_STATUS:
NOT_A_PRODUCTION_SPEC
~~~

### Final 05 Flow

~~~text
04_KNOWLEDGE_APPLICABILITY
↓
ApplicableKnowledgeSet

────────────────────────────────
05_DECISION
────────────────────────────────

Decision Context Assembly
↓
DecisionContextSnapshot

↓
Knowledge Integration
↓
IntegratedKnowledgeContext

↓
Trade Thesis Construction
↓
TradeThesis 0..N

↓
Decision Scope Binding
↓
DecisionScope 0..N

↓
Individual Thesis Evaluation
↓
PreDecisionThesisAssessment[]

↓
Expected Value Assessment
↓
ExpectedValueAssessment[]

↓
Cross-Thesis Comparison
↓
CrossThesisComparisonResult

↓
Decision Candidate Resolution
↓
DecisionResultCandidate

↓
Decision Result Finalization / Integrity Gate
↓
DecisionFinalizationDecision

↓
FINALIZE_ALLOWED*
↓
DecisionResult

────────────────────────────────
05_DECISION END
────────────────────────────────

↓
Defense Handoff
↓
DefenseAdmissionEnvelope
↓
DefenseAdmissionDecision
↓
Defense Evaluation
~~~

### Final Cardinality

~~~text
1 DecisionCycle
→ 1 DecisionContextSnapshot

1 DecisionContextSnapshot
→ 1 IntegratedKnowledgeContext candidate

1 IntegratedKnowledgeContext
→ 0..N TradeThesis

1 DecisionCycle
→ 0..N DecisionScope

1 DecisionScope
→ 0..N TradeThesis

1 TradeThesis
→ 0..1 PreDecisionThesisAssessment per evaluation attempt/version

1 eligible TradeThesis
→ 0..1 ExpectedValueAssessment per evaluation attempt/version

1 DecisionScope
→ 0..1 CrossThesisComparisonResult per comparison attempt/version

1 DecisionScope
→ 0..1 Canonical DecisionResult

1 DecisionCycle
→ 0..N Canonical DecisionResult
~~~

### Supersession Rule

This Final Checkpoint does not delete the Intermediate Checkpoint.

Where a Final Correction below conflicts with 7.57–7.77, the Final Checkpoint is the later Reference interpretation.

The Intermediate Checkpoint remains historical review evidence.

---

## 7.79 Individual Thesis Evaluation / PreDecisionThesisAssessment — Final Checkpoint

### Formal Responsibility

Individual Thesis Evaluation evaluates one TradeThesis in isolation before economic EV comparison.

Question:

> Is this exact Trade Thesis semantically, evidentially and contextually coherent enough to enter Expected Value Assessment?

It does NOT decide whether the Thesis is profitable, better than another Thesis, or trade-worthy.

### Naming Boundary

~~~text
PreDecisionThesisAssessment
= pre-decision thesis health/readiness

TradeThesisEvaluation
= post-trade evaluation of what actually happened
~~~

Do not reuse the same object name.

### Inputs

~~~text
TradeThesis exact version
DecisionScope
DecisionContextSnapshot
IntegratedKnowledgeContext
TradeThesisMember projections
ApplicabilityAssessment refs
Evidence / Independence context
KnowledgeLifecycle context
FailureBoundary context
Constraint context
Runtime Quality / Freshness
Optional advisory AI review
~~~

### Evaluation Flow

~~~text
ITE0 Input Identity / Integrity
ITE1 Scope / Context Binding
ITE2 Thesis Construction Integrity
ITE3 Expected Effect Coherence
ITE4 Direction / Horizon Coherence
ITE5 Mechanism Coherence
ITE6 Thesis Member Role Integrity
ITE7 Evidence Independence
ITE8 Dependency / Common Cause / Overlap
ITE9 Applicability Quality
ITE10 Contradiction Burden
ITE11 Required / Weakening Condition Health
ITE12 Invalidation Proximity
ITE13 Failure Boundary Context
ITE14 Constraint Context
ITE15 Runtime Quality / Freshness
ITE16 Uncertainty Structure
ITE17 EV Input Readiness
ITE18 Assessment Resolution
~~~

### Role Integrity

The evaluator checks, but does not rewrite:

~~~text
PRIMARY
SUPPORTING
CONDITIONAL
CONTRADICTING
~~~

Examples:

~~~text
PRIMARY
= central to the Thesis

SUPPORTING
= additional compatible support
  ≠ extra vote

CONDITIONAL
= activation / regime / weakening / amplification context

CONTRADICTING
= material opposing knowledge
  must remain visible
~~~

Misassignment returns an assessment issue rather than silently changing the TradeThesis.

### Evidence Independence

Within-Thesis independence candidates:

~~~text
STRONGLY_INDEPENDENT
MOSTLY_INDEPENDENT
PARTIALLY_DEPENDENT
HIGHLY_DEPENDENT
UNKNOWN
~~~

Keep dependency structure.

Do not reduce to one unexplained independence score.

~~~text
3 Knowledge members
sharing one event
≠ 3 independent reasons
~~~

### Applicability Quality

Do not count Applicable members.

Preserve the role of each member.

~~~text
PRIMARY PARTIALLY_APPLICABLE
may be materially more important
than
minor SUPPORTING PARTIALLY_APPLICABLE
~~~

### Contradiction Burden

Evaluate contradiction dimensions such as:

~~~text
EXPECTED_EFFECT
DIRECTION
MECHANISM
HORIZON
REQUIRED_CONDITION
MAGNITUDE
PERSISTENCE
SEQUENCE
APPLICABILITY_CONTEXT
~~~

Contradiction count alone is not a rejection rule.

### Conditions

Required-condition candidates:

~~~text
SATISFIED
PARTIALLY_SATISFIED
NOT_SATISFIED
UNKNOWN
NOT_OBSERVABLE
~~~

A required premise not holding is a semantic result, not a system failure.

### Invalidation Proximity

Candidate:

~~~text
FAR
MODERATE_DISTANCE
NEAR
TRIGGERED
UNKNOWN
~~~

~~~text
Invalidation
≠ Stop Loss

Invalidation Triggered
≠ System Failure
~~~

If already triggered, the Thesis normally does not proceed to current EV evaluation.

### Failure Boundary

Preserve:

~~~text
SAFE_REGION
WEAK_REGION
UNSAFE_REGION
UNKNOWN_REGION
~~~

If an UNSAFE boundary or an effective hard Constraint appears in a Thesis that passed 04 as usable, treat it as an upstream consistency issue.

Do not silently rewrite Applicability.

### EV Input Readiness

Candidate:

~~~text
READY
READY_WITH_LIMITATIONS
INCOMPLETE
INSUFFICIENT
NOT_APPLICABLE
~~~

This checks whether EV can be responsibly assessed.

It does not calculate EV.

### Process Status

~~~text
COMPLETED
COMPLETED_WITH_LIMITATIONS
INCOMPLETE
STALE
INCONSISTENT
ASSESSMENT_FAILED
~~~

### Semantic Readiness

~~~text
READY_FOR_EV
READY_FOR_EV_WITH_LIMITATIONS
NOT_READY_FOR_EV
NOT_EVALUABLE
~~~

Important:

~~~text
READY_FOR_EV
≠ Trade-worthy

NOT_READY_FOR_EV
≠ NO_TRADE

NOT_EVALUABLE
≠ NO_TRADE

STALE
≠ NO_TRADE

ASSESSMENT_FAILED
≠ NO_TRADE
~~~

### PreDecisionThesisAssessment Minimum Concept

~~~text
Identity
- assessment id/version
- exact TradeThesis ref/version/digest
- DecisionScope ref
- DecisionContext ref
- assessment logic/policy version
- evaluated_at / trace

Integrity
- scope binding
- construction integrity
- trace integrity

Effect / Horizon / Mechanism
- effect coherence
- direction coherence
- horizon coherence
- mechanism assessment

Member Roles
- PRIMARY integrity
- SUPPORTING integrity
- CONDITIONAL integrity
- CONTRADICTING integrity

Evidence / Dependency
- independence profile
- shared evidence
- dependency
- common cause
- overlap

Applicability / Conflict
- applicability context
- critical partial members
- contradiction burden
- counter-mechanism context

Conditions / Invalidation
- required condition states
- weakening condition states
- premise state
- invalidation proximity

Boundary / Constraint
- failure boundary context
- constraint consistency

Runtime
- quality
- freshness
- thesis validity

EV Readiness
- available / missing / insufficient EV inputs

Uncertainty
- uncertainty axes
- unresolved questions
- limitations

Resolution
- process status
- semantic readiness
- reason codes
~~~

### Feedback

Unexpected contradiction, unknown dependency, repeated construction defects or missing EV research may create Findings.

~~~text
Finding
↓
ResearchCandidate
↓
03_RESEARCH
~~~

Do not directly mutate Knowledge.

---

## 7.80 Expected Value Assessment — Final Checkpoint

### Formal Responsibility

Expected Value Assessment owns the economic expectation of one eligible Trade Thesis.

It integrates, without collapsing their provenance:

~~~text
Expected Return
Expected Loss
Probability / Frequency
Gain-Loss Asymmetry
Tail Risk
Invalidation Risk
Estimated Fee
Estimated Spread
Estimated Slippage
Estimated Funding / Financing
Other material expected costs
Uncertainty
~~~

### Admission

Normally only:

~~~text
READY_FOR_EV
READY_FOR_EV_WITH_LIMITATIONS
~~~

enter EV Assessment.

Do not produce artificial EV for:

~~~text
NOT_READY_FOR_EV
NOT_EVALUABLE
~~~

### Position Size Boundary

05 does not own exact Position Size.

Therefore canonical EV is evaluated on an explicit normalized economic basis such as:

~~~text
RETURN_RATE
BPS_PER_UNIT_NOTIONAL
RETURN_PER_REFERENCE_NOTIONAL
~~~

Do not make canonical 05 EV a portfolio currency profit amount whose meaning depends on an unknown final size.

### EV Basis

Conceptually preserve:

~~~text
basis_type
currency when relevant
reference_notional when relevant
return_unit
evaluation_horizon
cost_basis
normalization_logic_version
~~~

### Assessment Flow

~~~text
EVA0 Input Identity / Admission
EVA1 EV Basis / Unit Normalization
EVA2 Outcome Scenario Structure
EVA3 Probability / Frequency Context
EVA4 Expected Return
EVA5 Expected Loss
EVA6 Gain-Loss Asymmetry
EVA7 Tail Risk
EVA8 Invalidation Risk
EVA9 Estimated Costs
EVA10 Dependency / Double-Count Control
EVA11 Uncertainty
EVA12 Gross EV Synthesis
EVA13 Cost-Adjusted EV Synthesis
EVA14 Sensitivity / Robustness
EVA15 Comparison Readiness
EVA16 Final Integrity
~~~

### Probability / Frequency

Keep separate:

~~~text
Historical Frequency
≠ True Probability
~~~

Source candidates:

~~~text
EMPIRICAL_FREQUENCY
CONDITIONAL_FREQUENCY
CALIBRATED_MODEL_PROBABILITY
SCENARIO_WEIGHT
UNKNOWN
~~~

For quantitative probability, preserve where available:

~~~text
value/range
condition scope
sample count
unique event count
independent cluster count
evidence channel
calibration ref
coverage
uncertainty
limitations
~~~

AI opinion alone is not canonical Probability.

### Expected Return

Expected Return is not Best Case.

Preserve available distribution context:

~~~text
mean
median
quantiles
range
distribution ref
horizon
regime scope
independent event count
uncertainty
~~~

### Expected Loss

~~~text
Expected Loss
≠ Stop Loss
~~~

Expected Loss is a research/economic adverse outcome profile.

Stop Loss is downstream risk/execution control.

### Gain-Loss Asymmetry

Candidate context:

~~~text
expected gain magnitude
expected loss magnitude
gain-loss ratio
positive vs negative tail
distribution skew
~~~

Neither win rate nor gain/loss ratio alone defines EV.

### Tail Risk

Tail Risk is separate from ordinary expected loss.

Where available:

~~~text
tail probability context
tail loss magnitude
expected shortfall
stress result refs
failure boundary refs
historical tail cases
live tail evidence
uncertainty
~~~

Unknown tail risk must not become zero.

### Invalidation Risk

Invalidation Risk is the risk that the Thesis premise ceases to be valid before the expected horizon is complete.

It is distinct from price-loss probability.

Preserve where available:

~~~text
invalidation proximity
historical invalidation frequency
time-to-invalidation context
counter-mechanism strength
uncertainty
~~~

### Estimated Costs

Decision-time cost components may include:

~~~text
Estimated Fee
Estimated Spread
Estimated Slippage
Estimated Funding / Financing
Borrow / Holding / Conversion Cost when applicable
~~~

~~~text
Estimated Cost
≠ Actual Execution Cost
~~~

Cost component metadata should identify whether a model already includes:

~~~text
spread
fee
market impact
funding
other embedded cost
~~~

### EV Validity Envelope

Formal Candidate:

> EV Validity Envelope = the market/execution assumption range within which this ExpectedValueAssessment remains economically interpretable.

May include:

~~~text
reference notional / size band
spread range
slippage range
funding range
venue assumption
liquidity assumption
execution style assumption
cost model version
~~~

Defense / Execution may be stricter.

They may not expand the economic envelope without new EV assessment.

### Double-Count Control

Maintain a component overlap map.

Examples:

~~~text
loss profile already net of fees
→ do not subtract fee again

all-in slippage already includes spread
→ do not add spread again

tail events already embedded in loss distribution
→ no second fixed tail penalty

invalidation cases already embedded in outcome distribution
→ no second fixed invalidation penalty
~~~

Overlap states may include:

~~~text
INDEPENDENT_COMPONENTS
PARTIAL_OVERLAP
FULLY_EMBEDDED
UNKNOWN_OVERLAP
~~~

UNKNOWN overlap increases uncertainty rather than encouraging arbitrary addition.

### EV Synthesis

Where scenario probability/weight semantics and outcome magnitudes are valid:

~~~text
Gross EV
=
Σ(
  Scenario Probability/Weight
  ×
  Scenario Gross Outcome
)
~~~

Cost-adjusted concept:

~~~text
Cost-Adjusted EV
=
Gross EV
-
Non-embedded Expected Costs
~~~

Do not calculate a false precise number if the required semantics are unsupported.

### Tail / Invalidation Integration

Use one of:

~~~text
A. explicitly modeled scenario
B. already embedded in distribution
C. unquantified uncertainty / limitation
~~~

Do not apply universal fixed penalties.

### Uncertainty

Keep dimensions such as:

~~~text
Return
Loss
Probability
Tail
Invalidation
Cost
Slippage
Funding
Model
Regime Transfer
Sample / Independence
~~~

Point estimate must not hide material range/uncertainty.

### Quantification Status

~~~text
QUANTIFIED
QUANTIFIED_WITH_LIMITATIONS
PARTIALLY_QUANTIFIED
NOT_QUANTIFIABLE
NOT_ASSESSED
~~~

~~~text
NOT_QUANTIFIABLE
≠ Negative EV
~~~

### EV Sign State

Candidate:

~~~text
POSITIVE
NEGATIVE
NEAR_ZERO
CROSSES_ZERO
UNKNOWN
NOT_QUANTIFIABLE
~~~

### Robustness Context

Candidate:

~~~text
ROBUSTLY_POSITIVE
POSITIVE_BUT_FRAGILE
CROSSES_ZERO_UNDER_PLAUSIBLE_ASSUMPTIONS
ROBUSTLY_NEGATIVE
INDETERMINATE
~~~

### Economic Viability Context

Candidate:

~~~text
FAVORABLE
FAVORABLE_BUT_FRAGILE
MARGINAL
UNFAVORABLE
INDETERMINATE
NOT_ASSESSABLE
~~~

This is economic context, not Decision Outcome.

### Comparison Readiness

~~~text
READY_FOR_COMPARISON
READY_FOR_COMPARISON_WITH_LIMITATIONS
NOT_READY_FOR_COMPARISON
NOT_ASSESSABLE
~~~

A negative EV assessment can still be READY_FOR_COMPARISON.

### Core Invariants

~~~text
Win Rate
≠ EV

Evidence Strength
≠ EV

Applicability
≠ EV

Causal Strength
≠ EV

Unknown
≠ zero

Positive EV
≠ TAKE_RISK

Negative EV
≠ NO_TRADE automatically

EV
≠ Position Size

EV
≠ Leverage

EV
≠ BUY/SELL Order
~~~

---

## 7.81 Cross-Thesis Comparison — Final Checkpoint

### Formal Responsibility

Cross-Thesis Comparison compares eligible TradeTheses inside one exact DecisionScope.

It compares more than EV:

~~~text
Expected Value
Expected Horizon
Evidence Independence
Mechanism Independence
Applicability Quality
Contradiction
Invalidation Risk
Failure Boundary / Constraint Context
Uncertainty
Overlap / Redundancy
Mutual Exclusivity / Coexistence
Context Compatibility
~~~

It does not produce the canonical trade Decision.

### Final Scope Correction

For v1 direct Cross-Thesis Comparison:

~~~text
all compared TradeTheses
must bind to the exact same
DecisionContextSnapshot
and decision_cycle_id
~~~

This supersedes the looser Intermediate Checkpoint phrase:

~~~text
same / compatible Decision Context
~~~

Different DecisionContextSnapshot values require a different Decision Scope / later meta-comparison.

### Comparison Flow

~~~text
CTC0 Input Integrity
CTC1 Scope Membership
CTC2 Thesis / Assessment Alignment
CTC3 EV Basis Compatibility
CTC4 Economic Value Comparison
CTC5 Evidence Independence
CTC6 Mechanism Independence
CTC7 Applicability Quality
CTC8 Contradiction
CTC9 Invalidation Risk
CTC10 Boundary / Constraint
CTC11 Uncertainty
CTC12 Overlap / Redundancy
CTC13 Mutual Exclusivity / Coexistence
CTC14 Context Compatibility
CTC15 Pairwise Comparison
CTC16 Scope-level Structure
CTC17 Comparison Frontier / Trade-off
CTC18 Comparison Integrity
~~~

### EV Basis Compatibility

Candidate:

~~~text
DIRECTLY_COMPARABLE
NORMALIZABLE
COMPARABLE_WITH_LIMITATIONS
NOT_COMPARABLE
UNKNOWN
~~~

Legitimate unit normalization is allowed.

Do not time-scale market return linearly merely to force comparability.

### Evidence Independence

Between-Thesis candidates:

~~~text
INDEPENDENT
MOSTLY_INDEPENDENT
PARTIALLY_SHARED
HIGHLY_SHARED
SAME_EVIDENCE_BASE
UNKNOWN
~~~

~~~text
same direction
≠ independent confirmation
~~~

### Mechanism Independence

Candidate:

~~~text
INDEPENDENT_MECHANISMS
DISTINCT_BUT_LINKED
PARTIALLY_OVERLAPPING
SAME_CORE_MECHANISM
UNKNOWN
~~~

Keep separate from Evidence Independence.

### Contradiction

Do not compare contradiction counts.

Preserve which dimension is contradicted and whether the contradictory evidence is independent/material.

### Invalidation

Compare Thesis premise stability, not stop-loss distance.

### Uncertainty

Do not average all uncertainty dimensions into one unexplained value.

Material unquantified risk stays explicit.

### Overlap / Redundancy

Compare:

~~~text
Knowledge-member overlap
Evidence overlap
Mechanism overlap
Effect overlap
Condition overlap
Market-event overlap
Common-cause overlap
~~~

Candidate overlap state:

~~~text
LOW
MODERATE
HIGH
NEAR_DUPLICATE
UNKNOWN
~~~

Do not merge or delete TradeThesis objects during runtime comparison.

### Mutual Exclusivity / Coexistence

Candidate:

~~~text
COEXISTENT
COMPATIBLE_BUT_COMPETING
PARTIALLY_EXCLUSIVE
MUTUALLY_EXCLUSIVE
CONDITIONALLY_EXCLUSIVE
UNKNOWN
~~~

Opposing expected direction alone is not enough to automatically declare mutual exclusivity because sequence/horizon may matter.

### Pairwise Comparison

Candidate relation:

~~~text
A_DOMINATES_ON_COMPARISON_CRITERIA
B_DOMINATES_ON_COMPARISON_CRITERIA
A_PREFERRED_WITH_LIMITATIONS
B_PREFERRED_WITH_LIMITATIONS
TRADEOFF
ROUGHLY_EQUIVALENT
NO_CLEAR_PREFERENCE
NOT_COMPARABLE
~~~

DOMINATES_ON_COMPARISON_CRITERIA is not a Trade Decision.

### Comparison Frontier

Formal Candidate:

> Comparison Frontier = TradeTheses in the DecisionScope that are not clearly dominated on the active comparison criteria.

~~~text
Comparison Frontier
≠ Selected Thesis Set
~~~

### Scope-level Comparison Outcome Candidate

~~~text
CLEAR_COMPARISON_PREFERENCE
MULTIPLE_NON_DOMINATED_THESES
TRADEOFF
NO_CLEAR_PREFERENCE
ALL_ECONOMICALLY_UNFAVORABLE
ALL_COMPARISON_FRAGILE
CONDITIONAL_BRANCH
SINGLE_THESIS_SCOPE
NO_COMPARABLE_THESIS
~~~

### Process Status

~~~text
COMPLETED
COMPLETED_WITH_LIMITATIONS
PARTIAL
INCOMPLETE
STALE
INCONSISTENT
COMPARISON_FAILED
~~~

### Finalization Readiness

~~~text
READY_FOR_DECISION_FINALIZATION
READY_FOR_DECISION_FINALIZATION_WITH_LIMITATIONS
NOT_READY_FOR_DECISION_FINALIZATION
NOT_COMPARABLE
~~~

A valid NO_CLEAR_PREFERENCE can still be READY_FOR_DECISION_FINALIZATION.

### Core Invariants

~~~text
Highest EV
≠ automatic winner

Thesis count
≠ direction vote

Knowledge count
≠ direction vote

Evidence Independence
≠ Mechanism Independence

Overlap
≠ automatic merge

Dominated
≠ false

Comparison Frontier
≠ Final Selection

All Negative EV
≠ least-negative Thesis should trade

NO_CLEAR_PREFERENCE
≠ Process Failure

NO_COMPARABLE_THESIS
≠ NO_TRADE
~~~

---

## 7.82 Decision Candidate Resolution — Final Checkpoint

### Why This Contract Is Required

Final Review found a missing formal boundary:

~~~text
CrossThesisComparisonResult
↓
?
↓
DecisionResultCandidate
~~~

Without a resolver, TAKE_LONG_RISK / TAKE_SHORT_RISK / NO_TRADE could appear without a clearly owned selection process.

### Formal Definition

> Decision Candidate Resolution = the 05 internal responsibility that uses a valid CrossThesisComparisonResult and its exact Thesis / PreDecision / EV inputs under a versioned DecisionResolutionPolicy to construct a candidate Risk-taking outcome, Primary Selected Thesis, Selected Thesis Set, Non-selected Thesis Set and structured reasons, without yet creating a Canonical DecisionResult.

### Inputs

~~~text
DecisionScope
TradeThesis[]
PreDecisionThesisAssessment[]
ExpectedValueAssessment[]
CrossThesisComparisonResult
DecisionResolutionPolicy
DecisionPolicyBundleVersion
~~~

### Resolution Flow

~~~text
DCR0 Input Integrity
DCR1 Scope Integrity
DCR2 Comparison Readiness
DCR3 Economic Eligibility
DCR4 Comparison Frontier Review
DCR5 Direction Grouping
DCR6 Conflict / Opposing Thesis Review
DCR7 Selected Thesis Eligibility
DCR8 Primary Thesis Selection
DCR9 Non-selection Reason Construction
DCR10 Candidate Outcome Resolution
DCR11 Reason / Limitation Assembly
DCR12 Candidate Integrity
~~~

### Candidate Outcome

~~~text
TAKE_LONG_RISK
TAKE_SHORT_RISK
NO_TRADE
~~~

At this stage these are candidate outcomes only.

### Economic Eligibility

A Thesis that is merely better than another Thesis is not automatically economically eligible.

Example:

~~~text
T-A EV = -4 bps
T-B EV = -20 bps

T-A is relatively better
but
relative preference
≠ positive risk-taking rationale
~~~

### Selection

Risk-taking candidates may contain:

~~~text
primary_selected_thesis_ref
selected_thesis_refs[]
non_selected_thesis_refs[]
non_selection_records[]
~~~

v1 rules:

~~~text
TAKE_LONG_RISK
→ selected risk Thesis directions compatible with UPWARD

TAKE_SHORT_RISK
→ selected risk Thesis directions compatible with DOWNWARD

cross-direction Selected Thesis Set
→ prohibited in v1

multiple same-direction selected Theses
→ allowed when policy supports it

selected count
≠ confidence / strength
~~~

### Primary Selection

One Primary Thesis is required for a risk-taking candidate.

It is the central Decision rationale.

~~~text
Primary
≠ highest EV automatically
~~~

### Non-selection

A non-selected Thesis is not necessarily false or weak.

Frontier Thesis non-selection should preserve an explicit reason.

Especially when an opposing, non-dominated Thesis exists.

### Candidate NO_TRADE

Candidate NO_TRADE is valid only after normal Decision Evaluation.

Examples:

~~~text
ALL_ECONOMICALLY_UNFAVORABLE
NO_CLEAR_PREFERENCE
OPPOSING_ROBUST_THESES
EV_TOO_FRAGILE
MATERIAL_UNCERTAINTY
MATERIAL_UNQUANTIFIED_TAIL_RISK
INSUFFICIENT_ECONOMIC_ADVANTAGE
~~~

### Candidate Resolution Status

~~~text
RESOLVED
RESOLVED_WITH_LIMITATIONS
NO_CANONICAL_CANDIDATE
INCOMPLETE
INCONSISTENT
RESOLUTION_FAILED
~~~

~~~text
NO_CANONICAL_CANDIDATE
≠ NO_TRADE
~~~

### Prohibited Shortcuts

~~~text
highest EV
→ automatic selected Thesis

most Theses
→ direction vote

most Knowledge
→ direction vote

lowest uncertainty
→ automatic selection

Comparison Frontier
→ automatic selected set

Process Failure
→ NO_TRADE
~~~

### DecisionResultCandidate

Transient object candidate:

~~~text
Identity
- candidate id/version/digest
- decision cycle/scope/context
- comparison ref
- policy version
- created_at / trace

Candidate Outcome
- candidate outcome
- candidate risk direction

Selection
- primary selected Thesis
- selected Thesis refs
- non-selected Thesis refs
- non-selection records

Reasons
- structured reason records
- primary reason codes

Economic / Conflict Context
- EV refs
- comparison frontier
- conflict refs
- invalidation context
- uncertainty
- limitations
~~~

DecisionResultCandidate has no Defense or Execution authority.

---

## 7.83 Decision Result Finalization / Integrity Gate — Final Checkpoint

### Formal Responsibility

Finalization answers:

> Can this exact DecisionResultCandidate still be frozen now as a Canonical DecisionResult?

It does not decide which direction is better.

### Boundary

~~~text
Decision Candidate Resolution
↓
DecisionResultCandidate
↓
Decision Result Finalization / Integrity Gate
↓
DecisionFinalizationDecision
↓
FINALIZE_ALLOWED*
↓
DecisionResult Writer
~~~

### Finalization Flow

~~~text
DRF0 Candidate Identity
DRF1 Input Chain Integrity
DRF2 Scope Integrity
DRF3 Thesis Selection Integrity
DRF4 PreDecision Assessment Integrity
DRF5 EV Integrity
DRF6 Comparison Integrity
DRF7 Outcome / Direction Consistency
DRF8 Multi-Thesis Selection Integrity
DRF9 Contradiction / Frontier Integrity
DRF10 Decision Context Freshness
DRF11 Thesis Validity / Expiry
DRF12 EV Validity Envelope
DRF13 Runtime Data / Market Freshness
DRF14 Post-Snapshot Material Event
DRF15 Uncertainty / Limitation Preservation
DRF16 Policy / Logic Version Integrity
DRF17 Trace Completeness
DRF18 Authority Boundary
DRF19 Concurrency / TOCTOU
DRF20 Final Resolution
~~~

### Exact Chain

~~~text
DecisionResultCandidate
→ CrossThesisComparisonResult
→ ExpectedValueAssessment
→ PreDecisionThesisAssessment
→ TradeThesis
→ DecisionScope
→ DecisionContextSnapshot
~~~

All refs/versions must resolve exactly.

### Digest Chain

Candidate:

~~~text
DecisionContext digest
IntegratedKnowledgeContext digest
TradeThesis digest
PreDecisionThesisAssessment digest
ExpectedValueAssessment digest
CrossThesisComparisonResult digest
DecisionResultCandidate digest
~~~

Digest match means unchanged, not correct.

### Scope

One Canonical DecisionResult belongs to one DecisionScope.

Do not mix multiple scopes into one DecisionResult.

### Candidate Integrity

Finalization validates that:

~~~text
Selected Thesis belongs to Scope
Selected Thesis was evaluated
EV refs match selected Thesis
Comparison included the Thesis
Outcome direction matches selected Thesis directions
Frontier opposition was not silently deleted
Non-selection reasons are present where required
limitations are preserved
~~~

Finalization does not pick a replacement Thesis.

### Freshness

Thresholds are policy/horizon-specific.

Candidate states may include:

~~~text
FRESH
WITHIN_TOLERANCE
NEAR_EXPIRY
STALE
UNKNOWN
~~~

~~~text
STALE
≠ NO_TRADE
~~~

### Material Change Barrier

Finalization checks the interval:

~~~text
DecisionContextSnapshot market watermark
→ Finalization market watermark
~~~

Decision-material change requires a refreshed Decision Cycle rather than silently finalizing an old candidate.

### EV Validity Envelope Recheck

If a currently observable economic assumption is already outside the EV envelope:

~~~text
→ EV_REASSESSMENT_REQUIRED
~~~

Do not recalculate EV inside Finalization.

### Policy Bundle Integrity

A DecisionCycle should bind one:

~~~text
DecisionPolicyBundleVersion
~~~

and should not silently mix hot-reloaded policy versions inside the same cycle.

### Concurrency / TOCTOU

Finalization should bind:

~~~text
candidate digest
context digest
comparison digest
market watermark
policy bundle version
~~~

The Canonical Writer must not use a FinalizationDecision after these bindings have materially changed.

### Finalization Outcomes

~~~text
FINALIZE_ALLOWED
FINALIZE_ALLOWED_WITH_LIMITATIONS
REFRESH_CONTEXT_REQUIRED
THESIS_REASSESSMENT_REQUIRED
EV_REASSESSMENT_REQUIRED
RECOMPARE_REQUIRED
CANDIDATE_CORRECTION_REQUIRED
FINALIZATION_BLOCKED
FINALIZATION_FAILED
~~~

Only FINALIZE_ALLOWED* may create a Canonical DecisionResult.

### Mandatory Route Candidate

~~~text
FINALIZE_ALLOWED*
→ DECISION_RESULT_WRITER

REFRESH_CONTEXT_REQUIRED
→ NEW_DECISION_CYCLE

THESIS_REASSESSMENT_REQUIRED
→ PREDECISION_ASSESSMENT

EV_REASSESSMENT_REQUIRED
→ EXPECTED_VALUE_ASSESSMENT

RECOMPARE_REQUIRED
→ CROSS_THESIS_COMPARISON

CANDIDATE_CORRECTION_REQUIRED
→ DECISION_CANDIDATE_RESOLUTION

FINALIZATION_BLOCKED
→ MANUAL / SYSTEM REVIEW

FINALIZATION_FAILED
→ SYSTEM_RECOVERY
~~~

### Finalization vs Defense

~~~text
Finalization
= Is the Decision still logically/currently valid?

Defense
= Is taking this Risk safe now?
~~~

No overlap in authority.

---

## 7.84 Decision Result — Final Checkpoint

### Formal Definition

> DecisionResult = the immutable canonical 05_DECISION output for one DecisionScope, created only after normal Thesis evaluation/comparison and a successful Finalization Gate, recording whether the system currently wants Long-direction Risk, Short-direction Risk, or no new Risk, together with the exact selected/non-selected Thesis, economic context, conflict, invalidation, uncertainty, reasons, validity, policy/version and trace.

### Canonical v1 Outcomes

~~~text
TAKE_LONG_RISK
TAKE_SHORT_RISK
NO_TRADE
~~~

### Legacy Semantic Refinement

~~~text
Legacy BUY
→ TAKE_LONG_RISK

Legacy SELL
→ TAKE_SHORT_RISK

Legacy NO_TRADE
→ NO_TRADE
~~~

Reason:

~~~text
TAKE_LONG_RISK
≠ BUY Order

TAKE_SHORT_RISK
≠ SELL Order
~~~

05 expresses Risk-taking intent, not Exchange action.

### TAKE_LONG_RISK

Means:

> Under the finalized DecisionScope and policy, Long-direction Risk-taking has sufficient current decision rationale.

Does NOT mean:

~~~text
BUY now
market order
full position
max leverage
Defense approved
Execution permitted
~~~

### TAKE_SHORT_RISK

Same boundary for Short-direction Risk.

### NO_TRADE

Formal meaning:

> Valid TradeThesis material was normally evaluated through the required Decision process, and the finalized 05 judgment is that current risk-taking rationality is insufficient.

~~~text
NO_TRADE
≠ Error
≠ Failure
≠ Stale
≠ No Thesis
≠ No Scope
≠ Defense BLOCK
~~~

### Correct NO_TRADE Path

~~~text
valid evaluated Thesis exists
↓
Individual Evaluation completed
↓
EV Assessment completed
↓
Comparison / single-Thesis evaluation completed
↓
Candidate Resolution selects no new Risk
↓
Finalization passes
↓
Canonical NO_TRADE
~~~

### Decision Selection Fields

~~~text
evaluated_thesis_refs[]

primary_selected_thesis_ref

selected_thesis_refs[]

non_selected_thesis_refs[]

comparison_excluded_thesis_refs[]
~~~

Semantics:

~~~text
evaluated
= evaluated in the Decision process

selected
= directly adopted as rationale for taking Risk

non-selected
= evaluated but not directly adopted

comparison-excluded
= did not become a normal final comparison input
~~~

### Risk-taking Selection Rules

For TAKE_LONG_RISK / TAKE_SHORT_RISK:

~~~text
primary_selected_thesis_ref
= REQUIRED

selected_thesis_refs.length
>= 1

primary_selected_thesis_ref
∈ selected_thesis_refs

all selected Thesis
must belong to the same DecisionScope

all selected Thesis
must be direction-compatible with the v1 Risk outcome
~~~

Multiple selected same-direction Theses are allowed.

Their count is not a strength/confidence score.

### NO_TRADE Selection Rules

Normally:

~~~text
primary_selected_thesis_ref = null

selected_thesis_refs = []

evaluated_thesis_refs.length >= 1
~~~

All evaluated Thesis and reasons for not taking Risk remain traceable.

### Directional v1

TradeThesis may conceptually contain:

~~~text
UPWARD
DOWNWARD
NON_DIRECTIONAL
TWO_SIDED
UNRESOLVED
~~~

but v1 Risk-taking Decision only maps:

~~~text
UPWARD
→ TAKE_LONG_RISK-compatible

DOWNWARD
→ TAKE_SHORT_RISK-compatible
~~~

NON_DIRECTIONAL / TWO_SIDED / UNRESOLVED are not primary directional Risk selections in v1.

Future strategy types require a versioned outcome-registry extension.

### Decision Reasons

Do not store reasons only as prose.

Candidate structure:

~~~text
reason_code
reason_category
related_thesis_refs
related_assessment_refs
related_ev_refs
related_comparison_refs
materiality
optional human explanation
trace
~~~

Reason categories may include:

~~~text
ECONOMIC
COMPARISON
CONFLICT
INVALIDATION
APPLICABILITY
UNCERTAINTY
TAIL_RISK
COST
CONTEXT
CONDITIONAL_BRANCH
OTHER
~~~

### Non-selection Records

For evaluated but non-selected Theses preserve structured reasons.

Examples:

~~~text
ECONOMICALLY_UNFAVORABLE
LOWER_COMPARISON_PREFERENCE
HIGHER_INVALIDATION_RISK
MATERIAL_UNCERTAINTY
HIGH_EVIDENCE_OVERLAP
NEAR_DUPLICATE
OPPOSING_DIRECTION_NOT_SELECTED
PARTIAL_APPLICABILITY
DOMINATED_ON_COMPARISON_CRITERIA
CONDITIONAL_BRANCH_INACTIVE
NO_CLEAR_ADVANTAGE
~~~

Non-selected ≠ false.

### Economic Context

Reference exact:

~~~text
expected_value_assessment_refs[]
primary_selected_ev_assessment_ref when applicable
EV sign/viability projection
robustness projection
tail-risk context
cost context
EV validity envelope refs
~~~

ExpectedValueAssessment remains the Source of Truth.

Do not average EVs of multiple selected Theses into a fake combined portfolio EV.

### Conflict

Preserve:

~~~text
opposing_thesis_refs[]
cross_thesis_conflict_refs[]
unresolved_conflict_refs[]
contradiction context
conditional branch context
~~~

Selecting one Risk direction does not erase the opposing Thesis.

### Invalidation / Applicability / Uncertainty

Preserve:

~~~text
selected Thesis invalidation refs
invalidation proximity
counter-mechanism context
critical partial applicability refs
applicability limitations
decision uncertainty dimensions
dominant uncertainty sources
unquantified risks
unresolved questions
limitations
~~~

Do not require one universal confidence score.

### Validity

Candidate fields:

~~~text
finalized_at
valid_from
valid_until
decision_horizon
evaluation_window
decision_context_market_watermark
finalization_market_watermark
validity_basis
finalization_decision_ref
~~~

### Final Correction — Risk-taking valid_until

For v1:

~~~text
TAKE_LONG_RISK
TAKE_SHORT_RISK
→ valid_until REQUIRED candidate
~~~

Do not treat null as indefinite validity.

NO_TRADE may also preserve valid_until for audit/current-decision reuse, but it does not normally enter Defense.

### DecisionResult Conceptual Structure

~~~text
Identity
- id/version
- decision cycle
- DecisionScope
- DecisionContext
- candidate ref
- FinalizationDecision ref
- created_at / trace

Outcome
- TAKE_LONG_RISK / TAKE_SHORT_RISK / NO_TRADE
- risk direction LONG / SHORT / NONE
- completed process status

Evaluation Set
- evaluated Thesis
- comparison-ready Thesis
- comparison-excluded Thesis

Selection
- primary selected Thesis
- selected Thesis
- non-selected Thesis
- non-selection records

Economic
- EV refs
- economic summary projection
- robustness
- tail/cost context
- EV validity envelopes

Comparison
- CrossThesisComparison ref
- comparison outcome
- frontier
- dominated refs
- overlap
- evidence/mechanism independence

Conflict
- opposing Thesis
- unresolved conflicts
- contradiction
- conditional branches

Invalidation / Applicability
- invalidation refs/context
- critical partial applicability
- limitations

Uncertainty
- decision uncertainty
- dominant sources
- unquantified risks
- unresolved questions

Reasons
- structured reason records
- primary reason codes
- optional summary

Validity
- finalized/valid_from/valid_until
- horizon/window
- watermarks

Versions / Integrity
- policy bundle
- resolution / finalization / assessment / EV / comparison versions
- decision digest

Limitations
- decision limitations
- Finalization limitations
- diagnostics ref
~~~

### DecisionResult Writer

Single canonical writer candidate.

It:

~~~text
verifies FINALIZE_ALLOWED*
verifies exact candidate digest
creates immutable canonical ID/version
writes trace
~~~

It does NOT:

~~~text
reselect Thesis
change direction
recalculate EV
add hidden reasons
drop limitations
~~~

### Outcome Correctness Boundary

~~~text
TAKE_LONG_RISK + WIN
≠ Decision automatically correct

TAKE_SHORT_RISK + LOSS
≠ Decision automatically wrong

NO_TRADE + missed move
≠ Decision automatically wrong
~~~

Correctness is a post-decision research/evaluation problem.

---

## 7.85 DecisionCycleProcessingResult — Final Checkpoint

### Why It Is Required

Strict NO_TRADE semantics mean a DecisionCycle may validly produce zero Canonical DecisionResults.

Examples:

~~~text
0 TradeThesis
0 DecisionScope
all Thesis NOT_EVALUABLE
EV pipeline failure
context restart before Decision
~~~

These must not be mislabeled NO_TRADE.

### Formal Definition

> DecisionCycleProcessingResult = a non-market-decision orchestration/audit result that records how far one DecisionCycle progressed, which DecisionScopes were processed, which Canonical DecisionResults were created, and why any scope produced no Canonical DecisionResult.

### Boundary

~~~text
DecisionCycleProcessingResult
≠ DecisionResult
~~~

### Conceptual Structure

~~~text
decision_cycle_id
decision_context_ref

decision_scope_refs[]
decision_result_refs[]

decision_result_count

scope_processing_records[]

processing_status

restart_required

failure / no-result reason refs[]

created_at

trace_id
~~~

### Processing Status Candidate

~~~text
COMPLETED_WITH_DECISIONS
COMPLETED_WITHOUT_CANONICAL_DECISION
RESTART_REQUIRED
PARTIAL
FAILED
~~~

### Example — No Buildable Thesis

~~~text
TradeThesis count = 0

DecisionResult count = 0

DecisionCycleProcessingResult:
COMPLETED_WITHOUT_CANONICAL_DECISION

reason:
NO_BUILDABLE_TRADE_THESIS
~~~

This is not NO_TRADE.

### Example — Multiple Scopes

~~~text
DS-1
→ TAKE_LONG_RISK

DS-2
→ NO_TRADE

DecisionCycleProcessingResult:
COMPLETED_WITH_DECISIONS

decision_result_refs:
DR-1
DR-2
~~~

### Purpose

This object prevents process state from contaminating market Decision outcome semantics.

---

## 7.86 05 → Defense Handoff — Final Checkpoint

### Formal Responsibility

The Handoff transfers a finalized Canonical DecisionResult into the Defense domain without letting Defense redo 05.

~~~text
DecisionResult
↓
Defense Handoff Builder
↓
DefenseAdmissionEnvelope
↓
Defense Admission Gate
↓
DefenseAdmissionDecision
↓
Defense Evaluation
~~~

### Outcome Routing

~~~text
TAKE_LONG_RISK
TAKE_SHORT_RISK
→ Defense Admission candidate

NO_TRADE
→ DEFENSE_NOT_REQUIRED
→ Logger / Audit / Research Trace
~~~

NO_TRADE is a Canonical Decision but does not request new Risk.

### DefenseAdmissionEnvelope

Formal Candidate:

> An immutable transfer projection of the exact Canonical DecisionResult containing the minimum identity, scope, selected-Thesis, economic validity, validity-window, limitation, uncertainty and trace information required by Defense.

~~~text
DecisionResult
= Source of Truth

DefenseAdmissionEnvelope
= Transfer Projection
~~~

Do not deep-copy all Knowledge/Research.

### Minimum Envelope Context

~~~text
Identity
- handoff id/version
- DecisionResult exact ref/version/digest
- decision cycle/scope/context
- FinalizationDecision ref
- created_at / trace

Decision
- decision outcome
- risk direction
- reason refs

Selection
- primary selected Thesis
- selected Thesis exact refs/versions
- opposing Thesis refs
- comparison ref

Economic Validity
- EV Assessment refs
- primary selected EV ref
- EV Validity Envelope refs
- economic/cost assumption refs
- economic limitations

Scope
- asset
- market
- instrument
- venue scope
- decision horizon
- evaluation window

Validity
- finalized_at
- valid_from
- valid_until
- validity basis
- DecisionContext watermark
- Finalization watermark

Upstream Limitations
- decision limitations
- finalization limitations
- uncertainty refs
- unquantified risks
- invalidation refs
- applicability limitations

Versions / Integrity
- policy bundle
- EV/comparison/finalization/handoff versions
- envelope digest
~~~

### Defense Admission Gate

~~~text
DHA0 Handoff Identity
DHA1 Outcome Routing
DHA2 Canonical Decision / Finalization
DHA3 Version / Digest Integrity
DHA4 Decision Scope Integrity
DHA5 Decision Validity Window
DHA6 Selected Thesis Integrity
DHA7 Selected Thesis Validity
DHA8 EV Assessment Integrity
DHA9 EV Validity Envelope
DHA10 Limitation / Uncertainty Preservation
DHA11 Post-Finalization Material Change
DHA12 Policy / Contract Version
DHA13 Trace Completeness
DHA14 Authority Boundary
DHA15 Concurrency / Final Resolution
~~~

### Decision Digest

Digest mismatch does not trigger silent latest-object replacement.

Candidate result:

~~~text
HANDOFF_REJECTED
reason:
DECISION_DIGEST_MISMATCH
~~~

### Decision Validity

Admission verifies:

~~~text
valid_from <= now < valid_until
~~~

for time-bounded risk decisions.

Expired:

~~~text
→ DECISION_REFRESH_REQUIRED
~~~

Expired ≠ Defense BLOCK.

### Selected Thesis

Admission verifies identity/integrity only:

~~~text
primary exists for TAKE_*
primary ∈ selected
selected exact versions resolve
selected belong to DecisionScope
selected are direction-compatible
selected Thesis is not expired under its validity contract
~~~

Defense does NOT re-evaluate:

~~~text
Thesis correctness
Mechanism strength
PRIMARY role assignment
Cross-Thesis winner
Direction
~~~

### EV Validity Envelope

Admission checks whether currently observable economic assumptions still remain inside the EV envelope.

Examples:

~~~text
spread
funding
venue assumption
liquidity assumption
other cost assumptions
~~~

If current economic assumptions breach the envelope:

~~~text
→ EV_REASSESSMENT_REQUIRED
~~~

Do not turn this into Defense BLOCK.

### Size Envelope

Exact final Position Size does not yet exist.

If EV is valid only up to a notional ceiling, that ceiling is passed downstream as an economic upper boundary.

Defense may be more restrictive.

Defense may not expand the economic envelope.

Conceptually:

~~~text
effective downstream envelope
<=
EV economic envelope
~~~

### Economic Validity vs Safety Validity

~~~text
Handoff / 05:
Is the economic Decision still valid?

Defense:
Is that valid Decision safe to execute now?
~~~

Example:

~~~text
EV valid at spread <= 10 bps
current spread = 7 bps
→ economic Decision still valid

Defense safety policy requires spread <= 5 bps
→ Defense may REDUCE/BLOCK
~~~

Reverse:

~~~text
EV valid only at spread <= 5 bps
current spread = 7 bps
Defense would tolerate 10 bps
→ still EV_REASSESSMENT_REQUIRED
~~~

Safety cannot make invalid economics valid.

### Limitations

Upstream limitations must survive Handoff.

Candidate classes:

~~~text
TRACE_ONLY
SAFETY_RELEVANT
DOWNSTREAM_ENFORCEABLE
~~~

But:

~~~text
Limitation
≠ Authorized Runtime Constraint
~~~

Constraint authority remains separate.

### Post-Finalization Material Change

Admission checks the interval:

~~~text
Finalization market watermark
→ Defense Admission market watermark
~~~

Event materiality may distinguish:

~~~text
DECISION_MATERIAL
SAFETY_MATERIAL
BOTH
NEITHER
~~~

Decision-material change:

~~~text
→ DECISION_REFRESH_REQUIRED
~~~

Safety-only change:

~~~text
→ continue to Defense Evaluation
→ Defense may ALLOW/REDUCE/BLOCK
~~~

### Defense Admission Outcomes

~~~text
ADMITTED_TO_DEFENSE
DEFENSE_NOT_REQUIRED
DECISION_REFRESH_REQUIRED
EV_REASSESSMENT_REQUIRED
HANDOFF_CORRECTION_REQUIRED
HANDOFF_REJECTED
HANDOFF_FAILED
~~~

~~~text
ADMITTED_TO_DEFENSE
≠ ALLOW
~~~

### Defense Must Not Re-evaluate

~~~text
Knowledge correctness
Knowledge Applicability
Trade Thesis construction
Thesis member roles
Expected Direction
Expected Effect
Expected Horizon
Mechanism correctness
Probability
Expected Return
Expected Loss
Gain-Loss Asymmetry
Expected Value
Economic Viability
Cross-Thesis ranking
Comparison Frontier
Selected Thesis
Non-selected Thesis
Decision Direction
NO_TRADE vs TAKE_RISK
~~~

### Defense May Validate / Evaluate

Admission/integrity:

~~~text
Canonical Decision?
Digest?
Expiry?
Selected refs?
EV envelope?
Limitations?
Decision-material event?
~~~

Defense safety:

~~~text
RiskState
Authorized Runtime Constraints
Exposure
Drawdown / loss context
Liquidity safety
Spread/slippage safety
Data / Runtime Quality
Exchange / API health
Position state
Abnormal safety event
Global Risk Limits
~~~

### Defense Outcome

Separate object:

~~~text
ALLOW
REDUCE
BLOCK
~~~

~~~text
BLOCK
≠ Decision wrong

REDUCE
≠ exact Position Size

ALLOW
≠ Order sent
~~~

---

## 7.87 05_DECISION — Integrated Final Review / Closure Candidate

### Review Result

The Final Review compared:

~~~text
Decision Context
Knowledge Integration
Trade Thesis
Decision Scope
PreDecision Thesis Assessment
Expected Value Assessment
Cross-Thesis Comparison
Decision Candidate Resolution
Decision Finalization
Decision Result
DecisionCycleProcessingResult
Defense Handoff
Defense boundary
~~~

against the saved Current 03 / 04 boundary and Legacy Reference material.

### Architecture Result

~~~text
ARCHITECTURE_BREAKING_CONFLICT:
NONE

RESPONSIBILITY_OVERLAP:
RESOLVED / MINOR BOUNDARY CORRECTIONS APPLIED

OBJECT_DUPLICATION:
NO MATERIAL DUPLICATION REQUIRED

STATE_COLLISION:
NO SEMANTIC COLLISION
NAMESPACED TYPES REQUIRED

BACKWARD_LOOP:
VALID
PRECEDENCE REQUIRED

TRACE_CONTINUITY:
COMPLETE CANDIDATE

NO_TRADE_SEMANTICS:
CONSISTENT

DEFENSE_BOUNDARY:
CONSISTENT AFTER VALIDITY-GATE REFINEMENT

ARCHITECTURE_REWRITE_REQUIRED:
NO
~~~

### Final Corrections

#### FINAL-CORRECTION-05-01 — Exact Decision Context per Scope

v1 direct Cross-Thesis Comparison requires:

~~~text
exact same DecisionContextSnapshot
+
exact same decision_cycle_id
~~~

not merely semantically compatible Decision Context.

#### FINAL-CORRECTION-05-02 — Namespaced Status Types

Generic words must not become one shared Enum.

Examples:

~~~text
DecisionContextAssemblyStatus.STALE

TradeThesisConstructionStatus.NOT_BUILDABLE

DecisionScopeBindingStatus.STALE

PreDecisionAssessmentProcessStatus.STALE

EVAssessmentProcessStatus.INCOMPLETE

ComparisonProcessStatus.PARTIAL

DecisionFinalizationOutcome.FINALIZATION_BLOCKED

DefenseAdmissionOutcome.HANDOFF_REJECTED

DefenseDecision.BLOCK
~~~

Critical semantic distinctions:

~~~text
BLOCKED_BY_CONSTRAINT
≠ FINALIZATION_BLOCKED
≠ HANDOFF_REJECTED
≠ DefenseDecision.BLOCK
≠ Fail-Closed
~~~

#### FINAL-CORRECTION-05-03 — Risk-taking Decision valid_until

For v1:

~~~text
TAKE_LONG_RISK
TAKE_SHORT_RISK
→ valid_until REQUIRED candidate
~~~

Null must not mean indefinite Risk-taking Decision validity.

#### FINAL-CORRECTION-05-04 — Full Decision Validity Moves to Defense Admission

Existing Defense Evaluation had a broad Decision Validity Gate.

Final refined ownership:

~~~text
Defense Admission owns:
- Canonical Decision verification
- Decision digest
- Decision validity window
- Selected Thesis ref integrity
- EV Validity Envelope
- Post-Finalization decision-material change
~~~

Defense Evaluation should narrow its old validity responsibility to a lightweight:

~~~text
Admission Snapshot Validity Recheck
~~~

between Admission and actual Defense Evaluation.

Defense does not redo full 05 validity.

#### FINAL-CORRECTION-05-05 — Three Temporal Barriers

Barrier A:

~~~text
DecisionContext Snapshot
→ Decision Finalization
~~~

Question:

> Did the market materially change while 05 was reasoning?

Barrier B:

~~~text
Decision Finalization
→ Defense Admission
~~~

Question:

> Did the finalized economic Decision become invalid before safety evaluation?

Barrier C:

~~~text
Defense Decision
→ EntryThesis / OrderIntent
~~~

Question:

> Did safety / constraint / market validity change before actual entry?

Candidate watermark chain:

~~~text
decision_context_market_watermark
finalization_market_watermark
defense_admission_market_watermark
defense_evaluation_market_watermark
entry_snapshot_market_watermark
~~~

#### FINAL-CORRECTION-05-06 — Backward Route Precedence

1. Material market/context change:

~~~text
→ NEW DECISION CYCLE
~~~

Do not partially patch an old Cycle.

2. Thesis premise/validity only changed:

~~~text
→ PreDecisionThesisAssessment
→ EV
→ Comparison
→ Candidate
→ Finalization
~~~

3. Economic assumption only changed:

~~~text
→ ExpectedValueAssessment
→ Comparison
→ Candidate
→ Finalization
~~~

4. Comparison input only changed:

~~~text
→ CrossThesisComparison
→ Candidate
→ Finalization
~~~

5. Candidate logic issue:

~~~text
→ Decision Candidate Resolution
→ Finalization
~~~

6. Handoff projection issue:

~~~text
→ Handoff Builder only
~~~

Do not mutate existing artifacts in place.

#### FINAL-CORRECTION-05-07 — DecisionPolicyBundleVersion

A DecisionCycle should freeze one Decision Policy Bundle candidate containing:

~~~text
Decision Context Policy
Knowledge Integration Policy
Trade Thesis Policy
Decision Scope Binding Policy
PreDecision Assessment Policy
Expected Value Policy
Cross-Thesis Comparison Policy
Decision Resolution Policy
Decision Finalization Policy
Defense Handoff Policy
~~~

Policy hot reload should apply to the next DecisionCycle rather than silently mixing rule versions inside the current cycle.

### Added Missing Contracts

Final Review adds:

~~~text
MAJOR-ADD-05-01
Decision Candidate Resolution

MAJOR-ADD-05-02
DecisionCycleProcessingResult
~~~

These close two semantic gaps:

~~~text
CrossThesisComparisonResult
→ who selects the candidate?

0 Canonical DecisionResult
→ how does orchestration record what happened
  without fabricating NO_TRADE?
~~~

### Object Separation Review

~~~text
DecisionContextSnapshot
= frozen input context

IntegratedKnowledgeContext
= thesis-independent knowledge structure

TradeThesis
= one composed market reasoning Thesis

DecisionScope
= comparison boundary

PreDecisionThesisAssessment
= pre-EV Thesis readiness/health

ExpectedValueAssessment
= economic expectation

CrossThesisComparisonResult
= relative comparison structure

DecisionResultCandidate
= transient candidate Decision

DecisionFinalizationDecision
= permission to canonicalize candidate now

DecisionResult
= canonical 05 market Decision

DecisionCycleProcessingResult
= outer process/audit result

DefenseAdmissionEnvelope
= transfer projection

DefenseAdmissionDecision
= boundary admission result

DefenseDecision
= runtime safety outcome
~~~

No material object is required to impersonate another.

### Value Object / Substructure Guidance

To avoid object proliferation, these do not automatically need independent canonical storage:

~~~text
Comparison Frontier
EV Validity Envelope
DecisionReasonRecord
NonSelectionRecord
ThesisOverlapProfile
ComponentOverlapMap
~~~

They may remain immutable substructures/value objects until independent identity/versioning is actually required.

### NO_TRADE Final Review

Only the normal Decision Resolution path may propose NO_TRADE.

~~~text
0 Thesis
≠ NO_TRADE

0 Scope
≠ NO_TRADE

THESIS_NOT_BUILDABLE
≠ NO_TRADE

NOT_EVALUABLE
≠ NO_TRADE

NOT_QUANTIFIABLE
≠ NO_TRADE

Comparison Failure
≠ NO_TRADE

Stale
≠ NO_TRADE

Finalization Failure
≠ NO_TRADE

Defense BLOCK
≠ NO_TRADE

Execution Failure
≠ NO_TRADE
~~~

Canonical NO_TRADE requires normal Decision evaluation and successful Finalization.

### Trace Continuity

Final candidate trace:

~~~text
DecisionResult
→ DecisionFinalizationDecision
→ DecisionResultCandidate
→ CrossThesisComparisonResult
→ ExpectedValueAssessment
→ PreDecisionThesisAssessment
→ DecisionScope
→ TradeThesis
→ IntegratedKnowledgeContext
→ DecisionContextSnapshot
→ ApplicableKnowledgeSet
→ ApplicableKnowledgeEntry
→ ApplicabilityAssessment
→ KnowledgeRecord
→ Validated Research Result boundary
→ ResearchSynthesisAssessment
→ ResearchResult
→ ResearchTrial
→ ResearchPlan
→ ResearchCandidate
→ Finding / Source
~~~

Defense:

~~~text
DefenseAdmissionEnvelope
→ DecisionResult

DefenseAdmissionDecision
→ DefenseEvaluationResult
→ DefenseDecision
→ EntryThesis
→ OrderIntent
~~~

Post-Trade can therefore trace:

~~~text
TradeResult
→ EntryThesis
→ DefenseDecision
→ DecisionResult
→ TradeThesis
→ Knowledge
→ Research
~~~

### 05 / Defense Responsibility Boundary

~~~text
05:
Do we want to take this Risk?

Defense Admission:
Is that finalized economic Decision still admissible for safety evaluation?

Defense Evaluation:
Is taking that Risk safe now?

Execution:
How exactly will the permitted Risk be entered?
~~~

Defense must not change:

~~~text
Direction
Selected Thesis
Expected Value
Knowledge Applicability
Trade Thesis composition
~~~

Defense may:

~~~text
ALLOW
REDUCE
BLOCK
~~~

based on Runtime Safety Context.

### Economic vs Safety Validity

~~~text
EV envelope breach
→ EV_REASSESSMENT_REQUIRED

RiskState / Authorized Constraint / Safety problem
→ Defense REDUCE / BLOCK
~~~

Defense may be stricter than 05 economics.

Defense may not make invalid economics valid.

### Research Feedback Boundary

05 runtime does not synchronously wait for Research.

Unexpected issues become Findings:

~~~text
unexpected contradiction
missing EV distribution
unknown dependency
repeated NO_TRADE
frequent stale Finalization
decision latency failure
Defense BLOCK pattern
missed opportunity
~~~

Then:

~~~text
Finding
↓
ResearchCandidate
↓
03_RESEARCH
~~~

No direct Knowledge mutation.

### Completion Gate — Responsibility

~~~text
□ Decision Context freezes only
□ Knowledge Integration structures only
□ Trade Thesis composes only
□ Scope Binding groups comparables only
□ PreDecision Assessment evaluates Thesis readiness only
□ EV Assessment owns economics only
□ Cross-Thesis Comparison compares only
□ Candidate Resolution selects candidate only
□ Finalization checks integrity/current validity only
□ DecisionResult owns canonical 05 outcome only
□ DecisionCycleProcessingResult owns non-decision process outcome only
□ Handoff transfers only
□ Defense Admission validates boundary only
□ Defense Evaluation owns safety only
~~~

### Completion Gate — Decision Semantics

~~~text
□ TAKE_LONG_RISK defined
□ TAKE_SHORT_RISK defined
□ NO_TRADE strictly defined
□ BUY/SELL separated from Decision intent
□ Selected / Non-selected / Evaluated separated
□ Primary Selected Thesis defined
□ Multiple same-direction selected Thesis allowed without vote inflation
□ Opposing Thesis remains traceable
□ EV remains traceable
□ Conflict remains traceable
□ Invalidation remains traceable
□ Uncertainty remains traceable
□ valid_until / watermark semantics defined
~~~

### Completion Gate — Failure Semantics

~~~text
□ Process Failure never becomes NO_TRADE
□ Stale never becomes NO_TRADE
□ 0 Thesis never becomes NO_TRADE
□ 0 DecisionResult is representable
□ Defense BLOCK remains separate
□ Fail-Closed remains separate
□ Backward routes are explicit
□ Material context change starts a new DecisionCycle
~~~

### Completion Gate — Version / Time

~~~text
□ exact versions bind each object
□ digest chain candidate defined
□ policy bundle candidate defined
□ Finalization temporal barrier defined
□ Defense Admission temporal barrier defined
□ Execution temporal barrier remains downstream
□ Risk-taking valid_until enforced
□ EV Validity Envelope preserved
~~~

### Final 05 High-Level Pipeline

~~~text
INPUT_READY
↓
CONTEXT_FROZEN
↓
KNOWLEDGE_INTEGRATED
↓
THESIS_CONSTRUCTED
↓
SCOPES_BOUND
↓
THESES_ASSESSED
↓
EV_ASSESSED
↓
THESES_COMPARED
↓
CANDIDATE_RESOLVED
↓
FINALIZATION_PASSED
↓
DECISION_FINALIZED
↓
HANDED_OFF
~~~

This is a conceptual pipeline, not one universal state Enum.

### Final Authority Chain

~~~text
Knowledge
↓
Applicability

↓
05 Decision Reasoning

↓
DecisionResult
"Want Risk?"

↓
DefenseAdmission
"Is the Decision still admissible?"

↓
DefenseDecision
"Safe?"

↓
EntryThesis
"Entry-time frozen rationale / safety snapshot"

↓
OrderIntent
"How to execute?"
~~~

### Final Closure Status

~~~text
05_DECISION_REFERENCE_DESIGN:
SEMANTICALLY_CLOSED_CANDIDATE

05_FINAL_REVIEW:
PASSED_WITH_CORRECTIONS_APPLIED

ARCHITECTURE_REWRITE_REQUIRED:
NO

CURRENT_03_CONFLICT_STATUS:
MINOR TERMINOLOGY RECONCILIATION REMAINS

CURRENT_04_CONFLICT_STATUS:
NO NEW BLOCKING CONFLICT

DEFENSE_BOUNDARY_STATUS:
REFINED / CONSISTENT

LEGACY_CONFLICT_STATUS:
MINOR / MULTI-THESIS AND AUTHORITY REFINEMENT

REVIEW_STAGE:
FINAL_CHECKPOINT

CURRENT_DESIGN_STATUS:
NOT_ADOPTED
~~~

### What This Closure Does NOT Mean

~~~text
NOT Current Design adoption

NOT final DB schema

NOT final Python class design

NOT final threshold selection

NOT final EV formula

NOT final Defense policy

NOT final Execution specification
~~~

Those require separate Current adoption / contract / implementation work.


# 8. FIX / Failure Index

FIX履歴を、単なるGit履歴ではなく再利用可能なFailure Knowledgeとして索引化する。

| FIX | Target | Problem | Separation / Change | Current Relevance |
|---|---|---|---|---|
| FIX-001 | Observation | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-002 | Hypothesis / Production State | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-003 | Research Plan State | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-004 | Edge / Knowledge State | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-005 | Object Naming | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-006 | Feature / Priority / DNA Cycle | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-007 | Market Event Responsibility | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-008 | Production Thesis Builder | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-009 | Entry / Production Evidence | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-010 | State Transition Event | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-011 | Research Plan Two-Axis State | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-012 | Lifecycle / Aging / Production Separation | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-013 | State Authority Matrix | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-014 | Source Metadata / Lifecycle Separation | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-015 | Approval Decision | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-016 | Production / Risk Stage Separation | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-017 | Knowledge Lifecycle | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-018A | Security / Identity / Authorization | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-018B | Credential Governance | `<TODO>` | `<TODO>` | `<TODO>` |
| FIX-018C | Data Classification | `<TODO>` | `<TODO>` | `<TODO>` |

詳細全文をここへ複製しない。

必要なら、

```text
Concept Review
または
Legacy Original Source
```

へ戻る。

---

# 9. Important Legacy Design Lessons

複数Concept / FIXから共通して確認できるLegacy上の学びを整理する。

重要:

```text
Legacy Lesson
≠ Current Design Principle
```

## LEGACY-LESSON-<N>

### Evidence

```text
<TODO>
```

### Lesson

```text
<TODO>
```

### Current Relevance

```text
<TODO / UNKNOWN>
```

### Source Pointer

```text
<TODO>
```

---

# 10. Legacy Revisit Index

現在は確定しないが、将来特定のCurrent Designを作る際に再確認価値があるLegacy Conceptを索引化する。

これは、

```text
Project Pending
Current Task
Next Action
```

ではない。

| Legacy Concept | Why Revisit | Conflict | Recommendation | Review Trigger |
|---|---|---|---|---|
| `<Concept>` | `<Reason>` | UNKNOWN | UNDECIDED | `<When Current Design reaches ...>` |

ここには、

```text
期限
担当者
優先順位
Project Next Action
```

を持たせない。

ProjectのPendingは `AI_CONTEXT.md` の責任。

---

# 11. Unknown / Unresolved

旧Sourceを確認しても確定できなかった内容を残す。

## LEGACY-UNKNOWN-<N>

```text
Question:
<TODO>

Why Unknown:
<TODO>

Checked Sources:
<TODO>

Additional Source Required:
<TODO>
```

分からない部分をGPTの一般知識でLegacy Definitionとして補完しない。

---

# 12. Source Pointer Index

ConceptからOriginal Sourceへ戻れるようにする。

| Source | LEGACY_SOURCE_CLASS | SOURCE_REVIEW_STATUS | Main Knowledge |
|---|---|---|---|
| `市場理解OS まとめ案 1.md` | LEGACY_SUMMARY | REVIEWED | Legacy全体像 / Domain構成 |
| `市場理解OS まとめ案 2.md` | LEGACY_SUMMARY | REVIEWED | Outer / Control / Connection |
| `市場理解OS まとめ案 3.md` | LEGACY_SUMMARY | REVIEWED | Market Understanding Core |
| `市場理解OS まとめ案 4.md` | LEGACY_SUMMARY | REVIEWED | Causal / Market DNA / Knowledge |
| `市場理解OS まとめ案 5.md` | LEGACY_SUMMARY | REVIEWED | Research / Experimental / Validation |
| `市場理解OS まとめ案 6.md` | LEGACY_SUMMARY | REVIEWED | Production / Trading |
| `市場理解OS まとめ案 7.md` | LEGACY_SUMMARY | REVIEWED | Post-Trade / Feedback / Trace |
| `市場理解OS まとめ案 8.md` | LEGACY_SUMMARY | REVIEWED | Python Runtime / Operations / Telegram |
| `市場理解OS まとめ案 9.md` | LEGACY_SUMMARY | REVIEWED | 固定候補 / 未解決TODO / Formal Design Checklist |
| `市場理解OS まとめ案 10.md` | LEGACY_SUMMARY | REVIEWED | Research Evidence Ladder / Multi-Hypothesis Trade Thesis |
| `市場理解OS まとめ案 11.md` | LEGACY_SUMMARY | REVIEWED | Long-term Governance / Plane / Knowledge Spine |
| `01_DICTIONARY/OBJECT_DICTIONARY.md` | LEGACY_ORIGINAL | NOT_REVIEWED | Object / Concept |
| `01_DICTIONARY/ROLE_DICTIONARY.md` | LEGACY_ORIGINAL | NOT_REVIEWED | Role |
| `01_DICTIONARY/STATE_DICTIONARY.md` | LEGACY_ORIGINAL | NOT_REVIEWED | State / Lifecycle |
| `01_DICTIONARY/SECURITY_DICTIONARY.md` | LEGACY_ORIGINAL | NOT_REVIEWED | Security |
| `01_DICTIONARY/CREDENTIAL_DICTIONARY.md` | LEGACY_ORIGINAL | NOT_REVIEWED | Credential |
| `01_DICTIONARY/DATA_CLASSIFICATION_DICTIONARY.md` | LEGACY_ORIGINAL | NOT_REVIEWED | Data Classification |
| `00_GOVERNANCE/DESIGN_CHANGE_RULES.md` | LEGACY_ORIGINAL | NOT_REVIEWED | Governance |
| `00_GOVERNANCE/GIT_RULES.md` | LEGACY_ORIGINAL | NOT_REVIEWED | Legacy Git Governance |
| `99_ARCHIVE/BACKUP/*` | LEGACY_BACKUP | NOT_REVIEWED | FIX / Failure Context |

---

# 13. Maintenance / Scalability Rule

このReferenceは、

```text
Master Index
+
Compressed Summary
+
Important Concept Reviews
```

として維持する。

原則:

```text
旧市場理解OS_設計知識リファレンス.md
≠
旧Repo全文コピー

旧市場理解OS_設計知識リファレンス.md
≠
全Concept詳細辞書
```

同一Domainの詳細Conceptが増え、

```text
可読性低下
検索性低下
同一Conceptの重複
Concept Reviewが大量化
```

した場合のみ、専用Reference Fileへの分割を検討する。

例:

```text
旧市場理解OS_研究知識リファレンス.md
旧市場理解OS_State知識リファレンス.md
```

ただし、

> **将来必要になりそうという理由だけで先にFileを作らない。**

新規Fileが必要になった時点で、

```text
00_AI/AI_WORKFLOW.md
↓
Save Destination Resolution
```

に従って判断する。

分割後も、このFileをLegacy KnowledgeのMaster Indexとして残す。

---

# 14. Reference Completion State

このReference全体の進捗を、Source Reviewとは別に管理する。

```text
REFERENCE_BUILD_STATE:
LEGACY_REVIEW_IN_PROGRESS
```

候補:

```text
SKELETON
SUMMARY_IN_PROGRESS
CONCEPT_INDEX_IN_PROGRESS
LEGACY_REVIEW_IN_PROGRESS
INITIAL_REFERENCE_COMPLETE
MAINTENANCE
```

## INITIAL_REFERENCE_COMPLETE の最低条件

```text
まとめ案1〜11の全体像Review済み

Dictionary群から主要Conceptを索引化済み

FIX-001〜018Cを索引化済み

主要ConceptにSource Pointerあり

Legacy → Current Concept Mapあり

重大Conflict候補を識別済み

UnknownをUnknownとして保持

Legacy DefinitionとCurrent Definitionを融合していない

ReferenceからCurrent Designへ直接昇格していない
```

全Legacy情報を完全転記することはCompletion条件ではない。

---

# Reference Usage

Concept Reviewの判定基準、Conflict、Reuse Recommendation、Currentへの昇格Rule等は、

```text
99_REFERENCE/README.md
```

を正本とする。

この文書は、

> **Policyを定義する場所ではなく、Policyを使った結果を蓄積する場所**

とする。

---

# 一文定義

> **`旧市場理解OS_設計知識リファレンス.md` とは、旧市場理解OS RepositoryのSummary・Dictionary・Governance・FIX / Failureから重要KnowledgeをSource追跡可能な形で圧縮・索引化し、Legacy DefinitionとCurrent Designを混合せず、旧Concept・失敗理由・Currentとの関係・再利用候補を検索できるようにする、Current Design Authorityを持たないLegacy Knowledge Master Indexである。**


---

## 7.88 Defense / Risk Post-05 Reconciliation — Checkpoint Scope

### Purpose

This checkpoint reconciles the previously saved Defense / Risk / Execution-boundary Reference (7.28–7.40) with the later 05_DECISION Final Checkpoint (7.86–7.87).

It is intentionally a Reference-only correction checkpoint.

~~~text
CURRENT_DESIGN_STATUS:
NOT_ADOPTED

REFERENCE_STAGE:
POST_05_DEFENSE_RECONCILIATION

ARCHITECTURE_REWRITE_REQUIRED:
NO

REFERENCE_LOCAL_PRECEDENCE:
Where 7.28–7.40 conflicts with 7.88+,
7.88+ is the newer Reference interpretation only.
This does NOT create Current Design authority.
~~~

### Major Review Result

No architecture-breaking contradiction was found.

The following older Reference responsibility is refined:

~~~text
OLD:
05 Decision
↓
Defense Evaluation
├ broad Decision Validity
└ Runtime Safety

REFINED:
05 Decision
↓
Defense Handoff
↓
Defense Admission
= full economic-decision admissibility / integrity boundary
↓
Defense Evaluation
= runtime safety only
~~~

### Critical Semantic Separation

~~~text
05_DECISION
= Do we want to take this Risk?

Defense Admission
= Is this finalized economic Decision still admissible
  for runtime safety evaluation?

Defense Evaluation
= Is taking this still-valid Risk safe now?

Execution
= How exactly will the permitted Risk be entered?
~~~

### Saving Principle

This checkpoint intentionally does NOT finalize:

~~~text
DB schema
Python classes
numeric thresholds
EV formula
Defense threshold values
IAM implementation
exact cooldown duration
exact execution retry policy
~~~

Those remain later Current adoption / contract / implementation work.

---

## 7.89 Defense Admission — Object / Responsibility Contract Checkpoint

### Formal Responsibility

> **Defense Admission = a boundary-validation responsibility that receives the exact finalized Canonical DecisionResult through a DefenseAdmissionEnvelope, does not re-run 05 economics, and verifies identity, integrity, version, validity, selected-Thesis references, EV validity envelope, post-finalization material change, limitations and trace before allowing runtime Defense Evaluation.**

~~~text
DecisionResult
↓
Defense Handoff Builder
↓
DefenseAdmissionEnvelope
↓
Defense Admission
↓
DefenseAdmissionDecision
↓
Defense Evaluation
~~~

### Handoff Routing Correction

~~~text
TAKE_LONG_RISK
TAKE_SHORT_RISK
→ Defense Admission

NO_TRADE
→ DEFENSE_NOT_REQUIRED
→ Audit / Logger / Research Trace
~~~

Correction:

~~~text
DEFENSE_NOT_REQUIRED
= Handoff routing outcome
≠ Defense Admission outcome
~~~

### DefenseAdmissionEnvelope

~~~text
DecisionResult
= Source of Truth

DefenseAdmissionEnvelope
= immutable transfer projection
≠ deep copy of Knowledge / Research / full Decision internals
~~~

Minimum conceptual groups:

~~~text
Identity
Source Binding
Decision Projection
Selection Projection
Economic Validity Projection
Scope
Temporal Validity
Upstream Limitations
Policy / Version Binding
Integrity / Trace
~~~

Core bindings:

~~~text
decision_result_ref
decision_result_version
decision_result_digest

decision_cycle_id
decision_scope_ref
decision_context_ref
decision_finalization_decision_ref

primary_selected_thesis_ref
selected_thesis_refs[]
opposing_thesis_refs[]
cross_thesis_comparison_ref

expected_value_assessment_refs[]
primary_selected_ev_assessment_ref
ev_validity_envelope_refs[]

finalized_at
valid_from
valid_until
decision_context_market_watermark
finalization_market_watermark

decision_policy_bundle_version
handoff_contract_version
envelope_schema_version
envelope_digest
~~~

### Projection Rule

~~~text
EconomicValidityProjection
= minimum runtime-checkable projection of already-finalized EV conditions

EconomicValidityProjection
≠ ExpectedValueAssessment
≠ EV recalculation
~~~

Candidate projected conditions may include:

~~~text
spread bound
funding bound
liquidity assumption
venue assumption
cost assumption
economic notional ceiling
~~~

### Limitation Rule

~~~text
TRACE_ONLY
SAFETY_RELEVANT
DOWNSTREAM_ENFORCEABLE
~~~

may be preserved as limitation classes, but:

~~~text
Limitation
≠ Authorized Runtime Constraint
~~~

### DefenseAdmissionProcessStatus

Candidate:

~~~text
COMPLETED
COMPLETED_WITH_LIMITATIONS
INCOMPLETE
FAILED
NOT_EVALUATED
~~~

### DefenseAdmissionOutcome

Candidate:

~~~text
ADMITTED_TO_DEFENSE
DECISION_REFRESH_REQUIRED
EV_REASSESSMENT_REQUIRED
HANDOFF_CORRECTION_REQUIRED
HANDOFF_REJECTED
~~~

Correction:

~~~text
HANDOFF_FAILED
≠ normal Admission outcome

processing failure
→ process status INCOMPLETE / FAILED
→ no fabricated Admission outcome
~~~

### Outcome Meaning

~~~text
ADMITTED_TO_DEFENSE
≠ Defense ALLOW

DECISION_REFRESH_REQUIRED
= Decision validity / premise materially changed

EV_REASSESSMENT_REQUIRED
= economic assumptions breached EV validity envelope

HANDOFF_CORRECTION_REQUIRED
= Canonical Decision is valid but transfer projection is defective

HANDOFF_REJECTED
= Canonical / integrity / authority boundary cannot be trusted
~~~

---

## 7.90 Defense Admission Gate Contract — Checkpoint

### Gate Set

~~~text
DHA0  Handoff Identity
DHA1  Outcome Routing
DHA2  Canonical Decision / Finalization
DHA3  Version / Digest Integrity
DHA4  Decision Scope Integrity
DHA5  Decision Validity Window
DHA6  Selected Thesis Integrity
DHA7  Selected Thesis Validity
DHA8  EV Assessment Integrity
DHA9  EV Validity Envelope
DHA10 Limitation / Uncertainty Preservation
DHA11 Post-Finalization Material Change
DHA12 Policy / Contract Version
DHA13 Trace Completeness
DHA14 Authority Boundary
DHA15 Concurrency / Final Resolution
~~~

### Gate Record Candidate

Keep gate details as immutable substructure first, not automatically a canonical top-level object.

~~~text
gate_code
gate_status
checked_refs[]
observed_values[]
expected_conditions[]
reason_codes[]
required_route
limitations[]
evaluated_at
market_watermark
diagnostics_ref
~~~

Gate status candidate:

~~~text
PASS
PASS_WITH_LIMITATION
NOT_APPLICABLE
FAIL
ERROR
~~~

### Critical Routing Rules

~~~text
Canonical / source integrity failure
→ HANDOFF_REJECTED

Envelope projection defect only
→ HANDOFF_CORRECTION_REQUIRED

Decision expired / superseded / premise invalidated
→ DECISION_REFRESH_REQUIRED

EV economic assumption breach only
→ EV_REASSESSMENT_REQUIRED

Safety-only material change
→ ADMITTED_TO_DEFENSE
  + safety change refs forwarded

Processing failure / unavailable critical validation data
→ INCOMPLETE / FAILED
  + no Admission outcome
  + no progression to Defense Evaluation
~~~

### Exact-Version Rule

~~~text
Digest mismatch
≠ silently load latest object

Superseded Decision
≠ silently replace with newer Decision
~~~

A new canonical artifact must enter through its own normal handoff path.

### Temporal Barrier B

~~~text
finalization_market_watermark
↓
defense_admission_market_watermark
~~~

Materiality candidate:

~~~text
DECISION_MATERIAL
SAFETY_MATERIAL
BOTH
NEITHER
~~~

Routing:

~~~text
DECISION_MATERIAL
→ DECISION_REFRESH_REQUIRED

BOTH
→ DECISION_REFRESH_REQUIRED

SAFETY_MATERIAL
→ ADMITTED_TO_DEFENSE
  + forward safety change context

NEITHER
→ normal admission
~~~

### Repair-Owner Principle

> **Route a defect to the earliest authoritative owner that can correctly repair that defect; do not restart the entire pipeline without need.**

Examples:

~~~text
Envelope projection defect
→ Handoff Builder

Economic assumption breach
→ EV Assessment onward

Decision-material market change
→ new Decision Cycle

Safety-only change
→ Defense Evaluation
~~~

---

## 7.91 Defense Evaluation — Refined Runtime Safety Contract

### Responsibility Correction

The broad Decision Validity responsibility in the earlier 7.29 Reference is moved to Defense Admission.

Defense Evaluation now owns:

> **runtime safety evaluation of an already-admitted economic Decision.**

### Refined Gate Set

~~~text
DE0  Admission Snapshot Validity Recheck
DE1  RiskState
DE2  Authorized Constraint
DE3  Exposure / Capacity
DE4  Liquidity / Execution Safety
DE5  Drawdown / Loss Context
DE6  Data / Runtime Quality
DE7  Exchange / API Health
DE8  Position / Account State
DE9  Abnormal Event / Global Risk Limit
DE10 Evaluation Integrity / Final Resolution
~~~

### DE0 Boundary

~~~text
DE0
= lightweight Admission Snapshot validity recheck
≠ full Decision validity evaluation
≠ EV recalculation
≠ Thesis rebuild
≠ Knowledge applicability review
~~~

If the Admission snapshot is no longer usable:

~~~text
→ no DefenseDecision
→ Defense Admission recheck / upstream route
~~~

### Known Unsafe vs Unable To Evaluate

Critical separation:

~~~text
Known unsafe state
→ normal Defense safety outcome may be BLOCK / REDUCE

Unable to evaluate required safety state
→ Process INCOMPLETE / FAILED
→ no fabricated DefenseDecision
→ Fail-Closed
~~~

Examples:

~~~text
Known ExchangeHealth = CRITICAL
→ BLOCK candidate

ExchangeHealth service unavailable
→ INCOMPLETE / FAILED
→ Fail-Closed
~~~

### Gate Outcome Candidate

~~~text
CLEAR
RESTRICT
BLOCK
UNKNOWN
NOT_EVALUATED
~~~

Hard BLOCK is never majority-voted away.

### DefenseEvaluationProcessStatus

Candidate:

~~~text
COMPLETED
COMPLETED_WITH_LIMITATIONS
INCOMPLETE
FAILED
NOT_EVALUATED
~~~

Generic STALE is not retained as one process status in this refined checkpoint.

Instead:

~~~text
Admission stale
→ Admission recheck

Evaluation context stale
→ Defense Evaluation restart

DefenseDecision expired
→ downstream rejects reuse
~~~

### DefenseDecision Creation Rule

~~~text
DefenseDecision exists
ONLY IF

process status =
COMPLETED
or COMPLETED_WITH_LIMITATIONS

AND

all required hard gates were evaluated

AND

no unresolved critical UNKNOWN remains

AND

final resolution succeeded
~~~

---

## 7.92 DefenseDecision / DefenseEvaluationResult — Refined Object Checkpoint

### DefenseDecision

Canonical outcomes remain:

~~~text
ALLOW
REDUCE
BLOCK
~~~

Semantics:

~~~text
ALLOW
= current runtime safety context permits normal Defense-envelope progression
≠ order sent

REDUCE
= economic direction remains intact,
  but only a stricter DefenseRestrictionContext may proceed
≠ exact position size

BLOCK
= Defense Evaluation completed normally,
  but current safety context prohibits new Risk progression
≠ Decision wrong
≠ NO_TRADE
≠ process failure
~~~

### DefenseRestrictionContext

Keep as an immutable substructure first.

Candidate dimensions:

~~~text
scope refs
RiskState ceiling refs
Authorized Constraint refs

max incremental exposure
max notional
max risk budget
max leverage if applicable

venue restrictions
order-style restrictions
liquidity restrictions
required protection conditions
time validity

reason codes
limitations
~~~

Critical correction:

~~~text
REDUCE
≠ one universal scalar reduction factor
~~~

Risk restriction is multi-dimensional.

### DefenseDecision Validity

Strong candidate:

~~~text
ALLOW
REDUCE
→ valid_until REQUIRED
~~~

Runtime safety permission must not be indefinitely reusable.

Candidate validity context:

~~~text
evaluated_at
valid_from
valid_until
validity_basis
defense_evaluation_market_watermark
~~~

### DefenseEvaluationResult

Conceptual groups:

~~~text
Identity
Input Binding
Processing
Gate Results
Decision Ref
Fail-Closed
Execution Projection
Routing
Temporal
Policy / Version
Trace / Diagnostics
~~~

### execution_disposition

Derived only:

~~~text
COMPLETED + ALLOW
→ PROCEED

COMPLETED + REDUCE
→ PROCEED_RESTRICTED

COMPLETED + BLOCK
→ DENY

INCOMPLETE / FAILED
+ Fail-Closed
→ DENY
~~~

~~~text
execution_disposition
≠ second Decision Authority
~~~

### Fail-Closed

~~~text
BLOCK
= normal completed safety prohibition

Fail-Closed
= safety evaluation could not be responsibly completed
~~~

Never collapse them for Post-Trade / Research analysis.

---

## 7.93 RiskState / Risk Governance — Reconciliation Checkpoint

### RiskState

Existing candidate states remain:

~~~text
NORMAL
CAUTION
RISK_REDUCED
MICRO_ONLY
NO_NEW_ENTRY
EMERGENCY
~~~

RiskState remains:

~~~text
Cross-Cutting Runtime Permission State

RiskState
≠ DefenseDecision
≠ Production Promotion
≠ Knowledge Health
≠ Runtime command
~~~

### Effective Risk Permission Context

Correction:

~~~text
RiskState
= authoritative source state(s)

Effective Risk Permission Context
= derived Defense evaluation view
≠ new canonical authority state
~~~

Multiple applicable RiskState scopes are resolved conceptually as the intersection of their permission envelopes, not by averaging or assigning arbitrary numeric severity to state names.

~~~text
Effective Permission
=
intersection of applicable authoritative Risk Envelopes
~~~

If the known intersection permits zero new Risk:

~~~text
→ normal BLOCK candidate
~~~

If applicable scope / permission cannot be determined:

~~~text
→ Evaluation INCOMPLETE
→ Fail-Closed
~~~

### Version Barrier

Defense Evaluation binds exact:

~~~text
RiskState refs / versions
Authorized Constraint refs / versions
DefensePolicyBundleVersion
Admission Decision ref/version
~~~

Before final Defense resolution, material state/version change requires restart rather than mixing old and new runtime authority in one DefenseDecision.

### Risk Governance

Canonical authority separation remains:

~~~text
REQUEST
≠ RECOMMEND
≠ APPROVE
≠ APPLY

APPROVE
≠ APPLIED
~~~

Single-writer principle remains:

~~~text
RiskState Machine
= canonical Apply authority

Defense / AI / Logger / Telegram / Post-Trade
must not directly mutate Current RiskState
~~~

Defense BLOCK / ALLOW does not itself change RiskState.

Defense may produce request / finding / recommendation material for Risk Governance.

---

## 7.94 Emergency Fast Path / Recovery Strict Path — Detailed Checkpoint

### Safety Asymmetry

~~~text
Restrict fast
Recover slow
~~~

Emergency Fast Path accelerates restrictive governance under explicit policy; it does not bypass governance.

### Action-Class Separation

Critical correction:

~~~text
RISK_INCREASING
RISK_NEUTRAL
RISK_REDUCING
~~~

Examples:

~~~text
RISK_INCREASING:
new entry
position add
exposure increase
leverage increase
weaken protection

RISK_REDUCING:
close / partial reduce
reduce-only action
leverage reduction
protection strengthening
cancel risk-increasing open order

RISK_NEUTRAL:
read-only reconciliation
status query
audit / logging
~~~

Important refinement:

~~~text
risk-reducing intent
≠ automatically proven actual risk reduction
~~~

Execution / venue semantics must be able to verify that an action cannot accidentally increase exposure (for example via reduce-only or equivalent enforceable semantics) before it is treated as safely risk-reducing.

### Emergency Meaning

~~~text
NO_NEW_ENTRY
= prohibit new Risk addition while existing Position safety management continues

EMERGENCY
= prioritize containment and block normal Risk-increasing progression,
  while allowing authorized risk-reducing / reconciliation / recovery actions
~~~

~~~text
EMERGENCY
≠ system everything off
≠ force liquidate all positions
~~~

### Emergency Fast Path Candidate

~~~text
Critical Safety Trigger
↓
Trigger Integrity
↓
Emergency Qualification
↓
Scope Resolution
↓
Restriction Direction Check
↓
Emergency Authority Match
↓
Current RiskState / Version Check
↓
Transition Legality
↓
Apply Preconditions
↓
RiskState Machine
↓
Atomic Restrictive Apply
↓
StateTransitionEvent
↓
Current RiskState Projection
↓
Downstream Permission invalidation / containment
~~~

### Emergency Scope Rule

> **Restrict the smallest scope that safely contains the known failure.**

But add a dependency rule:

~~~text
shared infrastructure dependency
cross-scope dependency
unknown failure scope
unresolved blast radius
↓
restriction scope may expand upward / outward
until containment is credible
~~~

Therefore:

~~~text
minimum scope
≠ blindly local scope
~~~

### Fast-Path Authority

Candidate:

~~~text
Standing Pre-Authorization
+
Runtime Authority Validation
~~~

The pre-authorization must constrain:

~~~text
allowed trigger classes
allowed scopes
allowed restrictive transitions
maximum authority scope
validity
policy version
authorized role/service
audit requirements
~~~

This is not "approval omitted"; it is pre-authorized restrictive governance.

### Existing Artifact Rule

Emergency restriction does not mutate old Decision / Defense artifacts.

~~~text
Old DefenseDecision ALLOW
remains historical fact

Current RiskState changes
↓
old ALLOW is no longer blindly executable
~~~

Downstream version barriers enforce this.

### Open-Order Containment

After emergency restriction, candidate containment responsibilities include:

~~~text
cancel risk-increasing open orders
preserve / recreate valid risk-reducing protection
reconcile fills
reconcile positions
reconcile account exposure
~~~

RiskState itself is Permission State; it does not perform those venue actions.

### Recovery Strict Path

Candidate:

~~~text
Restrictive RiskState
↓
Recovery Admission
↓
Original Trigger Status
↓
Root Cause Resolution / Containment
↓
Data Reconciliation
↓
Execution Reconciliation
↓
Position / Exposure Reconciliation
↓
Infrastructure Health
↓
Cooldown / Stability Window
↓
Revalidation
↓
Recovery Target Selection
↓
Recovery Readiness Assessment
↓
Strict Approval
↓
Apply Validation
↓
RiskState Machine
↓
Atomic Permission Expansion
↓
StateTransitionEvent
↓
Post-Recovery Monitoring
~~~

### Recovery Readiness

Candidate separation:

~~~text
RecoveryReadinessProcessStatus:
COMPLETED
COMPLETED_WITH_LIMITATIONS
INCOMPLETE
FAILED

RecoveryReadinessOutcome:
READY
READY_WITH_LIMITATIONS
NOT_READY
NEED_MORE_EVIDENCE
~~~

~~~text
RecoveryReadiness
≠ Approval
≠ Apply
~~~

### Recovery Principles

~~~text
Trigger disappeared
≠ Root Cause resolved

One healthy API call
≠ Recovery evidence

Cooldown elapsed
≠ Recovery permission

Previous RiskState
≠ required Recovery target

Restriction Authority
≠ Permission Expansion Authority
~~~

Recovery target is selected from current evidence, not merely by restoring the pre-incident state.

Limited recovery may be considered where root cause is not fully proven but failure is credibly contained and critical reconciliation / monitoring conditions are satisfied; full NORMAL restoration remains stricter.

### Concurrent Transition Precedence

~~~text
More Restrictive Safety Transition
>
Permission Expansion Transition
~~~

A new emergency condition interrupts Recovery expansion.

### Post-Recovery Monitoring

Recovery permission expansion should enter a stronger observation window rather than immediately returning to ordinary monitoring assumptions.

Exact duration remains policy / research work.

---

## 7.95 Defense → Execution / Temporal Barrier C — Reconciliation Checkpoint

### Barrier C Refinement

05 Final defined:

~~~text
Defense Decision
→ EntryThesis / OrderIntent
~~~

as Temporal Barrier C.

Detailed Reference refinement:

~~~text
Barrier C1
= DefenseDecision → Entry Snapshot / EntryThesis

Barrier C2
= OrderIntent → actual venue Submission
~~~

These are two checks inside the Execution boundary, not two new top-level architecture layers.

### C1 — Execution Admission

Candidate processing gates:

~~~text
EA0 Defense Chain Integrity
EA1 Execution Disposition
EA2 Decision Validity Recheck
EA3 DefenseDecision Validity
EA4 RiskState Version Barrier
EA5 Constraint Version Barrier
EA6 Restriction Integrity
EA7 Emergency / Runtime Permission
EA8 Entry Context Availability
EA9 Temporal / Market Compatibility
EA10 Final Admission Resolution
~~~

Execution Admission does NOT:

~~~text
create new Market Decision
create new Defense Decision
recalculate EV
rebuild Trade Thesis
rewrite RiskState
~~~

### Entry Snapshot Temporal Check

~~~text
defense_evaluation_market_watermark
↓
entry_snapshot_market_watermark
~~~

Materiality may distinguish:

~~~text
DECISION_MATERIAL
SAFETY_MATERIAL
EXECUTION_MATERIAL
NEITHER
~~~

Routing:

~~~text
DECISION_MATERIAL
→ new Decision / upstream refresh

SAFETY_MATERIAL
→ Defense Evaluation restart

EXECUTION_MATERIAL
→ Execution re-plan / snapshot handling

NEITHER
→ continue
~~~

### EntryThesis

EntryThesis remains:

~~~text
exact upstream refs
+
Entry-time runtime facts
~~~

not a deep copy of Research / Knowledge.

Strong candidate:

~~~text
EntryThesis valid_until
~~~

because entry snapshots are time-sensitive.

### Semantic Build Failure Separation

~~~text
ENTRY_SNAPSHOT_NOT_BUILDABLE
≠ Defense BLOCK
≠ NO_TRADE
≠ Snapshot Builder process failure
~~~

### OrderIntent Envelope Rule

~~~text
actual requested risk
<=
min(
  Economic Permission,
  Defense Safety Permission,
  Execution Feasibility
)
~~~

Execution may tighten upstream permission; it may not relax it.

### OrderIntent Validity

Strong candidate:

~~~text
OrderIntent
= immutable
+ time-bounded
~~~

An expired OrderIntent is replaced by a new planned artifact, not mutated in place.

### C2 — Submission Gate

Candidate processing gates:

~~~text
SG0 OrderIntent Integrity
SG1 EntryThesis Validity
SG2 Decision Validity
SG3 DefenseDecision Validity
SG4 RiskState Version
SG5 Constraint Version
SG6 Emergency / Kill State
SG7 Restriction Compliance
SG8 OrderIntent Validity / Expiry
SG9 Venue Conversion Preconditions
SG10 Final Submit Permission
~~~

Submission Gate:

~~~text
≠ Market Decision
≠ Defense Decision
≠ Order Planning
≠ Exchange Adapter
~~~

It only verifies that existing permission is still usable at submit time.

### Submission Routing

~~~text
Decision invalid
→ upstream Decision / Admission

Defense invalid
→ Defense Evaluation

RiskState / Constraint materially changed
→ Defense Evaluation

EntryThesis expired
→ Entry Snapshot rebuild

OrderIntent invalid / violates restriction
→ Order re-plan

Emergency restriction
→ deny new Risk-increasing submission now

Venue conversion impossible
→ Execution / Adapter boundary handling
~~~

### Submit Permission vs Failure

Critical separation:

~~~text
SUBMIT_NOT_ALLOWED
≠ SUBMISSION_PROCESS_FAILED
~~~

A correctly blocked submission is a successful safety behavior, not an execution-system failure.

### Deferred Next Work

After this checkpoint the next intentionally deferred detailed Execution work remains:

~~~text
Open Order Runtime Lifecycle
Retry
Idempotency
Reconciliation
Split Execution Lifecycle
Position creation / Position identity
Exit-side OrderIntent / ExecutionRecord reuse
Protection order lifecycle
Venue routing / multi-exchange policy
~~~

---

## 7.96 Defense / Risk / Entry Boundary — Integrated Checkpoint

### Integrated Flow

~~~text
05_DECISION
↓
DecisionResult
↓
Defense Handoff
↓
DefenseAdmissionEnvelope
↓
Defense Admission
↓
DefenseAdmissionDecision
↓
ADMITTED_TO_DEFENSE

↓
Defense Evaluation
├ Admission Snapshot lightweight recheck
├ RiskState
├ Authorized Constraint
├ Exposure / Capacity
├ Liquidity Safety
├ Drawdown / Loss Context
├ Data / Runtime Quality
├ Exchange / API Health
├ Position / Account State
└ Abnormal Event / Global Risk Limit

↓
DefenseEvaluationResult

normal completion only
↓
DefenseDecision
├ ALLOW
├ REDUCE
└ BLOCK

parallel governance:
Safety Trigger / Finding
↓
Risk Governance
↓
Emergency Restriction / Recovery
↓
RiskState Machine
↓
Current RiskState

when ALLOW / REDUCE remains valid
↓
Barrier C1
Execution Admission
↓
Entry Snapshot Builder
↓
EntryThesis
↓
Order Planning
↓
OrderIntent
↓
Barrier C2
Submission Gate
↓
SUBMIT_ALLOWED
↓
Exchange Adapter

[next checkpoint]
Open Order Runtime Lifecycle
Retry / Idempotency / Reconciliation
~~~

### Major Corrections Applied in This Checkpoint

~~~text
DA-01
DEFENSE_NOT_REQUIRED moved out of Admission outcome
into Handoff routing

DA-02
HANDOFF_FAILED treated as processing failure,
not semantic Admission outcome

DA-03
DefenseAdmissionEnvelope uses exact refs
+ minimal immutable projection, not deep copy

DA-04
Admission Process Status separated from Admission Outcome

DR-04
Full Decision Validity moved to Defense Admission;
Defense Evaluation keeps lightweight Admission recheck

DR-05
Known unsafe state separated from unable-to-evaluate failure

DR-06 / DR-07
REDUCE represented by multi-dimensional Restriction Context,
not one scalar

DR-08
Generic STALE removed from Defense Evaluation process status;
responsibility-specific recheck / restart used instead

DR-09
Effective Risk Permission Context is a derived view,
not a new authority state

DR-10
RiskState / Constraint version barriers added

DR-11
Risk-increasing / neutral / reducing actions separated

DR-12
Emergency scope minimizes blast radius but expands
for shared dependency / unknown scope when needed

DR-13
Fast Path authority uses constrained standing pre-authorization
+ runtime authority validation

DR-14
Emergency transitions do not mutate old Decision / Defense artifacts

DR-15
Cooldown alone cannot authorize Recovery

DR-16
Recovery target derives from current evidence,
not automatic return to previous state

DR-17
Restriction authority separated from permission-expansion authority

DR-18
Restrictive safety transition takes precedence over concurrent Recovery

DR-19
Post-Recovery strengthened monitoring window retained

EX-05
Entry semantic NOT_BUILDABLE separated from processing failure

EX-06
EntryThesis validity window candidate added

EX-07
Execution may tighten but never relax upstream permission envelopes

EX-08
OrderIntent time-bounded immutability candidate added

EX-09
Submit-not-allowed separated from submission process failure
~~~

### Final Cross-Review Result

~~~text
ARCHITECTURE_BREAKING_CONFLICT:
NONE FOUND

MAJOR_AUTHORITY_COLLISION:
NONE AFTER CORRECTIONS

05 / DEFENSE ECONOMIC-SAFETY COLLISION:
RESOLVED

DEFENSE / RISKSTATE WRITE COLLISION:
RESOLVED BY SINGLE-WRITER GOVERNANCE

EMERGENCY / EXECUTION COLLISION:
RESOLVED BY ACTION CLASSIFICATION + VERSION BARRIERS

PROCESS FAILURE / BUSINESS OUTCOME COLLISION:
RESOLVED

TRACE CONTINUITY:
PRESERVED

OBJECT PROLIFERATION:
CONTROLLED
- Gate records / Restriction context remain substructures where possible
- Execution Admission / Submission Gate remain processing responsibilities
  until independent identity is proven necessary

CURRENT_DESIGN_STATUS:
NOT_ADOPTED

REFERENCE_REVIEW_STATUS:
CHECKPOINT_READY

NEXT_REFERENCE_TARGET:
OPEN_ORDER_RUNTIME_LIFECYCLE
RETRY_IDEMPOTENCY_RECONCILIATION
~~~

### Remaining Known Limitations

This checkpoint intentionally leaves unresolved:

~~~text
exact numeric thresholds
exact TTL values
exact RiskState transition matrix
exact Emergency IAM implementation
exact Recovery approval actors
exact venue reduce-only semantics
exact order event model
exact retry count / backoff
exact reconciliation algorithm
exact multi-exchange routing
~~~

Those omissions are acceptable at this Legacy Reference stage and should not be silently invented as Current Design.


---

## 7.97 Execution Detailed Cross-Review — Checkpoint Scope

### Purpose

This checkpoint consolidates the detailed Execution Reference work designed after 7.96.

Source-backed anchors:

~~~text
7.37 OrderIntent
7.38 ExecutionRecord
7.40 Execution Integrated Review
7.95 Defense → Execution / Temporal Barrier C
7.96 Defense / Risk / Entry Boundary Checkpoint
~~~

Detailed unsaved design reviewed here:

~~~text
EX-10 .. EX-30
Open Order Runtime / Retry / Idempotency / Reconciliation

EX-31 .. EX-41
Split Execution

EX-42 .. EX-55
Position Creation / Position Identity

EX-56 .. EX-72
Exit / In-Trade Defense / Exit Execution

EX-73 .. EX-92
Protection Lifecycle

EX-93 .. EX-107
Venue Routing / Multi-Exchange
~~~

Status:

~~~text
CURRENT_DESIGN_STATUS:
NOT_ADOPTED

REFERENCE_STAGE:
EXECUTION_DETAILED_CROSS_REVIEW

ARCHITECTURE_REWRITE_REQUIRED:
NO

REFERENCE_LOCAL_PRECEDENCE:
Where 7.37–7.40 / 7.95–7.96 conflict with 7.97+,
7.97+ is the newer Reference interpretation only.
This does NOT create Current Design authority.
~~~

### Cross-Review Result

No architecture-breaking contradiction was found.

The detailed work is internally coherent if the following principles are preserved:

~~~text
Intent
≠ Runtime Attempt
≠ Event
≠ Projection
≠ Reconciliation Result
≠ Canonical ExecutionRecord

Order ACK
≠ Fill
≠ Position exposure

Logical Position
≠ Venue Position

Normal Exit Authority
≠ In-Trade Hard Safety Authority

Protection Intent
≠ Protection State

Venue Routing
≠ EV / Defense Decision
~~~

---

## 7.98 Execution Runtime Core — Attempt / Event / Reconciliation Contract

### Refined Runtime Flow

~~~text
Execution Intent
↓
Submission / Position / Venue checks
↓
ExecutionAttempt
↓
Adapter normalization
↓
Conversion Integrity Check
↓
Venue dispatch
↓
ExecutionEvent[]
↓
OpenOrderRuntimeProjection
↓
Reconciliation when required
↓
Terminal or Auditable Reconciled Boundary
↓
ExecutionRecord
~~~

### ExecutionAttempt

> **ExecutionAttempt = one durable venue-submission lifecycle for one immutable execution intent under one idempotency identity.**

Core identity:

~~~text
submission_attempt_id
attempt_sequence
execution_intent_ref/version
venue
account_scope
instrument
client_order_id
idempotency_key
semantic_request_digest
adapter_ref/version
created_at
trace_id
~~~

Invariant:

~~~text
same Attempt
→ same semantic request
→ same idempotency identity

semantic request changes
→ same-Attempt retry forbidden
→ new Attempt / Replan as appropriate
~~~

One active Attempt must not have multiple independent submission writers.

### ExecutionEvent

> **ExecutionEvent = an append-only immutable fact observed during an ExecutionAttempt.**

Candidate event families:

~~~text
ATTEMPT_CREATED
SUBMISSION_STARTED
REQUEST_DISPATCHED
ACK_RECEIVED
PRE_DISPATCH_FAILURE
ACK_UNKNOWN

ORDER_OPEN_OBSERVED
PARTIAL_FILL_OBSERVED
FILL_OBSERVED
ORDER_REJECTED_OBSERVED
ORDER_EXPIRED_OBSERVED

CANCEL_REQUESTED
CANCEL_ACK_RECEIVED
ORDER_CANCELED_OBSERVED

RECONCILIATION_STARTED
RECONCILIATION_EVIDENCE_OBSERVED
RECONCILIATION_RESOLVED
RECONCILIATION_UNRESOLVED
~~~

Time separation:

~~~text
occurred_at
= source-side occurrence time

observed_at
= OS observation time

local_event_sequence
= durable local append order
~~~

Source time and local commit order are not assumed identical.

### Runtime Projection

~~~text
OpenOrderRuntimeProjection
= derived current view
≠ historical authority
~~~

Candidate dimensions:

~~~text
submission_state
venue_order_state
reconciliation_state

filled_quantity
remaining_quantity
exchange_order_id

last_event_sequence
exposure_certainty
runtime_guard_required
projection_version
~~~

Projection must be rebuildable from durable facts.

### UNKNOWN

~~~text
ACK timeout
≠ REJECTED

UNKNOWN
≠ no order

UNKNOWN
≠ zero exposure
~~~

Where first submission may have reached the venue:

~~~text
ACK_UNKNOWN
↓
Reconciliation REQUIRED
~~~

No blind risk-increasing resend is allowed when idempotent safety cannot be established.

### Retry Separation

~~~text
Transport Retry
≠ New ExecutionAttempt
≠ Order Replan
≠ New Decision
~~~

Same-Attempt retry requires:

~~~text
same submission_attempt_id
same semantic_request_digest
same client_order_id / idempotency identity
same venue / account / instrument
no material permission invalidation
retry policy allows
~~~

### Reconciliation

> **Execution Reconciliation = compare local execution facts with venue order/fill/account evidence and resolve divergence without fabricating certainty.**

Candidate Process Status:

~~~text
COMPLETED
COMPLETED_WITH_LIMITATIONS
INCOMPLETE
FAILED
~~~

Candidate Outcome:

~~~text
CONSISTENT
RESOLVED_OPEN
RESOLVED_PARTIALLY_FILLED
RESOLVED_FILLED
RESOLVED_CANCELED
RESOLVED_EXPIRED
RESOLVED_REJECTED
DUPLICATE_DETECTED
STATE_DIVERGENCE
UNRESOLVED
~~~

Critical separation:

~~~text
FAILED
≠ UNRESOLVED
~~~

FAILED means the reconciliation process could not complete.
UNRESOLVED means the process completed to the available evidence boundary but certainty remains insufficient.

### Evidence Authority

~~~text
Intent
→ Execution Intent

Local dispatch fact
→ durable ExecutionEvent / adapter dispatch fact

Venue order existence/state
→ venue order query/history

Actual fill
→ authoritative venue trade/fill evidence

Current venue exposure
→ venue position/account evidence
~~~

Position difference alone does not prove a specific Attempt filled.

### Cancel Race

~~~text
CANCEL_REQUESTED
≠ CANCELED

CANCEL_ACK_RECEIVED
≠ terminal no-fill fact
~~~

Fill monitoring / reconciliation continues until a terminal or auditable reconciled boundary.

### Canonical ExecutionRecord Generator Correction

The older 7.38 wording:

~~~text
Exchange Adapter
= Canonical Generator
~~~

is refined.

New Reference interpretation:

~~~text
Exchange Adapter
= request conversion + venue interaction + venue fact observation

Execution Runtime
= durable ExecutionEvent commitment

ExecutionRecord Finalizer / Outcome Assembler
= Canonical ExecutionRecord generator

Logger
= Custodian

Post-Trade
= Analyzer
~~~

This avoids asking the Adapter to own terminal/reconciliation semantics.

### Auditable UNRESOLVED Boundary

An ExecutionRecord may be finalized with explicit incompleteness when the available evidence reaches an auditable unresolved boundary.

But:

~~~text
ExecutionRecord finalized as unresolved
≠ execution exposure safely resolved
≠ runtime safety guard released
~~~

Historical recording and safety clearance are independent.

### Adapter Conversion Integrity Barrier

After adapter normalization and before venue dispatch:

~~~text
normalized request
must preserve
execution intent semantics
+
quantity/risk ceiling
+
instrument identity
+
position-effect / reduce-only / no-flip requirements
+
venue/account scope
~~~

Mismatch:

~~~text
ADAPTER_CONVERSION_INTEGRITY_FAILED
→ do not dispatch
~~~

Adapter conversion failure is not Exchange rejection.

---

## 7.99 Split Execution / Capacity Contract

### Responsibility

~~~text
OrderIntent
= parent execution objective

ExecutionSliceIntent
= immutable child execution sub-intent

ExecutionAttempt
= one venue submission lifecycle for a Slice

SplitExecutionRuntimeProjection
= derived parent progress view
~~~

Candidate cardinality:

~~~text
1 OrderIntent
→ N Slice Intents

1 Slice
→ 0..N ExecutionAttempts

1 ExecutionAttempt
→ N ExecutionEvents
→ 1 ExecutionRecord candidate
~~~

### Future Permission Rule

~~~text
Split Plan
≠ future submission permission
~~~

Every risk-increasing Slice must recheck current permission before submission.

### Exposure Accounting

New Slice capacity must consider:

~~~text
actual filled exposure
+
open unfilled potential exposure
+
unknown potential exposure
+
reserved not-yet-submitted capacity
~~~

The same quantity/risk must not be counted twice.

### Runtime Reservation — Object Reduction

Entry capacity reservation and Exit reduction-claim reservation are not separate top-level business objects.

Use one generic runtime coordination concept candidate:

~~~text
ExecutionReservation
~~~

with purpose/kind such as:

~~~text
RISK_CAPACITY
EXPOSURE_REDUCTION_CLAIM
~~~

It is a concurrency-control record, not a Market / Risk Decision.

### UNKNOWN Rule

~~~text
UNKNOWN potential quantity
≠ zero capacity usage
~~~

In v1 Reference:

~~~text
UNKNOWN risk-increasing Slice
→ later conflicting Slice submission stops
until reconciliation
~~~

### Sequential-First

Preferred v1 complexity boundary:

~~~text
one active risk-increasing Slice
per OrderIntent / exposure scope

parallel execution
→ future extension
→ requires atomic reservation / aggregate exposure control
~~~

### Partial Fill

~~~text
filled portion
= actual exposure

remaining portion
= future execution intent
~~~

Upstream invalidation stops remaining execution but does not erase already-filled exposure.

### Replan Ownership

~~~text
execution mechanics only
→ Execution Replan

Defense permission change
→ Defense

economic validity change
→ EV / Decision route

market thesis / decision-material change
→ new Decision Cycle
~~~

### Recovery

~~~text
Crash Recovery
= restore execution progress

Crash Recovery
≠ restore old submission permission
~~~

Every remaining Slice must use current permission after restart.

---

## 7.100 Position Identity / Lifecycle Contract

### Position Identity

> **LogicalPosition = OS-managed economic exposure lineage created for one Trade/Thesis lineage and updated only from attributable execution facts.**

Core separation:

~~~text
LogicalPosition
≠ VenuePosition
≠ Order
≠ Fill
≠ TradeResult
~~~

### Creation

~~~text
position_id may be reserved before fill

position economic activation
= first authoritative exposure-changing Fill
~~~

Order acknowledgement does not create economic exposure.

### Position Allocation — Object Reduction

A separate top-level PositionAllocation object is not required at this Reference stage.

Instead, explicit Fill → Position attribution should be recorded in the Position ledger/event fact:

~~~text
fill_ref
position_ref
allocated_quantity
allocation_basis
~~~

No Fill is silently assigned by symbol alone.

### PositionEvent / Projection

Durable facts candidate:

~~~text
POSITION_ACTIVATED
EXPOSURE_INCREASED
EXPOSURE_REDUCED
POSITION_FLAT_OBSERVED
POSITION_RECONCILIATION_STARTED
POSITION_RECONCILIATION_RESOLVED
EXTERNAL_EXPOSURE_DETECTED
POSITION_CLOSED
~~~

~~~text
PositionEvent
= historical fact

CurrentPositionProjection
= derived current view
~~~

### Lifecycle

Candidate:

~~~text
RESERVED
ACTIVE
FLAT_PENDING_RECONCILIATION
CLOSED
UNRESOLVED
~~~

Local calculated quantity = 0 is not sufficient for CLOSED.

### Intended vs Actual

~~~text
intended_direction
≠ actual_side

BUY / SELL side
≠ economic position effect by itself
~~~

Position effect must be determined from actual pre/post exposure and attribution.

### Supervisor / Defense Activation

First actual exposure:

~~~text
Position ACTIVE
↓
Position Supervisor starts
+
In-Trade Defense starts
~~~

Full planned Entry completion is not required.

### Venue Position

~~~text
VenuePositionSnapshot
= external account fact
≠ LogicalPosition identity
~~~

Manual/external exposure must not be silently allocated.

Candidate reconciliation classifications:

~~~text
CONSISTENT
DIVERGENT
UNATTRIBUTED_EXPOSURE_FOUND
MISSING_EXPECTED_EXPOSURE
UNKNOWN
UNRESOLVED
~~~

Execution Reconciliation and Position Reconciliation remain separate.

### Single Writer

Current logical Position quantity/projection must have one accounting authority candidate:

~~~text
Position Ledger / Position State Projector
~~~

Supervisor, Defense, Exit Engine and Logger do not independently mutate quantity.

### Trade Boundary

Preferred v1:

~~~text
N Entry Fills
+
N Exit Fills
↓
1 Logical Position lifecycle
↓
1 TradeResult candidate
~~~

---

## 7.101 Exit / In-Trade Defense / Position Close Contract

### Authority Separation

~~~text
Position Supervisor
= Thesis Health / Warning
≠ Exit Authority

Exit Engine
= normal economic / thesis Exit authority

In-Trade Defense
= hard runtime safety authority

Execution
= turns authorized exposure reduction into venue actions

Position Accounting
= updates actual exposure from Fill facts
~~~

### ExitDecision

Candidate normal outcomes:

~~~text
MAINTAIN
REDUCE_EXPOSURE
CLOSE_POSITION
~~~

Process failure is not MAINTAIN.

ExitDecision should describe desired economic exposure:

~~~text
current_exposure
target_exposure
requested_reduction
expected_position_version
~~~

It should not merely encode BUY/SELL.

### InTradeDefenseDecision

Candidate hard-safety outcomes:

~~~text
CLEAR
TIGHTEN_PROTECTION
REDUCE_EXPOSURE
CLOSE_POSITION
~~~

Normal Exit and Hard Safety remain separate authorities.

### Position Action Coordination

Keep as a processing responsibility, not a new top-level object.

It coordinates:

~~~text
normal Exit
hard Safety Exit
Protection execution
existing exposure-changing orders
unknown execution exposure
position version
no-flip / reduce-only requirements
~~~

Hard Safety precedence does not authorize duplicate close orders.

### ExitOrderIntent

Treat as a member of an Execution Intent semantic family.

~~~text
Entry OrderIntent
→ WHY source: EntryThesis

ExitOrderIntent
→ WHY source: ExitDecision / InTradeDefenseDecision

ProtectionOrderIntent
→ WHY source: Protection Requirement / Safety authority
~~~

Do not force one overloaded object with many nullable authority fields.

### Exit Submission

Candidate checks:

~~~text
Position identity
Position version
Actual exposure
Exit authority validity
Existing Exit / Protection orders
Unknown exposure
Reduce-only / no-flip enforceability
Venue capability
Intent validity
Final submit permission
~~~

~~~text
NO_NEW_ENTRY
≠ NO_EXIT

EMERGENCY
≠ block verified risk-reducing action
~~~

### Exit Facts

~~~text
Exit Order ACK
≠ exposure reduced

authoritative Exit Fill
→ PositionEvent.EXPOSURE_REDUCED
~~~

### Position Close Gate

CLOSED requires candidate:

~~~text
known logical exposure = 0
no unresolved attributable fills
no unknown exit attempt that can change exposure
no live protection order that can reopen / flip exposure
no pending risk-changing action
acceptable venue / position reconciliation
consistent Position projection
~~~

Only then:

~~~text
POSITION_CLOSED
→ TradeResult assembly candidate
~~~

---

## 7.102 Protection Lifecycle Contract

### Semantic Separation

~~~text
Initial Protection Intent
= Entry-time protection intention

Protection Requirement
= current required coverage for an active Position

ProtectionOrderIntent
= venue-independent conditional execution intent

Venue Protection Order
= actual venue implementation

ProtectionState
= derived coverage state

Protection Fill
= actual execution fact that may change Position exposure
~~~

Initial Entry Stop is not perpetual Position-lifetime authority.

### Coverage

Candidate states:

~~~text
FULLY_PROTECTED
PARTIALLY_PROTECTED
PENDING_PROTECTION
UNPROTECTED
UNKNOWN
~~~

~~~text
UNPROTECTED
≠ UNKNOWN
~~~

### Quantity Binding

Protection coverage follows actual attributable exposure, not planned Entry target alone.

Every material Position quantity change triggers coverage re-evaluation:

~~~text
Entry Fill
Additional Entry
Partial Exit
Protection Fill
External / Manual exposure change
Reconciliation correction
~~~

### Trigger

~~~text
Protection Trigger
≠ exposure reduction

Protection Trigger
→ Execution lifecycle begins / continues

Protection Fill
→ actual Position exposure change
~~~

Trigger semantics should include:

~~~text
trigger source
trigger direction
trigger value / condition
~~~

not price alone.

### Mechanism

Candidate context:

~~~text
SERVER_SIDE
CLIENT_SIDE
HYBRID
~~~

Mechanism reliability is part of Protection interpretation.

### Replace / Mutual Exclusion

Protection replacement must consider both:

~~~text
coverage gap risk
double-execution / over-close risk
~~~

Core semantic requirement:

~~~text
mutually exclusive exit actions
must not together over-close / flip Position
~~~

Venue-native OCO / amend may implement this but does not define the Core meaning.

### Protection Reconciliation

Candidate outcomes:

~~~text
CONSISTENT
UNDER_PROTECTED
OVER_COVERED
MISSING_PROTECTION
DUPLICATE_PROTECTION
UNKNOWN
UNRESOLVED
~~~

Over-protection can be unsafe.

### Object Proliferation Correction

Do not add a separate ProtectionEvent stream at this stage.

Use:

~~~text
ExecutionEvent
= venue/order execution facts

PositionEvent
= actual exposure facts

ProtectionState / Protection Reconciliation
= protection semantic projection / audit
~~~

A separate ProtectionEvent becomes justified only if later lifecycle semantics cannot be reconstructed cleanly.

### Position Close

Exposure zero is not sufficient while residual protection remains unresolved.

~~~text
exposure = 0
↓
protection cleanup
↓
protection reconciliation
↓
no orphan risk-changing protection
↓
Position Close Gate
~~~

Orphan protection is a Safety Finding candidate.

---

## 7.103 Venue Routing / Multi-Exchange Contract

### Boundary

~~~text
Order / Execution Intent
= venue-independent execution meaning

Venue Routing
= choose eligible venue/account allocation

Exchange Adapter
= convert selected route to venue API representation
~~~

Venue Routing is not EV or Defense authority.

### Instrument Compatibility

~~~text
same asset
≠ same economic instrument
~~~

Routing must preserve:

~~~text
instrument type
spot / perpetual / future semantics
quote / settlement
contract specification
margin / leverage semantics
funding / expiry where applicable
position mode compatibility
~~~

### Venue Eligibility

Candidate checks:

~~~text
Venue authorization
Instrument compatibility
Account / credential health
Venue RiskState
Authorized Constraint
Venue / API health
Data / timestamp quality
Balance / margin capacity
Liquidity / slippage feasibility
Required execution capability
Protection capability
Position mode compatibility
Economic validity envelope
Exposure / capacity
Runtime reconciliation health
~~~

Hard ineligibility is not averaged away.

### Economic Boundary

~~~text
Routing
= does current venue execution fit existing economic validity envelope?

EV / 05
= is the Trade economically worthwhile?
~~~

Routing does not recalculate Trade EV.

### Fallback

~~~text
Pre-Submission Fallback
≠ Post-Submission Fallback
~~~

Post-submission UNKNOWN requires reconciliation before risk-increasing fallback.

Permission observed for Venue A is not automatically portable to Venue B.

### Routing Plan

Keep VenueRoutingPlan as an immutable execution-planning substructure / trace record first, not a new architecture layer.

~~~text
eligible venues
selected route(s)
venue/account/instrument
allocated quantity
route sequence / role
routing policy version
validity
trace
~~~

Routing Plan is time-bounded and is not future submit permission.

### Single-Venue First

Preferred v1 complexity boundary:

~~~text
Default:
1 Logical Position lineage
→ 1 venue/account exposure leg

Advanced:
1 Logical Position lineage
→ N VenueExposureLegs
~~~

### VenueExposureLeg

Keep as a value/substructure of Logical Position first:

~~~text
position_ref
venue
account
instrument
actual side
quantity
fill refs
execution record refs
protection state ref
venue position snapshot ref
exposure certainty
~~~

Logical Position owns Trade/Thesis lineage.
VenueExposureLeg shows where physical exposure exists.

### Multi-Venue Capacity

Per-Venue safety is insufficient by itself.

Applicable aggregate constraints must include:

~~~text
global
portfolio
account
venue
instrument
logical position
~~~

No concurrent route may double-consume the same authorized capacity.

### Exit / Protection

Logical Close is decomposed to actual VenueExposureLegs.

~~~text
Logical ExitDecision
↓
venue exposure resolution
↓
venue-local ExitOrderIntent(s)
~~~

Protection implementation also follows actual venue-local exposure.

### Reconciliation

Aggregate quantity equality alone is not enough.

Example:

~~~text
Expected:
A 0.4
B 0.6

Actual:
A 0.6
B 0.4

Total:
1.0
~~~

still represents Venue allocation divergence.

### Cross-Venue Hedge

~~~text
HEDGE
≠ CLOSE
~~~

A hedge on another venue may reduce delta exposure while original counterparty / liquidation / funding / venue risk remains.

Cross-venue emergency hedge authority remains intentionally deferred.

### Venue Capability

Candidate capability profile:

~~~text
market / limit
reduce-only
stop market / stop limit
OCO
native amend
hedge mode
client order id
idempotency behavior
position query
fill history
funding
leverage
~~~

Keep venue-specific API branching inside Adapter/Capability configuration rather than spreading venue-name conditionals through Core logic.

---

## 7.104 Execution Detailed Cross-Review — Object Reduction / Corrections / Final Checkpoint

### Object Proliferation Review

Keep / promote as durable Reference object candidates:

~~~text
ExecutionAttempt
ExecutionEvent
ExecutionReconciliationResult
ExecutionRecord

LogicalPosition
PositionEvent

ExitDecision
InTradeDefenseDecision

Entry / Exit / Protection Execution Intent family
~~~

Keep primarily as Value Structure / Child Structure / Derived Projection / Runtime Record:

~~~text
ExecutionSliceIntent
OpenOrderRuntimeProjection
SplitExecutionRuntimeProjection
ExecutionReservation

CurrentPositionProjection
VenuePositionSnapshot
VenueExposureLeg

ProtectionRequirement
ProtectionState / ProtectionReconciliationResult

VenueRoutingPlan
VenueCapabilityProfile
~~~

Keep as Processing Responsibilities, not top-level persistent objects:

~~~text
Submission Gate
Execution Recovery Gate
Position Action Coordination
Protection Reconciliation
Venue Routing
Position Close Gate
~~~

Do not create yet:

~~~text
separate PositionAllocation top-level object
separate ProtectionEvent stream
separate EntryCapacityReservation and ExitCapacityReservation object families
separate UNKNOWN lock objects per domain
~~~

Use explicit ledger attribution, generic reservation semantics and derived runtime safety guards first.

### Generic Runtime Safety Guard

The following conditions share one concept:

~~~text
unknown execution exposure
startup unreconciled execution
unknown Position state
critical protection uncertainty
~~~

Do not create multiple unrelated lock authorities.

Candidate semantic:

~~~text
ExecutionSafetyGuard
= runtime execution restriction derived from unresolved operational uncertainty
≠ RiskState
~~~

Long-lived/material guards may generate Risk Governance requests, but do not directly mutate RiskState.

### Additional Cross-Review Corrections

#### CORRECTION-EX-108 — ExecutionRecord Generator Responsibility

~~~text
Exchange Adapter
≠ terminal canonical ExecutionRecord owner

Adapter
= venue conversion / interaction / observation

ExecutionRecord Finalizer
= terminal or auditable reconciled outcome assembly
~~~

#### CORRECTION-EX-109 — Adapter Normalization Integrity Barrier

~~~text
Submission Gate PASS
↓
Adapter normalization
↓
semantic integrity check
↓
dispatch
~~~

Normalized venue request must remain within the approved execution meaning / quantity / scope / no-flip / protection semantics.

#### CORRECTION-EX-110 — Auditable UNRESOLVED Does Not Clear Safety

~~~text
ExecutionRecord created at unresolved audit boundary
≠ exposure certainty recovered
≠ ExecutionSafetyGuard released
~~~

Historical closure and safety closure are separate.

#### CORRECTION-EX-111 — Runtime Object Collapse

~~~text
PositionAllocation
→ Position ledger/event attribution

ProtectionEvent
→ not added yet; use ExecutionEvent + PositionEvent + Protection reconciliation

Entry / Exit reservations
→ generic ExecutionReservation

domain-specific unknown locks
→ generic ExecutionSafetyGuard

VenueRoutingPlan
→ execution planning trace/substructure first
~~~

### Consolidated Correction Index

Runtime Execution:

~~~text
EX-10  OrderIntent ≠ ExecutionAttempt
EX-11  Execution Event ≠ Runtime State
EX-12  UNKNOWN timeout ≠ REJECTED
EX-13  Transport Retry ≠ New Attempt ≠ Replan
EX-14  No blind retry when idempotent safety is unproven
EX-15  Reconciliation must not fabricate certainty
EX-16  Unknown exposure may require execution safety restriction
EX-17  Cancel does not stop fill monitoring before terminal/reconciled boundary
EX-18  Filled exposure ≠ remaining intent
EX-19  Restart reconciles unresolved execution before conflicting new Risk
EX-20  ExecutionAttempt gets durable runtime identity
EX-21  Source occurrence time ≠ local observation/append order
EX-22  Runtime Projection is rebuildable derived view
EX-23  Execution safety restriction ≠ RiskState
EX-24  Idempotency identity binds semantic request digest
EX-25  Position delta alone does not prove a specific Fill
EX-26  Resolved UNKNOWN does not erase UNKNOWN history
EX-27  Cancel ACK ≠ terminal canceled fact
EX-28  Process started ≠ Trading Ready
EX-29  Auditable unresolved boundary may produce incomplete ExecutionRecord
EX-30  Later authoritative evidence uses supersession/versioning, not mutation
~~~

Split Execution:

~~~text
EX-31  Split Plan ≠ future submission permission
EX-32  Slice lifecycle ≠ Venue order lifecycle
EX-33  Exposure accounting includes open / unknown potential exposure
EX-34  Permission check needs atomic capacity reservation for concurrency safety
EX-35  UNKNOWN quantity ≠ zero
EX-36  Sequential Split preferred for v1
EX-37  Upstream invalidation stops remaining intent, not already-filled exposure
EX-38  Slice validity cannot exceed parent validity
EX-39  Replan ownership follows earliest authoritative repair owner
EX-40  Aggregate execution metrics remain derived
EX-41  Crash recovery restores progress, not old permission
~~~

Position:

~~~text
EX-42  First authoritative exposure-changing Fill activates Position
EX-43  VenuePosition ≠ LogicalPosition identity
EX-44  Fill → Position attribution must be explicit
EX-45  Position Event ≠ Position command
EX-46  Intended direction ≠ actual exposure
EX-47  Local quantity zero ≠ Position CLOSED
EX-48  Position supervision / hard safety starts from first actual exposure
EX-49  Average entry price is derived
EX-50  Venue netting must not erase distinct Thesis lineage
EX-51  Order side ≠ Position exposure effect
EX-52  Unattributed venue exposure is not fabricated into a Logical Position
EX-53  Execution Reconciliation ≠ Position Reconciliation
EX-54  Multiple fills may belong to one Logical Position / TradeResult
EX-55  Position accounting needs one authoritative writer/projector
~~~

Exit:

~~~text
EX-56  MAINTAIN ≠ Exit evaluation failure
EX-57  ExitDecision targets exposure, not raw order side
EX-58  Normal Exit authority ≠ In-Trade hard safety authority
EX-59  Safety precedence ≠ duplicate Exit order
EX-60  Position actions bind expected_position_version
EX-61  Entry OrderIntent is not overloaded blindly for Exit
EX-62  Full Close means target exposure zero, not stale fixed sell quantity
EX-63  NO_NEW_ENTRY / EMERGENCY do not prohibit verified risk-reducing Exit
EX-64  Exit execution failure ≠ ExitDecision wrong
EX-65  ExecutionAttempt/Event/Record machinery is reusable for Entry and Exit
EX-66  Exit order submitted ≠ exposure reduced
EX-67  Full Close requires protection cleanup / reconciliation
EX-68  Protection Order exists ≠ Protection State sufficient
EX-69  Exit side also needs concurrency-safe exposure claim/reservation semantics
EX-70  Hard Safety urgency ≠ unlimited execution risk
EX-71  Safety CLEAR ≠ economic MAINTAIN
EX-72  Normal Exit reason and safety terminal reason remain distinct
~~~

Protection:

~~~text
EX-73  Protection quantity follows actual exposure
EX-74  Entry Fill → Protection confirmation gap is explicit
EX-75  UNPROTECTED ≠ UNKNOWN
EX-76  Initial Entry Stop is not lifetime protection authority
EX-77  Trigger semantics include source / direction / value
EX-78  Protection Trigger ≠ exposure reduced
EX-79  Server-side / Client-side / Hybrid mechanism context retained
EX-80  Protection coverage binds Position version
EX-81  Replace considers both coverage gap and double-execution risk
EX-82  OCO is venue capability; mutual exclusion is Core semantics
EX-83  Protection execution failure may escalate Hard Safety
EX-84  Insufficient/unknown protection may restrict scale-in
EX-85  Full Exit + protection cleanup are coordinated
EX-86  Supervisor advisory ≠ protection mutation authority
EX-87  Hard risk protection ≠ profit target
EX-88  Material Position quantity change re-evaluates protection coverage
EX-89  Over-protection can be unsafe
EX-90  Orphan Protection Order is Safety Finding candidate
EX-91  Protection recovery required before Position Runtime is fully ready
EX-92  Do not duplicate ExecutionEvent facts into a separate Protection event stream
~~~

Venue / Multi-Exchange:

~~~text
EX-93   Same asset ≠ same economic instrument
EX-94   Venue cost-envelope check ≠ EV recalculation
EX-95   ACK_UNKNOWN blocks blind post-submit fallback
EX-96   Defense permission is not portable across venues without validation
EX-97   Routing Plan ≠ future submit permission
EX-98   Single-Venue First for v1
EX-99   Per-Venue safety ≠ portfolio/global safety
EX-100  LogicalPosition ≠ VenueExposureLeg
EX-101  Venue failure ≠ automatic Logical Position full close
EX-102  Logical close decomposes to actual VenueExposureLegs
EX-103  Protection implementation follows venue-local exposure
EX-104  Aggregate quantity match ≠ venue allocation reconciliation
EX-105  Cross-Venue hedge ≠ Exit
EX-106  Pre-submit fallback ≠ Post-submit fallback
EX-107  Venue capability belongs in explicit capability/config semantics, not Core venue-name branching
~~~

Cross-Review additions:

~~~text
EX-108  Adapter is not canonical ExecutionRecord finalizer
EX-109  Adapter-normalized request gets pre-dispatch semantic integrity check
EX-110  Auditable unresolved record does not release safety guard
EX-111  Collapse redundant runtime objects before Current adoption
~~~

### Final Cross-Review Result

~~~text
ARCHITECTURE_BREAKING_CONFLICT:
NONE FOUND

MAJOR_AUTHORITY_COLLISION:
NONE AFTER CORRECTIONS

EXECUTION FACT / RUNTIME STATE COLLISION:
RESOLVED

RETRY / NEW ATTEMPT COLLISION:
RESOLVED

UNKNOWN / REJECTED COLLISION:
RESOLVED

POSITION / VENUE POSITION COLLISION:
RESOLVED

NORMAL EXIT / HARD SAFETY COLLISION:
RESOLVED

PROTECTION / EXIT COLLISION:
RESOLVED BY POSITION ACTION COORDINATION

VENUE ROUTING / EV / DEFENSE COLLISION:
RESOLVED

OBJECT_PROLIFERATION:
REDUCED

TRACE_CONTINUITY:
PRESERVED

CURRENT_DESIGN_STATUS:
NOT_ADOPTED

REFERENCE_REVIEW_STATUS:
EXECUTION_DETAILED_CHECKPOINT_READY
~~~

### Integrated Execution Reference Flow

~~~text
05 Decision
↓
Defense Admission
↓
Defense Evaluation
↓
Barrier C1
↓
EntryThesis
↓
Entry OrderIntent
↓
Split / Venue Planning
↓
ExecutionReservation
↓
Barrier C2 / Submission Gate
↓
ExecutionAttempt
↓
Adapter Normalization
↓
Conversion Integrity Check
↓
Venue Dispatch
↓
ExecutionEvent[]
↓
Runtime Projection / Reconciliation
↓
ExecutionRecord
↓
Fill Attribution
↓
LogicalPosition ACTIVE
↓
Position Supervisor
+
In-Trade Defense
+
Protection Management
+
Exit Engine
↓
Exit / Protection Execution Intents
↓
same ExecutionAttempt / Event / Reconciliation machinery
↓
PositionEvent / CurrentPositionProjection
↓
Position Close Gate
↓
POSITION_CLOSED
↓
TradeResult
↓
Post-Trade
~~~

### Remaining Intentionally Deferred Work

~~~text
exact DB schema
exact class hierarchy / inheritance
exact event storage technology
exact lock / lease / CAS implementation
exact retry / backoff values
exact idempotency key format
exact reconciliation query order per venue
exact Position PnL accounting formula
exact protection threshold / stop logic
exact Exit policy thresholds
exact routing ranking / weighting
exact multi-venue hedge policy
exact cross-venue collateral policy
exact IAM / credential design
~~~

These omissions are acceptable for the Legacy Reference stage.

### Next Reference Target

Execution detailed design has reached a clean checkpoint.

Candidate next work:

~~~text
TradeResult / Position Terminal reconciliation with the new Execution lifecycle
then
Post-Trade source-object consistency review
~~~

Do not jump to Current adoption from this checkpoint.

---

## 7.105 TradeResult / Position Terminal — Execution Reconciliation Checkpoint

### Purpose

This checkpoint reconciles the older Post-Trade Reference (7.41–7.49) with the newer detailed Execution / Position / Exit / Protection lifecycle (7.97–7.104).

Source-backed anchors retained:

~~~text
7.41 TradeResult
= final Trade outcome fact
≠ analysis

7.42–7.48
= versioned Post-Trade analysis objects

7.49
= integrated Post-Trade flow

7.50–7.56
= Finding → Research governance

7.100–7.104
= LogicalPosition / Exit / Protection / Execution detailed terminal boundary
~~~

Derived refinements in this checkpoint do NOT create Current Design authority.

~~~text
CURRENT_DESIGN_STATUS:
NOT_ADOPTED

REFERENCE_STAGE:
POST_TRADE_EXECUTION_RECONCILIATION

REFERENCE_LOCAL_PRECEDENCE:
Where 7.41–7.49 conflicts with 7.105+,
7.105+ is the newer Reference interpretation only.
~~~

### Position Terminal Refinement

Older shorthand:

~~~text
Trade / Position Terminal
↓
TradeResult
~~~

Newer detailed Reference interpretation:

~~~text
LogicalPosition
↓
known actual exposure = 0
↓
no unresolved Position-attributable execution effect
↓
Execution Reconciliation acceptable
↓
Protection cleanup
↓
Protection Reconciliation acceptable
↓
Position Reconciliation acceptable
↓
Position Close Gate
↓
POSITION_CLOSED
↓
TradeResult Finalization
~~~

Critical separation:

~~~text
Exit Order Filled
≠ Trade Terminal

Local calculated quantity = 0
≠ Position CLOSED

Position CLOSED
= hard prerequisite for canonical TradeResult finalization candidate
~~~

### CORRECTION-PT-07 — Position CLOSED is the TradeResult boundary

TradeResult is refined to:

> **A versioned immutable Final Trade Outcome Fact assembled only after the LogicalPosition lifecycle reaches POSITION_CLOSED, preserving the exact Decision / Thesis / Entry / Execution / Position / Exit / Safety / Protection / Venue lineage and realized economic outcome without adding interpretation.**

### TradeResult Finalization Gates

Candidate processing gates:

~~~text
TR0 Logical Position Identity
TR1 Position lifecycle = CLOSED
TR2 final Position version known
TR3 attributable exposure = known zero
TR4 no unresolved exposure-changing ExecutionAttempt
TR5 no unresolved Fill capable of changing Position
TR6 no live/orphan Protection capable of changing exposure
TR7 final Position Reconciliation acceptable
TR8 final Protection Reconciliation acceptable
TR9 Entry / Exit execution lineage resolvable
TR10 Source version / integrity sufficient
TR11 terminal timestamp fixed
TR12 Outcome Assembly integrity
~~~

### CORRECTION-PT-08 — Terminality ≠ Measurement Completeness

~~~text
Exposure safely terminal
+
some metric / funding / latency / MAE evidence incomplete
→ TradeResult may still finalize
→ preserve completeness / quality / uncertainty / limitations
~~~

But:

~~~text
Exposure UNKNOWN / unresolved
→ Position cannot be CLOSED
→ canonical TradeResult cannot be finalized
~~~

### TradeResult Source Contract Candidate

~~~text
Identity / Lineage
- trade_result_id
- logical_position_ref
- decision_result_ref
- entry_thesis_ref
- primary_trade_thesis_ref
- selected_trade_thesis_refs[]
- trace_id

Terminal
- position_closed_event_ref
- final_position_version
- activated_at
- closed_at
- final_position_reconciliation_ref
- final_protection_reconciliation_ref

Entry
- entry_execution_intent_refs[]
- entry_execution_record_refs[]
- entry_fill_refs[]

Exit
- exit_decision_refs[]
- exit_execution_intent_refs[]
- exit_execution_record_refs[]
- exit_fill_refs[]

Safety
- defense_decision_ref
- in_trade_defense_decision_refs[]
- risk_state_refs[]
- safety_reason_refs[]

Protection
- initial_protection_intent_ref
- protection_execution_record_refs[]
- protection_trigger_refs[]
- protection_failure_refs[]
- orphan_protection_refs[]

Venue
- venue_exposure_leg_refs[]
- venue_position_evidence_refs[]

Economics
- gross_pnl
- fee
- funding
- net_pnl
- slippage measurements
- metric / formula versions

Path
- holding_duration
- MAE
- MFE
- observation_window_refs[]

Evidence
- production_evidence_refs[]
- completeness
- quality
- uncertainty
- limitations[]

Integrity
- source versions / digests
- outcome_assembly_version
- trade_result_version
- supersedes_ref optional
~~~

TradeResult should use exact refs + final trade facts + derived measurements.
It should not deep-copy all upstream objects.

### CORRECTION-PT-09 — Exit Reason ≠ Terminal Close Authority

Preserve separately:

~~~text
normal_exit_reason_refs[]
safety_exit_reason_refs[]
protection_trigger_refs[]
terminal_close_authority_ref
~~~

Requested normal Exit reason and the action that actually completed terminal close may differ.

---

## 7.106 Multi-Thesis Lineage / Evaluation Window Refinement

### Source Contract Conflict Found

7.84 DecisionResult explicitly allows:

~~~text
primary_selected_thesis_ref
selected_thesis_refs[]
~~~

with multiple selected same-direction Thesis.

Older Entry / Position / Post-Trade wording often assumes one Thesis.

This is a correctable trace-contract mismatch, not an architecture-breaking conflict.

### CORRECTION-PT-10 — Preserve selected Thesis set through Production

Candidate lineage:

~~~text
DecisionResult
- primary_selected_thesis_ref
- selected_thesis_refs[]

↓
EntryThesis
- primary_trade_thesis_ref
- selected_trade_thesis_refs[]

↓
LogicalPosition
- one Decision / Entry lineage
- preserves primary + all selected Thesis refs

↓
TradeResult
- primary_trade_thesis_ref
- selected_trade_thesis_refs[]
~~~

No selected Thesis may silently disappear at the Execution boundary.

### CORRECTION-PT-11 — TradeThesisEvaluation cardinality

Preferred candidate:

~~~text
1 selected TradeThesis
→ 1 TradeThesisEvaluation

1 TradeResult
→ 1..N TradeThesisEvaluation
~~~

Each evaluation binds:

~~~text
trade_thesis_ref
is_primary_selected
decision_result_ref
entry_thesis_ref
relevant market evidence
evaluation window
~~~

ThesisMemberAttribution then binds to exactly one parent TradeThesisEvaluation / TradeThesis lineage.

Do not mix members from different selected Thesis into one attribution set.

### CORRECTION-PT-12 — Trade lifetime ≠ Thesis evaluation window

Example:

~~~text
TradeThesis expected horizon = 4h
Position stopped and CLOSED at 1h
~~~

Then:

~~~text
TradeResult
= READY after Position CLOSED

TradeThesisEvaluation
= may remain WAITING_FOR_EVIDENCE
until expected horizon / valid terminal invalidation / policy-defined evaluability boundary
~~~

Position Close does not automatically prove Thesis mismatch.

---

## 7.107 Production Evaluation Readiness / Common Source Binding

### Post-Trade Analysis Orchestration

Derived processing responsibility candidate:

> **Post-Trade / Production Evaluation Orchestration = checks whether each analysis type has the exact source versions, evaluation window, evidence channel and completeness required to run, and starts only analyses whose own readiness contract is satisfied.**

It is a processing responsibility, not a new canonical architecture layer.

### CORRECTION-PT-13 — Trade CLOSED ≠ all analyses READY

Candidate readiness semantics:

~~~text
READY
WAITING_FOR_EVIDENCE
NOT_APPLICABLE
INDETERMINATE
FAILED
~~~

Exact enum remains deferred.

### Analysis Source Matrix

| Analysis | Minimum source candidate | TradeResult required? | Readiness basis |
|---|---|---:|---|
| OutcomeAnalysisResult | TradeResult + execution/exit/position trace | YES | TradeResult finalized |
| TradeThesisEvaluation | exact TradeThesis + entry-time context + market evidence | NO | horizon / invalidation evaluation boundary ready |
| ThesisMemberAttribution | parent ThesisEvaluation + ThesisMember refs + provenance | NO | parent Thesis evaluation evaluable |
| DefenseDecisionEvaluation | DefenseDecision + defense-time context + later evidence | CONDITIONAL | outcome-specific evidence ready |
| InTradeDefenseDecisionEvaluation | InTradeDefenseDecision + Position / execution safety evidence | usually | safety episode evaluable |
| SupervisorEvaluation | Supervisor history + Position lifecycle + Thesis evidence + Exit refs | usually | monitoring episode evaluable |
| DemoLiveDivergence | ProductionEvidence + reference profile + comparability context | NO | both channels evaluable / comparable |
| CounterfactualResult | exact Decision Point + T0 Information Set + Alternative | NO | evaluation window + model inputs ready |
| DecisionResultEvaluation | DecisionResult + T0 DecisionContext + later market evidence | NO | decision evaluation window ready |

### CORRECTION-PT-22 — AnalysisSourceBinding common value structure

Do not create a new top-level object.

Candidate common substructure:

~~~text
AnalysisSourceBinding

subject_refs[]

source_object_refs[]
source_versions[]
source_digests[]

decision_time_context_ref optional

position_ref optional
trade_result_ref optional

observation_window
evaluation_window

evidence_channel_refs[]

completeness
quality
uncertainty

shared_origin_refs[]
dependency_refs[]

source_limitations[]

binding_policy_version
~~~

---

## 7.108 Decision / Defense / In-Trade Safety Evaluation Corrections

### CORRECTION-PT-14 — DefenseDecisionEvaluation does not require TradeResult

Defense BLOCK normally produces no Entry, Position or TradeResult.

For ALLOW / REDUCE with actual Trade:

~~~text
DefenseDecision
+
defense-time safety context
+
TradeResult when available
+
ProductionEvidence
+
later market evidence
+
valid Shadow / Counterfactual evidence when applicable
~~~

For BLOCK:

~~~text
DefenseDecision
+
defense-time safety context
+
later market evidence
+
valid Shadow / Counterfactual evidence when applicable
~~~

Preserve:

~~~text
would-have-profited
≠ BLOCK was wrong
~~~

### CORRECTION-PT-15 — In-Trade Defense gets a distinct evaluation path

Semantic analysis family candidate:

~~~text
Pre-Entry:
DefenseDecisionEvaluation

In-Position:
InTradeDefenseDecisionEvaluation
~~~

Candidate InTradeDefenseDecisionEvaluation axes:

~~~text
Trigger Validity
Response Timing
Safety Benefit
Exposure Reduction Effectiveness
Execution Feasibility
Restriction Cost
Protection Interaction
Emergency Interaction
False Escalation Candidate
Late Intervention Candidate
Missed Intervention Candidate
~~~

Avoided loss remains counterfactual / estimated, not Actual Fact.

### CORRECTION-PT-21 — DecisionResultEvaluation gap

7.84 explicitly states:

~~~text
TAKE + WIN
≠ Decision automatically correct

TAKE + LOSS
≠ Decision automatically wrong

NO_TRADE + missed move
≠ Decision automatically wrong
~~~

Candidate:

> **DecisionResultEvaluation = a versioned analysis of a canonical DecisionResult against its frozen decision-time information set and later evaluative evidence, without using hindsight to turn later price movement into an automatic correctness verdict.**

TAKE may use TradeResult when execution occurred.

NO_TRADE:

~~~text
DecisionResult
+
Decision-time Context
+
later market behavior
+
valid Counterfactual when available
~~~

No TradeResult is required.

Historical label "Post-Trade" is retained for compatibility, but semantic scope now includes Post-Decision / Post-Defense / Post-Execution / Post-Position Production Evaluation.

---

## 7.109 Post-Trade Analysis Source Corrections

### CORRECTION-PT-16 — OutcomeAnalysis is not Source Owner / Root Cause Authority

OutcomeAnalysisResult may reference:

~~~text
TradeResult
ExecutionRecord refs
Position history
Exit refs
Safety refs
Protection / Reconciliation diagnostics
~~~

to classify:

~~~text
Economic Outcome / Expectation Alignment
Opportunity
System Integrity
~~~

It does not own or overwrite Source Facts and does not prove Root Cause.

### CORRECTION-PT-17 — Execution topology joins Demo/LIVE Comparability

Add candidate comparability context:

~~~text
routing_policy_version
route allocation
single / multi venue
split execution policy
VenueExposureLeg structure
protection mechanism
server-side / client-side / hybrid protection
position mode
execution capability context
~~~

~~~text
same strategy
≠ automatically comparable execution environment
~~~

### CORRECTION-PT-18 — 7.49 direct Analysis → ResearchCandidate is superseded

Use 7.50+:

~~~text
Analysis
↓
Finding Extractor
↓
Finding Normalizer
↓
Canonical Finding
↓
Candidate Promotion
↓
ResearchCandidate
~~~

### CORRECTION-PT-19 — Peer analysis topology

Preferred relation:

~~~text
Immutable Source Facts / Snapshots
↓
Production Evaluation Orchestration

├ OutcomeAnalysisResult
├ TradeThesisEvaluation 1..N
│  ↓
│ ThesisMemberAttribution 0..N
├ DefenseDecisionEvaluation
├ InTradeDefenseDecisionEvaluation
├ DecisionResultEvaluation
├ SupervisorEvaluation
├ DemoLiveDivergence
└ CounterfactualResult
~~~

The clear parent/child relation retained is:

~~~text
TradeThesisEvaluation
→ ThesisMemberAttribution
~~~

### CORRECTION-PT-20 — Source supersession propagates by versioning

~~~text
ExecutionRecord v1
↓
TradeResult v1
↓
Analysis v1

later authoritative evidence
↓
ExecutionRecord v2 supersedes v1
~~~

If material:

~~~text
TradeResult v2 supersedes v1
↓
re-analysis v2
~~~

Do not mutate old source or analysis objects.

---

## 7.110 Finding Pipeline Reconciliation — Taxonomy / Source Contract

### Cross-Review Result

7.50–7.56 responsibilities remain usable.

No major responsibility collision was introduced by PT-07..PT-22.

However the Finding Registry and 7.56 source list need extension for the new analysis types.

### Finding Extractor Scope Refinement

Older wording:

~~~text
Versioned Post-Trade Analysis Result
~~~

Newer semantic interpretation:

~~~text
Versioned Production Evaluation Analysis Result
~~~

This includes non-trade Production decisions such as NO_TRADE and Defense BLOCK.

### CORRECTION-PT-23 — Finding Taxonomy requires versioned extension

Do NOT silently rewrite:

~~~text
FINDING_TAXONOMY_v1.0
FINDING_NORMALIZATION_v1.0
~~~

Historical v1.0 Findings remain valid.

Candidate extension:

~~~text
FINDING_TAXONOMY_v1.1
FINDING_NORMALIZATION_v1.1
~~~

### New DECISION Domain Candidate

~~~text
DecisionResultEvaluation
→ DECISION
~~~

Candidate mappings:

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| TAKE_RISK_RATIONALE_MISMATCH_CANDIDATE | DEVIATION | FND.DECISION.TAKE_RISK_RATIONALE_MISMATCH_CANDIDATE |
| NO_TRADE_OPPORTUNITY_CANDIDATE | OPPORTUNITY | FND.DECISION.NO_TRADE_OPPORTUNITY_CANDIDATE |
| DECISION_HORIZON_MISMATCH | DEVIATION | FND.DECISION.DECISION_HORIZON_MISMATCH |
| DECISION_UNCERTAINTY_UNDERSTATED | ANOMALY | FND.DECISION.DECISION_UNCERTAINTY_UNDERSTATED |
| DECISION_UNCERTAINTY_OVERSTATED | ANOMALY | FND.DECISION.DECISION_UNCERTAINTY_OVERSTATED |
| DECISION_CONFLICT_HANDLING_GAP | CONTRADICTION | FND.DECISION.DECISION_CONFLICT_HANDLING_GAP |
| DECISION_ECONOMIC_VALIDITY_GAP | BOUNDARY | FND.DECISION.DECISION_ECONOMIC_VALIDITY_GAP |

### In-Trade Defense Source Mapping

Reuse existing DEFENSE domain:

~~~text
DefenseDecisionEvaluation
→ DEFENSE

InTradeDefenseDecisionEvaluation
→ DEFENSE
~~~

Candidate additional codes:

| raw_finding_kind | Class | Canonical Code |
|---|---|---|
| INTRADE_LATE_INTERVENTION_CANDIDATE | SAFETY_GAP | FND.DEFENSE.INTRADE_LATE_INTERVENTION_CANDIDATE |
| INTRADE_FALSE_ESCALATION_CANDIDATE | SAFETY_GAP | FND.DEFENSE.INTRADE_FALSE_ESCALATION_CANDIDATE |
| INTRADE_UNDER_RESPONSE_CANDIDATE | SAFETY_GAP | FND.DEFENSE.INTRADE_UNDER_RESPONSE_CANDIDATE |
| INTRADE_PROTECTION_RESPONSE_GAP | SAFETY_GAP | FND.DEFENSE.INTRADE_PROTECTION_RESPONSE_GAP |
| INTRADE_EXECUTION_CONTAINMENT_GAP | SYSTEM_GAP | FND.DEFENSE.INTRADE_EXECUTION_CONTAINMENT_GAP |

### Shared-Origin Protection

DecisionResultEvaluation, DefenseDecisionEvaluation, OutcomeAnalysisResult and CounterfactualResult may share one Decision / Market episode.

Existing FP-03 / FP-06 therefore remain essential:

~~~text
multiple analysis objects
≠ independent evidence count
~~~

---

## 7.111 Finding → Research Flow — Revised Production Evaluation Entry

Older shorthand:

~~~text
Trade / Position Terminal
↓
Post-Trade Analysis
↓
Finding Pipeline
~~~

is too narrow for NO_TRADE / Defense BLOCK.

### Revised Reference Flow

~~~text
Production Decision / Safety / Execution / Position Sources
↓
Evaluation Readiness / Source Binding

├ DecisionResultEvaluation
├ DefenseDecisionEvaluation
├ TradeResult when Position CLOSED
│  ├ OutcomeAnalysisResult
│  ├ TradeThesisEvaluation 1..N
│  │  ↓
│  │ ThesisMemberAttribution
│  ├ SupervisorEvaluation
│  └ InTradeDefenseDecisionEvaluation
├ DemoLiveDivergence when comparable
└ CounterfactualResult when evaluable

↓
Cross-Analysis Review
↓
Finding Extractor
↓
ExtractedFindingDraft
↓
Finding Normalizer
↓
Finding Type Registry
↓
Canonical Finding
↓
Candidate Promotion
↓
ResearchCandidate
↓
Research Intake
↓ ACCEPT only
Research Router
↓
ResearchRoute
↓
03_RESEARCH Routing / Prioritization
↓
Research Plan / Validation
↓
Validated Research Result
↓
04_KNOWLEDGE_APPLICABILITY
~~~

No direct Analysis → Router / Production mutation bypass is added.

---

## 7.112 Post-Trade / Finding Source Consistency — Final Checkpoint

### Consolidated New Corrections

~~~text
PT-07 Position CLOSED is the TradeResult terminal boundary candidate
PT-08 Position terminality ≠ measurement completeness
PT-09 normal Exit reason ≠ terminal close authority
PT-10 multi-selected Thesis lineage preserved through Entry / Position / TradeResult
PT-11 TradeThesisEvaluation cardinality becomes 1..N per selected Thesis
PT-12 Trade lifetime ≠ Thesis evaluation horizon
PT-13 Production analyses use readiness-driven orchestration
PT-14 DefenseDecisionEvaluation does not require TradeResult for BLOCK
PT-15 In-Trade Defense gets a distinct post-production evaluation target
PT-16 OutcomeAnalysisResult does not own Source Facts or Root Cause authority
PT-17 Execution topology is part of Demo/LIVE comparability
PT-18 7.49 direct Analysis→ResearchCandidate is superseded by 7.50 Finding Pipeline
PT-19 Post-production analysis objects are peers except ThesisEvaluation→MemberAttribution
PT-20 Source corrections propagate through immutable supersession/versioning
PT-21 DecisionResultEvaluation covers TAKE / NO_TRADE decision-quality analysis
PT-22 AnalysisSourceBinding common substructure binds exact source versions/windows
PT-23 Finding Taxonomy extension is versioned; v1.0 is not silently rewritten
~~~

### Source Object Consistency Result

~~~text
ARCHITECTURE_BREAKING_CONFLICT:
NONE FOUND

TRADE TERMINAL / POSITION TERMINAL COLLISION:
RESOLVED

MULTI-THESIS TRACE LOSS:
RESOLVED BY LINEAGE SET PRESERVATION

TRADE LIFETIME / THESIS HORIZON COLLISION:
RESOLVED BY ANALYSIS READINESS

DEFENSE BLOCK / TRADERESULT DEPENDENCY:
RESOLVED

IN-TRADE DEFENSE POST-EVALUATION GAP:
RESOLVED BY DISTINCT EVALUATION TARGET

NO_TRADE EVALUATION GAP:
RESOLVED BY DECISIONRESULT EVALUATION

POST-TRADE / FINDING PIPELINE DIRECT-BYPASS CONFLICT:
RESOLVED

FINDING TAXONOMY SOURCE GAP:
RESOLVED BY VERSIONED v1.1 EXTENSION CANDIDATE

SHARED-ORIGIN OVERCOUNT RISK:
PRESERVED / CONTROLLED BY EXISTING CROSS-ANALYSIS CONTRACT

CURRENT_03_CONFLICT_STATUS:
NONE FOUND

CURRENT_DESIGN_STATUS:
NOT_ADOPTED

REFERENCE_REVIEW_STATUS:
POST_TRADE_SOURCE_CONSISTENCY_CHECKPOINT_READY
~~~

### Object Proliferation Review

New durable analysis candidates justified:

~~~text
DecisionResultEvaluation
InTradeDefenseDecisionEvaluation
~~~

No new top-level orchestration object:

~~~text
Production Evaluation Orchestration
= processing responsibility

AnalysisSourceBinding
= common value substructure
~~~

Finding Taxonomy remains one registry family; version it instead of creating a second taxonomy system.

### Next Reference Target

Candidate next work:

~~~text
Cross-Analysis Review detailed contract
+
analysis dependency / shared-origin / conflict handling
~~~

or, if sufficient for Legacy Reference closure:

~~~text
full Legacy Reference closure review
before any Current Design adoption
~~~

Do not jump to Current adoption from this checkpoint.
