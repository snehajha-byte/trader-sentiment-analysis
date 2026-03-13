**Trader Sentiment Analysis**



This project analyzes how market sentiment (Fear \& Greed Index) affects trader behavior and profitability using historical trading data.

The goal is to understand whether traders perform differently during Fear vs Greed markets and to identify behavioral patterns that could inform trading strategies.



**Project Structure**

trader-sentiment-analysis

│

├── analysis.ipynb

├── fear\_greed\_index.csv

├── historical\_data.csv

├── README.md

├── requirements.txt

│

└── charts

&#x20;    ├── pnl\_by\_sentiment.png

&#x20;    ├── winrate\_by\_sentiment.png

&#x20;    ├── trades\_per\_day.png

&#x20;    ├── long\_short\_ratio.png

&#x20;    └── leverage\_distribution.png

**Dataset**

Two datasets were used in this analysis.

1\. Fear \& Greed Index

Contains daily market sentiment values indicating whether the market is driven by fear or greed.

Key columns:

date

value

classification

2\. Historical Trading Data

Contains detailed records of trader transactions.

Key columns:

Account

Side

Closed PnL

Size USD

Timestamp

Methodology



The analysis followed these steps:



1\. ***Data Cleaning***



Loaded both datasets using Pandas

Converted timestamps to daily date format

Checked for missing values and duplicates



2\. **Data Integration**

Merged trading data with the Fear \& Greed Index by date



3\. **Feature Engineering**



Created new metrics such as:

Daily PnL

Win rate

Leverage

Trade frequency

Long vs short ratio



4\. **Exploratory Data Analysis**

Analyzed trader performance and behavior across different market sentiments.



5\. **Behavioral Segmentation**



Traders were grouped based on:

Trade frequency

Leverage usage

Profit consistency



**Key Insights**

1\. Higher Profitability During Greed Markets

Traders show higher average PnL and win rate when market sentiment indicates greed.



2\. Increased Trading Activity During Fear Markets

Fear periods show significantly higher trade frequency, suggesting traders react more actively to volatile markets.



3\. High-Leverage Traders Experience Greater Risk

Traders using higher leverage show larger PnL swings, indicating higher risk exposure.



**Strategy Recommendations**



Based on the analysis, two strategy rules are suggested:



1\. Sentiment-Based Leverage Adjustment

Reduce leverage during Fear markets to control risk and allow moderate leverage during Greed markets.



2\. Segment-Based Trading Strategy

Frequent traders may benefit from exploiting volatility during Fear markets, while less frequent traders may perform better during Greed markets with clearer trends.



**How to Run the Project**

1\. Clone the repository

git clone https://github.com/snehajha-byte/trader-sentiment-analysis

2\. Install dependencies

pip install -r requirements.txt

3\. Run the notebook

jupyter notebook analysis.ipynb

Tools Used



Python

Pandas

NumPy

Matplotlib

Scikit-learn

Jupyter Notebook



**Future Improvements**



Build a predictive model for trader profitability



Perform advanced clustering for trader archetypes



Create an interactive Streamlit dashboard





