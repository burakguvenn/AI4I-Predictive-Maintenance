# AI4I 2020 Predictive Maintenance Analysis 🏭

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Lib-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
This project aims to develop a **Predictive Maintenance** system for smart factories using the Industry 4.0 paradigm. By analyzing sensor data (temperature, torque, rotational speed) collected from production machines, the model predicts potential failures before they occur.

The project utilizes the **AI4I 2020 Predictive Maintenance Dataset** from the UCI Machine Learning Repository.

## 📂 Dataset Features
The dataset consists of 10,000 data points stored as rows with 14 features:
* **Air temperature [K]:** Generated using a random walk process.
* **Process temperature [K]:** Generated using a random walk process.
* **Rotational speed [rpm]:** Calculated from a power of 2860 W.
* **Torque [Nm]:** Normally distributed around 40 Nm.
* **Tool wear [min]:** The quality variants H/M/L add 5/3/2 minutes of tool wear.
* **Target:** Label '0' indicates no failure, '1' indicates machine failure.

## ⚙️ Methodology & Tech Stack
* **Data Preprocessing:** Handling missing values, dropping irrelevant IDs.
* **Feature Engineering:** Created `Delta_Temp` (Process Temp - Air Temp) to capture thermodynamic efficiency.
* **Algorithms Compared:**
    1.  **Logistic Regression** (Baseline)
    2.  **Random Forest Classifier** (Selected Model)

## 📊 Key Results
The **Random Forest** model outperformed the baseline with superior accuracy and recall rates.

| Model | Accuracy |
| :--- | :--- |
| Logistic Regression | 97.4% |
| **Random Forest** | **98.7%** |

### Confusion Matrix (Random Forest)
The model successfully identifies the majority of machine failures with low false negatives.

![Confusion Matrix](confusion_matrix_rf.png)

### Feature Importance
The analysis revealed that **Torque** and **Rotational Speed** are the most critical factors leading to machine failure.

![Feature Importance](feature_importance.png)

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/AI4I-Predictive-Maintenance.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the script:
   ```bash
   jupyter notebook main.ipynb
   ```

## 🔗 References

    [1] UCI Machine Learning Repository - AI4I 2020 Dataset.

    [2] Breiman, L. (2001). Random Forests. Machine Learning.

    [3] Scikit-learn: Machine Learning in Python.

Author: [Burak]
