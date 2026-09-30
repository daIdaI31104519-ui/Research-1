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
Phase 5 top-level responsibility reconstruction is checkpointed.
Current active work is Phase 5 concept-level reconstruction.

Important Boundary:
AI_CONTEXT remains authoritative for formal Project Current State.
PROJECT_CHARTER formal Current focus is unchanged.
Reconstruction work does NOT replace Current Architecture yet.
Current 01-04 remain Working Baselines until explicit adoption.
Phase 5 decisions are reconstruction candidates, not adopted design.

PHASE 5 WORKING RESPONSIBILITY SKELETON:
R1 Perception / Relation / Current Understanding
R2 Research
R3 Knowledge / Applicability / Decision Preparation
R4 Capital / Production
R5 Learning / Feedback
R6 Long-Term Foundation / Operations / Human Projection
X  Cross-Cutting Capabilities

TWO-SPEED CANDIDATE:
Evidence / Learning Path:
R1 → R2 → R3 → R4 → R5

Fast Runtime / Safety Path:
R1 runtime context + X10 system health + R3 assumption monitoring
→ R4 capital / position protection

BOUNDARY:
Fast Runtime Path does not create new Knowledge.
Slow Research Path does not block emergency protection.

MAJOR FIRST-PASS RECONSTRUCTION:
- World Economic Library + Research Foundation → Relation/Foundation responsibility candidate
- Cause Candidate retained as optional research-question source, not cause proof
- Causal Engine split between candidate generation and formal research
- Market DNA exact form deferred; state-comparison capability preserved
- Research Question added as broad conceptual research entry
- Research Intake/Router redesigned around priority/admission/routing
- Stress Lab becomes research method/boundary-discovery candidate, not mandatory top-level layer
- Knowledge Library/Pool retained logically, physical structure not fixed
- Decision Synthesis / Conflict Resolution added
- Signal Engine dropped as required top-level concept
- Defense Layer split into capital/risk permission, runtime protection, emergency safety
- Execution and Position/Protection remain separate responsibilities
- Feedback Router replaces universal Trainer/relearning loop
- Reverse Investigation is candidate-generation method, not root-cause authority
- AI Team monolith removed in favor of cross-cutting cognitive assistance
- Telegram treated as human-control adapter, not authority
- Human-readable research is derived projection, not Knowledge SoT
- explicit storage/retention/migration responsibility added

NEXT:
Concept-level Reconstruction Matrix beginning with R1:
1. Observation / Event / Feature / Context
2. Relation / Foundation
3. Current Market Understanding
4. Cause Candidate / Contradiction / Unexplained
5. Current market state representation / Market DNA candidate
6. exact R1 → R2 / R3 / R4 outputs

Do NOT:
- adopt Phase 5 skeleton as final architecture
- choose DB/Object/Python
- finalize Market DNA name
- run Phase 6 destruction review early
- modify formal Current Architecture without explicit adoption

READ:
- 98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md
- 98_DESIGN_STUDY/DAISUKE_MARKET_UNDERSTANDING_OS_PROPOSAL.md
- 98_DESIGN_STUDY/市場理解OS_研究機関_設計検討リファレンス.md
- 99_REFERENCE/旧市場理解OS_設計知識リファレンス.md
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