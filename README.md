# Medical Insurance Cost Prediction

This project predicts medical insurance charges using a **Linear Regression** model.

## Dataset
The dataset used in this project is from Kaggle:  
[Medical Insurance Dataset](https://www.kaggle.com/datasets/lokeshmendake/medical-insurance-cost-dataset)  

The dataset includes the following features:
- `age` – Age of the individual
- `sex` – Gender (`male`/`female`)
- `bmi` – Body Mass Index
- `children` – Number of children
- `smoker` – Smoking status (`yes`/`no`)
- `region` – Geographic region (`southwest`, `southeast`, `northwest`, `northeast`)
- `charges` – Individual medical costs (target)

## Steps Followed
1. **Data Cleaning & Outliers Handling**:  
   - Outliers in `bmi` and `charges` were capped using the IQR method.
2. **Categorical Encoding**:  
   - `sex`, `smoker`, `region` were encoded using One-Hot Encoding (drop first to avoid multicollinearity).
3. **Scaling Numeric Features**:  
   - `age`, `bmi`, `children` were scaled using StandardScaler.
4. **Train/Test Split**:  
   - Data was split into 80% train and 20% test sets.
5. **Target Transformation**:  
   - Log transform applied on `charges` to handle skewness.
6. **Model Training**:  
   - Linear Regression was trained on the processed data.
7. **Prediction & Evaluation**:  
   - Metrics used: MSE, RMSE, R².

## Model Performance
- **MSE**: 51,674,775  
- **RMSE**: 7,188  
- **R²**: 0.7187  

> Note: RMSE reflects the average prediction error in USD.

## Insights
1. Smokers have a significantly higher impact on insurance charges compared to non-smokers.  
2. Higher BMI is associated with increased charges, but outliers were capped to reduce skewness.  
3. The number of children has a relatively minor effect on insurance costs.  
4. Geographic region has a small influence on charges.  
5. Linear Regression explains about 72% of the variance in charges (R² ≈ 0.72).  
6. The average prediction error (RMSE ≈ 7,188) indicates that individual predictions can still vary.

## Notebook Source
[Kaggle Notebook](https://www.kaggle.com/code/omniaelsaka/notebook49b06b721e)
