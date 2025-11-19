# House Price Prediction Project

## Master 2 Data Science - Machine Learning

### Description

Ce projet vise à développer un modèle de prédiction du prix des maisons en utilisant des techniques de data science et de machine learning. Le projet suit une méthodologie rigoureuse incluant l'exploration des données, le nettoyage, le preprocessing, et l'implémentation de plusieurs modèles de régression.

### Équipe

- Youcef
- Mohamed-Amine

### Structure du Projet

```
projet_ml_housing/
├── README.md                  # Documentation du projet
├── requirements.txt          # Dépendances Python
├── config.py                # Configuration centralisée
├── main.py                  # Script principal (bonus)
├── notebook_principal.ipynb # Notebook Jupyter principal
│
├── data/                    # Données du projet
│   ├── raw/                # Données brutes
│   │   └── house_prices.csv
│   ├── processed/          # Données nettoyées
│   └── splits/            # Données train/test
│
├── src/                    # Code source
│   ├── __init__.py
│   ├── data_processing/   # Module de traitement des données
│   │   ├── __init__.py
│   │   ├── load_data.py      # Chargement des données
│   │   ├── clean_data.py     # Nettoyage des données
│   │   └── preprocessing.py  # Preprocessing et encodage
│   │
│   ├── data_science/      # Module de data science
│   │   ├── __init__.py
│   │   ├── data.py           # Split train/test
│   │   ├── models.py         # Modèles ML
│   │   └── evaluation.py    # Évaluation des modèles
│   │
│   └── figures/           # Module de visualisation
│       ├── __init__.py
│       ├── eda_plots.py     # Graphiques EDA
│       └── model_plots.py   # Graphiques des modèles
│
├── models/                # Modèles sauvegardés
├── figures/              # Graphiques générés
└── results/             # Résultats et rapports
```

### Installation

#### 1. Cloner le repository

```bash
git clone [URL_DU_REPO]
cd projet_ml_housing
```

#### 2. Créer un environnement Conda

```bash
conda create -n ml_housing python=3.8
conda activate ml_housing
```

#### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

#### 4. Créer les dossiers nécessaires

```python
python -c "import config; config.create_directories()"
```

### Dataset

Le dataset contient **809 maisons** avec **14 variables** :

- **Target** : `price` - Prix de la maison
- **Features numériques** : `area`, `bedrooms`, `bathrooms`, `stories`, `parking`, `house_age`
- **Features binaires** : `mainroad`, `guestroom`, `basement`, `hot_water_heating`, `airconditioning`, `prefarea`
- **Feature catégorielle** : `furnishing_status` (furnished, semi-furnished, unfurnished)

### Pipeline du Projet

#### 1. Exploration des Données (EDA)
   - Chargement et inspection des données
   - Statistiques descriptives
   - Visualisations univariées et multivariées
   - Identification des valeurs manquantes et outliers

#### 2. Nettoyage des Données
   - Standardisation des noms de colonnes
   - Gestion des valeurs manquantes
   - Suppression des doublons
   - Nettoyage des variables catégorielles

#### 3. Preprocessing
   - Encodage des variables binaires (0/1)
   - Encodage des variables catégorielles (One-Hot)
   - Feature engineering
   - Normalisation (optionnelle)

#### 4. Modélisation
   - **Baseline** : Prix moyen par nombre de chambres
   - **Régression Linéaire** : Modèle de référence
   - **Random Forest / Gradient Boosting** : Modèles ensemblistes
   - **Fine-tuning** : GridSearchCV et RandomizedSearchCV

#### 5. Évaluation
   - Métriques : MAE, RMSE, R²
   - Validation croisée
   - Courbes d'apprentissage
   - Importance des features

### Utilisation

#### Option 1 : Notebook Jupyter

```bash
jupyter notebook notebook_principal.ipynb
```

#### Option 2 : Script Python (Bonus)

```bash
# Preprocessing des données
python main.py --step=data-proc

# Entraînement des modèles
python main.py --step=train

# Évaluation sur le test set
python main.py --step=test
```

### Résultats Attendus

- **R² Score** : > 0.7
- **MAE** : < 15% du prix moyen
- **Visualisations** : Distributions, corrélations, prédictions vs réalité
- **Feature Importance** : Identification des variables les plus influentes

### Technologies Utilisées

- **Python 3.8+**
- **Pandas** : Manipulation des données
- **NumPy** : Calculs numériques
- **Scikit-learn** : Machine Learning
- **Matplotlib/Seaborn** : Visualisations
- **MLflow** : Tracking des expériences (bonus)

### Bonnes Pratiques

**Code**
- Respect des normes PEP8
- Fonctions documentées avec docstrings
- Code modulaire et réutilisable
- Gestion des erreurs

**Git**
- Commits atomiques et descriptifs
- Branches pour chaque feature
- Issues GitLab pour le suivi
- Merge requests avec review

**Documentation**
- README complet
- Notebook commenté
- Docstrings pour toutes les fonctions
- Rapport final détaillé

### Critères d'Évaluation

1. **Qualité du code** (30%)
   - Propreté et organisation
   - Respect PEP8
   - Documentation

2. **Démarche scientifique** (30%)
   - Méthodologie
   - Justification des choix
   - Rigueur analytique

3. **Résultats** (25%)
   - Performance des modèles
   - Qualité des visualisations
   - Interprétation

4. **Collaboration** (15%)
   - Utilisation de Git
   - Travail en équipe
   - Organisation

### Ressources

- [Documentation Scikit-learn](https://scikit-learn.org/stable/)
- [PEP8 Style Guide](https://www.python.org/dev/peps/pep-0008/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [MLU Explain](https://mlu-explain.github.io)
- [Illustrated Machine Learning](https://illustrated-machine-learning.github.io)

### Contact

Pour toute question sur le projet :
- Professeur : Massinissa SAÏDI (massinissa.saidi@univ-amu.fr)

### License

Ce projet est réalisé dans le cadre du Master 2 Data Science à AMU.

---

*Dernière mise à jour : Novembre 2025*
