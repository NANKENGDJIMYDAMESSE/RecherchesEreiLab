# Rapport de Recherche Scientifique : Évaluation et Optimisation de l'Impact des Algorithmes
# Résumé
Ce rapport de recherche examine en profondeur les mécanismes d'évaluation des algorithmes, en détaillant les métriques fondamentales et leurs formulations mathématiques, ainsi que le rôle des constantes dans la régulation du comportement algorithmique. Nous couvrons spécifiquement les algorithmes génétiques, bio-inspirés et non bio-inspirés, en citant les auteurs pionniers de ces domaines. De plus, nous explorons des techniques avancées d'optimisation de modèles d'IA, telles que la quantification et le network pruning, en soulignant leur développement historique. Enfin, nous évaluons leur impact à travers le prisme des métriques de Green AI, une approche émergente pour l'évaluation de l'efficacité énergétique et l'empreinte carbone, afin de promouvoir une intelligence artificielle plus durable.
# Mots-clés
- Métriques algorithmiques,
- Évaluation d'algorithmes,
- Algorithmes génétiques,
- Algorithmes bio-inspirés,
- Algorithmes non bio-inspirés,
- Constantes algorithmiques,
- Optimisation,
- Quantification,
- Network Pruning,
- Green AI,
- Efficacité énergétique,
- Empreinte carbone.
# 1. Introduction
L'essor fulgurant de l'intelligence artificielle (IA) a transformé de nombreux domaines, mais il a également mis en lumière l'importance d'évaluer non seulement la performance intrinsèque des algorithmes, mais aussi leur impact environnemental. Ce rapport s'articule autour de trois axes majeurs : d'abord, une explication des métriques d'évaluation et des constantes de paramétrage essentielles à tout algorithme, en rendant hommage aux contributions fondamentales des chercheurs ; ensuite, une exploration des techniques de réduction de la complexité des modèles comme la quantification et le network pruning, en retraçant leur origine et leur évolution ; et enfin, une analyse de l'impact de ces techniques sur les métriques de Green AI, offrant une perspective sur l'efficacité énergétique et la durabilité de l'IA.
# 2. Métriques d'Évaluation des Algorithmes
Les métriques sont des outils quantitatifs indispensables pour mesurer et comparer la performance et la qualité des solutions produites par les algorithmes. Leur formalisation a été essentielle au développement de l'informatique scientifique.
# 2.1. Métriques de Performance Algorithmique
Ces métriques évaluent l'efficience de l'algorithme lui-même.
- Temps d'exécution : Une mesure empirique du temps écoulé, fondamentale depuis les débuts de l'informatique.
- Complexité Spatiale et Complexité Temporelle : Les concepts de complexité algorithmique ont été formalisés par des pionniers comme Alan Turing (machines de Turing, 1936), Alonzo Church (lambda-calcul, 1936) et plus tard par des informaticiens comme Donald Knuth (série "The Art of Computer Programming", débutée en 1968).
- Nombre d'Itérations : Un simple décompte des cycles ou étapes, une métrique utilisée dans la plupart des algorithmes itératifs.
# 3. Explication des Constantes Utilisées dans les Algorithmes
Les constantes sont des paramètres fixes qui contrôlent le comportement et les performances d'un algorithme. Leur ajustement est crucial pour optimiser l'algorithme en fonction du problème spécifique.

