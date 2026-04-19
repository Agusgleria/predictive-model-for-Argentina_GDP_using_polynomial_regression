# GDP Prediction in Argentine Provinces using Socioeconomic Indicators

## 📊 Project Overview

This project explores whether it is possible to estimate provincial GDP (Gross Domestic Product) in Argentina using socioeconomic indicators such as poverty rates and school dropout rates.

The goal is not only to build predictive models, but also to understand the relationships between variables and evaluate how reliable these indicators are for economic estimation.
The model evaluates how **Provincial Gross Domestic Product (GDP / PBI)** is related as a function of two key socio-economic variables:

- Poverty
- School dropout

---

## 🎯 Objective

The main goal is to assess:

- Whether it is possible to build a reliable model to estimate GDP using limited socioeconomic variables
- The strength and nature of the relationship between GDP and the selected predictors
- The performance of different machine learning approaches in this context

---

## 📂 Dataset

The dataset contains socio-economic indicators for different provinces in Argentina, including:

- Province name
- Provincial GDP (PBI)
- Poverty rate
- School dropout rate
- illiteracy
- birth mortal

among others

Each observation represents a province.

*Note: The dataset was compiled from publicly available statistical sources.*

---

## 🛠 Methodology

The project follows a standard machine learning workflow:

### 1. Data Preparation

- Data cleaning and preprocessing
- Handling missing values
- Outliers were retained due to their real-world significance
- Features were scaled before modeling
- Train-test split: 80% / 20%

### 2. Exploratory Data Analysis

- Correlation matrix revealed:
  - Weak negative correlation between GDP and poverty
  - Weak negative correlation between GDP and dropout rates
- Slight positive correlation between poverty and dropout
- Scatter plots showed high dispersion and weak trends
- Boxplots confirmed the presence of significant outliers

📌 Key insight: Relationships between variables are weak and likely non-linear.

### 3. Model Training

📈 Multiple Linear Regression
- Baseline model
- Poor performance with negative R², indicating it performs worse than a simple mean prediction

📊 Polynomial Regression (degrees 2–5)
- Captured non-linear relationships
- Performance improved as degree increased
- Higher-degree models showed overfitting (R² ≈ 1, zero error)

🔀 Clustering + Regression
- K-Means clustering used to segment provinces
- Optimal number of clusters: 3
- Separate regression models applied per cluster
- Improved performance in some segments (R² ≈ 0.5), but still inconsistent overall

### 4. Model Evaluation

Metrics used:

- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- R² Score

📌 Findings:

- Linear models performed poorly due to weak correlations
- Polynomial models improved fit but risked overfitting
- Clustering helped partially but did not fully solve the problem

---

## 📎 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

## 💡 Key Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory data analysis
- Feature scaling and handling missing values
- Regression modeling (linear and polynomial)
- Clustering techniques (K-Means)
- Model evaluation and interpretation
- Critical thinking and model validation

---

## 🚀 Results & Insights

- Poverty and school dropout rates are not strong predictors of GDP on their own
- The relationship between variables is complex and non-linear
- High model performance (e.g., R² = 1) can indicate overfitting rather than true predictive power
- Segmenting data (clustering) can improve results, but only partially
- Data quality and feature selection are more important than model complexity

🔎 Additional Insight (Feature Selection)

Using feature selection techniques (Lasso, RFE, SelectFromModel):
- Population and illiteracy rate emerged as stronger predictors
- A linear model using these variables explained ~99% of GDP variance

⚠️ However, results should be interpreted cautiously due to the small dataset size

---

## 👤 Author

Agus Gleria

Data Science & Analytics Portfolio
