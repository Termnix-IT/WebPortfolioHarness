# Roadmap

このリポジトリで次に進める作業を、優先順位つきで管理します。

## Priority 0: Portfolio Repo Sync

- [x] 既存ポートフォリオrepoの現行構成を確認する
- [x] v2.1.0で問い合わせフォームが追加されたことを把握する
- [x] `ToolBox.html` / `Diagram.html` が `toolbox.html` / `diagram.html` に変更されたことを把握する
- [x] Career Document Layout (`body.cdoc-page`, `.cdoc-*`) への統一を把握する
- [ ] ハーネス側の反映案テンプレートを現行ページ構成に合わせて更新する
- [ ] `contact.html` 向けのレビュー観点を追加する
- [ ] 既存ポートフォリオrepo v2.1.0 を前提に、初回レビューと反映案を見直す

## Priority 1: Data Completion

- [ ] `data/certifications.md` の資格取得日を確認する
- [ ] `data/links.md` のPortfolio URLを確認する
- [ ] Project 01のGitHubリポジトリURLを確認する
- [ ] Project 01のQiita記事URLを確認する
- [ ] Project 02の実装状況を確認する
- [ ] Project 02のGitHubリポジトリURLと記事URLを確認する

## Priority 2: Review And Proposal

- [x] 既存ポートフォリオHTMLから `data/` の初期ドラフトを作る
- [x] 初回レビューを作る
- [x] `index.html` 向けの反映案を作る
- [x] `portfolio.html` 向けの反映案を作る
- [ ] `contact.html` の問い合わせフォーム文言と公開リスクをレビューする
- [ ] 小文字化後の `toolbox.html` / `diagram.html` を前提にリンク表記を確認する
- [ ] 人間が文案の事実確認を行う

## Priority 3: Manual Portfolio Update

- [ ] `index.html` のHero / Overview / Career文案を選定する
- [ ] `portfolio.html` のProject 01 / Project 02文案を選定する
- [ ] `contact.html` の問い合わせフォーム文言を見直す
- [ ] 既存ポートフォリオrepoへ手動反映する
- [ ] デスクトップ表示を確認する
- [ ] モバイル表示を確認する

## Priority 4: Repository Operation

- [ ] GitHub公開前に `docs/public_repository_policy.md` を再確認する
- [ ] READMEの見え方を確認する
- [ ] repo descriptionを決める
- [ ] remote repositoryを作成する
- [ ] 初回pushする

## Priority 5: Automation Design

- [x] 将来スクリプトの仕様を文書化する
- [ ] `build_context.py` を実装する
- [ ] `check_public_safety.py` を実装する
- [ ] `check_links.py` を実装する
- [ ] GitHub Actions導入可否を判断する
