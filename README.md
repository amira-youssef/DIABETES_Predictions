# 🩺 Diabetes Risk Prediction & Personalized Meal Recommendation System

This project is an end-to-end Machine Learning application that predicts diabetes risk, segments patients into health-based clusters, and generates personalized weekly meal plans based on BMI and Age.  
It also includes a Streamlit web application for real-time predictions and recommendations.

---

## 🚀 Features

### 🔹 1. Diabetes Risk Prediction  
A supervised ML model trained to predict whether a patient is likely to have diabetes.  
Includes:
- Data cleaning, preprocessing, and feature engineering  
- Model training (Logistic Regression / Random Forest / SVM / AutoML-ready)  
- Exported model (`classifier.pkl`) for deployment  

### 🔹 2. Patient Clustering  
Unsupervised learning (K-Means) to group patients by similar profiles.  
Used to understand risk categories and refine recommendations.

### 🔹 3. Content-Based Meal Recommendation System  
Generates a **7-day meal plan** tailored to the user based on:
- BMI  
- Age  
- Nutritional constraints  

The system:
- Normalizes features  
- Computes similarity between patients (Euclidean distance)  
- Extracts real meal plans from the dataset  
- Creates a complete breakfast/lunch/dinner/snack plan  

### 🔹 4. Streamlit Web Application  
The project includes a fully deployable `app.py` allowing users to:
- Enter personal health metrics  
- Get diabetes risk prediction  
- View cluster assignment  
- Receive a personalized weekly meal plan  
- Download the plan as CSV  

---

## 🧠 Tech Stack

- **Python**, **Pandas**, **NumPy**
- **Scikit-Learn** (classification, clustering, preprocessing)
- **Joblib** (model exporting)
- **Streamlit** (web deployment)
- **Matplotlib / Seaborn** (visualizations)
- Optional: **FLAML AutoML**

---

## 📦 Project Structure

├── data/
│ ├── diabetes_cleaned_final.csv
│ ├── meal_plans_complete.csv
│
├── models/
│ ├── classifier.pkl
│ ├── scaler.pkl
│ ├── cluster_model.pkl
│
├── app.py # Streamlit app
├── recommendation.py # Meal recommendation engine
├── training_notebook.ipynb # Data cleaning + model training
├── requirements.txt
└── README.md



---

## 🛠 How It Works

### **Step 1 — Data Preparation**
- Handle missing values  
- Detect and treat outliers  
- Normalize features  
- Train/validate ML models  

### **Step 2 — Build & Save Models**
Three models are saved for deployment:
- `classifier.pkl`  
- `scaler.pkl`  
- `cluster_model.pkl`  

### **Step 3 — Meal Recommendation Engine**
Implemented in `recommendation.py`.

### **Step 4 — Deployment (Streamlit)**
Run locally:
```bash
streamlit run app.py
