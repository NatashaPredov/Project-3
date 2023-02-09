![RBC Banner Image](Images/00_RBC_Banner.png)

## Project 3

# Overview, Project Proposal & Scope

For project 3, our core team will be extending off of project 1 (https://github.com/NatashaPredov/Project-1-.git) and project 2 (https://github.com/NatashaPredov/Project-2.git). In short, a summary of Project 1 and Project 2 is as follows:

  Project 1: 
  
    - Wanted to investigate and determine a predictive model for the long term behaviour of relatively stable ETFs.
    - Wanted understand how this model would react and change due to the unforseen impacts the COVID-19 pandemic had on the Canadian Banks.
    - The timeframe of the model data that the team will be analyzing covers 4 years: August 2016 through July 2020. While the validation data will cover:      - August 2019 through July 2020 - 6 months before and after the February 2020 COVID-19 crash. Due to this being unforseen and very out of the ordinary, the team will be ignoring the data up until Feb 2020 then picking our analysis back up 6 months post crash.
  
  Project 2: 
  
    - Determine a trading strategy for Scotiabank stocks (BNS) in a way that will beat a buy and hold strategy relative to the other correlated Bank stocks.

  
In project 3, our team used 3 years of data to build the models that would help to determine if we are confidnet that the trend for the next two weeks are up (= long trade), down (= short trade), flat to to emulate trading security multiple times within a business week. This would help to monitor the trade moving forward. 

In project 3, our team utilized RBC on TSX (CAD $) and on American Exchange (USD $) to understand correlation. In order to create an algorithm the predicts a stock’s trend over the next 10 trading days. The work below extends from the learning obtained since Project 2 completed through 

1.Utilizing Metrics for Feature engineering: std dev, average price as determined by the avg open/close high/low or all four
2. 3 types of Modes for prediction: Machine Learning, Neural Networks, and Moving Average Model.

Before we proceed to the Process of the work completed in Project 3, a few clarifying definitions: 

  Day Trading
  
    - If you buy and sell (or sell and buy) a security within the same day, you are day trading.
    - Day traders leverage fluctuations in an asset's daily price with a goal of turning a profit.
    
 Week Trading
    - If you buy and sell (or sell and buy) a security within a week or two, you are week trading. 
    - Week traders leverage fluctuations in an asset's price over several days with a goal of turning a profit.



# Process
 
Model 1: Machine Learning

Model 2: Neural Networks

Model 3: 

# Findings and Outcomes

# Next Steps

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
