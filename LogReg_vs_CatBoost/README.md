This is solution for this [Kaggle competition](https://www.kaggle.com/c/advanced-dls-spring-2021/overview) 
![](assets/exmpls.gif)

# Description
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](http://colab.research.google.com/github/Viktor-Sok/Classic_ML_Algorithms/blob/main/LogReg_vs_CatBoost/notebooks/Churn_Prediction_Kaggle.ipynb)

1. Thorough EDA is conducted
2. Made an attempt at some feature engineering
3. When we hot-encode categoorical variables for logistic regression it's important to drop one hot-encoded column to avoid multicollinearity. For CatBoost we want to keep that column, so it will take part in the splits of decision trees.
4. Feature Standartization/Scaling procedure and classifier are combined into sklearn pipeline, this way during GridSearchCV we avoid data leak from valid set as scaling will not be apllied to valid set on each cross-validation iteration.

Accuracy metric results: <br>
LogReg: 0.8518 <br>
CatBoost: 0.8524 <br>

