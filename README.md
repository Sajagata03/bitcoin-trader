# OBJECTIVE
To explore the relationship between trader performance and market sentiment, uncover hidden patterns, and deliver insights that can drive smarter trading strategies.

# DATASETS
Trader_data: execution price, size, direction, closed PnL, etc.
Sentiment_data: Daily Fear/Greed Index

# METHODS
- Preprocessing: merged datasets, feature engineering 
- Models: Logistic Regression & Random Forest
- Evaluation: accuracy, precision, recall, support

# INSIGHTS: 
This project analyzes the relationship between Bitcoin market sentiment and trader profitability. Results show that trades during "Greed" periods perform better, and buy trades are more effective under strong sentiment. Random Forest outperforms Logistic Regression, with direction and sentiment value being the most predictive features. These insights can help traders optimize strategies by aligning trade direction and size with market sentiment phases. 


A) Trades placed during periods of "Greed" sentiment (as per the Fear/Greed Index) showed a higher win rate than those placed during "Fear".
This indicates that market optimism can influence trader behavior and outcomes, likely due to more favorable conditions or collective bullish momentum.

B) Profitable trades tend to occur when the sentiment score is higher, reinforcing the idea that greedier markets offer better opportunities. This pattern can be used to time entries or filter trade opportunities.

C) The Random Forest model showed that the most influential features were:
- DIRECTION
- VALUE
- LOG SIZE
This suggests that what kind of trade is placed, and the sentiment context, are more important than raw trade size or fees.
(While Random Forest handled NaN values in fee_pct without error, Logistic Regression raised a ValueError, highlighting the importance of preprocessing. After filling missing fee_pct with zero, both models ran successfully — and found fee_pct to be non-informative for profitability prediction.)


D) MODELS: Applied two different models to get proper insights which are-
- RANDOM FOREST (had higher accuracy, recall, and F1 score, indicating better handling of non-linear interactions.)
- LOGISTIC REGRESSION (provided interpretability, useful in understanding general trends.)

E) CORRELATION :
- value (sentiment score) shows a positive correlation with profitability.
- Trade size (in log scale) and fee percentage have weaker correlations, but still relevant.

F) THE FEATURE:
Removing fee_pct from the model didn’t significantly impact performance. Suggests that while fees are important operationally, they do not strongly distinguish profitable from unprofitable trades in the dataset.







