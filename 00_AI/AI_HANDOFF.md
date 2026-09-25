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
2026-09-25

Conversation Focus:
Legacy Reference Closure side-thread.

Phase 1〜7 Closure Review、
Closure Documentation Sections 4 / 5 / 6 / 8 / 9 / 10 / 11、
FIX-001〜018C Review、
Dictionary major-concept Closure Reviewを完了し、
Pre-Governance CheckpointとしてReferenceへ保存した。

Important Boundary:
This does NOT change Project Current Task.
AI_CONTEXT remains authoritative for Current Project state.
Current Design adoption has NOT occurred.

DONE:
- Phase 1 Whole Architecture Flow Review
- Phase 2 Responsibility / Authority Review
- Phase 3 Object / Source-of-Truth Review
- Phase 4 Trace / Dependency / Circularity Review
- Phase 5 Deferred Register
- Phase 6 KEEP / REDESIGN / DROP / DEFER
- Phase 7 Final Closure Gate
- Section 4 Legacy Whole-System Overview saved
- Section 5 Legacy Concept Index saved
- Section 6 Legacy → Current Concept Map saved
- Section 8 FIX / Failure Index saved
- Section 9 Important Legacy Design Lessons saved
- Section 10 Legacy Revisit Index saved
- Section 11 Unknown / Unresolved saved
- Dictionary major Concept supplement saved
- Source Review Progress / Source Pointer synchronized
- FIX-001〜018C marked REVIEWED
- OBJECT / ROLE / STATE Dictionary = PARTIAL major-concept review
- SECURITY / CREDENTIAL / DATA_CLASSIFICATION = REVIEWED
- 7.40 / 7.49 / 7.56 marked LEGACY_FLOW_STATUS: SUPERSEDED
- Architecture-breaking conflict: NONE FOUND
- Legacy major Unknown Register: 8 items
- Current Design remains NOT_ADOPTED

UNSAVED:
None for this Pre-Governance Closure checkpoint.

OPEN:
- Legacy Governance Source Review:
  00_GOVERNANCE/DESIGN_CHANGE_RULES.md
  00_GOVERNANCE/GIT_RULES.md
- Final Reference Completion State after Governance review
- Section 14 INITIAL_REFERENCE_COMPLETE decision
- Current adoption remains a separate later task

NEXT:
LEGACY GOVERNANCE SOURCE CLOSURE REVIEW

Review:
1. DESIGN_CHANGE_RULES.md
2. GIT_RULES.md
3. Extract only reusable governance lessons / conflicts
4. Update Section 3 / 12 source statuses
5. Check whether any new Revisit / Unknown item is required
6. Re-evaluate Section 14 completion gate

READ:
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
  especially Sections 3–12 and 14
- Legacy:
  00_GOVERNANCE/DESIGN_CHANGE_RULES.md
  00_GOVERNANCE/GIT_RULES.md
- 00_AI/AI_CONTEXT.md
  only to preserve separation from Current Project state

Last Reference Checkpoint Commit:
9871acc07a75ed428c7e05b199630a96329c64ec

Reference Content SHA:
c62ead395fe0cf826f764f869e535523712e033a

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