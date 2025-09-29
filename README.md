# 🛍️ H&M Fashion Recommendation Pipeline

[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![LightFM](https://img.shields.io/badge/LightFM-compatible-green.svg)](https://making.lyst.com/lightfm/docs/home.html)

Pipeline complet de système de recommandation pour H&M utilisant LightFM avec optimisation des hyperparamètres et modèle hybride collaboratif + contenu.

## 🏗️ Architecture

```
📦 Pipeline Complet (8 Étapes)
├── 🔧 00_setup_and_data_loading        # Configuration & dépendances
├── 📊 01_Exploration_Donnees          # Analyse sparsité & distributions  
├── 🎯 02_Echantillonnage_Donnees      # Stratégies échantillonnage
├── 🔄 03_Preparation_Donnees          # Mappings & matrices LightFM
├── 🤖 04_Modele_Collaboratif          # Modèle collaboratif (WARP, BPR)
├── ⚙️ 05_Optimisation_Hyperparametres  # Grid search & validation
├── 📊 06_Evaluation_Modele            # Évaluation approfondie
├── 🔗 07_Modele_Hybride               # Modèle avec features articles
└── 🎯 08_Pipeline_Final               # Pipeline complet & démo
```

## 📊 Dataset

**H&M Personalized Fashion Recommendations**
- 31M+ transactions (2018-2020)
- 105K+ articles, 1.4M+ clients
- Sparsité: ~99.95%
- Échantillonnage intelligent: utilisateurs actifs (≥5) + articles populaires (≥10)

## 🚀 Installation

```bash
# Clone
git clone https://github.com/realnribal/hm-fashion-recommendation-pipeline.git
cd hm-fashion-recommendation-pipeline

# Google Colab (recommandé)
!pip install git+https://github.com/daviddavo/lightfm
!pip install -q tqdm pandas numpy scipy scikit-learn matplotlib seaborn
```

## 📖 Utilisation

**Google Colab - Exécuter dans l'ordre :**

```python
# Configuration des chemins (identique dans tous notebooks)
BASE_PATH = "/content/drive/MyDrive/PSL/00-RecommanderSystem/h2m-recsys"
DATA_PATH = f"{BASE_PATH}/data"
OUTPUTS_PATH = f"{BASE_PATH}/outputs"
```

1. **00_setup_and_data_loading** → Configuration & chargement
2. **01_Exploration_Donnees** → Analyse dataset
3. **02_Echantillonnage_Donnees** → Sélection échantillons optimaux
4. **03_Preparation_Donnees** → Preprocessing LightFM
5. **04_Modele_Collaboratif** → Premier modèle
6. **05_Optimisation_Hyperparametres** → Tuning automatique
7. **06_Evaluation_Modele** → Métriques approfondies
8. **07_Modele_Hybride** → Intégration features articles
9. **08_Pipeline_Final** → Système production + démo

## 🔬 Méthodologie

| Étape | Techniques Clés |
|-------|----------------|
| **Échantillonnage** | 5 stratégies testées, sélection "Combiné" optimale |
| **Preprocessing** | IDMapper custom, matrices sparse COO/CSR |
| **Modélisation** | LightFM collaborative, loss functions WARP/BPR |
| **Optimisation** | Grid search learning_rate, no_components, regularization |
| **Évaluation** | Precision@K, Recall@K, AUC, NDCG, diversité |
| **Hybride** | Features articles + fallback automatique |
| **Production** | Classe H2MRecommendationSystem, gestion d'erreurs |

## 📈 Résultats Clés

- **Sparsité extrême** : 99.95% - challenge principal
- **WARP loss** : Performance supérieure pour ranking
- **Modèle hybride** : Amélioration robustesse + cold-start
- **Pipeline robuste** : Fallbacks automatiques essentiels
- **Système production-ready** : Gestion d'erreurs complète

## 🎯 Livrables

✅ **Pipeline complet** 8 notebooks Google Colab  
✅ **Modèle optimisé** LightFM avec hyperparamètres tunés  
✅ **Système hybride** Collaboratif + features articles  
✅ **Interface production** Classe recommandation robuste  
✅ **Évaluation approfondie** Métriques multiples + segmentation  
✅ **Démo interactive** Tests utilisateurs réels  

## 👥 Auteur

**[@realnribal](https://github.com/realnribal)** - Pipeline de recommandation H&M

---
⭐ **Star ce projet si utile !**
