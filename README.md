# MachineLearning_Internship


![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?logo=matplotlib)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-F7931E?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab)

## 📌 About This Repository

This repository contains my work completed during an **8-week Machine Learning Internship**.

The internship was structured as a progressive journey through the complete machine learning workflow — starting with Python and data-handling fundamentals and gradually moving toward data preprocessing, exploratory data analysis, regression, classification, model evaluation, hyperparameter tuning, ensemble learning, clustering, dimensionality reduction, and a final capstone-oriented analysis.

The notebooks document my hands-on learning, experiments, visualizations, model evaluations, and key observations throughout the internship.

---

## 🎯 Internship Learning Path

```text
Python & Data Fundamentals
            ↓
      NumPy & Pandas
            ↓
 Exploratory Data Analysis
            ↓
 Data Preprocessing
            ↓
 Feature Engineering
            ↓
 Regression & Classification
            ↓
 Model Evaluation
            ↓
 Hyperparameter Tuning
            ↓
 Ensemble Learning
            ↓
 Clustering & PCA
            ↓
 Final Capstone Analysis
```

---

# 📚 Weekly Work

## Week 1 — Python for ML & Data Fundamentals

**Notebook:** [`Week1.ipynb`](./Week1.ipynb)

Focused on building the Python and data-analysis foundation required for machine learning.

### Topics Covered

* Dataset loading and inspection
* NumPy fundamentals
* Array creation and manipulation
* Mean, median, standard deviation, minimum and maximum
* Matrix operations
* Array slicing
* Boolean indexing
* Pandas DataFrames
* Data exploration
* Basic data visualization

### Libraries

* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

## Week 2 — Exploratory Data Analysis

**Notebook:** [`Week2.ipynb`](./Week2.ipynb)

Focused on understanding datasets before building machine learning models.

### Datasets

* Ames Housing Dataset
* Titanic Dataset

### Topics Covered

* Dataset inspection
* Missing-value analysis
* Univariate analysis
* Bivariate analysis
* Distribution analysis
* Correlation analysis
* Histograms
* Bar charts
* Correlation heatmaps
* Identifying important features

### Key Findings

Some of the important observations included:

* Several Ames Housing amenity-related columns contain substantial missing values because the corresponding feature may simply be absent.
* Titanic fare distribution is strongly right-skewed.
* `Sex` and `Pclass` show strong relationships with Titanic survival.
* `OverallQual` and `GrLivArea` are strongly associated with house sale price.
* Strong correlation between `GarageCars` and `GarageArea` highlights potential multicollinearity.

---

## Week 3 — Data Preprocessing & Feature Engineering

**Notebook:** [`Week3.ipynb`](./Week3.ipynb)

Focused on transforming raw data into a form suitable for machine learning algorithms.

### Topics Covered

* Handling missing values
* Understanding whether missing values represent absent features
* Median-based imputation
* Neighborhood-based imputation
* Categorical feature encoding
* Label Encoding
* Feature scaling
* StandardScaler
* MinMaxScaler
* Train-test splitting
* Stratified splitting
* Scikit-learn Pipelines

### Main Datasets

* Ames Housing
* Titanic

This week focused heavily on an important ML principle:

> Good machine learning starts with good data preparation.

---

## Week 4 — Regression & Classification

**Notebook:** [`Week4.ipynb`](./Week4.ipynb)

This week introduced predictive modeling using both regression and classification.

### Linear Regression — House Price Prediction

Used the following features:

* `GrLivArea`
* `OverallQual`
* `TotalBsmtSF`
* `GarageCars`
* `YearBuilt`

A logarithmic transformation was applied to the target variable to reduce skewness.

### Evaluation Metrics

* MSE
* RMSE
* MAE
* R²

### Result

**R² Score: 0.8673**

### Logistic Regression

A binary classification problem was created by dividing houses into:

* Above-median price
* Below-median price

Feature scaling was applied using `StandardScaler`.

### Result

**Test Accuracy: 92.47%**

The week also compared scaled and unscaled Logistic Regression models and examined confusion matrices and classification reports.

