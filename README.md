# AI Impact on Students — Projet Lakehouse avec Databricks

Ce projet présente une démarche de science des données réalisée avec Databricks Free Edition, PySpark, Delta Tables et une approche lakehouse simplifiée.

L’objectif est d’analyser un jeu de données portant sur l’impact de l’intelligence artificielle générative sur les étudiants, en structurant les données selon une logique Bronze, Silver et Gold, avant de réaliser une analyse exploratoire et une première expérimentation de machine learning.

## Version HTML du projet

Le notebook exécuté est publié sous forme de page HTML avec GitHub Pages :

https://aidatamodels.github.io/ai-impact-students-lakehouse-databricks/

Cette version permet de consulter le projet de manière plus fluide, sans dépendre du rendu parfois limité des notebooks volumineux dans GitHub.

## Objectifs du projet

Ce projet vise à démontrer une démarche complète de traitement et d’analyse de données dans Databricks :

- ingestion d’un fichier CSV dans un volume Unity Catalog ;
- création d’une table Bronze à partir des données brutes ;
- nettoyage et standardisation des données dans une table Silver ;
- création de tables Gold pour l’analyse exploratoire ;
- préparation d’une variable cible pour le machine learning ;
- entraînement d’un modèle Random Forest ;
- évaluation critique des résultats obtenus ;
- publication du notebook sous forme de rapport HTML.

## Source des données

Le jeu de données utilisé provient de Kaggle :

AI Impact on Students  
https://www.kaggle.com/datasets/laveshjadon/ai-impact-on-students

Le fichier CSV original a été téléchargé depuis Kaggle, puis téléversé manuellement dans un volume Unity Catalog de Databricks.

Le dataset original n’est pas inclus directement dans ce dépôt. Pour reproduire le projet, il doit être téléchargé depuis la page Kaggle officielle, en respectant les conditions d’utilisation et la licence associées au jeu de données.

## Architecture des données

Le projet suit une démarche lakehouse simplifiée.

```text
Dataset Kaggle CSV
        ↓
Unity Catalog Volume
        ↓
Bronze Delta Table
        ↓
Silver Delta Table
        ↓
Gold Analytical Tables
        ↓
Machine Learning Predictions
