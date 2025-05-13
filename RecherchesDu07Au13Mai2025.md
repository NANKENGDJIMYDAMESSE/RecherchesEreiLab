# Titre : Comparaison approfondie des modèles bio-inspirés, hybrides et traditionnels dans la modélisation prédictive épidémiologique : Étude de cas sur le COVID-19

## Résumé
Les modèles bio-inspirés, conçus à partir de mécanismes biologiques tels que la sélection naturelle, les comportements collectifs ou le système immunitaire, constituent une alternative innovante aux modèles d'apprentissage traditionnels. Ce travail présente une comparaison rigoureuse entre trois catégories de modèles : les modèles bio-inspirés purs, les modèles hybrides (partiellement bio-inspirés) et les modèles non bio-inspirés (traditionnels), appliqués à la prédiction du taux de reproduction du virus SARS-CoV-2. L’étude est basée sur le jeu de données mondial du COVID-19 fourni par Our World in Data. L’objectif est d’évaluer leurs performances selon des critères d’exactitude, de coût computationnel, de consommation énergétique approximée, et de généralisabilité.

# 1. Introduction
L’intelligence artificielle s’est inspirée depuis plusieurs décennies des mécanismes naturels pour proposer des paradigmes computationnels robustes face à l’incertitude, à la non-linéarité et à la complexité. Cette inspiration biologique a donné naissance à une classe de modèles appelés modèles bio-inspirés, fondés sur l'évolution naturelle, les comportements collectifs ou les réponses immunitaires.

Dès 1975, John Holland introduit les algorithmes génétiques dans Adaptation in Natural and Artificial Systems, en s’inspirant du mécanisme de sélection naturelle. Par la suite, Dorigo et Di Caro (1999) présentent l’optimisation par colonies de fourmis, et Dasgupta (2002) développe les systèmes immunitaires artificiels. Ces approches se caractérisent par leur capacité d’adaptation, leur tolérance au bruit et leur exploration efficace de grands espaces de recherche.

Parallèlement, les modèles partiellement bio-inspirés (ou hybrides) sont apparus. Ils combinent des algorithmes traditionnels (réseaux de neurones, forêts aléatoires, SVM) avec des composants d'optimisation bio-inspirés, comme des algorithmes évolutionnaires pour la sélection de variables ou le réglage des hyperparamètres. Ce paradigme est plus flexible et souvent plus efficace en pratique.

# 2. Cadre théorique
## 2.1 Modèles bio-inspirés purs
Ils dérivent de mécanismes biologiques sans inclure de modèles d’IA traditionnels. Exemples :

Algorithmes génétiques : Holland (1975)

Immune Algorithms : Dasgupta (2002)

Swarm Intelligence / PSO : Kennedy & Eberhart (1995)

ACO (Ant Colony Optimization) : Dorigo (1999)

Ces méthodes résolvent des problèmes d’optimisation difficiles en explorant l’espace des solutions selon des règles biologiques simulées.

# 2.2 Modèles Partiellement Bio-inspirés (Hybrides)

Les modèles hybrides bio-inspirés intègrent des composants ou mécanismes issus de la nature dans des modèles d'intelligence artificielle classiques. L’objectif est de tirer profit à la fois de la puissance prédictive des modèles traditionnels (comme les réseaux de neurones, les SVM ou les arbres de décision) et de la flexibilité adaptative des algorithmes bio-inspirés, qui excellent en optimisation, en exploration d’espace de recherche, et en robustesse aux données bruitées ou incomplètes.

