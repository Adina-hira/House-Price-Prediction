House Price Prediction using Linear Regression

**Project Overview:**

This project builds a **Linear Regression model** to predict house prices based on multiple housing features.

The goal is to understand:
1. How linear regression works
2. How to clean real-world data
3. How to evaluate a regression model
4. How well can house prices be predicted using structured features?

The dataset used is the **House Prices - Advanced Regression Techniques** dataset available through OpenML.

**Dataset Description:**

The dataset contains detailed information about residential homes, including:

1. Lot size
2.  Number of rooms
3. Year built
4. Overall quality
5. Garage size
6. Basement area
7. And many more features

**Target Variable:**

```
SalePrice → Final house sale price
```

---

**Technologies Used:**

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn

---

**Project Workflow:**

1. Data Loading

* Dataset fetched from OpenML
* Converted into a Pandas DataFrame

---

2. Data Cleaning

* Dropped columns with excessive missing values
* Filled numerical missing values using **median**
* Filled categorical missing values using **mode**

---

3. Encoding

* Converted categorical variables into numeric form using Label Encoding

---

4. Feature Selection

* Removed `Id`
* Defined:

  * **X → Input features**
  * **y → SalePrice**

---

5. Train-Test Split

* 80% training data
* 20% testing data

---

6.  Model Training

Used:

```python
LinearRegression()
```

The model learns a formula:

```
Price = b0 + b1x1 + b2x2 + ... + bn xn
```

---

7. Model Evaluation

Two evaluation metrics were used:

####  RMSE (Root Mean Squared Error)

* Measures average prediction error
* Lower value = better model

####  R² Score

* Measures how much variation in price is explained by the model
* Range: 0 to 1
* Higher value = better model

---

8. Visualization:

A scatter plot was created comparing:

* Actual Prices
* Predicted Prices

If points are close to the diagonal line → the model performs well.

---

9. Results Interpretation:

* A higher R² score indicates strong explanatory power.
* RMSE shows the average prediction error in price units.
* The model successfully captures most pricing trends but may struggle with extreme values.

---

10. Possible Improvements:

This is a baseline model. Performance can be improved by:

* Using One-Hot Encoding instead of Label Encoding
* Applying feature scaling
* Removing multicollinearity
* Trying advanced models like:

  * Ridge Regression
  * Lasso Regression
  * Random Forest Regressor

---

11. Project Structure:

```
House_Price_Prediction.ipynb
README.md
```

---

**Conclusion:**

This project demonstrates how linear regression can be applied to real-world housing data to predict prices. It covers the complete pipeline:

Data → Cleaning → Modeling → Evaluation → Visualization

It serves as a strong foundation for more advanced regression techniques.



