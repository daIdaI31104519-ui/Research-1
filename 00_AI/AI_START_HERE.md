# 市場理解OS — AI START HERE v0.2

**Document Role:** AI Cold Start Entry / Project Navigation Map  
**Status:** REVIEWED / WORKING BASELINE  
**Purpose:** 市場理解OSについて前Chat・Memory・会話履歴を持たないAIが、Gitだけを使ってProjectの正体・Current Designの読み方・現在地への到達方法を短時間で理解し、安全に作業を再開するための最初の入口。

---

# 0. この文書の役割

`AI_START_HERE.md` は、

> **市場理解OSを初めて見るAI、または前ChatのContextを失ったAIが最初に読む起動地図**

である。

この文書自身は、

```text
Project Constitution
Current Design
Detailed Design
Current Task
History
Chat Log
```

の正本ではない。

この文書の役割は、

```text
市場理解OSとは何かを短時間で理解する
↓
どのRepositoryを基準にするか理解する
↓
主要Documentの責任を理解する
↓
Current Designをどう判定するか理解する
↓
何をどの順番で読むか判断する
↓
現在Taskへ到達する
↓
必要なDesign / Historyだけ追加で読む
↓
人間との設計作業を再開する
```

ことである。

重要:

```text
AI_START_HERE
≠
市場理解OSの第二設計書

AI_START_HERE
≠
AI_CONTEXTのコピー

AI_START_HERE
≠
AI_WORKFLOWのコピー

AI_START_HERE
=
正しいSourceへ移動するための起動地図
```

---

# 1. 市場理解OSを60秒で理解する

市場理解OSは、一つのTrading Strategyや一つのAI Prediction Modelを完成させ、それを永久に使い続けるためだけのSystemではない。

基本思想は、

> **予測より理解**

である。

市場を継続的に観測し、

```text
Observation
↓
Understanding
↓
Research Candidate
↓
Research
↓
Validation / Refutation
↓
Research Result
↓
Knowledge
↓
Applicability
↓
Decision
↓
Risk
↓
Execution / No Action
↓
Post-Analysis
↓
Re-Research
```

という循環を形成する。

目標は、

```text
市場を観測する
↓
現在何が起きているか理解する
↓
未知・矛盾・Failure・利益機会のうち
研究価値のあるものを選ぶ
↓
検証する
↓
再利用可能なKnowledgeへ変換する
↓
現在市場で利用可能か確認する
↓
Expected ValueとRiskを分けて判断する
↓
TRADE / WAIT / REDUCE / NO TRADE等を選択する
↓
結果を再び研究へ戻す
```

ことである。

このSectionはOrientation Summaryであり、Project Missionの正本ではない。

最上位Mission・Success・Project Philosophyは、

```text
00_HUMAN/PROJECT_CHARTER.md
```

を確認する。

市場理解OS全体を人間向けに理解する場合は、

```text
00_HUMAN/HUMAN_MAP.md
```

を確認する。

---

# 2. Repository Map

市場理解OSのCurrent Rebuildは、

```text
Research-1
```

で行う。

基本認識:

```text
Research-1
=
現在の再構築先
Current Design Workspace

旧Repo
daIdaI31104519-ui/-OS-
=
Reference / Legacy Knowledge

既存実装Repo
daIdaI31104519-ui/btc_bot_new2
=
既存Code / Implementation Fact

過去Chat / 過去txt
=
Historical / Reference Material

外部Source
=
設計判断の材料
```

重要:

```text
旧Repoに存在
≠
Research-1でCurrent Design

既存Codeに存在
≠
現在Architectureの正本

過去Chatに存在
≠
現在採用中

外部Sourceに存在
≠
Current Design
```

旧設計・既存Code・過去会話は参考にできる。

ただし、

```text
Review
↓
Comparison
↓
Adoption / Simplification / Redesign / Rejection
```

を経ずにCurrent Designへ戻さない。

---

# 3. Document Map と Authority

市場理解OSでは、同じ情報を複数ファイルへ詳細に複製しない。

主要Documentは次の責任を持つ。

```text
00_AI/AI_START_HERE.md
=
初見AIの起動地図

00_AI/AI_WORKFLOW.md
=
GPTと人間が
どう設計・確認・保存するか

00_AI/AI_CONTEXT.md
=
現在Phase
Current Task
主要Working Baseline
重要Pending
Next Action
参照先

00_AI/AI_HANDOFF.md
=
直前Chatから次Chatへの短期引き継ぎ
※存在する場合に利用

00_HUMAN/PROJECT_CHARTER.md
=
Project Mission
Success
最上位原則
優先順位

00_HUMAN/HUMAN_MAP.md
=
市場理解OS全体の
人間向け理解

02_ARCHITECTURE/
=
Current Architecture
Connection
Responsibility Boundary

01_HISTORY/
=
変更理由
失敗
却下理由
過去判断
```

