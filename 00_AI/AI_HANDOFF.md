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
2026-09-30

Conversation Focus:
Whole Market Understanding OS Reconstruction.
Phase 1 Source Extraction is complete.
Phase 2 Design Intent is checkpointed.
Current active work is Phase 3 — Capability Map.

Important Boundary:
AI_CONTEXT remains authoritative for formal Project Current State.
PROJECT_CHARTER Section 3 — What Not To Maximize remains the formal Current design focus.
The Reconstruction side-thread does NOT replace Current Architecture yet.
Current 01〜04 remain existing Working Baselines until later Reconstruction / comparison.
Legacy Reference remains historical/non-authoritative.
DAISUKE proposal remains authoritative only as the user's reconstruction source, not Final Current Design.
Phase 2 Design Intent is a WORKING RECONSTRUCTION BASELINE, not Canonical Project Philosophy.

PHASE 1:
COMPLETE
- source-by-source intent extraction
- Shared / Unique / Overlap / Gap review
- HOW concepts separated from required capabilities

PHASE 2:
COMPLETE / WORKING RECONSTRUCTION BASELINE
Key intent:
- understand market/economic/world events through relationships, not price alone
- formalize human relationship-based market reasoning for AI / Python / Database
- proactive + reactive research
- research integrity and semantic separation
- conditional knowledge, runtime applicability, economic value, risk separation
- real-capital connection without destroying capital/research/system continuity for short-term profit
- forward + reverse investigation, with reverse investigation generating Cause Candidates rather than confirming root cause
- long-term Research Asset, extensibility, human-readable output
- evaluate past decisions using information available at that time, not hindsight

Important unresolved:
- exact Survival / Profit priority
- Human / AI / Production final authority
- Capital / Portfolio philosophy
- Foundation exact scope
- Relation Language formal structure
- Research Priority
- Market extension contract
- long-term storage policy
- runtime knowledge condition monitoring

CURRENT PHASE 3 METHOD:
Translate WHY into WHAT.
For each capability record:
1. Capability ID / Name
2. Design Intent supported
3. What the OS must be able to do
4. Inputs required in meaning, not schema
5. Outputs required in meaning, not object design
6. Failure if capability is absent
7. Cross-cutting dependencies
8. Existing source support
9. Known gaps
10. HOW candidates, clearly non-binding

Do NOT:
- choose final Layers yet
- choose final Engine names
- lock Market DNA / World Economic Library / AI Team etc.
- run Destruction Review yet

NEXT:
Build Phase 3 Capability Map, beginning with top-level capability families and then decomposing each family.

READ:
- 98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
- 98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md
- 98_DESIGN_STUDY/市場理解OS_研究機関_設計検討リファレンス.md
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
- 00_HUMAN/PROJECT_CHARTER.md
- 00_HUMAN/HUMAN_MAP.md
- Current 01〜04 only when responsibility comparison is needed

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