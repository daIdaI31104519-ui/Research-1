# DESIGN CHANGE LOG

Status: ACTIVE HISTORY

この文書は、市場理解OSで起きた主要な設計変更を保存する。
完成形だけでなく、**何を変え、なぜ変えたか**を残す。

---

## CHANGE-001 — 単純な「市場→AI→Trade」から循環型研究OSへ

### 変更前
市場情報をAIへ渡し、そのまま売買判断へつなげる単純な構造を中心に考えていた。

### 問題
- 市場変化の理由や失敗原因を後から説明しにくい。
- 負けた時に、Data / Feature / Causal / Signal / Executionのどこが悪かったか分からない。
- 未来予測へ依存しすぎる。

### 変更後
```text
観測
→ 測定
→ 市場理解
→ Evidence
→ Causal Hypothesis
→ Market DNA
→ Research
→ Knowledge
→ Production
→ Defense
→ Trade
→ Post-Trade
→ Researchへ戻る
```

### 状態
ADOPTED CONCEPT

---

## CHANGE-002 — 「負けた→Trainer」を廃止し、原因別再研究へ

### 変更前
```text
Trade
→ Logger
→ Trainer
→ Model Update
```

### 問題
Lossの原因がModelとは限らない。
Data Failure、Feature Failure、Causal Failure、DNA Failure、Signal Failure、Execution Failure、Regime Shift等を同じTrainerへ送ると誤学習しやすい。

### 変更後
```text
Trade / Trial Result
↓
Post-Trade Analysis
↓
どこから問題が始まったか分類
↓
適切なResearch領域へ戻す
```

### 状態
ADOPTED CONCEPT

---

## CHANGE-003 — ResearchがProductionを直接書き換えない

### 変更前
研究結果や再学習結果を本番戦略へ直接反映する考えが含まれていた。

### 問題
- 過学習や一時的な失敗へ過剰反応する。
- 未検証Hypothesisが実資金へ入る危険がある。
- ResearchとProductionの責任境界が壊れる。

### 変更後
```text
Research
→ Candidate
→ Validation
→ Forward Evidence
→ Approval / Governance
→ Production Candidate
→ Production
```

研究結果はCandidateとして扱い、昇格手順を通す。

### 状態
ADOPTED CONCEPT

---

## CHANGE-004 — AI Team / AI Meeting中心構造をLegacy化

### 変更前
複数AIをMarket AI / Risk AI / Psychology AI / Strategy AI等に分け、AI Meetingで統合してSignalへ送る構想があった。

### 問題
- AI同士が同じ誤りを共有する可能性。
- 多数決が正しさを保証しない。
- Production Pathが重くなる。
- AI障害がLive停止へ直結しやすい。
- Rule / Calculation / Hard RiskまでAIへ寄せる必要性が薄い。

### 変更後
AIは単独Layerではなく、横断的な **AI Assistance** として再配置する方向へ変更。

主な役割候補:
- Market Intelligenceの意味解釈
- Alternative Hypothesis生成
- Causal Candidate生成
- Research計画・反証案
- Trade Thesis査読
- Post-Trade Attribution候補
- Incident説明
- Human向け日本語説明

Hard Risk、Permission、Execution、確定計算は原則Rule/Python側に残す。

### 状態
SUPERSEDED / REDESIGNED

---

## CHANGE-005 — Quantumを必須通過LayerからResearch Toolへ

### 変更前
Quantum LayerをMarket UnderstandingからProductionへ向かう必須Layerとして扱う案があった。

### 問題
- Live Pathを不必要に複雑化する。
- 量子探索結果自体が正しさを保証しない。
- 探索とProduction判断の責任が混ざる。

### 変更後
Quantum / Searchは、特徴量・組み合わせ・パラメータ・探索候補を見つけるResearch Toolとして扱う。
探索結果も通常Candidateと同じValidationを通す。

### 状態
SUPERSEDED

---

## CHANGE-006 — Stress Labを独立巨大LayerからValidation Toolへ

### 変更前
Stress Labを研究全体に近い独立Layerとして扱う時期があった。

### 問題
Research、Validation、Knowledgeとの責任が重複した。

### 変更後
StressはResearch / Validation内で、仮説・Edge・Hypothesis Setを意図的に壊し、以下を得るToolとして整理する。

```text
StressResult
→ FailureBoundary
→ Constraint
```

### 状態
SUPERSEDED / REDESIGNED

---

## CHANGE-007 — 単一Hypothesis中心ProductionからMulti-Hypothesis Trade Thesisへ

### 変更前
一つの強いHypothesisを本番判断の中心に置く考えが強かった。

### 問題
現在市場では複数Mechanismが同時に存在する可能性があり、単一HypothesisだけではContextを表せない。
一方、Hypothesis数の多数決ではShared Evidenceを何度も数える危険がある。

### 変更後
```text
Approved Hypothesis Pool
+ Current Market DNA / Context
↓
Applicable Hypothesis Set
↓
Trade Thesis
```

