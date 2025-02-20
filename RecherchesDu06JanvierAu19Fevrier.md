# L’optimisation des données et des algorithmes constitue un domaine clé pour améliorer la performance des modèles tout en réduisant les biais. Cette dernière partie propose une synthèse des recommandations, des pistes d’amélioration et des perspectives pour des travaux futurs.


# 1.Description des approches heuristiques et des méthodes d’optimisation
Les approches heuristiques et les méthodes d’optimisation jouent un rôle central dans l'amélioration des algorithmes. Cette section vise à revoir ces concepts et proposer une comparaison plus approfondie.
# 2. Approches heuristiques
Les heuristiques sont des méthodes de résolution de problèmes qui permettent de trouver rapidement des solutions "raisonnables", même si elles ne sont pas garanties d'être optimales. Elles sont particulièrement utiles pour les problèmes complexes où la recherche de la solution parfaite prendrait un temps prohibitif.
Nature du problème: Problèmes combinatoires, où il faut choisir la meilleure solution parmi un nombre astronomique de possibilités (ex: logistique, transport, planification).
### Exemples d'heuristiques:
- Algorithmes gloutons: Choisir la meilleure option à chaque étape, sans se soucier de l'impact à long terme.
Exemple: Un livreur doit livrer plusieurs colis. Un algorithme glouton choisirait à chaque étape le colis le plus proche à livrer, sans forcément optimiser l'itinéraire global.
- Algorithmes génétiques: S'inspirer de l'évolution naturelle pour améliorer itérativement une population de solutions.
Exemple: Optimisation de la conception d'une aile d'avion. L'algorithme génétique ferait évoluer une population de conceptions en sélectionnant les meilleures et en les combinant.
Recuit simulé: Explorer l'espace de solutions en acceptant parfois des "mauvaises" solutions pour éviter de rester bloqué dans un optimum local.
Exemple: Optimisation de l'agencement des composants électroniques sur une carte mère. Le recuit simulé accepterait parfois des agencements moins bons pour explorer d'autres options.
Recherche tabou: Mémoriser les solutions déjà explorées pour éviter de les revisiter.
Exemple: Un robot doit explorer un labyrinthe. La recherche tabou mémoriserait les chemins déjà empruntés pour éviter de tourner en rond.
Algorithmes de colonies de fourmis: S'inspirer du comportement des fourmis pour trouver des chemins optimaux.
Exemple: Optimisation du réseau de distribution d'une entreprise. L'algorithme de colonies de fourmis simulerait le dépôt de phéromones par les fourmis pour trouver les meilleurs itinéraires.
# 2. Optimisation de modèles classiques
Ces méthodes suivent une approche plus formelle pour ajuster les modèles, en particulier les modèles d'apprentissage automatique "traditionnels" (par opposition aux réseaux de neurones profonds).

Nature du problème: Optimisation de modèles avec un nombre limité de paramètres, souvent pour des tâches de classification ou de régression.

Exemples de techniques:

