# 🛍️ H&M Fashion Recommendation Pipeline

[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![LightFM](https://img.shields.io/badge/LightFM-1.17+-green.svg)](https://making.lyst.com/lightfm/docs/home.html)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Un pipeline complet de système de recommandation pour les articles de mode H&M, utilisant des techniques de filtrage collaboratif et hybride avec LightFM.

## 📋 Table des Matières

- [🎯 Objectifs](#-objectifs)
- [🏗️ Architecture](#️-architecture)
- [📊 Dataset](#-dataset)
- [🚀 Installation](#-installation)
- [📖 Utilisation](#-utilisation)
- [📂 Structure du Projet](#-structure-du-projet)
- [🔬 Méthodologie](#-méthodologie)
- [📈 Résultats](#-résultats)
- [🤝 Contribution](#-contribution)

## 🎯 Objectifs

Ce projet implémente un système de recommandation de mode pour H&M avec les objectifs suivants :

- **Personnalisation** : Recommandations adaptées aux préférences individuelles
- **Scalabilité** : Pipeline optimisé pour traiter de gros volumes de données
- **Performance** : Modèles hybrides combinant filtrage collaboratif et contenu
- **Expérimentation** : Framework pour tester différentes approches et hyperparamètres

## 🏗️ Architecture

```
📦 Pipeline de Recommandation
├── 📊 Exploration des Données
├── 🎯 Échantillonnage Stratégique
├── 🔧 Preprocessing & Feature Engineering
├── 🤖 Modélisation (LightFM)
├── ⚡ Optimisation des Hyperparamètres
└── 📈 Évaluation & Métriques
```

## 📊 Dataset

Le projet utilise le dataset H&M Personalized Fashion Recommendations comprenant :

- **Transactions** : Historique d'achats des clients
- **Articles** : Métadonnées des produits (catégorie, couleur, prix, etc.)
- **Customers** : Informations démographiques des clients

### Caractéristiques
- **31M+ transactions** sur 2 ans
- **105K+ articles uniques**
- **1.4M+ clients actifs**
- **Sparsité élevée** (~99.9%)

## 🚀 Installation

### Prérequis
- Python 3.8+
- Jupyter Notebook
- Google Colab (recommandé)

### Installation des dépendances

```bash
# Clone du repository
git clone https://github.com/realnribal/hm-fashion-recommendation-pipeline.git
cd hm-fashion-recommendation-pipeline

# Installation des packages Python
pip install -r requirements.txt
```

### Packages principaux
```
lightfm>=1.17
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.5.0
seaborn>=0.11.0
tqdm>=4.62.0
```

## 📖 Utilisation

### 1. Configuration et chargement des données
```bash
jupyter notebook 00_setup_and_data_loading.ipynb
```

### 2. Exploration des données
```bash
jupyter notebook 01_Exploration_Donnees.ipynb
```

### 3. Échantillonnage stratégique
```bash
jupyter notebook 02_Echantillonnage_Donnees.ipynb
```

### 4. Préparation des données
```bash
jupyter notebook 03_Preparation_Donnees.ipynb
```

### 5. Modélisation collaborative
```bash
jupyter notebook 04_Modele_Collaboratif.ipynb
```

### 6. Optimisation des hyperparamètres
```bash
jupyter notebook 05_Optimisation_Hyperparametres.ipynb
```

## 📂 Structure du Projet

```
hm-fashion-recommendation-pipeline/
│
├── 📓 Notebooks
│   ├── 00_setup_and_data_loading.ipynb     # Configuration et chargement
│   ├── 01_Exploration_Donnees.ipynb        # Analyse exploratoire
│   ├── 02_Echantillonnage_Donnees.ipynb    # Stratégies d'échantillonnage
│   ├── 03_Preparation_Donnees.ipynb        # Preprocessing des données
│   ├── 04_Modele_Collaboratif.ipynb        # Modélisation LightFM
│   └── 05_Optimisation_Hyperparametres.ipynb # Tuning des paramètres
│
├── 📁 data/                                 # Données brutes et traitées
│   ├── raw/                                # Données originales H&M
│   ├── processed/                          # Données preprocessées
│   └── samples/                            # Échantillons pour développement
│
├── 📁 outputs/                             # Résultats et artefacts
│   ├── figures/                            # Visualisations
│   ├── models/                             # Modèles entraînés
│   └── results/                            # Métriques et rapports
│
├── 📄 requirements.txt                      # Dépendances Python
└── 📖 README.md                            # Documentation
```

## 🔬 Méthodologie

### 1. Exploration des Données
- **Analyse de distribution** : Patterns d'achat, saisonnalité
- **Profiling utilisateurs** : Segmentation par comportement
- **Analyse de sparsité** : Identification des défis du cold start

### 2. Échantillonnage Stratégique
- **Utilisateurs actifs** : Focus sur clients avec historique suffisant
- **Articles populaires** : Concentration sur produits avec interactions
- **Échantillonnage temporel** : Préservation des tendances saisonnières

### 3. Preprocessing
- **Encodage des identifiants** : Mapping vers entiers consécutifs
- **Feature engineering** : Extraction de métadonnées produits
- **Matrix sparse** : Optimisation mémoire pour interactions

### 4. Modélisation
- **LightFM** : Modèle hybride collaboratif + contenu
- **Loss functions** : WARP, BPR pour ranking
- **Embeddings** : Représentations latentes utilisateurs/articles

### 5. Évaluation
- **Split temporel** : Train/validation respectant chronologie
- **Métriques** : Precision@K, Recall@K, AUC, MRR
- **Cold start** : Évaluation spécifique nouveaux utilisateurs/articles

## 📈 Résultats

### Métriques de Performance
| Métrique | Valeur |
|----------|--------|
| Precision@10 | 0.XX |
| Recall@10 | 0.XX |
| AUC | 0.XX |
| MRR | 0.XX |

### Insights Clés
- ✅ **Saisonnalité forte** : Pics d'activité pendant les soldes
- ✅ **Segmentation claire** : Comportements distincts par âge/région
- ✅ **Long tail** : 80% des ventes sur 20% des articles
- ✅ **Cold start** : Challenge majeur pour nouveaux utilisateurs

## 🔧 Configuration Google Colab

Pour utiliser ce projet sur Google Colab :

1. **Montage Google Drive**
```python
from google.colab import drive
drive.mount('/content/drive')
```

2. **Configuration des chemins**
```python
BASE_PATH = "/content/drive/MyDrive/PSL/00-RecommanderSystem/h2m-recsys"
DATA_PATH = f"{BASE_PATH}/data"
OUTPUTS_PATH = f"{BASE_PATH}/outputs"
```

3. **Installation des dépendances**
```python
!pip install lightfm tqdm
```

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. **Fork** le projet
2. **Créer** une branche feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** vos changements (`git commit -m 'Add some AmazingFeature'`)
4. **Push** vers la branche (`git push origin feature/AmazingFeature`)
5. **Ouvrir** une Pull Request

## 📝 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 👥 Auteurs

- **Votre Nom** - *Développement initial* - [@realnribal](https://github.com/realnribal)

## 🙏 Remerciements

- Dataset H&M Personalized Fashion Recommendations
- Équipe LightFM pour l'excellent framework
- Communauté Kaggle pour les insights et discussions

---

**⭐ Si ce projet vous a été utile, n'hésitez pas à lui donner une étoile !**