# CONNECTION — 04_KNOWLEDGE_APPLICABILITY v0.1.1

**Document Role:** Partial Connection Map  
**Status:** REVIEWED / WORKING BASELINE  
**Parent:** `02_ARCHITECTURE/CONNECTION_MAP.md`  
**Purpose:** `03_RESEARCH` から得られる `Validated Research Result` を再利用可能なKnowledgeとして整理し、`02_MARKET_UNDERSTANDING` の現在市場Contextと照合して、「今この市場で意思決定材料として利用可能なKnowledge」を選別し、`05_DECISION` へ渡す接続境界を定義する。

---

# 0. このMapの役割

`04_KNOWLEDGE_APPLICABILITY` は、

> **研究済みKnowledgeをそのままProductionへ流さず、現在市場の状態・成立条件・Failure Boundary・Constraint・Evidence・Version・Uncertainty等と照合し、「今使ってよいKnowledgeだけ」を次の意思決定層へ渡すKnowledge適用フィルター領域**

である。

重要:

```text
Validated Research Result
≠ Knowledge

Knowledge
≠ Currently Applicable Knowledge

Applicable Knowledge
≠ Trade Signal

Applicable Knowledge
≠ Trade Permission
```

04自身はTrade判断を行わない。

---

# 1. 中心的な問い

このMapが扱う中心的な問いは、

> **「研究で得たこの知識は、今この市場で使ってよいのか？」**

である。

各領域の責任を分ける。

```text
03_RESEARCH
= このHypothesis / Edge / Failureは
  再現可能か？
  どこで成立し、どこで壊れるか？

04_KNOWLEDGE_APPLICABILITY
= その研究結果を再利用可能なKnowledgeとして扱えるか？
  そのKnowledgeは今この市場で使えるか？

05_DECISION
= 現在利用可能なKnowledgeをどう組み合わせ、
  どのようなTrade Thesis / 行動候補を作るか？
```

---

# 2. 04内部は二つの経路に分ける

04を一つの同期Pipelineとして扱わない。

大きく、

```text
A. Knowledge Maintenance Path
B. Runtime Applicability Path
```

に分ける。

## A. Knowledge Maintenance Path

```text
03_RESEARCH
↓
Validated Research Result
↓
Knowledge Admission / Promotion
↓
Knowledge Record / Knowledge Pool
```

研究結果を再利用可能なKnowledgeへ整理・更新する非同期寄りの経路。

## B. Runtime Applicability Path

```text
Knowledge Pool
+
Current Market Understanding
+
Market DNA Snapshot
+
Quality / Freshness / Runtime Context
↓
Applicability Evaluation
↓
Constraint / Failure Boundary / Conflict Check
↓
Applicable Knowledge Set
↓
05_DECISION
```

本番時に「今使えるKnowledge」を選ぶRuntime経路。

重要:

> **Production Runtimeが、毎回03_RESEARCHやKnowledge Promotion完了を待つ構造にしない。**

Researchは大きく、Productionは小さく保つ。

---

# 3. 04はTrade判断層ではない

04自身は、

```text
BUY
SELL
LONG
SHORT
TRADE
WAIT
NO TRADE
```

を最終決定しない。

例えば、

```text
Knowledge A
= Current MarketでAPPLICABLE
```

でも、

```text
BUY
```

には直結しない。

重要:

```text
Applicable
≠ Positive Expected Value
≠ Signal TRADE
≠ Risk Permission
```

04が答えるのは、

> **このKnowledgeを現在の意思決定材料として使ってよいか**

までである。

---

# 4. Upstream Input

04は主に二系統からInputを受ける。

## 4.1 Knowledge側

```text
03_RESEARCH
↓
Validated Research Result
```

03の正式Downstream Boundaryと一致させる。

## 4.2 Current Market側

```text
02_MARKET_UNDERSTANDING
├─ Current Market Understanding
└─ Market DNA Snapshot
```

必要に応じて、

```text
Quality Context
Freshness Context
Runtime / Observational Context
```

を参照する。

重要:

