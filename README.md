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

## Installation

1. Download the `.vsix` file matching your OS from [Releases](https://github.com/acrossreport/acr-viewer-vscode/releases):
   - Windows: `acr-viewer-X.X.X-win32-x64.vsix`
   - macOS (Apple Silicon): `acr-viewer-X.X.X-darwin-arm64.vsix`
   - Linux: `acr-viewer-X.X.X-linux-x64.vsix`
2. Install it in VSCode:

\`\`\`
code --install-extension acr-viewer-X.X.X-<your-platform>.vsix
\`\`\`

## Supported platforms

- Windows
- macOS (Apple Silicon)
- Linux

## Keyboard shortcuts

- `Ctrl+Alt+0`: Open print preview
- `Ctrl+Alt+9`: Export as PDF

## Learn more

[ACR — Across Report Renderer](https://acrossreport.com/products/vscode)
