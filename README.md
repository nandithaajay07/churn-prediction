
---

## 📊 Problem Statement

In the telecom industry, customer churn (i.e., customers leaving the service) can significantly impact revenue. The goal of this project is to **predict whether a customer will churn**, based on their usage patterns and service plans.

---

## 💡 Approach

### 1. Data Understanding & EDA
- Loaded and explored the dataset (`train.csv`)
- Visualized churn distribution
- Created bar plots and boxplots to analyze relationships between features and churn
- Identified imbalance in the target class (`churn`)

### 2. Data Preprocessing
- Converted categorical variables (`yes`/`no`) to numeric (0/1)
- Dropped irrelevant features like `state` and `area_code`
- Checked and handled missing values
- Performed **train-test split** (80/20)

### 3. Handling Imbalanced Data
- Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to generate synthetic samples for the minority class (`churn = 1`)

### 4. Model Training
- Trained and evaluated two models:
  - **Logistic Regression** (baseline model)
  - **Random Forest Classifier** (improved accuracy and recall)

### 5. Model Evaluation
- Evaluated using:
  - Accuracy
  - Confusion Matrix
  - Precision, Recall, F1-score (Classification Report)
- Observed significant performance improvement using Random Forest + SMOTE

---

## 📈 Results

| Model              | Accuracy | Precision (1) | Recall (1) | F1-Score (1) |
|-------------------|----------|---------------|------------|--------------|
| Logistic Regression (SMOTE) | ~73%     | ~0.32         | ~0.74      | ~0.45        |
| Random Forest (SMOTE)       | **Higher**    | **Better balance** | **Improved**  | **Stronger**    |

- The Random Forest model gave better results in handling class imbalance.
- Performance metrics suggest improved **recall** for churners, which is critical in business scenarios.

---

## 📦 Files Included

- `churn_prediction.py` – Contains entire workflow (EDA to evaluation)
- `train.csv` – Input data
- `random_forest_model.pkl` – Saved model (can be reused for deployment)

---

## 🧠 Key Concepts Demonstrated

- Exploratory Data Analysis (EDA)
- Data preprocessing and transformation
- Handling class imbalance using SMOTE
- Supervised learning with `sklearn`
- Evaluation with accuracy, confusion matrix, and classification report
- Model serialization using `joblib`/`pickle`

---

## ✅ Future Scope

- Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
- Feature engineering for improved performance
- Deploying the model using Flask / Streamlit
- Dockerizing and containerizing the application for production

---

## 👩‍💻 Author

**Nanditha Ajay**  
Engineering Student | AI/ML Enthusiast  
GitHub: [github.com/nandithaajay07](https://github.com/nandithaajay07)

---

> ⚡ If you found this project useful or learned something new, feel free to ⭐ star the repo and fork it!