設計内容のAuthorityは概念上、

```text
PROJECT_CHARTER
↓
HUMAN_MAP
↓
ARCHITECTURE / CONNECTION
↓
CROSS-CUTTING / DETAILED DESIGN
↓
CONTRACT / IMPLEMENTATION SPEC
↓
PYTHON / TEST
```

の順で上位思想から下位実装へ流れる。

重要:

```text
下位実装が存在する
≠
上位思想より優先

Pythonが動く
≠
Current Designとして正しい
```

下位設計と上位設計が矛盾する場合、まず下位側を再確認する。

---

# 4. Cold Start Protocol

前Chat・Memory・会話Contextが存在しない場合のみ、Cold Startとして次の順序を使う。

## STEP 1 — Orientation

```text
00_AI/AI_START_HERE.md
```

を読む。

目的:

```text
Project Identity
Repository Role
Document Role
Authority
Cold Start手順
```

を理解する。

---

## STEP 2 — 作業方法を理解する

```text
00_AI/AI_WORKFLOW.md
```

を読む。

ここで、

```text
GPTはどう設計するか
人間とどう会話するか
いつGitへ保存できるか
ProposalとCurrent Designをどう分けるか
Scopeをどう管理するか
```

を理解する。

---

## STEP 3 — 現在地を復元する

```text
00_AI/AI_CONTEXT.md
```

を読む。

ここで、

```text
現在Phase
Current Task
Current Documents
重要Pending
Next Action
```

を確認する。

---

## STEP 4 — 直前Chatを復元する

`00_AI/AI_HANDOFF.md` が存在する場合のみ読む。

目的:

```text
直前に何を話していたか
何が決まったか
何が未決定か
次に何をする予定だったか
```

を復元する。

重要:

```text
AI_HANDOFF
≠
Current Design正本
```

HANDOFFとCurrent Gitが矛盾する場合、HANDOFFを無条件に優先しない。

---

## STEP 5 — Current Task対象mdを読む

`AI_CONTEXT.md` が示す現在Taskの対象Designを読む。

必要に応じて、

```text
PROJECT_CHARTER
HUMAN_MAP
前後のConnection Map
Cross-Cutting
Detailed Design
```

を追加で確認する。

---

## STEP 6 — 必要な場合だけHistoryへ広げる

現在Taskの理由・矛盾・過去Failure確認が必要な場合のみ、

```text
DESIGN_CHANGE_LOG
LESSONS_LEARNED
REJECTED_IDEAS
FAILURE REVIEW
旧Repo
過去資料
```

を確認する。

原則:

> **Repo全体を読むことが目的ではない。現在Taskを正しく理解することが目的である。**

---

# 5. Cold Startと通常作業を分ける

毎回 `AI_START_HERE.md` から読み直す必要はない。

## Cold Start

以下の場合:

```text
新しいChat
前Chat Context消失
別AIへ交代
Memory不明
Project初見
現在地を完全に失った
```

は、

```text
AI_START_HERE
↓
AI_WORKFLOW
↓
AI_CONTEXT
↓
AI_HANDOFF
↓
Current Task
```

から復元する。

## 通常作業

すでにProjectとWorkflowを理解している場合は、

```text
AI_CONTEXT
↓
Current Task対象md
↓
必要なDesign / History
```

から開始してよい。

`AI_START_HERE.md` は毎Taskの必読書ではない。

---

# 6. Current DesignとSource Conflictの最低Rule

Current Design判定の詳細Ruleは、

```text
00_AI/AI_WORKFLOW.md
```

を正本とする。

START_HEREでは最低限だけ保持する。

重要:

```text
Gitに存在
≠
Current Design

新しい
≠
Current Design

Proposal
≠
Current Design

DRAFT
≠
Canonical

History
≠
Current Design

Legacy
≠
Current Design

HANDOFF
≠
Current Design

GITに保存
≠
自動Canonical化
```

Current Designを確認する場合は、

```text
Role
Status
History
Adopted / Proposed / Rejected
Superseded関係
現在Designとの整合
```

を見る。

---

## Source同士が矛盾する場合

異なるSourceに異なる内容がある場合、

> **自然な文章へ勝手に融合しない。**

基本対応:

```text
矛盾を発見
↓
Role / Status / Historyを確認
↓
Superseded関係を確認
↓
Current Taskとの関係を確認
↓
解決可能ならCurrent Designを特定
↓
解決不能なら矛盾を明示
↓
必要なら人間と会話して決める
```

勝手に中間案を作ってCurrent Designとして扱わない。

---

# 7. Cold Start時のCritical Guardrails

初見AIは最低限、次を誤解しない。

```text
Research
≠
Production

Research Result
≠
即Live利用

Expected Value
≠
Trade Permission

Gitにある
≠
Current Design

Proposal
≠
Current Design

HANDOFF
≠
Current Design
```

