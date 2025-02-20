# L’optimisation des données et des algorithmes constitue un domaine clé pour améliorer la performance des modèles tout en réduisant les biais. Cette dernière partie propose une synthèse des recommandations, des pistes d’amélioration et des perspectives pour des travaux futurs.
# 1. Description du travail pratique
## Objectif du travail pratique
L’objectif du travail pratique est de mettre en application les concepts d’optimisation des données et d’algorithmes dans un cadre expérimental concret. Cela inclut :
L’évaluation de différentes techniques d’optimisation des données (nettoyage, réduction de dimension, rééquilibrage des classes).
L’application de méthodes d’optimisation d’algorithmes (réglage d’hyperparamètres, heuristiques, modèles adaptatifs).
L’étude de l’impact de ces techniques sur les performances des modèles (précision, robustesse, biais).
# Plan du travail pratique
- Choix d’un jeu de données : Sélectionner un dataset contenant des biais potentiels (ex. : données de santé, finance, recrutement).
- Pré-traitement des données :
- Nettoyage des valeurs aberrantes.
- Imputation des valeurs manquantes.
- Normalisation et réduction de dimension.
- Application de modèles avec et sans optimisation :
- Comparaison de modèles non optimisés avec des versions améliorées par des techniques d’optimisation.
- Évaluation des performances et des biais :
- Utilisation de métriques standards (accuracy, F1-score, fairness metrics).
- Analyse des biais restants après optimisation.
- Visualisation des résultats :
- Graphiques comparant les performances des modèles optimisés et non optimisés.
# 2.Description des approches heuristiques et des méthodes d’optimisation
Les approches heuristiques et les méthodes d’optimisation jouent un rôle central dans l'amélioration des algorithmes. Cette section vise à revoir ces concepts et proposer une comparaison plus approfondie.

## 2.1. Approches heuristiques
Les heuristiques sont des méthodes approximatives permettant de trouver des solutions acceptables en un temps raisonnable. Elles sont souvent utilisées lorsque les solutions exactes sont trop coûteuses en calcul.
- Exemples d’heuristiques appliquées à l’optimisation des algorithmes :
- Recuit simulé (Simulated Annealing) : Technique inspirée du refroidissement des métaux, utilisée pour explorer l’espace des solutions en évitant les minima locaux.
- Algorithmes génétiques : Modélisation de l’évolution biologique pour optimiser des modèles complexes.
- Recherche tabou : Stratégie basée sur l’exploration intelligente de l’espace des solutions en évitant les répétitions.
## 2.2. Méthodes d’optimisation des algorithmes
Contrairement aux heuristiques, ces méthodes suivent une approche plus formelle pour ajuster les modèles.
- Optimisation des hyperparamètres :
- Grid Search : Exploration exhaustive de toutes les combinaisons d’hyperparamètres.
- Random Search : Exploration aléatoire des hyperparamètres, plus rapide que Grid Search.
- Bayesian Optimization : Utilisation de modèles probabilistes pour affiner la recherche des meilleurs paramètres.
# Etude Comparative 
- Les heuristiques sont des méthodes d'approximation rapide permettant d'obtenir une solution acceptable sans garantir une solution optimale. Elles sont adaptées aux problèmes complexes nécessitant une réponse rapide, comme la recherche d’itinéraires (exemple : Google Maps). Leur principal avantage est leur flexibilité, mais elles peuvent produire des solutions sous-optimales.

- L’optimisation classique, quant à elle, suit une approche plus systématique en ajustant précisément les paramètres du modèle. Elle est couramment utilisée pour des tâches comme le réglage des hyperparamètres. Cette approche est méthodique et rigoureuse, assurant une bonne robustesse, mais elle peut être coûteuse en temps de calcul, notamment lorsqu’il faut explorer un large espace de solutions.

- Enfin, le machine learning adopte un apprentissage adaptatif, où le modèle ajuste ses paramètres en fonction des données. Cette approche est particulièrement efficace pour des tâches comme la régression et la classification, où la capacité du modèle à généraliser et à s’adapter est cruciale. Toutefois, elle exige un temps de calcul élevé et présente un risque de surapprentissage si le modèle est trop complexe ou mal régularisé.

- En résumé, les heuristiques sont rapides mais parfois approximatives, l’optimisation classique est méthodique mais coûteuse en calcul, et le machine learning est puissant mais nécessite une gestion fine des risques de surajustement.
  
# Explication de la notion d’Hyperparamètres en Machine Learning
Les hyperparamètres sont des paramètres qu’on définit avant l'entraînement d'un modèle d'apprentissage automatique et qui influencent directement la performance et la généralisation du modèle. Contrairement aux paramètres (qui sont appris par le modèle pendant l'entraînement, comme les poids d’un réseau de neurones), les hyperparamètres doivent être définis manuellement et ajustés via une recherche expérimentale.
# Différence entre Paramètres et Hyperparamètres
- Un paramètre est une valeur interne à un modèle de machine learning, ajustée automatiquement pendant l'entraînement. Par exemple, dans une régression linéaire, les coefficients de la droite sont des paramètres, car ils sont appris à partir des données pour minimiser l'erreur du modèle.

