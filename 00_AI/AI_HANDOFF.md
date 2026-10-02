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
2026-10-03

Conversation Focus:
Whole Market Understanding OS Reconstruction.
Phase 5 R1-R4 concept-level reconstruction exists.
R3 Knowledge / Decision Preparation detailed recovery now includes Economic Value / Opportunity Evaluation.

WORKFLOW:
AI_WORKFLOW v0.5.3 Precision-First → Precision Review → Human View workflow is active.

LATEST SAVED CHECKPOINT:
Checkpoint 015 — R3 Detailed Refinement / Economic Value

PRIMARY:
98_DESIGN_STUDY/市場理解OS_全体再構築_設計ログ.md

ECONOMIC VALUE WORKING CANDIDATE:
- Economic Value evaluates a specific Decision Candidate Version, not Knowledge.
- Candidate Objective and Evaluation Baseline / Reference Context are explicit.
- Candidate As-Of != Evaluation As-Of.
- Expected Effect != Expected Economic Value.
- Current Effect Projection cannot re-decide Applicability or Direction.
- Monetization Mapping converts Market Effect to Candidate-specific Gross Economic Outcome.
- Gross Economic Outcome != Net Economic Outcome.
- Probability != Uncertainty; Unknown Probability != 50%.
- Evaluation Mode distinguishes Probabilistic / Empirical / Scenario / Stress semantics.
- Strict Expected Value requires valid probability semantics.
- Economic Cost refined to Economic Friction & Signed Holding Flow.
- Fee != Spread != Slippage != Market Impact.
- Cost coverage / dependency must prevent double count and false independence.
- Expected Economic Value != Economic Risk Profile.
- Positive EV != Acceptable Capital Risk.
- Downside / Tail / Asymmetry / Stress remain visible.
- Hedge / Insurance may require reference-exposure-relative evaluation.
- Multiple Candidates are evaluated standalone first, then relatively.
- Highest EV != Automatic Winner.
- Global Best Candidate ranking is not Canonical Economic Output.
- Cross-Candidate Economic Dependency remains visible.
- Candidate Advancement is Candidate-specific: ADVANCE / WAIT / ABSTAIN.
- ADVANCE != Trade / Capital Permission.
- WAIT requires a re-evaluation trigger.
- ABSTAIN != Knowledge Refutation.
- Trade Thesis references exact EVA / Advancement record and preserves Economic Validity Conditions + Accepted Unknowns.
- R4 Economic Contract governs allowed capital expression.
- Economic Envelope is a Joint evaluated region, not independent min/max bounds.
- R4 is Economic Envelope consumer, not author.
- Capital-only change stays in R4.
- Economic parameter change routes to Economic Value.
- Candidate semantic / new composite leg routes to Candidate Formation.
- Thesis / Knowledge validity change routes to Applicability / Decision Synthesis.
- R4 → EV re-evaluation creates new immutable lineage; past EVA is not overwritten.

PRECISION REVIEW:
Economic Value ①〜⑨ survived destruction review after refinements.
Major refinements:
A. Objective-relative Evaluation Baseline / Reference Exposure
B. Joint Economic Envelope
C. Strict Expected Value vs Scenario-weighted estimate
D. Economic Friction + Signed Holding Flow
E. Current Effect Projection authority boundary
F. Composite protection / new leg → Candidate Formation
G. Economic Re-evaluation Request / immutable lineage
H. Potential vs allocative opportunity cost
I. Cross-Candidate dependency
J. Objective-specific No-Action / Evaluation Baseline

HUMAN REVIEW:
Daisuke: 「問題はなそうやな」
No major conceptual issue found.
Proceed as Working Candidate.

FORMAL BOUNDARY:
AI_CONTEXT remains authoritative for Formal Project Current State.
Formal Current Architecture is unchanged.
00_HUMAN/HUMAN_MAP.md is not updated yet.
02_ARCHITECTURE/ is not updated by this checkpoint.
Human View is saved only as Working Study review projection.

NEXT:
R3 Integration Precision Review across:
Admission → Record → Relationship → Graph → Version → Lifecycle → Applicability → Decision Synthesis → Economic Value.

Review responsibility overlaps, terminology, object boundaries, version/as-of semantics, unknown handling, authority, return routing, and Human View consistency.
Revise only gaps that survive integration review.
Then proceed toward Phase 6 Destruction Review.

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