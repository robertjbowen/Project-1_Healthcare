# Health Care Analysis - COVID-19 Pandemic U.S. and Chicago, IL
# 30 October 2020

## Project Group:

- Michelle Bannon
- Robert Bowen
- Hema Sankaran 
- Sydney Williams

## Project Design

The objective of the project is to gather and analyze health care data related to the COVID 19 pandemic. The research will look at data for the entire United States, and then focus in on the city of Chicago, Illinois. The team will pull from various data sources and look at COVID 19 severity, hospitalization, and mortality versus various factors to assess correlation.

### Factors Considered: 

1. Age
2. Gender
3. Race
4. Complicating Risk Factors

***
Introduction of Analysis from Briefing Goes Here
#Data Sources:

(Data availability will influence scope and factor selection)

Potential data sources

Data.CDC.gov

covidcaremap.org
US Hospital Facility Bed Capacity Map | CovidCareMap

coronavirus-resources.esri.com
Definitive Healthcare: USA Hospital Beds

kaggle.com
Novel Corona Virus 2019 Dataset

***

Hema's Analysis Goes Here

***

Michelle's Analysis Goes Here

***

Sydney's Analysis Goes Here

***

## Chicago Analysis

### Data:
For my analysis I chose to focus specificly on the city of Chicago, IL as it was relevant to the the class population and data was readily available and well organized. For the initial analysis I imported three datawise COVID 19 related datasets from the Chicago Department of Health & Human Services.

1.  Chicago COVID-19 Daily Cases, Deaths, and Hospitalizations - naz8-j4nc
2.  COVID-19 Hospital Capacity Metrics - f3he-c6sv
3.  COVID-19 Daily Testing - By Person - t4hh-4ku9

Each data set can by imported using the following URL and changing the 8-digit identifier for each different set.

URL example - https://data.cityofchicago.org/resource/naz8-j4nc.json 

### Data Cleaning:
We merged the datasets based on "date". The first two weeks of data from 1-13 March 2020 had significant missing data elements. The data is updated daily and runs to the present day, but there is a lag in reporting in most data elements so the last week of the dataset was also unusable. The final cleaned and merged dataset was saved as chicago_data.csv.I used this dataset for all of my analysis calculations.

insert chicago case, hosp death chart

### Data Viewing:
When viewing the raw testing data it it is apparent that availability/ utilization of weekend and holiday testing is much lower or the resuts are not tabulated until the following workday with creates a significant "saw-tooth" effect which carries over to the daily COVID-19 positivity results. To improve the appearance of the data I created a copy of the dataset with all values transformed to a 7-day rolling average. I named this data file rolling_AVG.csv. This data set was only used for display purposes.

insert Covid testing over time chart


## Chicago Total Population Analysis:

For this analysis we wanted to investigate the changes in the rates of infection, hospitalization and death from COVID-19 in Chicago. This will tell us if the testing, mitigation, and protective measures we put in place are having an effect and if changes in treatment are lowering the severity of the illness.


### Positivity Rate = # of positive cases / # of tests administered 

- This is the metric used by most governments, including the State of Illinois to determine whether to impose or lift restrictions and prohibitions. The State of Illinois uses a standard of less than 6.5% Positivty as the benchmark. Positivity Rate is not a measure of the health of the population but epidemiologists use it as a metric to determine if a large enough sample of the population is being tested to give them a confidence that the infection is being contained. At the beginning of this analysis the positivity rate across the country began climbing as can be seen in the data and propted the state of Illinois to reimpose restrictions on bars, restaurants and other businesses in an effort to reverse the trend.


### Hospitalization Rate = # Hospitalized / # of positive cases
### Case Mortality Rate = # Deaths / # of positive cases

- These metrics look at the population of infected cases and measures the ratio of cases with symptoms severe enough to warrant hospitalization or result in death. Due to shortages of test kits and other resources early in the pandemic, only individuals with clear symptoms or who were already hospitalized were tested. Previous fatalities were reviewed for evidence of COVID 19 as well. This skewed the positivity, hospitalization, and death rates in the beginning months. Over time as knowledge of the infection and treatment developed, the rates of death and hospitalization went down even as the numbers of positive cases went down. For the past 4 months, the hospitalization and case mortality rates have remained relatively low and constant. In the next few weeks the recent uptick in the positivity rate may begin to impact the hospitalization and mortality rates but so far they have continued to remain flat or even decline.

insert Chicago rates 7-day rolling average chart

A box and whisker cart along with an Analysis of Variance (ANOVA) test of COVID 19 Deaths by months shows a significant statistical difference between the first 4 months and the sencond four months. 

insert box chart 


## Chicago Female Versus Male Populations Analysis:

For this analysis we wanted to investigate the difference in the rates of testing, infection, hospitalization and death from COVID-19 between females and males in Chicago. This will tell us if gender plays a role in how the virus is impacting the population. The same analysis as used on the total population was repeated for each gender population. 

insert mvf 7-day rolling average chart

### Positivity, Hospitalization, and Death Rates
Overall the trends for each population track ed very closely to one another over time and their overall rates are within 1-2 percentage points of each other.  

insert mvf rate chart

### T-test Analysis 
Running an independent T-test of the two populations revealed that Females are being tested for COVID-19 at a greater rate than men, but the probability of having a positive test result and subsequent hospitalization are within a 95% statistical confidence level of being the same for both populations while Males have a higher statistical probability of dying from the infection.

insert T-test charts

***



