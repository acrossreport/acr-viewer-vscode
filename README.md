# ACR Viewer for VSCode

A VS Code extension that previews and prints Markdown, plain text, and HTML.
Renders the document you are editing at true paper size in real time, and exports it as PDF.

[日本語版はこちら](https://github.com/acrossreport/acr-viewer-vscode/blob/main/README.ja.md) | [Version française ici](https://github.com/acrossreport/acr-viewer-vscode/blob/main/README.fr.md)

## Features

- Supports Markdown / plain text (.txt) / HTML
- Accurate print-size preview powered by the Google Skia engine
- Live preview updates with no save required
- One-click paper orientation toggle
- PDF export
- Proper CJK (Japanese/Chinese/Korean) font fallback in code blocks (v0.0.2+)
- Mermaid diagram rendering (flowchart, sequenceDiagram) via a pure-Rust pipeline — no headless Chromium required (v0.0.4+)
- Page numbers in PDF footer (v0.0.4+)
- Cursor (VS Code fork) compatibility confirmed (v0.0.4+)
- Source code printing support (v0.0.5+)
- Template design view: display an ACR template definition (.json) directly in VS Code (v0.0.6+)
- Data-merge preview: bind a data JSON to a template and preview the result page by page (v0.0.6+)
- Save the rendered result as PNG or PDF (v0.0.6+)
- UI language selection: English / 日本語 / Français (v0.0.6+)
- Intel Mac (darwin-x64) support (v0.0.6+)
- Windows (ARM64) and Linux (ARM64) support (v0.0.8+)
- "Save PNG" saves all pages as one ZIP file (ACR-PNG-PACKAGE: `manifest.json` + `pages/001.png` …), the same format as ACR CLI (v0.0.8+)
- ACR PNG Viewer: view the saved ZIP page by page, from the notification after saving ("Open in viewer") (v0.0.8+)

## Install (recommended)

- **VS Code**: [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=across-systems.acr-viewer-vscode)
- **Cursor / VSCodium / other VS Code forks**: [Open VSX Registry](https://open-vsx.org/extension/across-systems/acr-viewer-vscode)

## Installation

1. Download the `.vsix` file matching your OS from [Releases](https://github.com/acrossreport/acr-viewer-vscode/releases):
   - Windows (x64): `acr-viewer-vscode-win32-x64-X.X.X.vsix`
   - Windows (ARM64): `acr-viewer-vscode-win32-arm64-X.X.X.vsix`
   - macOS (Apple Silicon): `acr-viewer-vscode-darwin-arm64-X.X.X.vsix`
   - macOS (Intel): `acr-viewer-vscode-darwin-x64-X.X.X.vsix`
   - Linux (x64): `acr-viewer-vscode-linux-x64-X.X.X.vsix`
   - Linux (ARM64): `acr-viewer-vscode-linux-arm64-X.X.X.vsix`
2. Install it in VSCode:

```
code --install-extension acr-viewer-vscode-<your-platform>-X.X.X.vsix
```

## Supported platforms

- Windows (x64 / ARM64)
- macOS (Apple Silicon)
- macOS (Intel)
- Linux (x64 / ARM64)

ARM64 builds for Windows and Linux are available from v0.0.8.

> **Linux users:** The Snap-packaged build of VS Code is not supported due to its sandboxed glibc version, which is incompatible with ACR's native rendering module. Please use the official `.deb`/`.rpm` build, or Cursor. From v0.0.8, the extension detects the Snap build and shows this message instead of failing silently.

## Keyboard shortcuts

- `Ctrl+Alt+0`: Open print preview
- `Ctrl+Alt+9`: Export as PDF
- `Ctrl+Alt+8`: Template design view
- `Ctrl+Alt+7`: Data-merge preview

## ACR PNG Viewer (v0.0.8+)

"Save PNG" in the data-merge preview saves one ZIP file (ACR-PNG-PACKAGE). After saving, choose "Open in viewer" to see the pages in VS Code.

The viewer is a single HTML file (`resources/viewer/acr-zip-viewer.html` inside the extension) that also works on its own in a web browser: open the HTML file and choose a ZIP with "Open ZIP", or drop the ZIP onto the page. It uses no external libraries and needs no network connection. ZIP files made by ACR CLI can be viewed the same way.

## Learn more

[ACR — Across Report Renderer](https://acrossreport.com/products/vscode)
