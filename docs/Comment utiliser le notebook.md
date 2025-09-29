## Comment utiliser le notebook unifié du pipeline H&M Fashion Recommendation

Ce guide explique comment exploiter le notebook `HM_Fashion_Recommendation_Pipeline_Complete.ipynb` qui intègre tout le pipeline de recommandation, de l'import des données à la génération de recommandations personnalisées.

### 1. Pré-requis
- Compte Google et accès à Google Colab (recommandé)
- Espace de stockage Google Drive contenant les dossiers et fichiers de données H&M utilisés dans le projet
- Les dépendances Python sont automatiquement installées par le notebook (LightFM, pandas, etc.)

### 2. Ouverture du notebook
- Ouvrez le fichier `HM_Fashion_Recommendation_Pipeline_Complete.ipynb` dans Google Colab
- Exécutez la première cellule pour monter votre Google Drive (autorisation requise)
- Vérifiez que les chemins de données (`BASE_PATH`, `DATA_PATH`, `OUTPUTS_PATH`) correspondent à votre organisation dans Google Drive

### 3. Exécution séquentielle
- Faites défiler le notebook section par section et exécutez chaque cellule dans l'ordre
- Chaque étape du pipeline est clairement identifiée dans le sommaire (exploration, échantillonnage, préparation, entraînement, optimisation, etc.)
- Les outputs intermédiaires sont enregistrés automatiquement pour faciliter la reprise ou la modification d'une étape

### 4. Visualisation et analyse
- Vous trouverez des analyses exploratoires, des visualisations statistiques et des métriques d'évaluation dans les sections concernées
- Le notebook génère également des recommandations personnalisées pour des clients de test

### 5. Modification ou adaptation
- Vous pouvez ajuster les paramètres (chemins, hyperparamètres, features, etc.) directement dans les cellules correspondantes
- Pour utiliser d'autres données ou générer des recommandations pour de nouveaux clients, modifiez les variables d'entrée au bon endroit

### 6. Export et sauvegarde
- Les modèles entraînés, résultats d'évaluation, et systèmes finaux sont sauvegardés dans le dossier `outputs` du projet
- Vous pouvez télécharger ces fichiers pour les utiliser dans d'autres outils ou contextes

### 7. Support
- Si vous rencontrez un problème d'exécution ou de données, ouvrez une issue GitHub avec le label `question` ou `documentation`
