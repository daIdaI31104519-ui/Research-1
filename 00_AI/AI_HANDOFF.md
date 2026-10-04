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
R3 Integration Repair Packages A-D and Adjacent Contract Recheck are checkpointed.
Next is STEP 8 — R3 Full Destruction Test.

WORKFLOW:
AI_WORKFLOW v0.5.3 Precision-First → Precision Review → Human View workflow is active.

LATEST SAVED CHECKPOINT:
Checkpoint 021 — R3 Adjacent Contract Recheck / Cross-Cutting Contract Repair

PRIMARY:
98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md

CHECKPOINT 021 RESULT:
- R3-ADJ-001 Artifact Current-Use Validity Common Contract = REPAIRED / WORKING
- R3-ADJ-002 Evaluation Requirement Profile Governance = REPAIRED / WORKING
- R3-ADJ-003 Trade Thesis Adoption Contract Governance = REPAIRED / WORKING
- R3-ADJ-004 Multi-Domain Return / Minimal Semantic Owner Set = REPAIRED / WORKING
- Adjacent Contract Cross Check = PASS
- Blocking Issue = NONE
- Formal Current Architecture = UNCHANGED

R3-ADJ-001 CORE:
Historical Integrity
!= Current-Use Validity.

CUV is:
Exact Artifact
+ Intended Use
+ Context
+ As-Of / Cutoff
+ Material Dependency
+ Policy / Method Version.

UNDETERMINED
!= VALID.

CUV Result
!= Return Route
!= Action.

CUV is artifact-domain-owned under one common contract,
not a universal central truth engine.

R3-ADJ-002 CORE:
Evaluation Requirement Profile
= versioned Economic Evaluation Policy Contract.

Economic Evaluation Requirement Governance
owns:
what must be evaluated for sufficiency.

EVA / EAS / Advancement / R4 / Runtime / AI
must not author active requirements ad hoc.

Requirement Profile Resolver selects exact applicable basis.
Profile composition is explicit.
No silent fallback.
Research Sufficiency != Production Sufficiency.

R3-ADJ-003 CORE:
Trade Thesis Adoption Contract
= versioned Reasoning Integrity Contract.

Trade Thesis Adoption Contract Governance
owns:
what Formation Result must satisfy
to become a formal R3 Trade Thesis for R4.

Advancement Policy
!= Formation Policy
!= Adoption Contract
!= R4 Capital Contract.

Adoption Contract checks:
Exact refs,
CUV,
Temporal integrity,
Semantic preservation,
Unknown / Dependency preservation,
R4 handoff completeness.

Adoption Contract does not re-decide:
Economic attractiveness,
Sufficiency,
Unknown acceptance,
ADVANCE / WAIT / ABSTAIN,
Capital Permission.

Trade Thesis now preserves:
exact Adoption Contract basis,
Adoption Assessment ref,
Adoption Authorization ref.

R3-ADJ-004 CORE:
One Source Event
may produce multiple Atomic Findings.

Finding Count
!= Return Count.

Minimal Semantic Owner Set
= smallest non-redundant owner set
covering all material findings.

Upstream route may subsume downstream route
only when normal forward rebuild necessarily regenerates
the affected downstream semantics.

Independent semantic owner remains separate.

Actual Exposure Safety
is an independent fast route
and is never subsumed by slow semantic repair.

Route relations:
SEQUENTIAL / PARALLEL / SUBSUMED.

Required Join Point is explicit
when material slow routes must converge.

ADJACENT NON-BLOCKING CLARIFICATIONS:
ADJ-HO-001 CUV policy is domain-owned; common invariants cannot be weakened.
ADJ-HO-002 No recursive CUV-of-CUV chain.
ADJ-HO-003 Return Routing Group must not deadlock on circular waits.
ADJ-HO-004 Join resumes only from exact available current-use-valid repaired outputs.

R3 STATUS:
Package A = checkpointed.
Package B = checkpointed.
Package C = checkpointed.
Package D = checkpointed.
Adjacent Contract Recheck = checkpointed.
R3 Integration Blocking Issue = NONE.

FORMAL BOUNDARY:
AI_CONTEXT remains authoritative for Formal Project Current State.
00_HUMAN/HUMAN_MAP.md unchanged.
02_ARCHITECTURE/ unchanged.
Checkpoint 021 remains Working Repair, not formal adoption.

NEXT:
STEP 8 — R3 Full Destruction Test
→ R3 Integration Final Review
→ Formal Adoption Decision later.

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