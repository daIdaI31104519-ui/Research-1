# 市場理解OS HUMAN MAP — Part 1 v0.3

**Status:** DRAFT / NOT CANONICAL  
**目的:** 市場理解OS全体を、人間が短時間で理解できる形にする。

---

# 0. この文書の役割

この文書は、市場理解OSの詳細仕様書ではない。

ここで決めるのは、

> **市場理解OSとは何をするシステムなのか**

という全体思想である。

この段階では、

- Python Class
- Function
- DB Schema
- Object ID
- 詳細State
- API仕様
- 数式
- Threshold

までは固定しない。

まず人間が、

```text
何を作る？
なぜ作る？
どう市場を見る？
どう研究する？
どうKnowledgeを使う？
どうTradeする？
どう失敗から戻る？
AIは何をする？
```

を説明できることを優先する。

---

# 1. 市場理解OSとは何か

市場理解OSは、

> **市場を多方向から観測し、現在何が起きているかを理解し、原因候補や市場状態を研究し、過去の研究Knowledgeから現在使えるものを選び、期待値とRiskを別々に確認した上で、Tradeするか・見送るかを判断し、その結果を再び研究へ戻す循環型システム**

である。

単純な、

```text
Data
↓
AI
↓
BUY / SELL
```

を目的にはしない。

目指すのは、

```text
観測
↓
理解
↓
研究
↓
Knowledge
↓
現在への適用
↓
判断
↓
安全確認
↓
実行
↓
分析
↓
再研究
```

という循環である。

最終結果には、

```text
TRADE
WAIT
REDUCE
NO TRADE
```

が存在する。

**取引しないことも正常な判断である。**

---

# 2. 最上位思想

市場理解OSの基本思想は、

> **予測より理解**

である。

市場の未来を完全に予測することはできない。

市場には、

- 戦争
- 災害
- Regulation
- ハッキング
- Exchange障害
- 大口資金移動
- ETF等による市場構造変化
- 未知の参加者行動
- 観測できない要因

が存在する。

したがって、

```text
未来を当て続ける
```

ことより、

```text
変化を観測する
↓
今までの理解を疑う
↓
必要なら再研究する
↓
Knowledgeを更新する
↓
新しい市場へ適応する
```

能力を重視する。

また、

```text
勝率
```

だけを最大化しない。

重視するのは、

```text
Expected Value
+
Risk
+
不確実性
+
適用条件
+
長期生存
```

である。

> **利益を増やす前に、生き残れる構造を作る。**

---

# 3. 市場をどう理解するか

市場理解では、

```text
何が起きている？
```

と、

```text
なぜ起きている？
```

を分ける。

大きく、

```text
市場観測
↓
市場理解
↓
原因候補
↓
研究
```

と考える。

## 市場観測

事実を集める。

例:

```text
Price
Volume
OI
Funding
Liquidation
Orderbook
Liquidity
ETF
Whale
Macro
News
On-chain
```

この段階で原因を決めない。

## 市場理解

複数の観測結果から、

> **現在市場で何が起きている可能性が高いか**

を整理する。

例えば、

```text
Price上昇
+
OI急増
+
Funding上昇
+
Spot CVD低下
```

なら、

「単純な強い現物買い」とは違う可能性がある。

## 原因候補

その現象について、

```text
ETF Flow?
Short Squeeze?
新規Long?
Macro?
Whale?
Liquidity Vacuum?
```

など複数候補を作る。

しかし、

```text
同時に起きた
=
原因
```

とはしない。

原因候補はResearch対象になる。

---

# 4. 仮説・因果・Edgeをどう扱うか

市場理解OSは、単一Hypothesisを永久に信用しない。

また、

> **因果を完全に説明できるものだけ**

に限定もしない。

研究対象には大きく、

```text
Causal Edge
= なぜ起きるかMechanismを説明できる優位性

Empirical Edge
= 原因説明が完全でなくても
  再現可能な期待値が確認された優位性
```

が存在できる。

重要なのは、

```text
因果説明が綺麗
≠
利益が出る

因果説明が不完全
≠
期待値が存在しない
```

ということ。

## 市場に合わせてHypothesisを書き換えない

市場が変われば、

> **現在使うHypothesisの組み合わせ**

