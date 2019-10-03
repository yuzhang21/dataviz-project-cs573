
# Data Visualization Project (CS573)
**Refined dataviz-project-templateA-proposal**
A project proposal for US Flu Surveillance Data Review. 

#### History
  1. (09/25) Created template version A with initial sketch materials
  2. (10/02) Refine the proposal with defined components, tasks, interaction details and schedule 

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
  *In time series chart, 5 lines with different colors are displayed indicating the average values on different year, i.e., 2015-2019.
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
1. Choropleths map and legend, color choice (Wk 1)
2. Other charts (Wk 1: 3 days)
a. Different year line chart
b. Top 10 bar chart for aggregation
c. Top 10 line chart for trend
3. Data Preparation, Filtering, Calculation, Grouping (Wk 2,3: 3+1=4 days)
4. Multi-view plot assembly  (Wk 1,2: 1+1=2 days)
5. Interactions among views  (Wk 3,4: 3+4=7 days)
6. Future or additional improvements (N/A)

|Cat. No.|Task No.|Action Item|Estd. Time (day)|Actu. Time (day)|Whether the task is challenging and how|
|:---:|:------:|:------|---:|---:|:-----|
|C1|1|Map - Already show US map by states|0.5|0.5|No|
|C1|2|Display a value using choropleths map|0.5|0.5|No|
|C1|3|Show color bar and legend on map|0.5|0.5|No|
|C2|1|Line chart by years, show correct legend|0.5|0.5|No|
|C2|2|Bar chart to show top 10 states|0.5|0.5|No|
|C2|3|Line chart to show trend for top 10 states|0.5|0.5|No|
|**C2**|**-**|**Total for C1 and C2**|**3.0**|**3.0**|**NA**|
|C3|1|Data loading with multiple files|0.5|0.5|No|
|C3|2|Derived data calculation like ratio|0.5|0.5|No|
|C3|3|Data filtering based on interaction states|1.5|1.5|Yes|
|C3|4|Filtering top 10 states data|1.5|1.5|Yes|
|**C3**|**-**|**Total for C3**|**4.0**|**4.0**|**NA**|
|**C4**|**-**|**Put multiple (4) views together using D3**|**2.0**|**2.0**|**Yes, may need to explore the best way**|
|C5|1|From chart, select a year, update map|0.5|0.5|No|
|C5|2|From map, select a state, update chart|0.5|0.5|No|
|C5|3|Add a menu, select different data field|0.5|0.5|No|
|C5|4|Add a button, reset data to all years|0.5|0.5|No|
|C5|5|From bar chart, select a state, update map|0.5|0.5|No|
|C5|6|From bar chart, deselect any state, show top 10 states|0.5|0.5|No|
|C5|7|From trend chart, select a year, update map for top 10 states and give year|1.5|1.5|Yes|
|C5|8|From trend chart, deselect any year, update map for top 10 states for all years|1.5|1.5|Yes|
|C5|9|Show tooltip when mouse hover lines, bars, or state on maps|1.0|1.0|No|
|**C5**|**-**|**Total for C5**|**7.0**|**7.0**|**NA**|
|C6|1|There are some more interactions can be defined, or blocked in this project|0.0|0.0|No|
|C6|2|Expand one plot to the whole canvas and hide the rest. And toggle to bring back original views. |0.0|0.0|No|
|C6|3|The flu season is centered in winter, so it would be really nice if the cycle starts from the week 40 and ends on week 39 in the next year. Should be easy to shift the data but need to worry about the legend changes which may not be trivial to do. So far the plot matches calendar year which is also useful.|0.0|0.0|No|
|**C7**|**-**|**Total for all**|**16.0**|**16.0**|**NA**|


