
# IPL Match Winner Prediction

This project uses machine learning to predict the outcome of an IPL (Indian Premier League) match during the second innings based on real-time match data.

## 📂 Project Overview

The goal is to predict whether the batting team will win the match, given the current match situation (runs left, balls left, wickets remaining, etc.).

## 📊 Dataset

- **`matches.csv`**: Contains metadata about IPL matches (e.g., teams, winner, city).
- **`deliveries.csv`**: Ball-by-ball data for each match, including runs, wickets, overs, and players.

## 🧪 Features Used

- `batting_team`
- `bowling_team`
- `city`
- `runs_left`
- `balls_left`
- `wickets`
- `total_runs` (target score)
- `rrr` (required run rate)

## 🏗️ Model Pipeline

1. **Data Cleaning & Feature Engineering**
   - Calculates current score, runs left, balls left, required run rate.
   - Tracks wickets lost.
   - Labels result: 1 if batting team wins, else 0.

2. **Preprocessing**
   - Categorical features are one-hot encoded.
   - Numerical features are scaled.

3. **Model Training**
   - Logistic Regression is used to classify the match result.
   - Accuracy score is evaluated on the test set.

## 🛠️ Libraries Used

- `pandas`
- `numpy`
- `scikit-learn`

## ⚙️ How to Run

1. Place `matches.csv` and `deliveries.csv` in the same directory.
2. Run the Python script or Jupyter Notebook (`IPLL.ipynb`).
3. The final output will print the accuracy of the model.

## 📈 Output

The model provides the accuracy score based on a logistic regression classifier.

```
Model Accuracy Score: 0.82  # Example
```

## 🚀 Future Improvements

- Use more complex models like XGBoost or Random Forest.
- Add features like current run rate, batsmen stats, or bowler economy.
- Build a web app for real-time predictions.
