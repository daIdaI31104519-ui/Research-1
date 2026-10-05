# TEMP — PROJECT CHARTER RECONCILIATION PLAN v0.5

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
Current Crypto Scope / Future Expansion
Research Publication / User Value / Future Business Opportunity
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
10. Current Market Scope / Future Expansion
    - Current Scope = 仮想通貨FX + 仮想通貨現物
    - Crypto First
    - 株式 / 通常FX / その他市場は現在の完成条件に含めない
    - Future Expansion Readyだが、将来対応を理由に現在設計を複雑化しない
11. Research成果の利用先
    - Automated Trading
    - Human-readable Research Publication
    - 無料Application / Interface等による人間への還元方向
    - 具体的収益化方法は現時点で固定しない
12. AI / Human / Production Authority
13. 変えてよいもの / 変えてはいけないもの
14. Charter変更時のGovernance
```

具体DB Schema、Python Class、API、Threshold、Risk数値はここで固定しない。

現在進捗:

```text
Section 1 Project Mission
= DRAFT / LEADING CANDIDATE 保存済み

Section 2 Success Definition
= DRAFT / LEADING CANDIDATE 保存済み

Section 3 What Not To Maximize
= DRAFT / LEADING CANDIDATE 保存済み

Section 4 Survival / Profit Priority
= DRAFT / LEADING CANDIDATE 保存済み

Section 5 Research Mission
= DRAFT / LEADING CANDIDATE 保存済み

Section 6 Research Category Philosophy
= DRAFT / LEADING CANDIDATE 保存済み

Section 7 Capital / Risk Philosophy
= DRAFT / LEADING CANDIDATE 保存済み

Current Focus
= 8. Knowledge / Data Asset Philosophy
```

---

# 5. Research Missionの現在方向

Section 5はDRAFT / LEADING CANDIDATEとして保存済み。

中心思想:

~~~text
Research
!= Research Count Maximization
!= Hypothesis Confirmation Factory
!= Production Permission

Research
= Reusable Understanding / Evidence / Failure / Unknown Creation
~~~

Primary Research Mission Families:

~~~text
RM-1 FOUNDATIONAL / MECHANISM RESEARCH
RM-2 SURVIVAL / FAILURE RESEARCH
RM-3 ECONOMIC EDGE RESEARCH
RM-4 ADAPTATION / REVALIDATION RESEARCH
RM-5 DECISION / EXECUTION QUALITY RESEARCH
~~~

Cross-Cutting:

~~~text
Research Integrity / Methodology
= 全Research Missionへ適用
~~~

Boundary:

~~~text
Validated Research Result
!= Knowledge
!= Production Authority

Research Candidate Source
!= Research Mission

Research Mission
!= Intake Disposition
!= Priority
!= Validation Method
!= Research Result
~~~

Human-readable Research PublicationはPrimary Research MissionではなくDownstream Consumer / Output Routeとして扱う。

CORE EDGE / OPPORTUNITY / Adaptationの詳細研究思想はSection 6 Research Category Philosophyとして保存済み。



---

# 6. Research Category Philosophyの現在方向

Section 6はDRAFT / LEADING CANDIDATEとして保存済み。

中心構造:

~~~text
CORE EDGE / OPPORTUNITY
= Economic Edge Character

ADAPTATION / REVALIDATION
= Cross-Temporal Research Philosophy
~~~

CORE EDGE:

~~~text
Repeated Profit
!= CORE

CORE
!= Universal
!= Permanent
!= Always Applicable
~~~

CORE Researchは、成功条件だけでなくCounter-Evidence・Weak Condition・Failure Boundaryを含めて再利用可能性を研究する。

OPPORTUNITY:

~~~text
Rare
!= Opportunity

Volatile
!= Opportunity

Large Move
!= Opportunity

Large Potential Profit
!= Opportunity

Unknown
!= Opportunity
~~~

Opportunityは一時的Distortion / Imbalance / Event / Market Structure等へEconomic Valueが依存するEdge Characterとして研究する。

Boundary:

~~~text
Opportunity Research Result
!= Opportunity Mode Permission
!= Trade Permission
!= Capital Permission
~~~

Edge Characterが未解決である状態を許容し、CORE / OPPORTUNITYへ強制分類しない。

Adaptation / Revalidation:

~~~text
Unexpected Outcome
!= Edge Decay

Regime / Applicability Mismatch
!= Knowledge Failure

Edge Decay
!= Structural Break

Temporary Shock
!= Structural Break
~~~

Adaptation TriggerとAdaptation Conclusionを分離し、Data / Decision / Defense / Execution Failure等をEdge Failureへ誤変換しない。

Authority Boundary:

~~~text
CORE / OPPORTUNITY
= Edge Character

Knowledge Lifecycle
= separate authority

Current Applicability
= separate authority

Capital / Risk Permission
= Section 7以降
~~~

Historical Research Truthを保存し、Later Decay / Structural Breakによって過去の成立条件下で支持されていたResearch Historyを消さない。


---

# 7. Capital / Risk Philosophyの現在方向

Section 7はDRAFT / LEADING CANDIDATEとして保存済み。

中心構造:

~~~text
Hard Survival Boundary
= Project-level constitutional boundary

Risk Capacity Profile
= current multidimensional / scope-sensitive capacity

Risk Budget
= allocation of available capacity

Risk Posture
= CORE / OPPORTUNITY等のRisk treatment

Risk Envelope
= admissible risk conditions

Capital Permission
= current-use validなTrade Thesisに対するCapital / Exposure Riskの許可判断
~~~

重要境界:

~~~text
Capital != Risk
Risk Capacity != Capital Balance
Risk Capacity != Risk Budget
Risk Budget != Risk Envelope
Economic Edge Character != Risk Posture
Capital Permission != Execution Permission
~~~

Risk PostureはGlobal SwitchではなくScope-boundとし、複数Postureが共存してもShared Risk Capacityと同じHard Survival Boundaryの制約を受ける。

~~~text
CORE EDGE
!= CORE RISK POSTURE

OPPORTUNITY
!= OPPORTUNITY RISK POSTURE

OPPORTUNITY RISK POSTURE
!= Aggressive Mode
~~~

Risk PostureはRisk Capacityを作らず、Research / Knowledge / Applicability / Economic Value等の上流Truthを書き換えず、UNKNOWNをSAFEへ変換せず、Mode ShoppingによってRisk Ruleを回避しない。

Risk CapacityはCapital・Liquidity・Exposure・Venue・Operational Control・Recoverability・Material Unknown等を含む多面的状態として扱い、一つの万能Scoreへ潰さない。

Capacity ContractionはKnowledge / Edge Failureを意味せず、Existing Exposureに対するBlind Forced Liquidationも自動命令しない。

Recoveryは壊れたCapacity Dimensionに対応するEvidenceで確認し、

~~~text
Capacity Recovery
!= automatic Budget Restoration
!= Old Capital Permission Revival
!= Opportunity Recovery
~~~

とする。

Decision / Economic側とのBoundaryは、

~~~text
Decision / Economic Evaluation
↓
Trade Thesis
↓
Capital / Risk Authority
↓
Capital Permission
↓
Execution / Runtime Safety
~~~

を本命方向とする。

具体Risk数値、Capacity Formula、Budget Allocation Formula、Mode Entry / Exit Threshold、Risk Envelope Threshold、Capital Permission Contract等は後続Detailed Risk / Capital Architectureへ送る。

---

# 8. Knowledge / Data Asset Philosophyの現在方向

Current Focus。

Section 1〜7から詳細内容を自動確定しない。

次に、Knowledge / Dataを長期資産として扱う上位思想について、

~~~text
何を長期Assetとして残すか
Raw Data / Evidence / Research Result / Knowledgeの違い
Version / Lineage / Historyをどこまで守るか
再現・再検証・説明可能性
保存CostとInformation Value
Knowledge / Dataの更新・廃止・保持
~~~

等を、既存のResearch / Knowledge設計とAuthority重複しないようにPrecision-Firstで設計する。

具体Retention期間、DB Schema、Storage Engine、File Format、Compression、Cloud構成等はこの段階では固定しない。

---

# 9. 独自Data / 独自Metricの方向

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
Market Intelligence / Research / Publication
```

