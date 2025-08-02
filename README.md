# Walmart Sales Forecasting Project

## 📊 Project Overview

This project implements a comprehensive sales forecasting system for Walmart using machine learning techniques. The goal is to predict weekly sales for different stores and departments based on historical data and various features.

## 🎯 Project Objectives

- **Data Analysis**: Explore and understand Walmart sales data
- **Feature Engineering**: Create time-based features and rolling statistics
- **Model Development**: Build and compare multiple forecasting models
- **Performance Evaluation**: Assess model accuracy using RMSE and R² metrics
- **Advanced Analysis**: Implement seasonal decomposition and XGBoost forecasting

## 📁 Project Structure

```
ElevvoPathways Level3 Task7/
├── Level3Task7.ipynb          # Main Jupyter notebook
├── archive/                    # Dataset folder
│   ├── features.csv           # Store features and external data
│   ├── stores.csv             # Store information
│   ├── test.csv               # Test dataset
│   └── train.csv              # Training dataset
└── README.md                  # This file
```

## 📈 Dataset Description

### Data Files

| File | Shape | Description |
|------|-------|-------------|
| `features.csv` | (8,190, 12) | Store features, holidays, and external data |
| `stores.csv` | (45, 3) | Store information and characteristics |
| `test.csv` | (115,064, 4) | Test dataset for predictions |
| `train.csv` | (421,570, 5) | Training dataset with historical sales |

### Key Features

- **Store**: Store identification number
- **Dept**: Department number
- **Date**: Date of the sales record
- **Weekly_Sales**: Target variable (sales amount)
- **IsHoliday**: Holiday indicator
- **Temperature**: Average temperature
- **Fuel_Price**: Fuel price
- **CPI**: Consumer Price Index
- **Unemployment**: Unemployment rate
- **Size**: Store size
- **Type**: Store type

## 🚀 Implementation Steps

### Step 1: Data Loading and Exploration
- Load all CSV files from the `archive/` directory
- Display dataset shapes and sample data
- Understand data structure and relationships

### Step 2: Data Merging and Preparation
- Convert date columns to datetime format
- Merge training data with features and store information
- Sort data by Store, Department, and Date
- Final merged dataset: (421,570, 16) records

### Step 3: Feature Engineering
- **Time-Based Features**:
  - Year, Month, Week, Day extraction
  - Lag features (previous week sales)
  - Rolling averages (4-week, 8-week, 12-week windows)

### Step 4: Data Preprocessing
- Handle missing values
- Convert categorical variables to numeric
- Prepare features for modeling

### Step 5: Model Development

#### Linear Regression Model
- **Performance Metrics**:
  - RMSE: 5,382.75
  - R² Score: 0.9203

#### XGBoost Model
- **Performance Metrics**:
  - RMSE: 3,657.95
  - R² Score: 0.9636

### Step 6: Visualization
- Actual vs Predicted sales plots
- Time series analysis
- Model performance comparisons

## 🔬 Advanced Analysis

### Bonus Task 1: Seasonal Decomposition
- Implemented rolling averages with different windows
- Seasonal decomposition analysis for Store 1, Department 1
- Additive seasonal decomposition with 52-week period

### Bonus Task 2: XGBoost with Time-Aware Validation
- Advanced feature engineering with multiple rolling windows
- Time-aware train-test split (80-20)
- Enhanced XGBoost model with improved performance

## 📊 Results Summary

| Model | RMSE | R² Score | Performance |
|-------|------|----------|-------------|
| Linear Regression | 5,382.75 | 0.9203 | Good |
| XGBoost | 3,657.95 | 0.9636 | **Best** |

## 🛠️ Technical Requirements

### Python Packages
```bash
pip install pandas
pip install scikit-learn
pip install numpy
pip install matplotlib
pip install xgboost
pip install statsmodels
pip install jupyter
```

### System Requirements
- Python 3.8+
- Jupyter Notebook
- 4GB+ RAM (for large dataset processing)

## 🚀 Getting Started

1. **Clone or download the project**
2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Open Jupyter Notebook**:
   ```bash
   jupyter notebook Level3Task7.ipynb
   ```
4. **Run all cells** to execute the complete analysis

## 📋 Key Features Implemented

### Data Processing
- ✅ Multi-dataset merging and alignment
- ✅ Time series feature engineering
- ✅ Missing value handling
- ✅ Data type conversions

### Machine Learning
- ✅ Linear Regression baseline model
- ✅ XGBoost advanced model
- ✅ Time-aware cross-validation
- ✅ Performance metrics evaluation

### Advanced Analytics
- ✅ Seasonal decomposition analysis
- ✅ Rolling statistics calculation
- ✅ Lag feature creation
- ✅ Visualization and plotting

### Model Evaluation
- ✅ RMSE (Root Mean Square Error)
- ✅ R² Score (Coefficient of Determination)
- ✅ Actual vs Predicted comparisons
- ✅ Time series visualization

## 📈 Key Insights

1. **XGBoost outperforms Linear Regression** with 32% lower RMSE
2. **Time-based features significantly improve** model performance
3. **Rolling averages and lag features** capture temporal patterns
4. **Seasonal decomposition reveals** clear patterns in sales data
5. **Store and department-specific** patterns are important for forecasting

## 🔧 Customization Options

- **Feature Engineering**: Add more time-based features
- **Model Tuning**: Optimize hyperparameters for better performance
- **Additional Models**: Implement LSTM, Prophet, or other time series models
- **Ensemble Methods**: Combine multiple models for improved accuracy

## 📝 Notes

- The project was originally developed in Google Colab and has been adapted for local execution
- All file paths have been updated to use local directory structure
- The dataset is included in the `archive/` folder
- Results are reproducible with the provided notebook

## 🤝 Contributing

Feel free to enhance the project by:
- Adding new features or models
- Improving documentation
- Optimizing performance
- Adding new visualizations

## 📄 License

This project is for educational purposes and follows standard academic practices.

---

**Author**: Abdullah  
**Project**: Walmart Sales Forecasting  
**Date**: 2024  
**Level**: 3 Task 7 