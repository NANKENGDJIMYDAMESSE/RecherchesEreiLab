# AVANTAGES, DIFFÉRENCES ENTRE PYTORCH ET PYTORCH LIGHTNING & LEUR IMPACT GREEN IT / IT FOR GREEN
## Introduction
Le développement de modèles d’apprentissage profond (deep learning) repose largement sur des frameworks performants. PyTorch est reconnu pour sa flexibilité, tandis que PyTorch Lightning se distingue par sa capacité à structurer et simplifier les workflows. Mais au-delà de la performance algorithmique, un enjeu émerge : l’impact environnemental de l’IA. À ce titre, il est essentiel d’analyser ces frameworks à travers le prisme du Green IT et de l’IT for Green.
## Présentation rapide
###  PyTorch
Framework bas niveau, orienté recherche, permettant un contrôle complet sur la logique d’entraînement et la gestion des ressources.

### PyTorch Lightning
Surcouche haut niveau qui structure les projets PyTorch, réduit le code redondant et automatise de nombreuses tâches (GPU, logs, scalabilité...).

###  Green IT & IT for Green
### Green IT
Le Green IT désigne les pratiques visant à réduire l’impact environnemental du numérique : consommation énergétique, émissions de CO2, efficacité des ressources (GPU, CPU, RAM...).

### IT for Green
L’IT for Green consiste à utiliser les technologies numériques pour réduire l’impact écologique d’autres secteurs : agriculture, santé, transport, etc., en optimisant les ressources grâce à l’intelligence artificielle, par exemple.
## Contribution de PyTorch Lightning au Green IT
| Aspect                                 | PyTorch                     | PyTorch Lightning                               | Avantage Green                                                       |
| -------------------------------------- | --------------------------- | ----------------------------------------------- | -------------------------------------------------------------------- |
| **Gestion automatique des ressources** | Manuel                      | Oui (via `Trainer`, `accelerator`, `precision`) | ⚡ Optimise l’utilisation des GPU / CPU, réduit les cycles inutiles   |
| **Mixed Precision (FP16)**             | Doit être codé manuellement | Oui (`precision=16`)                            | ⚡ Réduit la consommation mémoire et énergétique                      |
| **Entraînement distribué**             | Complexe                    | Automatique (`ddp`, `tpu`)                      | ⚡ Exécute les tâches plus rapidement, donc moins d’énergie globale   |
| **Monitoring facile**                  | Non natif                   | Oui (WandB, TensorBoard)                        | ⚡ Aide à repérer les surentraînements inutiles et à stopper plus tôt |
| **Reproductibilité**                   | Doit être gérée à la main   | Intégrée                                        | ⚡ Moins d'essais répétés → économies d’énergie et de temps machine   |
Avantages IT for Green
## En structurant efficacement les projets IA, PyTorch Lightning permet :

- ✅ Une mise en production rapide de solutions d’IA durables (agriculture de précision, détection médicale, smart cities…)

- ✅ Une expérimentation optimisée : moins d’essais, plus d’efficacité énergétique

- ✅ Une meilleure collaboration interdisciplinaire (data scientists, ingénieurs, experts métier) autour de solutions "IT for Green"

Exemple : Un projet de détection de maladies pulmonaires via IA peut être développé avec PyTorch Lightning, quantifié, pruné et entraîné plus rapidement, ce qui réduit son coût carbone tout en apportant une contribution "IT for Green" au domaine de la santé.
##  Synthèse des différences principales
| Critère                                       | PyTorch           | PyTorch Lightning                                                          |
| --------------------------------------------- | ----------------- | -------------------------------------------------------------------------- |
| Contrôle du code                              | Total             | Abstrait et structuré                                                      |
| Apprentissage distribué                       | Complexe          | Simple et optimisé                                                         |
| Support Green IT (quantification, FP16, etc.) | Manuel            | Automatisé                                                                 |
| Logique de recherche                          | Flexible          | Moins adaptée aux cas ultra personnalisés                                  |
| Réduction de l’empreinte carbone              | Limité par défaut | Facilite par défaut (moins d’overfitting, précision mixte, early stopping) |
##  Conclusion
-  PyTorch reste la référence pour la recherche exploratoire, avec un contrôle total du code et de l’architecture. 
-  PyTorch Lightning se distingue pour les projets scalables, reproductibles, et respectueux de l’environnement. 

En intégrant les principes de Green IT et d’IT for Green, PyTorch Lightning permet de construire des modèles plus écologiques, plus rapides, et mieux structurés — ce qui en fait un choix idéal pour les ingénieurs conscients des impacts climatiques de l’IA moderne.

# Projet : Diagnostic de Pneumonie par IA Écologique avec ResNet et PyTorch Lightning
- Ce projet vise à développer un système de diagnostic de pneumonie à partir de radiographies thoraciques (dataset RSNA Pneumonia) en utilisant une architecture ResNet-50. Notre objectif n'est pas seulement d'atteindre une haute précision, mais aussi d'évaluer et de réduire l'empreinte carbone du modèle.

## Objectifs Clés
- Préparation des Données RSNA : Adapter et augmenter le dataset RSNA Pneumonia pour l'entraînement d'un modèle de classification binaire.
- Modélisation avec PyTorch Lightning : Implémenter et entraîner un ResNet-50 pré-entraîné, en utilisant la structure modulaire et reproductible de PyTorch Lightning pour la classification de la pneumonie.
- Évaluation de Performance : Mesurer des métriques clés comme l'Accuracy, le F1-Score, la sensibilité, la spécificité et l'AUC-ROC pour valider la performance clinique du modèle.
- Optimisation et IA Verte : Appliquer des techniques d'optimisation comme la quantification et le pruning pour réduire la taille et les temps d'inférence du modèle.
- Mesure d'Impact Carbone : Utiliser CodeCarbon (intégré à PyTorch Lightning) pour quantifier la consommation énergétique et les émissions de CO2eq des phases d'entraînement.
- Analyse Comparative : Comparer les performances, la taille du modèle et l'empreinte environnementale entre les modèles original et optimisés pour démontrer l'efficacité de l'IA Verte.
## Résultats Attendus
Nous prévoyons de démontrer qu'un ResNet-50 entraîné avec PyTorch Lightning peut diagnostiquer la pneumonie avec une grande efficacité. De plus, nous montrerons que l'optimisation (quantification, pruning) permet de réduire significativement la taille du modèle et l'impact carbone, prouvant qu'une IA performante peut aussi être plus durable.























