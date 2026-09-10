# CONNECTION MAP v0.1 FAILURE REVIEW

**Status:** REVIEWED / NEEDS REVISION  
**対象:** `02_ARCHITECTURE/CONNECTION_MAP.md` を本設計化する前の v0.1 Draft  
**目的:** v0.1 をCross Checkした結果、どこが噛み合わなかったか、なぜ問題か、v0.2でどう直すかを設計史として保存する。

---

# 0. 結論

Connection Map v0.1 の基本方針は有効だった。

特に、接続を単純な `A → B` ではなく、

```text
DATA
REFERENCE
FEEDBACK
GATE
ADVISORY
```

として分離したこと、さらに Requirement / Failure Impact / Cross-Cutting を見る方針は維持する。

一方、実際に全体接続として並べると、Human Mapだけでは見えにくかった責任抜け・戻り経路不足・Runtime依存の曖昧さが見つかった。

したがって v0.1 は失敗作として廃棄するのではなく、**v0.2へ進むための有効な設計実験**として保存する。

---

# 1. Current Market DNAがResearch経由に見えた

## 問題
v0.1の全体図では、

```text
市場理解
↓
原因候補 / Market DNA
↓
Research
↓
Knowledge
↓
Production
```

のように見え、現在のMarket DNAをProductionが利用するにもResearchを通るように読めた。

## なぜ問題か
Market DNAには、現在市場の状態を表すRuntime Snapshotとしての役割がある。
毎回Researchを通らないとProductionへ届かない構造にすると、本番経路がResearchへ同期依存する。

## v0.2修正方針

```text
Market DNA Snapshot
├─→ Research
└─→ Production Applicability
```

と分岐させる。

---

# 2. Execution後の保有中監督が抜けていた

## 問題
v0.1は、

```text
Risk / Defense
↓
Execution
↓
Post-Trade
```

となっていた。

## なぜ問題か
実際の取引には、Entry後からExitまでの保有期間が存在する。
その間に市場状態・Trade Thesis・Risk状態は変化する。

## v0.2修正方針

```text
Execution
↓
Position / In-Trade Supervision
↓
Exit
↓
Trade Result
↓
Post-Decision / Post-Trade Analysis
```

を明示する。

詳細なPosition Supervisor仕様は別設計で決める。

---

# 3. NO TRADE / WAIT / BLOCKの戻り経路が消えていた

## 問題
v0.1はTradeされたCaseのPost-Trade経路はあったが、

```text
WAIT
NO TRADE
Defense BLOCK
```

がExecutionへ行かないため、その後の評価経路が曖昧だった。

## なぜ問題か
市場理解OSでは、Tradeした判断だけではなく、Tradeしなかった判断も研究対象にする。

例えばDefense BLOCKが本当に正しかったかを後から評価できなければ、Defenseの改善が片方向になる。

## v0.2修正方針
Post-Tradeをより広い概念として扱い、

```text
TRADE
→ Trade Result
→ Post-Decision Analysis

WAIT / NO TRADE / BLOCK
→ Decision Record
→ Post-Decision Analysis
```

とする。

---

# 4. Expected ValueとSignal Decisionを一つにまとめすぎた

## 問題
v0.1では、

```text
Expected Value / Signal判断
```

として一領域にまとめた。

## なぜ問題か
Expected Valueは期待収益性の評価であり、Signalは行動候補の判断である。

```text
Positive Expected Value
≠ Signal TRADE
≠ Defense ALLOW
```

が成立する。

## v0.2修正方針

```text
Trade Thesis
↓
Expected Value Evaluation
↓
Signal Decision
↓
Trade Candidate / WAIT / NO TRADE
↓
Risk / Defense
```

へ分離する。

---

# 5. Evidenceという言葉が複数の責任で混ざった

## 問題
v0.1ではEvidenceがMarket Understanding、Research、Production、Post-Tradeで同じ名称のまま使われた。

## なぜ問題か
例えば以下は意味が違う。

```text
Runtime / Observational Evidence
Research Evidence
Production / Live Evidence
```

これらを同じEvidenceとして扱うと、現在観測された事実、研究で得た証拠、実運用で得た証拠の身分が混ざる。

## v0.2修正方針
Evidence Source / Evidence Roleを区別する。

現在市場のEvidenceは既存KnowledgeのApplicability判断には使えるが、それだけで新しい未検証EdgeをProductionへ昇格させない。

---

# 6. Data Qualityが領域とCross-Cuttingの両方に存在した

## 問題

```text
市場観測 / Data Quality
```

と、Cross-Cuttingの

```text
Data Quality
```

が重複していた。

## v0.2修正方針
責任を分ける。

```text
Data Quality Evaluation
= Data取得時などで品質を測る

Quality Propagation / Policy
= 品質低下を下流へどう伝え、どう制限するか
```

前者は局所機能、後者は横断責任とする。

---

# 7. Researchへの戻り口が多方向に直接接続されていた

## 問題
Data Quality、AI、Post-Trade、Execution、Market Understanding等から直接Researchへ接続すると、実装時に各ModuleがResearch内部へ直接依存しやすい。

## v0.2修正方針
共通入口を置く。

```text
各領域
↓
Research Candidate
↓
Research Intake / Router
↓
適切なResearch
```

各領域はResearchを直接実行せず、Research Candidateを生成する責任までにする。

---

# 8. Post-TradeがKnowledgeを直接変更できるように読めた

## 問題
Post-TradeからKnowledge Evaluationへ繋ぐだけでは、将来、

```text
LOSS
↓
Knowledge Update
```

