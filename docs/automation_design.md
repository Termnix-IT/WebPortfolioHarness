# Automation Design

将来的に追加する自動化の設計メモです。

## Principles

- 初期段階では既存ポートフォリオrepoを直接変更しない
- 自動化は確認作業を助けるために使う
- 生成物は `output/` に出し、人間が確認してから採用する
- 公開可否チェックは自動削除ではなく警告に留める

## Phase 1: Context Builder

- Script: `scripts/build_context.py`
- Goal: `data/` の情報をAIレビュー用にまとめる
- Output: `output/context/career_page_context.md`
- Risk: 古い情報を集約してしまうこと
- Mitigation: 出力に生成日時と参照ファイル一覧を含める

## Phase 2: Public Safety Check

- Script: `scripts/check_public_safety.py`
- Goal: 公開repoに置くべきでない語句を検出する
- Output: `output/reports/public_safety.md`
- Risk: 禁止語句を含むポリシー文も検出されること
- Mitigation: `docs/public_repository_policy.md` などは警告扱いにする

## Phase 3: Link Check

- Script: `scripts/check_links.py`
- Goal: GitHub、Qiita、Portfolio URLの確認を補助する
- Output: `output/reports/link_check.md`
- Risk: ネットワーク制限で失敗すること
- Mitigation: URL抽出だけでも有効な結果として扱う

## Phase 4: HTML Proposal Generator

- Script: `scripts/generate_html_proposal.py`
- Goal: 既存HTMLに手動反映する提案を生成する
- Output: `output/proposals/*.md`
- Risk: HTML構造に依存しすぎること
- Mitigation: 差し替え案は人間が確認するMarkdownに留める

## GitHub Actions Candidates

- Markdown lint
- TODO一覧の抽出
- 公開禁止語句の簡易チェック
- リンク一覧の抽出

GitHub Actionsで既存ポートフォリオrepoへ自動反映する処理は、初期段階では導入しません。
