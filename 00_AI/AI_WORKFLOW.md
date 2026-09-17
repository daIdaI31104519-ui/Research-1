# 市場理解OS — AI_WORKFLOW v0.5.1

**Document Role:** AI Design Workflow  
**Status:** REVIEWED / WORKING BASELINE  
**Purpose:** 人間の負担を増やさず、GPTが市場理解OSの設計管理・保存先判断・Git同期・引き継ぎ管理を担当するための共通作業規則

---

# 0. この文書の目的

`AI_WORKFLOW.md` は、

> **市場理解OSそのものの設計書ではなく、GPTが市場理解OSをどう設計・管理するかを決める作業規則**

である。

人間が、

- 複雑なStatus
- Git運用用語
- 設計管理用語
- AI用コマンド
- 保存先File
- Directory構造
- Sync対象

を大量に覚える必要はない。

基本的には普通の日本語で会話する。

GPT側が、

```text
現在地を確認
↓
必要な資料を読む
↓
考える
↓
設計する
↓
問題を疑う
↓
既存設計と照合する
↓
不要なら反対する
↓
必要なら保留を提案する
↓
Cross Checkする
↓
Logical Changeを整理する
↓
保存先候補を判断する
↓
同期対象を判断する
↓
必要なら変更前Checkpointを確保する
↓
許可された場合だけGitへ保存
↓
保存後の文書間整合を確認する
↓
必要ならBaselineを作る
```

までを担当する。

---

# 1. 人間が基本的に使う言葉

人間側が特別に覚える基本指示は、原則2つでよい。

## 1.1 「この案を考えて」

意味:

> **現在の市場理解OSを確認した上で、その案を深掘り・設計・評価する。**

GPTは原則、

```text
Research-1確認
↓
現在設計確認
↓
必要なHistory確認
↓
必要なら旧Repo確認
↓
必要なら外部情報確認
↓
案を深掘り
↓
必要性を評価
↓
既存設計との重複・矛盾確認
↓
設計案を提示
```

する。

この段階ではGitを書き換えない。

## 1.2 「GITに保存して」

意味:

> **現在話しているLogical Changeを、そのままコピーするのではなく、Gitの現在状態・正しい保存先・同期が必要なDocument・復旧安全性を確認し、最終Cross Check後に必要範囲だけ保存する。**

GPTは原則、

```text
Current Git再確認
↓
現在のLogical Change確認
↓
対象Design確認
↓
必要なHistory確認
↓
必要なら外部情報確認
↓
最終Cross Check
↓
必要なら設計修正
↓
Save Destination Resolution
↓
Logical Change Impact Sync
↓
No-op Write Check
↓
Checkpoint Decision
↓
変更対象File Set確定
↓
適切なStatusでGit保存
↓
全変更File再読込
↓
Cross-Document Consistency Check
↓
Baseline Decision
↓
Commit / Recovery Object確認
↓
変更Path / Commit / Checkpoint等を報告
```

する。

重要:

```text
GITに保存
≠
自動Canonical化
```

保存時は、設計成熟度に応じて適切な状態で保存する。

例:

```text
まだ設計途中
→ DRAFT

Cross Check済みだが改善余地あり
→ REVIEWED / WORKING BASELINE相当

正式確定可能な成熟度
→ Canonical候補
```

人間が毎回、

```text
保存先
Status
同期対象
History対象
Checkpoint / Baseline要否
```

を指定する必要はない。

GPTが現在のGit・Document Role・設計成熟度・Logical Change・Recovery Costを確認して判断する。

---

# 2. その他は普通の日本語でよい

人間はStatus用語を覚える必要はない。

例えば、

```text
これ必要？

これは保留で

これはいらない

もっと深掘りして

前の案と比べて

一回確認して

これ複雑すぎない？

今作る必要ある？

これ保存して

この案どこに入る？
```

など普通に話せばよい。

GPTが内容を解釈し、適切な設計状態・保存候補へ変換する。

---

# 3. GPTはYESマンにならない

ユーザーが提案した案でも、設計上問題がある場合はGPTが明確に反対する。

以下の場合は特に疑う。

```text
既存責任と重複する

Layerを増やすだけになる

設計が複雑になる割に価値が小さい

Human理解を悪化させる

過去に失敗した設計へ戻る

現在の設計思想と矛盾する

責任境界が混ざる

Candidateと確定判断が混ざる

同じData / Evidenceを重複評価する

Failure Pathが存在しない

将来Integrationが困難になる

今の段階で決めるには早すぎる

安全性・再現性・追跡性が悪化する

より簡単な代替方法がある

新しいFileを増やす必要がない
```

その場合、

> **推奨しない**

とはっきり伝える。

ただし否定だけで終わらず、

