# Portfolio Project Proposal

既存ポートフォリオrepoの `portfolio.html` 向け反映案です。

## Target Repository

```text
C:\Users\lugep\デスクトップ\ProjectFolder\WebProject\PortfolioPage
```

## Target File

- File: `portfolio.html`
- Section: Project cards
- Current Identifier: `project-1`, `project-2`

## Purpose

- 変更目的: プロジェクトの目的、運用観点、公開状態を明確にする
- 期待する見え方: 技術名だけでなく、インフラ運用目線のある個人検証として伝わる
- 関連する `data/`: `data/projects.md`, `data/skills.md`, `data/posts.md`

## Proposed Text

### Project 01 Description

```text
Flask + Linux構成でWebページを外部公開し、UFWによるセキュリティ制御、DDNS、Nginx、構成図整理まで実施。公開手順だけでなく、あとから保守しやすい形で残すことを意識した個人プロジェクトです。
```

### Project 01 Qiita Text

```text
UFW設定とサーバ公開の手順、構成整理についてまとめた記事
```

### Project 01 GitHub Text

```text
Flaskを用いたWebサーバ構成と、公開環境の手順整理
```

### Project 02 Description

```text
Raspberry Pi上にZabbix Serverを構築し、監視、通知、初期切り分けの流れを検証予定。実務での監視経験を、個人環境での監視基盤構築へ接続するプロジェクトです。
```

### Project 02 Qiita Text

```text
Zabbix agent設定、UFW、メール通知の構築手順をまとめる予定
```

### Project 02 GitHub Text

```text
Zabbix構成の設定ファイル、手順、監視設定を整理予定
```

## Manual Update Notes

- 差し替え対象: 各 `.project-desc`、Qiitaカード本文、GitHubカード本文
- 既存デザインへの影響: Project 01の説明は現状より長くなるため、モバイル表示確認が必要
- 確認すべき表示: status badgeがProject 01は公開準備中、Project 02は実装予定のままになっていること

## Review Checklist

- [ ] Project 01の実装状態と一致している
- [ ] Project 02を実装済みのように見せていない
- [ ] 公開前URLをリンク化していない
- [ ] 詳細な内部構成を書きすぎていない
- [ ] モバイル表示で長すぎない
