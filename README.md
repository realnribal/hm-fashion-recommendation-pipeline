# 🛍️ H&M Fashion Recommendatio```
📦 Pipeline de Recommandation H&M Complet (8 Étapes)
├── 🔧 00_setup_and_data_loading        # Configuration Google Drive & dépendances
├── 📊 01_Exploration_Donnees          # Analyse sparsité & distributions
├── 🎯 02_Echantillonnage_Donnees      # Stratégies échantillonnage optimales
├── 🔄 03_Preparation_Donnees          # Mappings & matrices LightFM
├── 🤖 04_Modele_Collaboratif          # Modèle collaboratif (WARP, BPR)
├── ⚙️ 05_Optimisation_Hyperparametres  # Grid search & validation croisée
├── 📊 06_Evaluation_Modele            # Évaluation approfondie & métriques
├── 🔗 07_Modele_Hybride               # Modèle hybride avec features articles
└── 🎯 08_Pipeline_Final               # Pipeline complet & démo interactive
```e

[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![LightFM](https://img.shields.io/badge/LightFM-1.17+-green.svg)](h### Insights Découverts
- 🔬 **Sparsité extrême** : 99.95-99.99% - défi majeur pour recommandations
- 📊 **Distribution power-law** : Peu d'utilisateurs très actifs, majorité occasionnelle
- 🎯 **Échantillonnage critique** : Stratégie "Combiné" (actifs + populaires) optimale
- ⚡ **Performance LightFM** : WARP loss function supérieure pour ranking
- 🔄 **Hyperparamètres sensibles** : Learning rate et regularization impact fort
- 💾 **Mémoire optimisée** : Matrices sparse essentielles pour scalabilité
- 🔗 **Modèle hybride** : Features articles apportent amélioration modérée mais robustesse
- 🛡️ **Robustesse critique** : Gestion d'erreurs automatique essentielle en production
- 🆕 **Cold-start** : Fallback sur popularité efficace pour nouveaux utilisateurs
- 📈 **Évaluation multi-niveaux** : Métriques diversifiées révèlent qualités cachéesmaking.lyst.com/lightfm/docs/home.html)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Un pipeline complet de système de recommandation pour les articles de mode H&M, utilisant des techniques de filtrage collaboratif avec LightFM. Le projet inclut une analyse exploratoire approfondie, des stratégies d'échantillonnage intelligentes et une optimisation systématique des hyperparamètres.

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

## 🎯 Stratégies d'Échantillonnage Implémentées

| Stratégie | Description | Avantages |
|-----------|-------------|----------|
| **Utilisateurs Actifs** | ≥5 interactions par user | Réduit cold start users |
| **Articles Populaires** | ≥10 interactions par item | Patterns plus clairs |
| **Combiné** | Actifs + Populaires | Équilibre optimal |
| **Aléatoire** | Simple random sampling | Baseline comparison |
| **Stratifié Temporel** | Échantillon par période | Préserve saisonnalité |

## 🎯 Caractéristiques Techniques Avancées

Ce projet implémente un système de recommandation de mode pour H&M avec les objectifs suivants :

- **Personnalisation** : Recommandations adaptées aux préférences individuelles
- **Scalabilité** : Pipeline optimisé pour traiter de gros volumes de données
- **Performance** : Modèles hybrides combinant filtrage collaboratif et contenu
- **Expérimentation** : Framework pour tester différentes approches et hyperparamètres

## 🏗️ Architecture

```
📦 Pipeline de Recommandation H&M
├── � 00_setup_and_data_loading      # Configuration Google Drive & deps
├── 📊 01_Exploration_Donnees        # Analyse sparsité & distributions
├── 🎯 02_Echantillonnage_Donnees    # Stratégies échantillonnage optimales
├── � 03_Preparation_Donnees        # Mappings & matrices LightFM
├── 🤖 04_Modele_Collaboratif        # Modèle collaboratif (WARP, BPR)
└── ⚙️ 05_Optimisation_Hyperparametres # Grid search & validation croisée
```

## 📊 Dataset

Le projet utilise le dataset H&M Personalized Fashion Recommendations comprenant :

- **Transactions** : Historique d'achats des clients
- **Articles** : Métadonnées des produits (catégorie, couleur, prix, etc.)
- **Customers** : Informations démographiques des clients

### Caractéristiques
- **31M+ transactions** sur 2 ans (septembre 2018 - septembre 2020)
- **105K+ articles uniques**
- **1.4M+ clients actifs**
- **Sparsité très élevée** (~99.95% - 99.99%)
- **Échantillonnage intelligent** : Focus sur utilisateurs actifs (≥5 interactions) et articles populaires (≥10 interactions)

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
# Installation via notebooks (Google Colab)
lightfm  # Version fork compatible
pandas
numpy
scipy
scikit-learn
matplotlib
seaborn
tqdm
pickle (built-in)
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

### 7. Évaluation approfondie du modèle
```bash
jupyter notebook 06_Evaluation_Modele.ipynb
```

### 8. Modèle hybride avec features
```bash
jupyter notebook 07_Modele_Hybride.ipynb
```

### 9. Pipeline final et démo
```bash
jupyter notebook 08_Pipeline_Final.ipynb
```

## 📂 Structure du Projet

```
hm-fashion-recommendation-pipeline/
│
├── 📓 Notebooks
│   ├── 00_setup_and_data_loading.ipynb         # Configuration et chargement
│   ├── 01_Exploration_Donnees.ipynb            # Analyse exploratoire
│   ├── 02_Echantillonnage_Donnees.ipynb        # Stratégies d'échantillonnage
│   ├── 03_Preparation_Donnees.ipynb            # Preprocessing des données
│   ├── 04_Modele_Collaboratif.ipynb            # Modélisation LightFM
│   ├── 05_Optimisation_Hyperparametres.ipynb   # Tuning des paramètres
│   ├── 06_Evaluation_Modele.ipynb              # Évaluation approfondie
│   ├── 07_Modele_Hybride.ipynb                 # Modèle avec features articles
│   └── 08_Pipeline_Final.ipynb                 # Pipeline complet & démo
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

