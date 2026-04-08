# 🏠 House Price Prediction using Machine Learning

## 📌 Overview

This project focuses on predicting house prices using real-world real estate data.
An end-to-end machine learning pipeline was developed, including data preprocessing, feature engineering, model building, and evaluation.

The goal is to build an accurate and interpretable model for estimating property prices based on structural features.

---

## 📊 Dataset

* Source: Realtor dataset (real estate listings)
* Size: ~10,000 sampled records (from large dataset)
* Features include:

  * Price (target variable)
  * Bedrooms, Bathrooms
  * House Size
  * Acre Lot
  * Property Status

---

## ⚙️ Data Preprocessing

* Removed irrelevant columns (`brokered_by`, `street`, `zip_code`, `prev_sold_date`)
* Handled missing values using median imputation
* Removed outliers using **IQR method**
* Applied **log transformation** on target variable to reduce skewness
* Encoded categorical variable (`status`) using one-hot encoding

---

## 🧠 Feature Engineering

* Created interaction features:

  * `bed_bath_ratio`
  * `size_per_room`
* Improved model’s ability to capture relationships between variables

---

## 🤖 Models Used

* Linear Regression (baseline)
* Random Forest Regressor
* XGBoost Regressor (final model)

---

## ⚡ Hyperparameter Tuning

* Applied **GridSearchCV** on XGBoost
* Optimized parameters:

  * learning_rate
  * max_depth
  * n_estimators

---

## 📈 Model Evaluation

| Model         | MAE       | RMSE      |
| ------------- | --------- | --------- |
| Random Forest | ~148K     | ~209K     |
| XGBoost       | ~140K     | ~201K     |
| Tuned XGBoost | **~138K** | **~200K** |

👉 Tuned XGBoost achieved the best performance.

---

## 📊 Visualizations

* Price distribution (log scale)
* Correlation heatmap
* Actual vs Predicted plot
* Residual analysis
* Feature importance (Top contributing features)

---

## 🔍 Key Insights

* House size and room-related features strongly influence price
* Model performs well for mid-range properties
* Performance is limited by feature representation rather than model complexity

---

## 🚀 Conclusion

A robust machine learning pipeline was developed for house price prediction.
Tuned XGBoost provided the best performance, demonstrating the effectiveness of boosting algorithms for structured data.

Further improvements can be achieved by incorporating location-based and economic features.

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn

---

## 📁 Project Structure

```
├── data/
├── notebook.ipynb
├── README.md
```

---

## 📌 Future Work

* Include location-based features (ZIP-level insights)
* Use advanced models (LightGBM, CatBoost)
* Deploy model using Flask/Streamlit

---

## 👤 Author

Divyadharshini
M.Sc Data Science (Integrated)
4th Year Student
