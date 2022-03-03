# kickstarter-analysis
Kickstarting with Excel: Performing analysis on Kickstarter data to uncover trends

## Overview of Project

The Kickstarter Analysis project examined 4,114 Kickstarter crowdfunding projects to derive insights regarding trends in 1) the amount of money sought and pledged, and 2) success or failure in meeting the crowdfunding goal. The analysis included information regarding each Kickstarter project's location, category of content, dates created and ended, number of backers, and average donation.


### Purpose

The specific purpose of this Excel analysis was to identify trends in a Kickstarter campaign's success relative to the campaign's launch dates and funding goals, specifically for campaigns related to theater productions. To do this, we created visualizations of: 1) theater campaign outcomes based on launch dates, and 2) success relative to funding goals for campaigns in the "plays" subcategory. 
 

## Analysis and Challenges

The dataset was presented as an Excel sheet, and we employed formulas, tables, pivot tables, pivot charts, and conditional formatting to help visualize any trends, for example: 
![screenshot-conditional formatting](https://user-images.githubusercontent.com/100863488/156620056-4b48eb16-89c5-4b98-95d9-ba7f433e4a20.png)

We also employed statistical analysis to identify the range of the dataset and outliers, e.g.:
![screenshot-statistics](https://user-images.githubusercontent.com/100863488/156620369-89c380d7-220d-4027-8cc8-d07b39801d5a.png)



### Analysis of Outcomes Based on Launch Date


We employed a pivot table, filtered by the category "theater," to visualize the numbers of theater-related Kickstarter campaigns according to their success and the month in which they were created. Only campaigns that had ended were included in this visualization (i.e., we did not include campaigns that were still ongoing). 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/100863488/156617944-81925f5f-a2df-4291-bb30-b44d1c810e67.png)



### Analysis of Outcomes Based on Goals

We employed a pivot table to visualize the percentage of total projects according to the dollar amount of their goal and the success or failure of their outcome. The dollar amounts of the goals were subdivided into $5,000 increments up to $50,000, with two exceptions: the first category included campaigns with goals under $1,000, and the next category between $1,000 and $4,999; the last category included all campaigns with goals above $50,000. 

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/100863488/156617890-33e0abac-2a05-43ac-9c03-273108ae3c2e.png)



### Challenges and Difficulties Encountered

The analysis presented few challenges. The data was generally clean and error-free, and it did not require significant cleaning. A few adjustments were made in order to facilitate analysis (e.g., separating the "parent category" and "subcategory" into two separate columns; translating Unix timestamps into traditional date formats). Additional formula-based columns were created to facilitate data analysis: Subcategory, Percentage Funded, Average Donation, Date Created (conversion from Unix timestamps), Date Ended (conversion from Unix timestamps), Years (of creation date).

However, the limitations of the dataset mean that we cannot infer causation from the trends that we may observe. Please see the discussion of the limitations of the dataset below.


## Results

- **What are two conclusions you can draw about the Outcomes based on Launch Date?**

From this visualization we can identify several trends: 

1. The number of theater campaigns that were canceled remained steady and very low regardless of the month in which the campaign was created.
2. The total number of theater campaigns appears to peak three times during the year: in February, May, and October. The May peak is significantly higher than the February and October peaks, and May has a higher total of created campaigns than any other month.
3. The number of successful theater campaigns is higher than the number of failed campaigns in every month, and most significantly in May and June, where the number of successful campaigns is more than double the number of failed campaigns (111 to 52 and 100 to 49, respectively). The month of December had the fewest successful campaigns, especially relative to the number of failed campaigns in December (37 to 35).

- **What can you conclude about the Outcomes based on Goals?**

From this visualization we can identify some trends: 

1. Campaigns with lower goals (less than $20,000) tended to be more successful than campaigns with higher dollar amounts. The exception is of campaigns between $35,000 and $44,999, where more campaigns were successful than not.
2. Campaigns with the highest goal amounts ($45,000 and above) overwhelmingly failed to meet their goals.

- **What are some limitations of this dataset?**

The data does serve to identify some trends regarding timing and goal amounts and the success of a campaign. However, the dataset offers little information as to **why** any conclusions may be valid, and this may make it difficult to reproduce the success of successful campaigns. There may be additional context affecting these factors not included here. For example, we do not know:

1. What advertising or media presence these campaigns may have had that may have influenced their success. We also do not know the size of the platforms or media markets associated with each campaign.
2. Whether the campaigns were associated with already-existing entities which may have had mailing lists, etc. to draw from.
3. Whether the dataset is complete for this timeframe (i.e, whether all campaigns on the Kickstarter platform from this timeframe are included here). Since we did not participate in the creation of the original Excel sheet, we cannot speak to the limitations of the program that exported this data, the filters that may have been used, or potential user error in creating a complete dataset. 
4. Whether more recent data would reveal other trends. The most recent campaign included in this dataset is from 2017. 


- **What are some other possible tables and/or graphs that we could create?**

Due to the size of the dataset we could create many additional analyses, including:

1. Success/failure relative to whether a campaign was "spotlighted" (e.g., a table showing counts of spotlighted campaigns with columns indicating success and failed)
2. Success/failure relative to country of origin (e.g., a table with rows showing countries and columns indicating success or failure; values would consist of counts of projects successful or failed)
3. Average donation relative to country of origin
4. Number of backers relative to category/subcategory and success/failure
5. Which categories and subcategories were more likely to succeed or fail to meet their goals
