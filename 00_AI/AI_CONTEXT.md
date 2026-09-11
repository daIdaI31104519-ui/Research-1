# 市場理解OS — AI_CONTEXT v0.1.1

**Document Role:** AI Current-State Index / Navigation Map  
**Status:** REVIEWED / WORKING BASELINE  
**Purpose:** GPTが市場理解OSの現在地・基準設計・重要保留・次作業・参照先を短時間で把握するための軽量な案内板

---

# 0. Purpose

`AI_CONTEXT.md` は市場理解OSの詳細設計書ではない。

目的は、

> **GPTが市場理解OSの現在地・現在使う資料・重要な未解決事項・次の作業を短時間で把握し、正しい設計書へ移動するための現在地マップを提供すること。**

役割分担:

```text
Research-1
= GPTの長期作業スペース / 図書館全体

AI_CONTEXT.md
= 現在地 / 案内板 / 目録

AI_WORKFLOW.md
= GPTの作業方法

各Design md
= 設計本文

01_HISTORY/
= 過去の変更・失敗・判断理由
```

原則:

```text
AI_CONTEXT = 現在
HISTORY = 過去
```

AI_CONTEXT自身が新しい設計正本になってはいけない。

---

# 1. Current Phase

```text
CURRENT PHASE:
Human-First Rebuild
+
AI設計運用基盤の整備
+
Architecture / Connection設計への移行段階
```

現在は、市場理解OS本体を詳細実装する前に、人間とGPTが設計全体で迷子にならないための設計管理基盤を整えている。

---

# 2. Current Task

```text
CURRENT TASK:
CONNECTION MAP v0.2 の設計準備
```

`AI_CONTEXT v0.1.1` の初版作成・保存は完了したため、現在Taskは次工程へ移行する。

---

# 3. Current Documents

## 3.1 AI_WORKFLOW

```text
Path: 00_AI/AI_WORKFLOW.md
Version: v0.4.1
Status: REVIEWED / WORKING BASELINE
Role: GPTが市場理解OSをどう設計・確認・保存するかを決める作業規則
```

設計作業の方法について判断が必要な場合は、この文書を優先して参照する。
AI_CONTEXTへAI_WORKFLOWの詳細ルールを複製しない。

## 3.2 HUMAN MAP

```text
Path: 00_HUMAN/HUMAN_MAP.md
Version: Part 1 v0.3
Status: DRAFT / NOT CANONICAL
Current Use: CURRENT HUMAN REFERENCE
```

Canonicalではないが、現在の市場理解OSのHuman思想を確認するときの主要参照先とする。

## 3.3 CONNECTION MAP

```text
Path: 02_ARCHITECTURE/CONNECTION_MAP.md
Status: PLACEHOLDER / NOT CANONICAL
Known State: v0.1は設計・Cross Check済み。Failure Reviewあり。
Next: v0.2を作成
```

現在のPlaceholderを完成設計として扱わない。

## 3.4 CROSS-CUTTING MAP

```text
Path: 02_ARCHITECTURE/CROSS_CUTTING_MAP.md
Status: PLACEHOLDER / NOT CANONICAL
```

Connection Map v0.2との接続を確認した後、本格設計する。

---

# 4. Current Design Guardrails

詳細な作業規則は `00_AI/AI_WORKFLOW.md` を参照する。
AI_CONTEXTでは現在地を理解するために必要な上位原則だけ保持する。

```text
Human-First
予測より理解
ResearchとProductionを分離する
Researchは大きく、Production / Live Pathは小さくする
Market DNA ≠ Signal
Expected Value ≠ Trade Permission
WIN ≠ 正しい理解
LOSS ≠ 間違った理解
Candidate ≠ Production Authority
Research Result ≠ 即Live反映
AIは主に 解釈 / 仮説 / 反証 / 査読 / 説明 へ使用する
Gitに存在 ≠ 現在採用中
局所100%より、全体を接続可能な状態へ先に進める
```

詳細な理由や例外が必要な場合は、Human Map / Current Design / Historyを確認する。

---

# 5. Current Roadmap

現在採用する上位ロードマップ:

```text
Human Understanding
↓
Architecture / Connection
↓
Cross-Layer Reconciliation
↓
Detailed Design
↓
Contract / Implementation Spec
↓
Python
↓
Tests
↓
Production
```

このAI_CONTEXTでは、Semantic Model、Relationship Model、Data Object、Calculation Rule、具体的Test順序などの詳細工程を新たに固定しない。
それらは該当する詳細設計段階で定義する。

