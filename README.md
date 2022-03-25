# Kickstarter_Analysis


## **Overview of Project**
This work was requested by a playwrite seeking funding for a play they were attempting to produce. This analysis leverages kickstarter data to assess the outcomes of various plays based on launch date and funding goals to better understand how these attributes play in to the success or failure of the project. 
### **Purpose**
The purpose of this analysis is to display the interactions between the year in which a project was launched and the liklihood of its success in funding. Additionally, the project analyzes different buckets of funding levels to understand the interactions of total dollars sought compared to overall success rate. 
## **Analysis and Challenges**
Leveraging excel formulas and pivot tables I was able to perform an analysis on launch date and funding goals. Below I outline what tools I leaveraged for each section and challanges I saw with each analysis 
### Analysis of Outcomes Based on Launch Date
In order to perform an analysis of the interaction of the launch date variable and amount of successful projects I first created a Pivot table from the total Kickstarter data that fitered out all subcategories that were not "Theater" then matrixed the data for each combination of month and outcome of funding: 

![image](https://github.com/mmilner3/Kickstarter_Analysis/blob/main/Resources/PT%201.PNG)

One challange I saw with this portion was that my version of excel wanted to create additional buckets for the year the project was launched. I had to go in to my pivot table fields and remove these auto created buckets. 

Once i had the data filtered i charted the data out in a line grahph to show each outcome and its assosiated amount of projects for each month. 

![Image](https://github.com/mmilner3/Kickstarter_Analysis/blob/main/Resources/Outcomes_vs_Goals.png)

### Analysis of Outcomes Based on Goals
To look at the interaction of funding goal and funding success I had to leverage countifs formulas to bucket each project in to a bin for use in data visualization. please see an example of these countifs below: 

     =COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,">=1000",Kickstarter!$D:$D,"<=4999",Kickstarter!$R:$R,"plays")

### Challenges and Difficulties Encountered
During this analysis i saw two challanges that i had to overcome-- one with each analysis:
##### **Challange with Pivot Tables**

During the building of my pivot tables my verison of Excel wanted to automatically add other buckets that fit the data within for year of launch. in order to get the table to look the correct way i had to be sure to remove this automatic bucketing by dragging them out of the pivot table set up fields.


##### **Challange with Countifs**
When it came to the countifs formula i wanted to make sure i had every observation accounted for based on manual sorting of the table. it was a challange to make sure i was building the formula to be inclusive of all numbers in the goal fields. after tinkering with the formulas for a while i was able to ensure all observatiosn were accounted for. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

    1. May is the best time of year to launch a play

    2. plays launched in december have an almost equal likihood of success and failure. 

- What can you conclude about the Outcomes based on Goals?
    1. Plays that ask for less than $5000 or between $35000 and $44999 have the greatest liklihood of success 

- What are some limitations of this dataset?

    This is a reletivetly small data set for what we want to analyze. with only 1047 observations for plays we will see a higher reflection of trends in this data that may not be representative of the popluation.

    This data set breaks out the information by country but not by smaller sections such as region or city. This sacrifices some pertainaint information as some projects funded in parts of countries may not be on the same playing field as others.  


- What are some other possible tables and/or graphs that we could create?
    * Outcome based on if the play was a staff pick 
    * Number of backers based on country 
    * Average backers based on Parent Category 
