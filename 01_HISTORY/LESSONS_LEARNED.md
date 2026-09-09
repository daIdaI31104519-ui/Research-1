# LESSONS LEARNED

Status: ACTIVE KNOWLEDGE

この文書は、市場理解OSを設計してきた過程で得た教訓を保存する。
単なる失敗一覧ではなく、**同じ設計ミスを繰り返さないための再利用可能なDesign Knowledge**として扱う。

---

## LESSON-001 — 精密化と人間理解は別問題

### 起きたこと
Role、Object、State、Contract、Governance等を細かく設計するほど、AIには扱いやすくなった一方、人間側が全体構造と現在位置を把握しにくくなった。

### 学んだこと
```text
詳細である
≠
人間が理解できる
```

### 今後
複雑なCanonical Design自体を無理に簡略化するのではなく、Human Mapという人間向けの窓を別に持つ。

---

## LESSON-002 — 一つの領域を完璧にしても全体は完成しない

### 起きたこと
Data保存を単体で深掘りしても、後からResearchを考えるとRaw再現性が必要になる。
AIを深掘りするとAI入出力の保存が必要になる。
Productionを深掘りするとTrade ThesisとEvidenceの保存が必要になる。

### 学んだこと
```text
Local Correctness
≠
System Consistency
```

### 今後
各Deep Dive後にCross-Layer Reconciliationを必須にする。

---

## LESSON-003 — 縦のFlowだけでは足りない

### 起きたこと
Collector → Market Intelligence → Causal → DNA → Research → Productionの縦Flowだけを考えると、Storage、Trace、Quality、Version、AI、Security、Failure等の横断責任が後から衝突する。

### 学んだこと
市場理解OSには少なくとも以下の3つの見方が必要。

1. HUMAN MAP — 人間が何を作っているか理解する
2. CONNECTION MAP — 領域同士の接続を見る
3. CROSS-CUTTING MAP — 全領域を横断する責任を見る

---

## LESSON-004 — ResearchとProductionを混ぜると自己改善が暴走しやすい

### 起きたこと
初期の「負ける→Trainer→Rule/Model変更」の発想では、一時的なLossや誤ったFailure Attributionが本番を直接変える危険があった。

### 学んだこと
Researchは発見と検証、Productionは検証済みKnowledgeの使用に責任を分ける。

### 今後
Research結果はCandidateとして昇格手順を通す。

---

## LESSON-005 — Lossだけ見ても原因は分からない

### 起きたこと
Trade LossをModel失敗として扱うと、Data、Feature、Causal、Market DNA、Signal、Defense、Execution、Regime Shift等の別原因を誤ってModelへ学習する。

### 学んだこと
```text
Trade Outcome
≠
Failure Cause
```

### 今後
Post-Tradeでは結果と責任領域を分離し、原因候補を適切なResearchへ戻す。

---

## LESSON-006 — 勝ったTradeも正しさの証明ではない

### 起こり得る問題
Primary Hypothesisが間違っていても別要因で利益になる可能性がある。
逆にTrade Thesisが妥当でもSlippageやExecution FailureでLossになる可能性がある。

### 学んだこと
```text
Trade Outcome
≠ Hypothesis Outcome
≠ Trade Thesis Outcome
≠ Execution Outcome
≠ Risk Outcome
```

---

## LESSON-007 — Hypothesisは数ではなく構造を見る

### 起きたこと
複数Hypothesisを使う方向へ進んだが、単純な3 BUY vs 2 SELLではShared EvidenceやCommon Causeを何度も数える問題がある。

### 学んだこと
Hypothesis間のIndependence、Shared Evidence、Dependence、Redundancy、Contradiction、Applicabilityを見る必要がある。

### 今後
Applicable Hypothesis Set → Trade Thesisへ構造化する。

---

## LESSON-008 — 市場に合わせて仮説を書き換えてはいけない

### 問題
Outcomeや現在市場に都合が良いようにHypothesisを変更すると、研究が後付け説明になる。

### 学んだこと
市場変化に応じて **使用する研究済みHypothesisを選び直すこと** と、Hypothesisそのものを変更することは別。

### 今後
Hypothesis自体を変更する場合は新VersionとしてResearchへ戻す。

