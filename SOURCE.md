# Code source correspondant

Les applications et composants LityOS publiés dans les [releases de ce dépôt](https://github.com/LityTech27/LityOS-Components/releases) sont distribués sous licence GNU GPL v3 (voir [LICENSE](LICENSE)). Cette page est l'offre de source qui les accompagne.

Le dépôt de développement de LityOS n'est pas public : les identifiants de commit cités ci-dessous sont des références, et le code se trouve dans l'archive de source décrite ici.

## Archive de source LityOS

Les releases publiées à partir de la mise en place des archives portent une archive de source LityOS, `LityOS-<tag>-source.tar.gz`, accompagnée de sa somme SHA-256. Pour une release qui n'en porte pas, la source correspondante est fournie sur demande : ouvrez une issue (voir « Contact »).

### Contenu prévu

- **APK `main-<sha7>`** : l'arbre de LityOS au commit indiqué, avec ses scripts de build et ses correctifs.
- **Runtime `lityos-r1-rcN` et packs** : l'arbre de LityOS au commit indiqué dans les notes de la release, avec les éléments nécessaires à la reconstruction du fichier concerné.

### Exceptions

- **Pilote Turnip** (`driver-turnip-v0.3.4`) : sa source est l'archive déjà jointe à la release, `DD-Turnip-v0.3.4-source.tar.xz` (voir `DD-Turnip-NOTICE.md`).
- **Miroir msitools** : paquets Arch Linux ARM (gcab, cabextract) ; la source amont est citée dans [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Correspondance entre un tag et un commit

- **`main-<sha7>`** : correspond au commit LityOS dont l'identifiant commence par `<sha7>`. L'identifiant complet est donné dans les notes de la release, sous « Commit: ».
- **`lityos-r1-rcN`** et **packs** (`pack-<nom>-<hash>`) : correspondent au commit nommé dans les notes de la release.

## Composants tiers

- **Paquets Ubuntu non modifiés** (runtime et bureau) : la source est celle de l'archive Ubuntu (par exemple `apt source <paquet>`). Si la version distribuée a disparu de l'archive Ubuntu, la source est fournie sur demande.
- **Paquets modifiés `+lityos1`** (KWin, Mesa, Quickshell) : la source, avec les correctifs LityOS, est dans l'archive de source LityOS ou fournie sur demande. Quickshell, présent dans la release `lityos-r1-rc5` seulement, provient d'un paquet source d'Ubuntu 26.10.
- **Firefox** : source publiée par Mozilla, <https://ftp.mozilla.org/pub/firefox/releases/159.0.1/source/>.
- **7-Zip, proot, talloc, directaudio et autres packs** : sources amont citées dans [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) ; les correctifs LityOS sont dans l'archive de source LityOS ; le reste est fourni sur demande.

Les textes de licence accompagnent la distribution ; ils sont repris dans l'archive de source LityOS dès sa mise en place.

## Anciennes préversions

Les anciennes préversions `main-*` sont supprimées automatiquement. Pour toute version distribuée depuis moins de trois ans dont l'archive de source LityOS n'est plus en ligne, la source est fournie sur demande via une issue.

## Contact

Ouvrez une [issue](https://github.com/LityTech27/LityOS-Components/issues) sur ce dépôt, **sans donnée personnelle** (pas d'adresse postale ni de coordonnées dans l'issue). Nous vous indiquerons un moyen de contact.

## Durée de l'offre

Cette offre est valable au moins trois ans après la dernière distribution de la version concernée.
