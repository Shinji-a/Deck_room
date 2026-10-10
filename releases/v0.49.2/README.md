# DeckLoom v0.49.2 配布ファイル

- `DeckLoom-v0.49.2-source.zip`: 最新Source一式。展開して `DeckLoom-v0.49.2` フォルダをAndroid Studioで開きます。
- `DeckLoom-v0.49.2-patch-from-v0.49.1.zip`: 前回納品した **v0.49.1 Source専用**の更新Patch。
- `SHA256SUMS-v0.49.2.txt`: 配布ZIPのSHA-256。

## GitHubからのダウンロード

対象ZIPのファイルページを開き、ダウンロードボタン（Download raw file）から保存してください。リポジトリ全体の「Code → Download ZIP」とは別です。

## Patchの適用

1. 前回のv0.49.1プロジェクトをバックアップし、実行中のアプリを停止します。
2. Patchを展開し、ZIP直下のapp・文書等を、元プロジェクトのsettings.gradle.ktsと同じ階層へ上書きします。
3. Gradle Sync、Clean Projectを行い、従来と同じapplicationId・署名で更新します。

元v0.49へこのPatchを直接適用しないでください。最新Sourceを別フォルダへ展開するか、先にv0.49.1へのPatchを適用する必要があります。アンインストール・データ消去・DB再取得は不要です。

## 検証と確認範囲

SourceとPatchのZIP整合性、元v0.49.1へPatchを適用した結果と最新Source全149ファイルの一致を検証済みです。Gradleビルドと57件の単体テストは成功しています。Lintは元版と同じ既存エラー6件が残り、実機の描画・スクロール・ドラッグ・操作感は未確認です。詳しくはSource内のRELEASE-v0.49.2.md、VALIDATION-v0.49.2.md、TODO.md、WEB_COLORS.mdを参照してください。
