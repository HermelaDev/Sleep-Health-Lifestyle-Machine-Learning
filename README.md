<p align="center">
  <img src="ai-generated-8517712_960_720.jpg" alt="Sleep Health ML Banner" width="500" style="border-radius:10px;">
</p>

# 📘 Sleep Health & Lifestyle - Machine Learning Analysis

This project investigates how lifestyle behaviors, health indicators, and daily habits affect **sleep duration** using modern machine learning techniques.  
Using a dataset of 374 individuals, the project includes **EDA**, **feature engineering**, **regression modeling**, and a **Gradio-powered interactive prediction app**.

---

## 📊 Dataset Overview

- **Dataset:** Sleep Health and Lifestyle  
- **Rows:** 374  
- **Columns:** 14  

### **Key Features**

- Age  
- Gender  
- Occupation  
- Quality of Sleep  
- Physical Activity Level  
- Stress Level  
- BMI Category  
- Heart Rate  
- Daily Steps  
- Sleep Disorder  
- Systolic_BP, Diastolic_BP  
- **Target:** Sleep Duration  

---

## 🧹 Data Preprocessing

- Handled missing values (`Sleep Disorder` → `"None"`)
- Split blood pressure into `Systolic_BP` and `Diastolic_BP`
- Removed `Person ID` (identifier)
- Detected outliers using IQR
- Encoded categorical features using **Ordinal Encoding**
- Scaled numerical features for linear models
- Ensured consistent feature ordering for model training

---

## 🔍 Exploratory Data Analysis (EDA)

### **Key Insights**

- **Stress Level** has the strongest negative correlation with Sleep Duration (**−0.81**)  
- **Quality of Sleep** is strongly positively correlated (**+0.88**)  
- Higher physical activity and more daily steps slightly improve sleep  
- Individuals with **insomnia** show the lowest sleep duration  
- The **Normal BMI** category shows the highest average sleep duration  

### **Visuals Used (Plotly)**

- ✔ Interactive histograms  
- ✔ Correlation heatmap  
- ✔ Boxplots  
- ✔ Grouped bar charts  

---

## 🤖 Regression Models

The following models were trained:

| Model | MAE ↓ | RMSE ↓ | R² ↑ |
|-------|--------|----------|---------|
| Linear Regression | 0.206 | 0.273 | 0.888 |
| **Random Forest (One-Hot)** | **0.058** | **0.080** | **0.990** |
| Random Forest (Ordinal Encoder) | 0.086 | 0.114 | 0.981 |
| CatBoost Regressor | 0.072 | 0.097 | 0.986 |

### ⭐ Best Model:  
**Random Forest with One-Hot Encoding**

### ⭐ Most Interpretable Feature Importance:  
**CatBoost + Ordinal RF**

---

## 🔑 Feature Importance Summary

### **Top Predictors of Sleep Duration**
1. Quality of Sleep  
2. Stress Level  
3. Age  
4. Heart Rate  
5. Physical Activity Level  
6. Daily Steps  

### **Least Important**
- Gender  
- Occupation  
- BMI Category  

---

## 🖥️ Interactive Prediction App (Gradio)

This project includes a fully interactive GUI where users can enter lifestyle and health values to predict **sleep duration**.

### **Launch the app:**

```bash
pip install gradio
```
### ⭐ Features

- Uses the trained Random Forest pipeline
- Encodes categorical variables internally
- Predicts sleep duration in hours
- Serves as a model deployment simulation

### 🧪 How to Run the Project
1. Clone the repository
```bash
git clone https://github.com/<YourUsername>/Sleep-Health-Lifestyle-Machine-Learning.git
cd Sleep-Health-Lifestyle-Machine-Learning
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Open the notebook

Run:
```bash
Sleep_Health_Analysis.ipynb
```
4. Launch the Gradio app
```bash
demo.launch()
```
### 📁 Project Structure

📂 Sleep-Health-Lifestyle-Machine-Learning

│── 📄 README.md

│── 📄 requirements.txt

│── 📄 Sleep_Health_Analysis.ipynb

│── 📂 dataset/

│     └── Sleep_Health_and_Lifestyle_Dataset.csv

│── 📂 images/   (optional for plots)

└── 📄 LICENSE (optional)

### 🚀 Future Enhancements
- Add classification (predict Sleep Disorder)
- Cluster lifestyle groups
- Deploy Gradio app on HuggingFace Spaces
- Add Explainable AI (SHAP values)
- Build a dashboard (Streamlit or PowerBI)

### 👩🏽‍💻 Author
Hermela Seltanu Gizaw

Data Science & Analytics, USIU-Africa

Mastercard Foundation Scholar
