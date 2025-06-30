# 🛍️ Online Shoppers Purchasing Intention

Un projet de machine learning visant à prédire si un visiteur en ligne effectuera un achat en fonction de son comportement de navigation. Le pipeline utilise les modèles **Arbre de Décision** et **SVM**, avec des résultats visualisés dans un **dashboard interactif construit avec Tableau Desktop**.

## 📁 Structure du projet

```
.
├── LICENSE
├── README.md
├── requirements.txt
├── dashboard
│   ├── dashboard_capture.png
│   └── tableau_dashboard.twbx
├── data
│   └── online_shoppers_intention.csv
├── models
│   ├── decision_tree_model.joblib
│   ├── logistic_regression_model.joblib
│   ├── random_forest_model.joblib
│   └── svm_model.joblib
└── notebooks
    ├── 01_data_preprocessing.ipynb
    ├── 02_model_training.ipynb
    ├── 03_tableau_visualisation.ipynb
    ├── cleaned_data.csv
    ├── predictions_decision_tree.csv
    ├── predictions_dt.csv
    ├── predictions_logistic_regression.csv
    ├── predictions_rf.csv
    ├── predictions_svm.csv
    ├── test_set.csv
    ├── train_set.csv
    ├── train_set_balanced.csv
    ├── .ipynb_checkpoints
    │   ├── 01_data_preprocessing-checkpoint.ipynb
    │   ├── 02_model_training-checkpoint.ipynb
    │   ├── 03_tableau_visualisation-checkpoint.ipynb
    │   └── cleaned_data-checkpoint.csv
    └── images
        └── logo.png
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
