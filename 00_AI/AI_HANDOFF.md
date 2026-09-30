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
Phases 1-4 are checkpointed.
Current active work is Phase 5 — Reconstruction.

Important Boundary:
AI_CONTEXT remains authoritative for formal Project Current State.
PROJECT_CHARTER Section 3 — What Not To Maximize remains the formal Current design focus.
The Reconstruction side-thread does NOT replace Current Architecture yet.
Current 01〜04 remain existing Working Baselines until Phase 5 comparison / redesign.
Legacy Reference remains historical/non-authoritative.
DAISUKE proposal remains authoritative only as the user's reconstruction source, not Final Current Design.
Phase 2 / 3 / 4 are WORKING RECONSTRUCTION BASELINES.

PHASE 4 CANDIDATES:
A Research-Centered
B Relation / World-Model-Centered
C Knowledge-Loop-Centered
D Multi-Core Hybrid

PHASE 4 STRESS RESULT:
- A is strongest as Research-domain design philosophy, but whole-OS use risks research overreach / latency
- B is strongest for relation-based market understanding and multi-market semantics, but whole-OS use risks world-model / ontology explosion
- C is strongest for long-term knowledge lifecycle and publication, but whole-OS use risks known-knowledge bias
- D gives the clearest whole-OS responsibility separation and failure routing, but risks contract/object/state bureaucracy
- no candidate is adopted yet

CROSS-CASE PRINCIPLES SENT TO PHASE 5:
1. Relation/Foundation may be shared market-understanding language, not truth authority
2. Research may be common research core, not runtime authority
3. Knowledge may be long-term semantic asset, not exclusive perception lens
4. Capital/Production needs independent real-capital authority boundary
5. Feedback routing needs cross-domain failure classification
6. X01-X11 should remain horizontal capabilities/governance rather than normal sequential layers
7. Whole OS likely needs two speeds:
   Evidence/Learning path
   Runtime/Safety path
8. Human-readable publication should be derived projection, not internal source of truth

PHASE 5 GOAL:
Compare and reconstruct:
- Legacy concepts
- Current responsibilities
- Daisuke proposal concepts
- Research Institute concepts
- Phase 4 architecture learnings

Use:
KEEP
REDESIGN
SPLIT
MERGE
DROP
DEFER
NEW

Do not preserve names automatically.
For every important concept record:
- original intent
- current problem
- capability served
- reconstruction decision candidate
- replacement / merge target
- what would be lost

NEXT:
Start Phase 5 with top-level responsibility reconstruction before individual object design.

Recommended first pass:
1. Perception / Relation / Current Understanding
2. Research
3. Knowledge / Applicability / Decision
4. Capital / Production
5. Feedback
6. Cross-Cutting / Operations / Human Output

Do NOT:
- finalize DB/Object/Python
- assume Candidate D wholesale
- run Phase 6 Destruction Review yet
- modify formal Current Architecture without explicit adoption

READ:
- 98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
- 98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md
- 98_DESIGN_STUDY/市場理解OS_研究機関_設計検討リファレンス.md
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
- 00_HUMAN/PROJECT_CHARTER.md
- Current 01〜04 for Phase 5 comparison

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