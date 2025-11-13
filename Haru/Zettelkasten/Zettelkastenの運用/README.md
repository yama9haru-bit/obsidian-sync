# Zettelkastenの運用ガイド

## ノート種別
- **PermanentNote**: `Zettelkasten/PermanentNote/` 配下。概念や自分の言葉で再構成したアウトプットのみを置く。`Main/` には領域ごとの定常ノートをまとめ、それ以外は個別ファイルとして直下に配置。
- **LiteratureNote**: `Zettelkasten/LiteratureNote/`。本・イベント・人物メモなど外部リソース由来の一次記録を集約し、PermanentNoteから参照する。
- **FleetingNote**: `Zettelkasten/FleetingNote/`。思いつきや下書き、Thinoに移す前の断片をいったん受け止めるインボックス。
- **IndexNote**: `Zettelkasten/IndexNote/`。`00_Haru_Index` を起点にタグ、ノート、テンプレートへジャンプできるよう再配線済み。

## Daily & MEMO連携
- `Daily/` で日次の進捗とTODOを管理し、必要になった FleetingNote へリンクを付ける。
- Thinoで書いたメモは `MEMO(Thino)/` にエクスポートしておき、後から FleetingNote へ昇格させるか削除するかを判断する。

## 添付ファイル
- すべて `Resources/Attachments/` にまとまっている。ファイル名のみで参照できるため、ノートを移動してもリンク切れしない。

## タグ運用
- タグノートは `Tags/` に移動済み。タグルールを Cursor に読み込んで自動生成した結果も同じ場所で管理する。

## テンプレート
- `Template/` に Permanent / Literature / Fleeting / Daily 用の雛形を格納。新規ノート作成時はコマンドパレットからテンプレートを差し込む。
