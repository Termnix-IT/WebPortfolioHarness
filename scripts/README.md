# scripts

将来、自動化スクリプトを置くためのディレクトリです。

初期段階ではスクリプトを追加せず、Markdownによる情報整理とAIレビューを優先します。

## Future Candidates

- `build_context.py`
  - `data/` のMarkdownを読み取り、AI投入用のまとめMarkdownを生成する
- `check_links.py`
  - `data/` や `README.md` のリンク切れを確認する
- `check_public_safety.py`
  - 公開repoに置くべきでない語句が含まれていないか簡易チェックする
- `generate_html_proposal.py`
  - `templates/html_patch_proposal.md` に沿ってHTML反映案を生成する

## Rules

- スクリプト名は English にする
- 既存ポートフォリオrepoを直接書き換える処理は初期段階では入れない
- 自動生成物は原則として `output/` に出す
- 個人情報や認証情報を読み込む処理は追加しない
