# TEMP — PROJECT CHARTER RECONCILIATION PLAN v0.1

**Document Role:** Temporary Design Migration / Navigation Plan  
**Status:** TEMPORARY / ACTIVE UNTIL RECONCILIATION COMPLETE  
**Purpose:** PROJECT_CHARTER導入によって既存設計が混乱しないよう、上位思想の確定・影響確認・既存Working Baseline再照合・05_DECISIONへの復帰までの作業順序を一時的に固定する。  
**Delete Condition:** PROJECT_CHARTERがWorking Baselineとなり、HUMAN_MAP / AI_WORKFLOW / 01〜04の再照合と必要修正が完了し、AI_CONTEXTのCurrent Taskが05_DECISIONへ復帰した後に削除する。

---

# 0. このファイルの扱い

これは市場理解OSの恒久設計書ではない。

目的は、

> **PROJECT_CHARTER導入作業中に、人間とGPTが作業順・影響範囲・元の設計地点を見失わないための一時ナビゲーションを提供すること。**

このファイル自身をCanonical Designへ昇格させない。
作業完了後は削除する。

---

# 1. 導入前Checkpoint

PROJECT_CHARTER導入前の基準地点:

```text
Commit:
28ce25a7739e0baf2653269255b29a8567831014

State:
01_EXTERNAL_DATA              = WORKING BASELINE
02_MARKET_UNDERSTANDING       = WORKING BASELINE
03_RESEARCH                   = WORKING BASELINE
04_KNOWLEDGE_APPLICABILITY    = WORKING BASELINE
05_DECISION                   = NOT YET CREATED
```

この地点を「Charter導入前Baseline」として扱う。

---

# 2. なぜ一旦05_DECISIONを止めるか

05_DECISION設計直前に、以下の上位思想が現在の新Repoで十分に統合されていないことを確認した。

```text
Project Mission / Success Definition
Research Mission
Capital / Risk Philosophy
Knowledge / Data Asset Philosophy
Independent Data / Metric Extensibility
Market / Asset Portability
Research Product / Business Mission
Constitution Change Governance
```

これらを決めずに05以降へ進むと、Research / Knowledge / Decision / Riskが異なる目的関数へ向かう危険がある。

したがって、05を破棄するのではなく、一時停止して上位思想を先に整理する。

---

# 3. 新しい上位階層

基本Authority階層:

```text
00_HUMAN/PROJECT_CHARTER.md
        ↓
00_HUMAN/HUMAN_MAP.md
        ↓
02_ARCHITECTURE / CONNECTIONS
        ↓
CROSS_CUTTING / DETAILED DESIGN
        ↓
CONTRACT / PYTHON / TEST
```

原則:

```text
PROJECT_CHARTER
= WHY / 最上位目的・優先順位・変えてはいけない原則

HUMAN_MAP
= WHAT / 市場理解OS全体の人間向け構造

CONNECTION MAP
= RESPONSIBILITY / CONNECTION
```

下位設計がPROJECT_CHARTERと矛盾した場合、まず下位設計を再確認する。
下位設計に合わせるためだけにPROJECT_CHARTERを都合よく変更しない。
PROJECT_CHARTER自体を変更する場合は明示的な上位設計変更として扱う。

---

# 4. PROJECT_CHARTERで固める対象

最低限、以下を議論してWorking Baseline化する。

```text
1. 市場理解OSは何のために存在するか
2. 成功とは何か
3. 何を最大化しないか
4. 長期生存と利益の優先順位
5. Research Mission
6. Core Edge / Adaptation / Opportunityの研究思想
7. Capital / Risk Philosophy
8. Knowledge / Dataを長期資産として扱う思想
9. 独自Data / Derived Metric / Research Outputを追加・交換・Version変更可能にする思想
10. BTCは初期対象でありCore Conceptは市場一般とするか
11. Research成果の利用先
    - Automated Trading
    - Research Product / Intelligence Output
12. AI / Human / Production Authority
13. 変えてよいもの / 変えてはいけないもの
14. Charter変更時のGovernance
```

具体DB Schema、Python Class、API、Threshold、Risk数値はここで固定しない。

---

# 5. Research Missionの現在方向

現時点の議論方向:

```text
最上位:
長期生存を壊さず、市場変化へ適応しながら、
再現可能な正の期待値を積み上げるKnowledgeを増やす。
```

研究カテゴリ候補:

```text
SURVIVAL RESEARCH
= DD / Tail Risk / Failure / No-Trade / Constraint / 生存

CORE EDGE RESEARCH
= 派手さより再現性のある正の期待値を積み上げる

ADAPTATION RESEARCH
= Regime Shift / Edge Decay / Knowledge Failureを早期発見する

OPPORTUNITY RESEARCH
= 非対称な大Opportunityを限定Risk内で研究する

INTELLIGENCE / PRODUCT RESEARCH
= 研究成果をグラフ・独自Data・Scenario等として人間が利用可能にする
```

ただし商品都合でResearch Coreを歪めない。

```text
Research Core
        ├─→ Automated Trading
        └─→ Research Product / Intelligence
```

を基本方向とする。

---

# 6. Capital / Risk Philosophyの現在方向

基本思想候補:

