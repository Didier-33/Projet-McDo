# Analyse d'avis clients de restaurants McDonald's

## 🎯 Objectif

Analyser les avis clients laissés sur plusieurs restaurants McDonald's pour :
- mesurer la satisfaction globale,
- comprendre la répartition des notes (1 à 5),
- comparer les restaurants entre eux,
- visualiser la localisation des restaurants sur une carte.

Ce projet s'inscrit dans ma reconversion vers le métier de Data Analyst. Il fait le lien entre mon expérience passée chez McDonald's et mes nouvelles compétences en analyse de données.

Macdo Projet.pdf
---

## 📂 Données

- Source : dataset public Kaggle (avis de restaurants McDonald's).
- Variables principales utilisées :
  - `store_name` / `store_address` : restaurant,
  - `rating` : note de l'avis (1 à 5),
  - `review` : texte de l'avis,
  - `latitude`, `longitude` : coordonnées du restaurant,
  - `review_time` : moment de l'avis (non exploité en date précise pour ce premier projet).

> Remarque : la colonne `rating_count` n'a pas été utilisée car son sens n'était pas clairement documenté et son import était incohérent.

---

## 🧹 Nettoyage & préparation

Principales étapes réalisées (dans Excel) :

- Import du CSV avec gestion du séparateur et de l'encodage (UTF-8).
- Correction de valeurs mal encodées (ex. `???McDonald's` remplacé par `McDonald's`).
- Suppression d'une ligne manifestement corrompue (`2476 Kal…` sans coordonnées).
- Vérification des types de données (notes en numérique, etc.).

Un premier tableau croisé dynamique a permis de :
- compter le nombre d'avis par restaurant et par note,
- vérifier la cohérence des données avant de passer à Power BI.

---

## 📊 Analyses et visualisations (Power BI)

Les analyses ont été réalisées dans Power BI à partir des données nettoyées.

### Indicateurs clés

- **Nombre total d'avis** : 
- **Note moyenne globale** :

### Visuels principaux

- **KPI** : nombre d'avis total et note moyenne globale.
- **Répartition des notes** :
  - graphique montrant la proportion de notes 1, 2, 3, 4 et 5.
- **Comparaison des restaurants** :
  - graphiques permettant de voir quels restaurants ont la meilleure / la moins bonne note moyenne.
- **Carte** :
  - visualisation des restaurants sur une carte grâce à `latitude` / `longitude`.

---

## 🧠 Exemple d'insights

- La note moyenne globale est de **3,13/5**, ce qui indique une satisfaction moyenne, avec des avis très contrastés.
- La répartition des notes montre une forte part de **notes 5**, mais également un volume non négligeable de **notes 1**, ce qui traduit une expérience client inégale selon les restaurants.
- Certains restaurants se démarquent avec un volume important d'avis et une note moyenne supérieure ou inférieure à la moyenne globale.

---

## 🛠️ Outils utilisés

- **Excel** : import, nettoyage, tableaux croisés dynamiques.
- **Power BI Desktop** : modélisation simple, mesures DAX (moyenne des notes), visualisations (KPI, graphiques, carte).

---

## 🔁 Pistes d'amélioration

Pour aller plus loin, je pourrais :
- analyser le texte des avis (`review`) pour détecter les thèmes récurrents (qualité, temps d'attente, service…),
- créer des indicateurs supplémentaires (taux d'avis positifs/négatifs par restaurant, etc.).

