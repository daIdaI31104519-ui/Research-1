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
Package A and Package B are checkpointed.
Package C — Decision Contract is next.

WORKFLOW:
AI_WORKFLOW v0.5.3 Precision-First → Precision Review → Human View workflow is active.

LATEST SAVED CHECKPOINT:
Checkpoint 018 — R3 Integration Repair / Package B — Temporal / Reproducibility

PRIMARY:
98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md

CHECKPOINT 018 RESULT:
- R3-INT-002 Temporal / Look-Ahead Contract = REPAIRED / WORKING
- R3-INT-003 Decision Material Snapshot Contract = REPAIRED / WORKING
- Package B Cross Check = PASS
- Blocking Issue = NONE
- Formal Current Architecture = UNCHANGED

PACKAGE B CORE:
Event / Domain Time
!= Source Available Time
!= System Information Available Time
!= As-Of / Information Cutoff
!= Assessment / Decision Time
!= Effective Time.

Historical Decision eligibility uses:
input.system_available_at <= information_cutoff.

Event Time alone is insufficient.

Historical Reconstruction
!= Retrospective / Counterfactual Analysis.

Derived information cannot be available before its material dependencies.

Later correction / Model / Policy / Relationship / Constraint / Lifecycle information
must not rewrite Past Decision Context.

Decision Material Snapshot:
= immutable Decision Input Boundary.

Decision Context must pin:
Target / Scope / Relevant Horizon / Decision As-Of.

Snapshot temporal header:
Decision As-Of / Information Cutoff / Sealed At are distinct.

Snapshot logical blocks:
A Identity / Decision Context
B Market Context
C ACTIVE INPUT
D Cross-Knowledge Context
E TRACE ONLY / Excluded / Blocked / Unknown Trace
F Integrity / Seal Trace

ACTIVE INPUT
!= TRACE ONLY.

TRACE ONLY:
may affect sufficiency / audit,
must not become directional support/opposition.

Snapshot Assembler
!= Decision Material Eligibility Authority.

Snapshot Sealer
= integrity authority,
not semantic truth authority.

Sealed Snapshot is immutable.

Historical Snapshot Integrity
!= Current-Use Validity.

Material current-use invalidation
→ new Snapshot,
not mutation.

Decision Synthesis consumes the sealed Snapshot
and does not silently re-query moving Current state.

PACKAGE B CLARIFICATIONS:
PB-HO-001
Snapshot Seal Success != Decision Sufficiency.

PB-HO-002
Original Snapshot Replay != Historical Reconstruction.

PB-HO-003
Exact Ref must resolve to immutable / historically reconstructable revision.

FORMAL BOUNDARY:
AI_CONTEXT remains authoritative for Formal Project Current State.
00_HUMAN/HUMAN_MAP.md unchanged.
02_ARCHITECTURE/ unchanged.
Checkpoint 018 remains Working Repair, not formal adoption.

NEXT:
Repair Package C — Decision Contract.

FIRST TARGET:
R3-INT-004 — Decision Candidate Contract Backfill.

Then:
R3-INT-008 Unknown identity / treatment
R3-INT-009 Dependency / independence provenance
R3-INT-010 Synthesis Result / Decision Thesis boundary
R3-INT-011 Candidate Advancement governance / terminology

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