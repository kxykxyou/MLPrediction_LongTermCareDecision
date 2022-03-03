This prediction model is for the in-class contest(AI and data science training class held by ITRI).

### Brief data description
- Including 2 sets, train.csv and test.csv, dimensions are (2879 observations , 46 predictors, 1 label) and (300 observations, 46 predictors), respectively.
- No missing value
- All features are dummy variables
- Feature names are encoded instead of real feature names.

### Two approaches for feature selection
- Feature selection-1: train 30 random forest models(RF model) to validate feature importance. Then filter features with importance > 0.02.
- Feature selection-2: select 12 features with chi-square test

### Model training approach: xgboost
- Object: softprob
- Metric: logloss
- Tuning method: one-factor-at-a-time
- Parameter tuning order: n_estimators --> max_depth --> min_child_weight --> gamma --> regalpha --> eta

### Model evaluation:
- Training set logloss: 0.49
- Testing set logloss: 0.49 (rank: 7/20 participant; best score: 0.45; total classmates: 50)
