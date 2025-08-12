# Fetal Health Classification Using Machine Learning

## 📌 Project Overview

This project focuses on predicting fetal health conditions using machine learning techniques based on Cardiotocogram (CTG) data. The classification task includes three categories: **Normal**, **Suspect**, and **Pathological**, aiming to support early detection of complications and timely clinical intervention to reduce maternal and fetal mortality.

## 🎯 Objective

To develop accurate and efficient ML models that classify fetal health using features derived from CTG data. This is targeted at providing clinical decision-making support in resource-constrained settings.

## 📚 Dataset

- **Source**: Kaggle
- **Records**: 2,126
- **Target**: `fetal_health` (1: Normal, 2: Suspect, 3: Pathological)
- **Features**: Derived from ultrasound-based CTG exams including fetal heart rate, movements, contractions, decelerations, and histogram metrics.

## 🔍 Data Preprocessing

- No missing values detected.
- Feature scaling was done using `StandardScaler`.
- Train-Test split: 70% training, 30% testing.

## 🛠️ Models Implemented

### K-Nearest Neighbors (KNN)
- k=5, used uniform weights
- Accuracy: ~91%
- Good performance with consistent cross-validation results

### Logistic Regression
- Applied multinomial classification
- Hyperparameter tuning using GridSearchCV
- Accuracy: 88–90%
- Slight performance gain on tuning

### Support Vector Machine (SVM)
- Kernel: RBF (after tuning)
- Accuracy: 93%
- Strong performance on Suspect/Pathological classification

### Random Forest (Best Performer)
- Tuned with GridSearchCV
- Training Accuracy: 99.79%
- Testing Accuracy: 94.67%
- Best F1 and ROC-AUC score among all models

## 📈 Evaluation Metrics

- Accuracy, Precision, Recall, F1-Score
- Confusion Matrix for class-specific insights
- ROC-AUC: Random Forest yielded the highest curve and score

## 🧠 Key Takeaways

- Data cleaning early in the pipeline led to efficient model tuning.
- Manual feature selection improved results over automated methods for this dataset.
- Random Forest provided superior balance between generalization and sensitivity.

## 🔗 Applications

- **Healthcare Providers**: Decision support for obstetricians
- **Hospitals**: Early warning systems in maternity wards
- **Public Health**: Support towards achieving SDGs in maternal care

## 📂 Project Structure

```
project/
│
├── data/
│   └── fetal_health_data.csv (Not uploaded due to size – [Download here](https://drive.google.com/drive/u/2/folders/10SXfkg7ILeiD_uWQwOtYs24pn3x7qtr2))
├── notebooks/
│   └── knn_model.ipynb
│   └── svm_model.ipynb
│   └── rf_model.ipynb
│   └── logistic_model.ipynb
├── visuals/
│   └── plots, heatmaps, ROC curves
├── report/
│   └── final_report.pdf
├── README.md
```

## 📝 Citation

Ayres de Campos et al. (2000). *SisPorto 2.0: A Program for Automated Analysis of Cardiotocograms*. J Matern Fetal Med, 5:311-318.

## 🧾 License

Dataset is publicly accessible; cite the authors appropriately.

## 🙌 Acknowledgements

Thanks to our professor, TAs, and peer reviewers for feedback throughout the development of this project.

---

🚨 **Note**: Due to size limits on GitHub, the dataset is hosted externally. You can access it here: [Download Dataset](https://drive.google.com/drive/u/2/folders/10SXfkg7ILeiD_uWQwOtYs24pn3x7qtr2)