は変えてよい。

しかし、

```text
現在市場に都合がいいように
Hypothesisそのものを変更
```

してはいけない。

Hypothesis自体を変更する場合は、

```text
変更
↓
新Version
↓
Research
↓
再検証
```

へ戻す。

## 複数Hypothesisを多数決しない

例えば、

```text
BUY Hypothesis 3
SELL Hypothesis 2
```

だからBUY、とはしない。

見るのは、

- 独立したEvidenceか
- 同じEvidenceを重複評価していないか
- 同じCauseから派生していないか
- 現在市場に適用できるか
- 反対Hypothesisは何か
- どの条件で壊れるか

である。

## Trade Thesis

現在市場で利用可能な研究済みHypothesisを組み合わせ、

> **現在市場に対する一つの取引論拠**

を作る。

これを、

**取引根拠（Trade Thesis）**

と呼ぶ。

Trade Thesisには、

```text
中心となる考え
支持する考え
成立条件
反対材料
失敗条件
期待するEffect
```

が含まれる。

Entry後に都合よく理由を差し替えない。

---

# 5. 市場DNA（Market DNA）の役割

市場DNAは、

> **現在市場を、過去市場と比較可能な形で表現する市場状態表現**

である。

重要な境界は、

```text
Market DNA
≠ BUY / SELL Signal

Market DNA
≠ Hypothesis Evaluator

Market DNA
≠ 未来予測
```

である。

Market DNA自身が、

「このHypothesisは儲かる」

と決めるわけではない。

市場DNAの役割は、

```text
今はどのような市場状態か？
```

を表すこと。

そのMarket DNAを使って、

```text
Research
Knowledge
Production
```

側が、

- 過去のどの市場と似るか
- どのKnowledgeが使えたか
- どこで失敗したか
- 現在何が適用可能か

を調べる。

---

# 6. 市場理解OSは2つの大きなLoopを持つ

市場理解OSを一本の巨大Pipelineとして考えない。

大きく、

```text
Research Loop
```

と、

```text
Production Loop
```

に分ける。

## 6.1 Research Loop

Researchは大きくてよい。

目的は、

> **新しい市場理解と再利用可能なKnowledgeを作ること。**

概念的には、

```text
市場観測
↓
市場理解
↓
原因候補 / Research Candidate
↓
Hypothesis
↓
Market DNA / 過去Case
↓
Historical / OOS / Forward / Stress等
↓
反証
↓
失敗条件
↓
Knowledge
↓
Knowledge Pool
```

となる。

Researchでは大量の探索・比較・失敗を許す。

## 6.2 Production Loop

Productionは小さく慎重にする。

目的は、

> **すでに研究済みのKnowledgeから、現在市場に利用可能なものだけを使って実資金判断を行うこと。**

概念的には、

```text
現在市場
↓
Current Market State / Market DNA
↓
研究済みKnowledgeを参照
↓
現在使えるHypothesisを選択
↓
Trade Thesis
↓
Expected Value
↓
Safety / Risk
↓
TRADE / WAIT / REDUCE / NO TRADE
↓
Execution
```

となる。

Productionは毎回巨大Researchを実行してからTradeする必要はない。

## 6.3 2つのLoopの関係

```text
       ┌──────────────────┐
       │   Research Loop   │
       │    大きな研究所    │
       └────────┬─────────┘
                │
             Knowledge
                │
                ▼
       ┌──────────────────┐
市場 → │ Production Loop  │ → Trade
       │   小さな本番機     │
       └────────┬─────────┘
                │
           Trade Result
                │
                ▼
          Post-Trade
                │
                └────→ Research
```

一言で言えば、

> **巨大な研究所、小さな本番取引機。**

---

# 7. Expected ValueとRiskを分ける

Expected ValueとRiskは同じ判断ではない。

## Expected Value

問い:

> **このTrade候補には、期待収益性が存在するか？**

## Risk / Defense

問い:

> **期待収益性が存在しても、今この状況で実際にRiskを取ってよいか？**

例えば、

```text
Expected Value
= Positive

しかし

Data Quality低下
Exchange障害
Liquidity急減
DD Limit超過
異常Event
```

なら、

```text
NO TRADE
```

になり得る。

つまり、

