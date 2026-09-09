# REJECTED / LEGACY IDEAS

Status: ACTIVE HISTORY

この文書は、過去に検討したが現在の新市場理解OSでは採用しない、または役割を変更した案を保存する。

`REJECTED` は「価値がなかった」という意味ではない。
その時点の設計課題を解くために考えられたが、後の検討でより良い配置・責任分離が見つかったものも含む。

---

## LEGACY-001 — AI Team / AI MeetingをProduction判断の中心に置く

### 旧案
複数AIを役割分担させ、AI Meetingで議論・多数決・統合してSignalへ送る。

### 問題
- 同じ誤りを複数AIが共有できる。
- AI多数決はEvidenceの独立性を保証しない。
- Production Pathが重くなる。
- AI障害がLive判断へ直結しやすい。

### 現在の代替
AI Assistanceを横断機能化する。
AIはInterpreter / Hypothesis Generator / Research Assistant / Reviewer / Attribution Assistant / Human Explainer等として使う。

### Status
SUPERSEDED

---

## LEGACY-002 — 「Trade Loss → Trainer → 即Model更新」中心Loop

### 旧案
LossをTrainerへ送り、ModelやRuleへ反映する。

### 問題
Loss原因がModelとは限らない。
誤ったFailure Attributionが本番を壊す可能性がある。

### 現在の代替
Post-Trade Attribution → Research Router → 原因別Research。

### Status
REJECTED AS CORE LOOP

---

## LEGACY-003 — QuantumをLive必須Layerにする

### 旧案
Market UnderstandingからAI / Signalへ進む前にQuantum Layerを必ず通す。

### 問題
探索・最適化とProduction判断が混ざる。
Live Pathが重くなる。
Quantumの出力自体はValidation済みKnowledgeではない。

### 現在の代替
Quantum / Search = Research Tool。
候補探索後は通常Candidateと同じValidationへ送る。

### Status
SUPERSEDED

---

## LEGACY-004 — Stress LabをResearch全体の独立Layerとして扱う

### 旧案
Sandbox / Stress Lab / Failure Museum等を多数の連続Layerとして配置する。

### 問題
Research、Validation、Knowledgeの責任が重複する。

### 現在の代替
Stress = Research / ValidationのTool。
成果はStressResult / FailureBoundary / Constraint等へ整理する方向。

### Status
SUPERSEDED

---

## LEGACY-005 — Single Hypothesis Only Production

### 旧案
最も強い一つのHypothesisをProduction判断の中心へ置く。

### 問題
現在市場では複数Mechanism、条件、反対Evidenceが同時に存在する。

### 現在の代替
Approved Hypothesis Pool → Applicable Hypothesis Set → Trade Thesis。

### Status
SUPERSEDED

---

## LEGACY-006 — Hypothesis多数決

### 旧案候補
BUY仮説の数とSELL仮説の数を比較して方向を決める。

### 問題
同じEvidenceやCommon Causeから派生したHypothesisを独立票として数える危険がある。

### 現在の代替
Shared Evidence / Dependence / Redundancy / Contradiction / Applicability / Expected Valueを構造として見る。

### Status
REJECTED

---

## LEGACY-007 — Research結果を直接Production Ruleへ反映

### 問題
未検証Candidateや一時的Edgeがそのまま実資金へ入る危険がある。

### 現在の代替
Research → Validation → Forward Evidence → Governance / Promotion → Production。

### Status
REJECTED

---

## LEGACY-008 — AIがその場で未検証HypothesisをLive Trade Thesisへ追加

### 問題
AIの発想と研究済みKnowledgeを混同する。

### 現在の代替
AIが見つけた新HypothesisはResearch Candidateとして保存し、現在Tradeへ直接追加しない。

### Status
REJECTED

---

## LEGACY-009 — Human DiaryをMachine Learningの正本にする

### 問題
自然言語要約には省略・解釈・生成誤差が含まれる。

### 現在の代替
Machine-readableなData / Evidence / Traceを正本にし、Human Diaryは表示・理解用Viewとして扱う方向。

### Status
HOLD / NOT CORE SOURCE

---

## LEGACY-010 — 独立Layerを増やせば責任が明確になるという考え

### 問題
Layerを細分化しすぎると、責任・Data Contract・順序・依存関係が増え、人間理解とIntegrationが悪化する。

### 現在の代替
Domain / Component / Tool / View / Cross-Cutting Responsibilityを区別し、必要以上に一本道のLayerへしない。

### Status
SUPERSEDED ARCHITECTURE STYLE

---

# 再検討ルール

REJECTED / LEGACY案も永久禁止ではない。

将来、
- 新しいEvidence
- 技術変化
- Production要件変化
- Cost変化
- 安全性改善

等によって再検討する場合は、新Proposalとして理由を明示し、旧問題が解決されたことを確認する。
