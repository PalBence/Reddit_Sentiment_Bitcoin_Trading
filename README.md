# This is the GitHub Repository corresponding to the BSc Thesis "Trading Bitcoin with Reddit Sentiment: Strategic Capital Allocation using ML-Enhanced Technical Signals"

To showcase the methodology without having to re-run long blocks of code I have uploaded the processed data at every step to show what it looks like and how it is fed into the next preprocessing steps.

The workflow is the following:
1. post_extraction.ipynb (takes the 'reddit' folder as input and creates the 'submissions' folder)
2. post_filtering.ipynb (takes the 'submissions' folder as input and creates the 'filtered_dfs' folder as output)
3. comment_extraction.ipynb (takes the 'reddit' and the 'filtered_dfs' folder as inputs and outputs the 'comments' folder)
4. extracting_sentiment.ipynb (takes the 'filtered_dfs' and 'comments' folder as inputs and creates the 'posts_with_sentiment' and 'comments_with_sentiment' folders)
5. preparing_sentiment.ipynb (takes the 'posts_with_sentiment' and 'comments_with_sentiment' folders as inputs and outputs the 'daily_entry_df.csv' file)
6. base_strategy.ipnyb and macd_strategy.ipnyb (take the daily_entry_df.csv and BTC-USD.csv file as inputs and execute the strategies)

Remarks:
- The folders are not uploaded due to them being too large, but the final, pre-processed data that was used for the strategies is uploaded ('daily_entry_df.csv)
- The BTC-USD.csv file was collected using the yfinance package of Python, but that has become subscription-based since then, so I am using the csv file instead of the API call
- The 'windowed_data_track_1' folder was used for visualization in base_strategy.ipnyb in saves the relevant data from the windows