```text
通常時
= 無理をせず、再現性のあるEdgeをコツコツ積み上げる

明確な非対称Opportunity
= Failure Boundaryと最大損失を把握した上で、限定Risk内で攻める
```

これは「普段は安全、時々無根拠にギャンブルする」という意味ではない。

```text
CORE MODE
+
OPPORTUNITY MODE
```

として後続Risk / Decision設計へ反映する方向。

具体Risk Budgetや数値は後で設計する。

---

# 7. 独自Data / 独自Metricの方向

上位思想として、

> **独自Data・Derived Metric・Research Outputは、Core OS全体を書き直さず、追加・交換・Version変更できる構造を目指す。**

例:

```text
Liquidation Pressure Index
ETF-BTC Misalignment Index
Leverage Fragility Index
Whale Divergence Index
Market DNA Similarity Index
```

ただしこの段階ではPlugin Class / Registry / JSON Schema / Python Interfaceは固定しない。

後のData Contract / Feature Contract / Python Architectureで、

```text
Custom Metric Definition
↓
Versioned Calculation
↓
Standard Output Contract
↓
Market Intelligence / Research / Product
```

へ落とす。

---

# 8. 既存ファイルへの影響順位

```text
NEW
00_HUMAN/PROJECT_CHARTER.md
= 最優先で作成

HIGH IMPACT
00_HUMAN/HUMAN_MAP.md
00_AI/AI_WORKFLOW.md
02_ARCHITECTURE/CONNECTIONS/03_RESEARCH.md
00_AI/AI_CONTEXT.md

MEDIUM IMPACT
02_ARCHITECTURE/CONNECTIONS/04_KNOWLEDGE_APPLICABILITY.md
README.md
01_HISTORY/DESIGN_CHANGE_LOG.md

LOW / REVIEW FIRST
02_ARCHITECTURE/CONNECTIONS/01_EXTERNAL_DATA.md
02_ARCHITECTURE/CONNECTIONS/02_MARKET_UNDERSTANDING.md

NOT YET CREATED
05_DECISION.md
06_EXECUTION_POST_DECISION.md
= Charter Reconciliation完了後に新規設計する
```

既存Working Baselineをゼロから作り直さない。
影響箇所のみ最小修正する。

---

# 9. Reconciliation順序

この順番を守る。

```text
STEP 1
PROJECT_CHARTER v0.1 Draft

STEP 2
PROJECT_CHARTER Cross Check
↓
Working Baseline化

STEP 3
HUMAN_MAP Reconciliation

STEP 4
AI_WORKFLOW Reconciliation

STEP 5
01_EXTERNAL_DATA Review

STEP 6
02_MARKET_UNDERSTANDING Review

STEP 7
03_RESEARCH Reconciliation
Research MissionをIntake / Prioritizationへ反映

STEP 8
04_KNOWLEDGE_APPLICABILITY Reconciliation
Knowledge Consumer / Product分岐との責任境界確認

STEP 9
DESIGN_CHANGE_LOGへ今回の上位設計補完を記録

STEP 10
全体Cross Check

STEP 11
AI_CONTEXT Current Taskを05_DECISIONへ戻す

STEP 12
このTEMPファイルを削除

STEP 13
05_DECISION設計を再開
```

---

# 10. 修正原則

既存設計は以下の順で扱う。

```text
KEEP
= Charterと整合 → 変更しない

CLARIFY
= 思想は整合するが目的説明不足 → 最小追記

ADJUST
= 一部責任が新Charterと不整合 → 必要箇所だけ修正

REDESIGN
= 上位思想と重大に衝突 → その領域だけ再設計
```

原則:

> **全文書き直しをDefaultにしない。**

Working Baselineは資産として維持し、Charter導入による差分だけ再照合する。

---

# 11. 今回やらないこと

Charter Reconciliation中に以下へ広げない。

```text
05_DECISION詳細設計
06_EXECUTION詳細設計
最終Risk数値
Capital Allocation数値
DB Schema
Python Class
Plugin実装
商品価格
販売サイト
API料金設計
全独自Indexの計算式
```

関連していても後続Taskへ残す。

---

# 12. 完了条件

以下がすべて満たされたら、このTEMPファイルを削除して05へ戻る。

```text
□ PROJECT_CHARTERがWorking Baseline
□ HUMAN_MAPがCharterと整合
□ AI_WORKFLOWがCharter Authorityを認識
□ 01_EXTERNAL_DATA再照合済み
□ 02_MARKET_UNDERSTANDING再照合済み
□ 03_RESEARCHへResearch Mission反映済み
□ 04_KNOWLEDGE_APPLICABILITY再照合済み
□ DESIGN_CHANGE_LOGへ変更理由記録済み
□ 01〜04のBoundaryが維持されている
□ 新しい重大矛盾がない
□ AI_CONTEXTが05_DECISIONへ復帰
```

その後:

```text
DELETE:
00_AI/TEMP_CHARTER_RECONCILIATION_PLAN.md
```

---

# 一文定義

> **TEMP_CHARTER_RECONCILIATION_PLANとは、PROJECT_CHARTERという最上位思想を市場理解OSへ安全に導入し、既存Working Baselineを壊さず必要箇所だけ再照合・修正した後、05_DECISION設計へ確実に復帰するための一時的な設計移行ナビゲーションである。**
