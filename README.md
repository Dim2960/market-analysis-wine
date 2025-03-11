# Market Analysis - Domaine des Croix

Bienvenue dans ce projet d’analyse de données pour le **Domaine des Croix**, un vignoble bourguignon souhaitant s’implanter sur le marché américain. L’objectif principal est de **définir le prix** de ses bouteilles de vin afin d’être compétitif tout en valorisant la qualité de son produit.
**Ce projet est un sujet d’étude (business case) proposé dans le cadre de mon examen de certification Data Analyst.**

---

## 🌟 Contexte et problématique

Le Domaine des Croix envisage de proposer un vin (Pinot Noir de Bourgogne) sur le marché américain. Pour cela, il souhaite :

1. **Analyser le marché** : comprendre la concurrence, les tendances de prix, les pays/régions les mieux notés, etc.
2. **Évaluer la valeur de son propre vin** par rapport aux concurrents : notamment les vins français, bourguignons, et plus précisément les Pinot Noir de la même année.
3. **Proposer un prix ou une fourchette de prix** : ce prix doit être compétitif tout en reflétant la qualité du produit, afin de bien se positionner sur le segment de marché visé.

---

## 📂 Jeux de données

Deux sources de données principales ont été utilisées :

1. **Jeu de données de 130k vins** :  
   [Téléchargement ici](https://github.com/Dim2960/market-analysis-wine/data/raw/wine.zip)  
   Il contient :
   - Les cépages
   - Les pays et régions de production
   - Les millésimes
   - Les notes (points) et descriptifs d’œnologues
   - Les prix moyens en dollars

2. **Données du vin du Domaine des Croix** :  
   [Téléchargement ici](https://github.com/Dim2960/market-analysis-wine/data/raw/domaine_des_croix.csv)  
   Il s’agit de la fiche d’information du vin que le client souhaite vendre aux États-Unis.

---

## 🗃️ Structure du Projet

```
market-analysis-wine/
├── data/
│   ├── external/                # Données complémentaires
│   │   ├── font/                # Polices d’écriture 
│   │   ├── icones/              # icones pour le readme
│   │   └── img/                 # Images, logos, icônes
│   ├── processed/               # Données nettoyées ou transformées
│   └── raw/                     # Données brutes (ex: wine.zip, domaine_des_croix.csv)
├── notebooks/
│   └── Dimitri_Lefebvre_Notebook_EDA.ipynb  # Notebook d'analyse exploratoire
├── outputs/
│   └── reports/                 # Rapports finaux, présentations, documents livrables
│       ├── pwBI/                # Rapport Power BI 
│       └── ptt/                 # Présentation de l'étude
├── .gitignore                   
└── README.md                    
```

---

## 🛠️ Méthodologie 

1. **Collecte des données** : récupération des fichiers `wine.zip` et `domaine_des_croix.csv`.
2. **Nettoyage et préparation** : suppression des valeurs manquantes ou aberrantes, uniformisation des formats (par ex. devises, millésimes).
3. **Exploration** : utilisation de notebooks Jupyter et d’un outil BI (Power BI, Tableau) pour visualiser la répartition des prix, notes, cépages, pays, etc.
4. **Comparaison** : focus sur la Bourgogne et plus précisément sur les Pinot Noir du même millésime que le vin du client.
5. **Recommandation de prix** : proposition basée sur l’analyse statistique (quartiles, déciles) et le positionnement marketing souhaité.
6. **Présentation** : création d’un tableau de bord visuel et interactif, accessible et esthétique.

🔗 **Accédez au tableau de bord Power BI** :  [![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-orange?logo=powerbi)](https://app.powerbi.com/view?r=eyJrIjoiYjA2NWNiNTktM2Q1YS00YWE4LWI5OGUtMTBlY2VkNTdmYjA3IiwidCI6IjQ0OTFmMGVlLWY1MDMtNDcyNi1hNWViLTFmMGM0ZGFjODJhOSJ9&pageName=0ddccbb621013b0fcf8d) 

---

## 🛠️ Outils et langages

- **Python** (pandas, numpy, matplotlib, seaborn) pour le nettoyage et la visualisation exploratoire.
- **Power BI** pour la création d’un tableau de bord interactif.
- **GitHub** pour la gestion de version et la collaboration.

| Languages | Librairies python | Outils |
|-----------|------------------|--------|
| ![python](data/external/icones/python-color.svg) Python | ![numpy](data/external/icones/numpy-color.svg) numpy | ![jupiter](data/external/icones/jupyter-color.svg) Jupiter Notebook |
| | ![pandas](data/external/icones/pandas-color.svg) pandas | ![github](data/external/icones/github-color.svg) Github |
| | ![matplotlib](data/external/icones/python-color.svg) matplotlib | ![vscode](data/external/icones/visualstudiocode-color.svg) VS code |
| | ![seaborn](data/external/icones/python-color.svg) seaborn | ![Git](img_rdata/external/iconeseadme/scikitlearn-color.svg) Git  |
| | ![skimpy](data/external/icones/python-color.svg) skimpy | |
| | ![nltk](data/external/icones/python-color.svg) nltk | |

---