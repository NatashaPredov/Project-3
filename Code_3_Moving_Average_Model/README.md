# Project 3 - Predict Weekly Trends of Royal Bank (RY.TO)
# Moving Average Model
![RBC Banner Image](../Images/00_RBC_Banner.png)
  
## Project Overview  
---
Objective: To enhance returns savings accounts through an active trading process that can be executed in all types accounts.    
Approach:  By predicting the weekly trend of Royal Bank (RY.TO)  
  
## Moving Average Modeling Process  
![EMATREND_BNS… (3) - JupyterLab - Google Chrome 2_8_2023 11_53_21 AM](https://user-images.githubusercontent.com/110307714/218336164-2300cb9a-2bc5-4ba1-9917-c0e7a584c1cd.png)

### The purpose of this code is to calculate the average change for the UpsideBreakout (ema8 > ema20) and DownsideBreakout (ema20 > ema8) over the lookahead period in stock data.
- A copy of the input stock data is created using the "dfCopy = stock_data.copy()" line.
- The index of the copy of the data is reset using "dfCopy = dfCopy.reset_index()" line.
- The lookahead period is defined as 'lookahead = 30' and the variables 'UpsideBreakout' and 'DownsideBreakout' are set to False. The variable 'CloseAtCrossover' is     set to 'NaN'. 
- Two dictionaries, 'dctUpsideBreakout' and 'dctDownsideBreakout' are also created to store the change in the close price.
- The dfCopy dataframe is then iterated over using for index, row in 'dfCopy.iterrows():' to identify the occurrences of the 'UpsideBreakout' and 'DownsideBreakout'     events.
- If an 'UpsideBreakout' event is identified, the average change for the next lookahead days is calculated and stored in the 'dctUpsideBreakout' dictionary.
- If a 'DownsideBreakout' event is identified, the average change for the next lookahead days is calculated and stored in the 'dctDownsideBreakout' dictionary.
- The code will output the average change for the 'UpsideBreakout' and 'DownsideBreakout' events over the lookahead period, stored in the dictionaries 'dctUpsideBreakout' and 'dctDownsideBreakout'. The close price after 16 days from the crossover event is also stored in the 'Close16' column of the 'dfCopy' dataframe.
![Project-3_EMA_TREND_BMO ipynb at main · NatashaPredov_Project-3 - Google Chrome 2_12_2023 3_51_59 PM](https://user-images.githubusercontent.com/110307714/218336539-fa8867f3-ee06-4a52-8151-98efb1524126.png)
### Trend Length
- A new column, trend_length, is created to store the length of the trend, and a new column, trend, is created to store the direction of the trend.

- The following variables are initialized to track the crossovers:

- prev_ema8 to store the previous period's EMA8
- prev_ema20 to store the previous period's EMA20
- The dataframe is looped through using df.iterrows() to find the crossovers and track the trend length and direction. The following logic is used:

- If the previous period's EMA8 is less than the previous period's EMA20 and the current period's EMA8 is greater than the current period's EMA20,a crossover from       below to above the EMA20 has occurred, and the trend is set to 'up'.
  The current period's trend_length is set to 1 and the trend is set to 'up'.
  If the previous period's EMA8 is greater than the previous period's EMA20 and the current period's EMA8 is less than the current period's EMA20, a crossover from     above to below the EMA20 has occurred, and the trend is set to 'down'. 
  The current period's trend_length is set to 1 and the trend is set to 'down'.
  If the trend is not None, the current period's trend_length is set to the previous period's trend_length plus 1 and the trend is set to the previous period's trend.
  The final dataframe is displayed using the display function and the tail function to show the last 10 rows of the data.
  With this code, you can track the trend length and direction based on the crossover of the EMA8 and EMA20 indicators.
  
![Project-3_EMA_TREND_BMO ipynb at main · NatashaPredov_Project-3 - Google Chrome 2_12_2023 3_53_53 PM](https://user-images.githubusercontent.com/110307714/218336647-ccf230ae-15d1-46ed-a011-615e512302c5.png)

![Project-3_EMA_TREND_BMO ipynb at main · NatashaPredov_Project-3 - Google Chrome 2_12_2023 3_59_59 PM](https://user-images.githubusercontent.com/110307714/218336916-1acfdd28-f9b6-4afe-91df-479f65481afe.png)
### Average Duration of Trend
- The average duration of the trend is calculated by looping through the dataframe and keeping track of the length of each trend. The following logic is used:
- A list, trend_lengths, is created to store the length of each trend.
- A variable, current_trend_length, is initialized to keep track of the length of the current trend.
- The dataframe is looped through using df.iterrows().
- If the current row has a trend (row['trend'] is not None), the current_trend_length is incremented.
- If the current row is not the last row in the dataframe (i < df.shape[0] - 1) and the trend direction in the next row is different from the current row (df.iloc[i+1]['trend'] != row['trend']), the current_trend_length is added to the trend_lengths list and the current_trend_length is reset to 0.
- After looping through the dataframe, if the trend_lengths list has any elements, the average duration of the trend is calculated as the sum of the trend lengths divided by the number of trends.
- If no trends are found in the data (the trend_lengths list is empty), a message is printed to indicate this.

![Project-3_EMA_TREND_BMO ipynb at main](https://user-images.githubusercontent.com/110307714/218336984-561b66f0-cd74-4cf4-bade-2345dfd541d7.png)

### Trend Accuracy

In this section, the accuracy of the trend is calculated based on the comparison of the closing price and the opening price of each period. The following steps are taken:

- A variable, total_rows, is created to store the total number of rows in the dataframe.
- A variable, correct_trend, is created to keep track of the number of times the trend direction correctly matches the direction of the price movement.
- The dataframe is looped through using df.iterrows() to check the accuracy of the trend.
- For each row, if the trend is not None, the closing price is compared with the opening price. If the closing price is greater than the opening price and the trend     is 'up', the correct_trend variable is incremented. If the closing price is less than the opening price and the trend is 'down', the correct_trend variable is         incremented.
- The accuracy is calculated by dividing the correct_trend by the total_rows.

![Project-3_EMA_TREND_BMO ipynb at main ](https://user-images.githubusercontent.com/110307714/218337138-78936712-3a50-4321-a8a0-45474b53310f.png)

### Trend Crossover Frequency
- A new variable, crossovers, is initialized to keep track of the number of trend crossovers.
- The dataframe is looped through using df.iterrows() and the following logic is used:
  If the trend length is equal to 1, it means that it is a crossover, so the crossovers counter is incremented.
  The final value of crossovers is printed, giving us the frequency of crossovers in the data.
 
![Project-3_EMA_TREND_BMO ipynb at main Project-3 - Google Chrome 2_12_2023 4_05_02 PM](https://user-images.githubusercontent.com/110307714/218337203-196e5b31-2830-477b-a158-1be1fe4578b2.png)

### The code above calculates the average impact of crossovers on the price of an asset. The following steps are taken:

 - Initialize variables to track the impact of crossovers:
   Crossover_count to keep track of the number of crossovers.
   Crossover_impact_sum to keep track of the total impact of the crossovers.
   Loop through the data using df.iterrows().

-  If a row has a value in the trend column (indicating a crossover), increment the crossover_count and add or subtract the difference between the close and open        prices from the crossover_impact_sum, depending on the trend direction.

-  After looping through the entire dataframe, divide the crossover_impact_sum by the crossover_count to find the average impact of the crossover on the price. 
