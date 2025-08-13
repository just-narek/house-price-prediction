# Boston House Prices - Linear Regression Analysis

A simple linear regression analysis to predict house prices based on the number of rooms using the Boston housing dataset.

## 📊 Project Overview

This project demonstrates a basic linear regression model that predicts house values based on the number of rooms. The analysis includes data exploration, model fitting using statsmodels, and visualization of results.

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation and analysis
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization
- **statsmodels** - Statistical modeling

## 📁 Dataset

The project uses `Boston_House_Prices.csv` containing:
- **Rooms**: Average number of rooms per dwelling
- **Distance**: Weighted distances to employment centers
- **Value**: Median value of owner-occupied homes (target variable)

### Dataset Statistics
- **Total records**: 506 rows
- **Features**: 3 columns
- **Missing values**: None
- **Duplicates**: Removed during preprocessing

## 🔍 Analysis Workflow

### 1. Data Loading & Preprocessing
```python
df = pd.read_csv('Boston_House_Prices.csv')
df = df.drop_duplicates()  # Remove duplicate records
```

### 2. Exploratory Data Analysis
- Check for missing values
- Remove duplicates
- Scatter plot visualization of Rooms vs Value

### 3. Simple Linear Regression
- **Dependent Variable**: House Value
- **Independent Variable**: Number of Rooms
- **Model**: Ordinary Least Squares (OLS) regression

### 4. Model Results
```
Linear Equation: Value = 9.1021 × Rooms - 34.6706
```

#### Key Statistics:
- **R-squared**: 0.484 (48.4% of variance explained)
- **F-statistic**: 471.8 (highly significant)
- **Rooms coefficient**: 9.1021 (each additional room increases value by ~$9,102)
- **Constant**: -34.6706

## 📈 Visualizations

The project generates:
1. **Scatter plot**: Relationship between Rooms and House Value
2. **Regression line plot**: Shows the fitted linear model with actual vs predicted values

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas matplotlib seaborn statsmodels
```

### Running the Analysis
1. Clone this repository
2. Ensure `Boston_House_Prices.csv` is in the project directory
3. Run the Jupyter notebook or Python script
4. View generated plots and regression results

## 📊 Results Interpretation

- **Positive relationship**: More rooms generally lead to higher house values
- **Model fit**: The R-squared of 0.484 indicates moderate explanatory power
- **Statistical significance**: All coefficients are highly significant (p < 0.001)
- **Practical interpretation**: Each additional room adds approximately $9,102 to the house value

## 🔮 Future Improvements

- [ ] Multiple linear regression including Distance variable
- [ ] Feature engineering and polynomial terms
- [ ] Cross-validation and model evaluation metrics
- [ ] Residual analysis and assumption checking
- [ ] Comparison with other regression algorithms

## 📝 Files Structure

```
├── Boston_House_Prices.csv    # Dataset
├── analysis.ipynb             # Jupyter notebook with analysis
├── linear_regression.png      # Generated visualization
└── README.md                  # This file
```

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements or additional analysis techniques.

## 📄 License

This project is open source and available under the MIT License.

---

*This analysis demonstrates basic linear regression concepts and serves as a foundation for more advanced housing price prediction models.*
