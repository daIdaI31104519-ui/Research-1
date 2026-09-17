# 市場理解OS — AI_CONTEXT v0.1.10

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

AI_START_HERE.md
= Cold Start / Context Recoveryの起動入口

AI_WORKFLOW.md
= GPTの作業方法 / 保存先判定 / Impact Sync / Git Safety / Recovery Rule

AI_CONTEXT.md
= 長期Project Current State / 現在地 / 案内板 / 目録

AI_HANDOFF.md
= Latest Conversation Delta / 直前Conversationの短期引き継ぎ

各Design md
= 設計本文

01_HISTORY/
= 過去の変更・失敗・判断理由
```

原則:

```text
AI_CONTEXT = Project Current State
AI_HANDOFF = Latest Conversation Delta
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
Project Charter Reconciliation
```

現在は05_DECISIONへ進む直前に、Project Mission / Research Mission / Capital-Risk Philosophy / Knowledge-Data Asset Philosophy / Extensibility等の最上位思想不足を確認したため、Partial Connection Map構築を一時停止し、`PROJECT_CHARTER` を先に整備して既存Working Baselineと再照合する段階にある。

---

# 2. Current Task

```text
CURRENT TASK:
00_HUMAN/PROJECT_CHARTER.md v0.1 Draft の作成

Section 1:
Project Mission
= DRAFT / LEADING CANDIDATE 保存済み

Section 2:
Success Definition
= DRAFT / LEADING CANDIDATE 保存済み

現在焦点:
3. What Not To Maximize
```

`01_EXTERNAL_DATA`、`02_MARKET_UNDERSTANDING`、`03_RESEARCH`、`04_KNOWLEDGE_APPLICABILITY` はWorking Baselineとして保存済み。

05_DECISIONは破棄していない。PROJECT_CHARTERをWorking Baseline化し、HUMAN_MAP / AI_WORKFLOW / 01〜04を必要最小限で再照合した後に05_DECISIONへ復帰する。

一時移行手順:

```text
00_AI/TEMP_CHARTER_RECONCILIATION_PLAN.md
```

---

# 3. Current Documents

## 3.1 AI_WORKFLOW

```text
Path: 00_AI/AI_WORKFLOW.md
Version: v0.5.2
Status: REVIEWED / WORKING BASELINE
Role: GPTが市場理解OSをどう設計・確認・保存し、保存先・同期対象・文書間整合・Checkpoint / Baseline / Recovery・Human-Readable File Namingをどう管理するかを決める作業規則
```

設計作業・Git保存・復旧判断・新規File命名について判断が必要な場合は、この文書を優先して参照する。
AI_CONTEXTへAI_WORKFLOWの詳細ルールを複製しない。

## 3.2 PROJECT CHARTER

```text
Path: 00_HUMAN/PROJECT_CHARTER.md
Version: v0.1
Status: DRAFT / LEADING CANDIDATE
Current State:
- Section 1 Project Mission = 保存済み
- Section 2 Success Definition = 保存済み
- Section 3以降 = 未設計
Current Focus: 3. What Not To Maximize
```

Project Missionの現在本命方向には、Crypto First、選択的Research、Fast Adaptation / Research Adaptation、Research Note / Research Asset、長期生存と正の期待値、人間向けResearch Publicationが含まれる。

Success Definitionの現在本命方向は、資本・Research Asset・意思決定能力を成長させながら、Knowledge / Edge / Success状態を継続的に再検証し、市場変化へ適応する循環を止めないことを中心とする。

重要:

```text
Section 1〜2 保存済み
≠
PROJECT_CHARTER Working Baseline
```

Section 3以降を設計し、PROJECT_CHARTER全体をCross Checkするまでは、Charter全体を確定扱いしない。

## 3.3 HUMAN MAP

```text
Path: 00_HUMAN/HUMAN_MAP.md
Version: Part 1 v0.3
Status: DRAFT / NOT CANONICAL
Current Use: CURRENT HUMAN REFERENCE
```

Canonicalではないが、現在の市場理解OSのHuman思想を確認するときの主要参照先とする。

## 3.4 TEMP CHARTER RECONCILIATION PLAN

```text
Path: 00_AI/TEMP_CHARTER_RECONCILIATION_PLAN.md
Version: v0.3
Status: TEMPORARY / ACTIVE UNTIL RECONCILIATION COMPLETE
Role: PROJECT_CHARTER導入中の作業順・影響範囲・Checkpoint・復帰条件を固定する一時ナビ
```

恒久設計ではない。PROJECT_CHARTER導入と01〜04再照合が完了し、Current Taskが05_DECISIONへ戻った後に削除する。

## 3.5 PARTIAL CONNECTION MAP — EXTERNAL / DATA

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

## 3.6 PARTIAL CONNECTION MAP — MARKET UNDERSTANDING

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

## 3.7 PARTIAL CONNECTION MAP — RESEARCH

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

## 3.8 PARTIAL CONNECTION MAP — KNOWLEDGE / APPLICABILITY

```text
Path: 02_ARCHITECTURE/CONNECTIONS/04_KNOWLEDGE_APPLICABILITY.md
Version: v0.1.1
Status: REVIEWED / WORKING BASELINE
Role: Validated Research Resultを条件付きKnowledgeへ整理し、Current Market Contextと照合して現在利用可能なKnowledgeだけをApplicable Knowledge Setとして05へ渡す境界
```

主要Downstream Boundary:

```text
Applicable Knowledge Set
```

重要境界:

```text
Validated Research Result
≠ Knowledge

