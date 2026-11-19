# SKYRISE DEFENSE — Phaser 3

Prototype jouable de défense de tours roguelike, reconstruit à partir de **Bible_SkyriseDefense.pdf** et des données/scripts PoC fournis dans le dossier Dropbox public. Interface et documentation en français. La présentation adopte un poste de contrôle de science-fiction, avec palette pétrole, cuivre et menthe.

## Lancer

Dans ce dossier, lancer `python -m http.server 8000`, puis ouvrir http://localhost:8000. Il faut servir les fichiers par HTTP (ne pas ouvrir `index.html` directement). Phaser 3.90 est embarqué dans `lib/phaser.min.js`; un CDN jsDelivr est déclaré en secours si le fichier local ne se charge pas. Une connexion Internet n’est nécessaire que pour le secours CDN et la police Google Fonts, avec repli typographique système.

## Boucle disponible

Menu → choix parmi 9 pilotes → atelier avec installation de modules (limite de hauteur 7) → combat tour par tour (tir, réparation, passage) → récompenses en crédits et points tech. L’arbre technologique expose les données disponibles des branches Offense, Economy et Resilience. La campagne jouable compte 20 étapes; le référentiel original PoC fournit ses 14 entrées ennemies et 70 modules. Sauvegarde, recrutements, méta-progression persistante et simulation fidèle des compétences restent hors périmètre de ce prototype.

## Données et assets

- `src/data/config.js` est extrait des structures JavaScript PoC (70 modules, 9 pilotes, 14 ennemis, nœuds d’arbre par branche), accompagné de notes sur la provenance.
- `assets/placeholders/` contient des PNG synthétiques de substitution, pas les illustrations de production; chaque entité répertoriée a son image. `assets/manifest.json` contient les chemins, dimensions et notes.
- Pour remplacer une illustration, garder le nom et les dimensions recommandées, ou modifier le chemin dans le manifeste / le code de chargement. Ne pas réutiliser/copier les images de référence originales.

## Limites connues

Ce livrable est un prototype Phaser jouable, pas une reproduction exhaustive du jeu. La Bible décrit des systèmes (arbre de 198 nœuds, campagnes, équipage, économie et effets) qui ne sont pas tous présents dans les données PoC ou implémentés ici. Le script PoC déclare 70 modules, 9 pilotes, 14 ennemis; les branches de l’arbre disponibles dans le fichier source contiennent 59 entrées au total (23/18/18), contrairement à l’objectif de conception de 198 nœuds de la Bible. Les 20 nœuds de campagne sont une séquence légère construite pour le prototype, et non une carte originale exacte. Le combat simplifie stats, énergie, effets et IA. Les visuels fournis ici sont des placeholders générés.
