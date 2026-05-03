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

## Script Specifications

### `build_context.py`

- Input: `data/*.md`
- Output: `output/context/career_page_context.md`
- Purpose: AIレビューに渡すための情報を1つのMarkdownに集約する
- Initial behavior: ファイルを見出し付きで連結するだけに留める
- Do not: 既存ポートフォリオrepoを書き換えない

### `check_links.py`

- Input: `data/links.md`, `data/posts.md`, `README.md`
- Output: 標準出力または `output/reports/link_check.md`
- Purpose: 公開URLのリンク切れや `TODO` を確認する
- Initial behavior: `TODO` とURL一覧を抽出するだけでもよい
- Do not: ネットワーク確認ができない環境で失敗扱いにしない

### `check_public_safety.py`

- Input: `data/`, `docs/`, `README.md`
- Output: 標準出力または `output/reports/public_safety.md`
- Purpose: 公開repoに置くべきでない語句の混入を検出する
- Initial behavior: 禁止語句の単純検索でよい
- Do not: 検出結果だけで自動削除しない

### `generate_html_proposal.py`

- Input: `data/`, `templates/html_patch_proposal.md`
- Output: `output/proposals/*.md`
- Purpose: 既存HTMLに手動反映するための差し替え案を作る
- Initial behavior: Markdownの提案ファイル生成までに留める
- Do not: `C:\Users\lugep\デスクトップ\ProjectFolder\WebProject\PortfolioPage` を直接変更しない
