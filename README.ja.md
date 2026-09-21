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
- - Mermaid diagram rendering (flowchart, sequenceDiagram) via a pure-Rust pipeline — no headless Chromium required (v0.0.4+)
- Page numbers in PDF footer (v0.0.4+)
- Cursor (VS Code fork) compatibility confirmed (v0.0.4+)

## Marketplaceからインストール（推奨）
- **VS Code**: [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=across-systems.acr-viewer-vscode)
- **Cursor / VSCodium などのフォーク**: [Open VSX Registry](https://open-vsx.org/extension/across-systems/acr-viewer-vscode)

## インストール方法

1. [Releases](https://github.com/acrossreport/acr-viewer-vscode/releases) からお使いのOSに対応する `.vsix` をダウンロード
   - Windows: `acr-viewer-vscode-win32-x64-X.X.X.vsix`
   - macOS (Apple Silicon): `acr-viewer-vscode-darwin-arm64-X.X.X.vsix`
   - Linux: `acr-viewer-vscode-linux-x64-X.X.X.vsix`
2. VSCodeで以下を実行:

\`\`\`
code --install-extension acr-viewer-vscode-<お使いのOS名>-X.X.X.vsix
\`\`\`

## 対応OS

- Windows
- macOS (Apple Silicon)
- Linux

> **Linuxをお使いの方へ:** Snap版のVS Codeは、サンドボックス化されたglibcのバージョンがACRのネイティブレンダリングモジュールと非互換のため非対応です。公式の`.deb`/`.rpm`版、またはCursorをご利用ください。


## ショートカット

- `Ctrl+Alt+0`: 印刷プレビューを開く
- `Ctrl+Alt+9`: PDFとして出力

## 詳細情報

[ACR — Across Report Renderer](https://acrossreport.com/products/vscode)
