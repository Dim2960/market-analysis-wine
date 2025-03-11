# Market Analysis - Domaine des Croix

Bienvenue dans ce projet d’analyse de données pour le **Domaine des Croix**, un vignoble bourguignon souhaitant s’implanter sur le marché américain. L’objectif principal est de **définir le prix** de ses bouteilles de vin afin d’être compétitif tout en valorisant la qualité de son produit.
**Ce projet est un sujet d’étude (business case) proposé dans le cadre d’un examen de certification Data Analyst.**

---

## 1. Contexte et problématique

Le Domaine des Croix envisage de proposer un vin (Pinot Noir de Bourgogne) sur le marché américain. Pour cela, il souhaite :

1. **Analyser le marché** : comprendre la concurrence, les tendances de prix, les pays/régions les mieux notés, etc.
2. **Évaluer la valeur de son propre vin** par rapport aux concurrents : notamment les vins français, bourguignons, et plus précisément les Pinot Noir de la même année.
3. **Proposer un prix ou une fourchette de prix** : ce prix doit être compétitif tout en reflétant la qualité du produit, afin de bien se positionner sur le segment de marché visé.

---

## 2. Jeux de données

Deux sources de données principales ont été utilisées :

1. **Jeu de données de 130k vins** :  
   [Téléchargement ici](https://github.com/WildCodeSchool/wilddata/raw/main/wine.zip)  
   Il contient :
   - Les cépages
   - Les pays et régions de production
   - Les millésimes
   - Les notes (points) et descriptifs d’œnologues
   - Les prix moyens en dollars

2. **Données du vin du Domaine des Croix** :  
   [Téléchargement ici](https://raw.githubusercontent.com/WildCodeSchool/wilddata/main/domaine_des_croix.csv)  
   Il s’agit de la fiche d’information du vin que le client souhaite vendre aux États-Unis.

---

## 3. Objectifs et livrables attendus

### 3.1 Présentation finale (non-technique)

Le client n’étant pas data analyst, il attend une **présentation claire et vulgarisée** de l’analyse, incluant :
- Le **contexte** et la **problématique** (pourquoi fixer un prix compétitif et comment).
- Une **analyse exploratoire** du marché (répartition des vins par pays, notes moyennes, cépages, etc.).
- La **méthodologie**, les **outils** et les **langages** utilisés (par ex. Python, Excel, Power BI, Tableau, Seaborn, Plotly…).
- Une présentation de la partie **technique** (code et scripts) de manière simple et compréhensible.
- Un **tableau de bord** contenant plusieurs éléments :
  - Des **graphiques** variés (barres, camemberts, boxplots, etc.).
  - Au moins une **visualisation interactive** (par ex. un graphique Plotly ou un visuel Power BI interactif).
  - Au moins une **carte géographique** (pour situer les régions productrices).
  - Au moins un **tableau croisé** (pour comparer différentes dimensions).
  - Des **visuels accessibles** (couleurs contrastées, légendes explicites, police lisible, etc.).
- Les **conclusions** et **recommandations** : proposition de prix ou de fourchette de prix pour le Domaine des Croix, en fonction du positionnement souhaité (haut de gamme, moyen de gamme, etc.).

### 3.2 Analyse du marché

- **Répartition du nombre de vins par pays**  
  Permet de comprendre la concurrence et la représentativité des différents pays sur le marché.
- **Comparaison des notes moyennes**  
  Identifier les pays ou régions les mieux notés, et la position de la Bourgogne dans ce classement.
- **Moyennes de notes par cépage**  
  Vérifier si certains cépages sont plus appréciés ou mieux notés.
- **Distribution des prix** (par exemple par décile)  
  Pour repérer les segments de prix (entrée de gamme, milieu de gamme, haut de gamme).

### 3.3 Analyse comparative

- **Focus sur la Bourgogne** : comparer les vins français, puis zoomer progressivement sur la région Bourgogne et enfin sur les Pinot Noir de Bourgogne du même millésime.
- **Tarifs pratiqués** : observer la moyenne, la médiane, ou la gamme de prix de ces concurrents directs.
- **Positionnement** : en fonction de la volonté du client (haut de gamme, milieu de gamme), déterminer un prix pertinent.

### 3.4 Proposition de valeur

- À partir de la connaissance des prix de la concurrence, **recommander un prix ou une fourchette de prix** au Domaine des Croix.
- Expliquer l’argumentaire : 
  - Positionnement haut de gamme : alignement avec le **top 25%** le plus cher.
  - Positionnement moyen de gamme : alignement sur la **médiane** ou le prix moyen du segment.
  - Autres stratégies (prix d’appel, etc.) selon la demande du client.

### 3.5 Qualité esthétique du tableau de bord

- Soigner la **mise en forme** (couleurs, typographie, icônes, etc.), en lien avec l’univers du vin.
- Veiller à la **lisibilité** pour toutes et tous (contrastes de couleurs, taille de police, légendes, etc.).

---

## 4. Organisation du dépôt

```
market-analysis-wine/
├── data/
│   ├── external/                # Données externes ou complémentaires
│   ├── font/                    # Polices d’écriture si besoin
│   ├── img/                     # Images, logos, icônes
│   ├── processed/               # Données nettoyées ou transformées
│   └── raw/                     # Données brutes (ex: wine.zip, domaine_des_croix.csv)
├── notebooks/
│   └── Dimitri_Lefebvre_Notebook_EDA.ipynb  # Exemple de notebook d'analyse exploratoire
├── outputs/
│   └── reports/                 # Rapports finaux, présentations, documents livrables
├── scripts/
│   ├── data_cleaning.py         # Script de nettoyage et préparation des données
│   ├── feature_engineering.py   # Script de création de variables
│   └── modeling.py              # Script de modélisation ou analyses avancées
├── pBI/                          # Dossier contenant les fichiers Power BI (ex: .pbix)
├── .gitignore                   # Fichiers à ignorer (données brutes volumineuses, etc.)
└── README.md                    # Présentation générale du projet
```

---

## 5. Méthodologie (exemple)

1. **Collecte des données** : récupération des fichiers `wine.zip` et `domaine_des_croix.csv`.
2. **Nettoyage et préparation** : suppression des valeurs manquantes ou aberrantes, uniformisation des formats (par ex. devises, millésimes).
3. **Exploration** : utilisation de notebooks Jupyter ou d’un outil BI (Power BI, Tableau) pour visualiser la répartition des prix, notes, cépages, pays, etc.
4. **Comparaison** : focus sur la Bourgogne et plus précisément sur les Pinot Noir du même millésime que le vin du client.
5. **Recommandation de prix** : proposition basée sur l’analyse statistique (quartiles, déciles) et le positionnement marketing souhaité.
6. **Présentation** : création d’un tableau de bord visuel et interactif, accessible et esthétique.

---

## 6. Outils et langages

- **Python** (pandas, numpy, matplotlib, seaborn, plotly) pour le nettoyage et la visualisation exploratoire.
- **Power BI** ou **Tableau** (ou tout autre outil BI) pour la création d’un tableau de bord interactif.
- **GitHub** pour la gestion de version et la collaboration.

---

## 7. Comment contribuer ou reproduire l’analyse

1. **Cloner** le dépôt :  
   ```bash
   git clone https://github.com/username/market-analysis-wine.git
   ```
2. **Installer les dépendances** (si un fichier `requirements.txt` est fourni) :  
   ```bash
   pip install -r requirements.txt
   ```
3. **Exécuter les notebooks** (si vous souhaitez reproduire l’analyse) :  
   - Ouvrez le notebook Jupyter dans `notebooks/` et suivez les étapes.
4. **Consulter la présentation finale** :  
   - Disponible dans `outputs/reports/` ou sous forme d’un fichier Power BI/ Tableau.

---

## 8. Conclusion

Grâce à cette analyse, le **Domaine des Croix** disposera d’une vision claire du marché américain du vin, avec un focus particulier sur la **Bourgogne** et les **Pinot Noir**. Le tableau de bord et les visualisations fournies permettront de :

- Comprendre la concurrence et les tendances de prix.
- Comparer les notes et caractéristiques de vins similaires.
- Déterminer une **stratégie de positionnement tarifaire** adaptée.

La démarche se veut **accessible**, **visuelle** et **pédagogique**, afin que le client puisse rapidement se faire une idée précise du marché et prendre la décision de prix la plus adaptée à ses objectifs.

---

## 9. Auteurs et contact

- **Auteur principal** : [Votre Nom / Équipe]
- **Contact** : [Votre email ou celui de l’équipe]

N’hésitez pas à ouvrir une _issue_ ou à proposer une _pull request_ pour toute suggestion ou amélioration.

---

© 2025 – Projet d’analyse de données pour le Domaine des Croix. Tous droits réservés.