より詳しいCurrent Guardrailは、

```text
00_AI/AI_CONTEXT.md
00_HUMAN/HUMAN_MAP.md
Current Architecture
```

を確認する。

---

## Cold Start AIが勝手にしてはいけないこと

```text
失われたChat内容を推測して補完する

Legacy DesignをCurrentへ戻す

異なるSourceを勝手に融合する

質問を採用扱いする

ProposalをCurrent Design扱いする

AI_CONTEXTを詳細設計正本として扱う

HANDOFFを設計正本として扱う

関連しているという理由だけでTaskを拡張する

人間の目的を勝手に変更する

明示的な書込許可なしにGitへ書く
```

---

# 8. Recovery Failure / Fallback

## AI_CONTEXTが存在しない

作業を停止しない。

次の順序でBootstrapする。

```text
AI_START_HERE
↓
README
↓
PROJECT_CHARTER
↓
HUMAN_MAP
↓
Current Architecture
↓
必要なHistory
```

その後、現在状態を復元する。

不確実な部分は不確実として扱う。

---

## AI_CONTEXTが古い可能性がある

AI_CONTEXTだけでCurrent Designを確定しない。

```text
AI_CONTEXT
↓
Current Task対象md
↓
Role / Status
↓
必要ならHistory
```

を照合する。

---

## AI_HANDOFFが存在しない

正常。

HANDOFFなしでも、

```text
AI_WORKFLOW
+
AI_CONTEXT
+
Current Task対象md
```

から復元する。

---

## AI_HANDOFFが古い可能性がある

Current Gitと照合する。

矛盾時:

```text
HANDOFF
=
Conversation Reference

Current Git
=
Design確認対象
```

として扱う。

---

## Gitを確認できない

Current Designを検証済みであるかのように扱わない。

```text
何を確認できたか
何を確認できていないか
```

を区別する。

---

# 9. この文書に書かないもの

`AI_START_HERE.md` を巨大な第二設計書にしない。

原則として次は持たない。

```text
Current Task本文

現在Sectionの細かい進捗

全Pending一覧

詳細Architecture

全History

Chat全文

DB Schema

Python Class

API仕様

Threshold

Risk数値

Calculation Rule

Research詳細Protocol

全FileのStatus一覧

毎回変化するCommit SHA
```

これらは担当Documentへ置く。

重要:

```text
Current Taskが変わる
↓
通常START_HEREは変更しない

Charter Sectionが進む
↓
通常START_HEREは変更しない

Pendingが増える
↓
通常START_HEREは変更しない
```

START_HEREは、できるだけ長期間安定して利用する。

---

# 10. Update Conditions

この文書を更新するのは、主にAIのProject Navigation構造自体が変わった場合とする。

更新候補:

```text
Cold Start Protocol変更

主要Document Role変更

Source Authority変更

新しいAI Navigation Document追加

AI Navigation Document削除

Repositoryの役割変更

Current Design判定Ruleの大幅変更

Recovery手順変更
```

通常更新しないもの:

```text
Current Task変更

Charter Section進行

新しいResearch Result

Architecture細部変更

新しいPending追加

通常のGit Commit
```

---

# 11. Recovery Completion Check

Cold StartしたAIは、作業再開前に最低限次を理解できている必要がある。

```text
1.
市場理解OSとは何か

2.
Current Rebuild Repoはどれか

3.
Projectの最上位Sourceはどこか

4.
現在Phaseは何か

5.
Current Taskは何か

6.
現在対象mdは何か

7.
何がCurrent / Draft / Pendingか

8.
次のActionは何か

9.
重要な未解決事項はあるか

10.
Gitへの書込許可が現在あるか
```

特に重要:

```text
新しいChatになった
≠
Git書込許可が自動継続する
```

書込許可が不明な場合は、勝手にGitへ保存しない。

---

# 12. Cold Start最短フロー

```text
NEW AI / NEW CHAT / LOST CONTEXT
↓
AI_START_HERE
↓
AI_WORKFLOW
↓
AI_CONTEXT
↓
AI_HANDOFF
※存在する場合
↓
CURRENT TASK DESIGN
↓
必要なHuman / Architecture / History
↓
RECOVERY COMPLETION CHECK
↓
CURRENT STATE RECOVERED
↓
人間との作業再開
```

---

# AI_START_HERE v0.2 一文定義

> **AI_START_HEREとは、市場理解OSについて前Chat・Memory・会話Contextを持たないAIが、Research-1の位置づけ、主要Documentの責任、設計Authority、Current Designの読み方、Cold Start手順、Recovery Failure時のFallbackを最初に理解し、AI_WORKFLOW・AI_CONTEXT・必要に応じてAI_HANDOFF・Current Taskへ正しく移動して、安全に作業を再開するための安定したAI専用起動地図である。**
