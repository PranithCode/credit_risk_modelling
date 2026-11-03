# 🔍 Credit Risk Prediction Web Application

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/XGBoost-006600?style=for-the-badge&logo=xgboost&logoColor=white" />
  <img src="https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white" />
</p>

> A web application that predicts **credit risk** based on personal and financial data using a trained **XGBoost ML model**. Built with a clean multi-step form on the front end and a robust Flask API on the backend.

🎯 **[Live Demo](https://credit-risk-predictor-02fj.onrender.com/)**

---

## 🚀 Features

- ✅ **Multi-Step Form:** Intuitive and grouped inputs for a smoother experience  
- ⚡ **Real-Time Prediction:** Instantly returns predictions using a Flask API  
- 🎯 **XGBoost Model:** High-performing classifier for credit risk prediction  
- 💻 **Clean & Responsive UI:** Built with Tailwind CSS for all screen sizes  
- 🌐 **Deployed on Render:** Live and accessible from anywhere  

---

## 🧠 Tech Stack

| Layer         | Tools Used                                  |
|---------------|---------------------------------------------|
| **Backend**   | Python, Flask                               |
| **Machine Learning** | Scikit-learn, XGBoost, Pandas, NumPy     |
| **Frontend**  | HTML, Tailwind CSS                          |
| **Server**    | Gunicorn                                    |
| **Deployment**| Render                                      |

---

## 📊 Feature Selection, Data Preprocessing & Model Improvement

A rigorous machine learning pipeline was implemented to ensure high accuracy and generalizability of the model.

---

### 🧪 Statistical Testing & Feature Selection

- ✅ **Chi-Square Test:** Assessed the dependency between categorical features (e.g., `MARITALSTATUS`, `EDUCATION`) and the target variable `Approved_Flag`. Features with **p-value < 0.05** were selected.
- ✅ **ANOVA F-Test:** Applied to numerical features to determine their statistical significance with respect to the target.
- ✅ **Variance Inflation Factor (VIF):** Removed features with **high multicollinearity (VIF > 6)** to avoid redundant information.
- ✅ **Hypothesis Testing:** Applied across feature types to support statistically sound feature engineering.

---

### 🧹 Data Cleaning & Preparation

- 🧼 **Handled Missing Values** using appropriate imputation techniques.
- 🔗 **Merged Two Datasets** to enhance the available features and improve prediction capability.
- 🧠 **Feature Encoding:** Used Label Encoding and One-Hot Encoding where necessary to convert categorical variables.
- 📐 **Data Alignment:** Ensured input format strictly matches the training data structure expected by the model.

---

### 🔧 Model Training & Optimization

- ⚙️ **Model Used:** `XGBoostClassifier`
- 🔍 **Hyperparameter Tuning:** Performed exhaustive **Grid Search** to find the optimal set of hyperparameters.
- 🔁 **Cross-Validation:** Integrated cross-validation during grid search to avoid overfitting.
- 📈 **Accuracy Boost:** Achieved a significant performance improvement, increasing model accuracy by **~78%** through tuning and preprocessing.

---

## ⚙️ How It Works

1. **🧾 User Input:** Multi-step form collects user data
2. **📤 API Request:** Data sent to `/predict` Flask endpoint as JSON
3. **🧪 Preprocessing:** Data is encoded/mapped to model format
4. **🤖 Prediction:** Model returns a class (0–3)
5. **🔁 Response Mapping:** Output mapped to risk labels (`P1`, `P2`, `P3`, `P4`)
6. **📺 Result Display:** Prediction shown dynamically on frontend

---

## 🧪 Local Setup

### 📥 Clone the Repository

```bash
git clone https://github.com/Ashish152003/Credit_Risk_Prediction.git
cd Credit_Risk_Prediction
```

### 🧰 Create Virtual Environment (Recommended)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

### ▶️ Run the Application

```bash
python app.py
```


---

## 📁 File Structure

```
Credit_Risk_Prediction/
├── app.py                 # Flask backend logic
├── xgb_best_model.pkl     # Trained ML model
├── requirements.txt       # Project dependencies
├── build.sh               # Deployment script for Render
└── templates/
    └── index.html         # Web interface (multi-step form)
```

---