> **Positive Expected Value ≠ Trade Permission**

である。

また、

```text
Expected Value
Data Quality
Applicability
Constraint
Uncertainty
Risk
```

を全部一つの万能Scoreへ潰さない。

それぞれ役割が違う。

---

# 8. 証拠とKnowledgeをどう考えるか

Researchでは、

```text
Historical
OOS
Forward
Stress
Live
```

など異なるEvidenceを使う。

これらは意味が違うため、

```text
全部足して
総件数
総勝率
```

とは扱わない。

重要なのは、

> **どこから得られたEvidenceなのかを残すこと。**

またKnowledgeには成功だけを残さない。

```text
成功条件
失敗条件
Failure Boundary
Constraint
矛盾
UNKNOWN
使えなかったCase
```

もKnowledgeになる。

> **失敗も研究成果である。**

---

# 9. Trade後に何を学ぶか

市場理解OSは、

```text
WIN
LOSS
```

だけで評価しない。

重要原則は、

```text
Trade Outcome
≠ Hypothesis Outcome
≠ Trade Thesis Outcome
≠ Execution Outcome
≠ Risk Outcome
```

である。

例えば、

```text
Hypothesisは間違っていた
↓
別要因で利益
↓
WIN
```

もあり得る。

逆に、

```text
Trade Thesisは妥当
↓
Execution failure
↓
LOSS
```

もあり得る。

そのためPost-Tradeでは、

> **どこから成功・失敗が始まったのか**

を分析する。

分析結果は、

```text
Research Candidate
```

として適切なResearchへ戻す。

## Tradeしなかった判断も研究する

研究対象は実行したTradeだけではない。

```text
NO TRADE
WAIT
Defense Block
Missed Opportunity
Unexpected Success
Unexpected Failure
```

なども研究対象にする。

例えば、

> 「Defenseが止めたTradeは、本当に止めて正しかったか？」

も後から検証できる。

---

# 10. AIは何のために使うのか

AIを市場理解OSの必須計算Layerにはしない。

基本分担は、

```text
Python / Rule
= 測る・計算する・守る・実行する

AI
= 解釈する・疑う・仮説を作る・査読する・説明する
```

である。

AIは特に、

## Market Intelligence

```text
大量Data
↓
現在何が起きている可能性があるか整理
```

## Causal / Hypothesis

```text
原因候補
Alternative Hypothesis
Contradiction
Confounder候補
```

## Research

```text
研究案
反証方法
Stress案
見落とし候補
```

## Production Review

```text
Trade Thesisの弱点
Evidence重複
反対Hypothesis
見落とし
```

## Post-Trade

```text
失敗原因候補
Attribution候補
新しいResearch Candidate
```

## Human Explanation

```text
複雑な内部状態
↓
人間向け日本語
```

に利用できる。

## AIのAuthority

AIは、

> **研究者・査読者・説明者**

として利用する。

しかし、

```text
AIが勝手に
Production Ruleを変更
Risk Limitを変更
未検証HypothesisをLiveへ追加
Codeを書き換えて即本番反映
```

する構造にはしない。

自動Tradeそのものを禁止するわけではない。

事前に定義されたRule・Governance・Risk範囲内でProductionを自動運用することは可能である。

また、

> **AI停止 = OS全体崩壊**

にならない構造を目指す。

---

# 11. 長期的に何を残すのか

市場理解OSは長期間改善されることを前提にする。

そのため、

```text
Code
Formula
Feature
AI Model
API
Source
Data Format
```

は将来変更できる。

しかし、

```text
何を観測したか
何を研究したか
何を根拠に判断したか
何が失敗したか
どのKnowledgeを使用したか
なぜTradeしたか
なぜTradeしなかったか
```

という研究履歴は重要な資産になる。

ただし、

```text
全Raw Dataを永久保存する
```

という意味ではない。

目的は、

> **後から研究・再現・検証・説明できるために必要なEvidenceと履歴を維持すること。**

である。

## 判断は後から追えるようにする

人間が後から、

```text
どんな市場だった？
↓
何を理解した？
↓
何のKnowledgeを使った？
↓
なぜそのTrade Thesisになった？
↓
なぜTrade / No Tradeになった？
↓
結果はどうだった？
↓
何を再研究した？
```