### 1. Optimisation des paramètres d’un MLP par algorithme génétique (GA)
### Contexte
Un MLP (Multi-Layer Perceptron) est un réseau de neurones classique, qui nécessite le réglage de nombreux hyperparamètres :
- Nombre de couches et de neurones
- Fonction d’activation
- Taux d’apprentissage
### Critère d’arrêt
- Paramètres d'entraînement (batch size, epochs...)
- La performance d’un MLP dépend fortement de ces hyperparamètres.
# Apport bio-inspiré
Les algorithmes génétiques (GA), introduits par John Holland (1975), sont des techniques d’optimisation stochastiques inspirées de l'évolution naturelle. Chaque solution candidate est encodée sous forme de chromosome (vecteur), et les meilleurs individus (configurations de MLP) sont sélectionnés, croisés, et mutés pour évoluer vers une solution optimale.
## Fonctionnement
- Encodage : Chaque chromosome encode une configuration du MLP (nombre de neurones, taux d’apprentissage...).
- Population initiale : Générée aléatoirement.
- Évaluation : Chaque individu est évalué via une fonction objectif (ex. : erreur RMSE sur les données de validation).
- Sélection, croisement, mutation : Appliqués pour générer une nouvelle population.
- Répétition : Jusqu’à convergence ou un nombre fixe de générations.
### Avantages
- Évite les minima locaux
- Trouve des configurations optimales sans recherche exhaustive
- Très efficace pour les MLP où la recherche manuelle est difficile
# Références
Yao, X. (1999). Evolving artificial neural networks. Proceedings of the IEEE.

Ferreira, C. (2001). Gene expression programming: a new adaptive algorithm for solving problems. Complex Systems.

## 2. Sélection des caractéristiques par systèmes immunitaires artificiels (AIS)
### Contexte
Le choix des variables (features) a un impact majeur sur la performance et la généralisation des modèles. Trop de variables mènent à l’overfitting ; trop peu risquent de perdre l’information utile.
### Apport bio-inspiré
Les systèmes immunitaires artificiels (AIS), inspirés du système immunitaire humain, utilisent des métaphores comme la sélection clonale, la mémoire immunitaire, et la suppression pour détecter, apprendre et mémoriser les modèles pertinents.
### Fonctionnement
- Encodage : Chaque anticorps (solution candidate) encode un sous-ensemble de variables.
- Évaluation : Chaque anticorps est évalué en entraînant un modèle (ex. : SVM) sur les variables sélectionnées.
- Clonage et mutation : Les meilleurs anticorps sont dupliqués avec de petites variations.
- Suppression : Élimination des anticorps redondants ou peu efficaces.
### Avantages
Découvre des sous-ensembles de variables pertinents
Évite l’exploration exhaustive combinatoire
Tolérant au bruit et aux données manquantes
### Références
Dasgupta, D. (2002). Artificial Immune Systems and Their Applications. Springer.
de Castro, L. N., & Timmis, J. (2002). Artificial Immune Systems: A New Computational Intelligence Approach.
### 3. Utilisation d’un Particle Swarm Optimization (PSO) pour entraîner un SVM
### Contexte
- Les SVM (Support Vector Machines) sont puissants pour la classification/régression, mais leur performance dépend fortement du choix des paramètres :
- Coût de régularisation (C)
- Paramètre du noyau (γ dans les RBF)
- Type de noyau (linéaire, polynomial, RBF...)
##  Apport bio-inspiré
Le PSO (Particle Swarm Optimization) est un algorithme d’optimisation inspiré du comportement collectif des oiseaux ou bancs de poissons. Chaque particule explore l’espace des paramètres SVM, influencée par sa meilleure solution individuelle et celle du groupe.
### Fonctionnement
- Encodage : Chaque particule est un vecteur de paramètres SVM (ex : [C, γ]).
- Positionnement : Initialisation aléatoire.
- Évaluation : Chaque particule est évaluée sur une fonction de coût (ex. : précision, RMSE).
- Mouvement : Les particules se déplacent dans l’espace paramétrique, influencées par :
- leur propre historique (meilleur score)
- la meilleure particule du groupe
- Convergence : Vers la meilleure combinaison de paramètres.
### Avantages
- Optimisation globale sans gradient
- Réduction du temps d’essai-erreur
- S’adapte à des fonctions objectifs non convexes
### Références
Kennedy, J., & Eberhart, R. (1995). Particle swarm optimization. IEEE ICNN.

Lin, C.-F., & Wang, S.-D. (2002). Fuzzy support vector machines. IEEE Transactions on Neural Networks.

![image](https://github.com/user-attachments/assets/101c7eea-075a-4406-af85-b144a9c2c28b)

Les modèles hybrides permettent ainsi :
- d’améliorer la performance prédictive
- de réduire la dépendance à l'expertise humaine
- de gagner en robustesse dans des environnements instables ou bruyants, comme celui d’une pandémie.
