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

## Install (recommended)

- **VS Code**: [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=across-systems.acr-viewer-vscode)
- **Cursor / VSCodium / other VS Code forks**: [Open VSX Registry](https://open-vsx.org/extension/across-systems/acr-viewer-vscode)

## Installation

1. Download the `.vsix` file matching your OS from [Releases](https://github.com/acrossreport/acr-viewer-vscode/releases):
   - Windows: `acr-viewer-vscode-win32-x64-X.X.X.vsix`
   - macOS (Apple Silicon): `acr-viewer-vscode-darwin-arm64-X.X.X.vsix`
   - Linux: `acr-viewer-vscode-linux-x64-X.X.X.vsix`
2. Install it in VSCode:

\`\`\`
code --install-extension acr-viewer-vscode-<your-platform>-X.X.X.vsix
\`\`\`

## Supported platforms

- Windows
- macOS (Apple Silicon)
- Linux

> **Linux users:** The Snap-packaged build of VS Code is not supported due to its sandboxed glibc version, which is incompatible with ACR's native rendering module. Please use the official `.deb`/`.rpm` build, or Cursor.
## Keyboard shortcuts

- `Ctrl+Alt+0`: Open print preview
- `Ctrl+Alt+9`: Export as PDF

## Learn more

[ACR — Across Report Renderer](https://acrossreport.com/products/vscode)