を追えることを重視する。

詳細なTrace構造やObject順序は、このHuman Mapでは固定しない。

---

# 12. 市場理解OS全体像

市場理解OS全体を最も簡単に表す。

```text
━━━━━━━━━━━━━━━━━━━━━━━━━━
市場
━━━━━━━━━━━━━━━━━━━━━━━━━━
        │
        ▼
観測・Data Quality
        │
        ▼
市場理解
        │
        ├──────────────┐
        │              │
        ▼              ▼
原因候補           Market DNA
        │              │
        └──────┬───────┘
               ▼
━━━━━━━━━━━━━━━━━━━━━━━━━━
Research Loop
━━━━━━━━━━━━━━━━━━━━━━━━━━
Hypothesis
↓
検証
↓
反証
↓
失敗条件
↓
Knowledge
━━━━━━━━━━━━━━━━━━━━━━━━━━
               │
               ▼
━━━━━━━━━━━━━━━━━━━━━━━━━━
Production Loop
━━━━━━━━━━━━━━━━━━━━━━━━━━
現在市場
+
研究済みKnowledge
↓
現在使えるHypothesis
↓
Trade Thesis
↓
Expected Value
↓
Risk / Defense
↓
TRADE / WAIT / REDUCE / NO TRADE
↓
Execution
━━━━━━━━━━━━━━━━━━━━━━━━━━
               │
               ▼
Post-Trade Analysis
               │
               ├→ Knowledge評価
               ├→ Hypothesis評価
               ├→ Production評価
               └→ Research Candidate
                        │
                        └────→ Research Loop
```

その全体を横方向から、

```text
AI Assistance
Data Quality
Storage
Trace / Provenance
Version
Security
Monitoring
Failure / Recovery
Governance
```

などが支える。

これらは別々の市場分析Layerではなく、

> **複数領域を横断して支える共通機能**

として考える。

---

# 13. 市場理解OSが避けること

市場理解OSでは、基本的に次を避ける。

```text
未来予測だけに依存する

単一指標でTradeする

単一Hypothesisを永久に信用する

Hypothesis数の多数決をする

同じEvidenceを二重評価する

現在市場に都合よくHypothesisを書き換える

Entry後に理由を後付けする

Market DNAを直接Signal化する

Research結果を即Liveへ反映する

Historical / Forward / Liveを同じEvidenceとして混ぜる

WINを正しさの証明と考える

LOSSだけでModelを再学習する

全部を一つの万能Scoreへ潰す

AIへ無制限Authorityを与える

分からない状態を無理にBUY / SELLへ変える

常にTradeしようとする
```

---

# 14. Part 1 v0.3の中心思想

市場理解OSとは、

> **市場を当てる機械ではなく、市場を観測し、理解し、疑い、研究し、Knowledgeを蓄積し、現在市場に適用可能な研究済み知識から取引根拠を作り、期待値とRiskを分離して判断し、その結果を再び研究へ戻し続けるシステム**

である。

中心思想を短くまとめると、

```text
予測より理解

理解したつもりにならない

因果だけにも依存しない

研究済みHypothesisを現在市場に適用する

Hypothesisを都合よく書き換えない

複数Hypothesisを多数決しない

反対材料を消さない

Expected ValueとTrade Permissionを分ける

Researchは大きく
Productionは小さく

成功だけでなく失敗もKnowledgeにする

Tradeしなかった判断も研究する

WIN ≠ 正しい理解
LOSS ≠ 間違った理解

AIは考える補助として使う
Hard Ruleの代わりにはしない

Codeは変えられる
研究履歴は失わない

市場が変われば再研究する
```

そして最も重要なのは、

> **市場理解OS自身が、自分の理解・仮説・Knowledge・判断を疑い、必要なら再研究できる構造を持つこと。**

---

# Part 1 v0.3 一文定義

> **市場理解OSとは、巨大なResearch Loopで市場理解とKnowledgeを育て、小さく慎重なProduction Loopが現在市場に適用可能な研究済みKnowledgeだけを利用し、複数HypothesisからTrade Thesisを構築し、Expected ValueとRiskを分けて判断し、その結果を再びResearchへ返して適応し続ける市場研究・意思決定システムである。**
