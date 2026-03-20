# CodeAlpha - Car Price Prediction 🚗💰

## 📌 Project Overview
This project is part of the **CodeAlpha Data Science Internship**.  
The goal is to predict the **selling price of cars** based on features such as year, present price, kilometers driven, fuel type, transmission, and ownership history.

## 📊 Dataset
- Source: Provided `car data.csv`
- Features:
  - Year
  - Present Price (current showroom price)
  - Driven kms (distance driven)
  - Fuel Type (Petrol/Diesel/CNG)
  - Selling type (Dealer/Individual)
  - Transmission (Manual/Automatic)
  - Owner (number of previous owners)
- Target: Selling Price

## ⚙️ Workflow
1. **Data Preprocessing**
   - Dropped `Car_Name` column
   - Encoded categorical features (`Fuel_Type`, `Selling_type`, `Transmission`)
2. **Train/Test Split**
   - 80% training, 20% testing
3. **Model Training**
   - Linear Regression
   - Decision Tree Regressor
   - Random Forest Regressor
4. **Evaluation**
   - R² score
   - RMSE (Root Mean Squared Error)
5. **Visualization**
   - Actual vs Predicted scatter plots
   - Residual plots
   - Feature importance (Random Forest)

## 📈 Results
- **Linear Regression**: R² ≈ 0.85  
- **Decision Tree**: Higher accuracy, risk of overfitting  
- **Random Forest**: Best performance, highest R² and lowest RMSE  
- Key predictors: `Present_Price`, `Year`, `Driven_kms`

## 🛠️ Libraries Used
- pandas
- numpy
- matplotlib
- scikit-learn

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/tashkidd1/CodeAlpha_CarPricePrediction.git