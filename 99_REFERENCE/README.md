# 市場理解OS — REFERENCE POLICY / LEGACY REVIEW GATE

**Document Role:** Legacy Knowledge Governance / Reference Router  
**Status:** REVIEWED / WORKING BASELINE  
**Current Design Authority:** NONE  
**Parent Workflow:** `00_AI/AI_WORKFLOW.md`  
**Purpose:** 旧市場理解OSの設計・定義・失敗・改善履歴を、Current Designへ混入させず、安全に比較・再利用するためのLegacy専用Sub-Protocolを定義する。

---

# 0. この文書の役割

`99_REFERENCE/README.md` は、Legacy / Referenceを利用するTaskでのみ使用する専門Ruleである。

この文書は、

```text
00_AI/AI_WORKFLOW.md
```

を置き換えない。

一般的な、

```text
設計作業
Current Design判定
Save Destination
Git Write Authorization
No-op Write Check
Checkpoint / Baseline
Recovery
Context Sync
```

は `00_AI/AI_WORKFLOW.md` を正本とする。

この文書が担当するのは、

> **Legacy KnowledgeをCurrent Designへ混ぜず、安全に読む・比較する・再利用候補として扱う方法**

だけである。

---

# 1. Legacy Knowledge Source

現在の主要Legacy Source:

```text
daIdaI31104519-ui/-OS-
```

旧Repositoryには、

```text
市場理解OS全体構想
Object
Role
State
Lifecycle
Research
Hypothesis
Evidence
Knowledge
Market DNA
Production
Trade Thesis
Approval
Risk
Authority
Security
Credential
Data Classification
Governance
過去FIX / Backup
```

等の設計資産が存在する。

これらは今後の、

```text
Definition
Detailed Design
Contract
Implementation Spec
Python Design
Test Design
```

で重要な参考資料になり得る。

ただし、

```text
旧Repoに存在する
≠ Current Design

詳細に書かれている
≠ 現在も正しい

過去に採用された
≠ 現在も採用中
```

である。

---

# 2. 最重要原則

Legacy Knowledgeは、

> **Current Designを考える材料**

であり、

> **Current Designを決定するAuthority**

ではない。

したがって、

```text
Legacy
≠ Current

Reference
≠ Current

Reference
≠ Authority

Review済み
≠ 採用済み

ADOPTABLE
≠ ADOPTED

Recommendation
≠ Decision

Proposal
≠ Current Design
```

とする。

---

# 3. Authority Boundary

Current Design Authorityの詳細は、

```text
00_AI/AI_START_HERE.md
00_AI/AI_WORKFLOW.md
Current Design Documents
```

を確認する。

この文書で固定するのは次だけとする。

```text
99_REFERENCE
= NON-AUTHORITATIVE SOURCE

Legacy Repository
= NON-AUTHORITATIVE SOURCE
```

重要:

> **99_REFERENCEはAuthorityが低いのではなく、Current Design Authorityを持たない。**

Legacy側がCurrent Designより詳細であっても、詳細さを理由に優先しない。

---

# 4. Legacy Knowledge Flow

旧設計をCurrent Designへ利用する場合、原則として次の経路を通す。

```text
Current Task
↓
Current Design確認
↓
必要ならCurrent History確認
↓
99_REFERENCE
↓
Legacy Original / FIX / Backup
↓
Comparison
↓
Legacy Review Gate
↓
Proposal
↓
Current Designとして採用するか別途判断
↓
Current Owner Document
```

禁止:

```text
Legacy Repository
↓
Current Design
```

LegacyからCurrentへの直接コピー・直接昇格は行わない。

---

# 5. GPTがLegacyを確認する順番

Legacyを利用する場合、GPTは原則として次の順番で確認する。

```text
1. Current Task確認

2. Current Owner候補確認

3. Current Definition / Responsibility確認

4. Currentの上流 / 下流Boundary確認

5. 必要ならCurrent History確認
   - DESIGN_CHANGE_LOG
   - LESSONS_LEARNED
   - REJECTED_IDEAS
   - FAILURE REVIEW

6. 99_REFERENCE確認

7. 必要なLegacy Original Source確認

8. 必要なLegacy FIX / Backup / Change History確認

9. CurrentとLegacyのDifference抽出

10. Conflict判定

11. Legacy Review Status判定

12. Reuse Recommendation作成

13. Proposal作成

14. Current Designへ反映するか別途判断
```

原則:

> **Currentを先に理解し、その後Legacyを比較材料として読む。**

Legacyを最初の正解として扱わない。

---

# 6. Legacy Source Classification

Legacy関連Sourceを利用する場合、必要に応じて次の分類を使用する。

```text
LEGACY_SOURCE_CLASS = LEGACY_ORIGINAL
```

旧Repo内の通常設計File。

