# Student Performance Prediction & Analysis

An end-to-end **Data Science and Machine Learning project** focused on analyzing factors associated with student exam performance and building predictive models to estimate exam scores.

This project was completed as the **Final Data Science Project** of my internship at **Codomax Digital Solutions**.

---

## 📌 Project Overview

Student performance can be influenced by several academic, behavioral, and environmental factors such as study time, attendance, previous academic performance, sleep, tutoring, motivation, parental involvement, and access to resources.

The objective of this project is to:

* Explore patterns in student performance
* Identify factors associated with exam scores
* Perform data cleaning and exploratory analysis
* Prepare numerical and categorical features for Machine Learning
* Build multiple regression models
* Compare model performance using standard evaluation metrics
* Identify the most influential features
* Use the final models to predict exam scores for new student profiles

The project follows a complete Data Science workflow:

**Data → Cleaning → EDA → Feature Engineering → Preprocessing → Machine Learning → Evaluation → Insights**

---

## 🎯 Problem Statement

Given information about a student's academic habits, background, and learning environment, can we use Machine Learning to predict their expected exam score?

### Key Questions

1. Which factors are most strongly associated with student exam performance?
2. How do study hours and attendance relate to exam scores?
3. Does previous academic performance help predict future exam performance?
4. Which Machine Learning model performs best on unseen data?
5. Which features contribute most to the model's predictions?

---

## 📊 Dataset

The project uses a **synthetic student-performance dataset** containing **6,607 student records and 15 variables**.

The dataset was generated specifically for this portfolio project to simulate realistic relationships between student characteristics and exam performance.

### Features

| Feature                    | Description                               |
| -------------------------- | ----------------------------------------- |
| `Hours Studied`            | Number of hours spent studying            |
| `Attendance`               | Student attendance percentage             |
| `Previous Scores`          | Previous academic score                   |
| `Sleep Hours`              | Average hours of sleep                    |
| `Tutoring Sessions`        | Number of tutoring sessions               |
| `Physical Activity`        | Physical activity level                   |
| `Parental Involvement`     | Level of parental involvement             |
| `Access to Resources`      | Student's access to educational resources |
| `Motivation Level`         | Student motivation level                  |
| `Internet Access`          | Whether the student has internet access   |
| `School Type`              | Type of school                            |
| `Parental Education Level` | Highest parental education level          |
| `Distance from Home`       | Distance between home and school          |
| `Gender`                   | Student gender                            |
| `Exam Score`               | Final exam score — **target variable**    |

### Dataset Structure

```text
Rows:       6,607
Columns:       15
Target:   Exam Score
```

The CSV file is located in:

```text
data/Student_Performance_Factors.csv
```

---

## 🔎 Exploratory Data Analysis

The project performs several EDA techniques to understand the dataset and identify relationships between variables.

### Analysis includes:

* Dataset structure and data types
* Missing-value analysis
* Duplicate-value checks
* Numerical feature distributions
* Categorical feature distributions
* Study hours vs. exam score
* Attendance vs. exam score
* Previous scores vs. exam score
* Exam-score distribution
* Correlation analysis
* Outlier visualization

### Visualizations

The notebook uses:

* Histograms
* Scatter plots
* Box plots
* Count plots
* Correlation heatmap

These visualizations help identify patterns before applying Machine Learning.

---

## 🧹 Data Preprocessing

Before training the models, the dataset goes through a preprocessing pipeline.

### Steps performed

1. Checked data types
2. Identified missing values
3. Checked duplicate records
4. Handled missing numerical values
5. Handled missing categorical values
6. Separated features and target
7. Identified numerical and categorical columns
8. Applied numerical preprocessing
9. Applied categorical encoding
10. Created a reusable Scikit-learn preprocessing pipeline

Categorical variables are converted into numerical representations using **One-Hot Encoding**.

---

## 🤖 Machine Learning Models

Three regression algorithms were implemented:

### 1. Linear Regression

Used as a baseline model to understand the linear relationship between the input variables and exam score.

