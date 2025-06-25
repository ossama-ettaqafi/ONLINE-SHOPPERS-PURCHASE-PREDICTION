# 🛍️ Online Shoppers Purchasing Intention

Un projet de Machine Learning pour prédire si un utilisateur effectuera un achat en ligne en se basant sur son comportement de navigation. Le pipeline utilise **Random Forest** et **SVM**, avec des résultats visualisés dans un **dashboard interactif construit avec Tableau Desktop**.

---

## 📁 Structure du Projet

```
OnlineShoppersML/
├── data/
│   └── online_shoppers_intention.csv      # Données originales
├── notebooks/
│   ├── 01_preprocessing_and_training.ipynb # Prétraitement + Modèles
├── models/
│   ├── rf_model.pkl                        # Modèle Random Forest enregistré
│   └── svm_model.pkl                       # Modèle SVM enregistré
├── dashboards/
│   └── tableau_dashboard.twbx              # Dashboard Tableau Desktop
├── requirements.txt
└── README.md
```

---

## 🎯 Objectifs du Projet

* Prétraiter le dataset Kaggle sur l'intention d’achat
* Entraîner deux modèles de classification :

  * ✅ **Random Forest**
  * ✅ **SVM (Support Vector Machine)**
* Évaluer leurs performances
* Visualiser les résultats (courbes, matrices)
* Présenter les insights et les prédictions dans un **Tableau Dashboard**

---

## ⚙ Technologies Utilisées

| Composant        | Outils / Bibliothèques                                                                                                         |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Langage          | Python 3.x                                                                                                                     |
| Machine Learning | Scikit-learn                                                                                                                   |
| Visualisation    | Matplotlib, Seaborn                                                                                                            |
| Dashboard        | Tableau Desktop (.twbx)                                                                                                        |
| Notebook         | Jupyter Notebook                                                                                                               |
| Dataset          | [Online Shoppers Intention (Kaggle)](https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset) |

---

## 🚀 Lancement du Pipeline

### 1. Installer les dépendances

```bash
pip install -r requirements.txt
```

### 2. Exécuter le notebook

Lance le fichier `notebooks/01_preprocessing_and_training.ipynb`. Il effectue :

* Nettoyage et encodage des données
* Séparation en jeu d'entraînement/test
* Entraînement des deux modèles
* Évaluation (accuracy, F1, ROC, confusion matrix)
* Sauvegarde des modèles (`models/`)
* Export des prédictions au format `.csv` pour Tableau

---

## 🧠 Modèles Utilisés

| Modèle           | Description                                       |
| ---------------- | ------------------------------------------------- |
| Random Forest    | Ensemble robuste, évite le surapprentissage       |
| SVM (RBF Kernel) | Classifieur efficace pour séparation non-linéaire |

---

## 📈 Dashboard Tableau

Le fichier `dashboards/tableau_dashboard.twbx` contient :

* La prédiction finale de chaque session (issue du modèle choisi)
* Des filtres dynamiques : par mois, type de visiteur, région, etc.
* Des graphiques : taux de conversion, importance des variables, comparaison SVM vs RF

> 📤 Le tableau est alimenté par un fichier `.csv` exporté depuis le notebook (`predictions.csv`).

---

## 📋 requirements.txt

```txt
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

---

## 📄 Licence

MIT License

---