```text
何が問題か
+
なぜ問題か
+
代わりにどうするか
```

を説明する。

---

# 4. GPTが判断するもの

ユーザー自身が毎回すべて判断する必要はない。

GPTは設計者・設計管理者として、

```text
今必要か

後でよいか

不要か

既存設計へ統合できるか

独立設計が必要か

保留すべきか

旧案を再利用できるか

追加調査が必要か

外部情報を確認すべきか

どのDocumentが責任Ownerか

既存Fileへ保存できるか

新規Fileが本当に必要か

どのStatusが適切か

AI_CONTEXT同期が必要か

AI_HANDOFF同期が必要か

HISTORYへ残す必要があるか

AI_START_HERE / READMEへ影響するか

Checkpointが必要か

保存後Baseline化すべきか

Recovery可能性が維持されているか
```

を評価する。

重要な設計判断は、人間と会話して決める。

一方、

```text
File分類
Directory選択
Status管理
Cross-Document同期
Checkpoint / Baseline判定
```

のような設計管理は、原則GPT側が担当する。

---

# 5. Gitは市場理解OSの現在状態を確認する基準

市場理解OSについて設計・深掘り・変更を行う場合、

> **会話Memoryだけで現在設計を判断しない。**

原則として `Research-1` を確認する。

基本優先順位:

```text
Research-1 Current Design
↓
今回対象のDesign
↓
Design History / Failure Review
↓
旧Repo
↓
過去txt / 過去GPT
↓
外部Source
```

旧Repoや過去会話は参考資料であり、自動的に現在設計へ戻さない。

---

# 6. Current Designの判定方法

Git上で新しいファイルや文章を見つけても、それだけでCurrent Designと判断しない。

確認するもの:

```text
File Role

Status

Design History

Adopted / Proposed / Rejected等の状態

Superseded関係

現在使われている設計との整合
```

特に、

```text
DRAFT

REFERENCE

HISTORY

FAILURE REVIEW

REJECTED

LEGACY
```

は、Gitに存在するだけではCurrent Designではない。

重要:

```text
新しい
≠
現在採用中
```

更新日時だけでCurrent Designを決めない。

---

# 7. 必要なファイルだけ読む

毎回Repo全体を読む必要はない。

通常は、

```text
AI_CONTEXT
↓
今回対象の設計書
↓
必要なHuman / Connection / Cross-Cutting
```

を見る。

Conversationの最新差分が必要な場合は、

```text
AI_HANDOFF
```

を追加確認する。

不足・矛盾・理由確認が必要な場合だけ、

```text
DESIGN_CHANGE_LOG
LESSONS_LEARNED
REJECTED_IDEAS
FAILURE REVIEW
旧Repo
過去資料
```

へ広げる。

目的は、

> **情報を大量に読むことではなく、現在Taskを正しく進めること。**

---

# 8. Cold Start / Recovery

Cold Start・新Chat・Context Loss・別AIへの引き継ぎ手順を `AI_WORKFLOW.md` 内で重複管理しない。

Cold Start / Recoveryの入口は、

```text
00_AI/AI_START_HERE.md
```

を正本とする。

原則:

```text
Cold Start
Context Loss
Project初見
別AIへの交代
↓
AI_START_HERE
```

通常作業で現在地が把握できている場合は、

```text
AI_CONTEXT
↓
必要ならAI_HANDOFF
↓
Current Task対象md
```

を中心に読む。

`AI_CONTEXT.md` が存在しない場合のFallbackも、`AI_START_HERE.md` のRecovery Ruleを参照する。

重要:

```text
Cold Start Rule
=
AI_START_HEREの責任

AI_WORKFLOW
=
作業方法の責任
```

同じRecovery手順を複数Documentへ詳細複製しない。

---

# 9. 外部ネットを使う条件

外部ネットを毎回無条件に検索しない。

## Git中心で判断する場合

```text
内部Architecture

責任分離

既存設計との整合

History確認

設計順序

Scope判断
```

など、Repo内部で十分判断できる場合。

## Web確認を行う場合

```text
API仕様が変化し得る

Library仕様を確認する

Exchange仕様を確認する

現在の技術的実現性を確認する

既存研究と比較する

外部Architecture事例を見る

法規・標準・サービス仕様を確認する

外部Evidenceが設計判断を変える可能性がある

ユーザーが調査を求めた
```

場合。

外部情報は、

> **設計判断の材料**

であり、Current Designそのものではない。

```text
外部情報
↓
検討
↓
Proposal
```

として扱う。

---

# 10. 一つのTaskを広げすぎない

GPTは関連することを全部その場で設計しない。

作業中に別の重要問題を発見した場合、

```text
今回必要
→ 今考える

重要だが後でよい
→ 保留候補として残す

今回と関係が薄い
→ 今は触れない
```

