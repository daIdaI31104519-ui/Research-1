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
2026-09-26

Conversation Focus:
Formal Current Architecture redesign preparation side-thread.
Research Institute design study has been consolidated and saved as a non-authoritative Working Reference.

Important Boundary:
AI_CONTEXT remains authoritative for Project Current State.
PROJECT_CHARTER Section 3 — What Not To Maximize remains the formal Current design focus.
This side-thread does NOT replace Current Architecture yet.
Current 01〜04 remain existing Working Baselines until later comparison / redesign.
Legacy Reference remains historical/non-authoritative.

DONE:
- Re-examined Research Institute using:
  Current Git
  Current 01〜04 Connection Maps
  HUMAN_MAP / PROJECT_CHARTER
  Legacy Reference
  recent user research philosophy
- Identified current strength:
  Reactive / diagnostic / validation research is already comparatively strong
- Identified current weakness:
  Proactive / exploratory research before anomaly/failure is weak
- Developed Dual-Entry / Single-Core Research direction
- Added Research Foundation concept
- Added Research Question before Research Candidate as a design candidate
- Clarified candidate roles for:
  Market Foundation
  Open Discovery
  Cause Candidate
  Hypothesis
  Market DNA
  Research Mode
  Research Ledger
  Red Team / Independent Challenge
  Research Synthesis
  Validated Research Result
- Reconfirmed boundaries with:
  External Data
  Market Understanding
  Knowledge
  Applicability
  Decision
  Risk / Defense
  Execution
  Production Evaluation
- Saved design study reference:
  98_DESIGN_STUDY/市場理解OS_研究機関_設計検討リファレンス.md
- Saved document status:
  WORKING REFERENCE / NOT CURRENT DESIGN / NOT CANONICAL

UNSAVED:
None for the current Research Institute study checkpoint.

OPEN:
- Research Foundation exact scope
- Foundation fact / mechanism / model / heuristic distinction
- Proactive Research exact entry conditions
- Research Question / Candidate boundary
- Research Domain / Intent / Mode / Method taxonomy
- Market DNA / Cause Candidate / Hypothesis exact responsibility placement
- Research Ledger / Red Team exact authority
- Later whole-OS major-category redesign
- Later comparison against Current 01〜04
- Later KEEP / REDESIGN / DROP / MERGE decision

NEXT:
Continue the Design Study before formal Architecture replacement.

Recommended next study:
Research Foundation
- what belongs in it
- what must not belong in it
- how it reduces noise without suppressing original discovery

READ:
- 98_DESIGN_STUDY/市場理解OS_研究機関_設計検討リファレンス.md
- 00_HUMAN/PROJECT_CHARTER.md
- 00_HUMAN/HUMAN_MAP.md
- Current 01〜04 only when comparison is needed
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md only when Legacy comparison is needed

Design Study Save Commit:
d44efa101b68190e8b45416d01167366ab18ab9a

Design Study Content SHA:
d7fad4c18e0a1db7574c8d62a6bc170174db449a

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