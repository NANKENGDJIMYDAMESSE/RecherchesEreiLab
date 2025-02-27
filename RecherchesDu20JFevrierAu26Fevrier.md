# Learning rate (taux d'apprentissage) :

- C'est un paramètre essentiel dans l'entraînement des modèles d'apprentissage automatique, en particulier les réseaux de neurones et les algorithmes de descente de gradient.
- Il détermine la taille des pas que le modèle fait pour ajuster ses poids lors de l'apprentissage.
- Un taux d'apprentissage élevé peut entraîner une convergence rapide, mais risque de dépasser l'optimum.
- Un taux d'apprentissage faible peut conduire à une convergence lente, mais peut aider à trouver un optimum plus précis.
# Régularisation (L1/L2) :

- Ce sont des techniques utilisées pour éviter le surapprentissage dans les modèles d'apprentissage automatique.
- La régularisation L1 (Lasso) ajoute la valeur absolue des poids à la fonction de coût, ce qui peut entraîner une sélection de caractéristiques en mettant certains poids à zéro.
- La régularisation L2 (Ridge) ajoute le carré des poids à la fonction de coût, ce qui pénalise les grands poids et les réduit, mais ne les met généralement pas à zéro.
- Ces techniques aident à simplifier le modèle et à améliorer sa capacité de généralisation.
# Profondeur du modèle :

- Ce paramètre est particulièrement pertinent pour les modèles basés sur des arbres de décision, tels que les forêts aléatoires et les arbres de décision boostés.
- Il détermine le nombre de niveaux ou de nœuds dans l'arbre.
- Une profondeur élevée permet au modèle de capturer des relations complexes, mais peut conduire au surapprentissage.
- Une profondeur faible limite la complexité du modèle, mais peut entraîner un sous-apprentissage.
- Nombre d'arbres (Random Forest, Gradient Boosting) :

Ces algorithmes sont des méthodes d'ensemble qui combinent plusieurs arbres de décision pour améliorer la performance.
Le nombre d'arbres détermine la taille de l'ensemble.
Un nombre élevé d'arbres peut améliorer la robustesse et la précision du modèle, mais augmente également le temps de calcul.
Il existe un point de rendement décroissant où ajouter plus d'arbres n'améliore pas significativement la performance.

# 1. Analyser l’impact des hyperparamètres dans différentes applications

L’optimisation des hyperparamètres joue un rôle crucial dans l’amélioration des performances des modèles d’apprentissage automatique. Toutefois, leur impact peut varier selon le type d’application. Cette analyse pourrait inclure :

Classification et Régression : Étudier l’influence de l’apprentissage du taux (learning rate) et de la régularisation sur la précision et la robustesse du modèle.

Vision par ordinateur : Examiner comment le choix de la taille des batchs et des filtres impacte la convergence des réseaux neuronaux convolutifs.

Traitement du langage naturel (NLP) : Observer l’effet du réglage de la longueur des séquences et des tailles d’embeddings sur la performance des modèles.

Détection d’anomalies : Comparer la sensibilité des hyperparamètres dans des modèles supervisés et non supervisés appliqués à la cybersécurité ou à la finance.

# 2. Déterminer dans quels contextes les hyperparamètres sont plus pertinents que les paramètres ajustables

Les hyperparamètres contrôlent la manière dont un modèle apprend tandis que les paramètres ajustables sont directement dérivés des données. Une étude approfondie pourrait s’intéresser aux aspects suivants :

Taille des données : Lorsque le volume de données est limité, l’optimisation des hyperparamètres (par exemple, la régularisation) devient plus déterminante que l’ajustement fin des paramètres internes.

Types de modèles : Les algorithmes nécessitant des architectures complexes (comme les réseaux neuronaux profonds) dépendent fortement de l’optimisation des hyperparamètres, tandis que des modèles plus simples (régressions, arbres de décision) peuvent être ajustés plus directement.

Environnements en ligne vs hors ligne : Dans des environnements évolutifs (systèmes de recommandation, détection de fraudes), l’optimisation dynamique des hyperparamètres peut surpasser un simple ajustement périodique des paramètres internes.

# 3. Comparer les performances des algorithmes en fonction de différentes techniques d’optimisation

L’efficacité de l’optimisation des hyperparamètres dépend fortement de la méthode employée. Une étude comparative entre différentes techniques pourrait inclure :

Grid Search : Exploration exhaustive d’un espace de recherche prédéfini. Utile pour les petits ensembles de données mais coûteux en calcul pour des espaces de grande dimension.

Random Search : Sélection aléatoire de combinaisons d’hyperparamètres. Plus efficace que Grid Search dans des espaces de recherche vastes et complexes.

Bayesian Optimization : Modélisation probabiliste de la fonction objectif pour une recherche plus efficiente des meilleures valeurs.

Optimisation par descente de gradient : Méthodes adaptatives comme Adam ou RMSProp pour un ajustement dynamique et rapide.

Les performances des modèles seront évaluées selon plusieurs critères :

Temps d’entraînement et de convergence

Précision et généralisation

Complexité computationnelle et coût en ressources

# 4. Utiliser des visualisations avancées pour démontrer l’impact des optimisations appliquées

L’optimisation des hyperparamètres doit être accompagnée d’une analyse visuelle pour mieux comprendre son influence. Quelques approches :

Cartes de chaleur (Heatmaps) : Pour illustrer l’interaction entre différents hyperparamètres et leur effet sur la performance du modèle.

Courbes d’apprentissage : Montrer l’évolution de la perte et de la précision en fonction des différentes configurations d’hyperparamètres.

Diagrammes de distribution : Visualiser l’impact de la régularisation sur la distribution des poids et des biais dans un réseau neuronal.

Graphiques comparatifs : Comparer les performances obtenues avec différentes techniques d’optimisation sur un même jeu de données.

# Recommandations

- Mieux structurer sous forme de power point
- Presenter totutes les 2 dernieres recherches.
- 
