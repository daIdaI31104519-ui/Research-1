# AI_WORKFLOW — 失敗と改善履歴

**Status:** ACTIVE HISTORY  
**対象:** AI_WORKFLOW v0.1 → v0.5.1  
**目的:** 市場理解OSをGPTと人間で設計する際に、どの運用案がなぜ問題になり、どう改善したかを残す。

---

# 0. この文書の役割

この文書は現在使う作業規則ではない。

現在の作業規則は、

```text
00_AI/AI_WORKFLOW.md
```

を参照する。

ここでは、

```text
何が問題だったか
↓
なぜ問題だったか
↓
どう直したか
↓
何を今後繰り返さないか
```

を履歴として残す。

目的は古い案を守ることではなく、将来同じ失敗を理由を忘れたまま再発明しないことである。

---

# 1. 最初の問題 — 設計が精密になるほど人間が分からなくなった

## 起きたこと

市場理解OSの設計を精密化するため、Role、Object、State、Contract、Governance、AI、Research、Market DNA等を細かく分けていった。

しかし詳細化するほど、

```text
今どこを設計している？
何が確定？
何が案？
次は何？
```

を人間が把握しにくくなった。

## 問題

AIには扱いやすいが、人間側が設計全体を追えない。

## 改善

Human-First Rebuildを採用し、AI用にも作業方法を管理する `AI_WORKFLOW` を作る方向へ進んだ。

## 教訓

```text
精密
≠
分かりやすい
```

---

# 2. v0.1 — GPTが関連事項を広げすぎる問題

## 問題

GPTが一つの設計を深掘りすると、関連する別Layer、Storage、AI、Failure、Contract等まで一度に展開しやすかった。

結果、

```text
1つ設計する
↓
別問題発見
↓
その問題を深掘り
↓
さらに別問題発見
↓
現在Taskを見失う
```

状態になった。

## 改善

Scope Lockと、

```text
今考える
後で考える
今は考えない
```

という分離を導入した。

## 教訓

```text
関連している
≠
今設計する
```

---

# 3. v0.1 — ユーザーの発言を設計変更と誤認する危険

## 問題

ユーザーが、

```text
この案どう？
```

と質問しただけでも、GPTがCurrent Design変更として扱う可能性があった。

## 改善

一時期、

```text
Task Authority
Design Authority
Git Write Authority
```

を明示的に分離した。

後のv0.4では、人間がこれらの専門語を覚える必要はなくし、GPT側が意味を判断する方向へ簡略化した。

## 教訓

```text
質問
≠
採用

検討
≠
変更

保存
≠
Canonical化
```

---

# 4. v0.1 — DRAFTと現在基準の間がなかった

## 問題

設計途中では、Canonicalではないが次の設計の基準として使いたい文書が存在する。

DRAFT / CANONICALだけではこの状態を表現しにくかった。

## 改善

`WORKING BASELINE` の考え方を導入した。

## 教訓

```text
DRAFT
+
現在の作業基準
```

は成立する。

Canonical化を待ってすべての作業を止める必要はない。

---

# 5. v0.1 — Source同士の矛盾をAIが勝手に融合する危険

## 問題

Human Map、Detailed Design、History、旧Repo等に異なる内容がある場合、AIが自然な文章へ勝手に統合すると、どれが現在設計か分からなくなる。

## 改善

Current Design判定時に、

```text
Role
Status
History
Superseded関係
```

を見る方向へ変更した。

## 教訓

```text
新しい
≠
正しい

Gitにある
≠
採用中
```

---

# 6. v0.1 — OPEN ISSUEの保存場所問題

## 問題

後で考える重要問題を会話だけに残すと、新しいChatで失われる。

一方、すべてを独立Issue Fileへ保存すると管理が重くなる。

## 初期案

`00_AI/OPEN_ISSUES.md` を作る案が出た。

## 改善

v0.4.1では簡略化し、

```text
軽い保留
→ 会話内

今後へ影響する重要保留
→ AI_CONTEXT

大きな変更・失敗・却下理由
→ HISTORY
```

とした。

## 教訓

未解決事項を忘れてはいけないが、管理ファイルを増やしすぎてもいけない。

---

# 7. v0.1 — Git書込許可の範囲が曖昧

## 問題

ユーザーが、

```text
この設計を保存して
```

と言った場合に、GPTがDesign、History、README、AI_CONTEXT等を無制限に変更する危険があった。

## 改善

現在は、

> **「GITに保存して」は現在会話しているLogical Changeへの書込許可**

とした。

