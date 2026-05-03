# Index Profile Proposal

既存ポートフォリオrepoの `index.html` 向け反映案です。

## Target Repository

```text
C:\Users\lugep\デスクトップ\ProjectFolder\WebProject\PortfolioPage
```

## Target File

- File: `index.html`
- Section: Hero / Overview / Career / Skill Set
- Current Identifier: `hero-title`, `Overview`, `Career`, `Skill Set`

## Purpose

- 変更目的: 運用保守、構成整理、個人検証のつながりをより明確にする
- 期待する見え方: インフラエンジニアらしい運用・改善・自動化志向が伝わる
- 関連する `data/`: `data/career.md`, `data/skills.md`, `data/projects.md`

## Proposed Text

### Hero Lead

```text
Linux・ネットワーク・監視を中心に、保守運用の現場経験と個人での構築検証をつなげています。公開環境、監視基盤、手順化を通じて、あとから見返せる構成整理と安定運用を意識しています。
```

### Overview 01

```text
Windows Server やネットワーク維持保守の現場で、監視、ログ確認、障害切り分け、手順書作成を継続して担当してきました。
```

### Overview 02

```text
Linux、UFW、Nginx、DDNSを使った自宅サーバ公開や、Zabbix監視環境の構築を個人プロジェクトとして進めています。
```

### Overview 03

```text
構築手順や学習内容をQiita・GitHubに整理し、あとから再利用できる形でアウトプットすることを意識しています。
```

### Career Lead

```text
実務では保守運用と監視・切り分けを中心に経験し、個人活動ではLinux構築、Web公開、監視基盤、Python活用を継続しています。現場での安定運用と、個人検証での構築経験を接続している点が今の強みです。
```

## Manual Update Notes

- 差し替え対象: `bp-lead-text`, Overview3項目, `profile-column-lead`
- 既存デザインへの影響: 文字量は現状と同程度。Hero Leadはやや短くなる
- 確認すべき表示: モバイル幅でHero LeadとOverview本文が長すぎないこと

## Review Checklist

- [ ] 事実と一致している
- [ ] 誇張表現がない
- [ ] 個人情報や機密情報がない
- [ ] 実務経験と個人検証が混ざっていない
- [ ] モバイル表示で長すぎない
