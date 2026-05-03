# Initial Review

既存ポートフォリオrepoの `index.html` / `portfolio.html` と、ハーネスrepoの `data/` 初期ドラフトをもとにした初回レビューです。

## Summary

現状のページは、保守運用を土台にLinux、Network、Python、監視、自宅サーバ公開へ広げている流れが伝わります。一方で、プロジェクトの状態や公開準備中の成果物が多いため、事実確認が必要な箇所を明確にした上で、文案を少し整理するとより信頼感が出ます。

## Strengths

- 保守運用、監視、障害切り分け、手順書作成の経験が軸になっている
- 個人プロジェクトが実務経験とつながっており、Linux、UFW、Nginx、Zabbixの学習・検証意図が伝わる
- Qiita、GitHub、構成図ギャラリーにより、継続的なアウトプット姿勢を見せられる
- インフラエンジニアらしい「安定運用」「構成整理」「再現性」の思想がある

## Gaps

- Project 01のGitHubリポジトリURLとQiita記事URLが未確定
- Project 02は実装予定のため、実装済みと誤解されない表現が必要
- 資格の取得日が未記入
- `VLAN`、`S3 / CloudFront`、`GitHub Actions` は具体根拠の追記があると強くなる
- 自動化の成果物がまだ抽象的なので、Python / PowerShellで何を効率化したかを追記したい

## Priority Actions

1. `data/links.md` の公開URLと `TODO` を埋める
2. `index.html` のHero / Overviewを、運用改善と構成整理の文脈に少し寄せる
3. `portfolio.html` のProject 01に「運用上の工夫」を追加する
4. Project 02は「実装予定」であることを明確にし、実装後に更新する
5. 資格取得日とSAA Associateの学習状況を確認する

## Suggested Portfolio Updates

### `index.html`

- Hero leadは現状でも方向性がよい。少し短くして「運用」「構築」「手順化」を前に出すと読みやすい
- Overviewの3項目は、実務、個人検証、発信の3軸として整理されているため維持する
- Career leadは、実務と個人検証を区別している点がよい

### `portfolio.html`

- Project 01は「外部公開した」だけでなく、UFW、DDNS、構成図、保守しやすさを含めると強い
- Project 02は「構築済み」に見えないよう、状態表記を維持する
- Qiita記事とGitHub欄は、URL公開後にリンク化する

## Public Repository Concerns

- 現時点で危険な個人情報や機密情報は見当たらない
- 「某省」「医療系ITシステム」は公開粒度としては比較的抽象化されている
- 実務の詳細構成、障害内容、内部IP、顧客固有情報は今後も追加しない

## Next Review Timing

- Project 01のリポジトリまたはQiita記事が公開されたとき
- Project 02の実装が完了したとき
- 資格情報やAWS学習状況が更新されたとき
