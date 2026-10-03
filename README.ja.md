# ACR Viewer for VSCode

VSCode拡張機能として動作するMarkdown・テキスト・HTMLの印刷プレビューツールです。
編集中のドキュメントを実際の用紙サイズでリアルタイムにレンダリングし、PDFとして出力できます。

[English version here](https://github.com/acrossreport/acr-viewer-vscode/blob/main/README.md) | [Version française ici](https://github.com/acrossreport/acr-viewer-vscode/blob/main/README.fr.md)

## 特徴

- Markdown / テキスト(.txt) / HTMLに対応
- Google Skiaエンジンによる正確な用紙サイズプレビュー
- 保存不要のライブ更新
- ワンクリックで縦横切替
- PDF出力対応
- コードブロック内の日本語・中国語・韓国語フォントの正しいフォールバック表示に対応（v0.0.2〜）
- Mermaid diagram rendering (flowchart, sequenceDiagram) via a pure-Rust pipeline — no headless Chromium required (v0.0.4+)
- Page numbers in PDF footer (v0.0.4+)
- Cursor (VS Code fork) compatibility confirmed (v0.0.4+)
- ソースコードの印刷に対応 (v0.0.5+)
- テンプレート定義(.json)のデザイン表示 (v0.0.6+)
- データJSONを結合したプレビュー(ページ送り付き) (v0.0.6+)
- 表示結果のPNG/PDF保存 (v0.0.6+)
- 表示言語の選択(English / 日本語 / Français) (v0.0.6+)
- Intel Mac(darwin-x64)対応 (v0.0.6+)
- Windows(ARM64)・Linux(ARM64)対応 (v0.0.8+)
- 「PNG保存」で、全ページを1つのZIPファイルに保存(ACR-PNG-PACKAGE: `manifest.json` + `pages/001.png` …、ACR CLIと同じ形式) (v0.0.8+)
- ACR PNGビューア: 保存したZIPを、保存後の通知の「ビューアで開く」からページ送りで表示 (v0.0.8+)

## インストール（推奨）

- **VS Code**: [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=across-systems.acr-viewer-vscode)
- **Cursor / VSCodium などのフォーク**: [Open VSX Registry](https://open-vsx.org/extension/across-systems/acr-viewer-vscode)

## インストール方法

1. [Releases](https://github.com/acrossreport/acr-viewer-vscode/releases) からお使いのOSに対応する `.vsix` をダウンロード
   - Windows (x64): `acr-viewer-vscode-win32-x64-X.X.X.vsix`
   - Windows (ARM64): `acr-viewer-vscode-win32-arm64-X.X.X.vsix`
   - macOS (Apple Silicon): `acr-viewer-vscode-darwin-arm64-X.X.X.vsix`
   - macOS (Intel): `acr-viewer-vscode-darwin-x64-X.X.X.vsix`
   - Linux (x64): `acr-viewer-vscode-linux-x64-X.X.X.vsix`
   - Linux (ARM64): `acr-viewer-vscode-linux-arm64-X.X.X.vsix`
2. VSCodeで以下を実行:

```
code --install-extension acr-viewer-vscode-<お使いのOS名>-X.X.X.vsix
```

## 対応OS

- Windows (x64 / ARM64)
- macOS (Apple Silicon)
- macOS (Intel)
- Linux (x64 / ARM64)

WindowsとLinuxのARM64版は、v0.0.8から提供しています。

> **Linuxをお使いの方へ:** Snap版のVS Codeは、サンドボックス化されたglibcのバージョンがACRのネイティブレンダリングモジュールと非互換のため非対応です。公式の`.deb`/`.rpm`版、またはCursorをご利用ください。v0.0.8からは、Snap版を検出すると、黙って失敗せずにこの旨のメッセージを表示します。


## ショートカット

- `Ctrl+Alt+0`: 印刷プレビューを開く
- `Ctrl+Alt+9`: PDFとして出力
- `Ctrl+Alt+8`: テンプレートのデザイン表示
- `Ctrl+Alt+7`: データ結合プレビュー

## ACR PNGビューア（v0.0.8〜）

データ結合プレビューの「PNG保存」は、1つのZIPファイル(ACR-PNG-PACKAGE)で保存します。保存後の通知で「ビューアで開く」を選ぶと、VS Codeの中でページを表示できます。

ビューアは1つのHTMLファイル(拡張機能の中の `resources/viewer/acr-zip-viewer.html`)で、ブラウザ単体でも使えます。HTMLファイルを開いて「ZIPを開く」でZIPを選ぶか、ZIPを画面にドラッグしてください。外部ライブラリやネット接続は使いません。ACR CLIで作ったZIPも、同じように表示できます。

## 詳細情報

[ACR — Across Report Renderer](https://acrossreport.com/products/vscode)

