# REFERENCE POLICY

Status: ACTIVE

旧Repository:

`daIdaI31104519-ui/-OS-`

は、市場理解OSの過去設計・検討・失敗・改善を参照するためのLegacy Knowledge Sourceとして扱う。

## ルール

1. 旧Repoは削除しない。
2. 旧Repoの設計を新Repoへ自動コピーしない。
3. 新Repoへ採用する場合は、現在のHuman Map / Connection / Cross-Cutting設計と照合する。
4. 旧案と現在案が矛盾する場合、新Repoの現在Statusを優先する。
5. 旧案を却下・変更する場合、理由を `01_HISTORY/` に残す。
6. 旧RepoのSecret / Credential / Sensitive情報を新Public Repoへ転記しない。

## 採用フロー

```text
Old Repo
↓
Reference
↓
Review
↓
Adopt / Simplify / Merge / Redesign / Reject
↓
New Design
```

旧RepoはCanonicalではなく、再構築のための研究資産である。
