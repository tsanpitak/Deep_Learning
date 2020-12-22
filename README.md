# Deep_Learning
---
## Files
[lstm_stock_predictor_closing.ipynb](Code/lstm_stock_predictor_closing.ipynb)

[lstm_stock_predictor_fng.ipynb](Code/lstm_stock_predictor_fng.ipynb)

[btc_historic.csv](Code/btc_historic.csv)

[btc_sentiment.csv](Code/btc_sentiment.csv)

---
## LSTM_Stock_Predictor - Closing
This model using RNN with 30 estimator units in each layer with 20% dropout rate. Using closing price as feature to train the model. 

Resulting in 0.0616 loss.

The predictions don't look great. However, it's still directionally correct. This model would track price better than FNG model over time.

| Window Size | Losses |
| :--- | :---: |
| 1 | 0.0267 |
| 2 | 0.0323 |
| 3 | 0.0392 |
| 4 | 0.0448 |
| 5 | 0.0490 |
| 6 | 0.0547 |
| 7 | 0.0584 |
| 8 | 0.0573 |
| 9 | 0.0607 |
| 10 | 0.0616 |

## LSTM_Stock_Predictor - FNG
This model using RNN with 30 estimator units in each layer with 20% dropout rate. Using FNG index value as feature to train the model. 

Resulting in 0.1219 loss. 

The predictions are terrible. However, it seems to suggest cycles if FNG, which possibly can be use with additional information to improve other models.

| Window Size | Losses |
| :--- | :---: |
| 1 | 0.1117 |
| 2 | 0.1138 |
| 3 | 0.1138 |
| 4 | 0.1200 |
| 5 | 0.1211 |
| 6 | 0.1165 |
| 7 | 0.1230 |
| 8 | 0.1332 |
| 9 | 0.1434 |
| 10 | 0.1219 |