---

## Week 5 — Classification Algorithms

**Notebook:** [`Week5.ipynb`](./Week5.ipynb)

Focused on understanding and comparing multiple classification algorithms.

### Algorithms Covered

#### K-Nearest Neighbors (KNN)

* Understanding nearest-neighbor classification
* Testing different values of `K`
* Comparing training and testing performance

#### Decision Trees

* Decision tree classification
* Understanding feature-based splits
* Controlling tree depth
* Reducing overfitting

#### Support Vector Machines (SVM)

Explored different kernels:

* Linear
* RBF
* Polynomial

### Evaluation

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Classification reports

---

## Week 6 — Model Evaluation & Hyperparameter Tuning

**Notebook:** [`Week6.ipynb`](./Week6.ipynb)

Focused on going beyond simple accuracy and understanding how to properly evaluate machine learning models.

### Topics Covered

* Cross-validation
* 5-fold cross-validation
* 10-fold cross-validation
* Confusion matrix
* Precision
* Recall
* F1-score
* ROC curves
* AUC
* Logistic Regression
* Decision Trees
* GridSearchCV
* RandomizedSearchCV
* Learning curves
* Overfitting vs underfitting

### Selected Results

| Experiment             | Model               |  Score |
| ---------------------- | ------------------- | -----: |
| 5-Fold CV              | Logistic Regression | 89.79% |
| 10-Fold CV             | Logistic Regression | 89.79% |
| Classification Metrics | Logistic Regression | 97.37% |
| ROC-AUC                | Logistic Regression | 99.74% |
| ROC-AUC                | Decision Tree       | 93.55% |
| GridSearchCV           | Logistic Regression | 99.12% |
| RandomizedSearchCV     | Logistic Regression | 98.25% |

This week strengthened my understanding of why model evaluation should consider the problem context rather than relying on a single metric.

---

## Week 7 — Ensemble Learning

**Notebook:** [`Week7.ipynb`](./Week7.ipynb)

Focused on ensemble methods and improving predictive performance by combining multiple decision trees.

### Algorithms Covered

* Decision Tree
* Random Forest
* Gradient Boosting

### Model Comparison

| Model               | Mean 5-Fold CV Accuracy |
| ------------------- | ----------------------: |
| Decision Tree       |                  86.47% |
| Random Forest       |                  91.95% |
| Gradient Boosting   |                  90.75% |
| Tuned Random Forest |              **92.38%** |

### Random Forest Hyperparameter Tuning

The tuned Random Forest used:

```text
max_depth = 10
max_features = log2
n_estimators = 300
```

### Final Result

**Tuned Random Forest Test Accuracy: 95.21%**

The week also included feature-importance analysis to identify influential features used by the Random Forest model.

---

## Week 8 — Unsupervised Learning, PCA & Capstone Analysis

**Notebook:** [`Week8.ipynb`](./Week8.ipynb)

The final week introduced unsupervised learning and dimensionality reduction while bringing together concepts learned throughout the internship.

### K-Means Clustering

Used the Mall Customers dataset to explore customer segmentation using:

* Annual Income
* Spending Score

Topics included:

* Feature standardization
* K-Means clustering
* Cluster analysis
* Silhouette score
* Visualization of customer segments

### PCA — Principal Component Analysis

Used the Scikit-learn Digits dataset to understand dimensionality reduction.

Topics included:

* Feature scaling
* PCA
* Reducing high-dimensional data
* Explained variance
* 2D visualization
* Understanding information loss after dimensionality reduction

### Final Capstone Analysis

The final section focused on the Ames Housing dataset and exploratory analysis for a house-price prediction problem.

Important observations included relationships between:

* `OverallQual`
* `GrLivArea`
* `GarageCars`
* `GarageArea`
* `TotalBsmtSF`
* `1stFlrSF`

and `SalePrice`.

The internship concluded with a reflection on the complete machine learning workflow and the importance of preprocessing and exploratory analysis before model development.

---

# 🛠️ Technologies & Tools

### Programming

* Python

### Data Analysis