Knowledge
≠ Applicable Knowledge

Applicable Knowledge
≠ Trade Signal

Knowledge Maintenance Path
≠ Runtime Applicability Path
```

## 3.9 MASTER CONNECTION MAP

```text
Path: 02_ARCHITECTURE/CONNECTION_MAP.md
Status: PLACEHOLDER / NOT CANONICAL
Known State: v0.1は設計・Cross Check済み。Failure Reviewあり。
Current Direction: Partial Connection Map群を先に作成し、その後Masterへ統合する。
```

現在のPlaceholderを完成設計として扱わない。

## 3.10 CROSS-CUTTING MAP

```text
Path: 02_ARCHITECTURE/CROSS_CUTTING_MAP.md
Status: PLACEHOLDER / NOT CANONICAL
```

Partial Connection Map群およびMaster Connection Mapとの接続を確認した後、本格設計する。

## 3.11 AI_START_HERE

```text
Path: 00_AI/AI_START_HERE.md
Version: v0.2
Status: REVIEWED / WORKING BASELINE
Role: Cold Start / 新Chat / Context Loss / 別AI交代時のAI用起動地図
```

Cold Start順・主要Document Role・Recovery Ruleの正本として扱う。
通常Taskごとに毎回読む必要はない。

## 3.12 AI_HANDOFF

```text
Path: 00_AI/AI_HANDOFF.md
Version: v0.2
Status: REVIEWED / WORKING BASELINE
Role: AI_CONTEXTでは保持しないLatest Conversation Deltaを短く引き継ぐConversation Snapshot
```

AI_HANDOFFはCurrent Designや長期Pendingの正本ではない。
具体的なField / State / Maintenance RuleはAI_HANDOFF自身を正本とする。

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
Knowledge ≠ Applicable Knowledge
Applicable Knowledge ≠ Trade
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
Human Understanding / Project Charter
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
- Current Taskを次Map / 次Charter項目へ更新
- 不要な作業履歴はAI_CONTEXTへ蓄積しない
- AI_CONTEXT = Project Current State / AI_HANDOFF = Latest Conversation Deltaへ責任分離
- AI_WORKFLOW v0.5でSave Destination Resolution / Logical Change Impact Syncを導入
- AI_WORKFLOW v0.5.1でNo-op Write Check / Checkpoint / Baseline / Recovery / Independent Backup原則を導入
- AI_WORKFLOW v0.5.2でHuman-Readable File Naming Policyを追加
```

```text
PENDING-002
Runtime Knowledge Switching / Unknown Market / In-Trade Thesis Re-evaluation

再開時期:
PROJECT_CHARTER Reconciliation完了後、04_KNOWLEDGE_APPLICABILITY → 05_DECISION → 06_EXECUTION_POST_DECISION の接続を設計するとき。

現在方向:
1. Positionなし:
   市場を常時観測し、Current Market Pattern / Market DNA / Contextに応じてApplicable Knowledgeを動的に切り替える。
   Applicable Knowledgeが見つかっても自動Tradeとはせず、Entry条件成立まではWAITできる。

2. 既存Pattern / Knowledgeに十分属さない市場:
   無理にTradeせず、UNKNOWN / NOT_APPLICABLEとしてWAIT / NO TRADEを許容し、必要ならResearch Candidateとして03_RESEARCHへ戻す。

3. Position保有中:
   市場Patternが変化して別KnowledgeがApplicableになっても、Entry時Trade Thesisの理由を後付けで差し替えない。
   新しい市場状態に対して、元のTrade Thesisがまだ成立するかを再評価し、HOLD / REDUCE / EXIT等へ接続する。

4. 詳細なPattern State、Switch Threshold、HOLD / REDUCE / EXIT Ruleは未設計。
```

