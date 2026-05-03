# Projects

ポートフォリオ掲載候補の個人プロジェクト、GitHub成果物、検証環境を整理します。

## Project Entry Template

### Project Name

- Status:
- Repository:
- Demo / Page:
- Related Article:
- Purpose:
- Background:
- Tech Stack:
- Architecture:
- What I Built:
- Operations / Maintenance Points:
- Security Considerations:
- Troubleshooting / Improvements:
- What This Shows:
- Portfolio Page Target:
  - `index.html`:
  - `portfolio.html`:

## Projects

### 自宅サーバ公開プロジェクト

- Status: 公開ページ掲載中。Qiita記事とGitHubリポジトリは公開準備中
- Repository: TODO: 公開URL確認。既存ページでは「公開準備中」
- Demo / Page: `portfolio.html#project-1`
- Related Article: UFW設定とサーバ公開についてまとめた記事。既存ページでは「公開準備中」
- Purpose: Flask + Linux構成でWebページを外部公開し、公開・制御・構成整理を一通り検証する
- Background: 実務の運用保守経験に加え、個人でも構築と公開の流れを確認するため
- Tech Stack: Flask、Linux、Nginx、UFW、DDNS
- Architecture: `static/img/server-diagram.png` に構成図あり。公開repoでは詳細すぎる内部情報を出さない
- What I Built: FlaskとLinuxを使った公開環境、UFWによるセキュリティ制御、DDNSによる外部公開、構成図と手順整理
- Operations / Maintenance Points: 公開手順だけでなく、保守しやすさ、あとから見返せる構成整理を意識
- Security Considerations: UFWによる制御を実施。詳細な公開ポートや内部構成は必要以上に書かない
- Troubleshooting / Improvements: TODO: 実際に詰まった点、改善した点を追記
- What This Shows: Linux、Nginx、UFW、DDNS、Flaskを組み合わせ、運用を見据えた公開環境を自分で構築していること
- Portfolio Page Target:
  - `index.html`: 注目プロジェクト
  - `portfolio.html`: project-1

### Zabbix監視環境構築

- Status: 実装予定 / 掲載準備中
- Repository: TODO: 公開URL確認。既存ページでは「実装予定」
- Demo / Page: `portfolio.html#project-2`
- Related Article: エージェント設定・UFW・通知の構築まとめ。既存ページでは「実装予定」
- Purpose: Raspberry Pi上にZabbix Serverを構築し、監視環境を整備する
- Background: 実務での監視・アラート対応経験を、個人検証の監視基盤構築へ接続するため
- Tech Stack: Zabbix、Raspberry Pi、UFW、メール通知
- Architecture: TODO: 実装後にスクリーンショットまたは構成図を追加
- What I Built: TODO: 実装後にZabbix Server、agent設定、通知設定、監視対象を追記
- Operations / Maintenance Points: 監視、通知、初期切り分け、あとから見返せる手順化を訴求予定
- Security Considerations: UFW利用予定。公開範囲や通知設定の詳細は公開しすぎない
- Troubleshooting / Improvements: TODO: 実装後に追記
- What This Shows: 監視基盤、通知、運用設計への関心と、実務の監視経験を個人検証へ広げていること
- Portfolio Page Target:
  - `index.html`: スキル・監視領域
  - `portfolio.html`: project-2