---

## LESSON-009 — EvidenceはSourceごとに意味が違う

### 問題
Historical、OOS、Demo Forward、Stress、Liveをまとめて「合計N件・勝率XX%」にすると、証拠の質と現実摩擦の違いが消える。

### 学んだこと
Evidenceは件数だけでなく、どこから得られたかを保持する。

---

## LESSON-010 — 一つのScoreは説明を失わせる

### 問題
Overall Scoreだけ残すと、通常市場では強いがStressに弱い等の重要な違いが消える。

### 学んだこと
Expected Value、Data Quality、Causal Support、Applicability、Constraint、Contradiction、Uncertainty、Riskは意味が違う。

### 今後
総合値を使っても内訳を失わない。Production Permissionを単一Scoreだけへ依存させない。

---

## LESSON-011 — AIを使うこと自体を目的にしない

### 起きたこと
設計が進むほど、計算、State、Risk、Execution等は通常Python / Ruleの方が再現性が高く、「AIがなくても動く」部分が増えた。

### 学んだこと
これは失敗ではなく、AIの責任を絞る機会。

AIが向いているのは主に:
- 意味解釈
- Alternative Hypothesis
- Cause Candidate
- Research Design
- Contradiction / Red Team
- Trade Thesis Review
- Post-Trade Attribution Candidate
- Human Explanation

### 原則
```text
AIを使える
≠
AIを使うべき
```

---

## LESSON-012 — AIはAuthorityではないが、自動化禁止でもない

### 問題
「AIにAuthorityを渡さない」を「毎Trade人間承認」と誤解すると完全自動化の目的と衝突する。

### 学んだこと
事前に定義されたRule / Policy / Risk Limit内で自動運用は可能。
禁止したいのは、生成AIが未検証Hypothesis、Rule、Risk、Credential、Production権限等を勝手に変更して即Liveへ反映すること。

---

## LESSON-013 — Market DNAは万能判断器にしない

### 起きたこと
Human Mapを整理する中で、Market DNAが過去Case検索やHypothesis性能評価まで行うように読める責任混同が見つかった。

### 学んだこと
Market DNAは基本的に「現在市場を比較可能な状態表現へ変換する」責任へ絞る。

Hypothesis評価やKnowledge Retrievalは別責任として設計する。

---

## LESSON-014 — Expected ValueとRisk Permissionは違う

### 起きたこと
Expected Valueを「Riskを取る価値があるか」と定義するとDefense / Riskと役割が重なった。

### 学んだこと
```text
Expected Value
= 期待収益性があるか

Risk / Defense
= 期待収益性があっても今Riskを取ってよいか
```

Positive EVでもData Quality低下、Exchange異常、Liquidity不足、DD超過等でNO TRADEになり得る。

---

## LESSON-015 — 長期保存は「全部永久保存」ではない

### 問題
「研究資産を失わない」を文字通り全Raw永久保存とすると、Storage CostやData Lifecycleと衝突する。

### 学んだこと
本当に守るべきなのは、研究の再現性・説明責任・重要なEvidence・失敗知識・判断履歴。

### 今後
Retention / Regeneration / Provenanceを別途設計し、必要な研究資産を失わずStorageを管理する。

---

## LESSON-016 — 一本の巨大Pipelineで全体を説明しすぎない

### 起きたこと
ResearchからProductionまでを一本線で表すと、毎Trade前にResearchが必要なように見えた。

### 学んだこと
- Research Loop = Knowledgeを作る大きなLoop
- Production Loop = Knowledgeを使う小さなLoop

をHuman Mapで明示する。

---

## LESSON-017 — 旧設計を削除するより、理由付きでLegacy化する

### 学んだこと
AI Team、Quantum Layer、Trainer Loop等の旧案には、その時点では合理的だった理由がある。
完全削除すると将来同じ案を再発明し、同じ失敗を繰り返す。

### 今後
旧案は `REJECTED_IDEAS.md` / Design Historyへ理由付きで残す。

---

# この文書の原則

新しい失敗が出た場合、隠したり消したりしない。

```text
Design Failure
↓
Cause
↓
Lesson
↓
Design Change
↓
再利用可能なDesign Knowledge
```

へ変換する。