関連するHistoryやAI_CONTEXTは必要な範囲で更新できるが、無関係なRepo全体は変更しない。

## 教訓

Git Writeは必要範囲に閉じる。

---

# 8. v0.2 — Workflow自身にCurrent Designを書きすぎた

## 問題

AI_WORKFLOWへ、

```text
Market DNA ≠ Signal
Research ≠ Production
AI ≠ Authority
```

など市場理解OS固有のCurrent Designを大量に書く案が出た。

この方法ではCurrent Designが変わるたびにWorkflowも変更する必要がある。

## 改善

```text
AI_WORKFLOW
= HOW

AI_CONTEXT / 各設計書
= WHAT / CURRENT STATE
```

へ責任を分離した。

## 教訓

Workflowは作業方法を持ち、設計内容そのものを第二の正本として持たない。

---

# 9. v0.2 — VersionとStatusを混同した

## 問題

`v1.0 = Canonical` のようにVersionと成熟状態を結びつける案があった。

しかし、

```text
Version
= 内容の世代

Status
= 文書や判断の状態
```

であり別物。

## 改善

Version自体へAuthorityを与えない方向へ変更した。

## 教訓

```text
新Version
≠
正式採用
```

---

# 10. v0.2 — AI_CONTEXT Commit SHAの自己参照問題

## 問題

AI_CONTEXT本文へ自分自身を含むCommit SHAを書こうとすると、ファイル内容変更でCommit SHAも変わるため自己参照になる。

## 改善

AI_CONTEXTはCurrent Stateの索引として扱い、Git自体が持つCommit情報を無理に本文へ埋め込まない方向へ簡略化した。

## 教訓

状態管理を精密化しすぎて、運用を複雑にしない。

---

# 11. v0.2 — Bootstrap問題

## 問題

Workflowでは `AI_CONTEXT.md` を最初に読む設計だったが、初回構築時にはそのファイル自体が存在しない。

## 改善

AI_CONTEXTがない場合は、

```text
README
↓
HUMAN_MAP
↓
Current Architecture
↓
History
```

から現在状態を復元するBootstrap方式を採用した。

後に `AI_START_HERE.md` を追加し、Cold Start / Context Lossの入口を独立したNavigation責任として分離した。

## 教訓

運用規則は初回起動時も成立しなければならず、Cold Start手順をWorkflow本文へ重複保持し続けない。

---

# 12. v0.3 — 人間向けCommand体系を作りすぎた

## 問題

人間がGPTへ正確に意思を伝えるため、

```text
採用
保留
OPEN
WORKING BASELINE
History同期
AI_CONTEXT同期
Canonical
```

等の専用Commandを多く定義する案が出た。

しかしこれはHuman-Firstの目的と逆行した。

## 改善

人間が覚える基本表現を、原則として次の2つまで削った。

```text
「この案を考えて」

「GITに保存して」
```

その他は普通の日本語で会話する。

## 教訓

人間へ設計管理の複雑さを押し付けない。

---

# 13. v0.3 — 「採用」と「Working Baseline」を混ぜた

## 問題

一つのConceptを採用したことと、文書全体を現在基準へ昇格させることを同じ扱いにしそうになった。

## 改善

後の簡略化では、人間にこの違いを操作させるのではなく、GPTが文書の成熟度・役割・Current Designとの整合を見て扱う方向へ変更した。

## 教訓

局所Decisionと文書全体のDesign Roleは同じではない。

---

# 14. v0.3 — Workflowが長くなりすぎた

## 問題

安全性を高めるためRuleを追加し続けた結果、Workflow自体が巨大化し、毎回読むコストが増えた。

## 改善

v0.4では、人間操作を簡略化し、GPT側の責任を中心に再設計した。

## 教訓

```text
Workflowを精密化する
≠
Ruleを増やし続ける
```

Workflowは設計を前へ進めるための道具である。

---

# 15. v0.4 — 「GITに保存」がCanonical化に見える問題

## 問題

保存命令だけで正式採用扱いになる可能性が残った。

## 改善

v0.4.1で、

```text
GITに保存
≠
自動Canonical化
```

を明示した。

GPTが現在成熟度を見て適切なStatusで保存する。

## 教訓

StorageとAuthorityを混ぜない。

---

# 16. v0.4 — Current Designを更新日時で判断する危険

## 問題

GitにはCurrent Designだけでなく、Draft、Reference、History、Failure Review、Rejected、Legacyが存在する。

新しいファイルがCurrent Designとは限らない。

## 改善

v0.4.1でCurrent Design判定時に、