```text
Current Market Understanding
= Interpretation / Context

Market DNA Snapshot
= Runtime Market State Representation

Runtime Observation
= Observation / Measurement
```

これらの身分を混同しない。

---

# 5. Validated Research Resultの受け取り

03からの主要Upstream Boundary:

```text
Validated Research Result
```

重要:

```text
Validated Research Result
≠ Supported Resultだけ
```

以下も正しく検証・記録されたResearch Resultになり得る。

```text
SUPPORTED
REFUTED
INCONCLUSIVE
REGIME DEPENDENT
FAILURE BOUNDARY FOUND
CONSTRAINT FOUND
UNKNOWN
```

04はResearch Outcomeの方向だけで価値を決めない。

---

# 6. Knowledge Admission / Promotion

Validated Research Resultを、そのままProduction用Knowledgeとして扱わない。

まず、

```text
Knowledge Admission / Promotion
```

を通す。

ここでいうPromotionは、

> **研究結果を再利用可能なKnowledge Recordとして正式に扱える状態へ整理すること**

であり、

```text
Positive Edgeとして承認
Productionで使用許可
```

という意味ではない。

重要:

```text
Knowledge Admission
≠ Positive Knowledge Approval
≠ Production Approval
```

---

# 7. Knowledge Admissionで確認すること

具体Ruleは後で決めるが、最低限以下を確認可能にする。

```text
再利用可能な意味があるか
Research Resultの身分が明確か
成立条件が追跡可能か
Failure Boundaryが追跡可能か
Constraintが追跡可能か
Evidence Source / Roleが追跡可能か
Uncertaintyが残されているか
Versionを識別できるか
既存Knowledgeとの重複・更新関係を識別できるか
Traceが辿れるか
```

不足する場合、Knowledge Poolへの正式Admissionを保留できる構造を持つ。

---

# 8. Knowledgeは成功したHypothesisだけではない

Knowledgeには、

```text
成功した知識
```

だけでなく、

```text
失敗した知識
反証された知識
利用禁止条件
Failure Boundary
Constraint
矛盾
Unknown
未解決条件
```

も含める。

概念上、例えば以下を保持可能にする。

```text
Positive / Edge Knowledge
Negative / Refutation Knowledge
Failure Knowledge
Constraint Knowledge
Uncertainty Knowledge
Context Knowledge
```

正式分類は後で定義する。

---

# 9. Knowledgeは条件付き知識として扱う

Knowledgeを、

```text
Fundingが高い
→ 下落する
```

のような単純な一文だけで扱わない。

概念上、Knowledgeは以下のContextを持てる必要がある。

```text
Claim / Effect
成立条件
成立しやすい市場状態
弱くなる条件
Failure Boundary
Constraint
Evidence Profile
Uncertainty
対象Asset / Market
Time Horizon
Regime
Version
Validation History
```

具体Field名やSchemaは後で決める。

---

# 10. Knowledge Pool

AdmissionされたKnowledgeを論理的に、

```text
Knowledge Pool
```

として扱う。

Knowledge Poolは、

```text
Trade Rule一覧
SUPPORTED Hypothesis一覧
```

ではない。

役割は、

```text
何が分かったか
どこで成立するか
どこで失敗するか
何が否定されたか
何が禁止条件か
何が不明か
```

を再利用可能な形で参照できるようにすること。

重要:

> `Knowledge Pool` は論理的なKnowledge領域を示す。具体DB / Storage / Retention実装はCross-Cutting / Detailed Designで決める。

---

# 11. Knowledge Version

Knowledgeを永久に同じ内容として扱わない。

```text
Knowledge v1
↓
追加Research
↓
新Evidence / 新Failure Boundary
↓
Knowledge v2
```

となり得る。

重要:

```text
Knowledge Update
≠ 過去Knowledgeの履歴消去
```

将来、

```text
Version
Research Date
Last Validation
Superseded By
Evidence Update
```

等を追跡可能にする。

具体Schemaは後で定義する。

---

# 12. Knowledge Status