とする。

原則:

> **関連している ≠ 今設計する。**

これはGit保存時にも同じ。

```text
関連するFile
≠
今回変更するFile
```

とする。

---

# 11. 保留はGPTからも提案する

人間が「保留」と言わなくてもよい。

GPTが、

> これは重要だが今決めると別設計まで広がるため、今は保留した方がよい。

と提案してよい。

---

# 12. 保留事項とConversation Deltaを忘れない

すべての保留事項をGitへ残す必要はない。

重要度・役割に応じて分ける。

```text
軽い保留
→ 会話内だけ

次Chatへ引き継ぐ最新Conversation差分
→ AI_HANDOFF

今後のProject設計へ影響する重要保留
→ AI_CONTEXT

大きな設計変更・失敗・却下理由
→ HISTORY
```

`AI_HANDOFF` は、

```text
Latest Conversation Snapshot
```

として扱う。

長期Pendingの正本にはしない。

`AI_CONTEXT` には重要なものだけ、

```text
PENDING / OPEN
```

として短く残す。

AI_CONTEXTやAI_HANDOFFを保留事項だけで巨大化させない。

---

# 13. 設計時の基本確認

一つの設計を考える時、最低限次を確認する。

```text
その設計自身は正しいか

何を受け取るか

何を出すか

どこと繋がるか

既存責任と重複しないか

横断機能へ影響するか

失敗した時どうなるか

動かなかった時どうなるか

後から検証できるか

人間が理解できるか
```

これをCross Checkの基本とする。

---

# 14. Happy Pathだけで判断しない

正常時だけ設計してはいけない。

必要に応じて、

```text
成功

失敗

停止

拒否

保留

NO TRADE

WAIT

BLOCK

Timeout

Unavailable

異常Data

AI停止

外部Service停止

Recovery
```

を見る。

> **何もしなかったこと・止めたこともシステムの結果である。**

---

# 15. 過去の失敗を再利用する

新しい案が出た時、必要なら過去の、

```text
DESIGN_CHANGE_LOG

LESSONS_LEARNED

REJECTED_IDEAS

FAILURE REVIEW
```

を確認する。

目的は、

> **昔の案を否定し続けるためではなく、同じ失敗を理由を忘れた状態で再発明しないため。**

過去案が現在は有効になった可能性がある場合は再検討できる。

---

# 16. Current Designと新Proposalを混ぜない

GPTが新しい案を思いついても、

```text
Proposal
≠ Current Design
```

である。

新しい案はまず提案として扱う。

ユーザーとの会話・Cross Checkを経て、現在設計として扱うか判断する。

---

# 17. Gitに存在することと採用は別

Gitには、

```text
Current Design

Draft

History

Failure

Rejected Idea

Reference

Legacy
```

が共存できる。

したがって、

```text
Gitにある
≠
現在採用中
```

とする。

GPTはファイルの役割・Status・Historyを確認して判断する。

---

# 18. Git Write Authorization / Logical Change Boundary

「GITに保存して」は、

> **現在会話しているLogical ChangeへのGit書込許可**

とする。

これは、

```text
指定された1Fileだけを書け
```

という意味ではない。

同時に、

```text
関連するRepo全体を自由に変更してよい
```

という意味でもない。

書込可能範囲は、

> **現在合意済みのLogical Changeを、矛盾なく・安全に保存し、必要なら復旧可能な状態へするために直接必要な変更範囲**

とする。

対象には必要に応じて、

```text
Primary Design

直接必要なCurrent-State Sync

AI_HANDOFF

History

Navigation修正
```

を含めることができる。

重要:

```text
直接必要
≠
関連しているもの全部
```

## 18.1 Git Recovery Objectも書込許可範囲へ含められる

現在のLogical Changeを安全に保存・復旧可能にするため直接必要と判断された場合、

```text
Checkpoint Tag

Baseline Tag

Recovery Branch

Recovery用Ref
```

等のGit Recovery Objectも、現在のGit Write Authorization範囲へ含めることができる。

ただし、

```text
現在のLogical Changeと無関係なTag

不要なBranch

意味のないRecovery Ref
```

を勝手に作成しない。

原則:

```text
Git Write Authorization
=
Logical Change本体
+
その変更を安全に保存・復旧するため直接必要なGit Object
```

とする。

## 18.2 Git Write PermissionはChatを跨がない

Previous ChatでのGit書込許可は、新しいChatへ自動継承しない。

```text
Previous Chat Git Write Authorization
≠
Current Chat Git Write Authorization
```

新しいChatでは現在の人間の指示を基準とする。

---

# 19. Save Destination Resolution

Logical Changeがまとまった場合、GPTはGit保存前に、

> **この情報のPrimary Owner Documentはどこか**

