# Machine Learning Training Bot

This application compares different machine learning algorithms and strategies. It compares a 3 month training window to shortening it to 1 month, then to 6 months for what is ideal.

---

## Technologies

Using Python 3.7

* [pandas](https://github.com/google/pandas) - For data analysis

* [Scikit-Learn](https://github.com/scikit-learn) - For data analysis using train_test_split, StandardScaler, and LogisticRegression.

---

## Installation Guide

```python
  pip install pandas
  pip install -U scikit-learn
```

---

## Usage

![BaselinePrediction](images/Baseline_Prediction.png)

The baseline prediction shows that the strategy did still outperform the actual returns without any strategy.

![1moPrediction](images/1mo_Prediction.png)

The 1mo Prediction didn't do as well as the baseline of using 3 months of data to train the model. The Baseline prediction had a nearly 50% return, vs the 1mo which had below a 40% return. Thus, the model performance decreased with decreased training data.

![2by20prediction](images/2_by_20_rolling_windows_training_prediction.png)

By shortening the windows for the trading signals to 2 periods for the fast SMA and 20 periods for the slow SMA. The returns were increased to over 60%!

![LogisticRegression](images/Logistic_Regression_Plot.png)

This model started off performing significantly better than the returns without a strategy; however, halfway thru 2020 it started significantly underperforming the actual returns. So much so, that the returns by the end of the testing period were slightly below that without any strategy.


 All in all, I recommend a longer training data set, with shorter windows in order to create more data and outcomes to fit the models. As the more instances/trade signals there were, the better the model performed. Moreover, the SVM/SVC model performed better over a greater set of financial conditions. Considering it even out performed during Covid, vs the less testing data underperforming significantly.


---

## Contributors

Sole Contributor - Josh Thompkins

---

## License

Everyone is free to view and work with this project, you may not alter text unless given explicit permission.
