# Kickstarting with Excel

## Overview of Project
The process of using data from past crowdfunding projects that include lifestyle categories such as, food, film, technology, etc. to identify success/failure rates in order to support a new Kickstarter campaign with a focus in the theater category.

The requestor, Louise, a playwright is looking to create a campaign to fund her upcoming project, a play "Fever". She has asked for assistance to understand how campaigns work and what key factors should she focus on in order to plan a successful campaign.
 

### Purpose
The purpose of this project is to learn how to use excel as a tool to analyze a dataset consisting of greater than 4,000 crowdfunding projects to identify trends and provide recommendations on how a new campaign should be approached based on historical outcomes. Within this exercise, I learned how to:

* convert Unix Timestamps into month/day/year format.
* use Pivot Tables on specific data points (i.e. theaters)
* create Pivot Charts to provide a visual summary of outcomes.
* using Statistical Formulas to identify outliers.

## Analysis and Challenges
Most of the analysis was done by sorting the dataset using Pivot Tables and creating Pivot Charts to plot the results. 
Firstly, percentage funded data was added and was calculated using the formula =`ROUND(E2/D2*100,0)`.
Average donation(replacing the error zero)=`IFERROR(ROUND(E2/L2,2),0)`.
Converting the Unix timestrap for the launch and deadline date=`(((J2/60)/60)/24)+DATE(1970,1,1)`

There were a few challenges I faced working on the dataset.
* Unix timestamp formula returned values, but the format did not appear as mm/dd/yyyy. Used the "date" format function in order to convert to the correct format.
* The process to use COUNTIFS formula to calculate the number of successful vs. failed vs. canceled campaigns was done manually. When the range was greater than x, but less than y, I would end up with an error depending on how I wrote the formula. I have not used the term successful in the formula so was unclear for which coulmn to show to outcomes.
number successful =`COUNTIFS(Kickstarter!$F:$F,"=successful",Kickstarter!$D:$D,"<1000",Kickstarter!$R:$R,"plays")`.

### Analysis of Outcomes Based on Launch Date
Campaigns launched in May or June are more successful than in November-Janurary.
In the chart we see that more than 100 successfully funded campaigns are from May/June compared to less than 40 in December.

### Analysis of Outcomes Based on Goals
Campaigns with goals less than $5000 saw an average of 76% success rate compared to the other ranges. When you analyze why campaigns failed, the results showed that the average goal for failed campaigns was greater than $10554 with only an average of $559 funded. This would mean that the higher the goal, the less likely it would succeed due to campaign length of time.
### Challenges and Difficulties Encountered
Challenges and difficulties encountered were mainly the learning curve of using Office 365 version of Excel on windows.

Being new to GitHub, gitlab and virtual learning, I found it confusing at times getting set up and knowing what to do and where to go for a detail outline/instructions or maybe a "how-to" guide. Now that I am set up properly and completed this first challenge, I am hoping that the upcoming weeks will run a lot smoother.
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

    1. The best time to launch a campaign is May or June as result showed higher successful outcomes.

    2. Campaigns mostly failed in November-Janurary.
- What can you conclude about the Outcomes based on Goals?
    
    Campaigns are more successful when goals are 5000 whereas campaigns with goals greater than 10000 had failed the most.
- What are some limitations of this dataset?

    * Some of the limitations that would be helpful in making this dataset more powerful are:

   * Provide references on why campaigns failed. Was it due to length of time, launch date or unreasonable goals?

   * Determine what marketing tool was used to advertise the campaign (i.e. flyers, social media, TV Ads,etc.)

- What are some other possible tables and/or graphs that we could create?
    * A comparison of US vs. GB by success rate compared to total campaigns. 
    * A comparison of US vs. GB by launch date. 