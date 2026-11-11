# Dissertation: forecasting weekly mask counts (SARIMAX vs LSTM)

Code for a data-analytics approach to anticipating personal protective equipment (PPE) needs, using weekly data (ICU staffed beds and mask counts, 2024 collection weeks).

## What is here
- `SARIMAX NOW.ipynb`: SARIMAX time-series model with week-of-year seasonality.
- `lstm latest.ipynb`: LSTM neural network (Keras) on the same data.

## Results (hold-out evaluation in the notebooks)
| Model | RMSE | MAPE |
|---|---|---|
| SARIMAX | 3,081 | 5.48% |
| LSTM | 4,054 | 7.52% |

On this dataset the classical SARIMAX model was more accurate than the LSTM, which is a common result for
small, strongly seasonal weekly series.

## Method notes
- Data prepared with pandas (dates parsed, week-of-year feature added).
- Models evaluated with RMSE and MAPE on a held-out period.

## Tools
Python, pandas, NumPy, statsmodels, scikit-learn, Keras, matplotlib.

