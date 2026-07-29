# 🚗 Ford Car Price Prediction

A regression-based machine learning project that predicts the resale price of used Ford cars using features such as model, year, mileage, transmission, fuel type, road tax, mpg, and engine size. The project covers the full workflow — exploratory data analysis, feature encoding, scaling, model training, and evaluation.

## 📌 Overview

Used-car pricing depends on a mix of categorical and numerical factors that don't always have an obvious relationship with price. This project explores that relationship on a real-world dataset of ~18,000 Ford listings and builds a Linear Regression model to estimate price, comparing two different categorical-encoding strategies along the way.

## 📊 Dataset

- **Source:** [Ford Car Price Prediction](https://www.kaggle.com/datasets/adhurimquku/ford-car-price-prediction) (Kaggle)
- **File used:** `ford.csv`
- **Rows:** 17,966
- **Columns:** 9
  - `model` — Car model
  - `year` — Year of manufacture
  - `price` — Selling price (target variable)
  - `transmission` — Transmission type
  - `mileage` — Distance driven
  - `fuelType` — Fuel type (Petrol/Diesel/Hybrid/Electric)
  - `tax` — Road tax
  - `mpg` — Miles per gallon
  - `engineSize` — Engine size in litres

## 🔍 Exploratory Data Analysis (EDA)

- Checked dataset shape, info, summary statistics, and missing values
- Visualized price distribution using a histogram
- Correlation heatmap between numerical features
- Boxplots of price vs. year, transmission, fuel type, model, and tax bins
- Scatter plot of mileage vs. price

## ⚙️ Data Preprocessing

- **Categorical encoding:** Tried both
  - One-Hot Encoding (`pd.get_dummies`) for `model`, `transmission`, `fuelType`
  - Label Encoding (`LabelEncoder`) for the same columns
- **Feature scaling:** Standardized numerical columns (`year`, `mileage`, `tax`, `mpg`, `engineSize`) using `StandardScaler`
- Split data into training and test sets (80/20 split)

## 🤖 Model

- **Algorithm:** Linear Regression (`sklearn.linear_model.LinearRegression`)
- Trained two versions of the model — one on one-hot encoded features and one on label-encoded + scaled features
- **Evaluation metric:** R² Score

### Results

| Model | Encoding Used | R² Score |
|-------|---------------|----------|
| Linear Regression | Label Encoding + Scaling | **0.737** |

## 🛠️ Tech Stack

- **Language:** Python
- **Data Handling:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn

## 💡 Key Skills Demonstrated

- Exploratory data analysis and data visualization
- Categorical feature encoding (One-Hot vs. Label Encoding)
- Feature scaling with `StandardScaler`
- Train/test splitting and model evaluation
- Regression modeling with Scikit-learn
- Interpreting model performance using R² score

## 📁 Project Structure

```
Ford-Car-Price-Prediction/
├── car-price-predict.ipynb   # Main notebook: EDA, preprocessing, model training & evaluation
└── README.md                 # Project documentation
```

## 🚀 How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/siddharajbarad7/Ford-Car-Price-Prediction.git
   cd Ford-Car-Price-Prediction
   ```
2. Install dependencies
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn kagglehub
   ```
3. Open and run the notebook
   ```bash
   jupyter notebook car-price-predict.ipynb
   ```

## 📈 Future Improvements

- Try other regression models (Random Forest, XGBoost, Gradient Boosting) for better accuracy
- Perform hyperparameter tuning
- Handle outliers (e.g., the `year` column has a max value of 2060, which is likely a data entry error)
- Feature engineering (e.g., car age instead of year)

## 👤 Author

**Siddharaj Barad**
GitHub: [@siddharajbarad7](https://github.com/siddharajbarad7)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
