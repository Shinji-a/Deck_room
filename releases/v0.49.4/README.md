# DeckLoom v0.49.4

現行Web版Deckroomのスマホ表示を基準に、Androidの色・文字・角丸・細い境界線・Outlinedアイコン・淡い選択状態を整理しました。検索の絞り込みと除外は下部シートへ集約。一人回しは盤面・手札と既存の操作を維持します。versionCode 23、Room 8、検索DB schema 4。DB取得・日本語補完・更新・保存形式・出典・依存は変更していません。

## ダウンロード

- [Source一式](https://github.com/Shinji-a/Deck_room/raw/refs/heads/main/releases/v0.49.4/DeckLoom-v0.49.4-source.zip)
- [v0.49.3用Patch](https://github.com/Shinji-a/Deck_room/raw/refs/heads/main/releases/v0.49.4/DeckLoom-v0.49.4-patch-from-v0.49.3.zip)
- [SHA-256](SHA256SUMS-v0.49.4.txt)

各ZIPのGitHubファイルページのDownload raw fileボタンからも保存できます。

## Source版

Source ZIPを別フォルダへ展開し、`DeckLoom-v0.49.4`をAndroid Studioで開いてください。Gradle JDK 17・Android SDK 36・Wrapper 8.14.4を利用します。Gradle Sync → Clean Project → 従来と同じapplicationId・署名・端末へRunします。端末固有のlocal.propertiesと署名キーは各自の環境を利用してください。

## Patch版

適用元は**前回納品のDeckLoom-v0.49.3-source.zip**だけです。元SourceのSHA-256は`b626d7f816edb228d4fdc06f0a97c221bcf5d043d508b255ff574eb372f183f6`です。

1. v0.49.3プロジェクトをバックアップし、実行中なら停止します。
2. Patch ZIPを解凍し、**直下のapp・文書等を、元のsettings.gradle.ktsと同じ階層へ上書き**します。files等の中間フォルダはありません。
3. JDK 17でGradle Sync → Clean Project → 同じ署名・端末へRunし、アプリ内READMEのv0.49.4と保存データを確認します。

v0.49.2以前や異なる手修正版へ直接適用しないでください。適用元が違う場合は最新Sourceを利用するか、対応する過去Patchを順番に適用します。アプリのアンインストール・データ消去・検索DB／画像パックの再取得は不要です。

## 検証と未確認項目

2026-10-10、クラウドのDebugビルド、既存JUnit57件、Roomの5テーブル／移行／FK、ICU 76の22正規表現とマナ抽出9ケースが成功しました。採用HEX 35色を現行WebのCSSと照合し、主要文字色22組の静的コントラストは4.5:1以上です。

Lintは既存のFullBackupContentエラー6件・警告31件・ヒント2件で失敗し、前版と全指摘が一致します。抑制やバックアップ仕様の変更はしていません。実際のv0.49.3 ZIPにPatchを適用し、Source全156ファイルとのバイト一致とZIPのCRCを確認しました。変更20・追加5・削除0ファイル。

Android実機／エミュレーターの見た目・スクロール・ドラッグ・操作感、ユーザーのWindows Android Studioでの新版Sync／Runは未確認です。現行Web専用エラー画面とダーク表示の確認も残ります。

ZIP内のREADME・TODO・PROJECT_STATEを更新しました。DESIGN_RULES.mdに共通スタイルとWeb参照の根拠、WEB_COLORS.mdに色の根拠と未確認範囲、RELEASE-v0.49.4.mdに適用手順、VALIDATION-v0.49.4.mdに検証結果を記載しています。SDK・ビルド生成物・キャッシュ・署名キー・過去の配布ZIPはSourceに含みません。