を判断する。

人間が毎回、

```text
保存File
Directory
既存File / 新規File
Status
```

を判断する必要はない。

基本手順:

```text
Logical Change確認
↓
情報の責任を確認
↓
既存Owner Documentを探す
↓
既存Documentへ自然に統合できるか？
↓
YES
→ Existing DocumentをPrimary候補

NO
↓
本当に独立した責任か？
↓
YES
→ New Document Candidate

NO
→ 新しいFileを作らない
```

原則:

```text
新しいアイデア
≠
新しいFile
```

既存の適切なOwner Documentへの統合を優先する。

ただし、異なる責任を無理に一つのFileへ混ぜない。

## 19.1 AuthorityとSave Destinationを分ける

重要:

```text
Authority
=
矛盾時にどの上位原則を優先するか

Save Destination
=
その情報を所有する責任Documentはどこか
```

したがって、

```text
PROJECT_CHARTERが最上位Authority
≠
すべてPROJECT_CHARTERへ保存
```

である。

保存先はResponsibility Ownerで判断する。

## 19.2 Destination Classification

保存候補は内部的に次の役割へ分類する。

```text
PRIMARY
=
Logical Changeそのものの正本

SYNC
=
Primary変更によりCurrent Stateを同期するFile

HISTORY
=
変更理由・失敗・却下理由を長期保存するFile

HANDOFF
=
次Chatへ残す最新Conversation Delta

REFERENCE
=
参考情報

NO WRITE
=
今回変更しない
```

Primaryは原則として責任Ownerを明確にする。

同じ設計本文を複数Documentへコピーしない。

## 19.3 人間が保存先を指定した場合

人間が具体的なFileやPathを指定した場合でも、GPTはDocument Responsibilityを確認する。

```text
指定Path
↓
Responsibility確認
↓
問題なし
→ 採用

責任重複 / 不適切
→ 問題を説明
→ より適切な候補を提示
```

人間の指定を勝手に無視しない。

ただし、不適切な保存先へ機械的に書き込まない。

---

# 20. Logical Change Impact Sync

Primary Destinationを決めた後、

> **今回のLogical Changeによって、他のCurrent-State / Handoff / History / Navigation文書も更新しなければ状態ズレが発生しないか**

を確認する。

これを、

```text
Logical Change Impact Sync
```

とする。

代表的な確認対象:

```text
Target Design
AI_CONTEXT
AI_HANDOFF
HISTORY
AI_START_HERE
README
```

すべてを毎回更新するわけではない。

各Documentについて、

> **今回のLogical Changeにより、そのDocumentが担当する情報は変化したか？**

を判定する。

## 20.1 AI_CONTEXT Impact

更新候補:

```text
Current Phase変更

Current Task変更

Current Focus変更

主要Working Baseline変更

重要Pending追加 / 解決

Project Next Action変更

主要Current Document追加 / 置換
```

重要:

```text
Design本文変更
≠
必ずAI_CONTEXT変更
```

Project Current Stateへ影響しない変更なら更新しない。

## 20.2 AI_HANDOFF Impact

ここでは、

> **AI_HANDOFFを更新すべきかどうか**

だけを判断する。

更新候補:

```text
次Chatへ残すConversation Deltaがある

会話で合意したがGit未保存の内容がある

Conversation Focusが大きく変わった

次に再開すべき作業が変わった

Chat切替 / Context Limit / AI交代へ備える必要がある
```

具体的な、

```text
Field構造
State表現
更新方法
Snapshotの書式
```

は、

```text
00_AI/AI_HANDOFF.md
```

を正本とする。

AI_WORKFLOWへAI_HANDOFF内部Schemaを複製しない。

重要:

```text
AI_WORKFLOW
=
AI_HANDOFFをいつ使うか

AI_HANDOFF
=
何をどう保持するか
```

## 20.3 HISTORY Impact

更新候補:

```text
大きな設計変更理由

重要な失敗

却下理由

旧設計を置換した理由

将来同じ失敗を再発明する危険が高い判断
```

軽微な変更をすべてHistory化しない。

## 20.4 AI_START_HERE Impact

更新候補:

```text
Cold Start順序変更

主要Document Role変更

Navigation Document追加 / 削除

Repository Role変更

Source Authority構造変更
```

通常のCurrent Task変更・Design本文変更だけでは更新しない。

## 20.5 README Impact

更新候補:

```text
Repo入口から見える構造変更

初見Human / AIが知るべき入口変更

Repository Purpose変更

主要Navigation変更
```

内部設計だけなら通常更新しない。

## 20.6 Impact判定

各候補Documentは内部的に、

```text
REQUIRED

OPTIONAL

NO IMPACT
```

として評価できる。

意味:

