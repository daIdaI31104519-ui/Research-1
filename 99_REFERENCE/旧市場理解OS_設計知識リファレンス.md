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
