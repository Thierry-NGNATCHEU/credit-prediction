  
Projet Machine Learning – Analyse et Prédiction Clientèle Bancaire  
---------------------------------------------------------------
Auteurs : NGNATCHEU THIERRY & NGUEKOUO CINTHIA 

👋 Bienvenue !

Ce projet a été réalisé dans le cadre d’un travail en Machine Learning appliqué à un dataset bancaire. Le but : utiliser les données de clients pour comprendre leurs comportements et prédire deux choses essentielles pour une banque :

1. Est-ce qu’un client va accepter un prêt personnel ? (classification)
2. Quel est le revenu estimé d’un client ? (régression)

L’approche est complète : nettoyage des données, traitement des valeurs manquantes, exploration visuelle, modélisation avec plusieurs algorithmes, évaluation des performances... et en bonus : une simulation en live avec le public à la fin.

---

 Ce qu'on a dans le jeu de données

- Source : https://www.kaggle.com/code/bmag8923/alllife-bank-loan-predictions?select=Bank_Personal_Loan_Modelling.csv
- Fichier utilisé : Financial_Datasets.csv

Le jeu de données contient des infos classiques sur les clients : âge, niveau d'éducation, revenu, utilisation de carte de crédit, prêt immobilier, etc.
 
Voici un aperçu rapide :

- Age / Experience : âge et années d'expérience
- Income : revenu annuel
- Family : taille du foyer
- Education : niveau d’étude (1 = Undergraduate à 3 = Graduate)
- CCAvg : dépenses mensuelles avec carte de crédit
- Mortgage, CD Account, Online, etc.

Certaines valeurs manquantes ont été intentionnellement ajoutées pour tester le pipeline de nettoyage. On les a traitées de deux manières :
- Par imputation médiane pour les cas simples
- Par modèle de régression quand une meilleure prédiction était possible (ex. : prédire l'expérience à partir de l'âge)

---

 Standardisation & Visualisation

Les variables numériques comme le revenu ou l'âge ont été standardisées pour éviter que certaines dominent les autres lors de l'entraînement des modèles. On a comparé les données avant et après pour vérifier que la transformation était bien faite (graphiques inclus).

---

 Modèles utilisés

Pour chaque tâche classification et régression, on a testé 4 modèles différents :
-  Deux modèles ensemblistes (Random Forest, Gradient Boosting, Stacking, Bagging)
-  Un modèle appris en cours (Naive Bayes, Régression linéaire)
-  Un modèle plus original (SVR, KNN.)
---

 Métriques utilisées :

- Pour la classification : accuracy, recall, AUC, precision
- Pour la régression : R², RMSE, MAE

---

 
Structure du projet :
- classification.ipynb : Notebook pour la tâche de classification
- regression.ipynb : Notebook pour la tâche de régression
- environment.yml : Fichier pour créer l'environnement jupyter
- README.txt : Ce fichier de documentation


