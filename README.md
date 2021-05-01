# tps-202104
EDA and modelling for the April 2021 kaggle tabular playground series

All work for this April playground series is in jupyter notebooks, the main approach being:
- some light data cleaning and feature engineering
- binary classification by a range of classifiers, most successful being `GradientBoostingClassifier`
- model parameters tuned by grid search, cross-validation

## Changelog
2021-04-30 end of competition, scored 0.806 ranking in top quartile
- was not improving on the submission from the 26th, so tried a binning approach to feature engineering
- with more time, would have applied `CatBoost` to this approach but settled for an ensemble of GBC's and `XGBoost` trained on continuous and binned features
- this resulted in a marginal increase in accuracy, ending up at top 24% on the private leaderboard

2021-04-28 adds SGDClassifier
- doesn't perform as well as previous attempt, but may be retained for an ensemble approach

2021-04-26 improved feature extraction, scored 0.804
- with parameter grid search, and added trial TPOT notebook

2021-04-23 improved EDA and formatting of notebook
- scored 0.786 with same preprocessing but with gradient boosting classifier

2021-04-06 first notebook-only submission scored 0.770
- basic EDA and modelling, filled null age and fare with training set median
- standard scaler on numeric columns, one hot encoded categorical columns, logistic regression estimator
