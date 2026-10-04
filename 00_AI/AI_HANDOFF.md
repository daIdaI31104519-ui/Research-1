# 市場理解OS — AI HANDOFF v0.2

**Document Role:** Short-Term Conversation Delta / Handoff Bridge  
**Status:** REVIEWED / WORKING BASELINE  
**Purpose:** Chat切替・Context Limit・別AIへの交代時に、`AI_CONTEXT.md` では分からない直前Conversationの差分だけを短時間で復元する。

---

# 0. CURRENT HANDOFF

~~~text
State:
ACTIVE

Last Updated:
2026-10-04

Conversation Focus:
Whole Market Understanding OS Reconstruction.
R3 Integration Repair is active.
Packages A, B and C are checkpointed.
Package D — Economic / Trade Exit is next.

WORKFLOW:
AI_WORKFLOW v0.5.3 Precision-First → Precision Review → Human View workflow is active.

LATEST SAVED CHECKPOINT:
Checkpoint 019 — R3 Integration Repair / Package C — Decision Contract & Decision Lineage

PRIMARY:
98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md

CHECKPOINT 019 RESULT:
- R3-INT-004 Decision Candidate Contract = REPAIRED / WORKING
- R3-INT-008 Unknown Identity / Treatment = REPAIRED / WORKING
- R3-INT-009 Dependency / Independence Provenance = REPAIRED / WORKING
- R3-INT-010 Decision Synthesis Result / Decision Thesis Boundary = REPAIRED / WORKING
- R3-INT-011 Candidate Advancement Governance / Terminology = REPAIRED / WORKING
- Decision Lineage Contract = ADDED / WORKING
- Package C Cross Check = PASS
- Blocking Issue = NONE
- Formal Current Architecture = UNCHANGED

PACKAGE C CORE FLOW:
Decision Material Snapshot
→ Decision Synthesis Result
→ Decision Thesis
→ Decision Candidate
→ Economic Value Assessment
→ Candidate Advancement Record
→ Trade Thesis Formation.

This is not a one-to-one pipeline.
It is a branching immutable Decision Lineage DAG.

R3-INT-004 CORE:
Decision Candidate
= meaning-fixed Action Option evaluated by Economic Value.

Candidate semantics include:
Target / Instrument / Exposure Intent / Objective / Horizon /
Evaluation Baseline Specification / Preconditions /
Candidate Invalidation / Critical Unknown refs /
Decision Thesis lineage / Decision Context.

Candidate semantics
!= EVA Context.

Economic Value must not repair / invent missing Candidate semantics.

R3-INT-008 CORE:
Unknown Source / Finding
!= downstream Treatment.

Unknown existence
!= Criticality.

UNKNOWN
!= FALSE / ZERO / 50%.

Accepted Unknown
!= Resolved Unknown.

Downstream layers preserve source Unknown identity.

R3-INT-009 CORE:
Semantic Relationship
!= Dependency.

Provenance Fact
!= Dependency Assessment.

No known dependency
!= Proven independence.

Independence is dimension-scoped and requires explicit Independence Basis.

Decision Dependency
!= Cross-Candidate Economic Dependency.

R3-INT-010 CORE:
Decision Synthesis Result
= one whole synthesis event.

Decision Thesis
= one immutable Snapshot-bound Market Judgment.

Decision Thesis Candidate
= deprecated unless a real promotion boundary is later introduced.

THESIS_FORMED
→ one or more Formal Theses.

INCONCLUSIVE
→ zero Formal Theses.

Synthesis Outcome
!= Thesis Set Structure.

R3-INT-011 CORE:
PROCEED
→ deprecated.

ADVANCE
= preferred Candidate Advancement term.

Candidate Advancement Disposition:
ADVANCE / WAIT / ABSTAIN.

Disposition belongs to immutable Candidate Advancement Record,
not mutable Candidate state.

Candidate Advancement Policy must be explicit / versioned.

Positive EV != Automatic ADVANCE.
Negative Standalone EV != Automatic ABSTAIN for Hedge / Insurance.

WAIT requires Re-evaluation Trigger + Route.
WAIT != R4 HOLD.
ABSTAIN != Knowledge / Thesis refutation.
ADVANCE != Trade Permission / Capital Permission.

DECISION LINEAGE:
Decision Lineage is a cross-cutting trace concept,
not a new R3 layer or truth owner.

Exact Parent / Source Artifact refs
= canonical lineage basis.

Decision Lineage ID
= correlation / traversal aid only.

Decision Lineage may branch.

Historical artifacts are immutable.

