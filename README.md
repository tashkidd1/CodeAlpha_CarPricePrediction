# 🚗 Car Price Prediction — Machine Learning Regression

> **Internship Project | CodeAlpha Data Science Internship**  
> Predicting used car selling prices using supervised machine learning — comparing Linear Regression, Decision Tree, and Random Forest models.

---

## 📌 Project Overview

This project builds and evaluates regression models to predict the **selling price of used cars** based on features such as year of purchase, present price, fuel type, transmission, and ownership history. Three models are trained and benchmarked side-by-side, with performance assessed using R² and RMSE metrics.

---

## 🗂️ Table of Contents

- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Workflow](#-workflow)
- [Models & Results](#-models--results)
- [Visualizations](#-visualizations)
- [How to Run](#-how-to-run)
- [Key Findings](#-key-findings)
- [Internship Context](#-internship-context)

---

## 📁 Dataset

| Attribute | Details |
|-----------|---------|
| **File** | `car data.csv` |
| **Target Variable** | `Selling_Price` (in lakhs) |
| **Features** | `Year`, `Present_Price`, `Driven_kms`, `Fuel_Type`, `Selling_type`, `Transmission`, `Owner` |
| **Preprocessing** | Dropped `Car_Name` (identifier), one-hot encoded categorical columns |

---

## 📂 Project Structure

```
car-price-prediction/
│
├── car_price_prediction.ipynb    # Main ML notebook
├── car data.csv                  # Dataset
└── README.md                     # Project documentation
```

---

## 🔄 Workflow

The notebook follows a standard machine learning pipeline:

1. **Data Loading & Inspection** — Load CSV, preview structure with `.head()`, `.info()`, `.describe()`
2. **Feature Engineering**
   - Drop non-predictive column (`Car_Name`)
   - One-hot encode categorical features: `Fuel_Type`, `Selling_type`, `Transmission`
3. **Train/Test Split** — 80/20 split with `random_state=42` for reproducibility
4. **Model Training** — Three regression models trained on the same data split
5. **Model Evaluation** — R² and RMSE computed for each model
6. **Visualization** — Actual vs. Predicted scatter plots for all three models

---

## 🤖 Models & Results

Three regression models were trained and compared:

| Model | Description |
|-------|-------------|
| **Linear Regression** | Baseline model — assumes linear relationships between features and price |
| **Decision Tree Regressor** | Non-linear model that splits data on feature thresholds |
| **Random Forest Regressor** | Ensemble of 100 decision trees — reduces variance and overfitting |

> **Metrics used:**
> - **R²** (coefficient of determination) — closer to 1.0 is better
> - **RMSE** (root mean squared error) — lower is better

---

## 📈 Visualizations

**Actual vs. Predicted Price — All Three Models**

A 1×3 subplot scatter chart compares each model's predictions against actual selling prices. The red dashed diagonal represents a perfect prediction. A tighter cluster along this line indicates a stronger model.

---

## ▶️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/tashkidd1/car-price-prediction.git
cd car-price-prediction
```

### 2. Install Dependencies

```bash
pip install pandas scikit-learn matplotlib jupyter
```

### 3. Launch the Notebook

```bash
jupyter notebook car_price_prediction.ipynb
```

> Make sure `car data.csv` is in the same directory as the notebook before running.

---

## 💡 Key Findings

- 🌲 **Random Forest outperformed both baseline models**, achieving the highest R² and lowest RMSE — demonstrating the value of ensemble methods for non-linear regression tasks.
- 📉 **Linear Regression** provided a solid baseline but was limited by its assumption of linear relationships between features and price.
- 🌳 **Decision Tree** captured non-linear patterns but was prone to overfitting compared to the Random Forest ensemble.
- ⛽ **Fuel type and transmission** type were strong categorical predictors of price after one-hot encoding.
- 📅 **Present price and year of manufacture** were among the most influential numerical features in predicting resale value.

---

## 🎓 Internship Context

This project was completed as part of the **CodeAlpha Data Science Internship**. The objective was to apply the full supervised machine learning workflow — from raw data to model evaluation — using Python's core ML stack.

**Skills demonstrated:**
- Data preprocessing and feature engineering with Pandas
- Categorical encoding (one-hot encoding)
- Supervised ML model training with Scikit-Learn
- Model evaluation using R² and RMSE
- Comparative model analysis with visualizations

---

## 📬 Contact

**Tashinga Ncube**  
GitHub: [@tashkidd1](https://github.com/tashkidd1)

---