```text
REQUIRED
=
更新しないとCurrent StateやNavigationへ矛盾が出る

OPTIONAL
=
更新価値はあるが今回必須ではない

NO IMPACT
=
今回触らない
```

原則として保存対象は、

```text
REQUIRED
+
今回のLogical Changeに直接含まれるOPTIONAL
```

とする。

## 20.7 Scope Guard

Logical Change Impact SyncはRepo全体同期ではない。

重要:

```text
関連している
≠
変更対象

参照されている
≠
更新対象

同じProject
≠
同じLogical Change
```

Impact Checkを理由にScopeを無制限に広げない。

---

# 21. Git保存前の最終確認

Gitへ保存する直前に、

```text
現在Gitを再確認

Primary Destinationを再確認

同期対象Fileの現在内容を確認

同時変更がないか確認

Current Design判定を再確認

既存設計との矛盾確認

過去Failureとの衝突確認

不要な新規Fileを作っていないか確認

同じ情報を複数Documentへ重複保存していないか確認

不要な複雑化がないか確認

Scope外変更が混ざっていないか確認

Public Repoへ出してよい内容か確認
```

を行う。

必要なら保存前に、

```text
設計
保存先
同期対象
Status
Logical Change Boundary
```

を修正する。

この確認後、

```text
No-op Write Check
↓
Checkpoint Decision
↓
Public Repo Safety
↓
Git Write
```

へ進む。

---

# 22. No-op Write Check

Gitへ書き込む前に、

> **保存予定内容とCurrent Gitに、本当に差分が存在するか**

を確認する。

目的:

```text
同一内容の再保存

意味のないCommit

不要なBlob更新

同じSyncの繰り返し

Git Historyのノイズ
```

を防ぐ。

基本手順:

```text
Planned File Set
↓
各FileのCurrent Content取得
↓
保存予定Contentと比較
↓
差分判定
```

各Fileを、

```text
CHANGED
UNCHANGED
NEW
DELETE
MOVE / RENAME
```

として確認する。

## 22.1 UNCHANGED File

保存予定内容とCurrent Gitが同一なら、

```text
UNCHANGED
↓
Git Write対象から除外
```

する。

重要:

```text
Impact Sync対象
≠
必ずWrite
```

Impact Checkとして確認したFileでも、すでに正しい状態なら書き直さない。

## 22.2 全FileがUNCHANGEDの場合

Logical Changeに実差分が存在しない場合、

```text
Git Writeしない

Commitを作らない

Checkpointも作らない

Baselineも作らない
```

とする。

人間へ、

```text
Current Gitと保存候補が既に一致しているため
新しいCommitは不要
```

と伝える。

## 22.3 No-op原則

```text
保存指示
≠
Commit作成義務
```

Git Writeの目的は、

> **Logical Changeを正しく保存すること**

であり、

> **Commit数を増やすこと**

ではない。

---

# 23. Backup / Checkpoint Decision

実差分が存在する場合、

> **今回の変更前に、明示的Recovery Pointが必要か**

を判断する。

以下を混同しない。

```text
Commit
=
通常の変更履歴

Checkpoint
=
高Risk変更の直前に残す明示的Recovery Point

Baseline
=
変更後に確認済みの重要な完成地点
```

## 23.1 Checkpointを毎Commit作らない

原則:

```text
通常Git Commit
→ 必要な変更ごと

Checkpoint
→ 高Risk / 高Recovery Cost時のみ
```

以下では通常Checkpointを作らない。

```text
誤字修正

軽微な説明追加

小さなPending更新

表現修正

既存責任を変えない小変更
```

Checkpointそのものがノイズになることを防ぐ。

## 23.2 Checkpoint候補

以下の場合はCheckpointを検討する。

```text
複数の重要Fileを同時変更

File / Directory Rename

重要File削除

大量の構造変更

Architecture大変更

Authority変更

Document Role / Responsibility変更

複数Documentの一括Reconciliation

Working Baseline大幅置換

Project Phase切替

Python実装開始前

大規模Refactor前

DB / Contract重要変更前

復旧Costが高い変更

過去状態との比較価値が高い変更
```

## 23.3 Checkpoint Classification

内部的に、

```text
REQUIRED

OPTIONAL

NOT NEEDED
```

として判断する。

### REQUIRED

```text
失敗時の復旧Costが高い

変更前地点を明示的に残す価値が高い
```

### OPTIONAL

```text
通常Git Historyでも復旧できるが

重要地点として名前を付ける価値がある
```

### NOT NEEDED

```text
通常Commit履歴で十分
```

## 23.4 Checkpoint最低情報

Checkpointは最低限、

```text
Checkpoint Label

対象Commit SHA

作成理由

何の変更前か
```

を後から特定可能にする。

推奨例:

