# Code source correspondant

Les applications et composants LityOS publiés dans les [releases de ce dépôt](https://github.com/LityTech27/LityOS-Components/releases) sont distribués sous licence GNU GPL v3 (voir [LICENSE](LICENSE)). Cette page est l'offre de source qui les accompagne.

## Où trouver la source

Le code source correspondant à chaque version est joint à la release sous la forme `LityOS-<tag>-source.tar.gz`. Sa somme SHA-256 figure dans le fichier `SHA256SUMS.txt` de la même release.

Les notes de chaque release indiquent si elle porte déjà une archive de source ; ne supposez pas qu'une release en possède une si ses notes ne la mentionnent pas.

## Correspondance entre un tag et un commit

- **`main-<sha7>`** : correspond au commit LityOS dont l'identifiant commence par `<sha7>`. L'identifiant complet est donné dans les notes de la release, sous « Commit: ».
- **`lityos-r1-rcN`** et **packs** (`pack-<nom>-<hash>`) : correspondent au commit nommé dans les notes de la release.

## Composants tiers (Ubuntu, KDE, Mesa…)

La source des paquets d'origine est celle de l'archive Ubuntu (par exemple `apt source <paquet>`). Les correctifs propres à LityOS (par exemple pour KWin, Mesa et Quickshell, dont les paquets portent le suffixe `+lityos1`) sont contenus dans l'archive de source jointe à la release.

La liste complète des composants et de leurs licences est dans [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Contact

Pour toute question, ou pour demander la source sur un autre support, ouvrez une [issue](https://github.com/LityTech27/LityOS-Components/issues) sur ce dépôt.

## Durée de l'offre

Cette offre est valable au moins trois ans après la dernière distribution de la version concernée.