Current-use validity is artifact-specific,
not one universal Lineage state.

Material Unknown must be carried forward by exact ref
or explicitly treated as non-material.

Downstream cannot use a required upstream artifact
before that artifact became available.

Retrospective / Counterfactual artifacts
must not masquerade as Original Decision Lineage descendants.

PACKAGE D CROSS-PACKAGE DEPENDENCIES:
R3-INT-005
Evaluation Availability / Sufficiency.

R3-INT-012
Trade Thesis immutable revision / adoption.

R3-INT-014
Backward Return Router common rule.

FORMAL BOUNDARY:
AI_CONTEXT remains authoritative for Formal Project Current State.
00_HUMAN/HUMAN_MAP.md unchanged.
02_ARCHITECTURE/ unchanged.
Checkpoint 019 remains Working Repair, not formal adoption.

NEXT:
Repair Package D — Economic / Trade Exit.

FIRST TARGET:
R3-INT-005 — Evaluation Availability / Sufficiency.

Git Write Permission Reminder:
REQUIRE CURRENT-CHAT USER AUTHORIZATION
~~~

---
# 1. ROLE

```text
AI_CONTEXT
=
長期Project Current State

AI_HANDOFF
=
Latest Conversation Delta
```

`AI_HANDOFF.md` は、

```text
Current Design
Project Constitution
Long-Term Pending List
History Log
Git Write Authority
```

の正本ではない。

Project全体の現在地は、

```text
00_AI/AI_CONTEXT.md
```

を確認する。

Cold Start / Recovery順は、

```text
00_AI/AI_START_HERE.md
```

を正本とする。

作業方法・Git書込許可・HANDOFFを更新すべき条件は、

```text
00_AI/AI_WORKFLOW.md
```

を正本とする。

---

# 2. STATE MEANING

```text
ACTIVE
=
次のAIへ引き継ぐべきConversation Deltaがある

CLEAR
=
特別なConversation Deltaなし
AI_CONTEXTから再開可能
```

---

# 3. FIELD MEANING

## NOW

```text
今このConversationで何をしているか
```

Project全体のCurrent Taskを再定義しない。

```text
Conversation Focus
≠
Project Current Task
```

## DONE

```text
直前Conversationを理解するために必要な最近の完了事項
```

長期履歴として蓄積しない。
不要になったDONEは次回更新時に削除する。

## UNSAVED

```text
会話では合意・設計されたが
まだGitへ保存されていない重要事項
```

重要:

```text
UNSAVED
≠
Current Design
```

Chat切替時に最も失われやすい差分を保持する。

## OPEN

```text
まだ決まっていないConversation固有の事項
```

新しいAIはOPENを推測で確定しない。
不要・解決済みになったOPENは削除する。

## NEXT

```text
次のAIが最初に行う具体的な作業
```

単に、

```text
続きをやる
```

だけにはしない。

## READ

```text
今回のConversationを再開するために追加で読む必要があるFile
```

だけを書く。

Cold Startの固定読込順をここへ複製しない。
Cold Start順は `AI_START_HERE.md` を正本とする。

---

# 4. MAINTENANCE RULE

`AI_HANDOFF.md` は日記ではない。

```text
AI_HANDOFF
=
常に最新Conversation Snapshot
```

とする。

更新時:

```text
Old Conversation Snapshot
↓
Current Conversation Snapshot
```

へ置換する。

過去Snapshotを追記し続けない。

長期的に残す必要がある情報は、その責任に応じて、

```text
Current Design
AI_CONTEXT
HISTORY
Git History
```

へ移る。

AI_HANDOFFを更新すべき条件自体は、

```text
00_AI/AI_WORKFLOW.md
```

を正本とする。

重要:

```text
AI_WORKFLOW
=
WHEN to update

AI_HANDOFF
=
HOW / WHAT to hold
```

---

# 5. CLEAR STATE

次Chatへ引き継ぐ固有のConversation Deltaが無い場合、HANDOFFを無理に埋めない。

最小状態:

```text
State:
CLEAR

No unique conversation state to transfer.

Resume From:
00_AI/AI_CONTEXT.md

Git Write Permission Reminder:
REQUIRE CURRENT-CHAT USER AUTHORIZATION
```

---

# AI_HANDOFF v0.2 一文定義

> **AI_HANDOFFとは、市場理解OSの長期Current Stateや作業規則を保存する文書ではなく、AI_CONTEXTでは把握できない直前Conversationの最新差分だけを短く保持し、Chat切替・Context Limit・AI交代後も現在の会話地点を安全に復元するためのLatest Conversation Snapshotである。**