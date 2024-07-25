# Files:
- data.parquet/data.csv (.parquet format is good for efficient loading and saving)
    - The main dataset containing stock price, trade volume, news events and news sentiment for S&P 500 companies during the period Oct 2020-Jul 2022
    - 217811 samples in total
    - Total 26 features per sample
    - Prediction Task:
        - Focus on prediction the following 4 features: "Open" (opening price on the day), "Close" (closing price of the day), "High" (highest price on that day), "Low" (lowest price on that day). If you predicting for day X, then you cannot use any of these 4 feature values of day X as model input
        - If you are predicting for day X, then you should also use some attributes of previous N (experiment with different values of N) days (remember that this is a time series task -> prediction of today is also affected by the occurrences of the near past). These attributes may include "Open", "Close", "High" and "Low" features as well.
- sp500wiki.parquet/sp500wiki.csv
    - List of S&P 500 companies as of July 2022 and various metadata in tabular format
    - Contains information for over 500 companies (524 rows in total)
    - 10 attributes per company (10 columns)
    - You can use these attributes as assisting feature when performing prediction task on a particular day for a particular company

# Additional Information:
- "Symbol" which denotes the company brand, is the common feature between the two datasets
- Missing values are there in the dataset
- Categorical, discrete and continuous attributes exist in the dataset
- The prediction tasks are regression tasks
- Make sure that train and test data have minimum information leakage (this is something you need to think about deeply)  