```text
LEGACY_SOURCE_CLASS = LEGACY_SUMMARY
```

市場理解OSまとめ案等の過去総合資料。

```text
LEGACY_SOURCE_CLASS = LEGACY_FIX
```

過去に行われた設計修正。

```text
LEGACY_SOURCE_CLASS = LEGACY_BACKUP
```

FIX前状態やBackup。

```text
LEGACY_SOURCE_CLASS = REFERENCE_SUMMARY
```

Research-1側で作成したLegacy整理資料。

重要:

```text
LEGACY_SOURCE_CLASS
≠ Authority
```

どのLegacy SourceにもCurrent Design Authorityを与えない。

---

# 7. Current Owner Resolution

Legacy Conceptを確認した場合、

> **現在その責任を所有するDocumentはどこか**

をCurrent Designから判断する。

Current Ownerは、過去の対応表やLegacy File名だけで固定しない。

必要に応じて、

```text
AI_CONTEXT
Current Task
PROJECT_CHARTER
HUMAN_MAP
Current Architecture
Current Detailed Design
Current Contract
```

等を確認する。

原則:

```text
Reference File
≠ Current Owner

過去にOwnerだったFile
≠ 現在のOwner
```

`99_REFERENCE/` はCurrent Definitionの保存先にはならない。

---

# 8. Legacy Review Status

Legacy Conceptの比較状態は、他のDocument Statusと混同しないよう専用Namespaceを使用する。

## LEGACY_REVIEW_STATUS = NOT_REVIEWED

Current Designとの比較が完了していない。

Currentへの利用判断を確定しない。

## LEGACY_REVIEW_STATUS = REFERENCE_ONLY

参考知識として有用だが、Current Designへ採用する理由は現在ない。

## LEGACY_REVIEW_STATUS = ADOPTABLE

Current Designと大きな矛盾がなく、再利用可能性が高い。

ただし、

```text
ADOPTABLE
≠ ADOPTED
```

である。

## LEGACY_REVIEW_STATUS = PARTIAL_REUSE

一部の、

```text
考え方
責任
Field
Relation
Failure Knowledge
Governance
```

等だけ再利用可能。

## LEGACY_REVIEW_STATUS = REDESIGN_REQUIRED

問題意識・思想・経験は有用だが、そのままCurrent Architectureへ入れることはできない。

## LEGACY_REVIEW_STATUS = REJECTED

現在条件では利用しない。

REJECTEDでもLegacy Knowledgeとして削除しない。

---

# 9. Conflict Status

Current DesignとLegacyを比較した場合、必要に応じて次を使用する。

```text
LEGACY_CONFLICT_STATUS = NONE
```

重大な不整合なし。

```text
LEGACY_CONFLICT_STATUS = MINOR
```

名称・表現・局所責任等の軽微な差。

```text
LEGACY_CONFLICT_STATUS = MAJOR
```

Authority、Responsibility Boundary、Lifecycle、State、Research / Production Separation、Risk、Security、Production Permission、Data Meaning等に重大な不整合。

```text
LEGACY_CONFLICT_STATUS = UNKNOWN
```

現在情報だけでは判断不能。

重要:

```text
UNKNOWN
↓
自動採用禁止
↓
追加確認
```

とする。

---

# 10. Reuse Recommendation

Legacy Review後、GPTは必要に応じて次のRecommendationを提示できる。

```text
LEGACY_REUSE_RECOMMENDATION = ADOPT
```

ほぼそのまま利用可能な候補。

```text
LEGACY_REUSE_RECOMMENDATION = SIMPLIFY
```

旧設計の責任を維持しながら簡略化する候補。

```text
LEGACY_REUSE_RECOMMENDATION = MERGE
```

現在存在する責任へ一部を統合する候補。

```text
LEGACY_REUSE_RECOMMENDATION = REDESIGN
```

問題意識や教訓を利用し、現在Architecture向けに再設計する候補。

```text
LEGACY_REUSE_RECOMMENDATION = REJECT
```

現在には利用しない候補。

```text
LEGACY_REUSE_RECOMMENDATION = REFERENCE_ONLY
```

参考情報としてのみ維持する候補。

```text
LEGACY_REUSE_RECOMMENDATION = UNDECIDED
```

判断材料不足。

重要:

```text
LEGACY_REUSE_RECOMMENDATION
≠ Current Design Decision
```

GPTは再利用候補を評価できるが、RecommendationだけでCurrent Designとして採用しない。

---

# 11. Legacy DefinitionとCurrent Definitionを融合しない

LegacyとCurrentで異なる定義が存在する場合、自然な文章へ勝手に統合しない。

禁止例:

```text
LegacyではA
CurrentではB
だから現在定義はA+B
```

正しくは、

