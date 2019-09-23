
# Data Visualization Project (CS573)
#dataviz-project-templateA-proposal
A project template version A with initial proposals for US Flu Surveillance Data Review. 

## Data

The data I propose to visualize for my project is a multi-year flu patient visits data collected by healthcare providers across the United States, who participated in the Influenza-like Illness Surveillance Network (ILINet). 
[Weely U.S. Influenza Surveillance Reports](https://www.cdc.gov/flu/weekly/index.htm#ILIMap) are generated from the ILINet Program, which presents an [interactive FluView visualization](https://gis.cdc.gov/grasp/fluview/fluportaldashboard.html) of the data. 
In this proposal, I am going to present the data with more visualizations in order to best answer the questions about the data. 

## Prototypes

I have created an overview of this data using color and sized dots, given the higher total visits corresponding to bigger circle size for each data point. It shows a clear pattern of peaks with big circle sizes in Feburary and December period for multiple-years of data. 

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
*

## Sketches

I created the following 3 sketches to illustrate the design of the visualization. 


## Open Questions

So far I am working on visualizting the data on the map and allow more complex logics to calculate the derived data to be visualized. D3 and React seems to be powerful tools that can achieve all of them but I need to learn those details to put things together. 

Next step after data visualization is going to be the interaction of the interface. Some more calculations need to be triggered and to update the corresponding visualization. 
