# 旧市場理解OS — 設計知識リファレンス

**Document Role:** Legacy Knowledge Master Index / Comparison Reference  
**Status:** DRAFT / REFERENCE CONTENT NOT YET POPULATED  
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
| まとめ案 1〜11 | NOT_REVIEWED | Legacy全体像 |
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
| `市場理解OS まとめ案 1.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 2.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 3.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 4.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 5.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 6.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 7.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 8.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 9.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 10.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
| `市場理解OS まとめ案 11.md` | LEGACY_SUMMARY | NOT_REVIEWED | `<TODO>` |
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
SKELETON
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