Hypothesisは役割を分けて扱う。
- Primary
- Supporting
- Conditional
- Contradicting

Hypothesis数ではなく、独立性、Shared Evidence、Dependence、Applicability、Contradiction、Expected Value等を見る。

### 状態
ADOPTED CONCEPT

---

## CHANGE-008 — Historical / OOS / Demo / Live Evidenceを分離

### 変更前
異なる検証結果を件数や勝率でまとめて評価する危険があった。

### 問題
Evidence Sourceごとに意味が違う。

### 変更後
Historical、OOS、Demo Forward、Stress、Live等は別Evidence Channelとして保持し、単純合算しない。

### 状態
ADOPTED CONCEPT

---

## CHANGE-009 — Overall Scoreだけを正本にしない

### 変更前
Hypothesis Score等を最終的に一つの総合値へまとめる案があった。

### 問題
Overallが同じでも、Stress、Causal Support、Data Quality、Contradiction等の内訳によって意味が全く異なる。

### 変更後
総合値を使う場合でも内訳を保持する。
さらにProductionではExpected Value、Data Quality、Applicability、Constraint、Uncertainty、Risk等を意味の違う要素として扱い、単純な一つの総合点だけでTrade Permissionを決めない方向へ改善。

### 状態
REDESIGNED

---

## CHANGE-010 — Human-First Rebuildへ

### 変更前
設計を非常に細かく深掘りし、Role / Object / State / Contract / Governance等を先行して増やしていた。

### 問題
設計自体は精密になった一方、Human側が全体像・現在位置・なぜその構造になったかを把握しにくくなった。

### 変更後
新Repo `Research-1` で次の順番を採用する。

```text
Human Understanding
↓
Connection
↓
Cross-Cutting
↓
Detailed Design
↓
Implementation Spec
↓
Python
↓
Integration
```

旧RepoはReference / Legacy Knowledgeとして残す。

### 状態
ADOPTED PROCESS

---

## CHANGE-011 — Layer単体深掘りからCross-Layer Reconciliationへ

### 変更前
Data保存、Market DNA、Research等を一つずつ深掘りし、その領域内で完成度を上げていた。

### 問題
別領域を後から深掘りすると、必要なData、責任、保存、AI利用、Failure処理等が変わり、単体では正しい設計同士が噛み合わなくなることが分かった。

### 変更後
各Deep Diveに以下を追加する。

```text
単体設計
↓
上流接続確認
↓
下流接続確認
↓
横断機能確認
↓
Impact Analysis
↓
Cross-Layer Reconciliation
↓
設計完了候補
```

さらに `CONNECTION_MAP` と `CROSS_CUTTING_MAP` を用意する。

### 状態
ADOPTED PROCESS

---

## CHANGE-012 — 一本の巨大FlowからResearch Loop / Production Loopへ

### 変更前
Human Mapでも、市場観測からResearch、Knowledge、Production、Tradeまでを一本線で表現していた。

### 問題
毎Trade前にResearchを実行するようにも見え、`Researchは大きく、Live Pathは小さく` という思想とぶつかる。

### 変更後
- Research Loop = Knowledgeを作る大きな循環
- Production Loop = 研究済みKnowledgeから現在使えるものを利用する小さな循環

Post-Trade結果はResearchへ戻す。

### 状態
ADOPTED HUMAN-DESIGN DIRECTION

---

## CHANGE-013 — Market DNAの責任を狭める

### 問題
Human Map上でMarket DNAが、過去比較だけでなくHypothesisの有効性評価まで行うように読める箇所があった。

### 変更後
Market DNAの基本責任は **現在市場を比較可能な状態表現へ変換すること** とする。
過去市場検索やHypothesis性能評価はResearch / Knowledge / Retrieval側の責任として今後詳細化する。

### 状態
PROPOSED / NEXT HUMAN MAP FIX

---

## CHANGE-014 — Expected ValueとRisk Permissionを分離

### 問題
Expected Valueを「Riskを取る価値があるか」と表現すると、後段Risk / Defenseと責任が重なる。

### 変更後
- Expected Value = そのTrade候補に期待収益性があるか
- Risk / Defense = 期待収益性があっても、今実際にRiskを取ってよいか

```text
Positive Expected Value
≠
Trade Permission
```

### 状態
PROPOSED / NEXT HUMAN MAP FIX

---

## CHANGE-015 — AIを「必要だから置くLayer」から「適材適所の横断補助」へ

### 問題
Rule、Calculation、Research、Riskが精密化すると、AIを外しても主要Pipelineが動くため「AIは何のためにいるのか」が曖昧になった。

### 変更後
AIを必須依存にするのではなく、機械だけでは扱いにくい曖昧性へ集中させる。

```text
Python / Rule
= 測る・計算する・守る・実行する

AI
= 解釈する・疑う・仮説を作る・反証する・査読する・説明する
```

### 状態
ADOPTED DIRECTION
