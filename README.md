# 🛍️ Online Shoppers Purchasing Intention

A machine learning project to predict whether an online user will make a purchase based on their browsing behavior. The pipeline uses **Decision Tree** and **SVM** models, with results visualized in an **interactive dashboard built with Tableau Desktop**.

## 📁 Project Structure

```
OnlineShoppersML/
├── data/
│   └── online_shoppers_intention.csv          # Original dataset
├── notebooks/
│   ├── 01_data_preprocessing.ipynb             # Data cleaning, encoding, and splitting
│   └── 02_model_training.ipynb                  # Training and evaluation of Decision Tree & SVM models
├── models/
│   ├── dt_model.pkl                            # Saved Decision Tree model
│   └── svm_model.pkl                           # Saved SVM model
├── dashboards/
│   └── tableau_dashboard.twbx                   # Tableau Desktop dashboard
├── requirements.txt
└── README.md
```

## 🎯 Project Goals

* Preprocess the Kaggle Online Shoppers Purchasing Intention dataset
* Train two classification models:

  * ✅ **Decision Tree**
  * ✅ **Support Vector Machine (SVM)**
* Evaluate model performances
* Visualize results (ROC curves, confusion matrices, etc.)
* Present insights and predictions in a **Tableau Dashboard**

## ⚙ Technologies Used

| Component        | Tools / Libraries                                                                                                                         |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Language         | Python 3.x                                                                                                                                |
| Machine Learning | Scikit-learn                                                                                                                              |
| Visualization    | Matplotlib, Seaborn                                                                                                                       |
| Dashboard        | Tableau Desktop (.twbx)                                                                                                                   |
| Notebook         | Jupyter Notebook                                                                                                                          |
| Dataset          | [Online Shoppers Purchasing Intention (Kaggle)](https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset) |

## 🚀 How to Run

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Run the notebooks in order

* Run `notebooks/01_data_preprocessing.ipynb`
  *(Data cleaning, encoding, and train/test splitting)*

* Run `notebooks/02_model_training.ipynb`
  *(Training, evaluation of Decision Tree and SVM, model saving, exporting predictions to CSV for Tableau)*

## 🧠 Models Used

| Model            | Description                                        |
| ---------------- | -------------------------------------------------- |
| Decision Tree    | Interpretable model, effective for rule-based data |
| SVM (RBF Kernel) | Powerful classifier for non-linear data separation |

## 📈 Tableau Dashboard

* File: `dashboards/tableau_dashboard.twbx`
* Visualizations: Session-level predictions, conversion rates, dynamic filters by month, visitor type, region, etc.
* Data: CSV file exported from the notebook (`predictions.csv`)

## 📋 requirements.txt

```txt
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

## 📄 License

MIT License
