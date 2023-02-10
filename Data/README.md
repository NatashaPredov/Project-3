# Project 3 - Predict the Weekly Trend of Royal Bank (RY.TO)
# Data
![RBC Banner Image](../Images/00_RBC_Banner.png)
  
## Project Overview  
---
Objective: To enhance returns savings accounts through an active trading process that can be executed in all types accounts.    
Approach:  By predicting the weekly trend of Royal Bank (RY.TO)  
  
## Data Dictionary  
---
| No. | Field	                        | Description  
| --- | -----	                        |	-----------  
|  1. | 'Open'                        | Stock Data Opening Price  
|  2. | 'High'                        | Stock Data High Price  
|  3. | 'Low'                         | Stock Data Low Price  
|  4. | 'Close'                       | Stock Data Closing Price  
|  5. | 'Adj Close'                   | Stock Data Adjusted Closing Price  
|  6. | 'Volume'                      | Stock Data Volume  
|  7. | 'Mid_hl'                      | Average of High and Low Price  
|  8. | 'Mid_oc'                      | Average of Open and Close Price  
|  9. | 'Mid_hloc'                    | Average of High, Low, Open and Close Price  
| 10. | 'Close_in_range'              | Close as a Percent of High (1) and Low (0)  
| 11. | 'Returns_1Day_Moc'            | 1 Day Percent Change in Avg Open/Close   
| 12. | 'Returns_5Day_Moc'            | 5 Day Percent Change in Avg Open/Close   
| 13. | 'Returns_30Day_Moc'           | 30 Day Percent Change in Avg Open/Close   
| 14. | 'Returns_1Day_Mhloc'          | 1 Day Percent Change in Avg High/Low/Open/Close   
| 15. | 'Returns_5Day_Mhloc'          | 5 Day Percent Change in Avg High/Low/Open/Close   
| 16. | 'Returns_30Day_Mhloc'         | 30 Day Percent Change in Avg High/Low/Open/Close   
| 17. | 'Std_Dev_10Day_Moc'           | 10 Day Standard Deviation in Avg Open/Close  
| 18. | 'Std_Dev_30Day_Moc'           | 30 Day Standard Deviation in Avg Open/Close  
| 19. | 'Std_Dev_10Day_Mhloc'         | 10 Day Standard Deviation in Avg High/Low/Open/Close  
| 20. | 'Std_Dev_30Day_Mhloc'         | 30 Day Standard Deviation in Avg High/Low/Open/Close  
| 21. | 'SMA_Returns_8Day_Mhloc'      | Simple Moving Average (SMA) 8 Days High/Low/Open/Close  
| 22. | 'SMA_Returns_20Day_Mhloc'     | Simple Moving Average (SMA) 20 Days High/Low/Open/Close  
| 23. | 'SMA_Delta_8_20Day_Mhloc'     | 8 Day SMA less 20 Day SMA  
| 24. | 'SMA_Signal_8_20Day_Mhloc'    | 8 Day SMA >= 20 Day SMA then 1 else 0  
| 25. | 'high_slope'                  |	10 Day Regression Slope - High Price   
| 26. | 'high_intercept'              |	10 Day Regression Intercept - High Price   
| 27. | 'mid_hl_slope'                |	10 Day Regression Slope - Avg. High/Low Price   
| 28. | 'mid_hl_intercept'            |	10 Day Regression Intercept - Avg. High/Low Price   
| 29. | 'mid_oc_slope'                |	10 Day Regression Slope - Avg. Open/Close Price   
| 30. | 'mid_oc_intercept'            |	10 Day Regression Intercept - Avg. Open/Close Price   
| 31. | 'low_slope'                   |	10 Day Regression Slope - Low Price   
| 32. | 'low_intercept'               |	10 Day Regression Intercept - Low Price   
| 33. | 'trend_10day'                 | Up Trend (3/4 Slopes >= 0) = 1; Down Trend (3/4 Slopes < 0) = 0   
  
  
  
## Data csv Files
---
1. [BMO - Bank of Montreal CSV file](Feature_Engineering_BMO.csv)  
2. [BNS - Scotiabank CSV file](Feature_Engineering_BNS.csv)
3. [CL - Oil CSV file](Feature_Engineering_CL.csv)
4. [CM - Canadian Imperial Bank of Commerce CSV file](Feature_Engineering_CM.csv)
5. [NA - National Bank CSV file](Feature_Engineering_NA.csv)
6. [RY - Royal Bank CSV file](Feature_Engineering_RY.csv)
7. [TD - Toronton Dominion Bank CSV file](Feature_Engineering_TD.csv)
8. [XGB - Government Bond Index ETF CSV file](Feature_Engineering_XGB.csv)
9. [ZEB - Canadian Bank Index ETF CSV file](Feature_Engineering_ZEB.csv)
10. [ZWB - Canadian Covered Call Bank Index ETF CSV file](Feature_Engineering_ZWB.csv)


