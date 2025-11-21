# Peer Review: Sabriya Sowers Project
[Notebook reviewed](https://github.com/ssowers2/ml_regression_sowers/blob/main/notebooks/final/regression_sowers.ipynb) 

## 1. Clarity & Organization (Is the notebook structured and easy to follow?)
Sabriya’s notebook is very well organized and easy to follow. She starts with looking at the data, explores patterns, does some feature engineering, then jumps into modeling. Headings and reflections look great, plots are labeled and relevant, making the data patterns easy to interpret.

*Improvement Suggestion:* It could be helpful to add brief comments in code cells explaining why certain steps are done. That would make it even easier for someone new to follow the reasoning.

## 2. Feature Selection & Justification (Do the chosen features make sense given the objectives?)
The features chosen were: `age`, `bmi`, and `smoker_num`. The features make a lot of sense. Age and bmi are pretty well known to be health indicators. The smoker status really jumps out in the visualizations because it showed the largest difference in medical costs. 

*Improvement Suggestion:* It might be nice to briefly mention why other features (sex, region, children) weren’t included. This could really help show the reader why the features chosen were best.

## 3. Model Performance & Comparisons (Are the results and comparisons clearly explained?)
The comparison between linear regression and polynomial regression (degree=3) is clear. Sabriya reported R², MAE, and RMSE, and she explains that the polynomial model does better because it captures nonlinear relationships. Her notes on scaling really helped me as a reader as I read through the modeling process.

| Model                 | R²     | MAE     | RMSE    |
| --------------------- | ------ | ------- | ------- |
| Linear Regression     | 0.7777 | 4260.56 | 5874.76 |
| Polynomial (Degree 3) | 0.8615 | 2838.44 | 4637.02 |

*Improvement Suggestion:* Adding some visualization here of predicted vs actual charges for both models would make the improvement easier to “see” visually.

## 4. Reflection Quality (Are insights well thought out?)
Her reflections are solid. She talks about challenges like skewed target values and encoding, and she gives good ideas for next steps. Overall her notebook shows that she understands regression workflows. Great job Sabriya! 