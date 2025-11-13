# Zettelkastenの運用ガイド

## ディレクトリとノート種別
- **PermanentNote** (`Zettelkasten/PermanentNote/`): 自分の言葉に再構成したアウトプット。`Main/` に領域別ハブを置き、それ以外は直下に保管。
- **LiteratureNote** (`Zettelkasten/LiteratureNote/`): 書籍・記事・イベントなど外部ソースの一次メモ。PermanentNoteから参照する。
- **FleetingNote** (`Zettelkasten/FleetingNote/`): 思いつきや下書きのインボックス。後でPermanent/Literatureへ昇格させる。
- **IndexNote** (`Zettelkasten/IndexNote/`): `00_Haru_Index` を起点に全ノート/タグ/テンプレートへジャンプできるグローバル目次。

## Daily & MEMO 連携
- `Daily/` : 日次のTODO、ログ、振り返り。完了したアイデアは対応する FleetingNote へリンクを貼る。
- `MEMO(Thino)/` : Thinoからエクスポートした一時メモの保管庫。レビュー時に FleetingNote へ昇格 or 破棄を判断。

## 添付ファイル
- 画像や動画は `Resources/Attachments/` に集約。ノート内では `![[ファイル名]]` で参照すれば移動してもリンクが切れない。
- `Resources/README.md` に保管方針を記載。

## テンプレート
- `Template/` に Permanent / Literature / Fleeting / Daily 用の雛形を保存。コマンドパレットから差し込む。

## タグ運用（新ルール）
- すべてのタグノートは `Tags/content/<slug>.md` に格納し、`aliases` で旧表記（例: 日本語名）を保持する。  
- タグ一覧は常に `Zettelkasten/IndexNote/00_Haru_Index.md` の「Tag Library」で公開する。

### 命名 & 設計ガイドライン
1. **小文字スラッグ統一**: タグIDは必ず小文字。日本語タグは ASCII スラッグ＋`aliases` で対応する。  
2. **スペース禁止**: 区切りはハイフン（-）、アンダースコア（_）、必要に応じスラッシュ（/）のみを使用。  
3. **内容タグのみ**: 状態/時間/場所などのメタタグは禁止。ノートの主題やトピックを表す内容タグだけを作成する。  
4. **単数形で表現**: `#habit` のように基本は単数形。集合を示す場合のみ例外可。  
5. **特殊文字の制限**: 絵文字や記号は禁止。日本語の句読点は除去し、必要ならハイフンで置換。  
6. **重複チェック**: 新規作成前に `Tags/content/` と IndexNote を検索し、同義タグがないか確認する。  
7. **定期見直し**: 毎月30日にタグクリーンアップを行い、不要タグを削除・統合する。  
8. **具体的かつ簡潔に**: 曖昧な名称（例: `#戦略`）は避け、 `#マーケティング戦略` のように具体化する。一般的に認知される略語のみ許容。  
9. **固有名詞は正式名称**: 人名・組織名・地名は正式名称をスラッグ化し、aliasに元表記を入れる。  
10. **タグ数の上限**: 1ノートあたり最大5タグ。複数タグを併用しても意味が重複しないようにする。  
11. **禁止タグ**: テンプレート見出しや日課（`todo`, `journal`, `study`, `exercise`, `routine` など）をタグとして使わない。

### 運用フロー
1. **作成**: 既存タグを確認し、必要なら `Tags/content/<slug>.md` を追加。Frontmatter に `tag`, `aliases`, `status`, `description` を記載する。  
2. **付与**: ノートには `#slug` を付け、必要に応じて Wikiリンク `[[Tags/content/slug]]` で詳細にジャンプできるようにする。  
3. **複数タグ**: 関連タグを最大5つまで併用し、多面的な検索性を確保する。  
4. **共有**: 新規タグを追加・削除したら `00_Haru_Index` の Tag Library を再生成してメンテする。  
5. **レビュー**: 毎週の振り返りでタグが正しく使われているかチェックし、月末にクリーンアップを実施する。
