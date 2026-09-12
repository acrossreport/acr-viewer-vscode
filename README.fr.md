# ACR Viewer for VSCode

Une extension VS Code qui prévisualise et imprime des fichiers Markdown, texte brut et HTML.
Affiche le document en cours d'édition au format papier réel en temps réel et l'exporte en PDF.

[English version here](https://github.com/acrossreport/acr-viewer-vscode/blob/main/README.md)
[日本語版はこちら](https://github.com/acrossreport/acr-viewer-vscode/blob/main/README.ja.md)

## Fonctionnalités

- Prend en charge Markdown / texte brut (.txt) / HTML
- Aperçu précis au format papier réel, propulsé par le moteur Google Skia
- Mise à jour en direct sans besoin d'enregistrer
- Basculement portrait/paysage en un clic
- Export PDF
- Prise en charge correcte du repli de police CJK (japonais/chinois/coréen) dans les blocs de code (v0.0.2+)

## Installer depuis le Marketplace (recommandé)

[Installer ACR Report Viewer depuis le VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=across-systems.acr-viewer-vscode)

## Installation

1. Téléchargez le fichier `.vsix` correspondant à votre système depuis [Releases](https://github.com/acrossreport/acr-viewer-vscode/releases) :
   - Windows : `acr-viewer-vscode-win32-x64-X.X.X.vsix`
   - macOS (Apple Silicon) : `acr-viewer-vscode-darwin-arm64-X.X.X.vsix`
   - Linux : `acr-viewer-vscode-linux-x64-X.X.X.vsix`
2. Installez-le dans VSCode :

\`\`\`
code --install-extension acr-viewer-vscode-<votre-plateforme>-X.X.X.vsix
\`\`\`

## Plateformes prises en charge

- Windows
- macOS (Apple Silicon)
- Linux

## Raccourcis clavier

- `Ctrl+Alt+0` : Ouvrir l'aperçu avant impression
- `Ctrl+Alt+9` : Exporter en PDF

## En savoir plus

[ACR — Across Report Renderer](https://acrossreport.com/products/vscode)