---

# 6. Pending / Open

AI_CONTEXTへ残すのは、次の設計へ影響する重要事項だけとする。

```text
PENDING-001
AI_CONTEXTのContext Sync運用が実際のGit作業で正しく機能するか検証する。

確認ポイント:
- Current Taskが更新されるか
- Working Baseline変更を反映できるか
- 重要Pendingだけ残せるか
- 不要な履歴を蓄積しないか
```

軽微な保留、一時的な案、単なる思いつきはここへ保存しない。

---

# 7. Next Actions

```text
NEXT-001
CONNECTION MAP v0.2を設計

NEXT-002
Connection Map v0.2をCross Check

NEXT-003
問題が軽微ならGitへ保存し、AI_CONTEXT同期要否を判定

NEXT-004
Cross-Layer / Cross-Cutting設計へ進む
```

```text
NEXT = 次に実行する作業
PENDING = 今は解決しないが忘れてはいけない問題
```

---

# 8. Required Read

GPTが市場理解OSについて新しい設計作業を開始するとき、必要な範囲だけ読む。

基本入口:

```text
1. 00_AI/AI_WORKFLOW.md
2. 00_AI/AI_CONTEXT.md
3. 現在Taskの対象md
```

Human思想の確認が必要なら `00_HUMAN/HUMAN_MAP.md` を読む。
変更理由・過去失敗が必要なら `01_HISTORY/` を読む。
Connection設計では `02_ARCHITECTURE/CONNECTION_MAP.md` と関連Failure Reviewを優先する。
旧Repo・過去資料・外部情報は、現在Taskに必要な場合だけ確認する。

毎回Repo全体を読むことを要求しない。

---

# 9. Do Not Design Yet

現在は次を最終固定しない。

```text
最終DB Schema
Python Class詳細
全Field定義
最終API仕様
具体的Threshold
Production Capital Allocation
本番Credential
最終Risk数値
全例外ケース
全Test Case
```

理由は、Architecture / Connection / Cross-Layer責任がまだ十分に固定されていないため。
必要になった場合はProposalとして考えることはできるが、Current Designとして早期固定しない。

---

# 10. Context Sync Rules

AI_CONTEXTは日記ではない。

Git作業や重要設計変更後に、

> **今回の変更は「次のGPTが現在地を理解するために必要か？」**

を確認する。

YESの場合だけ更新候補とする。

主な更新対象:

```text
CURRENT PHASE変更
CURRENT TASK変更
主要Working Baseline変更
重要Pendingの追加 / 解決
主要Documentの追加 / 置換
NEXT ACTION変更
```

更新方法は原則として追記ではなく現在値の置換とする。

```text
悪い:
Connection Map v0.1
Connection Map v0.2
Connection Map v0.3

良い:
Current Connection Map: v0.3
```

過去Versionと変更理由はHistoryへ送る。

---

# 11. Workflow Reference

次のような作業判断はAI_CONTEXT自身で詳細定義しない。

```text
いつDeep Diveを止めるか
設計成熟度をどう判断するか
Git保存時の確認
Document Impact Check
Design Closure Guidance
外部Webを使う条件
GPTが反対すべき条件
Scope管理
```

これらは `00_AI/AI_WORKFLOW.md` を参照する。
AI_CONTEXTは必要に応じて、現在重要なWorkflow Ruleを短く示すだけにする。

---

# 12. Navigation Principle

GPTが迷った場合:

```text
AI_CONTEXT
↓
現在Taskを確認
↓
対象Designを読む
↓
不足した場合だけ関連Design
↓
理由が必要ならHistory
↓
必要なら旧Repo / 過去資料
↓
必要なら外部Source
```

目的は大量の情報を読むことではなく、現在Taskに必要な正しい情報へ移動すること。

---

# 13. Human Responsibility

人間が、全ファイル名、保存先、Version、Historyの場所、影響md、Current / Legacy判定を暗記することを前提としない。

人間は主に、

```text
目的
疑問
案
重視したいこと
最終的な方向性
```

を伝える。

GPTはGitとAI_CONTEXTを使って設計運用を補助する。

---

# AI_CONTEXT v0.1.1 一文定義

> **AI_CONTEXTとは、市場理解OSの設計内容そのものを複製する文書ではなく、GPTが現在Phase・Current Task・主要Documentの身分・重要Pending・Next Action・参照先を短時間で把握し、Gitという長期作業空間の中から現在Taskに必要な正しい設計情報へ移動するための軽量なAI専用現在地マップである。**
