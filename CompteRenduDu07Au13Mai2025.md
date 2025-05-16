# Rapport de Réunion 
# Titre de la réunion : Comparaison approfondie des modèles bio-inspirés, hybrides et traditionnels dans la modélisation prédictive épidémiologique : Étude de cas sur le COVID-19
# I.  Objectifs de la séance
- Clarifier les notions fondamentales de modèles bio-inspirés et partiellement bio-inspirés à partir de sources scientifiques référencées.

- Comparer ces modèles à des approches non bio-inspirées dans le contexte de la prédiction du taux de reproduction du virus SARS-CoV-2.

- Intégrer ces travaux dans une perspective de recherche orientée Green IT / IT for Green.

- Identifier des pistes d’optimisation énergétique et de réduction d’empreinte carbone pour les modèles d’intelligence artificielle utilisés.
# II.  Clarification des concepts clés
- 1. Modèles bio-inspirés (purs)
Inspirés directement de mécanismes biologiques : évolution, comportement collectif, système immunitaire.

Exemples : algorithmes génétiques (Holland, 1975), PSO (Kennedy & Eberhart, 1995), ACO (Dorigo, 1999), AIS (Dasgupta, 2002).

Structure et fonctionnement global 100% biologiquement inspirés.

- 2. Modèles partiellement bio-inspirés (hybrides)
Intègrent une structure classique (MLP, SVM, etc.) et une composante d’optimisation bio-inspirée (ex. : GA, PSO).

Exemples :

MLP + GA : réseau de neurones optimisé par algorithme génétique.

SVM + PSO : réglage automatique des hyperparamètres via essaim de particules.

Régression linéaire + GA : sélection de variables via un processus évolutif.

- 3. Modèles non bio-inspirés (traditionnels)
Fondés sur des techniques purement statistiques ou déterministes.

Exemple principal : Random Forest (ensemble d’arbres de décision, méthode algorithmique non inspirée de la nature).
# III.  Expérimentation : Prédiction COVID-19

| Modèle          | Type                | Bio-inspiré ? | Optimisation             | Cible               | Résultats (exemples) |
| --------------- | ------------------- | ------------- | ------------------------ | ------------------- | -------------------- |
| Random Forest   | Classique           | ❌             | Aucun                    | `reproduction_rate` | RMSE : 0.0872        |
| Régression + GA | Partiel             | ✅             | Feature selection via GA | `reproduction_rate` | RMSE : 0.1023        |
| MLP + GA        | Hybride bio-inspiré | ✅✅            | Hyperparamètres via GA   | `reproduction_rate` | RMSE : 0.0761        |
# IV.  Green IT / IT for Green
## Concepts clés abordés :
- Green IT : réduire l’empreinte carbone des systèmes informatiques (via efficacité énergétique, architecture).

- IT for Green : utiliser les technologies de l’information pour réduire l’impact écologique d'autres secteurs.

## Liens avec les modèles IA :
- L’algorithme génétique, bien qu’efficace en optimisation, est coûteux énergétiquement (évaluation multi-générationnelle).

- Les modèles hybrides (MLP + GA) offrent excellente précision, mais au prix d’un temps de calcul élevé, d’où l’importance d’évaluer leur empreinte environnementale.
# V.  Évaluation énergétique et impact environnemental (proposition de méthodologie)
| Métrique                      | Objectif                                                           |
| ----------------------------- | ------------------------------------------------------------------ |
| **Temps d’exécution**         | Mesure de performance brute                                        |
| **Utilisation CPU/GPU**       | Mesure de consommation énergétique (via `psutil` ou `GPUtil`)      |
| **Estimation CO₂ (kg)**       | À calculer via outils comme [codecarbon.io](https://codecarbon.io) |
| **Rapport précision/énergie** | Pour un arbitrage performance vs coût environnemental              |
# VI. Recommandations
- Intégrer outils de mesure énergétique (e.g., codecarbon, carbontracker) dans l’évaluation des modèles IA.

- Favoriser des modèles sobres énergétiquement si la perte de précision reste acceptable.

- Documenter systématiquement l’impact énergétique des algorithmes IA dans les travaux de recherche (pratique scientifique responsable).

- Envisager une normalisation méthodologique : toujours présenter RMSE, temps, énergie, CO₂.
# VII.  Synthèse de la réunion
| Axe discuté                  | Résultat                                                                  |
| ---------------------------- | ------------------------------------------------------------------------- |
| Compréhension des modèles IA | Clarification des types et structures (bio-inspiré / hybride / classique) |
| Lien avec Green IT           | Identifié comme critique et sous-estimé                                   |
| Métriques d’évaluation       | Nécessité d’ajouter empreinte carbone aux critères standards              |
| Méthodologie scientifique    | À renforcer sur les aspects énergétiques                                  |
| Perspectives                 | Article scientifique + prototype avec évaluation énergétique              |
# VIII.  Travaux à réaliser





