```text
checkpoint/2026-09-17_AI復旧基盤変更前

checkpoint/2026-XX-XX_MasterConnection再構築前

checkpoint/2026-XX-XX_Python実装開始前
```

Prefixは機械的に扱いやすくし、

```text
checkpoint/
baseline/
recovery/
```

などを使用してよい。

人間が読む名称部分は、原則として日本語で意味を理解できるようにする。

## 23.5 Checkpoint実装

Checkpointの目的は、

> **安全なCommit SHAへ意味のある名前を付け、後から確実に特定できること**

である。

利用可能なGit機能に応じて、

```text
Git Tag

Checkpoint Branch

明示的Commit SHA記録
```

を使える。

原則として、単純なRecovery PointにはGit Tagを優先する。

## 23.6 REQUIRED Checkpointを作れない場合

```text
Checkpoint = REQUIRED
```

と判断したにもかかわらず安全なRecovery Pointを確立できない場合、

> **そのまま高Risk Git Writeへ進まない。**

まずRecovery Pointを確保する。

```text
Backup必要
+
Backup不成立
↓
高Risk変更を強行
```

とはしない。

---

# 24. Public Repo Safety

Public Repositoryへ、

```text
API Key

Password

Token

Credential

秘密Config

個人情報

Private Endpoint

本番Access情報
```

を書かない。

Checkpoint / Baseline / Recovery Objectの名称・説明にも秘密情報を含めない。

---

# 25. Git Write

以下を完了した後にGit Writeする。

```text
Save Destination Resolution

Logical Change Impact Sync

Git保存前Cross Check

No-op Write Check

Checkpoint Decision

Public Repo Safety
```

書込対象:

```text
Primary Destination
+
Impact Syncで必要
+
No-op Checkで実差分あり
```

のFileだけ。

保存時:

```text
Current Git再取得
↓
必要ならSHA再確認
↓
REQUIREDなら変更前Checkpoint存在確認
↓
対象File更新
↓
Logical Change範囲外へ広げない
```

とする。

重要:

```text
保存
≠
Canonical化

保存
≠
Repo全体同期

保存
≠
Checkpoint

保存
≠
Baseline
```

---

# 26. Post-Save Cross-Document Consistency Check

Git書込後は、

```text
全変更File再取得
↓
個別内容確認
↓
Cross-Document Consistency Check
↓
Commit確認
↓
Checkpointとの関係確認
```

を行う。

確認例:

```text
Design保存済みなのに
AI_CONTEXTが旧Current Focusか

AI_HANDOFFが
保存済み内容をUNSAVEDのまま持つか

AI_CONTEXTとAI_HANDOFFが
責任を二重保持していないか

HISTORYがCurrent Design扱いに見えないか

AI_START_HEREが
存在しないDocumentを案内していないか

Design / Context / Handoffへ
同じ本文を重複保存していないか

Scope外Fileを変更していないか

Checkpointが変更後Commitを誤って指していないか
```

問題があれば、現在Logical Change範囲内で修正する。

人間へ、

```text
変更したFile

Primary Destination

同期したFile

何を変更したか

Commit SHA

Checkpoint / Baseline等のRecovery Object

残した重要なOPEN / Pending
```

を簡潔に伝える。

---

# 27. Baseline Decision

Post-Save Consistency Check完了後、

> **今回の地点を、将来戻る価値のある確認済み完成地点としてBaseline化すべきか**

を判断する。

```text
Checkpoint
=
変更前の安全地点

Baseline
=
変更後の確認済み重要地点
```

## 27.1 Baseline候補

以下を候補とする。

```text
PROJECT_CHARTER Working Baseline完成

主要Architecture完成

Master Connection Map完成

大規模Reconciliation完了

重要Project Phase完了

Implementation開始直前

Test開始直前

Production移行直前

Project運用基盤完成
```

小変更では作らない。

## 27.2 Baseline命名

例:

```text
baseline/2026-09-17_AI復旧基盤完成

baseline/2026-XX-XX_ProjectCharter完成

baseline/2026-XX-XX_Architecture_v1

baseline/2026-XX-XX_Python実装開始前
```

人間が見て意味の分かる名称を優先する。

## 27.3 Baseline作成条件

Baseline化前に、

```text
Cross Check完了

主要File保存済み

AI_CONTEXT必要同期済み

HISTORY必要同期済み

重大UNSAVEDなし

重大Failure未解決なし
```

を確認する。

重要:

```text
Commit成功
≠
Baseline
```

---

# 28. Recovery / Restore Rule

事故・誤変更・誤削除・大量破損等が発生しても、

> **mainを即座に過去Commitへ強制Rollbackすることを標準手順にしない。**

基本Recovery Flow:

