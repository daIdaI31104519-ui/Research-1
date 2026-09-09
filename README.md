# 市場理解OS — Human-First Rebuild

このRepositoryは、市場理解OSを旧設計からそのまま複製するのではなく、**人間が理解でき、AIが詳細設計を補助し、Pythonへ落とし込みやすく、領域間を接続・検証できる形へ再構築するための新Repository**である。

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

このRepoは再構築初期段階である。

`00_HUMAN/HUMAN_MAP.md` は現在作成中で、詳細設計を確定したものではない。

設計史は `01_HISTORY/` に保存する。

領域間接続は `02_ARCHITECTURE/` で今後整理する。

## 基本フロー候補

```text
Human Understanding
↓
Architecture / Connection
↓
Cross-Layer Reconciliation
↓
Detailed Design
↓
Contract / Implementation Spec
↓
Python
↓
Unit / Contract / Integration / E2E Test
```

## 注意

このRepoの文書は状態を明示する。

`DRAFT` / `PROPOSED` / `ADOPTED` / `SUPERSEDED` / `REJECTED` 等を使い、古い案と現在採用中の設計を混同しない。