```text
Legacy Definition
= A

Current Definition
= B

Difference
= ...

Conflict
= ...

Reuse Recommendation
= ...
```

と分ける。

その後、必要であればCurrent Design側で新しいDefinitionを設計する。

---

# 12. Legacy Concept Reference Format

今後作成するLegacy Reference Summaryでは、原則として次の構造を使用する。

```text
## Concept: <名称>

### Legacy Definition
旧設計上の定義。

### Legacy Responsibility
何を担当していたか。

### Legacy Inputs / Outputs
何を受け取り、何を出していたか。

### Legacy Relations
Object / Role / State / Layer等との関係。

### Fix / Failure History
どの問題が発生し、なぜ変更されたか。

### Current Research-1 Relation
Current Design上で近いConcept / Responsibility。

### Current Owner
現在の責任Owner候補。

### Difference
LegacyとCurrentの違い。

### LEGACY_CONFLICT_STATUS
NONE / MINOR / MAJOR / UNKNOWN

### LEGACY_REVIEW_STATUS
NOT_REVIEWED
REFERENCE_ONLY
ADOPTABLE
PARTIAL_REUSE
REDESIGN_REQUIRED
REJECTED

### LEGACY_REUSE_RECOMMENDATION
ADOPT
SIMPLIFY
MERGE
REDESIGN
REJECT
REFERENCE_ONLY
UNDECIDED

### REVIEWED_AGAINST
比較したCurrent Owner Path
Current Version / Baseline等

### Current Design Impact
採用した場合に影響するCurrent Document候補。

### Source
Legacy Path
Commit SHA
関連FIX
関連Backup
```

---

# 13. Review結果の鮮度

Legacy Review結果は永久固定ではない。

Current Designが後から変われば、過去のReview結果も再評価が必要になる場合がある。

したがって、

```text
過去Review結果
≠ 永久有効
```

とする。

Legacy Knowledgeを実際に利用するときは、

```text
前回Review確認
↓
REVIEWED_AGAINST確認
↓
Current Owner / Current Designに重要変更があるか確認
↓
重要変更あり
→ 再Review

重要変更なし
→ 前回Reviewを参考利用
```

とする。

---

# 14. Legacy FIX / Failureを重要Sourceとして扱う

Legacy Conceptを理解するとき、最終Definitionだけを読んで判断しない。

必要に応じて、

```text
なぜその責任になったか
何と何が重複したか
なぜStateを分離したか
なぜAuthorityを分けたか
なぜRiskを分離したか
なぜProduction Permissionを変更したか
どの設計が壊れたか
```

まで確認する。

特に、

```text
FIX-xxx
BEFORE_FIX-xxx
Backup
Design Change
```

は重要なKnowledge Sourceとして扱う。

目的は、

> **旧設計の答えだけではなく、その答えに至った失敗理由を再利用すること。**

---

# 15. Current Designへ採用するとき

Legacy ReviewからCurrent Designへ採用する場合、

```text
Legacy Review
↓
Proposal
↓
Current Owner確認
↓
Current Definition設計
↓
必要なCross Check
↓
Current Owner Document
```

とする。

Current Design側には原則、

> **現在採用するDefinition / Responsibility**

を書く。

Legacy比較の長い説明をCurrent Designへ複製しない。

---

# 16. Git Write Boundary

Legacy Review GateはGit Write Authorizationを与えない。

```text
LEGACY_REUSE_RECOMMENDATION
≠ Git Write Authorization
```

Gitへの保存、変更範囲、No-op Write Check、Checkpoint / Baseline、Recovery等は、

```text
00_AI/AI_WORKFLOW.md
```

を正本とする。

---

# 17. Historyとの責任分離

役割を次のように分ける。

```text
99_REFERENCE
=
昔どう考えていたか
何が存在したか
現在再利用できる可能性はあるか
```

```text
01_HISTORY
=
なぜCurrent Designを変更したか
なぜ採用したか
なぜ却下したか
何を学んだか
```

```text
Current Design
=
今どう設計されているか
```

LegacyをCurrentへ大きく再利用・再設計・却下した場合、重要であればHistoryへ理由を残す。

軽微な用語参考や説明補助だけならHistory保存を必須にしない。

---

# 18. Legacy Contamination Check

Legacyを参照してCurrent Design Proposalを作成した場合、必要に応じて最後に次を確認する。

```text
□ Legacy DefinitionをCurrent Definitionとして無断採用していないか

□ Legacy Object / Role / Stateを理由なく復活させていないか

□ Current Authorityと矛盾していないか

□ Current Owner Responsibilityを壊していないか

□ 既存Current Conceptと重複していないか

□ Legacy文章をそのままCurrent Design化していないか

□ Current Historyで既に却下された案を無断復活させていないか

□ FIX / Failure Historyを無視していないか

□ LEGACY_CONFLICT_STATUS = UNKNOWNなのに採用していないか

□ LEGACY_REUSE_RECOMMENDATIONの理由を説明できるか

□ 元Sourceを追跡できるか

□ 前回Reviewが古くなっていないか
```

