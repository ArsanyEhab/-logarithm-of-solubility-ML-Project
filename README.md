# 🧪 Molecular Solubility Prediction (logS) using Machine Learning

This project builds a **Machine Learning model** to predict the **aqueous solubility (logS)** of molecules using their physicochemical properties.  
It applies **Linear Regression** and other regression models to understand how molecular descriptors influence solubility.

---

## 📘 Overview

Predicting solubility is a key challenge in **drug discovery** and **chemical design**.  
This model uses descriptors such as:
- **MolLogP** – Hydrophobicity (octanol–water partition coefficient)
- **MolWt** – Molecular weight
- **NumRotatableBonds** – Molecular flexibility
- **AromaticProportion** – Fraction of aromatic atoms

to predict:
- **logS** – Logarithm of aqueous solubility

---

## 🧩 Dataset

The dataset includes molecular descriptors and solubility values (`logS`).

📂 **Data Source:** [Delaney Solubility Dataset](https://github.com/dataprofessor/data/blob/master/delaney_solubility_with_descriptors.csv)  
Originally compiled by **John S. Delaney**, this dataset contains molecular properties computed from SMILES using **RDKit**.

| MolLogP | MolWt | NumRotatableBonds | AromaticProportion | logS |
|----------|--------|-------------------|--------------------|------|
| 2.45 | 180.16 | 3 | 0.25 | -2.1 |

💡 Each row represents one molecule, with:
- **MolLogP** → Hydrophobicity (octanol–water partition coefficient)  
- **MolWt** → Molecular weight  
- **NumRotatableBonds** → Molecular flexibility  
- **AromaticProportion** → Ratio of aromatic atoms  
- **logS** → Experimental aqueous solubility (target variable)


---

## ⚙️ Model Details

| Model | Training MSE | Training R² | Test MSE | Test R² | Graph |
|--------|---------------|-------------|-----------|----------|----------| 
| **Linear Regression** | 1.0075 | 0.7645 | 1.0207 | 0.7892 | <img width="250" height="250" alt="LR Graph" src="https://github.com/user-attachments/assets/d83ae73b-2916-4b92-9b8d-136cfb36cd93" /> |



✅ The model explains **~78% of the variance** in solubility  
✅ Shows **good generalization** with close train/test results  
✅ Provides interpretable feature effects on solubility  

---

### 🔮 Future Model Extensions

This project currently uses **Linear Regression** as a baseline model.  
In future updates, additional regression algorithms will be implemented and compared, such as:
- **Random Forest Regressor**
- **XGBoost Regressor**
- **Support Vector Regressor (SVR)**
- **Neural Network (Deep Learning)**

Each model will be evaluated using the same metrics (**MSE** and **R²**) to identify the best-performing approach for solubility prediction.