Knowledge Poolに存在することと、現在利用可能であることを分ける。

将来的に、

```text
ACTIVE
WEAK
RETIRED
UNDER_REVIEW
SUPERSEDED
```

等を表現できる構造を残す。

ただし正式Lifecycleは後で設計する。

重要:

```text
Knowledge Poolに存在
≠ Current MarketでApplicable
```

---

# 13. Current Market Context

Runtime Applicabilityでは、

```text
Current Market Understanding
Market DNA Snapshot
```

を主要Contextとして利用する。

必要に応じて、

```text
Runtime Observation
Quality Context
Freshness Context
Current Event Context
```

を補助参照する。

04自身がCurrent Market UnderstandingやMarket DNAを再生成しない。

---

# 14. Market DNA Snapshotの役割

Market DNA SnapshotはApplicabilityで重要なReferenceになる。

例えばKnowledgeが、

```text
High Leverage
+
High Volatility
+
Thin Liquidity
```

で成立しやすい場合、Current Market DNAとの一致度は重要な情報になる。

ただし、

```text
Market DNA Similarity
≠ Applicability確定
```

である。

Market DNAはApplicability Contextの一つであり、唯一の判定材料にはしない。

---

# 15. Applicability Evaluation

04のRuntime中心機能。

```text
Knowledge
+
Current Market Context
↓
Applicability Evaluation
```

で、

> **Knowledgeの成立条件と現在市場がどの程度一致しているか**

を確認する。

照合候補:

```text
Asset
Market
Time Horizon
Regime
Trend
Volatility
Liquidity
Leverage
Funding
Flow
ETF
Whale
Macro
Event
Session / Time
Data Quality
Freshness
```

具体軸・式・Thresholdは後で固定する。

---

# 16. Applicability State

単純なTRUE / FALSEだけに潰さない。

概念状態候補:

```text
APPLICABLE
PARTIALLY_APPLICABLE
NOT_APPLICABLE
UNCERTAIN
BLOCKED_BY_CONSTRAINT
NOT_EVALUATED
```

正式State名は後で確定する。

---

# 17. APPLICABLE

Knowledgeの主要成立条件がCurrent Marketで満たされ、

```text
Failure Boundary
Constraint
重大なContradiction
```

も確認されていない状態。

重要:

```text
APPLICABLE
≠ TRADE
```

---

# 18. PARTIALLY_APPLICABLE

一部条件は一致しているが、

```text
重要Condition不足
Context差異
Regime差異
Evidence弱化
```

等がある状態。

後段へ渡す場合も、条件付き・弱い・注意が必要という身分を維持する。

---

# 19. NOT_APPLICABLE

Knowledgeの主要成立条件からCurrent Marketが外れている状態。

例えば、

```text
Knowledge成立Regime
= High Volatility

Current Regime
= Low Volatility
```

など。

重要:

```text
NOT_APPLICABLE
≠ RETIRED
```

Knowledge自体が間違っているのではなく、

> **今の市場では使わない**

という意味。

---

# 20. UNCERTAIN

Applicability判定に必要なContextが不足・矛盾している状態。

例:

```text
Market DNA一部欠損
Quality低下
Freshness問題
Knowledge条件が曖昧
Current Market UnderstandingがUNCERTAIN
```

重要:

> **分からない場合は、無理にApplicableへ昇格しない。**

---

# 21. BLOCKED_BY_CONSTRAINT

成立条件に近くても、明示Constraintに該当する場合。

例:

```text
Knowledge:
High Leverage + Weak Spotで成立しやすい

Constraint:
Major Macro Event直前は利用禁止
```

なら、

```text
Current Market Condition一致
+
Constraint違反
↓
BLOCKED_BY_CONSTRAINT
```

になり得る。

---

# 22. Failure Boundary Check

Applicabilityでは成功条件だけを見ない。

必ず、

```text
Failure Boundary
```

を確認する。

重要:

> **成功条件を見るだけでなく、どこから壊れるかを見る。**

Failure Boundary内に入っている場合、KnowledgeをCurrent Decision Materialとして通さない方向を取れる構造にする。

