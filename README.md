# SP500PREDICTOR
#### Video Demo:  <https://www.youtube.com/watch?v=Yp9yRsxIJJQ&ab_channel=FilipSentypal>
#### Description:
Project Overview
As a Finance and Computer Science major in college, I am fascinated by both the markets and technology. This interest led me to combine these areas and build a project that attempts to forecast the daily movements of the S&P 500 index, a benchmark in financial markets. Leveraging Python and machine learning techniques, specifically a RandomForestClassifier, I analyzed historical data to predict whether the S&P 500 will close higher on the next trading day. The project is encapsulated in a Jupyter Notebook file, predictor.ipynb, containing the complete code, models, and commentary on the methodology and results.

Contents of predictor.ipynb
The predictor.ipynb file begins with installing and importing necessary Python packages like yfinance for stock data retrieval and sklearn for machine learning. The initial sections cover data fetching for the S&P 500 index, feature creation, and an initial model setup leading to the first precision score of 0.4788. The later sections detail the iterative process of feature enhancement, inclusion of additional stock data, model refinement, and evaluation to achieve improved precision scores. After the first round of refinement, I achieved a precision score of 0.5275. Although this was better than my initial score, it was still not greater than the percentage of days the stock market actually went up without using any model, which ends up being .5332. After a few more rounds of refinement and feature development, like adding additional financial information and merging tech stocks with the S&P 500 data, I was finally able to achieve a precision score of around 0.6, which is significantly higher than the score without a model. Each step, from data preprocessing to model evaluation, is clearly annotated with visualizations like line plots and concatenated tables.

Design Choices and Rationale
Stock Selection:
In expanding the feature set, I included data from key tech stocks: AAPL, MSFT, NVDA, GOOGL, and AMZN. I chose these stocks because of their significant weight in the S&P 500 and their substantial influence on the tech sector and overall market trends. Their performance often reflects broader market dynamics, making their inclusion crucial for a model aiming to predict the S&P 500's movements.

Feature Selection and Engineering:
Selecting and engineering the right features was a critical part of this project. The features include:

Basic stock attributes: 'Close', 'Volume', 'Open', 'High', 'Low'.
Technical indicators: Moving Averages (e.g., MA_5, MA_30), Relative Strength Index (RSI).
Custom metrics: Day Percent Change, Price Ratios, Trend data over various horizons.
I chose these features because they were effective at increasing the model's precision score, reflecting their ability to capture market trends. Moving Averages and RSI are standard tools in market analysis, offering insights into momentum and potential price reversals. Price Ratios and Day Percent Change provide a relative perspective on price movements, essential for understanding market dynamics. In general I spent some time trying differnt features and stock groupings to see which combination led to the highest precision score and I landed on this set of features and additional stocks. As explained above, all these features improved my model's precision score and confidence in its predictions.

Model Training and Evaluation
I trained the RandomForestClassifier with different sets of features, and its performance was evaluated using precision scores at each stage. This score was crucial as it indicates the model's ability to correctly predict days when the S&P 500 would rise, which is vital for decision-making in trading and investment strategies. Through iterative testing and feature refinement, the model's precision improved, demonstrating the effectiveness of the selected features and the robustness of the RandomForestClassifier.

Conclusion and Future Work
This project stands as a comprehensive endeavor to apply machine learning to financial market predictions. It demonstrates how data-driven methods can provide insights into complex domains like stock market movements. While the current focus is on the S&P 500 and selected tech stocks, I plan to expand to other indexes and eventually a wide spectrum of sectors with more advanced technologies to enhance my predictions.
