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
Phase 5 R1-R4 concept-level reconstruction complete.
Current active work: R5 Learning / Feedback.

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

R4 KEY RECONSTRUCTION:
- Economic Opportunity does not equal Capital Permission
- Capital / Portfolio context is explicit, not only single-trade risk
- Risk Budget, Position Sizing, Drawdown/Ruin, Correlation/Concentration are explicit responsibilities
- Research Constraint Candidate, Knowledge Constraint and Runtime Authorized Constraint remain separate
- RiskState retained with single-writer principle; exact authority deferred
- Defense Layer monolith is split into capital permission, constraints, RiskState, emergency safety and runtime protection
- Emergency Fast Path is risk-reducing / risk-containing only; it cannot create new Knowledge, increase exposure or loosen risk limits
- Recovery from emergency is stricter than entering emergency
- Execution Admission rechecks current executability and decision staleness
- Execution Intent is distinct from order submission/fill/position
- Reservation / idempotency retained for duplicate-order safety
- Execution Attempt/Event and Reconciliation retained
- Adapter / API response is not canonical execution truth
- Logical Position is canonical exposure representation built from reconciled facts
- Protection Requirement ownership is placed in R4 candidate to resolve legacy gap
- R3 detects semantic assumption deviation; R4 decides capital/position protection action
- Protection orders use the same intent/event/reconciliation discipline
- TradeResult is only financial-result projection; broader Production Outcome is R4 → R5 boundary
- System failure remains distinct from market/knowledge failure
- AI is not Risk / Exit / Execution authority; hard safety should not depend on AI availability

R4 FLOW:
R3 Economic Opportunity
→ Capital / Portfolio Context
→ Risk Budget / Constraints / RiskState
→ Capital Permission
→ Position Sizing
→ Execution Admission
→ Execution Intent
→ Reservation / Venue Routing
→ Execution Attempts / Events
→ Reconciliation
→ Execution Record
→ Logical Position
→ Protection Requirement / State
→ Runtime Protection / Exit
→ Production Outcome
→ R5

FAST SAFETY:
R1 Runtime Context
+ R3 Assumption Monitoring
+ R4 Exposure/Protection
+ X10 System Health
→ Emergency Fast Path
→ risk-reducing action only
→ Execution/Reconciliation
→ updated position/protection

NEXT — R5:
Reconstruct:
1. Production Outcome understanding
2. Decision Quality vs financial result
3. Thesis / Knowledge / Applicability / Risk / Execution attribution
4. finding normalization
5. reverse investigation
6. root-cause candidate vs confirmed cause
7. feedback classification / routing
8. R1/R2/R3/R4/System return paths
9. missed opportunity / no-trade / block evaluation
10. counterfactual / demo-live divergence
11. outcome time-integrity / hindsight controls
12. feedback asset → R6 / R2

Do NOT:
- adopt Phase 5 candidates as final architecture
- finalize DB/Object/Python
- let Emergency Fast Path increase risk
- let Adapter become canonical position truth
- let Loss directly rewrite Knowledge
- run Phase 6 destruction review early
- modify formal Current Architecture

READ:
- 98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
- 98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md

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