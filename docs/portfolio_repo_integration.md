# Portfolio Repository Integration

既存ポートフォリオrepoとの接続方針をまとめます。

## Existing Portfolio Repository

```text
C:\Users\lugep\デスクトップ\ProjectFolder\WebProject\PortfolioPage
```

## Current Shape

既存repoは静的HTMLサイトです。

- `index.html`
  - Hero
  - Overview
  - Career
  - Skill Set
  - Publishing
- `portfolio.html`
  - Project cards
  - Related articles
  - GitHub repository references
- `toolbox.html`
  - 使用ツールや技術スタック
- `diagram.html`
  - 構成図ギャラリー
- `contact.html`
  - 連絡チャンネル
  - AWS Lambda Function URL へ JSON POST する問い合わせフォーム

## Current Design And Operation State

2026-05-25時点の既存ポートフォリオrepoは、v2.1.0相当の状態です。

- 全ページが Career Document Layout (`body.cdoc-page`, `.cdoc-*`) を使用している
- 共通スタイルは `static/style.css` の Career Document Layout ブロックが中心
- 共通JavaScriptは `static/main.js` に集約されている
- `static/main.js` はナビゲーションのactive表示、Qiita記事取得、問い合わせフォーム送信を担当する
- 問い合わせフォームは `name`, `email`, `topic`, `message`, `_gotcha` をJSONとして送信する
- サイト側にはメール送信処理や問い合わせ内容の保存処理を持たせない
- デプロイは GitHub Actions から AWS S3 + CloudFront へ行う前提
- deploy bundle は `*.html` と `static/` のみを対象にする

## Related Portfolio Docs

既存ポートフォリオrepo側では、以下のドキュメントも参照対象にします。

- `README.md`: 現行ページ構成、技術スタック、問い合わせフォーム概要
- `docs/MAINTENANCE.md`: 編集ルール、問い合わせフォーム運用方針
- `docs/DEPLOYMENT.md`: AWS S3 + CloudFront へのデプロイ方針
- `docs/security_best_practices_report.md`: 問い合わせフォーム追加時のセキュリティレビュー
- `docs/リリースノート_v2.1.0.md`: v2.1.0の変更履歴

## Initial Integration Policy

- このハーネスrepoから既存ポートフォリオrepoを直接書き換えない
- 生成するのは文案、レビュー、HTML差し替え案までにする
- 反映案を人間が確認し、明示的な許可が出た場合だけ反映する
- 反映対象は `index.html` と `portfolio.html` を中心にしつつ、必要に応じて `contact.html`, `toolbox.html`, `diagram.html` も扱う

## Approval Gate

既存ポートフォリオrepoへの変更は、反映案の確認後にだけ行います。

- 反映前に、変更対象ファイル、対象セクション、差し替え文案を提示する
- 反映案は `output/proposals/` に保存するか、同等に確認できる形で提示する
- ユーザーが明示的に許可するまで、既存ポートフォリオrepoのHTMLや関連ファイルを編集しない
- 許可後の反映は、確認しやすい小さな変更単位で行う

## Manual Update Targets

### `index.html`

- Hero lead
- Overview items
- Career timeline
- Credentials
- Skill Set
- Publishing

### `portfolio.html`

- Project description
- Tech tags
- Qiita article text
- GitHub repository text
- Diagram / screenshot notes

### `contact.html`

- Contact lead
- Contact channels
- Contact form explanatory text
- Public safety note
- Form topic labels

### `toolbox.html`

- Tool descriptions
- Roadmap text
- Prepared / planned status text

### `diagram.html`

- Diagram description
- Architecture notes
- Upcoming diagram notes

## Future Automation Policy

将来的にスクリプトやGitHub Actionsを追加する場合も、初期設定では自動反映しません。

推奨する段階:

1. MarkdownからAI投入用コンテキストを生成する
2. HTML差し替え案を `output/` に生成する
3. 人間が確認し、明示的な許可が出た場合だけ反映する
4. 必要になったらPR作成補助を検討する

## Review Checklist Before Applying To Portfolio Repo

- [ ] 反映案を事前に提示している
- [ ] ユーザーから明示的な反映許可が出ている
- [ ] 既存HTMLのデザインと文量に合っている
- [ ] モバイル表示で長すぎない
- [ ] 事実と一致している
- [ ] 公開してよい内容だけになっている
- [ ] 実務経験と個人検証の区別が明確