* NumPy
* Pandas

### Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-learn

### Development Environment

* Jupyter Notebook
* Google Colab

### Machine Learning Concepts

* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* Missing Value Handling
* Categorical Encoding
* Feature Scaling
* Train-Test Split
* Cross-Validation
* Regression
* Classification
* Model Evaluation
* Hyperparameter Tuning
* Ensemble Learning
* Clustering
* Dimensionality Reduction

---

# 📊 Datasets Used

The internship work involved several standard machine learning datasets:

* **Ames Housing Dataset** — house-price analysis and prediction
* **Titanic Dataset** — exploratory analysis and classification
* **Breast Cancer Wisconsin Dataset** — classification and evaluation metrics
* **Mall Customers Dataset** — customer segmentation using K-Means
* **Scikit-learn Digits Dataset** — dimensionality reduction using PCA
* **Iris Dataset** — introductory data exploration

---

# 📈 Key Outcomes

Throughout the internship, I gained practical experience with the complete machine learning workflow:

```text
Collect / Load Data
       ↓
Understand the Dataset
       ↓
Clean & Preprocess
       ↓
Explore & Visualize
       ↓
Engineer Features
       ↓
Split Data
       ↓
Train Models
       ↓
Evaluate Models
       ↓
Tune Hyperparameters
       ↓
Compare Models
       ↓
Interpret Results
```

### Highlights

* Built regression and classification models using Scikit-learn.
* Performed exploratory data analysis on multiple datasets.
* Implemented missing-value handling and categorical encoding.
* Applied StandardScaler and MinMaxScaler.
* Used cross-validation to obtain more reliable model estimates.
* Evaluated models using accuracy, precision, recall, F1-score, ROC-AUC, MAE, RMSE and R².
* Applied GridSearchCV and RandomizedSearchCV for hyperparameter tuning.
* Compared Decision Trees, KNN, SVM, Logistic Regression, Random Forest and Gradient Boosting.
* Implemented K-Means clustering.
* Applied PCA for dimensionality reduction.
* Practiced interpreting model results and identifying important features.

---

# 📁 Repository Structure

```text
MachineLearning_Internship/
│
├── Week1.ipynb
├── Week2.ipynb
├── Week3.ipynb
├── Week4.ipynb
├── Week5.ipynb
├── Week6.ipynb
├── Week7.ipynb
├── Week8.ipynb
│
└── README.md
```

---

# 🚀 How to Use This Repository

The notebooks were developed primarily in **Google Colab/Jupyter Notebook**.

1. Clone the repository:

```bash
git clone https://github.com/UzmaFatima07/MachineLearning_Internship.git
```

2. Open the repository:

```bash
cd MachineLearning_Internship
```

3. Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

4. Launch Jupyter Notebook:

```bash
jupyter notebook
```

5. Open any weekly notebook and run the cells sequentially.

> **Note:** Some notebooks use Google Colab and Google Drive paths for datasets. If running them locally, update the dataset paths accordingly.

---

# 📖 Learning Progression

This repository represents my progression from learning the basics of working with data to applying multiple machine learning techniques.

### From:

**Python → NumPy → Pandas → EDA**

### To:

**Preprocessing → Feature Engineering → Regression → Classification**

### And finally:

**Evaluation → Hyperparameter Tuning → Ensemble Learning → Clustering → PCA → Capstone Analysis**

---

# 🎓 Internship Takeaway

This internship helped me understand that machine learning is not only about selecting an algorithm.

A successful ML workflow requires:

* Understanding the data
* Cleaning the data correctly
* Exploring patterns
* Selecting meaningful features
* Choosing an appropriate model
* Evaluating it using the right metrics
* Tuning it carefully
* Interpreting the results

The experience strengthened my Python, data analysis and machine learning skills while giving me hands-on practice with the end-to-end ML workflow.

---

## 👩‍💻 Author

**Uzma Fatima**

Engineering Student | Aspiring Data Analyst / Machine Learning Practitioner

---

⭐ If you find this repository useful, feel free to explore the weekly notebooks and follow my learning journey.
