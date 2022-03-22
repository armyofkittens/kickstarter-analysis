# Analysis of Kickstarter Campaigns
## Overview of Project

### Purpose
After the kickstarter for Fever went live, it fell short of it's initial fundraising goal. The purpose of this analysis is to see if there was a more optimal Kickstarter launch date for a theater based production, or if the launch goal amount disuaded people from pledging to the campaign.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
<p align="center">
  <img src="https://github.com/armyofkittens/kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png" width="700"/>
</p>
  In the first quarter of the year the overall volume of kickstarters were lower, with January trending upwards but declining by March. In the second quarter we see the number of successful kickstarters skyrocket, but then continue to trend down through the third quarter. September seems to see a slight uptick in successful kickstarters however there is also a disproportionately large increase in failed kickstarters. The year ends with the lowest number of successful kickstarters. 

  **A new "Year" column was created in order to extract the year from the kickstarter date creation, and then the entire database was imported into a PivotTable. The Year and Category was added as a filter to allow user manipulation, and then for the pupose of this analysis the Theater category was selected. The column was then set to outcomes and the rows were set to Kickstarter creation dates. Each cell contains the number of outcomes based on selected criteria and then sorted to show the number of successful kickstarter campaigns first. Data was moved into a line chart by using PivotChart. 

### Analysis of Outcomes Based on Goals
<p align="center">
  <img src="https://github.com/armyofkittens/kickstarter-analysis/blob/main/Outcomes_vs_Goals_Final.png" width="700"/>
</p>
  The results indicate that there is a lot of success with very low goals, and mid-to-high goals. The highest percentage of overall successes is in the "less than 1000" range" as well as the $35,000-$45,000 range. The sweet spot for failed goals is in the $25,000-$29,000 range as well as anything over $45,000. The mid to low range of $15,000-$20,000 indiate that there isn't a huge difference in that rage between failed and success. 

  **A new worksheet was created using a range of goals to be pulled from the "goals" column of the Kickstarter worksheet. The =COUNTIF formula was used to filter the data by the subcategory "play" and also their outcomes. Pulling the data required using correct less than and equal anotations in the formula in order to pull an accurate dataset. After importing to a PivotTable, the goals were added to the rows, and the sum of percentages were added in values.

### Challenges and Difficulties Encountered
Some challenges faced with "Theater outcomes by launch date" included not being able to set the filter to ascend starting with the successful outcome. "Outcomes vs Goals" presented the most challenge, however. The =COUNTIF formula has you reference your columns from the Kickstarter worksheet, and if you're not paying attention it's possible to reference the wrong column. In addition, double checking yourself due to the tediousness of adding a different formula to account for the goal range is a must, as it can skew your results heavily. Changing the columns in both your worksheet representing percentages to the percentage data type was not explained, but something that could easily be missed. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
<ul><li> </li>
- The worst time to launch a Theater kickstarter is at the very end of the year

- What can you conclude about the Outcomes based on Goals?
*The best Goal to Outcome is in the very low end as well as mid-to-high end

- What are some limitations of this dataset?
*There isn't anything granular enough to tell us which genre of play is more successful than another, for example romance vs. comedy

- What are some other possible tables and/or graphs that we could create?
*The data in outcomes vs goals is not weighted by number of kickstarters, so would like to dig into theater outcomes by goal rather than percent successful.
