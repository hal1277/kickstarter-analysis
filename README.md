# Kickstarting with Excel
An Analysis of prior Kickstarter Campaigns

## Overview of Project
Louise has had success before with Kickstarter campaigns to fund plays.  She is considering begining another kickstarter campaign to fund a new play to be launched in the US and has asked for help with the analysis.  

### Purpose
The purpose of this analysis is to gain insights from the data on prior Kickstarter campaigns and use that to provide some recommendations to Louise on how to launch a new successful Kickstarter campaign to fund her next play.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
The data set was analyzed with a Pivot Table.  The table was filtered to focus on theater Kickstarter campaigns only.  The table sorted the data by month and by whether the campaign was successful, failed or cancelled.  A chart was then created to visual the data.  [Outcomes based on launch date](https://github.com/hal1277/kickstarter-analysis/blob/main/Theater_Outcomes_Based_on_Launch_Date.png)

### Analysis of Outcomes Based on Goals
The data set was also analyzed based on the original goal set.  The data was filtered specifically on plays and the table broke down the campaigns by goals in $5,000 increments and whether the campaign was successful, failed or cancelled.  A chart was then created to visual the data. [Outcomes vs Goals](https://github.com/hal1277/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
As with any data set the data first had to be reviewed and cleansed.  The dates originally presented were in Unix timestamp form so that had to be converted to a standard date format that is more easily understood. 
| deadline   | launched_at | Date Created Conversion | Date Ended Conversion |
|------------|-------------|-------------------------|-----------------------|
| 1411679804 | 1409087804  | 2014-08-26              | 2014-09-25            |

Statistical analysis revealed that there were some extreme outliers in the goal data field.  Closer examination of these outliers revealed that they were all tied to either failed or cancelled campaigns.  Since the analysis focused on the commonalities of successful campaigns these outliers did not affect the analysis.  However, it is important to regognize them should we do any further analysis on the failed campaigns.  
|                               | Successful  | Failed  |
|-------------------------------|-------------|---------|
| Mean Goal                     | $5,049      | $10,554 |
| Median Goal                   | $3,000      | $5,000  |
| Standard Deviation of Goal    | $7,749      | $21,968 |
| Upper Quartile of Goal        | $5,000      | $10,000 |
| Lower Quartile of Goal        | $1,500      | $2,000  |
| IQR of Goal                   | $3,500      | $8,000  |
|                               |             |         |
| Mean Pledged                  | $5,602      | $559    |
| Median Pledged                | $3,168      | $103    |
| Standard Deviation of Pledged | $8,335      | $1,331  |
| Upper Quartile of Pledged     | $5,699      | $501    |
| Lower Quartile of Pledged     | $1,717      | $9      |
| IQR of Pledged                | $3,982      | $492    |

## Results

The analysis indicates that May is the best month for launching a successful campaign.  And, December is the worst month for lauching a successful campaign.  

The analysis indicates that campaigns with goals lower than $5,000 have the highest success rates.  

We do not know how representatve this date set is.  Of the total data on the report just 25% of the data relates to plays which is specifically what Louise would like to start a Kickstarter campaign on.  But, we have no indiction of how this sample relates to the total population of plays funded by Kickstarter campaigns.  As well theater is a matter of personal taste and we cannot easily tell from this data how the different plays vary from each other, such as comedy, drama, etc, and how that might affect generating the interest of backers.

It would be useful to analyze outcomes based on launch date and goals together. Currently the data suggests that lauching in May is a predictor of succsess and that campaigns under $5,000 is a predictor as well.  It would be useful to see the goals by launch month to determine if the month alone is a predictor of success or if May just happened to be when the most under $5,000 campaigns were launched.  
