# DeckLoom v0.49.3 配布ファイル

Gradle Wrapperを8.14.4へ更新し、KotlinプラグインのGradle 8.13非推奨警告に対応しました。既存のAGP・Kotlin・KSP・JDK設定と、アプリのUI・DB処理・出典を維持します。

- `DeckLoom-v0.49.3-source.zip`: 最新Source一式。展開して `DeckLoom-v0.49.3` フォルダをAndroid Studioで開きます。
- `DeckLoom-v0.49.3-patch-from-v0.49.2.zip`: 前回納品した **v0.49.2 Source専用**の更新Patch。
- `SHA256SUMS-v0.49.3.txt`: 配布ZIPのSHA-256。

## GitHubからのダウンロード

対象ZIPのファイルページを開き、ダウンロードボタン（Download raw file）から保存してください。リポジトリ全体の「Code → Download ZIP」とは別です。

## Patchの適用

1. 前回のv0.49.2プロジェクトをバックアップし、実行中なら停止します。
2. Patchを展開し、ZIP直下のapp・gradle・gradlew・gradlew.bat・文書等を、元プロジェクトのsettings.gradle.ktsと同じ階層へ上書きします。
3. Android StudioのGradle JDKを17に設定してGradle Syncを実行します。初回はGradle 8.14.4のダウンロードに通信が必要です。
4. Clean Project後、従来と同じapplicationId・署名・端末へRunし、アプリ内READMEのv0.49.3を確認します。

元v0.49やv0.49.1へこのPatchを直接適用しないでください。最新Sourceを別フォルダへ展開するか、既存Patchを順番に適用してください。アンインストール・データ消去・DB再取得は不要です。

検証結果と未確認範囲はSource内のVALIDATION-v0.49.3.md、TODO.md、WEB_COLORS.mdに記載しています。WindowsのAndroid Studio実行、実機の描画・スクロール・ドラッグ・操作感はクラウドでは未確認です。
