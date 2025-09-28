# Loan Approval Prediction (Python · ML)

Binary classification modeli ilə **kredit təsdiqi (Loan_Status)** proqnozu.
Pipeline: **data cleaning → feature engineering → modeling → evaluation**.

## Overview
Bu repoda kiçik kredit datası üzərində təsdiq qərarını (Y/N) proqnozlaşdırmaq üçün
sadə, təkrarlana bilən bir ML axını qurulub. Kateqorik dəyişənlər üçün
**frequency encoding**, ədədi dəyişənlər üçün **z-score** standartlaşdırma tətbiq olunub.
Model olaraq **Logistic Regression**, **Decision Tree** və **Random Forest** sınaqdan keçirilib.

## Dataset
- Fayl: `loan_data.csv`  (≈381 sətr, 13 sütun)
- Açar sütunlar: `Gender, Married, Dependents, Education, Self_Employed,
  ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term,
  Credit_History, Property_Area, Loan_Status`
- Target: `y = 1 (Loan_Status == 'Y'), əks halda 0`

### Təmizləmə Qaydaları (qısa)
- `Gender` → `Male` (mode)
- `Dependents` → `0`
- `Self_Employed` → `No`
- `Loan_Amount_Term` → orta (≈340.8)
- `Credit_History` → `1.0` (mode)
- `Loan_ID` sütunu çıxarıldı

## Quickstart

# 1) Klonla
git clone https://github.com/asefmera/loan-status-project.git
cd loan-status-project

### 2) Virtual mühit (opsional) və quraşdırma
python -m venv .venv
# macOS/Linux:
source .venv/bin/activate
# Windows:
# .venv\Scripts\activate

pip install -r requirements.txt

### 3) Datası qoy
`loan_data.csv` faylını repo kökünə və ya `data/` qovluğuna yerləşdirin.

### 4) Notebook və ya skript

### Notebook ilə işlətmək**
```bash
jupyter lab
# və ya:
jupyter notebook

jupyter lab   # və ya: jupyter notebook
# Notebook-u aç, hüceyrələri ardıcıl işlə

# Alternativ olaraq skript:
# python src/train.py  (əgər src/ altında skript saxlayırsansa)

### Project Structure
loan-status-project/
│
├── data/
│   └── loan_data.csv         # Dataset (əsas fayl)
│
├── src/
│   └── train.py              # Skript (model training + nəticələr)
│
├── notebooks/
│   └── loan_modeling.ipynb   # Jupyter Notebook (addım-addım analiz)
│
├── requirements.txt          # Lazımi paketlər
├── README.md                 # Layihə təsviri
└── .gitignore                # Opsional (venv, pycache və s. istisna üçün)
##  Requirements

Layihəni işlətmək üçün əsas paketlər:

- pandas  
- numpy  
- scikit-learn  
- seaborn  
- matplotlib  
- plotly  
- jupyter

  
