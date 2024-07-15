Voici le texte modifié sans la partie retirée :

```markdown
<p align="center">
  <img width="160" src="./website/static/readme/NextusOs.png" />
  <p align="center">🚀 Alimentez Votre Monde avec l'IA - Explorez, Élargissez, Donnez du Pouvoir.</p>
</p>

[![Téléchargements de NextusOs](https://img.shields.io/github/downloads/NextusOfficiel/NextusOs/total.svg?style=flat)](https://github.com/NextusOfficiel/NextusOs/releases) [![NextusOs](https://img.shields.io/badge/NextusOs-discord-blue?style=flat&logo=discord&logoColor=f2f0ea)](https://discord.gg/kq2HXcpJSQ)

<a href="https://www.buymeacoffee.com/NextusOfficiel" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Coffee" style="height: 40px !important;width: 145px !important;"></a>

## Fonctionnalités

Présentation de NextusOs : un navigateur personnalisé amélioré par l'IA conçu pour simplifier votre expérience numérique :

- **Navigateur** : NextusOs inclut non seulement des sites web d'IA sélectionnés, mais permet également l'ajout de n'importe quelle URL, offrant une expérience de navigation personnalisée ([Configurations NextusOs](./configs)).
- **Gestion des Prompts** : Offre des options de personnalisation robustes, y compris l'ajout, la synchronisation, le marquage en lot et la suppression des prompts.
- **NextusOs Ask** : Permet d'envoyer des messages en lot à plusieurs chats d'IA, simplifiant ainsi le processus d'interaction avec divers services d'IA simultanément ([Extensions NextusOs](./extensions)). Les entrées faites via NextusOs Ask sont stockées localement, garantissant un accès facile pour une future consultation ou un bookmarking.
- **Thèmes** : `Clair`/`Sombre`/`Système`/`Monochromatique`/`Texture Givrée`
- **Mode Cache NextusOs** : NextusOs réinvente l'interaction sans le concept traditionnel des onglets du navigateur. Dans ce mode, les liens accessibles via la barre latérale sont mis en cache pour un échange rapide (accessible via `Menu -> Paramètres -> Mode Cache NextusOs`).
- **Isolation des Données de Cookies** : Supporte l'utilisation de plusieurs comptes sur le même site web, répondant aux besoins divers des utilisateurs.
- **Découvrez Plus** : De nombreux détails attendent votre découverte...

## Installation

[🕒 Versions précédentes...](https://github.com/NextusOfficiel/NextusOs/releases)

- **macOS**
  - [⬇️ x64](https://github.com/NextusOfficiel/NextusOs/releases/download/v0.4.0/NextusOs_macos_0.4.0.dmg)
  - [⬇️ arm64](https://github.com/NextusOfficiel/NextusOs/releases/download/v0.4.0/NextusOs_macos_0.4.0-arm64.dmg)
- **Windows**
  - [⬇️ x64](https://github.com/NextusOfficiel/NextusOs/releases/download/v0.4.0/NextusOs-win32-x64-0.4.0-setup.exe)
- **Linux**
  - [⬇️ AppImage](https://github.com/NextusOfficiel/NextusOs/releases/download/v0.4.0/NextusOs_linux_0.4.0.AppImage)
  - [⬇️ amd64.deb](https://github.com/NextusOfficiel/NextusOs/releases/download/v0.4.0/NextusOs_linux_amd64_0.4.0.deb)

|Aperçu|Aperçu|
|---|---|
|![theme-dark-1](./website/static/readme/NextusOs-theme-dark-1.png)|![theme-dark-2](./website/static/readme/NextusOs-theme-dark-2.png)|
|![theme-light-1](./website/static/readme/NextusOs-theme-light-1.png)|![theme-light-2](./website/static/readme/NextusOs-theme-light-2.png)|
|![NextusOs-settings](./website/static/readme/NextusOs-settings.png)|![NextusOs-prompts](./website/static/readme/NextusOs-prompts.png)|

## Configurations NextusOs

[📁 configs](./configs)

### Mode NextusOs

Pour configurer un lien de synchronisation personnalisé, suivez les étapes ci-dessous :

- **Étape 1** : Ouvrez les paramètres (sur macOS : `cmd`+`,`, sur Windows : `ctrl`+`,`)
- **Étape 2** : Modifiez l'URL dans `Mode Sync`
- **Étape 3** ou **Étape 4** : Cliquez sur le bouton `sync` pour commencer à synchroniser les données

> [!NOTE]
> L'`URL personnalisée` ne sera pas écrasée. Si vous souhaitez utiliser votre propre URL comme source de données, veuillez vous référer au format des données dans `NextusOs.mode.json`.

![Mode Sync](./website/static/configs/NextusOs-mode-sync.png)

#### URL de Synchronisation

- [AI](./NextusOs.mode.json) : Sites web d'IA populaires et communautés (ex : ChatGPT, Bard, Claude, Poe, etc.).

  ```bash
  https://raw.githubusercontent.com/NextusOfficiel/NextusOs/main/configs/NextusOs.mode.json
  ```

#### NextusOs.mode.json

Voici une description détaillée de certains champs :

- `name` : Nom (optionnel, sans signification particulière)
- `version` : Changement de version
- `sync` : Informations URL (optionnel, sans signification particulière)
- `modes[]` :
  - `id` : Identifiant unique (utilisez une chaîne de caractères aléatoire ; n'utilisez pas de formats comme `NextusOs:xxx` ou `NextusOs@xxx` car ils sont réservés à un usage interne dans NextusOs)
  - `parent` : Le dossier parent auquel cet élément appartient (supporte l'imbrication)
  - `text` : Nom
  - `url` : Lien
  - `dir` : Indique s'il s'agit d'un dossier (par défaut `false`)

### Proxy

En savoir plus : [electronjs/docs](https://www.electronjs.org/docs/latest/api/session#sessetproxyconfig)

- `proxyRules` : Règles indiquant quels proxies utiliser.
- `proxyBypassRules` : Règles indiquant quelles URLs doivent contourner les paramètres de proxy.

## Extensions NextusOs

[📁 extensions](./extensions)

Notez que NextusOs ne prend pas en charge l'ensemble des APIs d'extensions Chrome. Consultez les APIs d'extensions prises en charge pour plus de détails sur ce qui est supporté.

En savoir plus : [electronjs/doc](https://www.electronjs.org/docs/latest/api/extensions)

<!-- EXTENSIONS_START -->
| Nom | Version | Description |
| --- | --- | --- |
| [@NextusOs/ask](https://github.com/NextusOfficiel/NextusOs/tree/main/extensions/NextusOs-ask) | 0.1.7 | Le meilleur assistant pour poser des questions en lot et taper rapidement des prompts. |
| [@NextusOs/ask-custom](https://github.com/NextusOfficiel/NextusOs/tree/main/extensions/NextusOs-ask-custom) | 0.1.0 | Le meilleur assistant pour poser des questions en lot et taper rapidement des prompts. |
| [@NextusOs/export-chatgpt](https://github.com/NextusOfficiel/NextusOs/tree/main/extensions/NextusOs-export-chatgpt) | 0.1.0 | Exportation de l'historique de chat ChatGPT, prend en charge les formats PDF, Image et Markdown. |
| [@NextusOs/reset](https://github.com/NextusOfficiel/NextusOs/tree/main/extensions/NextusOs-reset) | 0.1.0 | Réinitialiser certains styles de site web pour améliorer la compatibilité avec NextusOs. |
<!-- EXTENSIONS_END -->

[🔗 Voir les extensions NextusOs](./extensions)

**Extensions en plein essor**
