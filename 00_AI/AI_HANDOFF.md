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
Phase 5 R1, R2, R3 concept-level reconstruction complete.
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
- R3 split conceptually into Knowledge Maintenance, Applicability/Runtime Assumption, Decision Preparation/EV
- Foundation and Research Knowledge remain separate epistemic categories
- Validated Research Result does not automatically become Knowledge
- Knowledge Admission may produce Knowledge, merge/update candidate, Research Asset only, or no Knowledge admission
- Negative/refutation/boundary knowledge retained; pure inconclusive/process-limited results need not become Knowledge claims
- Knowledge semantics remain conditional and versioned
- Knowledge relationships separated from Knowledge semantics; Knowledge Graph becomes derived view candidate
- Knowledge Lifecycle separated from Applicability
- Revalidation routes back to R2; R3 does not self-research
- Research Constraint Candidate / Knowledge Constraint / Runtime Authorized Constraint separated
- Knowledge Retrieval added before Applicability; retrieved does not mean applicable
- Applicability remains current-usability assessment and records excluded-knowledge reasons
- Runtime Assumption Monitoring split from pre-decision applicability but shares semantics
- Runtime deviation cannot directly mutate Knowledge or decide exit
- Multi-Knowledge Conflict/Dependency/Overlap explicitly retained
- Decision Synthesis added between Applicability and EV
- Trade Thesis renamed/deferred; responsibility retained as traceable Decision Thesis candidate
- Expected Value separated from Applicability and Capital Permission
- R3 outputs Economic Opportunity / Decision Proposal context to R4, not Order Intent
- Signal Engine not required top-level concept
- BUY/SELL-only canonical decision outcome dropped
- WAIT / NO ACTION / UNKNOWN / conflicted states remain valid candidates

R3 CANDIDATE FLOW:
Validated Research Result
→ Knowledge Admission
→ Knowledge Version/Lifecycle
→ Knowledge Domain
+ Current Market
→ Retrieval
→ Applicability
→ Conflict/Dependency/Overlap
→ Decision Synthesis
→ Decision Thesis/Candidate
→ EV
→ Economic Opportunity Context
→ R4

FAST RUNTIME:
Position-linked Knowledge Assumptions
+ Current Runtime Context
→ Assumption Monitoring
→ R4 Protection / R5 Feedback / R2 Question

NEXT — R4:
Reconstruct:
1. Capital governance
2. Portfolio / correlation / concentration
3. Risk budget / drawdown / ruin protection
4. risk permission
5. fast safety / emergency path
6. execution fidelity
7. exchange-independent order intent
8. reconciliation
9. canonical position / exposure truth
10. runtime position protection
11. exit / reduce / block
12. R4 → R5 production evidence

Do NOT:
- adopt Phase 5 candidates as final architecture
- finalize DB/Object/Python
- let R3 issue capital permission
- let runtime finding mutate Knowledge directly
- modify formal Current Architecture
- run Phase 6 destruction review early

READ:
- 98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
- 98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md
- 00_HUMAN/PROJECT_CHARTER.md
- future Current 05/06 only if/when created; do not invent them

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