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
旧市場理解OS Referenceの05_DECISION Final Checkpoint後を継続し、
Defense Admission → Defense Evaluation → Risk Governance →
Emergency / Recovery → Defense→Execution / Barrier C
まで詳細Reference設計を進めた。

Important Boundary:
This does NOT change Project Current Task.
AI_CONTEXT remains authoritative for Current Project state.
Current Design adoption has NOT occurred.

DONE:
- 05_DECISION Reference remains SEMANTICALLY_CLOSED_CANDIDATE.
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
  Sections 7.88–7.96 saved.
- Post-05 Defense / Risk / Entry boundary reconciliation completed as Reference checkpoint.
- No architecture-breaking conflict found.
- Major corrections saved:
  Defense Admission responsibility separation,
  process/outcome separation,
  RiskState / Constraint version barriers,
  Emergency restriction vs Recovery authority separation,
  Barrier C1/C2,
  EntryThesis / OrderIntent validity candidates,
  Submission Gate processing boundary.
- Emergency scope correction:
  use smallest safe scope, but expand for shared dependency / unknown blast radius.
- Risk-reducing action correction:
  intent alone is insufficient; venue/execution semantics must prevent accidental exposure increase.

UNSAVED:
None for the checkpoint above.

OPEN:
- This remains Reference only; Current adoption requires separate review later.
- Exact thresholds, TTLs, IAM actors, retry/backoff, reconciliation algorithm,
  order event model and multi-exchange routing intentionally remain unresolved.

NEXT:
Continue Legacy Reference detailed design from:
Open Order Runtime Lifecycle
→ Retry / Idempotency / Reconciliation
→ Split Execution Lifecycle
→ Position creation / Position identity
→ Exit / Protection lifecycle as needed.

READ:
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
  especially 7.88–7.96 and prior 7.36–7.40
- 00_AI/AI_CONTEXT.md
  only to preserve separation between Current Project state and this Reference side-thread

Last Reference Checkpoint Commit:
e9f30186dea98ae2ec9301216e5a3e0d29dd3a09

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