# Prédiction du coût des sinistres en assurance automobile

Projet réalisé dans le cadre de la 5e année du cycle ingénieur en Mathématiques Appliquées et Modélisation (MAM) à Polytech Lyon — année universitaire 2026-2027.

## Contexte

La tarification en assurance automobile repose notamment sur l'estimation du risque associé à chaque assuré. Deux éléments sont étudiés :

- **La fréquence des sinistres** : nombre moyen de sinistres sur une période donnée.
- **La sévérité des sinistres** : coût moyen d'un sinistre.

Le coût attendu des sinistres est obtenu en combinant ces deux estimations :

$$
\text{Coût attendu} = \text{Fréquence} \times \text{Sévérité}
$$

Ce projet s'appuie sur l'article scientifique *A Comparison of Generalised Linear Modelling with Machine Learning Approaches for Predicting Loss Cost in Motor Insurance* (Wilson et al., 2024).

## Objectifs

L'objectif est d'étudier et de comparer différentes approches statistiques et de Machine Learning pour prédire le coût des sinistres automobiles.

Les méthodes considérées sont :

- **GLM** : modèles linéaires généralisés.
- **GBM** : Gradient Boosting Machine.
- **ANN** : réseaux de neurones artificiels.
- **Modèle hybride GLM + ANN** : combinaison des approches statistique et neuronale.

Le travail consiste à modéliser séparément la fréquence et la sévérité des sinistres, puis à combiner leurs prédictions pour estimer le coût attendu.

Les performances des différentes méthodes seront ensuite comparées à partir de tests numériques.

## Données

Le projet utilise les jeux de données d'assurance automobile française présentés dans l'article :

- `freMTPL2freq` : caractéristiques des assurés, exposition et nombre de sinistres.
- `freMTPL2sev` : montants des sinistres associés aux contrats.

Ces données sont disponibles dans le package R `CASdatasets`.

## Organisation du dépôt

projet-assurance-ml/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── src/
│   ├── models/
│   │   ├── glm.py
│   │   ├── gbm.py
│   │   ├── ann.py
│   │   └── hybrid.py
│   ├── preprocessing.py
│   └── evaluation.py
├── tests/
├── results/
│   ├── figures/
│   └── metrics/
├── presentation/
│   ├── decembre/
│   └── fevrier/
├── rapport/
├── docs/
├── requirements.txt
└── README.md

## Démarche envisagée

1. Étude de l'article et analyse des données.
2. Nettoyage et préparation des jeux de données.
3. Modélisation de la fréquence et de la sévérité.
4. Développement des différentes approches.
5. Évaluation et comparaison des performances.
6. Analyse des résultats et rédaction du rapport.

## Calendrier

- **Décembre 2026** : présentation de la problématique, des modèles et de la méthodologie.
- **Décembre 2026 – janvier 2027** : développement et expérimentation.
- **11–12 février 2027** : soutenance finale.

## Référence

Wilson, A. A., Nehme, A., Dhyani, A., & Mahbub, K. (2024).

*A Comparison of Generalised Linear Modelling with Machine Learning Approaches for Predicting Loss Cost in Motor Insurance.*

Risks, 12(4), 62.

https://doi.org/10.3390/risks12040062