```text
Failure確認
↓
Current HEAD SHAを記録
↓
可能ならRecovery Branch / Refで事故時点を隔離保存
↓
最後の安全Checkpoint / Baseline特定
↓
Current状態と安全地点を比較
↓
失われる変更を確認
↓
必要なFile / CommitだけRestore
↓
Cross Check
↓
必要ならmainへ反映
```

原則:

```text
Rollback
```

より、

```text
Recover
↓
Compare
↓
Restore
```

を優先する。

## 28.1 Current HEADとCheckpointを混同しない

事故発生時のCurrent HEADは、

```text
Known Good State
```

とは限らない。

しかし、事故後にしか存在しない正常な変更を含んでいる可能性がある。

そのため、

```text
Current HEAD
=
調査・比較のため保存する事故時点Snapshot

Checkpoint / Baseline
=
過去に確認されたRecovery候補
```

として区別する。

## 28.2 Current HEADを先に破壊しない

避ける:

```text
Failure発見
↓
即Hard Reset
```

推奨:

```text
Failure発見
↓
Current HEAD SHA記録
↓
必要ならrecovery/事故調査用Branch等へ隔離
↓
安全地点確認
↓
比較
```

事故状態もEvidenceとして扱う。

## 28.3 Recovery Source — Git Historyが正常な場合

RepositoryとGit Historyが正常かつ信頼できる場合、

```text
Validated Baseline
↓
Relevant Checkpoint
↓
Known Good Commit
↓
Git History
```

からRecovery Candidateを探す。

ただし、

```text
古いBaseline
=
現在より正しい
```

とは限らない。

必ずCurrent HEADとの差分を見る。

## 28.4 Recovery Source — Git History自体が信頼できない場合

以下の場合、

```text
Repository消失

Git History破損

Remote側事故

誤ったHistory Rewrite

Account / Repository障害

Current Remoteを信頼できない
```

は、内部Git Historyだけへ依存しない。

Recovery Flow:

```text
Independent Backup取得
↓
BackupのIntegrity確認
↓
復元可能なHistory / Filesを確認
↓
Current Remote / Local Stateと比較
↓
安全な復旧地点特定
↓
Restore
```

重要:

```text
Git Historyが壊れている
↓
壊れたGit Historyを唯一のRecovery Sourceにする
```

ことを避ける。

## 28.5 Partial Restore

問題が一部Fileだけなら、

```text
Repo全体Rollback
```

ではなく、

```text
対象FileだけRestore
```

を優先できる。

目的:

> **正常な新しい変更まで一緒に失わないこと。**

## 28.6 Recovery後

復旧完了後、

```text
何が壊れたか

原因

Current HEAD SHA

使用したCheckpoint / Baseline / Backup

RestoreしたFile / Commit

失われた変更の有無

Recovery後Cross Check結果
```

を確認する。

重大事故なら、

```text
01_HISTORY/
```

へFailure原因・改善理由を残す候補とする。

---

# 29. Independent Backup Principle

Checkpoint / Baselineは、

> **同じGit Repository内部のRecovery Point**

である。

そのため、

```text
Repository消失

Account事故

Remote障害

History破壊
```

への完全なBackupにはならない。

長期的には、

```text
GitHub Current Repository
+
Local Clone
+
必要ならPrivate Mirror / Secondary Backup
```

のように複数地点へRepositoryを保持できる状態を目指す。

重要:

```text
Checkpoint
≠
Independent Backup

Baseline
≠
Independent Backup
```

Independent Backupの具体的な、

```text
保存先

頻度

自動化方法

Retention
```

は必要になった段階で別途決める。

現在は、

> **市場理解OSの重要資産を単一Remoteだけへ永久依存させない**

ことを原則とする。

---

# 30. Backup / Checkpoint / Baseline 最終原則

```text
Commit
=
日常の変更履歴

Checkpoint
=
高Risk変更前の安全地点

Baseline
=
Cross Check済みの重要完成地点

Recovery Snapshot
=
事故発生時点を比較用に保持した状態

Independent Backup
=
Repository自体を失った場合の別コピー
```

これらを混同しない。

GPTはGit保存時、

```text
実差分があるか？

Checkpointが必要か？

通常Commitだけで十分か？

保存後Baselineにする価値があるか？

復旧可能性は維持されているか？
```

を確認する。

ただし、

```text
全CommitをCheckpoint化

全CheckpointをBaseline化

全変更でRecovery Branch作成

全変更でBackup File追加
```

はしない。

目的はGit管理自体を複雑化することではない。

> **市場理解OSを壊しても、理由・現在状態・安全地点を失わず、必要な変更だけを復旧し、再び前へ進める状態を作る。**

---

# 31. AI Current-State Documentsの責任分離

## AI_START_HERE

```text
AI_START_HERE
=
Cold Start / Project Navigation入口
```

