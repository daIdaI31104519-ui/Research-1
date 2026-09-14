# 市場理解OS — AI_CONTEXT v0.1.3

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
Architecture / Connection分割設計
+
Partial Connection Map構築段階
```

現在はMaster Connection Mapを一気に完成させるのではなく、主要責任領域をPartial Connection Mapへ分割し、各Mapを70〜80%程度のWorking Baselineとして接続可能にしてから全体統合する段階にある。

---

# 2. Current Task

```text
CURRENT TASK:
04_KNOWLEDGE_APPLICABILITY の役割・境界設計準備
```

`01_EXTERNAL_DATA`、`02_MARKET_UNDERSTANDING`、`03_RESEARCH` はCross Check後、Working Baselineとして保存済み。

次は、`Validated Research Result` を受け取り、Knowledgeとしてどう昇格・保持・Version管理するか、さらにCurrent Market Understanding / Market DNA Snapshotと照合して現在市場で利用可能かを判断するKnowledge / Applicability境界を設計する。

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

## 3.3 PARTIAL CONNECTION MAP — EXTERNAL / DATA

```text
Path: 02_ARCHITECTURE/CONNECTIONS/01_EXTERNAL_DATA.md
Version: v0.1.1
Status: REVIEWED / WORKING BASELINE
Role: External SourcesをQualified Market Observation Setへ変換する接続境界
```

主要Downstream Boundary:

```text
Qualified Market Observation Set
```

## 3.4 PARTIAL CONNECTION MAP — MARKET UNDERSTANDING

```text
Path: 02_ARCHITECTURE/CONNECTIONS/02_MARKET_UNDERSTANDING.md
Version: v0.1.1
Status: REVIEWED / WORKING BASELINE
Role: Qualified ObservationからFeature / Context / Market Intelligence / Current Market Understandingへ接続し、Cause CandidateとMarket DNA Snapshotへ分岐する境界
```

主要Downstream Boundaries:

```text
Current Market Understanding
Cause Candidate
Market DNA Snapshot
```

## 3.5 PARTIAL CONNECTION MAP — RESEARCH

```text
Path: 02_ARCHITECTURE/CONNECTIONS/03_RESEARCH.md
Version: v0.1.1
Status: REVIEWED / WORKING BASELINE
Role: Research Candidateを共通入口から受け取り、Research Plan / Hypothesis / Validation / Refutation / Failure Boundaryを経てValidated Research Resultへ接続する研究境界
```

主要Downstream Boundary:

```text
Validated Research Result
```

重要境界:

```text
Research Candidate
≠ Research Context

Validated Research Result
≠ Supported Hypothesis
≠ Production Knowledge
≠ Current Market Applicable
```

## 3.6 MASTER CONNECTION MAP

```text
Path: 02_ARCHITECTURE/CONNECTION_MAP.md
Status: PLACEHOLDER / NOT CANONICAL
Known State: v0.1は設計・Cross Check済み。Failure Reviewあり。
Current Direction: Partial Connection Map群を先に作成し、その後Masterへ統合する。
```

現在のPlaceholderを完成設計として扱わない。

## 3.7 CROSS-CUTTING MAP

```text
Path: 02_ARCHITECTURE/CROSS_CUTTING_MAP.md
Status: PLACEHOLDER / NOT CANONICAL
```

Partial Connection Map群およびMaster Connection Mapとの接続を確認した後、本格設計する。

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
Validated Research Result ≠ Supported Hypothesis
Observation ≠ Feature ≠ Interpretation ≠ Candidate
AIは主に 解釈 / 仮説 / 反証 / 査読 / 説明 へ使用する
Gitに存在 ≠ 現在採用中
局所100%より、全体を接続可能な状態へ先に進める
```

詳細な理由や例外が必要な場合は、Human Map / Current Design / Historyを確認する。

---

# 5. Current Connection Split

現在採用するConnection Map分割:

```text
01_EXTERNAL_DATA
↓
02_MARKET_UNDERSTANDING
↓
03_RESEARCH
↓
04_KNOWLEDGE_APPLICABILITY
↓
05_DECISION
↓
06_EXECUTION_POST_DECISION
↓
MASTER CONNECTION MAP
```

Cross-Cutting責任はこの縦分割へ無理に混ぜず、別途 `CROSS_CUTTING_MAP.md` で扱う。

---

# 6. Current Roadmap

現在採用する上位ロードマップ:

```text
Human Understanding
↓
Architecture / Partial Connection
↓
Master Connection
↓
Cross-Layer Reconciliation
↓
Cross-Cutting
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

# 7. Pending / Open

AI_CONTEXTへ残すのは、次の設計へ影響する重要事項だけとする。

```text
PENDING-001
AI_CONTEXTのContext Sync運用が実際のGit作業で正しく機能するか継続確認する。

現在までの確認:
- Working Baseline追加をCurrent Documentsへ反映
- Current Taskを次Mapへ更新
- 不要な作業履歴はAI_CONTEXTへ蓄積しない
```

軽微な保留、一時的な案、単なる思いつきはここへ保存しない。

---

# 8. Next Actions

```text
NEXT-001
04_KNOWLEDGE_APPLICABILITY の役割・境界を設計

NEXT-002
04_KNOWLEDGE_APPLICABILITYをCross Checkし、問題が軽微ならWorking Baseline候補として保存

NEXT-003
05_DECISIONへ進み、Trade Thesis → Expected Value → Signal → Risk / Defenseの責任境界を設計

NEXT-004
06_EXECUTION_POST_DECISIONまでPartial Connection Mapを構築

NEXT-005
Partial Connection Map群が揃った段階でMaster Connection Mapへ統合

NEXT-006
Master統合後にCross-Layer / Cross-Cutting整合を確認
```

```text
NEXT = 次に実行する作業
PENDING = 今は解決しないが忘れてはいけない問題
```

---

# 9. Required Read

GPTが市場理解OSについて新しい設計作業を開始するとき、必要な範囲だけ読む。

基本入口:

```text
1. 00_AI/AI_WORKFLOW.md
2. 00_AI/AI_CONTEXT.md
3. 現在Taskの対象md
```

Connection分割設計では、直前のPartial Connection MapとのBoundary一致を確認する。

Human思想の確認が必要なら `00_HUMAN/HUMAN_MAP.md` を読む。
変更理由・過去失敗が必要なら `01_HISTORY/` を読む。
旧Repo・過去資料・外部情報は、現在Taskに必要な場合だけ確認する。

毎回Repo全体を読むことを要求しない。

---

# 10. Do Not Design Yet

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

# 11. Context Sync Rules

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

過去Versionと変更理由はHistoryへ送る。

---

# 12. Workflow Reference

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

# 13. Navigation Principle

GPTが迷った場合:

```text
AI_CONTEXT
↓
現在Taskを確認
↓
対象Designを読む
↓
直前 / 直後Boundaryを確認
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

# 14. Human Responsibility

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

# AI_CONTEXT v0.1.3 一文定義

> **AI_CONTEXTとは、市場理解OSの設計内容そのものを複製する文書ではなく、GPTが現在Phase・Current Task・主要Working Baseline・重要Pending・Next Action・参照先を短時間で把握し、Gitという長期作業空間の中から現在Taskに必要な正しい設計情報へ移動するための軽量なAI専用現在地マップである。**