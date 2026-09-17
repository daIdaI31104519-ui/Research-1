# 市場理解OS — Human-First Rebuild

このRepositoryは、市場理解OSを旧設計からそのまま複製するのではなく、**人間が理解でき、AIが詳細設計を補助し、Pythonへ落とし込みやすく、領域間を接続・検証できる形へ再構築するための新Repository**である。

## AI / GPT Entry

Cold Start、新しいChat、Context Loss、別AIへの引き継ぎ時は、最初に次を読む。

```text
00_AI/AI_START_HERE.md
```

ここを市場理解OSのAI用起動入口とし、作業方法・現在地・直前Conversation・Current Taskへ必要な範囲だけ移動する。

## このRepoの位置づけ

- `Research-1` = 現在の再構築先 / Current Rebuild
- 旧Repo `daIdaI31104519-ui/-OS-` = Reference / Legacy Knowledge
- 旧Repoの内容は、自動的に新Canonicalへ昇格しない。
- 旧設計は Review → Adoption / Simplification / Redesign / Rejection を経て利用する。

## 再構築の最重要方針

1. Human Understandingを先に作る。
2. 各領域を単体で完成させるだけでなく、他領域との接続を必ず確認する。
3. ResearchとProductionを分離する。
4. Researchは大きく、Live Pathは小さく保つ。
5. AIは計算やHard Riskの代替ではなく、解釈・仮説・反証・査読・説明を中心に使う。
6. 設計変更・失敗・却下理由を消さず、Design Knowledgeとして残す。
7. Python実装前に、Human / Semantic / Connection / Contract / Testを整える。
8. 秘密情報、API Key、CredentialをPublic Repoへ保存しない。

## 現在の状態

現在のProject Phase、Current Task、主要Working Baseline、重要Pending、Next Actionは、

```text
00_AI/AI_CONTEXT.md
```

を正本とする。

README自身へ、頻繁に変化するProject Current Stateを重複保存しない。

設計変更・失敗・却下・教訓の履歴入口は、

```text
01_HISTORY/README.md
```

を参照する。

Architecture / Connection設計は、

```text
02_ARCHITECTURE/
```

を参照する。

## 基本フロー

```text
Human Understanding / Project Charter
↓
Architecture / Connection
↓
Cross-Layer Reconciliation
↓
Cross-Cutting
↓
Detailed Design
↓
Contract / Implementation Spec
↓
Python
↓
Tests
↓
Production
```

詳細な現在地点は `00_AI/AI_CONTEXT.md` を参照する。

## 注意

このRepoには、

```text
Current Design

Draft

Working Baseline

History

Failure Review

Rejected / Legacy

Reference
```

が共存できる。

したがって、

```text
Gitに存在する
≠
現在採用中
```

である。

現在採用中の設計を判断するときは、Document Role、Status、History、Superseded関係を確認する。
