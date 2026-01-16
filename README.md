# Construction Cost Prediction Using Linear Regression (Machine Learning)

This project builds a **regression** model to predict the **total construction cost (in Lakhs)** based on factors like **area, number of floors, and labor cost per day**. It follows the standard ML workflow:

**Problem Statement → Selection of Data → Collection of Data → EDA → Train/Test Split → Model Selection → Evaluation Metric**

---

## Problem Statement
Construction cost depends on multiple factors such as built-up area, floors, and labor charges.  
The goal of this project is to predict the **Total Construction Cost (Lakhs)** using key inputs.

**Input Features:**
- `Area_sqft`
- `Floors`
- `Labor_Cost_per_day`

**Output:**
- Predicted `Total_Cost_Lakhs`

---

## Selection of Data
**Dataset Type Used:** Structured tabular dataset (numeric features)

Why this dataset is suitable:
- Clear regression target (`Total_Cost_Lakhs`)
- Numeric features are easy to train with regression models
- Useful for learning real-world cost estimation workflows

---

## Collection of Data
In this project, the dataset is created inside the code as a sample dictionary and converted into a DataFrame using `pandas`.  
(The same workflow works with real construction datasets loaded using `pd.read_csv()`.)

---

## EDA (Exploratory Data Analysis)
EDA is kept simple to confirm the dataset before training:
- Confirm feature columns and target column
- Understand basic value ranges for area, floors, labor cost, and total cost

---

## Dividing Training and Testing
The dataset is split using `train_test_split`:
- Training set: model learns relationships
- Testing set: model is evaluated on unseen data

---

## Model Selection
**Model used:** Linear Regression (`sklearn.linear_model.LinearRegression`)

Why Linear Regression:
- Simple baseline model for numeric regression problems
- Easy to train and interpret for beginners
- Works well when relationships are roughly linear

---

## Evaluation Metric (Used in this Project)
This project uses **R² Score** (`r2_score`) to evaluate model performance.

Simple meaning:
- R² shows how well the model fits the test data
- Higher R² means predictions match actual cost values better

Used in code:
- `r2_score(y_test, y_pred)`

---

## Main Libraries Used (and why)

1. `pandas`  
   - Creates and manages the dataset as a DataFrame.

2. `numpy`  
   - Supports numerical operations and array handling.

3. `sklearn.model_selection.train_test_split`  
   - Splits the dataset into training and testing sets.

4. `sklearn.linear_model.LinearRegression`  
   - Trains the regression model.

5. `sklearn.metrics.r2_score`  
   - Evaluates model performance using R² score.

---

## Output
- Printed **R² Score** for model performance
- Predicted construction cost for a new input (example: `[1600, 2, 1500]`)

---

## Developer
Grishma C.D