へ落とす。

---

# 10. 既存ファイルへの影響順位

```text
CURRENT DRAFT
00_HUMAN/PROJECT_CHARTER.md
= Section 1 Project Mission保存済み
= Section 2 Success Definition保存済み
= Section 3 What Not To Maximize保存済み
= Section 4 Survival / Profit Priority保存済み
= Section 5 Research Mission保存済み
= Section 6 Research Category Philosophy保存済み
= Section 7 Capital / Risk Philosophy保存済み
= 現在はSection 8 Knowledge / Data Asset Philosophyを設計する

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

# 11. Reconciliation順序

この順番を守る。

```text
STEP 1
PROJECT_CHARTER v0.1 Draft
- Section 1 Project Mission = 保存済み
- Section 2 Success Definition = 保存済み
- Section 3 What Not To Maximize = 保存済み
- Section 4 Survival / Profit Priority = 保存済み
- Section 5 Research Mission = 保存済み
- Section 6 Research Category Philosophy = 保存済み
- Section 7 Capital / Risk Philosophy = 保存済み
- Current = Section 8 Knowledge / Data Asset Philosophy

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
Knowledge Consumer / Publication分岐との責任境界確認

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

# 12. 修正原則

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

# 13. 今回やらないこと

Charter Reconciliation中に以下へ広げない。

```text
05_DECISION詳細設計
06_EXECUTION詳細設計
最終Risk数値
Capital Allocation数値
DB Schema
Python Class
Plugin実装
無料Applicationの具体UI / 機能一覧
ユーザー獲得施策
収益化方式の固定
全独自Indexの計算式
```

関連していても後続Taskへ残す。

---

# 14. 完了条件

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