# 🚗 Car Price Prediction – Data Preprocessing and Analysis Project

This project focuses on preparing a dataset for predicting used car prices by performing comprehensive **data preprocessing**. The pipeline includes handling missing values, encoding categorical variables, filtering out outliers, and grouping categorical features for optimal modeling performance.

---

## 📁 Dataset

The dataset (`cars.csv`) contains the following columns:

- `Brand`
- `Model`
- `Year`
- `Fuel_Type`
- `Transmission`
- `Owner_Type`
- `Kilometers_Driven`
- `Mileage`
- `Engine`
- `Power`
- `Seats`
- `Price`

---

## 🛠 Main Steps

### 🔹 1. Handling Missing Values
- Missing values in columns like `Mileage`, `Engine`, `Power`, and `Seats` were filled using appropriate statistical methods such as **mean**, **median**, or **mode**.
- Numerical columns were cleaned and converted into float format.

### 🔹 2. Encoding Categorical Variables
- `Fuel_Type` and `Transmission` were **label encoded** into numerical values.
- `Owner_Type` was **one-hot encoded** into dummy variables.

### 🔹 3. Grouping Brand and Model
- The `Brand` and `Model` columns were **grouped based on their average price**, reducing the impact of rarely occurring entries.
- This grouping improves the model's ability to generalize by minimizing the noise from less common categories.

### 🔹 4. Outlier Detection and Removal
- Outliers were identified in columns such as `Price`, `Kilometers_Driven`, `Mileage`, `Power`, and `Engine` using the **Z-score method** (with a threshold of ±3).
- These outliers were removed to enhance model accuracy.

### 🔹 5. Preparing the Final Dataset
- All features were converted to numerical values and structured for machine learning algorithms.
- The cleaned dataset can be saved in `.csv` or `.pkl` format for further modeling.

---

## 🧰 Libraries Used

```python
pandas         # Data manipulation and analysis
numpy          # Numerical operations
matplotlib     # Data visualization
sklearn        # Machine learning tools (preprocessing, encoding, outlier detection)
