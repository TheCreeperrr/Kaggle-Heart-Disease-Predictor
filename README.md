# Kaggle Playground Series - S6E2: Predicting Heart Disease

This is my first attempt at participating in a Kaggle contest and building a prediction model.  
- Final Roc Auc Score: 0.95518  
- Final Leaderboard Rank: 823/4371  

## Information about the Contest

The following link contains all details of the contest, the scoring metrics and the datasets for training and testing.  
[Link to the Kaggle Contest](https://www.kaggle.com/competitions/playground-series-s6e2/overview)

## My Approach

### 1. Feature Engineering

- Apply one-hot-encoding on features containing nominal data
- Add extra features: Hypertension (BP>=120) And Old Age (Age>55)
- Tested additional features that ultimately did not show any improvement in the models.

### 2. Hyperparameter Tuning

- Optuna was used to tune the parameters of the models, which I then stored into dictionaries.

### 3. Training the model

- Used XGBoost, LightGBM and CatBoost models.
- Trained each model on the complete dataset and used 5-fold cross-validation to generate out-of-fold (OOF) predictions.
- A logistic regression meta-model was trained on OOF predictions for the final predictions.

