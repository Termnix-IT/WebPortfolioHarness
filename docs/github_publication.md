# GitHub Publication

このリポジトリをGitHubで公開する前の準備メモです。

## Repository Name

候補:

```text
career-page-harness
```

## Description

候補:

```text
Markdown-based career page improvement harness for portfolio review and proposal generation.
```

## Before First Push

- [ ] `data/` に非公開情報がないことを確認する
- [ ] `output/` に公開してよいレビュー・提案だけが入っていることを確認する
- [ ] `TODO` が公開しても問題ない内容だけであることを確認する
- [ ] `README.md` の関連repoパスを公開して問題ないか確認する
- [ ] GitHub上のrepo visibilityを決める

## Suggested Topics

- portfolio
- career
- markdown
- ai-workflow
- infrastructure
- operations

## Initial Push Flow

```powershell
git remote add origin <repository-url>
git push -u origin master
```

公開先URLは作成後に `data/links.md` と `README.md` に反映します。
