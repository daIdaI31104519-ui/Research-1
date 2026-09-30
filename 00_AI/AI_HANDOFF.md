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
Phase 5 R1 and R2 concept-level reconstruction complete.
Current active work: R3 Knowledge / Applicability / Decision Preparation.

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

R2 KEY RECONSTRUCTION:
- Research Question is the broad conceptual entry
- Research Candidate is admission target after Question, not the question itself
- Research Intake / Priority / Routing redesigned around admission and multi-axis routing
- Research is Multi-Entry / Common-Core, not only anomaly-driven
- Research Mode explicitly separates EXPLORATORY / CONFIRMATORY / REPLICATION
- Research Plan is central reproducible specification; material post-result changes require new version
- Hypothesis / Claim remains distinct from Evidence / Result / Knowledge
- Causal and Empirical research coexist as Method families
- Evidence Channel / Role / Outcome / Strength / Dependency remain separate
- Research Ledger retains full search/trial history to expose hidden search space
- Red Team / independent challenge retained as responsibility
- Stress Lab merged into Research Method / Boundary Discovery; stress capability preserved
- Failure Boundary / Constraint Candidate retained
- Research Synthesis cannot use simple evidence majority vote
- Research Process Failure remains separate from Hypothesis Refutation
- Validated Research Result means research integrity/trace requirements passed, not hypothesis proven true
- Negative / Refuted / Inconclusive / Unknown results remain valuable research assets
- Reverse Investigation generates candidates/questions before formal R2 research
- External Research is a source to replicate/validate, not internal truth
- AI suggestion/judgment is advisory, not evidence/validation/production authority
- Research cannot directly mutate Knowledge or Production

R2 CANDIDATE FLOW:
Question Sources
→ Research Question
→ Research Candidate
→ Admission / Priority
→ Research Plan
→ Mode + Methods
→ Trials
→ Evidence
→ Independent Challenge
→ Research Synthesis
→ Research Result
→ Validation Gate
→ Validated Research Result
→ R3

NEXT — R3:
Reconstruct:
1. Knowledge Admission / Formation
2. Knowledge semantics / relationships
3. Knowledge lifecycle / aging / revalidation
4. Negative knowledge / failure boundary / constraints
5. Applicability
6. Runtime assumption monitoring
7. Multi-knowledge conflict
8. Decision Synthesis
9. Expected Value
10. R3 → R4 handoff
11. distinction between Foundation and Research Knowledge

Do NOT:
- adopt Phase 5 candidates as final architecture
- finalize DB/Object/Python
- convert research result directly into Knowledge
- run Phase 6 destruction review early
- modify formal Current Architecture

READ:
- 98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
- 02_ARCHITECTURE/CONNECTIONS/04_KNOWLEDGE_APPLICABILITY.md
- 98_DESIGN_STUDY/市場理解OS_研究機関_設計検討リファレンス.md
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