重大な問題が残る場合、Current Designへの採用を止める。

---

# 19. Reference Summary

Current Legacy Knowledge Master Index:

```text
99_REFERENCE/
└─ 旧市場理解OS_設計知識リファレンス.md
```

役割:

> **旧Repositoryの大量の設計知識を、Current Design作業で検索・比較しやすくするための圧縮Index / Knowledge Summary**

とする。

このFileは、

```text
Current Design
Canonical Design
Architecture Authority
```

ではない。

Reference Summaryに記載されたことだけではCurrent Designへ採用されたことにならない。

---

# 20. Reference Summaryへ残すもの

原則として次を整理する。

```text
重要Concept
重要Object
重要Role
重要State
重要Lifecycle
重要Responsibility Boundary
過去の主要Fix
過去Failure
Currentとの重要Difference
再利用可能性
Source Pointer
```

目的:

```text
Compression
+
Navigation
+
Comparison
+
Failure Knowledge Reuse
```

旧Repo全文の複製を目的にしない。

---

# 21. 旧Repoを丸ごと移植しない

次は禁止する。

```text
旧OBJECT_DICTIONARYをCurrentへ丸ごとコピー

旧STATE_DICTIONARYをCurrent Standardとして復活

旧ROLE_DICTIONARYをそのまま採用

旧まとめ案をCurrent Architectureとして採用

旧FIX後の最終状態を自動Canonical化
```

必要なKnowledgeだけLegacy Review Gateを通す。

---

# 22. Security Rule

旧RepoからCurrent Public Repositoryへ、

```text
Secret
Credential
API Key
Token
Private Identifier
Sensitive Value
```

等を転記しない。

旧設計の、

```text
Credential Governance
Security Structure
Data Classification
Authority Design
```

等の考え方はReferenceとして利用できる。

ただし実値はCurrent Public Repoへコピーしない。

---

# 23. Legacy Review Complete Definition

あるLegacy Conceptについて、最低限次を説明できればReview完了候補とする。

```text
何だったか
↓
何の責任だったか
↓
何と接続していたか
↓
何が問題になったか
↓
どのように変更されたか
↓
現在の近いConceptは何か
↓
Currentと何が違うか
↓
Conflictは何か
↓
再利用価値はあるか
↓
Reuse Recommendationは何か
↓
どのCurrent Version / Baselineと比較したか
↓
元Sourceはどこか
```

説明できない場合、

```text
LEGACY_REVIEW_STATUS = NOT_REVIEWED
```

または、

```text
LEGACY_CONFLICT_STATUS = UNKNOWN
```

を維持する。

---

# 24. GPT Legacy Decision Flow

```text
Legacy Concept発見
↓
Current Task確認
↓
Current Owner確認
↓
Current Definition確認
↓
必要ならCurrent History確認
↓
Legacy確認
↓
FIX / Failure確認
↓
Difference抽出
↓
Conflict?

UNKNOWN
→ 追加確認

MAJOR
→ REDESIGN / REJECT候補

MINOR
→ SIMPLIFY / MERGE候補

NONE
→ ADOPT候補
↓
LEGACY_REUSE_RECOMMENDATION
↓
Proposal
↓
Current Designとして採用するか別途判断
```

重要:

```text
ADOPT候補
≠ ADOPTED

Proposal
≠ Current Design
```

---

# 25. このPolicy自身の責任境界

この文書は、

```text
市場理解
Research Definition
Knowledge Definition
Trading Rule
Risk Rule
Production Rule
Python Architecture
```

等を決めない。

この文書が決めるのは、

> **GPTがLegacy Knowledgeをどう安全に読み、比較し、再利用候補として扱うか**

だけである。

また、新しい市場理解OS Layerを追加するものでもない。

これは、

```text
AI / Design Knowledge Governance
```

である。

---

# 一文定義

> **REFERENCE POLICY / LEGACY REVIEW GATEとは、AI_WORKFLOW配下でLegacy利用時だけ発動し、旧市場理解OS RepositoryをCurrent Design Authorityとして扱わず、Current Designと必要なCurrent Historyを先に確認した上で、Legacy Definition・FIX・Failure・Backupを比較材料として読み、Difference・Conflict・Review Status・Reuse Recommendation・Review鮮度を明示し、必要な知識だけをProposalとしてCurrent Ownerへ接続することで、Legacy Knowledgeを再利用しながら旧設計と現行設計の混在を防ぐAI向けKnowledge Governance Sub-Protocolである。**
