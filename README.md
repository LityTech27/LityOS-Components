# LityOS-Components

Dépôt public de distribution des releases de LityOS. Il ne contient pas de code : il sert à publier les fichiers téléchargés par l'application. Le dépôt de développement de LityOS n'est pas public ; le code source correspondant est fourni comme décrit dans [SOURCE.md](SOURCE.md).

## Contenu

Les fichiers sont publiés dans les [releases](https://github.com/LityTech27/LityOS-Components/releases) :

- les APK de préversion `main-<sha7>` (canal preview) ;
- le runtime Linux `lityos-r1-rcN` (Ubuntu arm64 et bureau KDE Plasma) ; seule la release `lityos-r1-rc5` est publique ;
- les packs complémentaires (`pack-<nom>-<hash>`) : proot, directaudio, tracking et butler ;
- le pilote Turnip (`driver-turnip-v…`) ;
- le miroir de dépendances de build msitools (paquets gcab et cabextract) ;
- `catalog.json`, le catalogue que l'application lit pour connaître les versions disponibles.

## Pourquoi ce dépôt est public

L'application LityOS télécharge son runtime, ses packs et ses mises à jour depuis les releases de ce dépôt, sans authentification (aucun jeton). Il doit donc rester public.

## `catalog.json`

Ce fichier est généré par la CI de LityOS. Ne le modifiez pas à la main : vos changements seraient écrasés et pourraient casser les mises à jour.

## Vérifier un téléchargement

**Intégrité** (le fichier n'est pas corrompu) :

- les releases d'APK `main-*` et le pilote Turnip contiennent un fichier `SHA256SUMS.txt` (`sha256sum -c SHA256SUMS.txt`) ;
- le runtime `lityos-r1-rcN` contient des fichiers `.sha256` ;
- pour les packs et le miroir msitools, la somme SHA-256 est indiquée dans les notes de la release.

**Authenticité des APK** : ces sommes et ces notes viennent du même dépôt que les fichiers ; elles prouvent l'intégrité, pas l'authenticité. Pour vérifier qu'un APK est signé par LityOS, comparez l'empreinte SHA-256 du certificat de signature avec celle-ci (également donnée dans les notes des releases `main-*`, ligne `Signer:`, et dans `catalog.json`) :

```
a768efdbe5be84fffc1bbc1b428ae2f0432ddaaf4d47ffa2cf896828a2b91ff1
```

Avec l'outil `apksigner` du SDK Android :

```
apksigner verify --print-certs -v LityOS-main-<sha7>.apk
```

Lisez le certificat du signataire du schéma v3 (Android 9 et plus). À vérifier : l'affichage exact d'`apksigner` sur un APK publié n'a pas été testé ici ; les anciens schémas v1/v2 peuvent faire apparaître une autre clé.

## Licences

- **LityOS** est distribué sous licence **GNU GPL v3** : voir [LICENSE](LICENSE).
- Les **composants tiers** (Ubuntu, KDE, Mesa, proot, etc.) restent sous leurs propres licences : voir [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Code source

Où obtenir le code source correspondant à chaque release : voir [SOURCE.md](SOURCE.md).

## Marques

Les marques appartiennent à leurs propriétaires. LityOS n'est ni affilié ni approuvé par Canonical, Mozilla, Google, KDE ou itch.io.

## Signaler un problème

Ouvrez une [issue](https://github.com/LityTech27/LityOS-Components/issues) sur ce dépôt.
