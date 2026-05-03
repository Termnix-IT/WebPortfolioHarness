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
- `ToolBox.html`
  - 使用ツールや技術スタック
- `Diagram.html`
  - 構成図ギャラリー
- `contact.html`
  - 問い合わせ導線

## Initial Integration Policy

- このハーネスrepoから既存ポートフォリオrepoを直接書き換えない
- 生成するのは文案、レビュー、HTML差し替え案までにする
- 反映は人間が確認して手動で行う
- 反映対象は当面 `index.html` と `portfolio.html` を中心にする

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

## Future Automation Policy

将来的にスクリプトやGitHub Actionsを追加する場合も、初期設定では自動反映しません。

推奨する段階:

1. MarkdownからAI投入用コンテキストを生成する
2. HTML差し替え案を `output/` に生成する
3. 人間が確認して手動反映する
4. 必要になったらPR作成補助を検討する

## Review Checklist Before Applying To Portfolio Repo

- [ ] 既存HTMLのデザインと文量に合っている
- [ ] モバイル表示で長すぎない
- [ ] 事実と一致している
- [ ] 公開してよい内容だけになっている
- [ ] 実務経験と個人検証の区別が明確