---

# 23. Constraint Check

Failure BoundaryとConstraintを分ける。

```text
Failure Boundary
= Knowledgeが実際に壊れやすい研究上の境界

Constraint
= 安全・運用・研究上、利用を禁止 / 制限する条件
```

例:

```text
Failure Boundary:
Deep Liquidity

Constraint:
Data Quality INVALID時は利用禁止
```

---

# 24. Evidence Profile

KnowledgeのEvidenceを一つの万能Scoreへ潰さない。

最低限、

```text
Historical Evidence
OOS Evidence
Forward Evidence
Stress Evidence
Production / Live Evidence
```

を区別可能にする。

04はEvidenceを再Researchしない。

04の責任は、既存Knowledgeに付随するEvidence ContextをApplicability判断材料として参照すること。

---

# 25. Evidence StrengthとApplicabilityを分離する

重要:

```text
Evidenceが強い
≠ Current MarketでApplicable
```

Historical / OOS / Forwardで強いKnowledgeでも、Current Regimeが成立条件外なら `NOT_APPLICABLE` になり得る。

逆にCurrent条件が似ていても、EvidenceやValidation Ageに問題があれば `UNCERTAIN` 等になり得る。

---

# 26. Knowledge Recency / Validation Age

Knowledgeにも時間的Contextを持たせる。

候補:

```text
Research Date
Last Validation
Last Forward Evidence
Last Production Evidence
Knowledge Version
```

市場構造変化により、過去に強かったKnowledgeが現在も同じとは限らない。

ただし具体的なDecay Formulaや期限Thresholdはここで固定しない。

`Data Freshness` と `Knowledge Validation Age` を同一概念へ潰さない。

---

# 27. Regime Stability

Knowledgeが、

```text
特定Regimeのみ成立
複数Regimeで成立
Regimeに弱く依存
Regime依存不明
```

等の研究結果を持つ場合、Current Regimeと照合する。

重要:

```text
SUPPORTED
≠ All Regime Applicable
```

---

# 28. Knowledge Conflict

複数Knowledgeが同時にApplicableになる可能性がある。

例:

```text
Knowledge A → Long方向を支持
Knowledge B → Long方向を支持
Knowledge C → Short方向を支持
Knowledge D → Trade回避条件を示す
```

04は、

```text
Long 2票
Short 1票
↓
Long
```

とはしない。

---

# 29. Knowledgeの独立性 / Overlap

複数Knowledgeが、

```text
同じEvidence
同じCause
同じResearch
同じMarket Event
```

から派生している可能性がある。

したがってKnowledge数を独立Evidence数として扱わない。

後段が認識できるよう、概念上、

```text
Shared Evidence
Shared Cause
Derived Relationship
Duplicate / Overlap
```

等のRelationship Contextを保持可能にする。

---

# 30. Conflict Resolutionは05へ残す

04は、

```text
どのKnowledgeがCurrent Marketで利用可能か
```

を判定する。

しかし、Applicableな複数Knowledgeをどう一つのTrade Thesisへまとめるかは `05_DECISION` の責任。

```text
04
= 選別・適用審査

05
= 統合・意思決定
```

とする。

---

# 31. Applicability Assessment

04は各Knowledgeについて、Applicability判定だけでなく、その理由を追跡可能にする。

概念上、

```text
Knowledge
Applicability State
Matched Conditions
Missing Conditions
Failure Boundary Status
Constraint Status
Contradictions
Evidence Context
Uncertainty
Relationship / Overlap Context
```

等を持つ `Applicability Assessment` を生成できる構造にする。

具体Object Schemaは後で決める。

---

# 32. Applicable Knowledge Set

04の主要Downstream Boundaryを、

```text
Applicable Knowledge Set
```

とする。

これは単なるKnowledge ID一覧ではない。

05がTrade Thesis構築時に、

```text
なぜ使えるのか
どの条件付きか
どんなContradictionがあるか
どのConstraintが近いか
Evidenceはどの身分か
```

