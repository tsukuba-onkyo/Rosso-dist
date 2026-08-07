# Rosso — 配布用リポジトリ

[Rosso](https://github.com/naozane26n1100629-gif/Rosso) デスクトップ版のインストーラを配布するためのリポジトリです。
**ソースコードは置いていません。**

## ダウンロード

[Releases](../../releases/latest) から環境に合ったものを取得してください。

| ファイル | 対象 |
|---|---|
| `Rosso_x.y.z_x64_en-US.msi` | Windows 64bit |
| `Rosso_x.y.z_x64-setup.exe` | Windows 64bit (インストーラ) |
| `Rosso_x.y.z_aarch64.dmg` | macOS (Apple Silicon) |

## 自動アップデート

アプリ内のアップデータがこのリポジトリの `latest.json` を参照します。
新しいバージョンが公開されると、起動時に更新を案内します。

## 署名について

現時点でインストーラにコード署名を行っていないため、初回起動時に
macOS では Gatekeeper、Windows では SmartScreen の警告が出ます。
