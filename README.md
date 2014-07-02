![Imprimante 3D](https://raw.githubusercontent.com/landru29/printer/master/doc/src/img/printer.jpg)

Cadre du projet
===============
Une imprimante 3D est une machine qui permet de reproduire des pièces plus ou moins complexes par apport de matière. Il existe plusieurs types d'imprimantes, selon le principe d'apport de matière utilisé. Le prérimètre de ce projet est une imprimante qui extrude du plastique à déposer couches par couches.


Objectif
========
Le principal objectif est, évidement, de construire une imprimante 3D. Cette imprimante fonctionnera sur le principe d'extrusion de matière plastique. Je m'appuie sur les imprimantes Reprap http://reprap.org/wiki/RepRap/fr. Dans cette perspective, je m'autorise à réutiliser, modifier, adapter des pièces conçues pour d'autres imprimantes Reprap.
Une contrainte forte de ce projet est le budget. En référence, une imprimante Reprap i3 en kit est vendue 450€ sans l'électronique de commande (600€ tout compris). Mon objectif est de limiter mon budget à 250€. C'est difficilement atteignable, mais pas impossible.

Les imprimantes RepRap
======================
Le principe de ces imprimantes est qu'elles sont réplicables. Concrêtement, pour fabriquer une imprimante RepRap, on profite d'une autre imprimante pour imprimer des pièces. Mon projet repose sur ce principe. En effet, pour des questions de facilité (je m'affranchis de certains usinages complexe), la plupart des supports seront imprimés.

Organisation du projet
======================
On trouve deux dossiers:
> * `doc` (documentation du projet, source LaTeX)
> * `mecanical` (conception mécanique du projet)

Doc
---

La documentation est écrite en LaTeX. Pour la regénérer il faut "compiler" les sources. Certaines extensions sont nécessaire à la construction du document (tous ces dépendances se trouvent dans le fichier `doc/source/printer.tex`).
Chaque chapitre a sont propre fichier `*.tex` pour plus de facilité à la rédaction. Un `Makefile` (et un `make.bat`) est à disposition pour faciliter la compilation

Mecanical
---------
Vous trouverez les différents éléments:
> * Les pièces qui devront être imprimées sont dans le dossier `mecanical/to_print`.
> * Les sous-ensembles constituant l'imprimante sont dans `mecanical/assembly`.
> * L'imprimante complete se trouve à la racine de `mecanical`.
> * La bibliothèque de roulement à billes est dans `mecanical/bearing`
> * Les éléments de la structure sont dans `mecanical/tubes`
> * La pré-étude de la tête d'extrusion est dans `mecanical/head`
> * Toute la quincaillerie standard est dans `mecanical/standard`

Attention, il arrive que j'oublie de mettre à jour les fichiers `*.stl` (que je maintiens uniquement pour la visionneuse de GitHub). Vérifiez bien les dates !