- Un hyperparamètre, en revanche, est une valeur définie avant l'entraînement, qui contrôle le fonctionnement du modèle mais n'est pas ajustée directement à partir des données. Par exemple, le taux d’apprentissage (learning rate) dans un réseau de neurones ou le nombre d’arbres dans une forêt aléatoire sont des hyperparamètres, car ils doivent être définis par l'expérimentateur et peuvent influencer la performance du modèle.

- En résumé, les paramètres sont appris automatiquement par le modèle, tandis que les hyperparamètres sont définis manuellement et optimisés par des techniques comme Grid Search ou Random Search.
# Techniques d’Optimisation des Hyperparamètres
Ajuster les hyperparamètres manuellement est inefficace. Voici les principales méthodes :
## Grid Search (Recherche exhaustive)
- Principe : Tester toutes les combinaisons possibles d’hyperparamètres.
- Avantage : Trouve la meilleure combinaison.
- Inconvénient : Coût computationnel élevé.
## Random Search (Recherche aléatoire)
- Principe : Tester un sous-ensemble d’hyperparamètres choisis aléatoirement.
-  Avantage : Plus rapide que Grid Search.
- Inconvénient : Peut manquer la meilleure combinaison.
## Bayesian Optimization
- Principe : Utilise des modèles probabilistes pour prédire les meilleurs hyperparamètres à tester.
- Avantage : Plus efficace que Random Search et Grid Search.
- Inconvénient : Plus complexe à implémenter.
# Impact des Hyperparamètres sur la Performance
L’optimisation des hyperparamètres permet de :
-  Améliorer la précision (éviter l’overfitting et l’underfitting).
- Réduire le temps de calcul (éviter des modèles trop complexes).
- Rendre le modèle plus robuste (meilleure généralisation).
# Optimisation des modèles :
- Gradient Descent et variantes (SGD, Adam) : Techniques d’apprentissage permettant d’optimiser les paramètres d’un modèle de deep learning.
- Réduction de complexité : Pruning des réseaux neuronaux, réduction du nombre de paramètres.
# Comparaison des approches
Une analyse comparative des différentes approches est essentielle pour choisir la meilleure méthode en fonction du contexte.
# Choix de l’approche en fonction du contexte
Problèmes combinatoires (ex. : logistique, transport) → Heuristiques.
Optimisation de modèles classiques (ex. : tuning d’algorithmes) → Optimisation par hyperparamètres.
Cas nécessitant une adaptation dynamique (ex. : détection de fraudes, systèmes évolutifs) → Machine Learning.
Visualisations
# Importance des visualisations
Les visualisations permettent d’expliquer clairement les résultats des optimisations appliquées et d’identifier les biais restants.

# Types de visualisations
- Comparaison des modèles avant/après optimisation :
- Graphiques de performance (courbes ROC, précision, rappel).
- Heatmaps des matrices de confusion.
- Impact de la réduction de dimension :
- PCA : Graphique des composantes principales.
- t-SNE : Représentation des clusters.
# Détection des biais :
- Distribution des classes avant et après équilibrage.
- Graphiques de fairness metrics (Equalized Odds, Disparate Impact).
Perspectives et conclusions du TP
# Enseignements clés
- L’optimisation des données améliore significativement la performance des modèles.
- Les méthodes d’optimisation d’algorithmes permettent de réduire le biais introduit par des paramètres mal réglés.
- La détection et l’atténuation des biais restent des défis ouverts, nécessitant une approche multidimensionnelle.
# Limitations
Certaines techniques (comme SMOTE) peuvent introduire un surajustement.
L’optimisation des algorithmes peut être coûteuse en calcul et nécessiter des ressources importantes.
La réduction des biais ne garantit pas une équité totale des modèles.
# Travaux futurs
- Optimisation avancée des modèles : Tester des approches hybrides combinant heuristiques et deep learning.
- Amélioration des techniques d’équité : Explorer des métriques comme Fairness Constraints ou Equalized Odds.
- Exploration de modèles explicables : Développement d’algorithmes interprétables pour mieux comprendre les décisions prises par les modèles.

# TRAVAUX PRATIQUE 
# TP 1 : Comparaison des approches (Heuristiques, Optimisation classique, Machine Learning)

- Chargement d’un dataset de sklearn.
- Application des trois approches sur une même tâche.
- Calcul de toutes les métriques possibles.
- Visualisations des résultats.
- Tableau comparatif final pour choisir la meilleure méthode.
# TP 2 : Mise en évidence de la notion d’hyperparamètre
- Expérimentation avec différents hyperparamètres.
- Comparaison des performances en fonction du tuning des hyperparamètres.
- Optimisation via GridSearchCV, RandomSearchCV et Bayesian Optimization.


























