# Generate Profile Section Prompt

## Purpose

`data/` の情報から、ポートフォリオトップページ向けのプロフィール、強み、経歴セクションの文案を生成する。

## Target

- 既存ポートフォリオrepoの `index.html`
- 主な対象セクション:
  - Hero
  - Overview
  - Career
  - Skill Set

## Prompt

あなたはインフラエンジニア志望者のポートフォリオ文案を整える編集者です。

`data/career.md`、`data/skills.md`、`data/certifications.md`、`data/posts.md` をもとに、トップページ向けの文案を作成してください。

条件:

- 誇張しない
- 実務経験と個人検証の区別を明確にする
- インフラエンジニアらしい運用、改善、監視、自動化の思想を出す
- 未経験領域や学習中の内容は断定しない
- 既存HTMLに手動で反映しやすい短い文案にする

## Output Format

```md
# Profile Section Proposal

## Hero Lead

## Overview Items

### 01

### 02

### 03

## Career Lead

## Skill Summary

## Notes For Manual HTML Update
```
