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
2026-09-29

Conversation Focus:
Whole Market Understanding OS Reconstruction.
Current active work is Phase 1 — Source Extraction.

Important Boundary:
AI_CONTEXT remains authoritative for formal Project Current State.
PROJECT_CHARTER Section 3 — What Not To Maximize remains the formal Current design focus.
The Reconstruction side-thread does NOT replace Current Architecture yet.
Current 01〜04 remain existing Working Baselines until later Reconstruction / comparison.
Legacy Reference remains historical/non-authoritative.
DAISUKE proposal is authoritative only as the user's reconstruction source, not as Final Current Design.

RECONSTRUCTION SOURCES:
1. 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
2. Current PROJECT_CHARTER / HUMAN_MAP / 01〜04 Working Baselines
3. 98_DESIGN_STUDY/市場理解OS_研究機関_設計検討リファレンス.md
4. 98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md

CURRENT METHOD:
Do NOT compare by Layer / Engine / Object names first.
Extract:
- why each responsibility existed
- what capability it tried to create
- what it tried to protect
- what is lost if removed
- where responsibilities overlap
- whether it is WHY / WHAT / HOW

CURRENT HIGH-LEVEL EXTRACTION:
Legacy:
- strong at separating observation / interpretation / cause / research / production
- strong at reactive anomaly, causal, stress, failure, defense, execution, feedback
- strong at research evidence separation and failure routing
- weaker / incomplete at proactive foundation-driven research and some canonical ownership

Current:
- strong at Human-First semantics and responsibility boundaries
- strong at qualified observation → current understanding → research → knowledge → applicability
- strong at Research Result ≠ Knowledge ≠ Applicable ≠ Trade
- Decision / Execution remain incomplete

Research Institute Reference:
- adds proactive + reactive Dual-Entry / Single-Core
- adds Research Foundation, Research Question, Open Discovery
- adds Exploratory / Confirmatory / Replication distinction
- adds Research Ledger, Red Team, Benchmark, Negative Knowledge emphasis
- remains Working Reference, not Current Design

Daisuke Proposal:
- adds relationship-based human market understanding as a formal machine-readable idea
- adds world / market foundation and common relation language
- separates world/economic foundation library from OS-derived knowledge library
- adds forward research + reverse investigation from unexpected results
- emphasizes real-capital safety, runtime market support, long-term storage, modular replacement, multi-market expansion, human-readable research asset

PHASE 1 GOAL:
Convert the four sources into a source-extraction map of required capabilities and preserved design intents.
Do NOT yet decide final Architecture.
Do NOT yet run Destruction Review.
Do NOT yet assign KEEP / DROP except as later reconstruction work.

NEXT:
Continue Phase 1 by building:
1. source-by-source intent extraction
2. shared capabilities
3. unique capabilities
4. overlaps / gaps
5. HOW concepts that must not be mistaken for required capabilities

READ:
- 98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
- 98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md
- 98_DESIGN_STUDY/市場理解OS_研究機関_設計検討リファレンス.md
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
- 00_HUMAN/PROJECT_CHARTER.md
- 00_HUMAN/HUMAN_MAP.md
- 02_ARCHITECTURE/CONNECTIONS/01_EXTERNAL_DATA.md
- 02_ARCHITECTURE/CONNECTIONS/02_MARKET_UNDERSTANDING.md
- 02_ARCHITECTURE/CONNECTIONS/03_RESEARCH.md
- 02_ARCHITECTURE/CONNECTIONS/04_KNOWLEDGE_APPLICABILITY.md

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