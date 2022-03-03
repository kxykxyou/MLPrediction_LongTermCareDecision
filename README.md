This prediction model is for the in-class contest(AI and data science training class held by ITRI).

### brief data description
- Including 2 sets, train.csv and test.csv, dimension (2879 observations , 46 predictors, 1 label) and (300 observations, 46 predictors)
- No missing value
- All features are dummy variables; feature names are encoded instead of real feature names.

### two approaches for feature selection
- Feature selection-1: train 30 random forest models(RF model) to validate feature importance. Then filter features with importance > 0.02.
- Feature selection-2: select 12 features with chi-square test

### model training approach: xgboost
- object: softprob
- metric: logloss
- tuning method: one-factor-at-a-time
- parameter tuning order: n_estimators --> max_depth --> min_child_weight --> gamma --> regalpha --> eta

### model evaluation:
- training set logloss: 0.49
- testing set logloss: 0.49 (rank: 7/20 participant; best score: 0.45; total classmates: 50)
