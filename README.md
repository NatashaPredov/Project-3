# Project 3 - Predict Weekly Trends of Royal Bank (RY.TO)
![RBC Banner Image](Images/00_RBC_Banner.png)

# Overview, Project Proposal & Scope

For project 3, our core team will be extending off of project 1 (https://github.com/NatashaPredov/Project-1-.git) and project 2 (https://github.com/NatashaPredov/Project-2.git). In short, a summary of Project 1 and Project 2 is as follows:

  Project 1: 
  
- Wanted to investigate and determine a predictive model for the long term behaviour of relatively stable ETFs.
- Wanted understand how this model would react and change due to the unforseen impacts the COVID-19 pandemic had on the Canadian Banks.
-  The timeframe of the model data that the team will be analyzing covers 4 years: August 2016 through July 2020. While the validation data will cover:      
    - August 2019 through July 2020 
    - 6 months before and after the February 2020 COVID-19 crash. Due to this being unforseen and very out of the ordinary, the team will be ignoring the data up until Feb 2020 then picking our analysis back up 6 months post crash.
  
  Project 2: 
  
- Determine a trading strategy for Scotiabank stocks (BNS) in a way that will beat a buy and hold strategy relative to the other correlated Bank stocks.

  
In project 3, our team used 3 years of data to build the models that would help to determine if we are confidnet that the trend for the next two weeks are up (= long trade), down (= short trade), flat to to emulate trading security multiple times within a business week. This would help to monitor the trade moving forward. 
  
Project 3:  
In project 3, our team utilized RBC on TSX (CAD $) and on American Exchange (USD $) to understand correlation. In order to create an algorithm the predicts a stock’s trend over the next 10 trading days. The work below extends from the learning obtained since Project 2 completed through: 

1. Utilizing Metrics for Feature engineering: std dev, average price as determined by the avg open/close high/low or all four
2. 3 types of Modes for prediction: Machine Learning, Neural Networks, and Moving Average Model.

Before we proceed to the Process of the work completed in Project 3, a few clarifying definitions: 

>**Day Trading** 
>- If you buy and sell (or sell and buy) a security within the same day, you are day trading.
>- Day traders leverage fluctuations in an asset's daily price with a goal of turning a profit.
     
>**Week Trading**
>- If you buy and sell (or sell and buy) a security within a week or two, you are week trading. 
>- Week traders leverage fluctuations in an asset's price over several days with a goal of turning a profit.



# Process
## Step 1: Feature Engineering
---
1. Imput: Import Daily Data with an API
    - Prices: High, Low, Open, Close, and Adjusted Close; and Volume
    - API: Yahoo Finance
2. Create New Variables - Feature Engineering
    - Feature X Variables
      - Feature X data is used to predict Target Y data
      - Backward Looking becase the data must exist in order to be used in a prediction
      - Average Prices: High/Low, Open/Close, High/Low/Open/Close,
      - Price Changes: Percent Change, Standard Deviations, z-Scores
      - Moving Average Prices
    - Target Y Varibles
      - Target Y Data is predicted from Feature X data
      - Forward Looking because the data will not exist when making predictions 
      - 10-Day Linear Regresion where the slope indicates the trend
    - [Feature Engineering README](/Code_0_Feature_Engineering/README.md)  
3. Output: CSV Files
    - Create 1 csv file for each security
    - Files are to be combined during the Variable Selection step
    - [Data Files README](/Data/README.md)  
    - [Data Files Data Dictionary](/Data/Feature_Engineering_Data_Dictionary.txt)
4. Feature Engineering Jupyter Notebooks and CSV Files  
    > Links to Jupyter Notbook and CSV Data files.  

      | No. | Jupyter Notebook	                            | CSV File  
      | --- | ----------------	                            | -----------  
      |  1. | [RY.TO](/Code_0_Feature_Engineering/Fearure_Engineering_RY_TO.ipynb)      | [Royal Bank](/Data/Feature_Engineering_RY.csv)  
      | --- | ----------------------                        | -------------------------------------------   
      |  2. | [BMO.TO](/Code_0_Feature_Engineering/Fearure_Engineering_BMO_TO.ipynb)    | [Bank of Montreal](/Data/Feature_Engineering_BMO.csv)  
      |  3. | [BNS.TO](/Code_0_Feature_Engineering/Fearure_Engineering_BNS_TO.ipynb)    | [ScotiaBank](/Data/Feature_Engineering_BNS.ipynb)  
      |  4. | [CM.TO](/Code_0_Feature_Engineering/Fearure_Engineering_CM_TO.ipynb)      | [Bank of Commerce/CIBC](/Data/Feature_Engineering_CM.csv)  
      |  5. | [NA.TO](/Code_0_Feature_Engineering/Fearure_Engineering_NA_TO.ipynb)      | [National Bank](/Data/Feature_Engineering_NA.csv)  
      |  6. | [TD.TO](/Code_0_Feature_Engineering/Fearure_Engineering_TD_TO.ipynb)      | [TD Bank](/Data/Feature_Engineering_TD.csv)  
      | --- | ----------------------                        | -------------------------------------------  
      |  7. | [CL.TO](/Code_0_Feature_Engineering/Fearure_Engineering_CL.ipynb)         | [Crude Oil](/Data/Feature_Engineering_CL.csv)  
      |  8. | [XGB.TO](/Code_0_Feature_Engineering/Fearure_Engineering_XGB_TO.ipynb)    | [Government Bond Index](/Data/Feature_Engineering_XGB.csv)  
      |  9. | [ZEB.TO](/Code_0_Feature_Engineering/Fearure_Engineering_XEB_TO.ipynb)    | [Canadian Bank Index](/Data/Feature_Engineering_ZEB.csv)  
      | 10. | [ZWB.TO](/Code_0_Feature_Engineering/Fearure_Engineering_ZWB_TO.ipynb)    | [Canadian Bank Index with Covered Call](/Data/Feature_Engineering_ZWB.csv)  
  
## Step 2: Variable Selection
1. Project 1 Outcome
    - Feature Engineering data from other securities can generate highly correlated relationships to the Target security 
    - Focus on percent change and variing the number of days to calculate percent change  
2. Project 2 Outcome 
    - Highly correlated Feature X and Target Y percent change variables (Project 1) can be used to create strong predictive models
    - Refined the outputs of Project 1 and tested several modeling techniques with the data
3. Project 3 Experiment
    - Engineer an number of both Feature X and Target Y varibles
    - Identify highly correlated Feature X and Target Y varibles to be used in the modeling process 
> **Note:** There was insufficent time to inplement a robust variable selection process
## Step 3: Modelling
---
### Model 1: Machine Learning
  - [Machine Learning README](Code_1_Machine_Learning_Model)    
### Model 2: Neural Networks
  - [Neural Networks README](/Code_2_Neural_Network_Model/README.md)    
### Model 3: Moving Average
  - [Moving Average README](/Code_3_Moving_Average_Model/README.md)    
  
  
# Findings and Outcomes
---
  
# Next Steps
---
From project 1 to project 3, our team's output of the project has been code first focus meaning that we did not have a front end user interface for our project. User interfaces allow users whom may not be as technically savy as the project group, to view, access, alter and use the code we have developed over the last 6 months. Therefor if the cumulation of our work were to be fully recognized and utilized by the general public, our next step would be to connect the backend code to a front end UI that incorporates an easy to use user experience. The UI/UX will focus on delivering our code in a simplistic, straightforward, consistent manner. 

From detailed research, a few options stuck out that range from pre built options to building of our own solution:

(1) Django - a python framework that produces maintainable webesites. It removes the barrier to entry for front end development and design, and allows developers to focus on the meat of a website, the backend logic

  Link: https://www.djangoproject.com/start/overview/
  
(2) Utilization of APIs - APIs, Applicaton Programming Interface, connects the server side (where the code lives) to the client side (what the user interacts with) to allow the requests sent by the user to be absorbed by the code side to then output a result

(3) React - JS web application interface that can be used in parallel with Django with less code than other front end options  

The answer to which of these above options would fully depend on the timeline of which we want to produce this front end and how much invovlement we, as a team would like. If, for example, we are pitching our projects as a POC, looking for seed investments, I would suggest utilizing Django as it outlines  clear documentation on how to write a database driven web app through extensive docs and community contributions. If on the other hand our team had another 6 months to really stregthen the code, build up low and high fidelity prototypes, conduct beta user testing and meet the satisfactions of the stakeholders, I would suggest that we build strong configuration files and APIs of which the front end could call to when a user interacts with the UI that was curated specifically for our users. 

# Installation Guide and Slide Revision

To view this project, follow the main branch found in this Github repo to the final code that encompasses all of the contributions made by the team members.

The code which is submitted is commented with concise, relevant notes that other developers can understand so future extensions on the work submitted can be explored if needed.

To review the Google Slides that were presented to the class kindly use: https://docs.google.com/presentation/d/1C8Vvf03I_RBEGCyahndJCq-2HyYml-AoFkWYqBYA9f0/edit?usp=sharing
