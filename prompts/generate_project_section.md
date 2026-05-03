# Generate Project Section Prompt

## Purpose

`data/projects.md` から、`portfolio.html` に掲載しやすいプロジェクト紹介文案を生成する。

## Target

- 既存ポートフォリオrepoの `portfolio.html`
- 主な対象:
  - `project-1`
  - `project-2`
  - 今後追加するプロジェクトカード

## Prompt

あなたはインフラ・運用改善系ポートフォリオの編集者です。

`data/projects.md` をもとに、プロジェクト紹介文を作成してください。

条件:

- 何を作ったかだけでなく、なぜ作ったかを書く
- 運用、監視、セキュリティ、改善の観点を含める
- 実装済み、準備中、学習中を明確に分ける
- 公開してはいけない構成情報や認証情報は含めない
- 既存の `portfolio.html` に手動反映しやすい粒度にする

## Output Format

```md
# Project Section Proposal

## Project Summary

## Project Card Text

## Tech Tags

## Related Article Text

## GitHub Repository Text

## HTML Patch Notes
```
