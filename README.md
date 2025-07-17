Updated README with full project description, results, and architecture
# 🚑 Smart Re-admit: AI-Powered Patient Re-admission Predictor

Predicting patient re-admissions using AI to improve healthcare efficiency and outcomes.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![ML](https://img.shields.io/badge/Machine_Learning-Yes-green)
![Deep Learning](https://img.shields.io/badge/Deep_Learning-MLP%20%2F%20LSTM-purple)
![Accuracy](https://img.shields.io/badge/Accuracy-89.03%25-success)

---

## 📌 Project Overview

**Smart Re-admit** is a machine learning and deep learning-based project designed to predict whether a patient will be re-admitted to the hospital after discharge (particularly after 30 days). Leveraging Electronic Health Records (EHR), this system provides early warnings to healthcare providers for timely intervention.

> 🏥 Developed as a major academic project at Sir C R Reddy College of Engineering under the mentorship of M. Ganesh Babu, Asst. Professor.

---

## 🎯 Objectives

- Predict patient re-admissions using structured healthcare data.
- Implement robust data preprocessing (missing value handling, encoding, scaling).
- Address class imbalance using **SMOTEENN**.
- Compare multiple models including **XGBoost, Random Forest, MLP, and LSTM**.
- Tune models using **RandomizedSearchCV**.
- Provide real-time predictions via **Streamlit web app**.
- Analyze top features influencing re-admission risk.

---

## 📊 Dataset

- Source: [UCI Diabetic Dataset](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)
- Features: 35 (after cleaning) including:
  - Demographics (age, gender)
  - Visit details (number of inpatient visits, lab procedures)
  - Medications (insulin, metformin)
  - Diagnoses (diag_1, diag_2, diag_3)
- Target:
  - `1` = Re-admitted after >30 days
  - `2` = Not Re-admitted

---

## 🧠 Models Used

| Model              | Accuracy |
|-------------------|----------|
| Logistic Regression | 72%      |
| Random Forest       | 74%      |
| **XGBoost**         | **89.03% ✅** |
| MLP (Neural Net)    | 89%      |
| LSTM (DL)           | 98% (overfitted - not deployed) |

> ✅ Final deployed model: **XGBoost** (due to generalizability and interpretability)

---

## 🧰 Tech Stack

| Category              | Tools / Libraries                        |
|-----------------------|------------------------------------------|
| Language              | Python 3.10                              |
| ML Libraries          | Scikit-learn, XGBoost, imbalanced-learn |
| Deep Learning         | Keras, TensorFlow                        |
| Visualization         | Matplotlib, Seaborn                      |
| Deployment            | Streamlit                                |
| IDE/Platforms         | Google Colab, Jupyter Notebook           |

---

## 🧪 Key Features

- **Preprocessing**: Categorical encoding, scaling, missing value handling
- **Balancing**: SMOTEENN for robust class handling
- **Evaluation**: Accuracy, Precision, Recall, F1-Score, ROC-AUC
- **Explainability**: Top 10 features ranked by importance
- **Deployment**: Interactive app for CSV upload, predictions, and feature visualization

---

## 🧪 Streamlit App Preview

```bash
streamlit run app.py
```
## 🔄 Re-admission Prediction Process Overview

Here’s how the system works:

### 📥 Upload
User uploads a `.csv` file containing patient EHR (Electronic Health Record) data through the Streamlit interface.

### ⚙️ Preprocessing
- Missing values handled
- Categorical features encoded
- Feature scaling applied

### 🧠 Prediction
- Preprocessed data is passed through the trained **XGBoost model**

### 📊 Output
- Displays whether the patient is likely to be re-admitted:
  - `1` = Yes (Re-admitted after 30+ days)
  - `2` = No (Not re-admitted)
- Visuals such as **feature importance** charts are shown within the UI

✅ This process enables fast, reliable, and non-technical risk prediction for hospitals and care teams.

---

## 🔍 Results

### ✅ Best Model: XGBoost

**Evaluation Metrics:**
- **Accuracy:** 89.03%
- **Precision:** 88.50%
- **Recall:** 89.10%
- **F1-Score:** 88.80%
- **AUC Score:** 0.92

> High recall and F1-score indicate that the model performs well in detecting high-risk patients and minimizing false negatives.

---

### 🔬 Top Predictive Features (Ranked by Importance)

1. `number_inpatient`  
2. `num_medications`  
3. `time_in_hospital`  
4. `number_diagnoses`  
5. `admission_type_id`  
6. `discharge_disposition_id`  
7. `age`  
8. `a1cresult`  
9. `insulin`  
10. `diag_1`

---

## 🚀 Future Scope

- 🔄 Real-time integration with hospital management systems
- 📱 Mobile-friendly prediction interface for clinicians
- 📊 Integration with live EHR data streams for adaptive learning
- 🩺 Personalized care recommendations based on patient risk profile
- ☁️ Cloud deployment of Streamlit app

---

## 🧑‍💻 Author

**Tanna Naga Sri Durga Mallesh**  
Department of Computer Science and Engineering  
Sir C R Reddy College of Engineering, Eluru  
🔗 [GitHub Profile](https://github.com/TNSDMallesh)

---

## 📜 License

This project is licensed under the **MIT License** – feel free to use and modify with credit.

---

## 🤝 Acknowledgments

## 🤝 Acknowledgments

Special thanks to my **Gen AI & Prompt Engineering tutor – [Datavalley.ai](https://datavalley.ai)**  
and my project guide **Mr. M. Ganesh Babu**,  
Assistant Professor, Department of CSE,  
Sir C R Reddy College of Engineering,  
for their constant support and expert guidance throughout this project.