のような直接更新へ実装が流れる可能性がある。

これは過去に避けた `Loss → Trainer → Model Update` と同型の問題になる。

## v0.2修正方針

```text
Post-Decision Analysis
↓
Research Candidate / Evidence
↓
Research
↓
Validation
↓
Knowledge Update Candidate
```

とし、Post-TradeはKnowledgeを直接書き換えない。

---

# 9. Dependencyの強さが定義されていなかった

## 問題
接続先が分かっても、それが本番停止に直結する必須依存なのか、補助依存なのか分からなかった。

## v0.2修正方針
Connection Typeとは別にDependency Strengthを持つ。

候補:

```text
HARD
SOFT
OPTIONAL
ASYNC
```

例:

```text
Production → Current Market Data
= HARD

Production → AI Review
= OPTIONAL

Post-Decision → Research
= ASYNC
```

特にProductionをResearchやAIへ無条件に同期依存させない。

---

# 10. Time / Cycle / Freshnessが横断責任から抜けていた

## 問題
市場システムでは、同じ値でも「いつの値か」で意味が変わる。

```text
Current Data
Stale Data
Previous Cycle DNA
Current Cycle DNA
Old Knowledge
```

を区別できないと接続自体が正しくても時系列が壊れる。

## v0.2修正方針
Cross-Cutting Responsibilityへ、

```text
Time / Cycle / Freshness
```

を追加する。

具体的なID・Timestamp Contractは後の詳細設計で決める。

---

# 11. AI Outputの身分が曖昧だった

## 問題
AI AssistanceをADVISORYにした方向は正しいが、AI InterpretationがMeasured Factのように扱われる危険が残った。

## v0.2修正方針
概念上、最低限以下を分離する。

```text
Measurement
≠ AI Interpretation
≠ AI Hypothesis Candidate
```

AI Outputには、

```text
ADVISORY
INTERPRETATION
CANDIDATE
```

等の身分が分かるようにする。

AIからExecution / Hard Risk / Permissionへ直接Authority線を引かない。

---

# 12. Approved Trade Intentを誰が作るか曖昧だった

## 問題
Execution入力として `Approved Trade Intent` を置いたが、どの領域が何を確定するのかが曖昧だった。

## v0.2修正方針

```text
Trade Thesis
↓
Expected Value Evaluation
↓
Signal Decision
↓
Trade Candidate
↓
Risk / Defense
↓
Risk Permission / Risk Ceiling
↓
Execution Logic
↓
Order Intent
↓
Exchange
```

と分ける。

基本責任は、

```text
Signal
= 行動候補

Risk / Defense
= 許可・制限

Execution
= 注文方法へ変換
```

とする。

---

# 13. Market DNAの「定義」と「Snapshot」を区別する必要が見えた

これはv0.1の重大矛盾ではないが、将来のVersion管理上重要な発見。

```text
Market DNA Definition
= DNAをどう計算・表現するか

Market DNA Snapshot
= 特定時点で実際に生成された市場状態
```

Researchが改善する対象と、ProductionがRuntimeで読む対象を混ぜない。

正式Object設計は後で行う。

---

# 14. v0.1から残すもの

以下はv0.2でも維持する。

```text
DATA
REFERENCE
FEEDBACK
GATE
ADVISORY
```

というConnection Type。

さらに、

- 上流 / 下流
- Input / Output
- Requirement
- Failure Impact
- Trace
- Cross-Cutting Responsibility

を見る方針も維持する。

---

# 15. 今回の一般化された教訓

## 教訓A — 実行された経路だけ描いてはいけない

市場理解OSでは、

```text
TRADEした
TRADEしなかった
BLOCKされた
WAITした
異常で止まった
```

すべてがシステム上の結果である。

成功経路だけでなく、**非実行経路・停止経路・戻り経路**までConnection Mapへ入れる。

## 教訓B — Connectionは矢印だけでは不足する

最低でも、

```text
Connection Type
+
Dependency Strength
+
Failure Impact
```

を見る必要がある。

## 教訓C — Runtime経路とResearch経路を分ける

研究対象だからといって、Runtime Productionが毎回Researchへ依存してよいわけではない。

```text
Researchは大きく
Productionは小さく
```

というHuman Mapの思想を、接続レベルでも守る。

## 教訓D — CandidateとAuthorityを混ぜない

AI、Post-Trade、Anomaly Detector等は新しい知見を提案できる。

しかし、

```text
Candidate
≠ Production Authority
```

である。

Research / Validation / Governanceを通して昇格させる。

---

# 16. v0.2へ進む際の必須修正一覧

```text
01 Current Market DNA → Production直結経路を追加
02 Position / In-Trade Supervisionを追加
03 WAIT / NO TRADE / BLOCKのPost-Decision経路を追加
04 Expected ValueとSignal Decisionを分離
05 Evidence Role / Sourceを区別
06 Data Quality EvaluationとQuality Propagationを分離
07 Research Intake / Routerを共通入口化
08 Post-TradeからKnowledge直接更新を禁止
09 Dependency Strengthを追加
10 Time / Cycle / FreshnessをCross-Cuttingへ追加
11 AI Outputの身分を明確化
12 Signal / Risk / Executionの責任を分離
13 Market DNA DefinitionとSnapshotを将来分離可能にする
```

---

# 17. Status

```text
Connection Map v0.1
= REVIEWED / NEEDS REVISION

次
= CONNECTION MAP v0.2
```

v0.1は削除せず、このReviewを設計史として残す。

目的は古い案を守ることではなく、**なぜv0.2へ変えたのかを将来追跡できるようにすること**である。
