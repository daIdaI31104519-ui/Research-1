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
Legacy Reference side-thread.
Cross-Analysis Review詳細Contract、
Shared Origin / Dependency / Conflict Handlingを横断Reviewし、
CA-01〜CA-27を8テーマへ重複整理してCheckpoint保存した。

Important Boundary:
This does NOT change Project Current Task.
AI_CONTEXT remains authoritative for Current Project state.
Current Design adoption has NOT occurred.

DONE:
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
  Sections 7.113–7.125 saved.
- Cross-Analysis placementを
  Analysis Results → CrossAnalysisReviewResult → Finding Extractor
  へ固定候補化。
- v1 Review Scopeを1 Production Evaluation Episode中心へ固定候補化。
- Shared Origin / Dependency / Common Causeを分離。
- Analysis / Finding / Trade count ≠ Independent Evidence countを明示。
- Structural mismatchをSemantic Conflictより先に処理する順序を固定。
- Responsibility Chain ≠ Causal Chainを固定。
- CrossAnalysisReviewResultを唯一の新Durable candidateとして整理。
- SharedOriginRef / DependencyEdge / ConflictRecord等はChild/Value structureへ圧縮。
- Cross-Analysis Reviewをincremental/versionedにし、Source supersession時の
  selective re-analysis impact detection候補を追加。
- CA-01〜CA-27を8 governing themesへ統合。
- Architecture-breaking conflict: NONE FOUND.
- Current Design remains NOT_ADOPTED.

UNSAVED:
None for this Cross-Analysis detailed checkpoint.

OPEN:
- Full Legacy Reference Closure Review.
- Exact DB/schema/graph storage/thresholds remain intentionally deferred.
- Exact CROSS_ANALYSIS taxonomy governance remains deferred.
- Current adoption requires separate review later.

NEXT:
OLD MARKET-UNDERSTANDING-OS
FULL LEGACY REFERENCE CLOSURE REVIEW

Closure Review targets:
1. Whole architecture flow
2. Duplicate / redundant responsibilities
3. Object proliferation
4. Authority collisions
5. Source-of-Truth conflicts
6. Trace discontinuities
7. Circular dependencies
8. Deferred items
9. Current adoption candidates
10. KEEP / REDESIGN / DROP / DEFER candidates
11. Legacy Reference closure state

READ:
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
  especially 7.113–7.125,
  plus 7.41–7.56, 7.97–7.112
- 00_AI/AI_CONTEXT.md
  only to preserve separation between Current Project state and this Reference side-thread

Last Reference Checkpoint Commit:
acc321fe7bd4764892d0a51bfb4ace7e0abb6891

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