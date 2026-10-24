# media3-exoplayer-sandbox
Claude Codeを活用してAndroidのJetpack Media3 ExoPlayer実装を検証するためのテスト用リポジトリです。AI駆動開発による実装効率の検証と、Media3を用いたメディア再生機能の動作確認を行っています。

## 構成

| 項目 | バージョン |
| --- | --- |
| Android Gradle Plugin | 9.0.0（Kotlin組み込み） |
| Gradle | 9.1.0 |
| Jetpack Media3 | 1.8.0 |
| compileSdk / targetSdk | 36 |
| minSdk | 24 |

```
app/src/main/java/com/example/media3sandbox/MainActivity.kt  # ExoPlayer + PlayerView のサンプル
gradle/libs.versions.toml                                     # 依存バージョン管理（Version Catalog）
```

`MainActivity` は `onStart` でプレイヤーを生成し、`onStop` で再生位置を保持したうえで解放します。サンプルとしてHLSストリームを再生します。

## ビルド

Android Studio で本ディレクトリを開くか、コマンドラインで以下を実行します（JDK 17以上が必要）。

```bash
./gradlew assembleDebug
```
