# DeckLoom v0.49.5

タイル表示をサムネイル中心に戻し、カテゴリ切り替えのアニメーション、Web版を参考にした検索条件の整理、候補タブでのリストコピーを反映しました。versionCode 24、Room 8、検索DB schema 4。DB取得・日本語補完・更新・保存形式・出典は維持します。

- タイル：画像下の名前／タイプを外し、実枚数・選択・両面操作を保持。名前はリスト／詳細と画像なし時の代替表示に残します。
- カテゴリ：タップ／スワイプ切り替えに短いフェードと左右移動。
- 絞り込み：6項目の選択要約と開閉、折り返すチップ、日本語のレア度、選択済み項目の名前表示。全条件と保存済み検索を維持。
- コピー：候補表示時は候補全体を日本語／英語で出力。実枚数を保持し、メインを混ぜません。メイン／履歴と選択分コピーは従来どおりです。

## ダウンロード

- [Source一式](https://github.com/Shinji-a/Deck_room/raw/refs/heads/main/releases/v0.49.5/DeckLoom-v0.49.5-source.zip)
- [v0.49.4専用Patch](https://github.com/Shinji-a/Deck_room/raw/refs/heads/main/releases/v0.49.5/DeckLoom-v0.49.5-patch-from-v0.49.4.zip)
- [SHA-256](SHA256SUMS-v0.49.5.txt)

各ZIPのファイルページのDownload raw fileからも保存できます。

## Source版

ZIPを別フォルダへ展開し、DeckLoom-v0.49.5をAndroid Studioで開いてください。Gradle JDK 17・Android SDK 36・Wrapper 8.14.4を使用します。Gradle Sync → Clean Project → 従来と同じapplicationId・署名・端末へRunします。端末固有のSDK設定と署名キーは各自の環境を使ってください。

## Patch版

適用元は**前回納品のDeckLoom-v0.49.4-source.zip**だけです。元SourceのSHA-256は`89f8c56963b30b1a798ab220ea31ad5af022b769ecc1ef269787d32fa1f8e635`です。

1. v0.49.4プロジェクトをバックアップし、実行中なら停止します。
2. Patchを解凍し、**ZIP直下のapp・文書等を、元のsettings.gradle.ktsと同じ階層へ上書き**します。files等の中間フォルダはありません。
3. JDK 17でGradle Sync → Clean Project → 同じ署名・端末へRunし、アプリ内READMEのv0.49.5と保存データを確認します。

v0.49.3以前や異なる手修正版へ直接適用しないでください。適用元が違う場合は最新Sourceを使うか、対応する過去Patchを順番に適用します。アンインストール・データ消去・DB／画像パックの再取得は不要です。

## 検証と未確認項目

2026-10-13（日本時間）、クラウドでDebugビルド、JUnit61件（既存57＋コピー回帰4）、Room5テーブル／移行／FK、ICU 76の22正規表現とマナ抽出9ケースが成功しました。前版ZIPへ実際のPatchを適用し、Source全160ファイルとのバイト一致とCRCを確認。変更9・追加4・削除0です。

Lintは既存FullBackupContentエラー6件・警告31件・ヒント2件で失敗し、前版と全指摘が一致します。バックアップ仕様やLint抑制は変更していません。

実機のタイル表示、カテゴリの滑らかさ、条件の開閉／スクロール／キーボード、候補コピーの貼り付け、ドラッグと操作感、Windows Android Studioの新版Sync／Runは未確認です。README／TODO／PROJECT_STATEを更新し、ZIP内のRELEASE-v0.49.5.md・VALIDATION-v0.49.5.md・DESIGN_RULES.mdへ適用手順・検証・設計を記載しています。
