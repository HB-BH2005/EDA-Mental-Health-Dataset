# Analyse Exploratoire des Données (EDA) - Mental Health Dataset

## Équipe du Projet

| Nom | GitHub |
|------|---------|
| **Hadil Barzani** | https://github.com/HB-BH2005 |
| **Ijlal Sellak** | https://github.com/ijlal-sellak |

---

## Description du Projet

Ce projet porte sur une **analyse exploratoire des données (EDA)** réalisée sur un jeu de données synthétique lié à la santé mentale.

L’objectif principal est d’explorer et comprendre les données avant toute phase de modélisation :

- Comprendre la structure du dataset  
- Identifier les anomalies et incohérences  
- Nettoyer et préparer les données  
- Étudier les distributions et relations entre variables  
- Extraire des insights utiles pour une future analyse avancée  

> ⚠️ La partie modélisation est présentée uniquement à titre d’exemple pour illustrer une application possible des données après l’EDA.

---

# Jeu de Données

Le dataset est une **simulation synthétique** de 10 000 individus représentant une enquête sur la santé mentale.

Il contient des variables :

- Démographiques
- Professionnelles
- Comportementales
- Psychologiques

---

## Variables principales

| Catégorie | Variables |
|---|---|
| Démographie | `age`, `gender` |
| Profession | `employment_status`, `work_environment` |
| Santé mentale | `mental_health_history`, `seeks_treatment`, `mental_health_risk` |
| Habitudes de vie | `sleep_hours`, `physical_activity_days`, `stress_level` |
| Scores psychologiques | `depression_score`, `anxiety_score`, `social_support_score`, `productivity_score` |

---

# Table des Matières

1. Chargement et aperçu des données  
2. Nettoyage des données  
3. Analyse univariée  
4. Analyse bivariée  
5. Analyse multivariée  
6. Clustering exploratoire  
7. Réduction de dimension (PCA)  
8. Détection des anomalies  
9. Feature engineering  
10. Exemple de modélisation (optionnel)  
11. Visualisation finale et storytelling  

---

# 1. Chargement et Aperçu des Données

Les données ont été chargées avec Pandas afin de :

- Visualiser les premières lignes  
- Vérifier les types de données  
- Comprendre la structure globale  
- Observer les statistiques de base  

Taille du dataset :
- 10 000 lignes  
- 14 colonnes  

---

# 2. Nettoyage des Données

- Vérification des valeurs manquantes : aucune valeur critique détectée  
- Nettoyage de la variable `gender`  
- Gestion des valeurs `"Prefer not to say"`  
- Création d’une variable propre `Gender_clean`  

---

# 3. Analyse Univariée

## Variables numériques

Analyse des distributions avec :

- Histogrammes
- KDE plots
- Boxplots
- Statistiques descriptives

## Variables catégorielles

Analyse des fréquences avec :

- value_counts()
- countplot

---

# 4. Analyse Bivariée

## Corrélations

- Matrice de corrélation
- Pairplots
- Scatter plots

## Relations étudiées

- stress_level vs depression_score  
- sleep_hours vs productivity_score  

---

## Test du Chi²

Analyse des dépendances entre variables catégorielles.

Résultats :

- Certaines relations significatives (ex: seeks_treatment vs mental_health_risk)
- Majorité des relations non significatives

---

# 5. Analyse Multivariée

## Clustering (KMeans)

Application de KMeans pour explorer des groupes d’individus similaires.

## PCA

Réduction de dimension pour visualiser les données en 2D et 3D.

## Profils observés

- Groupe avec forte détresse psychologique  
- Groupe productif mais stressé  
- Groupe globalement équilibré  

---

# 6. Détection des Anomalies

- Méthode IQR utilisée  
- Visualisation avec boxplots  
- Peu d’outliers significatifs détectés  

---

# 7. Feature Engineering

Création de nouvelles variables :

- high_mental_risk  
- stress_category  
- sleep_deficit  
- support_category  

---

# 8. Modélisation (Exemple uniquement)

Une modélisation simple a été réalisée à titre illustratif.

- Algorithme : Random Forest Classifier  
- Objectif : prédire le risque mental élevé  

⚠️ Cette étape n’est pas le focus principal du projet et sert uniquement de démonstration.

---

# 9. Visualisation Finale & Storytelling

Analyse de l’impact du stress sur le risque mental.

Conclusion principale :

- Le stress est fortement corrélé au risque mental élevé  

---

# Conclusion Générale

Ce projet se concentre principalement sur l’EDA et permet de :

- Comprendre les données en profondeur  
- Identifier des tendances importantes  
- Préparer une base solide pour du machine learning futur  

La modélisation est optionnelle et uniquement illustrative dans ce contexte.
