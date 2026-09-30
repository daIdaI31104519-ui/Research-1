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
Phases 1-4 checkpointed.
Phase 5 R1 / R2 / R3 concept-level reconstruction complete.
Current active work: R4 Capital / Production.

Important Boundary:
AI_CONTEXT remains authoritative for formal Project Current State.
Formal Current Architecture is unchanged.
Phase 5 candidates are not adopted design.

PHASE 5 RESPONSIBILITY SKELETON:
R1 Perception / Relation / Current Understanding
R2 Research
R3 Knowledge / Applicability / Decision Preparation
R4 Capital / Production
R5 Learning / Feedback
R6 Long-Term Foundation / Operations / Human Projection
X Cross-Cutting

R3 KEY RECONSTRUCTION:
- Foundation and Research Knowledge remain separate epistemic domains
- Validated Research Result does not auto-promote to Knowledge
- Knowledge Admission / Formation replaces ambiguous Production-like promotion meaning
- Knowledge stores conditional semantics: conditions, failure boundaries, uncertainty, market/horizon, version, validation history
- positive, negative, no-edge, refutation, failure/boundary, constraint, unknown knowledge remain valuable
- Knowledge Pool/Library is a logical domain; Knowledge Graph is only a possible derived view
- Knowledge Lifecycle is separate from Runtime Applicability
- Lifecycle Assessment is separate from authoritative state transition
- old/stale does not mean false; revalidation can be requested
- Constraint is split into Research Constraint Candidate / Knowledge Constraint / Runtime Authorized Constraint
- Applicability remains current-usability assessment, not Trade
- Runtime Assumption Monitoring is separated from pre-decision applicability and cannot rewrite Knowledge
- Knowledge Conflict Detection is separate from Conflict Resolution
- shared evidence / dependency prevents knowledge-count majority voting
- Decision Synthesis / Conflict Resolution is a distinct R3 responsibility
- legacy Trade Thesis is broadened toward Decision Thesis / Action Candidate because WAIT / NO TRADE / REDUCE / UNKNOWN are valid
- Decision Scope / Horizon is explicit
- Economic Value is separate from Applicability and Capital Permission
- EV should retain distribution / uncertainty / costs, not only one average
- Signal Engine is dropped as a required top-level concept
- R3 outputs a traceable Economic Decision Candidate to R4, not Capital Permission or OrderIntent

R3 TWO-SPEED:
Slow:
Validated Research Result → Knowledge Admission / Version / Lifecycle

Fast:
Existing Knowledge + Current Context → Applicability → Decision Synthesis → EV

Active Runtime:
Knowledge assumptions + Runtime Context → Deviation assessment → R4 Fast Safety / R5 Feedback

NEXT — R4:
Reconstruct:
1. Capital state / portfolio view
2. risk budget / allocation
3. drawdown / ruin protection
4. Decision vs Risk Permission
5. authorized constraints
6. fast safety / emergency restriction
7. recovery / permission expansion
8. execution intent
9. order submission / fill / reconciliation
10. logical position / exposure truth
11. position protection / exit
12. AI/API/exchange failure boundaries
13. R4 → R5 outcome evidence

Do NOT:
- adopt Phase 5 candidates as final architecture
- finalize DB/Object/Python
- let EV grant capital permission
- let runtime monitoring rewrite Knowledge
- modify formal Current Architecture
- run Phase 6 destruction review early

READ:
- 98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
- 98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md
- 00_HUMAN/PROJECT_CHARTER.md

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