を理解できる情報を伴う。

---

# 33. Excluded / Blocked KnowledgeもTraceとして残す

`Applicable Knowledge Set` へ通らなかったKnowledgeを消さない。

概念上、別途Applicability Traceとして、

```text
NOT_APPLICABLE
UNCERTAIN
BLOCKED_BY_CONSTRAINT
NOT_EVALUATED
```

と、その理由を追跡可能にする。

目的:

> **なぜこのKnowledgeを今回使わなかったか後から説明できること。**

04のDownstream本流はApplicable Knowledge Setだが、除外理由もTrace / Post-Decision / Research Feedbackで利用できるようにする。

---

# 34. Current Market Evidenceの扱い

Current Runtime Observationは既存KnowledgeのApplicability判定に使用できる。

しかし、

```text
Current Observation
↓
新Knowledgeへ即昇格
```

にはしない。

新しい矛盾や異常が見つかった場合は、Research Candidateとして03の共通入口へ戻す。

---

# 35. Applicability Contradiction → Research

例えば、過去のKnowledgeではApplicableのはずなのに、Current Marketで明らかに成立しない状況が繰り返される場合。

04自身がKnowledgeを書き換えない。

```text
Applicability Contradiction
↓
Research Candidate
↓
03_RESEARCH / Research Intake
```

へ戻す。

重要:

```text
04 Feedback
≠ Research直接実行
```

03の共通Research入口を守る。

---

# 36. RuntimeでKnowledgeを直接更新しない

04が一回のRuntime結果だけを見て、

```text
このKnowledgeはダメ
↓
RETIRED
```

と即変更しない。

正しい方向:

```text
Contradiction / Failure
↓
Research Candidate
↓
03_RESEARCH
↓
Validation
↓
Validated Research Result
↓
Knowledge Maintenance Path
```

とする。

---

# 37. AIの役割

AIは04で補助的に利用できる。

候補:

```text
Knowledge検索補助
条件比較
Contradiction説明
Applicability理由説明
Knowledge間Relationship整理
Text Knowledge解釈
人間向け説明
```

ただし、

```text
AIが似ていると言った
=
Applicable
```

にはしない。

AI Outputは主に `ADVISORY / INTERPRETATION` として扱う。

---

# 38. Python / RuleとAI

概念上、

```text
Python / Rule
= 明示条件照合
  Market DNA比較
  Constraint Check
  Version Check
  Evidence Metadata処理
  Reproducible Matching

AI
= 文脈理解
  Text Knowledge解釈
  Contradiction説明
  Alternative Context提示
```

とする。

Hard Constraintや明示ConditionをAI判断だけで無効化しない。

---

# 39. Failure Path

04自身にもFailureがある。

例:

```text
Knowledge Pool unavailable
Knowledge Version不明
Current Market DNA不足
Current Market Understanding不明
Quality不足
Knowledge Condition欠損
Applicability評価不能
Conflicting Metadata
Stale / Old Validation
```

その場合、無理にApplicableへ通さない。

```text
UNCERTAIN
NOT_EVALUATED
BLOCKED
```

等を表現できる構造を持つ。

正式State名は後で決める。

---

# 40. Productionとの依存関係

Production RuntimeがResearchへ同期依存しないことを明示する。

```text
Research / Knowledge Maintenance
        ↓ ASYNC / OFFLINE寄り
Knowledge Pool
        │
        │
Current Market ────────┐
        │               │
        └───────┬───────┘
                ↓
      Runtime Applicability
                ↓
      Applicable Knowledge Set
                ↓
            05_DECISION
```

Production側は既にAdmissionされたKnowledgeをCurrent Marketへ適用する。

---

# 41. Connection Type

既存方針を維持する。

```text
DATA
REFERENCE
FEEDBACK
GATE
ADVISORY
```

例候補:

```text
Validated Research Result
→ Knowledge Admission
= DATA

Market DNA Snapshot
→ Applicability
= REFERENCE

Current Market Understanding
→ Applicability
= REFERENCE

Constraint
→ Applicability
= GATE

Applicability Contradiction
→ Research Candidate
= FEEDBACK

AI Review
→ Applicability
= ADVISORY
```