### 1. Configuration & Chargement (Notebook 00)
- **Google Drive** : Montage et configuration des chemins
- **Dependencies** : Installation automatique LightFM et dépendances
- **Structure** : Création automatique des dossiers de sortie

### 2. Exploration des Données (Notebook 01)
- **Analyse de sparsité** : Calcul précis (~99.95% sparsité)
- **Distributions** : Patterns utilisateurs/articles avec visualisations
- **Quality assessment** : Identification des caractéristiques clés
- **Visualisation** : Matrices de sparsité et distributions

### 3. Échantillonnage Stratégique (Notebook 02)
- **5 Stratégies** : Utilisateurs actifs, articles populaires, combiné, aléatoire, stratifié temporel
- **Comparaison quantitative** : Scoring automatique des échantillons
- **Tailles variables** : Tests 1K, 5K, 10K, 50K, 100K interactions
- **Sélection optimale** : Choix basé sur critères de performance

### 4. Preprocessing LightFM (Notebook 03)
- **IDMapper** : Classe custom pour mappings user/item vers entiers
- **Matrices sparse** : Génération COO/CSR pour LightFM
- **Features articles** : Encodage catégories, prix, descriptions
- **Train/Test split** : Division temporelle préservant chronologie

### 5. Modélisation Collaborative (Notebook 04)
- **LightFM** : Modèle collaboratif pur (sans features)
- **Loss functions** : Tests WARP, BPR, Logistic avec comparaison
- **Métriques** : Precision@K, Recall@K, AUC automatisées
- **Évaluation** : Validation sur échantillons test

### 6. Optimisation Hyperparamètres (Notebook 05)
- **Grid Search** : Exploration systématique learning_rate, no_components, regularization
- **Validation croisée** : Tests multiples configurations
- **Métriques comparatives** : Sélection modèle optimal
- **Sauvegarde** : Persistance meilleur modèle

### 7. Évaluation Approfondie (Notebook 06)
- **Métriques multiples** : Precision@K, Recall@K, NDCG, AUC
- **Segmentation utilisateurs** : Analyse par niveau d'activité
- **Diversité & Nouveauté** : Tests qualité recommandations
- **Cold-start analysis** : Performance nouveaux utilisateurs/articles

### 8. Modèle Hybride (Notebook 07)
- **Features articles** : Intégration métadonnées (catégorie, couleur, prix)
- **Comparaison hybride vs collaboratif** : Mesure amélioration
- **Gestion compatibilité** : Fallback automatique si erreurs features
- **Tests cold-start améliorés** : Validation robustesse

