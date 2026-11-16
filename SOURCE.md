# Code source correspondant

Les applications et composants LityOS publiés dans les [releases de ce dépôt](https://github.com/LityTech27/LityOS-Components/releases) sont distribués sous licence GNU GPL v3 (voir [LICENSE](LICENSE)). Cette page est l'offre de source qui les accompagne.

Le dépôt de développement de LityOS n'est pas public : les identifiants de commit cités ci-dessous sont des références, et le code se trouve dans l'archive de source décrite ici.

## Archives de source

Les releases publiées à partir de la mise en place des archives portent une archive `LityOS-<tag>-source.tar.gz` ; sa somme SHA-256 figure dans la release. Pour une release qui n'en porte pas, la source correspondante est fournie sur demande : ouvrez une issue (voir « Contact »).

### Contenu d'une archive

- **APK `main-<sha7>`** : l'arbre de LityOS au commit indiqué, avec ses scripts de build et ses correctifs.
- **Runtime `lityos-r1-rcN` et packs** : l'arbre de LityOS au commit indiqué dans les notes de la release, avec les chemins nécessaires à la reconstruction du fichier concerné (scripts de build, correctifs, références de version). Le code des composants tiers sous GPL/LGPL redistribués par les packs (par exemple proot et talloc, directaudio) est fourni avec l'archive ou sur demande.
- **Paquets Ubuntu modifiés `+lityos1`** (KWin, Mesa, Quickshell) : les sources de ces paquets sont fournies avec l'archive jointe ou sur demande ; l'offre ne dépend pas seulement de l'archive Ubuntu, qui ne conserve pas toutes les versions.

### Exceptions

- **Pilote Turnip** (`driver-turnip-v0.3.4`) : sa source est l'archive déjà jointe à la release, `DD-Turnip-v0.3.4-source.tar.xz` (voir `DD-Turnip-NOTICE.md`).
- **Miroir msitools** : ce sont des paquets Arch Linux ARM (gcab, cabextract) ; la source amont est citée dans [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) et fournie sur demande.

## Correspondance entre un tag et un commit

- **`main-<sha7>`** : correspond au commit LityOS dont l'identifiant commence par `<sha7>`. L'identifiant complet est donné dans les notes de la release, sous « Commit: ».
- **`lityos-r1-rcN`** et **packs** (`pack-<nom>-<hash>`) : correspondent au commit nommé dans les notes de la release.

## Composants tiers (Ubuntu, KDE, Mesa…)

La source des paquets d'origine est celle de l'archive Ubuntu (par exemple `apt source <paquet>`). Quickshell, présent dans la release `lityos-r1-rc5` seulement, provient d'un paquet source d'Ubuntu 26.10. Les correctifs propres à LityOS sont dans l'archive de source jointe ou fournis sur demande.

La liste des composants et de leurs licences est dans [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Anciennes préversions

Les anciennes préversions `main-*` sont supprimées automatiquement. Pour toute version distribuée depuis moins de trois ans dont l'archive n'est plus en ligne, la source est fournie sur demande via une issue.

## Contact

Ouvrez une [issue](https://github.com/LityTech27/LityOS-Components/issues) sur ce dépôt, **sans donnée personnelle** (pas d'adresse postale ni de coordonnées dans l'issue). Nous vous répondrons en indiquant un moyen de contact privé. Pour un envoi sur support physique, des frais raisonnables couvrant le support et l'envoi peuvent être demandés.

## Durée de l'offre

Cette offre est valable au moins trois ans après la dernière distribution de la version concernée.
