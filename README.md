# Titanic Survival Prediction (80.4% Accuracy)

This project uses a Logistic Regression model to predict the survival of passengers on the Titanic. The implementation focuses on building a clean, automated machine learning pipeline.

## 🚀 Performance
- **Accuracy**: 80.45%
- **Balanced F1-Score**: ~0.80

## 🛠️ Machine Learning Pipeline
I used a `ColumnTransformer` to handle different data types automatically:

### Numerical Features (Age, Fare, SibSp, Parch)
- **Imputation**: Filled missing values using the `median`.
- **Scaling**: Applied `StandardScaler` to normalize units.

### Categorical Features (Sex, Embarked, Pclass, Deck, etc.)
- **Imputation**: Filled missing values using `most_frequent` (mode).
- **Encoding**: Used `OneHotEncoder(drop='first')` to transform text into 17 numerical features.

## 📊 Evaluation
The model shows strong balance between Precision and Recall:
- **Precision (Survived)**: 0.77
- **Recall (Survived)**: 0.74

## 📁 Files
- `titanic_model.ipynb`: Full training and analysis notebook.
- `titanic_model_pipeline.pkl`: The saved joblib model for reuse.