正式割当はMaster統合時に確認する。

---

# 42. Dependency Strength

Connection Typeとは別に、

```text
HARD
SOFT
OPTIONAL
ASYNC
```

を保持可能にする。

例候補:

```text
Knowledge Pool
→ Runtime Applicability
= HARD

Current Market State
→ Runtime Applicability
= HARD

Market DNA Snapshot
→ Applicability
= Knowledge種別により HARD / SOFT候補

AI Review
→ Applicability
= OPTIONAL

Applicability Feedback
→ Research
= ASYNC

03 Research Completion
→ Current Runtime Applicability
= 非同期。Runtimeの毎回HARD依存にはしない
```

具体割当はMaster統合時に確定する。

---

# 43. Upstream Boundary Summary

Knowledge Maintenance Path:

```text
03_RESEARCH
↓
Validated Research Result
```

Runtime Current Market Reference:

```text
02_MARKET_UNDERSTANDING
├─ Current Market Understanding
└─ Market DNA Snapshot
```

Cross-Cutting Context候補:

```text
Quality
Freshness
Version
Trace / Provenance
Time / Cycle
```

---

# 44. Internal Boundary Summary

Knowledge Maintenance Path:

```text
Validated Research Result
↓
Knowledge Admission / Promotion
↓
Knowledge Record / Knowledge Pool
```

Runtime Applicability Path:

```text
Knowledge Pool
+
Current Market Context
↓
Eligibility / Status Check
↓
Current Market Matching
↓
Failure Boundary Check
↓
Constraint Check
↓
Evidence / Version / Validation Age Context
↓
Applicability Evaluation
↓
Applicability Assessment
↓
Applicable Knowledge Set
```

---

# 45. Downstream Boundary Summary

主要Downstream Boundary:

```text
Applicable Knowledge Set
```

Next Map:

```text
05_DECISION
```

05はこのOutputを利用して、

```text
Trade Thesis
↓
Expected Value Evaluation
↓
Signal Decision
```

等へ進む。

---

# 46. 03との境界

03の責任:

```text
Research Candidate
↓
Hypothesis / Research Plan
↓
Validation
↓
Validated Research Result
```

04の責任:

```text
Validated Research Result
↓
Knowledge Admission / Maintenance
↓
Knowledge Pool
↓
Current Market Applicability
↓
Applicable Knowledge Set
```

簡単に言えば、

```text
03 = 知識を作る研究
04 = 知識を現在に適用するための審査
05 = 適用可能Knowledgeから意思決定
```

---

# 47. 02との境界

02:

```text
現在市場を理解する
↓
Current Market Understanding
Market DNA Snapshot
```

04:

```text
そのCurrent Market Contextを使って
既存Knowledgeが今利用可能か確認する
```

02自身がKnowledgeを選ばない。

04自身がMarket Understanding / DNAを作り直さない。

---

# 48. 05との境界

04:

```text
これは今使ってよいKnowledge
```

まで。

05:

```text
このKnowledge群を
どうTrade Thesisへ統合するか
```

を担当する。

重要:

```text
04 Applicability
≠ 05 Decision
```

---

# 49. このMapが保証すること

Working Baselineとして最低限、以下を保証する。

```text
Research ResultとKnowledgeを分離
KnowledgeとApplicable Knowledgeを分離
Applicable KnowledgeとTrade判断を分離
Knowledge MaintenanceとRuntime Applicabilityを分離
Production RuntimeをResearchへ同期依存させない
Positive / Failure / Constraint / Unknown等のKnowledgeを保持可能
Knowledgeを条件付き知識として扱える
Market DNA SnapshotをCurrent Contextとして利用可能
Current Market UnderstandingのInterpretation身分を保持
ApplicabilityをTRUE / FALSEだけに潰さない
Failure Boundaryを確認
Constraintを確認
Evidence StrengthとApplicabilityを分離
Knowledge Version / Validation Ageを考慮可能
Knowledge多数決をしない
Shared Evidence / Overlapを認識可能
Conflict統合は05へ残す
除外Knowledgeの理由をTrace可能
Applicability ContradictionをResearch Candidateへ戻せる
RuntimeでKnowledgeを直接書き換えない
Applicable Knowledge Setを05へ渡せる
```

