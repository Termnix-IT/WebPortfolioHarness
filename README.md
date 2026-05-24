# career-page-harness

経歴ページを継続的に改善するための補助リポジトリです。

このリポジトリは、公開用ポートフォリオサイトそのものではありません。職務経歴、スキル、資格、技術記事、GitHub成果物、ポートフォリオ掲載候補を Markdown で整理し、AI にレビューや文案生成を依頼しやすくすることを目的にしています。

## Purpose

- 公開可能な経歴情報を Markdown で管理する
- AI に渡しやすい粒度で実績、スキル、発信内容を整理する
- 経歴ページの改善案、修正文案、HTML反映案を作りやすくする
- 既存ポートフォリオrepoとは責務を分離する
- 初期段階では自動反映せず、人間の確認を前提に運用する

## Related Repository

既存ポートフォリオページrepo:

```text
C:\Users\lugep\デスクトップ\ProjectFolder\WebProject\PortfolioPage
```

このハーネスrepoでは、既存repoの `index.html` や `portfolio.html` を直接変更しません。必要な場合は、差し替え候補やHTML反映案を作成し、内容を確認したうえで明示的な許可が出た場合だけポートフォリオrepoへ反映します。

### Current Portfolio Repo State

2026-05-25時点の既存ポートフォリオrepoは、以下の構成です。

- 全ページが Career Document Layout (`body.cdoc-page`, `.cdoc-*`) に統一済み
- 公開ページは `index.html`, `portfolio.html`, `toolbox.html`, `diagram.html`, `contact.html`
- `ToolBox.html` / `Diagram.html` は小文字の `toolbox.html` / `diagram.html` に変更済み
- `contact.html` には AWS Lambda Function URL へ JSON POST する問い合わせフォームを実装済み
- デプロイは GitHub Actions から AWS S3 + CloudFront へ行う前提
- 公開bundleは `*.html` と `static/` を対象にし、`docs/` や `README.md` は配布対象外

## Directory Structure

```text
career-page-harness/
├─ README.md
├─ .gitignore
├─ data/
│  ├─ career.md
│  ├─ skills.md
│  ├─ projects.md
│  ├─ certifications.md
│  ├─ posts.md
│  └─ links.md
├─ prompts/
│  ├─ review_career_page.md
│  ├─ generate_profile_section.md
│  ├─ generate_project_section.md
│  └─ improve_wording.md
├─ templates/
│  ├─ profile_section.md
│  ├─ project_card.md
│  ├─ skill_matrix.md
│  └─ html_patch_proposal.md
├─ output/
│  └─ .gitkeep
├─ scripts/
│  └─ README.md
└─ docs/
   ├─ automation_design.md
   ├─ checklists.md
   ├─ github_publication.md
   ├─ roadmap.md
   ├─ workflow.md
   ├─ design_policy.md
   ├─ public_repository_policy.md
   └─ portfolio_repo_integration.md
```

## Basic Workflow

1. `data/` のMarkdownを更新する
2. `prompts/` のプロンプトを使ってAIにレビューや文案生成を依頼する
3. 必要に応じて `templates/` の形式で出力を整える
4. 生成案を人間が確認する
5. 明示的な許可が出た場合だけ、既存ポートフォリオrepoへ反映する

## Practical Workflow

既存ポートフォリオページを改善するときは、次の順で進めます。

1. `data/` の `TODO` を確認する
2. `output/reviews/initial_review.md` を読み、改善優先度を確認する
3. `output/proposals/` の反映案を確認する
4. 事実・公開可否・表現を人間が確認する
5. 反映許可が出た場合だけ、既存ポートフォリオrepoへ反映する
6. 表示確認後、必要に応じて `data/` に戻して情報を更新する

## Approval Policy

既存ポートフォリオrepoへ変更を入れる前に、必ず反映案を提示します。

- 反映案は `output/proposals/` など、確認しやすい形で残す
- 変更対象、差し替え文案、公開可否の確認点を明記する
- ユーザーが明示的に許可するまで、既存ポートフォリオrepoのHTMLや関連ファイルを編集しない
- 許可後に反映した場合も、表示確認と差し戻ししやすい変更単位を意識する

## Priority Backlog

現時点の優先順位は以下です。

1. 既存ポートフォリオrepo v2.1.0 の構成変更をハーネス側のdocsへ反映する
2. `data/` の `TODO` を埋める
3. 初回レビューをもとに改善候補を選ぶ
4. `index.html` の Hero / Overview / Career 文案を調整する
5. `portfolio.html` の Project 01 / Project 02 文案を調整する
6. 問い合わせフォーム、公開URL、デプロイ方針を確認してから既存ポートフォリオrepoへ反映する

## Public Repository Policy

このリポジトリは公開しても問題ない情報だけを置く前提です。

- 住所、電話番号、非公開メールアドレスは置かない
- 顧客名、案件名、内部構成、障害詳細、契約情報は置かない
- 実務内容は公開可能な粒度に抽象化する
- AI生成文は事実確認してから採用する

詳細は `docs/public_repository_policy.md` を参照してください。

## Current Scope

初期段階では以下のみを対象にします。

- Markdownによる情報整理
- AIレビュー用プロンプト管理
- プロフィール、プロジェクト、スキル表の文案生成
- 既存HTMLへ反映するための手動提案作成

以下は初期段階では対象外です。

- 既存ポートフォリオrepoへの自動書き込み
- GitHub Actionsによる自動反映
- 個人情報を含む職務経歴書の完全管理
- 非公開情報や機密情報の保存

## Future Ideas

- `data/` からAI投入用Markdownを生成するスクリプト
- Markdown lint
- リンクチェック
- 公開禁止ワードの簡易チェック
- HTML差し替え案の自動生成
- 既存ポートフォリオrepoへのPR作成補助

詳細な拡張方針は `docs/automation_design.md` と `docs/roadmap.md` を参照してください。
