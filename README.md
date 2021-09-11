# Kickstarting with Excel 

## Overview of Project 

### Purpose 

Previous analysis of Kickstarter fundraising campaigns was conducted for a client looking to produce her play with a fundraising goal of $12,000. Initial analysis revealed that both the launch date and the fundraising goal amount played significant roles in the outcome of the campaign. Further analysis was conducted to provide detailed insight into how these two factors played out in similar campaigns to the client's. 

This report illuminates how theater campaigns were impacted by their launch date, and more specifically, how play campaigns were impacted by their fundraising goals. As the goal of $12,000 was shown to be significantly higher than most successful campaigns in the initial report, this analysis seeks to investigate trends and patterns that would contribute to the success of the client's fundraising campaign. 

## Analysis and Challenges 

### Analysis of Outcomes Based on Launch Date 

Using the Kickstarter data set, I created a pivot table to compare the outcomes of theater campaigns based on the date they were launched. The table was filtered by the parent category of theater and by years. The rows were comprised of the date created conversiond data, and the columns portrayed outcomes with live campaigns filtered out. The values were set as count of outcomes. The columns were also filtered to show the outcomes in descending order, beginning with successful and ending with canceled outcomes. 

I then created the following pivot chart using the above pivot table. The chart type chosen was a line chart that plotted how many successful, failed, and canceled theater campaigns were launched by month. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/89217291/132950864-5732ec99-9c42-4336-b4c5-4dd4cba79d84.png)


### Analysis of Outcomes Based on Goals 

For the second focus area of the report, I created a new sheet titled "Outcomes Based on Goals" and labeled the rows based on different ranges of fundraising goal amounts. The following ranges were included and analyzed: 

* Less than 1,000
* 1,000-4,999
* 5,000-9,999
* 10,000-14,999
* 15,000-19,999
* 20,000-24,999
* 25,000-29,999
* 30,000-34,999
* 35,000-39,999
* 40,000-44,999
* 45,000-49,999
* Greater than 50,000

The first three columns were labeled "Number Successful," "Number Failed," and "Number Canceled." These data point were calculated using the COUNTIFS formula to filter outcomes by the criteria of successful, failed, or canceled, by goal amounts for the relevant range, and by the subcategory of plays. 

For example, the successful campaigns in the 1,000-4,999 range were calculated using the following formula:

=COUNTIFS(Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays", Kickstarter!$D:$D, ">=1000", Kickstarter!$D:$D, "<5000")

The next column, titled "Total Projects," was filled in using the SUM formula to tally up the number of successful, failed, and canceled campaigns for each range. 

The final three columns, titled "Percentage Successful," "Percentage Failed," and "Percentage Canceled," were calculated using the ROUND formula to divide the relevant columns by the total project column in order to get the nearest percent out of 100 with zero decimal places. 

After each cell of the table was filled in, I created the following corresponding line chart to plot the percentage of outcomes based on fundraising goal ranges. 

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/89217291/132950920-83593db5-54f0-40ca-9000-ac6aa8355fa2.png)

### Challenges and Difficulties Encountered 

Challenges in analyzing the data were primarily logistical difficulties that accompanied maneuvering through a large data set. I originally did not protect my formulas with the $ symbol, leading to some of the values sliding when I tried to leverage them into another column. When creating a pivot table for the theater outcomes based on launch date, the rows automatically included additional values that complicated the table. This was quickly solved by removing these values. 

## Results 

### Conclusions about Outcomes Based on Launch Date 

Analysis of outcomes based on launch dates showed that the month of May launched the most successful theater campaigns with 111 successful outcomes. 

However, May also had one of the highest numbers of failed campaigns, with 52 failed outcomes. Months similarly high in failed outcomes proved to be June with 49, July with 50, August with 47, and October with 50 failed campaigns. 

### Conclusions about Outcomes Based on Goals 

Overall, the percentage of successful play campaigns tended to decrease and the percentage of failed play campaigns increase as the fundraising goals increased. The highest percentage of successful play campaigns occurred in goals less than $1,000, which was closely followed by the $1,000-$4,999 range. 

### Limitations of the Data Set 

As much information as this data set is comprised of, it does not give the full scope of factors responsible for certain outcomes. We don't know what capacity or resources each campaign already had for promoting their play and fundraising campaign. We don't know if the play producers of successful campaigns already had a platform or what type of advertising they participated in. 

Although this report provides valuable insight into trends in Kickstarter crowdfunding campaigns, further analysis is needed into the circumstances surrounding each campaign in order to analyze comparable data to the client's proposed campaign. 

### Suggested Additional Analysis

Further analysis would benefit from increased specialization to more closely reflect the circumstances of the client's fundraising goals. Both above charts and tables could be filtered by the US, the country of client's production, and by the subcategory of plays. 

Another possible significant factor is the outcome of the play campaigns based on the length of campaign. Although May showed the highest percentage of successful play campaigns, it also displayed a higher percentage of failed campaigns. Further analysis on contributing factors is therefore necessary. 
