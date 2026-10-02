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
2026-10-02

Conversation Focus:
Whole Market Understanding OS Reconstruction.
Phase 5 R1-R4 concept-level reconstruction exists.
Current detailed work remains R3 Knowledge / Decision Preparation refinement.

WORKFLOW:
AI_WORKFLOW v0.5.3 Precision-First → Precision Review → Human View workflow is active.

LATEST SAVED CHECKPOINT:
Checkpoint 014 — R3 Detailed Refinement / Decision Synthesis

PRIMARY:
98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md

DECISION SYNTHESIS WORKING CANDIDATE:
- Decision Synthesis = usable Decision Materialsから「今の市場について何が言えるか」を構成する責任
- Decision Synthesis != Applicability / EV / Capital Permission / Execution
- Formal output candidate = Decision Synthesis Result
- Decision Thesis != Decision Candidate
- Decision Thesis may be non-directional
- Opposite Direction != Contradiction
- Canonical CONTRADICTS != Winner Selection
- Majority Vote / Confidence Sum / Evidence double counting prohibited
- Independent Convergence is preserved as context, not vote
- Universal Knowledge Weight is not a Semantic Core primitive
- Material Influence is Thesis-specific / multi-dimensional
- ACTIVE INPUT and TRACE ONLY are separated
- Readable != Influence-Eligible
- Immutable Snapshot != Forever Valid Snapshot
- Input Validity != Synthesis Outcome
- THESIS_FORMED / INCONCLUSIVE is separate from SINGLE / MULTIPLE_COMPATIBLE / MULTIPLE_COMPETING
- No Decision Candidate → No Fake EV
- INCONCLUSIVE != WAIT != ABSTAIN != NO-TRADE
- Trade Thesis != Knowledge Truth / Capital Permission / Executed Trade
- R4 may alter capital expression, not semantic decision meaning
- Trade Thesis creation != Position activation
- No Fill → no Active Runtime Assumption Set
- Applicable Knowledge != Used Knowledge != Must-Monitor Assumption
- Runtime Deviation != R4 Position Action

RUNTIME HANDOFF:
Trade Thesis
→ Runtime Assumption Seed
→ R4
→ Execution
→ Actual Exposure
→ Pre-Activation Validity Recheck
→ Active Runtime Assumption Set
→ Runtime Monitoring
→ R4 Runtime Protection + R5 Feedback

PRECISION REVIEW:
Decision Synthesis ①〜⑦ survived destruction review with refinements.
Major corrections:
1. COHERENT / COMPETING / INCONCLUSIVEを単一State軸にしない
2. INCONCLUSIVE + no CandidateでFake EVを作らない
3. TRACE ONLYを実質的Influenceに使わない
4. R4がDecision semanticsを書き換えない
5. Snapshot immutabilityとcurrent-use validityを分離
6. Trade ThesisとRuntime activationを分離

HUMAN REVIEW:
Daisuke: 「問題は特に無さそう」
No major conceptual issue found.
Proceed as Working Candidate.

FORMAL BOUNDARY:
AI_CONTEXT remains authoritative for Formal Project Current State.
Formal Current Architecture is unchanged.
00_HUMAN/HUMAN_MAP.md is not updated yet.
02_ARCHITECTURE/ is not updated by this checkpoint.
Human View is saved only as Working Study review projection.

NEXT:
Economic Value / Opportunity Evaluation detailed refinement.

LATER INTEGRATION:
After R3 detailed recovery completes, run:
Admission → Record → Relationship → Graph → Version → Lifecycle → Applicability → Decision Synthesis → Economic Value
as R3 Integration Precision Review.
Then revise only gaps that survive review and proceed toward Phase 6 Destruction Review.

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