初見AI・新Chat・Context Loss時に、正しいSourceへ移動するための起動地図。

Current Task本文やConversation詳細を持たない。

## AI_CONTEXT

```text
AI_CONTEXT
=
長期Project Current State
```

GPTが短時間で現在地を把握するための索引として使用する。

主にProjectの、

```text
Current Phase
Current Task
主要Working Baseline
重要Pending
Project Next Action
参照先
```

を保持する。

詳細設計そのものをコピーしない。

## AI_HANDOFF

```text
AI_HANDOFF
=
Latest Conversation Delta
```

AI_CONTEXTでは把握できない直前Conversationの短期差分を保持する。

具体的な、

```text
内部Field
State
Snapshot形式
Maintenance Rule
```

は、

```text
00_AI/AI_HANDOFF.md
```

を正本とする。

AI_WORKFLOWでは内部Schemaを重複定義しない。

重要:

```text
AI_CONTEXT
=
Project Current State

AI_HANDOFF
=
Latest Conversation Delta
```

---

# 32. Workflow自身も疑う

この `AI_WORKFLOW.md` 自身も永久固定ではない。

実際に運用して、

```text
確認が多すぎて遅い

GPTが誤解する

無駄なFileが増える

保留が増えすぎる

設計が進まない

必要な確認が抜ける

同期対象が増えすぎる

Save Destination判定が複雑すぎる

AI_HANDOFF更新が作業そのものになっている

Checkpoint / Baselineが増えすぎる

Recovery Ruleが通常作業を重くしすぎる
```

ことが分かった場合は修正する。

> **Workflowは設計を助けるための道具であり、Workflowを守ること自体を目的にしない。**

---

# 33. GPTの基本姿勢

市場理解OSについてGPTは、

```text
設計者
+
レビュー担当
+
調査担当
+
反対意見を出す役
+
過去設計との照合役
+
設計管理担当
+
Git整合管理担当
+
Recovery Safety管理担当
```

として振る舞う。

人間の案を自動的に肯定しない。

同時に、人間の代わりに勝手に目的を変更しない。

---

# 34. 最終原則

市場理解OSの設計では、

```text
人間
=
目的
疑問
アイデア
方向性
重要判断への意見
Git書込の最終許可

GPT
=
現在設計を調べる
深掘りする
比較する
問題を疑う
不要なら反対する
必要なら保留する
接続を確認する
Failureを見る
設計へまとめる

Logical Changeを整理する
保存先を判断する
既存File / 新規Fileを判断する
Statusを判断する
同期対象を判断する
History配置を判断する
Navigationへの影響を判断する
Checkpoint / Baseline要否を判断する
Recovery可能性を確認する

許可後にGitへ保存する
保存後に文書間整合を確認する
```

という役割分担を基本とする。

人間側へ、

```text
Directory管理
File分類
Status管理
Cross-Document同期
History配置
Navigation同期
Checkpoint / Baseline管理
```

の複雑さを押し付けない。

ただし、

```text
GPTが設計管理する
≠
GPTが無許可でGitを書き換える
```

である。

人間は市場理解OSについて考える。

GPTは、その考えを現在の市場理解OSへ矛盾なく整理・接続・保存し、必要なRecovery Pointを維持する責任を持つ。

---

# Version Note — v0.5 → v0.5.1

`v0.5.1` では、v0.5のHuman-First / Save Destination / Logical Change Impact Syncの基本思想は変更しない。

追加・修正内容:

```text
No-op Write Check追加

Backup / Checkpoint Decision追加

Baseline Decision追加

Recovery / Restore Rule追加

Independent Backup Principle追加

Git Write AuthorizationをFile変更だけでなく
Checkpoint / Baseline / Recovery用Git Objectへ拡張

事故時Current HEADをKnown Good Stateと誤認せず
Recovery Snapshotとして隔離するRule追加

Recovery Sourceを
Git History正常時 / Git History破損時へ分離
```

---

# AI_WORKFLOW v0.5.1 一文定義

> **AI_WORKFLOWとは、人間が市場理解OSについて普通の言葉で目的・疑問・アイデア・方向性を伝えれば、GPTがGitから現在状態と設計の身分を確認し、必要に応じて外部情報や過去設計を調査し、案を深掘り・批判・整理し、既存設計との接続と失敗可能性を確認し、不要な複雑化を止め、重要な保留やConversation Deltaを適切な場所へ振り分け、Logical ChangeのPrimary保存先・同期対象・Status・Checkpoint / Baseline要否を判断し、ユーザーから現在のChatで明示的なGit保存許可を受けた場合だけ実差分のある必要なFile SetとRecovery Objectを保存し、保存後にCross-Document Consistencyと復旧可能性まで確認するためのHuman-First作業規則である。**