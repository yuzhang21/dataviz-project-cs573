
# Data Visualization Project (CS573)
**Refined dataviz-project-templateA-proposal**
A project proposal for US Flu Surveillance Data Review. 

#### History
  1. (09/25) Created template version A with initial sketch materials
  2. (10/02) Refine the proposal with defined components, tasks, interaction details and schedule 
  3. (10/09) Update progress for first week at 1/4.
  4. (10/17) Update progress for second week at 2/4.
  5. (10/23) Update progress for third week at 3/4.
  6. (10/29) Update progress for third week at 4/4.
  
## Data

The data I propose to visualize for this project is a multi-year flu patient visits data collected by healthcare providers across the United States, who participated in the Influenza-like Illness Surveillance Network (ILINet). 
[Weekly U.S. Influenza Surveillance Reports](https://www.cdc.gov/flu/weekly/index.htm#ILIMap) are generated from the ILINet Program, which presents an [interactive FluView visualization](https://gis.cdc.gov/grasp/fluview/fluportaldashboard.html) of the data. 
In this proposal, I am going to present the data with more visualizations in order to answer the questions about the data better. 

## Prototypes

I have created an overview of this data using color and sized dots, given the higher total visits corresponding to bigger circle size for each data point. It shows a clear pattern of peaks with big circle sizes in February and December period for multiple-years of data. 

[![image](https://user-images.githubusercontent.com/26355743/65399943-6d932d80-dd8d-11e9-9db8-9b305f729e50.png)](https://beta.vizhub.com/yuzhang21/53e4bb9a916a407cba5aa0a72e8ef17d)

Another newer visualization view closer to the target:

[![image](https://user-images.githubusercontent.com/26355743/65400105-6caecb80-dd8e-11e9-8ec5-3a585eadcc13.png)](https://beta.vizhub.com/yuzhang21/fdf81343da5d43878e86c250c01cb146)

## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

* Q1: What are the national illness (flu) weekly pattern from 2015-2019?
* Q2: What are the peak and its duration variations over the years?
* Q3: When and where is the highest illness (flu) ratio state wise from 2015-2019 by week or month, year?
* Q4: Which State has the most illness patient, or ratio?
* Q5: What are the patient to health care professional (HCP) ratio across the states?
* Q6: Can the visualization allow user to narrow down their focus to individual states? 

## Sketches

I created the following three sketches to illustrate the design of the visualization. 

![sketch02-1](https://user-images.githubusercontent.com/26355743/65400710-cf559680-dd91-11e9-829a-76e36d865c51.png)

In this page, two major visuals are proposed. On the left is the time series line plot, the Y-axis can be the national total values or averages over weekly data. On the right side is a US map showing state level of any interesting values as a choropleths map.   

![sketch02-2](https://user-images.githubusercontent.com/26355743/65400712-d2508700-dd91-11e9-9458-d31409d7bf8a.png)

The 2nd page proposes to group states into limited (5-10) groups so that the colors are more distinct. Further statistics base on those groups can be presented as bar charts to answer top 10 or bottom 10 questions. 

![sketch02-3](https://user-images.githubusercontent.com/26355743/65400714-d54b7780-dd91-11e9-81fd-5ce4b7500e47.png)

The 3rd page proposes in the last plot to replace bar chart with line chart to display the trend of top states number changes over time. It helps to understand whether the conditions on those top states are getting better or worse. This page also proposes the interactive elements so that different data can be visualized and more detailed data are presented on demand. 


## Open Questions and Answers Learned

### Technical Issues Addressed or Decisions Made
* So far I am working on visualizing the data on the map and allow more complex logics to calculate the derived data to be visualized. D3 and React seems to be powerful tools that can achieve all of them. I will need to learn more details to put things together. 
* Avoid to use vega-lite and vega-lite-api given they may not be compatible or integrated easily.  

### Remaining Issues to be Addressed
* Next step after data visualization is going to be the interaction of the interface. 
* Some more calculations need to be triggered and to update the corresponding visualization. 

## Interaction List
In this project, the following interactions with user are proposed. Only the first one is explained in details. Others are similar and relatively straight forward to understand. It is critical to maintain the consistency among them, therefore, the implementation could be more complex than the list below. 

 1. From chart, select a year, update map
   + In time series chart, 5 lines with different colors are displayed indicating the average values on different year, i.e., 2015-2019.
If user move the mouse cursor and hover on one of the line, a tooltip will show up to display the year on the line. When user click on the line, only data from that given year is selected/filtered, the map will display a different color for different states to reflect that. The top 10 states will also be calculated again and the bar chart will be updated accordingly. Since the top 10 states are changed, their trend plot will be updated accordingly as well.  
 2. From map, select a state, update chart
 3. Add a menu, select different data field
 4. Add a button, reset data to all years
 5. From bar chart, select a state, update map
 6. From bar chart, deselect any state, show top 10 states
 7. From trend chart, select a year, update map for top 10 states and give year
 8. From trend chart, deselect any year, update map for top 10 states for all years
 9. Show tooltip when mouse hover lines, bars, or state on maps

## Schedule of Deliverables
In the following table, I classify and schedule the tasks into several components and steps. There are total 4 weeks left for the project. Assuming I can work 4 days per week, the total working days are 16. So I can roughly distribute the 5 categories into 4 weeks as the following: 
 1. Choropleths map and legend, color choice (Wk 1)**(Done by Wk 2)**
 2. Other charts (Wk 1: 3 days)**(Done by Wk 2)**
  + a. Different year line chart
  + b. Top 10 bar chart for aggregation
  + c. Top 10 line chart for trend
 3. Data Preparation, Filtering, Calculation, Grouping (Wk 2,3: 3+1=4 days)**(Done by Wk 2)**
 4. Multi-view plot assembly  (Wk 1,2: 1+1=2 days)**(Done by Wk 1)**
 5. Interactions among views  (Wk 3,4: 3+4=7 days) -- Will do mostly in Week 3 and polish in Week 4
 6. Future or additional improvements (N/A)

Later on each week, I captured the activities on each item and added the progress information on each week. 
Some items are done in one shot, but a few challenging ones have changes made for multiple weeks. In the end,
all tasks are done, including a new section of tasks added in the last week's polishing stage. 
The total estimation of time extended from 16.0 days to 19.5 days, and the actual execution time takes about
17.5 days. There is a small discrepancy when calculated by weekly progress. I didn't try to fix it because the
first a few weeks calculation maybe recorded a bit differently. Overall, the following table demonstrated a 
relatively accurate plan estimation and execution time line, with tasks priority adjusted along the way. 


|Cat. No.|Task No.|Action Item|Estd. Time (day)|Actu. Time (day)|Whether the task is challenging and how|
|:---:|:------:|:------|---:|---:|:-----|
|C1|1|Map - Already show US map by states|0.5|**D0.5wk1**|**Done**|
|C1|2|Display a value using choropleths map|0.5|**D0.5wk1**|**Done**|
|C1|3|Show color bar and legend on map|0.5|**D1.5(P0.3wk3)(P1.2wk4)**|Yes,**Done**|
|C2|1|Line chart by years, show correct legend|0.5|**D1.0wk2**|**Done**|
|C2|2|Bar chart to show top 10 states|0.5|**D0.8(P0.3wk1)(P0.5wk2)**|Yes,**Done**|
|C2|3|Line chart to show trend for top 10 states|0.5|**D0.5wk2**|**Done**|
|**C12**|**-**|**Total for C1 and C2**|**3.0**|**T4.8(P1.3wk1)(P2.0wk2)(P0.3wk3)(P1.2wk4)**|**NA**|
|C3|1|Data loading with multiple files|0.2|**D0.2wk1**|**Done**|
|C3|2|Derived data calculation like ratio|0.0|**0.0**|**Dropped**|
|C3|3|Data filtering based on all views|1.5|**D1.5wk2**|**Done**|
|C3|4|Filtering top 10 states data|1.5|**D2.0(P0.3wk1)(P0.7wk2)(P0.2wk3)(P0.8wk4)**|Yes,**Done**|
|**C3**|**-**|**Total for C3**|**3.2**|**D3.7(P0.5wk1)(P2.2wk2)(P0.2wk3)(P0.8wk4)**|**NA**|
|**C4**|**-**|**Put multiple (4) views together using D3**|**2.0**|**D1.5wk1**|**Done**|
|C5|1|From chart, select a year, update map|0.5|**D0.5wk3**|**Done**|
|C5|2|From map, select a state, update chart|0.5|**D0.5wk3**|**Done**|
|C5|3|Add a menu, select different data field|0.5|**T0.5(P0.2wk1)(P0.5wk2)**|**Done**|
|C5|4|Add a button, reset data to all years|0.5|**D0.5wk3**|**Done**|
|C5|5|From bar chart, select a state, update map|0.5|**D0.5wk3**|**Done**|
|C5|6|From bar chart, deselect any state, show top 10 states|0.5|**D0.5wk3**|**Done**|
|C5|7|From trend chart, select a year, update map for top 10 states and give year|1.0|**D1.0(P0.5wk3)(P0.5wk4)**|**Done**|
|C5|8|From trend chart, deselect any year, update map for top 10 states for all years|1.0|**D1.0(P0.5wk3)(P0.5wk4)**|**Done**|
|C5|9|Show tooltip when mouse hover lines, bars, or state on maps|1.0|**D1.0wk3**|**Done**|
|**C5**|**-**|**Total for C5**|**6.0**|**T5.7(P0.2wk1)(P4.5wk3)(P1.0wk4)**|**NA**|
|C6|1|There are some more interactions can be defined, or blocked in this project|0.0|0.0|No|
|C6|2|Expand one plot to the whole canvas and hide the rest. And toggle to bring back original views. |0.0|0.0|No|
|C6|3|The flu season is centered in winter, so it would be really nice if the cycle starts from the week 40 and ends on week 39 in the next year. Should be easy to shift the data but need to worry about the legend changes which may not be trivial to do. So far the plot matches calendar year which is also useful.|0.0|0.0|No|
|C7|1|Used a different project for US map to show Hawaii and Alaska|0.1|**D0.1wk3**|**Done**|
|C7|2|Added a Top N States menu to determine number of top states to show because 10 is too many|0.2|**D0.2wk3**|**Done**|
|C7|3|Need to change circle legends to line shape for line charts|0.2|**D0.2wk4**|**Done**|
|C7|4|Highlight a state by its border color, not using opacity|0.2|**D0.2wk4**|**Done**|
|C7|5|Choose a better color combination for lines and bar charts|0.2|**D0.3wk4**|**Done**|
|C7|6|Bug fix: When click or hover on the map, the state must be in the top list. Otherwise, no change.|0.3|**D0.5wk4**|**Done**|
|C7|7|Bug fix: Highlight bar chart malfunctions due to render order.|0.3|**D0.3wk4**|**Done**|
|**C7**|**-**|**Total for C7**|**1.5**|**T1.8(P0.3wk3)(P1.5wk4)**|**NA**|
|**C8**|**-**|**Total for all**|**19.5**|**Total Time:17.5(3.5wk1)(4.7wk2)(5.3wk3)(4.5wk4)Total by week:18.0**|**NA**|

## Major Visualization Output Of The Project


## Future Improvement On The Project
Some items from the above schedule table and a few more task worth to do are listed below:
1. There are some more interactions can be defined, or blocked in this project.
The overall interactions among different visual components are satisfactory. They are pretty consistant and no major flaws as concerned before. 

2. Expand one plot to the whole canvas and hide the rest. And toggle to bring back original views. 
This is worth to do because 1/4 of the screen sometimes not enough to see details, especially for the map. But in single view modes, the interactions are not visible. There maybe some logic need to be adjusted accordingly. 

3. The flu season is centered in winter, so it would be really nice if the cycle starts from the week 40 and ends on week 39 in the next year. Should be easy to shift the data but need to worry about the legend changes which may not be trivial to do. So far the plot matches calendar year which is also useful.
It is nice to be able to horizontally shifting the cyclic data. The effects may not be much different. 

4. Derived data calculation like ratio
We may want to add additional information like patient to healthcare provider ratio that can be derived from the original data. That will involve some menu changes. 

5. Add Pan and Zoom capability in the map view
Because the map is relatively small, allow zoom and pan can allow user to review more details. And it can be reset together by the Reset button. 

(The End)

