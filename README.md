# Kickstarting with Excel

## Overview

###  Purpose
This analysis was compiled and run to provide Louise with information intended to help her build a successful campaign for her play on kickstarter. This particular analysis focuses on trends for the Outcomes of Plays' Kickstarter campaings based on goals, and Theatre Outcomes based on Launch date. This way Louise can examine factors that influence the success or failure of campaigns, and apply it to her own project. Below are images graphs for "Outcomes Based on Launch Date" and "Outcomes Based on Launch Date."
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/100614266/159132749-ca9497d4-b66a-47d2-8e6c-dd9a45e51534.png)

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/100614266/159132744-121b0316-aa00-4ba3-95a8-fb6cb48592b4.png)

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
This sheet gathers the outcomes of the kickstarter data, however, for the ease of use for Louise, two filters have been added: "Parent Category," so she can filter by category easily, and "Years," so she can see the trends for each year, or for all years. The pivot table displays this data with Rows that specify months, to determine which months in any year experience the highest success, and which months to avoid launching her kickstarter campaign in. When opening the "Kickstarter-Challenge" workbook, the filter "Theater" should already be applied and the filter for years should be set to "All" so that the data displayed focuses on the outcomes of theater kickstarters for each month. 
![Sheet Launch](https://user-images.githubusercontent.com/100614266/159132752-0c46cf55-31f6-4c86-a2fb-d49517270caf.png)

### Analysis of Outcomes Based on Goals
This sheet attempts to determine trends between the monetary goal of campaigns in the subcategory of "Plays." The data has already been pre-filtered to focus on what would be most helpful for Louise and her play, *"Fever"*. The data is arranged in 12 Rows that represent increasing ranges that campaign goals would fall into. The columns organize outcomes for each campaign goal range, and show the percentage successful in relation to percentage failed in a line graph. Percentage canceled is also included, however, no campaigns for plays were cancelled in the dataset.
![Sheet Goals](https://user-images.githubusercontent.com/100614266/159132759-03139098-1e4e-49ed-92ba-22c6da4fce62.png)

### Challenges and Difficulties Encountered
Most operations went smoothly, however, while writting COUNTIFS for the "Outcomes Based on Goals" (written as "Outcomes(Goals)") in the workbook sheets), I made the mistake of forgetting to set criteria as being greater than/less than OR equal to, and ended up excluding a big chunk of relevant data. It too me several moments to identify the problem, which I did by filtering in the main data sheet ("Kickstarter") "Plays" that experienced Success and had a goal of 30,000. In my "Outcomes(Goals)" sheet, my cell that contained that data marked the value of successful plays in that goal range as 0. However, after cross checking with the main data sheet with my filters manually, I determined that there were 3 that fit this criteria. Therefore, I was doing something that was excluding data from being transferred properly. I played around with my formulas until I realized my exact mistake, and then corrected it.
## Results

### Results of Analysis of Outcomes Based on Launch Date
- Canceled Theater Kickstarters do not have any strong correlation to a specific time during the year. 
- Kickstarters launched between mid-April to Mid -June experience the most success, peaking during May. So, Kickstarters launched in late spring to early summer appear to be more successful than campaigns launched outside of those months. 
- Late fall and winter experience the least success and the most failure with a dip in success rates beginning in late October. December is the worst month to launch a campaign, based on the data. January and March are also bad months to launch a theater campaign.
- Summary: May is the best month to launch a theater campaign, while December is the worst.
### Results of Analysis of Outcomes Based on Goals
- The most success for plays can be found for goals that are less than 1000, or between 30,000 to 39,999, based on the chart.
- The least success for plays can be found between 20,000 to 24,999 and 40,000 to 44,999. However, due to the fact that there are significantly less data points for campaigns that had goals greater than 19,999, the trends of campaigns beyond this goal should be not be considered with great confidence. That being said, it does tell us that the majority of play campaigns are less than 19,999.
- Play campaigns within the range of 1000 to 19,999 experience about 50% (give or take a few percentage points) success or failure. Depending on the scope of Louise's play, campaign goals within this range may be most manageable, while mitigating failure as much as possible.
### Limitations of the Dataset
- We don't know any of the motivations that backers had for contributing their money, so we cannot help provide marketing data that would support Louise's campaign.
- We don't know the income brackets of the backers in this dataset, and therefore cannot help Louise determine what groups of backers drive the success of campaigns.
- We also don't know from this dataset if some of these campaigns were launched by groups that had previously encountered success with Kickstarter, and therefore have had better experience with Kickstarter, making the data from the groups possibly more valuable. Although it is also hard to tell if those who have experienced success with Kickstarter would need to rely on Kickstarter after success has been attained.
### Possible Tables and Graphs for Greater Success
- We could see some more statistics of backers, perhaps average donation per backer, to get an overall estimate of how many backers would help Louise reach success. This would also need to take into account backers who donate extreme amounts, and thereby represent an outlier. A box and whisker plot of the average donation per backer could be beneficial for Louise to get a grasp on how many people she would need to donate.
- We could also examine the relationship between duration of a campaign to its success. This would need the creation of a seperate column to hold the new data. Then, it would be best to organize this new data in a new sheet, establishing duration ranges in rows. We would then use the COUNTIFS function, like we did for the "Outcomes Based on Goals" analysis. I would use a line chart for this, with Count of Outcomes on the Y-axis, and Duration Ranges on the X-axis.
