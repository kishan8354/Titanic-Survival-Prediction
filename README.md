# Titanic Survival Prediction

A machine learning solution for the Kaggle Titanic competition using Logistic Regression and Random Forest classifiers.

## Competition

Kaggle Competition: Titanic - Machine Learning from Disaster

Notebook Link: https://www.kaggle.com/code/kishankushavaha/titanic-survival-prediction

## Problem Statement

The objective of this competition is to predict whether a passenger survived the Titanic disaster based on information such as passenger class, gender, age, and fare.

## Dataset

The dataset contains passenger information including:

* PassengerId
* Pclass
* Name
* Sex
* Age
* SibSp
* Parch
* Ticket
* Fare
* Cabin
* Embarked
* Survived (Target Variable)

## Data Preprocessing

The following preprocessing steps were performed:

* Missing values in **Age** were filled using the mean value.
* Missing values in **Fare** were filled using the mean value.
* Missing values in **Cabin** were filled using the most frequent value.
* Categorical features (**Sex** and **Embarked**) were converted into numerical values using Label Encoding.
* Cabin was removed before model training.

## Features Used

The following features were selected for model training:

```text
Pclass
Sex
Age
Fare
```

Target Variable:

```text
Survived
```

## Models Used

### Logistic Regression

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
model.fit(X_train, y_train)
```

### Random Forest Classifier

```python
from sklearn.ensemble import RandomForestClassifier

rf = RandomForestClassifier()
rf.fit(X_train, y_train)
```

## Workflow

1. Load Training Dataset
2. Handle Missing Values
3. Encode Categorical Variables
4. Select Features
5. Split Data into Training and Testing Sets
6. Train Machine Learning Models
7. Evaluate Performance
8. Generate Predictions on Test Dataset
9. Create Kaggle Submission File

## Submission Format

Predictions were generated on the competition test dataset and saved as:

```text
submission.csv
```

Example:

```text
PassengerId,Survived
892,0
893,1
894,0
...
```

## Libraries Used

* NumPy
* Pandas
* Matplotlib
* Scikit-learn

## Run the Notebook

1. Clone the repository

```bash
git clone <repository-url>
```

2. Install dependencies

```bash
pip install numpy pandas matplotlib scikit-learn
```

3. Open the notebook and run all cells.

## Kaggle Notebook

https://www.kaggle.com/code/kishankushavaha/titanic-survival-prediction

## Author

Kishan Kushavaha

M.Tech (Computer Science)
