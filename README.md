# AI & ML Internship Task 4

## Title
Feature Encoding & Scaling

---

## Objective

The objective of this task is to convert categorical features into numerical formats and scale numerical features to a common range for better machine learning model performance.

This task focuses on:
- Identifying categorical and numerical features
- Applying Label Encoding
- Applying One-Hot Encoding
- Understanding and avoiding the Dummy Variable Trap
- Applying Standardization and Normalization
- Comparing feature distributions before and after scaling

---

## Tools & Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Google Colab
- GitHub

---

## Dataset Used

### Adult Census Income Dataset

The dataset contains demographic and employment-related information used to predict whether a person's annual income exceeds $50,000.

### Features Included

- Age
- Workclass
- Education
- Education Number
- Marital Status
- Occupation
- Relationship
- Race
- Sex
- Capital Gain
- Capital Loss
- Hours Per Week
- Native Country
- Income

Dataset File:

```text
adult.csv
```

---

## Libraries Used

### Pandas
Used for:
- Loading datasets
- Data preprocessing
- Feature manipulation

### NumPy
Used for numerical operations.

### LabelEncoder
Used to convert binary categorical values into numerical format.

### StandardScaler
Used for Standardization.

### MinMaxScaler
Used for Normalization.

### Matplotlib & Seaborn
Used for visualizing feature distributions before and after scaling.

---

## Tasks Performed

### 1. Loaded Dataset

Loaded the Adult Census Income dataset using Pandas.

```python
df = pd.read_csv('adult.csv')
```

---

### 2. Explored Dataset

Used:

```python
df.head()
df.info()
df.shape
```

to understand:
- Dataset structure
- Data types
- Number of records
- Feature information

---

### 3. Identified Categorical Features

Used:

```python
df.select_dtypes(include=['object'])
```

to identify text-based features requiring encoding.

Examples:
- workclass
- education
- occupation
- sex
- native.country
- income

---

### 4. Applied Label Encoding

Applied Label Encoding on the target column:

```python
income
```

Example:

Before:

```text
<=50K
>50K
```

After:

```text
0
1
```

---

### 5. Applied One-Hot Encoding

Applied One-Hot Encoding on nominal categorical columns using:

```python
pd.get_dummies()
```

Example:

Before:

```text
Male
Female
```

After:

```text
sex_Male
```

---

### 6. Avoided Dummy Variable Trap

Used:

```python
drop_first=True
```

to remove redundant columns and prevent multicollinearity.

---

### 7. Applied Standardization

Used:

```python
StandardScaler()
```

to transform numerical features.

Formula:

z = (x - mean) / standard deviation

Benefits:
- Mean becomes 0
- Standard deviation becomes 1
- Useful for KNN, SVM, Logistic Regression

---

### 8. Applied Normalization

Used:

```python
MinMaxScaler()
```

Formula:

x' = (x - xmin) / (xmax - xmin)

Benefits:
- Values scaled between 0 and 1
- Useful for Neural Networks and Distance-Based Algorithms

---

### 9. Compared Data Before and After Scaling

Visualized distributions using Histograms.

Compared:
- Original Features
- Standardized Features

to understand scaling impact.

---

### 10. Saved Processed Dataset

Generated processed dataset:

```text
adult_encoded_scaled.csv
```

for future machine learning tasks.

---

## Concepts Learned

### Label Encoding
Converts categorical labels into numerical values.

### One-Hot Encoding
Creates separate binary columns for categories.

### Dummy Variable Trap
Occurs when encoded features become highly correlated.

### Standardization
Transforms data to mean 0 and standard deviation 1.

### Normalization
Scales values to a fixed range (0–1).

### Feature Scaling
Ensures all numerical features contribute equally during model training.

---

## Key Observations

1. The dataset contains both categorical and numerical features.

2. Income was successfully encoded using Label Encoding.

3. Nominal categorical variables were transformed using One-Hot Encoding.

4. Dummy Variable Trap was avoided using `drop_first=True`.

5. Standardization centered numerical features around zero.

6. Normalization scaled numerical features between 0 and 1.

7. Feature scaling improved data consistency for machine learning algorithms.

---

## Outcome

Successfully performed Feature Encoding and Feature Scaling on the Adult Census Income Dataset.

The dataset is now machine-learning ready and can be used for classification algorithms such as:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Decision Trees
- Random Forest

---

## Files Included

```text
Feature_Encoding_and_Scaling.ipynb
adult.csv
adult_encoded_scaled.csv
README.md
```

---

## Repository Name

```text
AI-ML-Internship-Task-4
```

---

## Author

**Arya Chighare**
Artificial Intelligence & Data Science
YCCE, Nagpur
