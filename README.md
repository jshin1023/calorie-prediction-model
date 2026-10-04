# Calorie Prediction Model

Predicts per-minute calorie expenditure from heart rate, steps, MET value, activity intensity, and body weight, using the public [Fitbit Fitness Tracker dataset](https://www.kaggle.com/datasets/arashnic/fitbit) on Kaggle.

**Approach:** merged minute-level calories, steps, intensity, and METs with heart rate (averaged from seconds to minutes) and each user's average weight; added time features (hour, day of week) and 5-minute rolling features (heart-rate mean, step sum); trained a random forest regressor (50 trees, max depth 10) on an 80/20 split.

**Results (test set):** MAE 0.1057 calories/minute, R² 0.979.

Python, pandas, NumPy, scikit-learn, matplotlib, seaborn.