## 3.1. Algorithmes Génétiques (AG)
Inspirés de l'évolution biologique, les AG utilisent des constantes pour guider les processus de sélection, de croisement et de mutation. Les travaux fondateurs ont été menés par John Holland dans les années 1960 et 1970 (ouvrage "Adaptation in Natural and Artificial Systems", 1975) . David E. Goldberg a popularisé et approfondi les AG dans les années 1980 (ouvrage "Genetic Algorithms in Search, Optimization, and Machine Learning", 1989) .
### Formulation mathématique de l’Algorithme Génétique
![image](https://github.com/user-attachments/assets/11553d39-6be5-4c3f-a0dc-691748a1949c)
![image](https://github.com/user-attachments/assets/04475352-4cec-4dd8-abde-1a1b7812c96f)
![image](https://github.com/user-attachments/assets/d771cb76-b238-4031-ba66-f2ec3d3cf7ce)
# 4. Formulation mathématique globale des techniques d’optimisation d’algorithmes
## Objectif général
![image](https://github.com/user-attachments/assets/cb487077-8748-4238-ac39-a005f887cb89)
![image](https://github.com/user-attachments/assets/233f9a35-c287-47a9-b9a6-bb74da85df2f)
![image](https://github.com/user-attachments/assets/2f16f68a-f233-41cc-a2bd-dc361022b607)
![image](https://github.com/user-attachments/assets/91ae1c4a-44f3-4978-8326-623676b5974e)
![image](https://github.com/user-attachments/assets/ca1ab339-4170-41bb-9251-63d2e968f74a)
![image](https://github.com/user-attachments/assets/d9402673-69de-4dc2-b0f8-977d34e1d0fe)
![image](https://github.com/user-attachments/assets/089eef48-d7b0-47f6-a5b4-247c0ba28eba)
# 5. Évaluation de l'Impact sur les Métriques de Green AI
L'attention croissante portée à l'impact environnemental de l'IA a conduit à l'émergence du concept de "Green AI". Ce domaine relativement récent a été formalisé par des initiatives et des publications, notamment des rapports de la Green Software Foundation (depuis 2021) et des analyses de l'IEA (International Energy Agency) (rapports annuels sur l'énergie et l'IA) [20, 21].

## 5.1. Métriques de Green AI
Consommation Énergétique (Energy Consumption) : Mesurée en Watt-heures (Wh) ou Joule (J). L'intégration de ces mesures dans les évaluations de l'IA est devenue plus systématique avec des outils comme le Green Metrics Tool développé par green-coding.io (depuis 2022).
- Formulation : E=P
timest, où P est la puissance moyenne et t est le temps d'exécution.
Émissions de Carbone Équivalent (
textCO_2eq) : Calculées à partir de la consommation énergétique et de l'intensité carbone du réseau électrique. Des études pionnières sur l'empreinte carbone des modèles d'IA ont été menées par Strubell, Ganesh, et McCallum (article "Energy and Policy Considerations for Deep Learning in NLP", 2019), qui ont mis en évidence l'importante consommation d'énergie de certains grands modèles .
Formulation :
textCO_2eq=E
times
textCarbonIntensity
Nombre de Paramètres (Parameter Count) : Une métrique clé pour la taille du modèle, directement liée aux coûts de calcul et d'énergie.
FLOPS (Floating Point Operations Per Second) : Une métrique indirecte de la charge de calcul, utilisée depuis les premières analyses de performance des processeurs.
Temps d'Inférence (Inference Time) : Le temps nécessaire pour qu'un modèle fasse une prédiction, essentiel pour l'efficacité énergétique en phase de déploiement.
Efficacité Énergétique (Energy Efficiency) : Performance du modèle par unité d'énergie consommée (par exemple, Accuracy/kWh).




# Projet de Deep Learning : Détection de Chiffres MNIST avec ResNet et Impact Green AI
## 1. Introduction
Ce projet de Deep Learning vise à explorer l'application d'une architecture de réseau neuronal complexe, ResNet-50, à un problème de classification plus simple : la reconnaissance de chiffres manuscrits du célèbre dataset MNIST. Au-delà de l'atteinte d'une performance de classification élevée, un objectif central de ce projet est d'évaluer l'empreinte environnementale des modèles de Deep Learning. Nous analyserons l'impact de l'entraînement et de l'inférence, en mesurant la consommation de ressources et les émissions de carbone, et en explorant l'efficacité de techniques d'optimisation comme la quantification et le pruning dans le cadre de l'IA Verte.

## 2. Contexte et Problématique
L'explosion de l'IA a mis en lumière la puissance des modèles de Deep Learning, mais aussi leur coût énergétique. Des architectures comme ResNet, bien que très performantes sur des tâches complexes d'imagerie, demandent des ressources considérables. Comprendre le compromis entre performance et efficacité énergétique est crucial, surtout lorsqu'on adapte ces modèles à des tâches moins exigeantes. MNIST, avec ses images de petite taille et sa classification à 10 classes, offre un terrain de jeu idéal pour cette exploration.

## 3. Objectifs du Projet
Ce projet se décline en plusieurs objectifs clés, couvrant la modélisation, l'évaluation de performance et l'analyse de l'impact environnemental :

### 3.1 Objectifs Techniques
Préparation des Données MNIST : Adapter les images MNIST (28x28, niveaux de gris) pour les rendre compatibles avec l'entrée de ResNet-50 (32x32, 3 canaux), en appliquant un padding et une duplication des canaux, suivis d'un pré-traitement spécifique à ResNet.
Implémentation et Entraînement du Modèle ResNet-50 : Construire un modèle de classification à 10 classes en utilisant une architecture ResNet-50 pré-entraînée sur ImageNet, en gelant les couches de base et en entraînant une nouvelle tête de classification adaptée à MNIST.
Évaluation de la Performance : Mesurer la précision (Accuracy) et le F1-Score du modèle sur l'ensemble de test, ainsi que la matrice de confusion et le rapport de classification.
### 3.2 Objectifs d'Optimisation et d'IA Verte
Quantification Post-Entraînement (PTQ) : Appliquer la quantification sur le modèle ResNet-50 entraîné pour réduire sa taille et potentiellement son temps d'inférence.
Network Pruning : Mettre en œuvre le pruning (élagage) pour réduire la complexité du modèle en supprimant les connexions moins importantes, et ré-entraîner le modèle pruné.
Mesure des Métriques de Green AI : Utiliser des outils comme codecarbon pour estimer la consommation d'énergie et les émissions de CO2 équivalent (CO2eq) pendant l'entraînement des modèles (non optimisé et pruné).
Analyse Comparative : Comparer la taille des modèles, les temps d'inférence, la consommation énergétique et les émissions de CO2eq entre le modèle original et les modèles optimisés.
Interprétation de l'Impact : Analyser le compromis entre la performance du modèle et son empreinte environnementale, en mettant en évidence l'efficacité des techniques d'optimisation pour une IA plus durable.
# 4. Résultats Attendus
À l'issue de ce projet, nous devrions être en mesure de démontrer :

La capacité d'un modèle ResNet-50 à classer les chiffres MNIST avec une haute précision, même après adaptation de l'entrée.
Une réduction significative de la taille du modèle et du temps d'inférence grâce à la quantification et au pruning.
Une quantification de l'impact carbone des phases d'entraînement des modèles non optimisés et optimisés.
Des conclusions claires sur l'efficacité des techniques d'optimisation pour construire des modèles de Deep Learning plus "verts" et plus économes en ressources.





