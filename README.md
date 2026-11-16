# LityOS-Components

Dépôt public de distribution des releases de [LityOS](https://github.com/LityTech27/LityOS). Il ne contient pas de code : il sert à publier les fichiers téléchargés par l'application.

## Contenu

Les fichiers sont publiés dans les [releases](https://github.com/LityTech27/LityOS-Components/releases) :

- les APK de préversion `main-<sha7>` (canal preview) ;
- le runtime Linux `lityos-r1-rcN` (Ubuntu arm64 et bureau KDE Plasma) ;
- les packs complémentaires (`pack-<nom>-<hash>`) ;
- le pilote Turnip (`driver-turnip-v…`) ;
- `catalog.json`, le catalogue que l'application lit pour connaître les versions disponibles.

## Pourquoi ce dépôt est public

L'application LityOS télécharge son runtime, ses packs et ses mises à jour depuis les releases de ce dépôt, sans authentification (aucun jeton). Il doit donc rester public.

## `catalog.json`

Ce fichier est généré par la CI de LityOS. Ne le modifiez pas à la main : vos changements seraient écrasés et pourraient casser les mises à jour.

## Vérifier un téléchargement

- Chaque release contient un fichier `SHA256SUMS.txt` : comparez la somme SHA-256 du fichier téléchargé avec celle qui y figure (`sha256sum -c SHA256SUMS.txt`).
- Les notes d'une release d'APK indiquent l'empreinte du certificat de signature (ligne `Signer:`) ; comparez-la avec celle du certificat de l'APK.

## Licences

- **LityOS** est distribué sous licence **GNU GPL v3** : voir [LICENSE](LICENSE).
- Les **composants tiers** (Ubuntu, KDE, Mesa, proot, etc.) restent sous leurs propres licences : voir [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Code source

Où obtenir le code source correspondant à chaque release : voir [SOURCE.md](SOURCE.md).

## Marques

Les marques appartiennent à leurs propriétaires. LityOS n'est ni affilié ni approuvé par Canonical, Mozilla, Microsoft, GOG ou itch.io.

## Signaler un problème

Ouvrez une [issue](https://github.com/LityTech27/LityOS-Components/issues) sur ce dépôt.
