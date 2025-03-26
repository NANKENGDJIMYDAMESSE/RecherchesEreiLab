# Titre :
# Corrélation entre la Performance et les Biais dans les Modèles d’Apprentissage Automatique : Étude des Différents Biais et Leviers d’Optimisation

## Résumé :
L’apprentissage automatique est aujourd’hui omniprésent dans divers domaines (finance, santé, justice, recrutement, etc.), soulevant des enjeux critiques en matière d’équité et d’efficacité. Cette thèse propose d’explorer la corrélation entre la performance des modèles et les biais présents dans les données et les algorithmes. L’objectif est de mieux comprendre comment ces biais influencent les performances des modèles et d’identifier des stratégies d’optimisation permettant de concilier précision et équité.

## L’étude abordera trois axes principaux :

- Une revue de littérature approfondie sera menée sur les différents types de biais (biais de sélection, biais algorithmique, biais de confirmation, etc.) et leurs implications. L’apport de cette thèse réside dans la proposition de nouvelles métriques et approches d’optimisation, permettant une meilleure compréhension des compromis entre équité et performance dans les systèmes d’intelligence artificielle.
- Identification et analyse des biais dans les jeux de données et les modèles d’apprentissage supervisé et non supervisé.

- Corrélation entre biais et performance : mesure de l’impact des biais sur la généralisation et la robustesse des modèles.

- Leviers d’optimisation : exploration des techniques d’atténuation des biais et d’amélioration des performances (ex. : rééchantillonnage des données, ajustement des fonctions de coût, régularisation, fairness-aware learning).


# Axe 1 : Revue de la littérature sur les biais en apprentissage automatique

L’analyse des biais dans les modèles d’intelligence artificielle est un sujet d’étude crucial (Barocas et al., 2016 ; Mehrabi et al., 2021). Cette revue de la littérature abordera les types de biais les plus courants, notamment :

- Biais de sélection : Il se produit lorsque les données d’entraînement ne sont pas représentatives de la population cible (Heckman, 1979). Exemples : sous-représentation de certaines classes, échantillons déséquilibrés.

- Biais algorithmique : Introduit par la manière dont les algorithmes apprennent et généralisent les données (Feldman et al., 2015). Certains algorithmes amplifient les inégalités présentes dans les données d’entrée.

- Biais de confirmation : Les modèles peuvent refléter des biais humains existants si les données sont annotées de manière subjective (Nickerson, 1998).

- Biais d’échantillonnage : Une mauvaise sélection des données peut fausser l’entraînement et la prédiction (Kruskal & Mosteller, 1979).**
L’analyse des biais dans les modèles d’intelligence artificielle est un sujet d’étude crucial. Cette revue de la littérature abordera les types de biais les plus courants, notamment :

- Biais de sélection : Il se produit lorsque les données d’entraînement ne sont pas représentatives de la population cible. Exemples : sous-représentation de certaines classes, échantillons déséquilibrés.

- Biais algorithmique : Introduit par la manière dont les algorithmes apprennent et généralisent les données. Certains algorithmes amplifient les inégalités présentes dans les données d’entrée.

- Biais de confirmation : Les modèles peuvent refléter des biais humains existants si les données sont annotées de manière subjective.

- Biais d’échantillonnage : Une mauvaise sélection des données peut fausser l’entraînement et la prédiction.