```text
File Role
Status
Design History
採用状態
Superseded関係
```

を見るRuleを追加した。

## 教訓

GitはKnowledge Storeであり、最新ファイル一覧がそのままCurrent Designではない。

---

# 17. v0.4 — 保留事項の扱い

## 問題

人間操作を簡単にすると、後回しにした重要問題を失う危険がある。

## 改善

v0.4.1で重要度に応じて、

```text
会話
AI_CONTEXT
HISTORY
```

へ振り分ける方式にした。

v0.5ではさらに、

```text
次Chatへ引き継ぐ最新Conversation差分
→ AI_HANDOFF

長期Project Current State / Pending
→ AI_CONTEXT
```

へ責任を分離した。

## 教訓

簡略化しても重要な未解決事項のTraceは失わず、短期Conversation Stateと長期Project Stateを混ぜない。

---

# 18. v0.4 — 外部ネットを毎回見るべきか問題

## 問題

毎回Web調査すると作業が重くなり、内部Architectureの設計まで外部情報へ引っ張られる。

逆に全く見ないと、API、Library、Exchange仕様、技術実現性等で古い前提を使う危険がある。

## 改善

v0.4.1では、

```text
内部設計だけで判断できる
→ Git中心

外部仕様・現在技術・研究・実現性が判断を変える
→ Web確認
```

とした。

## 教訓

外部Sourceは必要な時に使う設計材料であり、Current Designの正本ではない。

---

# 19. 現在の人間とGPTの役割分担

## 人間

```text
目的
疑問
アイデア
方向性
重要判断への意見
Git書込の最終許可
```

を普通の言葉で伝える。

基本指示は、

```text
「この案を考えて」

「GITに保存して」
```

を中心とする。

## GPT

```text
Current Git確認
必要なHistory確認
必要なら旧Repo / Web確認
深掘り
必要性判断
重複・矛盾確認
反対意見
保留提案
Cross Check
Failure確認
設計整理
Logical Change整理
保存先判定
既存File / 新規File判定
Status判定
Impact Sync判定
Checkpoint / Baseline判定
Recovery Safety確認
許可後のGit保存
保存後Cross-Document確認
```

を担当する。

---

# 20. 今後の再発防止原則

今後AI_WORKFLOWを改善する場合も、次を守る。

```text
人間側のCommandを増やしすぎない

保存先判断を人間へ押し付けない

WorkflowへCurrent Designをコピーしすぎない

AI_CONTEXTとAI_HANDOFFを混ぜない

関連事項を全部同時に設計しない

Git保存と採用を混同しない

Gitの更新日時だけでCurrent Designを決めない

同一内容のNo-op Commitを作らない

Checkpointを毎Commit作らない

CheckpointとBaselineを混同しない

事故時Current HEADを即破壊しない

同じ情報を複数Documentへ重複保存しない

過去失敗を削除しない

重要な保留を失わない

Webを使うこと自体を目的にしない

GPTはYESマンにならない

Workflowを守ること自体を目的にしない
```

---

# 21. 現在の到達点

```text
AI_WORKFLOW v0.1
↓
Scope / Authority / Source管理を追加
↓
AI_WORKFLOW v0.2
↓
Conflict / Git Safety / Context等を強化
↓
AI_WORKFLOW v0.3
↓
人間向けCommand体系が複雑化
↓
簡略化方針へ転換
↓
AI_WORKFLOW v0.4
↓
保存Status / Current Design判定 / 保留 / Web利用を修正
↓
AI_WORKFLOW v0.4.1
↓
Cold Start / Context RecoveryをAI_START_HEREとAI_HANDOFFへ責任分離
↓
Save Destination Resolution
+
Logical Change Impact Syncを導入
↓
AI_WORKFLOW v0.5
↓
No-op Write Check
+
Checkpoint / Baseline
+
Recovery / Restore
+
Independent Backup Principleを導入
↓
AI_WORKFLOW v0.5.1
```

現在のWorkflowは、

> **人間が設計管理用語・保存先・同期先・Recovery Pointを管理するのではなく、GPTが設計管理とGit Safetyの複雑さを引き受ける**

方向へ進んだ。

---

# 22. v0.5 — Context継続・保存先・文書同期の運用Failure

## 起きたこと

長いChatで設計を続けると、Context LimitやChat切替によって、Gitへまだ保存していないConversation Decisionや次の作業地点を失う危険が見えた。

同時に、設計が増えるほど人間が、

