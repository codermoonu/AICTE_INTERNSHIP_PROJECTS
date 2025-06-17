---

# 💧 Water Quality Prediction - Optimized ML Pipeline

## 📌 Project Overview

This project focuses on predicting multiple water quality parameters using a supervised multi-output regression model built with machine learning techniques. By leveraging historical water quality data, this solution aims to support environmental monitoring and decision-making for early detection of water pollution.

---

## 🎯 Objectives

* Predict multiple water pollutants such as NH₄, BOD₅ (BSK5), Suspended Solids, O₂, NO₃, NO₂, SO₄, PO₄, and Cl⁻.
* Develop a scalable and interpretable machine learning model using Python.
* Evaluate the model’s performance with standard regression metrics.
* Visualize model predictions to enhance interpretability.

---

## 🧠 Techniques Used

* **MultiOutput Regression** with `MultiOutputRegressor`
* **Random Forest Regressor** as the base model
* **Feature Engineering**: Extraction of `year` and `month` from timestamps
* **Data Scaling**: Standardization using `StandardScaler`
* **Visualization**: Scatter plots comparing actual vs. predicted values

---

## 🗃️ Dataset

* File: `PB_All_2000_2021.csv`
* Parameters:

  * `NH4`, `BSK5`, `Suspended`, `O2`, `NO3`, `NO2`, `SO4`, `PO4`, `CL`
  * Includes `id` and `date` for each sample

---

## 🛠️ Technologies Used

* Python 3.12+
* **Pandas**, **NumPy** – Data handling
* **Scikit-learn** – Machine learning model and evaluation
* **Matplotlib**, **Seaborn** – Visualization
* **Jupyter Notebook** – Experimentation and development

---

## 🧪 Model Pipeline

### 1. Data Preprocessing

* Convert `date` to datetime format
* Extract `year` and `month` as features
* Sort by `id` and `date` for temporal order
* Drop missing rows (can be replaced with imputation)

### 2. Feature and Target Selection

* **Input Features**: `id`, `year`, `month`
* **Targets**: `NH4`, `BSK5`, `Suspended`, `O2`, `NO3`, `NO2`, `SO4`, `PO4`, `CL`

### 3. Train-Test Split

* 80% for training, 20% for testing

### 4. Model Building

* `RandomForestRegressor` wrapped with `MultiOutputRegressor`

### 5. Evaluation Metrics

* **R² Score** for goodness of fit
* **Mean Squared Error (MSE)** for error measurement

### 6. Visualization

* Actual vs Predicted scatter plots for each water parameter

---

## 📈 Sample Results

```
===== Model Evaluation Results =====
NH4        | R2 Score: 0.78 | MSE: 0.15
BSK5       | R2 Score: 0.81 | MSE: 0.23
O2         | R2 Score: 0.85 | MSE: 1.92
...
```

---

## 📂 Repository Structure

```
📦 WaterQualityPrediction/
├── PB_All_2000_2021.csv                     # Dataset
├── Water_Quality_Prediction_Optimized.ipynb # Main notebook
└── README.md                                # Project documentation
```

---

## 🚀 How to Run

1. Clone the repository

   ```bash
   git clone https://github.com/your-username/water-quality-prediction.git
   cd water-quality-prediction
   ```

2. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

3. Launch the notebook

   ```bash
   jupyter notebook Water_Quality_Prediction_Optimized.ipynb
   ```

---

---
## Internship Details
* Internship Type: AICTE Virtual Internship - Edunet Foundation
* Sponsor: Shell
* Duration: June 2025 (1 month)
* Focus Area: Machine Learning in Environmental Monitoring
