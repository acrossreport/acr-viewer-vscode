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
- Rendu des diagrammes Mermaid (flowchart, sequenceDiagram) via un pipeline entièrement en Rust — sans Chromium headless (v0.0.4+)
- Numéros de page dans le pied de page du PDF (v0.0.4+)
- Compatibilité confirmée avec Cursor (fork de VS Code) (v0.0.4+)
- Impression du code source (v0.0.5+)
- Affichage de la définition de modèle ACR (v0.0.6+)
- Aperçu avec fusion de données, page par page (v0.0.6+)
- Enregistrement du rendu en PNG ou PDF (v0.0.6+)
- Choix de la langue de l'interface (v0.0.6+)
- Prise en charge des Mac Intel (darwin-x64) (v0.0.6+)
- Prise en charge de Windows (ARM64) et Linux (ARM64) (v0.0.8+)
- « Enregistrer PNG » enregistre toutes les pages dans un seul fichier ZIP (ACR-PNG-PACKAGE : `manifest.json` + `pages/001.png` …), le même format que ACR CLI (v0.0.8+)
- Visionneuse PNG ACR : affiche le ZIP enregistré page par page, depuis la notification après l'enregistrement (« Ouvrir dans la visionneuse ») (v0.0.8+)

## Installer depuis un registre (recommandé)

- **VS Code** : [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=across-systems.acr-viewer-vscode)
- **Cursor / VSCodium / autres forks** : [Open VSX Registry](https://open-vsx.org/extension/across-systems/acr-viewer-vscode)

## Installation

1. Téléchargez le fichier `.vsix` correspondant à votre système depuis [Releases](https://github.com/acrossreport/acr-viewer-vscode/releases) :
   - Windows (x64) : `acr-viewer-vscode-win32-x64-X.X.X.vsix`
   - Windows (ARM64) : `acr-viewer-vscode-win32-arm64-X.X.X.vsix`
   - macOS (Apple Silicon) : `acr-viewer-vscode-darwin-arm64-X.X.X.vsix`
   - macOS (Intel) : `acr-viewer-vscode-darwin-x64-X.X.X.vsix`
   - Linux (x64) : `acr-viewer-vscode-linux-x64-X.X.X.vsix`
   - Linux (ARM64) : `acr-viewer-vscode-linux-arm64-X.X.X.vsix`
2. Installez-le dans VSCode :

```
code --install-extension acr-viewer-vscode-<votre-plateforme>-X.X.X.vsix
```

## Plateformes prises en charge

- Windows (x64 / ARM64)
- macOS (Apple Silicon)
- macOS (Intel)
- Linux (x64 / ARM64)

Les versions ARM64 pour Windows et Linux sont disponibles à partir de la v0.0.8.

> **Utilisateurs Linux :** La version Snap de VS Code n'est pas prise en charge, car sa version de glibc en sandbox est incompatible avec le module de rendu natif d'ACR. Veuillez utiliser la version officielle `.deb`/`.rpm`, ou Cursor. À partir de la v0.0.8, l'extension détecte la version Snap et affiche ce message au lieu d'échouer sans explication.

## Raccourcis clavier

- `Ctrl+Alt+0` : Ouvrir l'aperçu avant impression
- `Ctrl+Alt+9` : Exporter en PDF
- `Ctrl+Alt+8` : Affichage du modèle
- `Ctrl+Alt+7` : Aperçu avec fusion de données

## Visionneuse PNG ACR (v0.0.8+)

Dans l'aperçu avec fusion de données, « Enregistrer PNG » enregistre un seul fichier ZIP (ACR-PNG-PACKAGE). Après l'enregistrement, choisissez « Ouvrir dans la visionneuse » pour afficher les pages dans VS Code.

La visionneuse est un seul fichier HTML (`resources/viewer/acr-zip-viewer.html` dans l'extension) qui fonctionne aussi seul dans un navigateur : ouvrez le fichier HTML et choisissez un ZIP avec « Ouvrir un ZIP », ou déposez le ZIP sur la page. Elle n'utilise aucune bibliothèque externe et ne nécessite aucune connexion réseau. Les ZIP créés par ACR CLI s'affichent de la même façon.

## En savoir plus

[ACR — Across Report Renderer](https://acrossreport.com/products/vscode)
