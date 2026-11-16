# Mentions des composants tiers

Ce fichier liste les composants distribués dans les releases de ce dépôt, avec leur auteur ou projet amont, leur licence (identifiant [SPDX](https://spdx.org/licenses/)) et un lien vers la source. Chaque composant reste sous sa propre licence.

Les mentions « à confirmer » signalent une information non vérifiée à ce jour. Le code source correspondant à LityOS et les correctifs LityOS sont décrits dans [SOURCE.md](SOURCE.md). Le texte de la GPL v3 de LityOS est dans [LICENSE](LICENSE).

## Récapitulatif

| Composant | Version | Licence (SPDX) |
| --- | --- | --- |
| LityOS | selon la release | `GPL-3.0` (dérivé de DroidDeck 0.6.9) |
| DD-Turnip / Mesa | v0.3.4 | `MIT` (Mesa), correctifs `GPL-3.0` |
| Ubuntu et Kubuntu / KDE Plasma | 26.04 | selon chaque paquet |
| KWin, Mesa, Quickshell (paquets `+lityos1`) | 6.6.6, 26.0.8, 0.3.0 | `GPL-2.0-or-later`, `MIT` et autres, `LGPL-3.0` |
| Firefox | à confirmer | `MPL-2.0` |
| proot / talloc | commit `4dba3afb…` / 2.4.3 | `GPL-2.0-or-later` / `LGPL-3.0-or-later` |
| directaudio | `directaudio-linux-v1.1.0` | `LGPL-2.1-or-later` |
| OpenCV / MediaPipe / modèles Google | 4.13.0 / 1.0.0 | `Apache-2.0` (modèles : à confirmer) |
| butler / 7-Zip (c7zip) | 15.32.0 / à confirmer | `MIT` / `LGPL-2.1-or-later` (+ restriction unRAR) |
| msitools : gcab / cabextract | 1.6 / 1.11 | `LGPL-2.1-or-later` / `GPL-3.0-or-later` |

## LityOS

- Licence : [GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html) (voir [LICENSE](LICENSE)).
- Dérivé de **DroidDeck 0.6.9** (projet [Droid-Deck/DroidDeck](https://github.com/Droid-Deck/DroidDeck), GPL-3.0), commit de départ `0a07926ef3477c90db911d169904137cfc5e2505`.
- Source : [LityTech27/LityOS](https://github.com/LityTech27/LityOS) ; source correspondante de chaque release : voir [SOURCE.md](SOURCE.md).
- Les bibliothèques embarquées dans l'APK (par exemple MediaPipe, OpenCV) ont leurs propres licences ; un inventaire détaillé de leurs textes est à confirmer.

## Pilote DD-Turnip v0.3.4 / Mesa

- Projet amont : DroidDeck ([Droid-Deck/Drivers-CI](https://github.com/Droid-Deck/Drivers-CI), release `DD-Turnip-v0.3.4`), construit à partir de Mesa 27.0.0-devel (commit `e2ab6687d5ad…`) avec des correctifs DroidDeck.
- Licences : Mesa [`MIT`](https://spdx.org/licenses/MIT.html) (avec des exceptions par fichier) ; correctifs et pilotes [`GPL-3.0`](https://www.gnu.org/licenses/gpl-3.0.html).
- Source : l'archive `DD-Turnip-v0.3.4-source.tar.xz` et le fichier `DD-Turnip-NOTICE.md` sont joints à la release `driver-turnip-v0.3.4` ; projet Mesa : <https://www.mesa3d.org/>.

## Ubuntu 26.04 (runtime arm64) et Kubuntu / KDE Plasma (bureau)

- Projet amont : [Ubuntu](https://ubuntu.com/) (Canonical Ltd) et ses paquets ; bureau Kubuntu / KDE Plasma 6.6.x.
- Licences : celles de chaque paquet (GPL, LGPL, MIT, BSD, etc.), dont le texte est dans `/usr/share/doc/<paquet>/copyright` de l'image.
- Liste exacte des paquets et versions : fichiers `*.packages.txt` joints aux releases `lityos-r1-rcN`.
- Source : archive Ubuntu, <https://archive.ubuntu.com/ubuntu/> (par exemple `apt source <paquet>`).
- « Ubuntu » et « Kubuntu » sont des marques de Canonical Ltd. LityOS n'est pas Ubuntu et n'est pas affilié à Canonical.

## Paquets modifiés `+lityos1`

Paquets source Ubuntu recompilés avec des correctifs LityOS ; les correctifs figurent dans l'archive de source jointe à la release (voir [SOURCE.md](SOURCE.md)).

| Paquet | Version | Licence (SPDX) | Source amont |
| --- | --- | --- | --- |
| KWin | 6.6.6 | [`GPL-2.0-or-later`](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html) | <https://invent.kde.org/plasma/kwin> et archive Ubuntu |
| Mesa | 26.0.8 | [`MIT`](https://spdx.org/licenses/MIT.html) et autres licences listées dans `debian/copyright` | <https://www.mesa3d.org/> et archive Ubuntu |
| Quickshell | 0.3.0 (`0.3.0-1build1+lityos1`, runtime rc5) | [`LGPL-3.0`](https://www.gnu.org/licenses/lgpl-3.0.html) | [quickshell-mirror/quickshell](https://github.com/quickshell-mirror/quickshell) et paquet source Ubuntu |

## Firefox

- Projet amont : [Mozilla](https://www.mozilla.org/), binaire installé depuis le dépôt apt de Mozilla.
- Licence du code : [`MPL-2.0`](https://www.mozilla.org/MPL/2.0/).
- **À confirmer** : la politique de marques et de redistribution de Mozilla pour le nom « Firefox » dans cette image n'a pas été vérifiée.
- Source : <https://firefox-source-docs.mozilla.org/> (code source de Firefox ; adresse à confirmer).

## proot et talloc

- **proot** : projet [Termux](https://github.com/termux/proot) (`termux/proot`), commit `4dba3afb…` ; licence [`GPL-2.0-or-later`](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html). Accompagné de 24 correctifs LityOS, dont certains portés de WinNative (GPL-3.0, dépôt exact à confirmer).
- **talloc 2.4.3** : projet Samba, <https://talloc.samba.org/>, lié statiquement ; licence [`LGPL-3.0-or-later`](https://www.gnu.org/licenses/lgpl-3.0.html) (à confirmer).
- Source : correspondant à la release (voir [SOURCE.md](SOURCE.md)).

## directaudio

- Auteur : The412Banner, projet [The412Banner/directaudio](https://github.com/The412Banner/directaudio), tag `directaudio-linux-v1.1.0`, commit `52aedbf8…`.
- Licence : [`LGPL-2.1-or-later`](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html). Copyright © 2026 The412Banner.

## OpenCV, MediaPipe et modèles Google (pack `tracking`)

- **OpenCV 4.13.0** : [opencv/opencv](https://github.com/opencv/opencv), `Apache-2.0`.
- **MediaPipe tasks 1.0.0** (Google) : [google-ai-edge/mediapipe](https://github.com/google-ai-edge/mediapipe), `Apache-2.0`.
- **Modèles Google** (`hand_landmarker.task`, `pose_landmarker_lite.task`, `hand_landmarker_lite.task`) : **licence à confirmer** (Apache-2.0 attendue, non vérifiée). Le modèle `hand_landmarker_lite.task` est assemblé par LityOS à partir d'actifs Google.
- Texte de la licence : <https://www.apache.org/licenses/LICENSE-2.0>.

## butler et 7-Zip (pack `butler`)

- **butler 15.32.0** : projet [itchio/butler](https://github.com/itchio/butler) (itch.io), licence [`MIT`](https://spdx.org/licenses/MIT.html).
- **7-Zip / c7zip** (`7z.so`, `libc7zip.so`) : projet [7-Zip](https://www.7-zip.org/) ; licence `LGPL-2.1-or-later` avec la restriction unRAR ([texte](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html)). Version et classification exacte de la licence : à confirmer.

## msitools (miroir `build-dependency-msitools`)

Paquets Arch Linux ARM ([archlinuxarm/PKGBUILDs](https://github.com/archlinuxarm/PKGBUILDs)), copie d'une release DroidDeck.

- **gcab 1.6** : `LGPL-2.1-or-later` ([texte](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html)).
- **cabextract 1.11** : `GPL-3.0-or-later` ([texte](https://www.gnu.org/licenses/gpl-3.0.html)).
