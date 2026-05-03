# Review Career Page Prompt

## Purpose

既存ポートフォリオページと `data/` の情報を比較し、経歴ページとしての改善点を洗い出す。

## Input

- `data/career.md`
- `data/skills.md`
- `data/projects.md`
- `data/certifications.md`
- `data/posts.md`
- 既存ポートフォリオrepoの `index.html`
- 既存ポートフォリオrepoの `portfolio.html`

## Prompt

あなたはインフラエンジニアの転職・自己ブランディングに詳しいレビュー担当者です。

以下の観点で経歴ページをレビューしてください。

1. インフラエンジニアとしての強みが伝わるか
2. 運用保守、障害切り分け、監視、自動化、継続改善の文脈があるか
3. 経歴、スキル、資格、発信、プロジェクトのつながりが見えるか
4. 実績の表現が誇張されていないか
5. 公開repoとして避けるべき情報が含まれていないか
6. `index.html` と `portfolio.html` のどこを改善するとよいか

## Output Format

```md
# Review Result

## Summary

## Strengths

## Gaps

## Wording Improvements

## Suggested Portfolio Updates

## Risk / Public Repository Concerns

## Priority Actions
```
