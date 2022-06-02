# Kickstarting with Excel

## Overview of Project: An Analysis of Kickstarter Campaigns

### Purpose: This analysis will describe some of the techniques used to uncover a series of trends - most notably, two distinct conclusions about 'Outcomes Based on Launch Date' and 'Outcomes Based on Goals'. It will also included an explaination of how I performed the analysis using images and links to code, as well as any challenges I encountered and how I overcame them.

#### Analysis and Techniques Used: I analyzed by using the different techniques and methods taught in class. For example, for deliverable 1, I had to click on the PIVOT TABLE button on the 'Tools' tab in excel in order to insert that graph. ![This is an image](file:///Users/carlosmorales/Desktop/Screen%20Shot%202022-05-30%20at%201.25.24%20PM.png). Afterwards, I had to pick and choose which sets of values, columns, rows, and filters that were necessary to display the information for the outcomes of theater campaigns based on launch date. In this scenario, I had to use "Parent Category" and "Years" as the filters, "Outcomes" as the legend, "Date Created" as the axis, and "Count of Outcomes" as the values. Although the information that was needed was properly pulled, it still needed some sort of visualization to tell the whole story. By selecting the 'Insert' tab, Excel offers a wide range of graphs - however, I needed to pick one that would make sense in this scenario. This led to using Excel's tool of creating a line graph. ![This is an image](file:///Users/carlosmorales/Desktop/Screen%20Shot%202022-05-30%20at%201.42.44%20PM.png) A line graph was most appropriate since it tells the story of information over a certain period of time, by using lines and points to display when each outcome was most and least prevalent. In Deliverable 2, I used functions such as `=COUNTIFS()` and `=SUM()` to populate the "Number Successful," "Number Failed," and "Number Canceled" columns in the "Outcomes Based on Goals" sheet based on certain filters. These filters were based on the "Goals" column which included parameters such as 'less than 1000'. The function that was used was to calculate the number of plays that were less than 1000 in the "Number Successful" column, was `=COUNTIFS(Kickstarter!$D:$D, "<1000", Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays")`. The `=COUNTIFS()` function accepts several criteria, like a cell range for the column of interest and the criteria to filter data from that column, therefore, in the example I provided, it is using the Kickstater sheet as a reference for the cell range and pulling data from the 'D' column which is set to goals, the 'R' column which is set to outcomes, and the 'R' column which is set to subcategories. This was done to each column to gather all the information needed for another visual graph.

#### Analysis of Outcomes Based on Launch Date and Results: One conclusion that I came up with from this graph is that May is an excellent month for a campaign to have a high chance of being successful. May had the most amount of campaigns that were successful, 111 - 11 more than the next highest month which was June with 100. This also leads to the next conclusion; after May, there comes a dropoff in the following months for successful campaigns. June through September see a steady decline of successful campaigns, therefore, one should become weary that to have the best chance of launching a sucessful campaign, one must do so before summer ends. The last quarter of the year becomes a difficult time for a campaign to be successful. December, by far, is the month that should be avodided if one is to decide when to launch a successful campaign. December only has 37 successful campaigns compared to 35 failed campaigns - this ratio is not favorable. Ultimately, one should have a good chance of a successful campaign if it is launched before the last quarter of the year, and the best chance if it is launched in May. ![This is an image](file:///Users/carlosmorales/Desktop/Data%20Science%20Class%20Folder/Module%201%20-%20Kickstarter%20Analysis/Resources/Theater_Outcomes_vs_Launch_.png)

#### Analysis of Outcomes Based on Goals and Results: One thing that I can conclude is that the line graph is symmetrical. The "Percentage Successful" line starts at a rate of "75.91%" while the "Percentage Failure" line starts at a rate of "24.19%". Both of these start to come to mirror each other as they move through the x-axis. They also meet each other at several points in the line graph - meaning that they had the same percentage. For example, for "plays" that had a goal of '15,000 to 19,999', both "Number Successful" and "Number Failed" were at a percentage of "50%", meaning that they had the same number of successful and failed plays at the parametere.The line graph also displayed equal outcomes/percentages for "Number Successful" and "Number Failed" at other parameters such '35,000 to 39,999' and '40,000 to 44,999'. ![This is an image](file:///Users/carlosmorales/Desktop/Screen%20Shot%202022-06-01%20at%207.59.24%20PM.png)

#### Challenges and Difficulties Encountered: There were was only one difficulty encountered - primarily, in deliverable 2. I managed to get the correct function that was needed in order to populate the different columns, but when I pulling data the number didn't make sense and the line graph that was created based off the data didn't match with what the challange had. I tried redo the formula again in each cell because I noticed that trying to copy and paste the formula and stick it in the next column over, even with changing the parameters, was pulling data that was wrong. It turns out that I was using the wrong data set to make my calculations.

#### Limitations and Possibilities: One limitation from the "Theater Outcomes by Launch Date" sheet is that it is only telling a certain part of the story. In other words, the data is limited to one Parent Category - there are other categories missing as well as subcategories. Including these can give us a clearer picture of what types of subcategories are actually succeeding, failing, or being canceled. This data set is also looking at all the years grouped together instead of a single year, where one might want to analyze how one particular year performed. One limitation from the "Outcomes Based on Goals" sheet is that the parameter set for 'Goals' just show the data from those specific ranges. For example, we analyze the data of 'plays' starting off with 'Less than 1000' - we could develve further into this by looking at a parameter within that range. The parameters are set only to a certain part of the whole data set - it is limited to what has been established. There are several possible tables that we could create. For example, the "Theater Outcomes by Launch Date" sheet could use a box to graphically demonstrate the spread and skewness groups of numerical data through their quartiles. We could use this graph to see which data points are misleading or off center. We can also use a bar graph for the same sheet - it demonstrates categorical data with rectangular bars with heights or lengths proportional to the values that they represent, therefore we can use it to visualize the outcomes of each month.
