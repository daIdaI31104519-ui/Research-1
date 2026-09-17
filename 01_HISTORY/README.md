# 市場理解OS — 設計史・失敗履歴の案内

**Document Role:** History Router  
**Status:** REVIEWED / WORKING BASELINE  
**Purpose:** `01_HISTORY/` の各文書が何を保存する場所なのかを、人間とAIが短時間で判断するための入口。

---

# 0. このDirectoryの役割

`01_HISTORY/` は、

> **現在使う設計本文ではなく、「なぜ現在の設計になったか」を保存する場所**

である。

ここに存在する内容は、

```text
History
Failure
Lesson
Rejected / Legacy
Change Reason
```

であり、Gitに存在するだけでCurrent Designとして扱わない。

現在の設計を確認する場合は、該当するCurrent Design文書を確認する。

---

# 1. 保存先Router

## 設計変更履歴

```text
DESIGN_CHANGE_LOG.md
```

保存するもの:

```text
何を変更したか

変更前はどうだったか

なぜ変更したか

変更後どうなったか
```

主な問い:

> **何を、なぜ変えた？**

---

## 個別Failure Review

```text
*_FAILURE_REVIEW.md
```

保存するもの:

```text
特定Version

特定Architecture

特定Workflow

特定機能
```

で発生した大きな失敗・不足・破綻理由。

主な問い:

> **具体的に何が壊れた？**

個別Failureが大きく、単独で後から参照する価値がある場合に使用する。

軽微な失敗ごとに新Fileを作らない。

---

## 設計教訓

```text
LESSONS_LEARNED.md
```

保存するもの:

> **個別の失敗や変更から一般化できた、再利用可能なDesign Knowledge**

主な問い:

> **そこから何を学び、今後どこでも再利用できる？**

単なる出来事の記録ではなく、

```text
Failure
↓
Cause
↓
Lesson
↓
再利用可能な原則
```

へ変換されたものを保存する。

---

## 却下・旧設計

```text
REJECTED_IDEAS.md
```

保存するもの:

```text
現在は採用しない案

役割を変更した旧案

SUPERSEDED Design

Legacy化したConcept
```

主な問い:

> **なぜ今はこの案を使わない？**

`REJECTED` は「価値が無かった」という意味ではない。

将来条件が変わった場合は再検討できる。

---

## AI / Git Workflowの失敗履歴

```text
AI_WORKFLOW_失敗と改善履歴.md
```

保存するもの:

```text
GPTとの設計作業方法

Git保存方法

Context Recovery

Save Destination

Impact Sync

Checkpoint / Baseline / Recovery
```

等の、**市場理解OS本文ではなく設計運用そのもの**の失敗・改善理由。

主な問い:

> **人間とGPTの作業方法を、なぜ変更した？**

現在の作業規則そのものは、

```text
00_AI/AI_WORKFLOW.md
```

を正本とする。

---

# 2. 保存判断

新しい出来事が起きても、すべてHistoryへ保存しない。

```text
軽微な修正
→ 原則History不要

Current Stateだけ変化
→ AI_CONTEXT等

次Chatだけ必要
→ AI_HANDOFF

大きな設計変更理由
→ DESIGN_CHANGE_LOG

特定設計の大きな失敗
→ FAILURE_REVIEW

再利用可能な学び
→ LESSONS_LEARNED

却下・Legacy化
→ REJECTED_IDEAS

AI / Git作業方法の失敗
→ AI_WORKFLOW_失敗と改善履歴
```

---

# 3. 重複保存しない

同じ内容を、

```text
DESIGN_CHANGE_LOG
+
LESSONS_LEARNED
+
FAILURE_REVIEW
```

へ全文コピーしない。

必要な場合は責任を分ける。

例:

```text
FAILURE_REVIEW
=
実際に何が失敗したか

DESIGN_CHANGE_LOG
=
その結果、設計を何へ変更したか

LESSONS_LEARNED
=
他の設計でも使える一般原則
```

各文書は自分の責任だけを保持する。

---

# 4. HistoryはCurrent Designではない

重要:

```text
Historyにある
≠
現在採用中

Rejectedにある
≠
永久禁止

古いDesignがある
≠
Current Designへ自動復活
```

過去設計を再利用する場合は、

```text
History確認
↓
Current Design確認
↓
現在条件で再評価
↓
Proposal
↓
必要なCross Check
↓
採用判断
```

を行う。

---

# 一文定義

> **`01_HISTORY/` とは、市場理解OSの現在設計を複製する場所ではなく、設計変更・失敗・教訓・却下理由・AI/Git運用改善の「なぜ」を保存し、同じ失敗を理由を忘れた状態で再発明しないためのDesign History Storeである。**