軽微な保留、一時的な案、単なる思いつきはここへ保存しない。

---

# 8. Next Actions

```text
NEXT-001
PROJECT_CHARTER v0.1 Draftを一項目ずつ作成
Section 1 Project Mission = DRAFT / LEADING CANDIDATE 保存済み
Section 2 Success Definition = DRAFT / LEADING CANDIDATE 保存済み
現在: 3. What Not To Maximize

NEXT-002
PROJECT_CHARTER全体をCross Checkし、問題が軽微ならWorking Baseline候補として保存

NEXT-003
TEMP_CHARTER_RECONCILIATION_PLANに従い、HUMAN_MAP / AI_WORKFLOW / 01〜04を必要最小限で再照合

NEXT-004
DESIGN_CHANGE_LOGへ今回の上位設計補完理由を記録し、AI_CONTEXT Current Taskを05_DECISIONへ復帰

NEXT-005
TEMP_CHARTER_RECONCILIATION_PLANを削除後、05_DECISION設計を再開
```

```text
NEXT = 次に実行する作業
PENDING = 今は解決しないが忘れてはいけない問題
```

---

# 9. Required Read

Cold Start / 新Chat / Context Loss / 別AI交代時の読込順は、

```text
00_AI/AI_START_HERE.md
```

を正本とする。

通常の設計作業では必要な範囲だけ読む。

基本入口:

```text
1. 00_AI/AI_WORKFLOW.md
2. 00_AI/AI_CONTEXT.md
3. 必要なら 00_AI/AI_HANDOFF.md
4. 現在Taskの対象md
```

PROJECT_CHARTER Reconciliation中は追加で、

```text
00_HUMAN/PROJECT_CHARTER.md
00_AI/TEMP_CHARTER_RECONCILIATION_PLAN.md
00_HUMAN/HUMAN_MAP.md
```

を必要範囲で参照する。

Connection分割設計では、直前のPartial Connection MapとのBoundary一致を確認する。
変更理由・過去失敗が必要なら `01_HISTORY/README.md` から該当Historyへ進む。
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
Runtime Knowledge Switch Threshold
In-Trade HOLD / REDUCE / EXIT詳細Rule
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

Conversation固有の短期差分はAI_HANDOFFへ送る。
過去Versionと変更理由はHistoryへ送る。

---

# 12. Workflow Reference

次のような作業判断はAI_CONTEXT自身で詳細定義しない。

```text
いつDeep Diveを止めるか
設計成熟度をどう判断するか
Git保存時の確認
Save Destination Resolution
Logical Change Impact Sync
No-op Write Check
Checkpoint / Baseline Decision
Recovery / Restore
Document Impact Check
Design Closure Guidance
外部Webを使う条件
GPTが反対すべき条件
Scope管理
Human-Readable File Naming
```

これらは `00_AI/AI_WORKFLOW.md` を参照する。
AI_CONTEXTは必要に応じて、現在重要なWorkflow Ruleを短く示すだけにする。

---

# 13. Navigation Principle

GPTが迷った場合:

```text
AI_CONTEXT
↓
必要ならAI_HANDOFF
↓
現在Taskを確認
↓
対象Designを読む
↓
直前 / 直後Boundaryを確認
↓
不足した場合だけ関連Design
↓
理由が必要ならHistory Router
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
Git書込の最終許可
```

を伝える。

GPTはGit・AI_WORKFLOW・AI_CONTEXT・必要ならAI_HANDOFFを使って設計運用を補助する。

---

# AI_CONTEXT v0.1.10 一文定義

> **AI_CONTEXTとは、市場理解OSの設計内容そのものや直前Conversationを複製する文書ではなく、GPTが現在Phase・Current Task・主要Working Baseline・重要Pending・Next Action・参照先を短時間で把握し、Gitという長期作業空間の中から現在Taskに必要な正しい設計情報へ移動するための軽量なAI専用Project Current-State Mapである。**
