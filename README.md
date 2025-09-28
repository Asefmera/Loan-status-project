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

  
