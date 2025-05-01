# AI-Driven-Ransomware-Detection-Using-Machine-Learning-Techniques

This project uses machine learning techniques to detect ransomware from Windows Portable Executable (PE) files using static analysis.

## Overview
We analyze static features of PE files and apply ML models to classify files as benign or malicious. The best-performing model is Random Forest, achieving over 98% accuracy and 99.7% AUC-ROC.

## Dataset
- Source: Kaggle (62,000+ PE file samples)
- Features: File metadata and static PE attributes
- Target: `Benign` (1 = benign, 0 = malicious)

## ML Models Used
- Random Forest (Best performer)
- Support Vector Machine (SVM)
- XGBoost
- Logistic Regression

## Evaluation Metrics
- Accuracy, Precision, Recall, F1 Score, AUC-ROC
- Visualizations include Confusion Matrix, ROC Curve, and Correlation Heatmap

## Results

| Model               | Accuracy | Precision | Recall | F1   | AUC-ROC |
|---------------------|---------:|----------:|-------:|-----:|--------:|
| Random Forest       | 0.987    | 0.99      | 0.98   | 0.99 | 0.997   |
| XGBoost             | 0.985    | 0.99      | 0.98   | 0.98 | 0.995   |
| SVM                 | 0.800    | 0.95      | 0.57   | 0.72 | 0.810   |
| Logistic Regression | 0.780    | 0.87      | 0.59   | 0.70 | 0.720   |

**Selected Model**: Random Forest (saved as `malware_detection_model.pkl`)

## Requirements

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