```text
どのmdへ保存するか
既存Fileか新規Fileか
AI_CONTEXTも更新するか
Historyへ残すか
READMEやNavigationへ影響するか
```

まで判断する必要が出始めた。

さらに、対象Designだけ保存すると、

```text
Designは新しい
AI_CONTEXTは古い
HANDOFFは未保存扱い
Navigationは旧状態
```

というDocument間の状態ズレが起こり得る。

## 問題

これはHuman-Firstの目的に反する。

人間が市場理解OSそのものではなく、File配置・同期・履歴管理へ注意を奪われる。

また、Conversation StateとProject Current Stateを同じFileへ持たせると、AI_CONTEXTが日記化・巨大化する。

## 改善

v0.5で次を導入した。

```text
AI_START_HERE
= Cold Start / Navigation

AI_WORKFLOW
= HOW / WHEN / Git管理

AI_CONTEXT
= Long-Term Project Current State

AI_HANDOFF
= Latest Conversation Delta
```

さらに、

```text
Save Destination Resolution
=
Logical ChangeのPrimary Owner DocumentをGPTが判断

Logical Change Impact Sync
=
Primary変更により同期が必要なDocumentだけを判定
```

をGit保存工程へ組み込んだ。

原則として、

```text
新しいアイデア
≠ 新しいFile

関連している
≠ 変更対象

Authority
≠ Save Destination
```

とする。

## 教訓

```text
Human
= 目的・疑問・アイデア・方向性・最終Git許可

GPT
= 設計・保存先・同期先・Status・History・Navigation整合
```

と分ける。

また、

> **対象Designを保存することではなく、Logical Changeを必要範囲で矛盾なく保存すること**

をGit運用の単位とする。

---

# 23. v0.5.1 — Git履歴だけではRecovery Pointが分かりにくい問題

## 起きたこと

Git保存工程を実運用した結果、同一内容の `AI_WORKFLOW` が複数回Commitされ、Git Historyへ意味のないNo-op Commitが発生した。

また、Repository全体を確認すると、

```text
main Branchのみ
Tagなし
明示的な一般Checkpoint Ruleなし
```

であり、Git History自体は存在しても、

```text
どの地点が安全なのか
どの変更前へ戻るべきか
どこまでが確認済み完成地点か
```

を人間・AIが一目で判断しにくい状態だった。

さらに、事故時に `main` を即Rollbackすると、事故後にしか存在しない正常な変更まで失う危険がある。

## 問題

```text
Commit Historyがある
≠
Recovery Strategyがある
```

である。

すべてのCommitをCheckpoint化すると逆にノイズになる一方、明示的Recovery Pointが全くないと高Risk変更の復旧Costが上がる。

また、CheckpointとRepository外Backupを同一視すると、Remote / History自体の破損へ対応できない。

## 改善

v0.5.1で次を導入した。

```text
No-op Write Check
=
Current Gitと同一内容ならWrite / Commitしない

Checkpoint
=
高Risk変更前の安全地点

Baseline
=
Cross Check済みの重要完成地点

Recovery Snapshot
=
事故時Current HEADを比較用に隔離保存

Independent Backup
=
Repository自体を失った場合の別コピー
```

Git保存フローを、

```text
Cross Check
↓
No-op Write Check
↓
Checkpoint Decision
↓
Git Write
↓
Post-Save Consistency Check
↓
Baseline Decision
```

へ拡張した。

事故時は、

```text
即Rollback
```

ではなく、

```text
Current HEAD記録
↓
必要ならRecovery Branchへ隔離
↓
Checkpoint / Baselineと比較
↓
必要部分だけRestore
```

を基本とする。

Git History自体が信頼できない場合はIndependent BackupをRecovery Sourceとする。

## 教訓

```text
Commit
≠ Checkpoint
≠ Baseline
≠ Independent Backup
```

である。

Git Safetyは「たくさんBackupを作ること」ではなく、

> **変更前の安全地点・変更後の確認済み地点・事故時点・Repository外Backupを役割分離し、必要な時だけ使うこと**

で成立する。

Human-Firstの観点では、Checkpoint / Baseline要否も人間へ毎回判断させず、GPTがLogical ChangeとRecovery Costから判定する。

---

# 一文まとめ

> **AI_WORKFLOWの改善は、安全性のために人間やWorkflowへ管理負荷を増やす方向ではなく、人間は普通の言葉で市場理解OSを考え、GPTがCurrent Git・保存先・同期先・History・Conversation Delta・Checkpoint / Baseline・Recovery Safetyを必要範囲で管理するHuman-Firstな方向へ進める。**