### 9. Pipeline Final (Notebook 08)
- **Système robuste** : Gestion d'erreurs et fallbacks automatiques
- **Interface recommandation** : Classe H2MRecommendationSystem
- **Démo interactive** : Tests sur utilisateurs variés
- **Pipeline production-ready** : Code optimisé et documenté

## 🎯 Caractéristiques Techniques Avancées

### Pipeline d'Évaluation Complète
- **Métriques automatisées** : Precision@K, Recall@K, AUC, NDCG
- **Segmentation intelligente** : Analyse par profil utilisateur
- **Tests diversité** : Mesure variété recommandations
- **Cold-start robuste** : Gestion nouveaux utilisateurs/articles

### Modèle Hybride Intelligent
| Caractéristique | Implémentation |
|-----------------|----------------|
| **Features articles** | Catégorie, couleur, prix, description |
| **Compatibilité** | Fallback automatique vers collaboratif |
| **Identity features** | Matrice identité + features custom |
| **Gestion erreurs** | Système robuste avec alternatives |

### Système de Recommandation Production
- **Classe H2MRecommendationSystem** : Interface unifiée
- **Gestion d'erreurs** : Fallbacks automatiques à tous niveaux
- **Nouveaux utilisateurs** : Recommandations basées popularité
- **Analyse profil** : Extraction caractéristiques utilisateur

## � Pipeline de Performance

### Métriques Automatisées
| Métrique | Description | Implémentation |
|----------|-------------|----------------|
| **Precision@K** | Précision top-K recommandations | `lightfm.evaluation.precision_at_k` |
| **Recall@K** | Rappel top-K recommandations | `lightfm.evaluation.recall_at_k` |
| **AUC** | Area Under Curve | `lightfm.evaluation.auc_score` |
| **NDCG** | Normalized Discounted Cumulative Gain | Custom implementation |
| **Diversité** | Variété catégories recommandées | Analyse post-traitement |

### Robustesse Système
- **Grid Search** : Test automatique combinaisons hyperparamètres
- **Validation Croisée** : Évaluation robuste performance
- **Sauvegarde Automatique** : Persistance résultats et modèles
- **Fallbacks intelligents** : Alternatives automatiques en cas d'erreur

### Insights Découverts
- 🕳️ **Sparsité extrême** : 99.95-99.99% - défi majeur pour recommandations
- 📊 **Distribution power-law** : Peu d'utilisateurs très actifs, majorité occasionnelle
- 🎯 **Échantillonnage critique** : Stratégie "Combiné" (actifs + populaires) optimale
- ⚡ **Performance LightFM** : WARP loss function supérieure pour ranking
- 🔄 **Hyperparamètres sensibles** : Learning rate et regularization impact fort
- 💾 **Mémoire optimisée** : Matrices sparse essentielles pour scalabilité

## 🔧 Configuration Google Colab

Ce projet est **optimisé pour Google Colab** avec gestion automatique des erreurs :

### 1. Montage Google Drive (standardisé dans tous notebooks)
```python
print("🔗 Connexion à Google Drive...")
from google.colab import drive
drive.mount('/content/drive')
print("✅ Google Drive monté avec succès")
```

### 2. Configuration des chemins (identique partout)
```python
BASE_PATH = "/content/drive/MyDrive/PSL/00-RecommanderSystem/h2m-recsys"
DATA_PATH = f"{BASE_PATH}/data"
OUTPUTS_PATH = f"{BASE_PATH}/outputs"

# Création automatique structure dossiers
directories_to_create = [
    f"{OUTPUTS_PATH}/models",
    f"{OUTPUTS_PATH}/figures", 
    f"{OUTPUTS_PATH}/metrics",
    f"{OUTPUTS_PATH}/samples"
]
```

### 3. Installation LightFM (version fork compatible)
```python
# Dans chaque notebook nécessitant LightFM
!pip install git+https://github.com/daviddavo/lightfm
!pip install -q tqdm
```

### 4. Persistance Robuste
- **Pickle automatique** : Sauvegarde intelligente entre notebooks
- **Gestion d'erreurs** : Fallbacks si fichiers manquants
- **Compatibilité** : Vérification versions et formats
- **Pipeline continu** : Chaque notebook utilise sorties précédentes

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