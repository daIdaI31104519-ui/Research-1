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
2026-10-07

Conversation Focus:
PROJECT_CHARTER Section 11 Research Results Usage Governance saved. Long-term formal integration strategy agreed and saved as a separate non-current design strategy. Current formal Charter focus moves to Section 12 AI / Human / Production Authority.

WORKFLOW:
AI_WORKFLOW v0.5.3 Precision-First → Precision Review → Human View remains active. Current Git workflow is valid for the present Daisuke-design detailing phase; the future Formal Integration phase shall design and approve its own comparative review / Git governance before formal synthesis begins.

LATEST SAVED WORKING CHECKPOINT:
PROJECT_CHARTER Section 11 — Research Results Usage Governance

PRE-SAVE RECOVERY POINT:
0ff7b0b58fac489df7802a770a39a02800a42a05
= Section 11 save completion point before the formal-integration strategy save

LONG-TERM STRATEGIC DIRECTION:
98_DESIGN_STUDY/正式市場理解OS_比較統合設計方針.md

Core direction:
- Legacy Market Understanding OS = implementation/history candidate, not automatically rejected.
- Daisuke Market Understanding OS = current human-origin design candidate being detailed now.
- GPT Independent Market Understanding OS = future independently generated AI-origin candidate; do not merely paraphrase Daisuke design.
- Final Market Understanding OS = compare, attack, reject/adopt, and integrate candidates with explicit decision records; do not average them mechanically.
- Before Formal Integration, redesign the formal comparison/review workflow and Git organization instead of blindly inheriting the current workflow.

PROJECT_CHARTER STATUS:
Section 1–11 = DRAFT / LEADING CANDIDATE SAVED
Section 12+ = UNDESIGNED

PROJECT SEQUENCING:
00_AI/TEMP_CHARTER_RECONCILIATION_PLAN.md v0.8 remains active.

CURRENT FORMAL PROJECT FOCUS:
12. AI / Human / Production Authority

CURRENT NAVIGATION:
AI_CONTEXT v0.1.18 synchronized to Section 12 focus and the long-term Formal Integration strategy.
TEMP_CHARTER_RECONCILIATION_PLAN v0.8 synchronized to Section 12 focus.

UNCHANGED BY THIS SAVE:
00_HUMAN/PROJECT_CHARTER.md content
00_HUMAN/HUMAN_MAP.md
00_AI/AI_WORKFLOW.md
02_ARCHITECTURE/
R3 Formal Current Architecture

NEXT:
1. Continue Daisuke-design PROJECT_CHARTER detailing from Section 12.
2. Do not treat the long-term integration strategy as Current Design or as permission to merge candidate designs now.
3. After the Daisuke design reaches an agreed closure, create a genuinely independent GPT design at comparable depth.
4. Only then enter comparative reconciliation and design the Formal Integration workflow / Git structure.

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