---

# 50. このMapで決めないこと

この段階では以下を最終固定しない。

```text
Knowledge DB Schema
Knowledge Object全Field
Knowledge Promotion詳細Rule
Knowledge Lifecycle詳細State
Applicability Score
Similarity Formula
Market DNA Distance Formula
Confidence Formula
Knowledge Decay Formula
具体Threshold
Conflict Resolution Formula
Knowledge Ranking Formula
Trade Thesis生成Rule
Expected Value
Signal
Risk
Execution
AI Prompt
Python Class
DB Table
```

これらはDetailed Design / Contract / Implementation Specで扱う。

---

# 51. v0.1 Failure Reviewとの対応

このMapで直接扱う主要MUST FIX:

```text
MUST FIX 01
Current Market DNAをResearch経由に限定しない
→ Market DNA Snapshotを02からRuntime Applicabilityへ直接参照

MUST FIX 05
Evidence Role / Source分離
→ Research EvidenceとRuntime Contextを混同しない

MUST FIX 07
Research共通入口
→ Applicability FeedbackはResearch Candidateとして03へ戻す

MUST FIX 08
Post-Decision / RuntimeからKnowledge直接更新禁止
→ 04 Runtimeでも直接Knowledgeを書き換えない

MUST FIX 09
Dependency Strength
→ HARD / SOFT / OPTIONAL / ASYNCを保持

MUST FIX 10
Time / Cycle / Freshness
→ Current Market ContextとKnowledge Validation Ageを区別して参照

MUST FIX 11
AI Outputの身分
→ AIはADVISORY / INTERPRETATION

MUST FIX 13
Market DNA Definition / Snapshot分離
→ RuntimeではMarket DNA Snapshotを参照
```

---

# 52. Completion Gate

`04_KNOWLEDGE_APPLICABILITY` をWorking Baselineとする最低条件:

```text
□ Upstreamが Validated Research Result と一致
□ Current Market Understandingを参照可能
□ Market DNA Snapshotを参照可能
□ Knowledge Maintenance PathとRuntime Applicability Pathを分離
□ Knowledge AdmissionがProduction Approvalを意味しない
□ Knowledge Poolの論理役割が明確
□ Knowledge ≠ Applicable Knowledge
□ Applicable Knowledge ≠ Trade
□ Failure Boundaryを確認
□ Constraintを確認
□ Evidence Profileを保持
□ Knowledge Version / Validation Ageを考慮可能
□ UNKNOWN / PARTIALを許容
□ Knowledge多数決をしない
□ Shared Evidence / Overlapを考慮可能
□ Conflict Resolutionを05へ残す
□ Excluded Knowledgeの理由をTrace可能
□ Applicability ContradictionをResearch Candidateへ戻せる
□ RuntimeでKnowledgeを直接書き換えない
□ Production RuntimeをResearchへ同期依存させない
□ Applicable Knowledge Setを05へ渡せる
□ Detailed Designへ踏み込みすぎていない
```

---

# 一文定義

> **04_KNOWLEDGE_APPLICABILITYとは、`03_RESEARCH` から得られた `Validated Research Result` を非同期のKnowledge Maintenance Pathで再利用可能な条件付きKnowledgeとして整理・保持し、Runtimeでは `02_MARKET_UNDERSTANDING` のCurrent Market Understanding・Market DNA Snapshot・Quality / Freshness等の現在市場Contextと照合し、成立条件・Failure Boundary・Constraint・Evidence・Version・Validation Age・Uncertaintyを確認した上で、「今この市場で意思決定材料として利用可能なKnowledge」だけを `Applicable Knowledge Set` として `05_DECISION` へ渡すKnowledge適用フィルターConnection Mapである。**