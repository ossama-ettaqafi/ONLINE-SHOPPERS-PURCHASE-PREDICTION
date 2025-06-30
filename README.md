# 🛍️ Online Shoppers Purchasing Intention

Un projet de machine learning visant à prédire si un visiteur en ligne effectuera un achat en fonction de son comportement de navigation. Le pipeline utilise les modèles **Arbre de Décision** et **SVM**, avec des résultats visualisés dans un **dashboard interactif construit avec Tableau Desktop**.

## 📁 Structure du projet

```
ONLINE-SHOPPERS-PURCHASE-PREDICTION/
.
├── LICENSE                            # Fichier de licence du projet
├── README.md                         # Documentation et présentation du projet
├── requirements.txt                  # Liste des dépendances Python requises
├── dashboard                        # Dossier contenant les fichiers du tableau de bord
│   ├── dashboard_capture.png         # Capture d'écran ou image du tableau de bord
│   └── tableau_dashboard.twbx        # Fichier du tableau de bord Tableau
├── data                             # Dossier des données brutes ou originales
│   └── online_shoppers_intention.csv  # Dataset principal utilisé dans le projet
├── models                           # Modèles d'apprentissage automatique sauvegardés
│   ├── decision_tree_model.joblib
│   ├── logistic_regression_model.joblib
│   ├── random_forest_model.joblib
│   └── svm_model.joblib
└── notebooks                        # Notebooks Jupyter et fichiers associés
    ├── 01_data_preprocessing.ipynb          # Notebook pour le nettoyage et prétraitement des données
    ├── 02_model_training.ipynb               # Notebook pour l’entraînement et l’évaluation des modèles
    ├── 03_tableau_visualisation.ipynb        # Notebook pour la visualisation avec Tableau
    ├── cleaned_data.csv                       # Dataset nettoyé après prétraitement
    ├── predictions_decision_tree.csv         # Prédictions issues du modèle arbre de décision
    ├── predictions_dt.csv                     # Variante ou doublon des prédictions arbre de décision
    ├── predictions_logistic_regression.csv   # Prédictions du modèle régression logistique
    ├── predictions_rf.csv                     # Prédictions du modèle random forest
    ├── predictions_svm.csv                    # Prédictions du modèle SVM
    ├── test_set.csv                           # Dataset de test au format CSV
    ├── train_set.csv                          # Dataset d’entraînement au format CSV
    ├── train_set_balanced.csv                 # Dataset d’entraînement équilibré (ex: SMOTE)
    ├── .ipynb_checkpoints                     # Sauvegardes automatiques des notebooks
    │   ├── 01_data_preprocessing-checkpoint.ipynb
    │   ├── 02_model_training-checkpoint.ipynb
    │   ├── 03_tableau_visualisation-checkpoint.ipynb
    │   └── cleaned_data-checkpoint.csv
    └── images                                # Dossier contenant les images utilisées dans les notebooks ou documentation
        └── logo.png                          # Logo du projet
````

## 🎯 Objectifs du projet

- Prétraiter le dataset Kaggle **Online Shoppers Purchasing Intention**
- Entraîner plusieurs modèles de classification :
  - ✅ **Arbre de Décision**
  - ✅ **Support Vector Machine (SVM)**
  - ✅ **Random Forest**
  - ✅ **Régression Logistique**
- Évaluer les performances des modèles
- Visualiser les résultats (courbes ROC, matrices de confusion, etc.)
- Présenter les insights et prédictions dans un **dashboard Tableau**

## 🔍 Modèles étudiés

Dans ce projet, plusieurs modèles ont été explorés pour prédire l’intention d’achat, avec un focus sur :

| Modèle                                    | Description / Particularités                                                                                  |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **Arbre de Décision**                     | Modèle simple et interprétable, efficace pour capturer des règles non linéaires.                             |
| **Support Vector Machine (SVM)**          | Classifieur puissant utilisant un noyau RBF pour gérer la séparation non linéaire des classes.              |
| **Régression Logistique (class_weight='balanced')** | Utilisée pour gérer le déséquilibre des classes, servant de baseline robuste.                                |
| **Random Forest**                         | Ensemble d’arbres de décision pour plus de robustesse, testé avec gestion du déséquilibre par pondération.  |
| **Techniques de rééchantillonnage** (SMOTE, undersampling) (Plus tard) | Appliquées pour corriger le déséquilibre et améliorer la détection de la classe minoritaire (acheteurs).   |

## ⚙ Technologies utilisées

| Composant        | Outils / Librairies                                                                                                                        |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Langage          | Python 3.x                                                                                                                                |
| Machine Learning | Scikit-learn                                                                                                                              |
| Visualisation    | Matplotlib, Seaborn                                                                                                                       |
| Dashboard        | Tableau Desktop (.twbx)                                                                                                                   |
| Notebook         | Jupyter Notebook                                                                                                                          |
| Dataset          | [Online Shoppers Purchasing Intention (Kaggle)](https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset) |

## 🚀 Comment lancer le projet

### 1. Installer les dépendances

```bash
pip install -r requirements.txt
````

### 2. Exécuter les notebooks dans l’ordre

* `notebooks/01_data_preprocessing.ipynb`
  *(Nettoyage, encodage, séparation train/test)*

* `notebooks/02_model_training.ipynb`
  *(Entraînement, évaluation des modèles Arbre de Décision et SVM, sauvegarde des modèles, export des prédictions pour Tableau)*

## 📈 Dashboard Tableau

* Fichier : `dashboards/tableau_dashboard.twbx`
* Visualisations : Prédictions par session, taux de conversion, filtres dynamiques par mois, type de visiteur, région, etc.
* Données : fichier CSV exporté depuis le notebook (`predictions.csv`)

## 📋 requirements.txt

```txt
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
joblib
imblearn
```

## 📄 Licence

MIT License
