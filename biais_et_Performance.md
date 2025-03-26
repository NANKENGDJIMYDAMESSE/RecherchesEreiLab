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

Formules associées aux biais et interprétation

## Biais d'estimation (Casella & Berger, 2002) :

![image](https://github.com/user-attachments/assets/cefca734-c0b9-4e84-a3f8-7deba831b878)

Commentaire : Cette formule représente la différence entre la valeur attendue d’un estimateur  et la vraie valeur du paramètre . 
Un modèle biaisé a une différence significative entre l’estimation et la réalité.


## Erreur quadratique moyenne (MSE) - (James et al., 2013) :
![image](https://github.com/user-attachments/assets/6b8df403-09b4-4e4b-ba81-12261a3afaa0)
Commentaire : Cette mesure permet d’évaluer si un modèle de classification favorise ou défavorise un groupe particulier. 
Une valeur inférieure à 0.8 indique une discrimination potentielle.

## Formule des performances de classification et biais (Fawcett, 2006) :

![image](https://github.com/user-attachments/assets/d1306bae-6fef-4d0b-afa0-6d4eb36b1c61)

Commentaire : Cette mesure compare la performance du modèle en fonction des vrais positifs (TP), faux négatifs (FN), vrais négatifs (TN) et faux positifs (FP). 
Un déséquilibre dans ces valeurs peut indiquer un biais en faveur ou en défaveur d’une classe spécifique.


# Axe 2 : Identification et analyse des biais dans les jeux de données et les modèles d’apprentissage

## Cette partie se concentre sur la méthodologie d’identification des biais et l’évaluation de leur impact sur les modèles d’apprentissage supervisé et non supervisé.

## Méthodes d’identification des biais

- Analyse exploratoire des données (EDA) : Identification des déséquilibres dans la distribution des classes et des variables sensibles.

- Tests statistiques : Mesure de la représentativité des données (Kolmogorov-Smirnov, tests de normalité, etc.).

- Métriques d’équité : Analyse de la parité démographique, taux de faux positifs et faux négatifs différenciés.

- Interprétabilité des modèles : Utilisation de SHAP, LIME et autres outils pour comprendre comment un modèle prend ses décisions.

# Axe 3 : Corrélation entre biais et performance des modèles

## L’objectif de cette section est de quantifier l’effet des biais sur la précision et la généralisation des modèles.

## Approches expérimentales

- Évaluation comparative des performances des modèles avec et sans correction des biais.

- Étude de la robustesse des modèles en testant sur des données en distribution décalée.

- Analyse de la variabilité des prédictions sur des groupes démographiques différents.

## Méthodologie de mesure

- Courbes ROC et AUC pour comparer les modèles avant et après correction des biais.

- Écart de performance entre différents sous-groupes (Gender Bias, Ethnic Bias, etc.).

- Analyse des erreurs pour identifier les groupes les plus affectés par les biais.

# Axe 4 : Leviers d’optimisation et stratégies d’atténuation des biais

## Techniques d’atténuation des biais

- Rééchantillonnage des données : Techniques de suréchantillonnage ou sous-échantillonnage pour équilibrer les classes.

- Ajustement des fonctions de coût : Attribution de poids aux classes minoritaires pour réduire l’impact des biais.

- Régularisation des modèles : Pénalisation des modèles favorisant certaines classes.

- Fairness-aware Learning : Algorithmes d’apprentissage intégrant des contraintes d’équité.

- Calibration des modèles : Ajustement des probabilités de prédiction pour aligner les décisions sur des critères d’équité.

# Conclusion et perspectives

Cette étude vise à établir un lien quantifiable entre les biais et la performance des modèles tout en explorant des solutions d’optimisation viables. À travers des expérimentations et des analyses rigoureuses, la thèse proposera des recommandations pour concevoir des modèles à la fois performants et équitables. Les futures recherches pourront s’orienter vers l’étude des biais dans les modèles génératifs et le développement d’algorithmes auto-adaptatifs capables de détecter et corriger leurs propres biais.

## Références

- Casella, G., & Berger, R. L. (2002). Statistical Inference. Duxbury Press.

- James, G., Witten, D., Hastie, T., & Tibshirani, R. (2013). An Introduction to Statistical Learning. Springer.

- Dwork, C., Hardt, M., Pitassi, T., Reingold, O., & Zemel, R. (2012). Fairness Through Awareness. ACM.

- Fawcett, T. (2006). An Introduction to ROC Analysis. Pattern Recognition Letters.







































