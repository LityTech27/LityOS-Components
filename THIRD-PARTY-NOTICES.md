# Mentions des composants tiers

Ce fichier liste les composants distribués dans les releases de ce dépôt, avec leur auteur ou projet amont, leur licence (identifiant [SPDX](https://spdx.org/licenses/)) et un lien vers la source. Chaque composant reste sous sa propre licence.

Les mentions « à confirmer » signalent une information non vérifiée à ce jour. L'offre de source (LityOS et correctifs LityOS) est décrite dans [SOURCE.md](SOURCE.md). Le texte de la GPL v3 de LityOS est dans [LICENSE](LICENSE).

## Récapitulatif

| Composant | Version | Licence (SPDX) |
| --- | --- | --- |
| LityOS | selon la release | GPL-3.0 (variante `-only` ou `-or-later` à confirmer ; dérivé de DroidDeck 0.6.9) |
| DD-Turnip / Mesa | v0.3.4 | `MIT` (Mesa), correctifs `GPL-3.0` |
| Ubuntu et Kubuntu / KDE Plasma | 26.04 | selon chaque paquet |
| KWin, Mesa, Quickshell (paquets `+lityos1`) | 6.6.6, 26.0.8, 0.3.0 | `GPL-2.0-or-later`, `MIT` et autres, LGPL-3.0 (variante à confirmer) |
| Firefox | 159.0.1 | `MPL-2.0` |
| proot / talloc | commit `4dba3afb…` / 2.4.3 | `GPL-2.0-or-later` / `LGPL-3.0-or-later` |
| directaudio | `directaudio-linux-v1.1.0` | `LGPL-2.1-or-later` |
| OpenCV / MediaPipe / modèles Google | 4.13.0 / 1.0.0 | `Apache-2.0` (modèles : à confirmer) |
| butler / 7-Zip (c7zip) | 15.32.0 / à confirmer | `MIT` / GNU LGPL (version à confirmer) avec restriction unRAR et parties BSD |
| msitools : gcab / cabextract | 1.6 / 1.11 | `LGPL-2.1-or-later` / `GPL-3.0-or-later` |

## LityOS

- Licence : [GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html) (voir [LICENSE](LICENSE)) ; variante `-only` ou `-or-later` à confirmer.
- Dérivé de **DroidDeck 0.6.9** (projet [Droid-Deck/DroidDeck](https://github.com/Droid-Deck/DroidDeck), GPL-3.0), commit de départ `0a07926ef3477c90db911d169904137cfc5e2505`.
- Le dépôt de développement de LityOS n'est pas public ; la source correspondante à chaque release est décrite dans [SOURCE.md](SOURCE.md).

### Bibliothèques et code adapté dans LityOS

Ces mentions reprennent les fichiers d'attribution de LityOS (`docs/third-party/`). La présence exacte de chaque élément dans chaque APK est à confirmer ; les textes de licence complets sont dans l'archive de source.

| Élément | Auteur / amont | Licence |
| --- | --- | --- |
| MediaPipe Tasks Vision 1.0.0 (et ses dépendances Maven) | Google LLC, [google-ai-edge/mediapipe](https://github.com/google-ai-edge/mediapipe) | Apache-2.0 |
| Fonction de distance de polygone (suivi des mains) | Inigo Quilez, © 2019 | MIT |
| Modèle de bras (adapté de `GvrArmModel.cs`) | Google VR SDK for Unity, © 2016 Google Inc. | Apache-2.0 |
| Simulation de mains (adaptée de l'exemple OpenVR) | Valve Corporation, [ValveSoftware/openvr](https://github.com/ValveSoftware/openvr) | BSD-3-Clause |
| Pose Valve Index (de Monado) | Collabora, Ltd., Daniel Willmott, [Monado](https://gitlab.freedesktop.org/monado/monado) | BSL-1.0 |
| Protocole RayNeo et filtre d'orientation (adaptés) | [informalTechCode/RayNeo-Air-Series-3DoF-Scaffold](https://github.com/informalTechCode/RayNeo-Air-Series-3DoF-Scaffold) | Apache-2.0 |
| Identification USB RayNeo GT | verncat, © 2025, [RayNeo-Air-3S-Pro-OpenVR](https://github.com/verncat/RayNeo-Air-3S-Pro-OpenVR) | MIT |
| Protocole VITURE V2 (adapté) | Holger Bartnick, © 2026, [elasticjava/viture-v2](https://github.com/elasticjava/viture-v2) | MIT |
| libusb 1.0.30 (caméra USB, optionnel) | [libusb](https://github.com/libusb/libusb) | LGPL-2.1-or-later |
| libuvc 0.0.8 (caméra USB, optionnel) | Ken Tossell, [libuvc](https://github.com/libuvc/libuvc) | BSD-3-Clause |

Les autres crédits hérités de DroidDeck (par exemple WinNative, FEX, Wine, Proton) figurent dans la section « Credits and licence » du [README de DroidDeck](https://github.com/Droid-Deck/DroidDeck#credits-and-licence) ; leur inventaire complet pour cette distribution est à confirmer.

## Pilote DD-Turnip v0.3.4 / Mesa

- Projet amont : DroidDeck ([Droid-Deck/Drivers-CI](https://github.com/Droid-Deck/Drivers-CI), release `DD-Turnip-v0.3.4`), construit à partir de Mesa 27.0.0-devel (commit `e2ab6687d5ad…`) avec des correctifs DroidDeck.
- Licences : Mesa [`MIT`](https://spdx.org/licenses/MIT.html) (avec des exceptions par fichier) ; correctifs et pilotes [`GPL-3.0`](https://www.gnu.org/licenses/gpl-3.0.html).
- Source : l'archive `DD-Turnip-v0.3.4-source.tar.xz` et le fichier `DD-Turnip-NOTICE.md` sont joints à la release `driver-turnip-v0.3.4` ; projet Mesa : <https://www.mesa3d.org/>.

## Ubuntu 26.04 (runtime arm64) et Kubuntu / KDE Plasma (bureau)

- Projet amont : [Ubuntu](https://ubuntu.com/) (Canonical Ltd) et ses paquets ; bureau Kubuntu / KDE Plasma 6.6.x.
- Licences : celles de chaque paquet (GPL, LGPL, MIT, BSD, etc.), dont le texte est dans `/usr/share/doc/<paquet>/copyright` de l'image.
- Liste exacte des paquets et versions : fichiers `*.packages.txt` joints aux releases `lityos-r1-rcN`.
- Source : archive Ubuntu, <https://archive.ubuntu.com/ubuntu/> (par exemple `apt source <paquet>`).
- Composants notables du bureau, présents dans `lityos-r1-rc5-desktop.packages.txt` : codecs et lecteurs (`ffmpeg` 7:8.0.1-3ubuntu2, `vlc-*` 3.0.23-1, `gstreamer1.0-plugins-ugly` 1.28.2-1, `libx264`, `libx265`) sous licences GPL/LGPL, pour lesquels des brevets peuvent s'appliquer selon les pays ; `fonts-ubuntu` 0.869+git20240321-0ubuntu2 sous Ubuntu Font Licence ; `unrar-free` 1:0.3.3-1build1 (GPL).
- « Ubuntu » et « Kubuntu » sont des marques de Canonical Ltd. LityOS n'est pas Ubuntu et n'est pas affilié à Canonical.

## Paquets modifiés `+lityos1`

Paquets source Ubuntu recompilés avec des correctifs LityOS ; la source de ces paquets est fournie avec l'archive de source ou sur demande (voir [SOURCE.md](SOURCE.md)). La source de Quickshell est celle d'un paquet Ubuntu 26.10, et ce paquet n'est présent que dans la release `lityos-r1-rc5`.

| Paquet | Version | Licence (SPDX) | Source amont |
| --- | --- | --- | --- |
| KWin | 6.6.6 | [`GPL-2.0-or-later`](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html) | <https://invent.kde.org/plasma/kwin> et archive Ubuntu |
| Mesa | 26.0.8 | [`MIT`](https://spdx.org/licenses/MIT.html) et autres licences listées dans `debian/copyright` | <https://www.mesa3d.org/> et archive Ubuntu |
| Quickshell | 0.3.0 (`0.3.0-1build1+lityos1`, runtime rc5) | [LGPL-3.0](https://www.gnu.org/licenses/lgpl-3.0.html) (variante à confirmer) | [quickshell-mirror/quickshell](https://github.com/quickshell-mirror/quickshell) et paquet source Ubuntu |

## Firefox

- Projet amont : [Mozilla](https://www.mozilla.org/), binaire Firefox 159.0.1 (`159.0.1~build1`) installé depuis le dépôt apt de Mozilla.
- Licence du code : [`MPL-2.0`](https://www.mozilla.org/MPL/2.0/). Marque Firefox régie par la politique de Mozilla.
- Source : <https://ftp.mozilla.org/pub/firefox/releases/159.0.1/source/>.

## proot et talloc

- **proot** : projet [Termux](https://github.com/termux/proot) (`termux/proot`), commit `4dba3afb…` ; licence [`GPL-2.0-or-later`](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html). Accompagné de 24 correctifs LityOS, dont certains portés de WinNative (dépôt exact et licence à confirmer).
- **talloc 2.4.3** : projet Samba, <https://talloc.samba.org/>, lié statiquement ; licence [`LGPL-3.0-or-later`](https://www.gnu.org/licenses/lgpl-3.0.html) (d'après l'en-tête de `talloc.h` au tag `talloc-2.4.3`). Source : <https://gitlab.com/samba-team/samba/-/tree/talloc-2.4.3/lib/talloc>.
- Source des correctifs et du build : celle de la release correspondante (voir [SOURCE.md](SOURCE.md)).

## directaudio

- Auteur : The412Banner, projet [The412Banner/directaudio](https://github.com/The412Banner/directaudio), tag `directaudio-linux-v1.1.0`, commit `52aedbf8…`.
- Licence : [`LGPL-2.1-or-later`](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html). Copyright © 2026 The412Banner.

## OpenCV, MediaPipe et modèles Google (pack `tracking`)

- **OpenCV 4.13.0** : [opencv/opencv](https://github.com/opencv/opencv), `Apache-2.0`.
- **MediaPipe tasks 1.0.0** (Google) : [google-ai-edge/mediapipe](https://github.com/google-ai-edge/mediapipe), `Apache-2.0`.
- **Modèles Google** (`hand_landmarker.task`, `pose_landmarker_lite.task`, `hand_landmarker_lite.task`) : **licence à confirmer** (Apache-2.0 attendue, non vérifiée). Le modèle `hand_landmarker_lite.task` est assemblé par LityOS à partir d'actifs Google (modifié par rapport aux modèles d'origine).
- Texte de la licence : <https://www.apache.org/licenses/LICENSE-2.0>.

## butler et 7-Zip (pack `butler`)

- **butler 15.32.0** : projet [itchio/butler](https://github.com/itchio/butler) (itch.io), licence [`MIT`](https://spdx.org/licenses/MIT.html).
- **7-Zip / c7zip** (`7z.so`, `libc7zip.so`) : projet [7-Zip](https://www.7-zip.org/) d'Igor Pavlov. Licence : GNU LGPL (version à confirmer), avec restriction unRAR et parties sous BSD 2 clauses et 3 clauses, voir <https://www.7-zip.org/license.txt>. Pour la redistribution binaire, les mentions de licence de ce fichier doivent être reproduites. Version à confirmer.

## msitools (miroir `build-dependency-msitools`)

Paquets Arch Linux ARM ([archlinuxarm/PKGBUILDs](https://github.com/archlinuxarm/PKGBUILDs)), copie d'une release DroidDeck.

- **gcab 1.6** : `LGPL-2.1-or-later` ([texte](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html)).
- **cabextract 1.11** : `GPL-3.0-or-later` ([texte](https://www.gnu.org/licenses/gpl-3.0.html)).