Optimisation des hyperparamètres: Trouver la meilleure combinaison de paramètres qui contrôlent le comportement du modèle (ex: profondeur maximale d'un arbre de décision, paramètre de régularisation d'une SVM).
Techniques: Recherche manuelle, recherche aléatoire, recherche par grille, optimisation bayésienne.
Optimisation des paramètres du modèle: Ajuster les paramètres internes du modèle (ex: poids d'un réseau de neurones) pour minimiser l'erreur.
Techniques: Descente de gradient et ses variantes (SGD, Adam).
# 3. Cas nécessitant une adaptation dynamique
Il s'agit de situations où les données ou les conditions changent au fil du temps, ce qui nécessite que le système s'adapte en conséquence. L'apprentissage automatique est particulièrement adapté à ces cas.
Nature du problème: Systèmes évolutifs, détection de changements, adaptation à de nouvelles situations.
Exemples:
Détection de fraudes: Les techniques de fraude évoluent constamment, il est donc essentiel que le système de détection puisse s'adapter aux nouvelles formes de fraude.
Systèmes de recommandation personnalisée: Les préférences des utilisateurs peuvent changer au fil du temps, il est donc important que le système de recommandation puisse s'adapter en conséquence.
Voitures autonomes: Les voitures autonomes doivent être capables de s'adapter à des conditions de circulation changeantes et imprévues.
Techniques: Apprentissage supervisé, apprentissage non supervisé, apprentissage par renforcement.

### Machine Learning: L'apprentissage automatique est idéal pour ces cas car il permet à un système d'apprendre à partir des données et de s'améliorer au fil du temps, sans avoir besoin d'être explicitement programmé pour chaque situation.
### Types d'apprentissage automatique:
- Apprentissage supervisé: Apprendre à partir de données étiquetées (par exemple, des exemples de transactions frauduleuses et non frauduleuses).
- Apprentissage non supervisé: Découvrir des motifs ou des structures dans des données non étiquetées (par exemple, segmenter les clients en groupes).
- Apprentissage par renforcement: Apprendre à prendre des décisions en interagissant avec un environnement (par exemple, entraîner un robot à marcher).
# Visualisations
Importance des visualisations: Les visualisations de données sont essentielles pour comprendre les données, identifier les tendances et les anomalies, et communiquer les résultats de l'analyse.
### Types de visualisations:
- Graphiques: Histogrammes, diagrammes de dispersion, courbes, etc.
- Tableaux: Tableaux de bord, rapports, etc.
- Cartes: Cartes géographiques, etc.
## Outils de visualisation: Il existe de nombreux outils de visualisation de données, tels que Matplotlib, Seaborn, Tableau, Power BI, etc.
- Analyse comparative et choix de la meilleure méthode
- Une analyse comparative des différentes approches (heuristiques, optimisation, machine learning) est essentielle pour choisir la meilleure méthode en fonction du contexte spécifique du problème. Il est important de prendre en compte les facteurs suivants :
La nature du problème: Quel est le type de problème à résoudre ? S'agit-il d'un problème combinatoire, d'un problème d'optimisation, ou d'un problème d'adaptation dynamique ?
- Les caractéristiques des données: Quelles sont les caractéristiques des données disponibles ? Sont-elles étiquetées ou non étiquetées ? Sont-elles statiques ou évolutives ?
- Les contraintes de temps et de ressources: Quelles sont les contraintes de temps et de ressources disponibles ? Quel est le niveau de précision requis ?
- Les objectifs de l'analyse: Quels sont les objectifs de l'analyse ? Recherche-t-on une solution optimale ou une solution "suffisante" ?

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

# Sources du travail
## 1. Optimisation des données :
- Nettoyage et prétraitement des données:
Scikit-learn: https://scikit-learn.org/stable/modules/preprocessing.html (Documentation sur les techniques de prétraitement)   
Kaggle: https://www.kaggle.com/ (Exemples de notebooks avec du code de prétraitement)
- Réduction de dimension:
Scikit-learn: https://scikit-learn.org/stable/modules/decomposition.html (Documentation sur l'ACP et autres méthodes)
StatQuest: https://www.youtube.com/user/joshstarmer (Chaîne YouTube expliquant des concepts statistiques et de ML)
- Rééquilibrage des classes:
Imbalanced-learn: https://imbalanced-learn.org/stable/ (Librairie Python dédiée au rééquilibrage)
SMOTE: https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html (Documentation sur la technique SMOTE)   
## 2. Optimisation des algorithmes :
- Approches heuristiques:
Recuit simulé: https://fr.wikipedia.org/wiki/Recuit_simul%C3%A9 (Explication du recuit simulé)
Algorithmes génétiques: https://fr.wikipedia.org/wiki/Algorithme_g%C3%A9n%C3%A9tique (Explication des algorithmes génétiques)
Recherche tabou: https://fr.wikipedia.org/wiki/Recherche_tabou (Explication de la recherche tabou)
## Optimisation des hyperparamètres:
Scikit-learn: https://scikit-learn.org/stable/modules/model_selection.html (Documentation sur GridSearchCV, RandomizedSearchCV)
Optuna: https://optuna.org/ (Librairie Python pour l'optimisation bayésienne)
Hyperopt: http://hyperopt.github.io/hyperopt/ (Autre librairie pour l'optimisation bayésienne)
## Modèles classiques et dynamiques:
Scikit-learn: https://scikit-learn.org/stable/index.html (Documentation sur les modèles classiques)
TensorFlow: https://www.tensorflow.org/ (Pour les modèles de deep learning)
PyTorch: https://pytorch.org/ (Autre librairie pour le deep learning)
## 3. Visualisations :
Matplotlib: https://matplotlib.org/stable/index.html (Librairie de base pour les graphiques)
Seaborn: https://seaborn.pydata.org/ (Librairie pour des graphiques statistiques plus avancés)
Plotly: https://plotly.com/python/ (Librairie pour des graphiques interactifs)

# Recommandations

- Constitution de l'hyperparametre 
- Est ce que le biais plus petit est indice du meilleur resultat 
- Dans quel conteste est il approprie d'avoir les hyperparametres ou les parametres
- Inclure l'hyperparametre dans le TP1
- 
























