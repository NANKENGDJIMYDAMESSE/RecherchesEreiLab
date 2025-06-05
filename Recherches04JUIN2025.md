# Rapport de Recherche Scientifique Évaluation et Optimisation Énergétique des Modèles de Deep Learning pour la Détection de Pneumonie sur Radiographies Thoraciques
## Résumé
Ce rapport étudie l'efficacité, la précision et l'empreinte énergétique de modèles de Deep Learning appliqués à la détection de la pneumonie à partir du jeu de données RSNA Pneumonia Challenge. En s’appuyant sur des métriques précises de performance, de complexité et de durabilité (Green AI), nous comparons un modèle ResNet-50 de base avec deux variantes optimisées : par quantification post-entraînement et par network pruning. L’étude démontre l’importance croissante d’une IA plus éco-efficace, tout en maintenant une performance clinique acceptable.
## Mots-clés
RSNA Pneumonia, Deep Learning, ResNet-50, Quantification, Network Pruning, IA verte, CO₂eq, Accuracy, F1-Score, Inference Time, FLOPs, Parameter Count.
# 1. Introduction
La montée en puissance des algorithmes de Deep Learning dans le domaine médical s’accompagne de préoccupations croissantes sur leur coût computationnel et écologique. Ce travail vise à évaluer la pertinence de techniques d’optimisation – quantification et pruning – sur ResNet-50 dans le cadre de la détection automatisée de pneumonies. En exploitant le dataset RSNA Pneumonia, nous analysons la balance entre précision diagnostique et durabilité énergétique.
# 2. Jeu de Données : RSNA Pneumonia Challenge
Le jeu de données contient des radiographies thoraciques annotées pour la présence ou non de signes de pneumonie, selon des experts radiologues. Il comporte :

- Environ 26 000 images au format DICOM.

- Trois classes : "Normal", "Pneumonia", "Uncertain".

- Dimensions originales : 1024×1024 pixels, converties et redimensionnées à 224×224×3 pour ResNet.
![image](https://github.com/user-attachments/assets/7167fef7-e548-4ed4-a3d9-8720ed8e9df0)
# 4. Architecture et Optimisations
## 4.1. Modèle de Base : ResNet-50
- Initialisé avec poids pré-entraînés sur ImageNet.

- Fine-tuning sur RSNA avec 3 classes.

- Taille du modèle : ~98 MB, 25.6M paramètres.

## 4.2. Quantification (PTQ)
- Réduction des poids 32 bits en 8 bits.

- Outils : torch.quantization.

- Objectif : Réduire taille et temps d'inférence sans perte majeure de précision.

## 4.3. Network Pruning
- Suppression des poids faibles (inférieurs à un seuil).

- Technique : Pruning itératif avec ré-entraînement.

- Réduction jusqu’à 50% des paramètres sans perte de performance.
![image](https://github.com/user-attachments/assets/23ec3862-2742-491b-b941-a8c1ea778cd9)
# 6. Analyse Comparative et Interprétation
- Performance : Légère perte de précision après quantification et pruning, mais dans des limites acceptables pour des applications cliniques.

- Gains énergétiques : Jusqu’à 46% de réduction de consommation avec le modèle pruné.

- Efficacité énergétique : Amélioration du ratio précision/Wh d’environ 35% pour le modèle pruné.

# Conclusion : 
Les techniques d’optimisation permettent des modèles plus écologiques sans sacrifier significativement la performance.

Les résultats démontrent qu’il est possible d’optimiser des architectures lourdes comme ResNet-50 pour des tâches médicales tout en réduisant considérablement leur empreinte énergétique. Quantification et pruning sont complémentaires et ouvrent la voie à une IA verte plus responsable.


# Points clés de la solution proposée :

Acquisition des données de pneumonie : Intégration d'un script de téléchargement (ou d'instructions claires) pour le dataset RSNA Pneumonia Detection Challenge, car c'est la cause principale de votre FileNotFoundError.
Dataset plus robuste : Utilisation de pydicom pour lire les fichiers .dcm natifs du dataset RSNA, ce qui est plus standard que de supposer des .png ou .jpg issus d'une conversion externe.
Implémentation du Pruning : Ajout de la logique PyTorch pour l'élagage (pruning) du modèle entraîné.
Métriques plus explicites : Ajout de fonctions d'évaluation claires pour calculer et afficher l'Accuracy, le F1-Score, le nombre de paramètres, le temps d'inférence, la taille du modèle, et des estimations de l'énergie/CO2eq.
Tableau Comparatif : Génération d'un tableau comparatif Pandas affichant toutes les métriques pour les modèles Baseline, Quantifié et Pruné.
Gestion de CodeCarbon : Utilisation de EmissionsTracker pour l'entraînement. Pour l'inférence, les valeurs d'énergie et de CO2eq seront des estimations ou des placeholders car une mesure précise en direct est complexe.
Pré-requis pour faire fonctionner ce code (TRÈS IMPORTANT) :

Accès à Kaggle : Le dataset RSNA Pneumonia Detection Challenge est sur Kaggle. Vous devrez installer la CLI de Kaggle et configurer vos identifiants.
Espace Disque : Le dataset est volumineux (~15 Go).