### 2. Decision Tree Regressor

A tree-based model capable of capturing non-linear relationships between features and exam performance.

### 3. Random Forest Regressor

An ensemble learning method that combines multiple decision trees to improve predictive performance and robustness.

---

## 📏 Model Evaluation

The models are evaluated on unseen test data using:

### Mean Absolute Error — MAE

Measures the average absolute difference between actual and predicted exam scores.

**Lower MAE = better performance**

### Root Mean Squared Error — RMSE

Measures prediction error while giving greater weight to larger errors.

**Lower RMSE = better performance**

### R² Score

Measures how much of the variation in exam scores is explained by the model.

**Higher R² = better performance**

The notebook creates a model-comparison table to make it easier to identify the strongest-performing model.

---

## 📈 Model Comparison

The project compares:

| Model             |                    MAE |                   RMSE |                     R² |
| ----------------- | ---------------------: | ---------------------: | ---------------------: |
| Linear Regression | Calculated in notebook | Calculated in notebook | Calculated in notebook |
| Decision Tree     | Calculated in notebook | Calculated in notebook | Calculated in notebook |
| Random Forest     | Calculated in notebook | Calculated in notebook | Calculated in notebook |

The exact scores are generated when the notebook is executed and depend on the train-test split and model configuration.

---

## 🔬 Feature Importance

Feature importance is analyzed using the tree-based model to understand which variables contribute most strongly to predictions.

This helps move beyond simply asking:

> "How accurately can we predict exam scores?"

and instead investigate:

> "Which characteristics are most useful for making those predictions?"

---

## 🧪 Example Prediction

The notebook also demonstrates how the trained Machine Learning pipeline can be used to predict the exam score of a new student based on their characteristics.

This demonstrates how the project could be extended into a practical prediction system.

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-learn

### Development Environment

* Google Colab
* Jupyter Notebook

### Version Control

* Git
* GitHub

---

## 📂 Project Structure

```text
student-performance-ml/
│
├── Student_Performance_Final_Data_Science_Project.ipynb
│
├── data/
│   └── Student_Performance_Factors.csv
│
├── README.md
│
└── requirements.txt
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

### 2. Navigate to the project directory

```bash
cd student-performance-ml
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

You can open:

```text
Student_Performance_Final_Data_Science_Project.ipynb
```

using Jupyter Notebook, JupyterLab, or Google Colab.

### 5. Run all cells

The notebook loads the dataset from:

```text
data/Student_Performance_Factors.csv
```

and performs the complete analysis and Machine Learning workflow.

---

## 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

* Structuring an end-to-end Data Science project
* Cleaning and preparing datasets
* Performing exploratory data analysis
* Selecting and transforming features
* Working with categorical variables
* Building Machine Learning pipelines
* Training regression models
* Evaluating models using MAE, RMSE and R²
* Comparing different Machine Learning algorithms
* Interpreting feature importance
* Making predictions on new data
* Presenting a Data Science project in a portfolio-ready format

---

## ⚠️ Limitations

This project is intended as an educational and portfolio project.

The dataset is **synthetic**, meaning it does not represent real students or real-world educational records.

Therefore, the model's predictions should not be interpreted as evidence of actual causal relationships between student characteristics and academic performance.

Additional real-world data would be required before using such a system for actual educational decision-making.

---

## 🔮 Future Improvements

Possible future extensions include:

* Testing additional regression algorithms
* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
* Cross-validation
* More extensive feature engineering
* Explainable AI techniques such as SHAP
* Interactive dashboards using Power BI or Tableau
* Deploying the model using Streamlit or Flask
* Testing the model on a real-world student-performance dataset
* Adding experiment tracking and model versioning

---

## 👩‍💻 Author

**Raksha S**

Aspiring Data Scientist

Interested in:

**Data Science • Machine Learning • Artificial Intelligence • Data Analytics**

---

## ⭐ Project

If you find this project useful, feel free to explore the notebook and the analysis.


**Google Colab:**
`<YOUR_GOOGLE_COLAB_URL>`
