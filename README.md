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
Link to Presentation: https://docs.google.com/presentation/d/1WZ_C9_m_zsvUAcY7eJCIjkzEN12qB_KzJiu4WtmJOsg/edit?usp=sharing
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
Datasets used : 
https://catalog.data.gov/dataset/conditions-contributing-to-deaths-involving-coronavirus-disease-2019-covid-19-by-age-group-7ee07
https://covid19.who.int/?gclid=Cj0KCQjwlvT8BRDeARIsAACRFiXRQTh6KPvvoyRnHRADbqEQmjmoHkUJsBwZJhVMfodvDyJ1tw_SsJ8aAnClEALw_wcB

Here is a comparison of mortality due to COVID in the World countries and US cities
![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/World-wide%20Cases%20Vs.%20Deaths.png)
![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/US%20Cases%20Vs.%20Deaths.png)
ANOVA of death grouped by a set of 7 underlying respiratory conditions.
This analysis is done using 'Cause of death in the US population observed in samples between the Feb 1 2020 to Oct 25 2020'.
Question:
Are existing respiratory conditions significant contributor to COVID mortality ? 

Note: In this ANOVA, 'conditions' is the independent variable. We  consider 7 conditions including COVID.
Our sample sizes are the app. same, i.e. the number of observations with each of the conditions are the app. same.

General ANOVA Hypotheses:

Null hypotheses: (Groups means are equal (no variation in means of groups))
RespiratoryConditions == RespiratoryCondition 
Existing respiratory conditions equally affect survival of patient upon getting affected with COVID

Alternative hypotheses: At least, one group mean is different from other groups
RespiratoryCondition =/= RespiratoryCondition 
Atleast one Existing respiratory condition might affect the patient fatally

One-way (one factor) ANOVA with Python results: 
F_onewayResult(statistic=10.800911913621759, pvalue=6.4228242186118545e-12)
After the analysis, we conclude that the results are statistically significant.)
Further analysis might be able to prove if some COVID deaths are misleadingly categorized as Influenza and Pneumonia or respiratory failures
![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/Number%20of%20COVID%20deaths%20by%20Condition.png)


Michelle's Analysis Goes Here
Coronavirus Impact on the Women and Men of Chicago
As I began to explore Chicago data I wanted to know how many male vs female deaths were from COVID; 58.7% which I found interesting since per Robs analysis, more females get tested but more males die from it.
Output/COVID Deaths by Gender.JPG 
Project-1_Healthcare/Output/COVID Deaths by Gender.JPG 

 

Coronavirus Impact on Ethnic Backgrounds in Chicago
Next, I looked at number of deaths by race for the Chicago data. Blacks died at a much higher rate than whites and Latino were also very high.  Further analysis would be needed to understand why?  Is there a higher population of black people or is there some other underlying reason? 
Project-1_Healthcare/Output/Comparision of Covid Deaths by Race.jpg
 
 


Coronavirus Impact on Different Age Groups in Chicago
Project-1_Healthcare/Output/Comparison of COVID Cases by Age Group.png

 
Project-1_Healthcare/Output/Comparision of Covid Deaths to Hospitalizations by Age Group.JPG

 


Coronavirus Impact on Different Age Groups in Chicago
When I first charted all cases by age group, I didn’t like how this looked so I wanted to see which age groups had the most cases.  I split it out the age groups. 

Coronavirus Impact on Different Age Groups in Chicago
Here are all the charts split out by highest cases.  I kept the y axis max limit the same so you can clearly see the distinction and so that I did not distort or mis represent the data.
 
Finally, I looked at the total cases for Chicago.  Coronavirus Impact on Chicago in 2020
 



## US Utilization of Hosiptal Beds Analysis
For my analysis I chose to focus on the utlilzation of hosiptal beds in the United States Pre COVID19 pandemic and current COVID-19 pandemic. For my initial analysis I imported the Pre COVID19 bed dataset, provided by kaggle. Then later improted current COVID19 dataset, provided by the CDC.

URL for pre pandemic - https://www.kaggle.com/ikiulian/global-hospital-beds-capacity-for-covid19

URL for current - https://www.cdc.gov/nhsn/covid19/report-patient-impact.html#anchor_1587406852

### Data:
Pre-COVID19 Bed Data
Import Dependencies
Import US Pre Pandemic Bed Data File
Create a bar chart to see the Number of ICU Beds & Bed Utilization in the United States


![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/WilliamsPicture1.png)
Note:This graph is showing the utilization of hosiptal beds in the United States pre covid-19

Current COVID19 Current Data
Import Dependencies
Import CDC Pandemic Data File

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/WilliamsPicture2.png)

Note:This graph will look at the number of patients in an inpatient care location who have suspected or confirmed COVID-19, percent estimate (percent of inpatient beds)

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/WilliamsPicture3.png)

Note:This graph will look at hospitals inpatient beds availability, a rough estimate

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/WilliamsPicture4.png)

Note:This graph will look at hospitals ICU beds availability, a rough estimate

Question: ICU Bed Capacity has an impact on COVID deaths?

Null Hypothesis: If deaths are correlated to bed capcity, then there will be no positive correlation.

Alternative Hypothesis: If deaths are correlatd to bed capcity, then there will be a strong negative correlation.


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

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture1.png) 

### Data Viewing:
When viewing the raw testing data it it is apparent that availability/ utilization of weekend and holiday testing is much lower or the resuts are not tabulated until the following workday with creates a significant "saw-tooth" effect which carries over to the daily COVID-19 positivity results. To improve the appearance of the data I created a copy of the dataset with all values transformed to a 7-day rolling average. I named this data file rolling_AVG.csv. This data set was only used for display purposes.

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture2.png)


## Chicago Total Population Analysis:

For this analysis we wanted to investigate the changes in the rates of infection, hospitalization and death from COVID-19 in Chicago. This will tell us if the testing, mitigation, and protective measures we put in place are having an effect and if changes in treatment are lowering the severity of the illness.


### Positivity Rate = # of positive cases / # of tests administered 

- This is the metric used by most governments, including the State of Illinois to determine whether to impose or lift restrictions and prohibitions. The State of Illinois uses a standard of less than 6.5% Positivty as the benchmark. Positivity Rate is not a measure of the health of the population but epidemiologists use it as a metric to determine if a large enough sample of the population is being tested to give them a confidence that the infection is being contained. At the beginning of this analysis the positivity rate across the country began climbing as can be seen in the data and propted the state of Illinois to reimpose restrictions on bars, restaurants and other businesses in an effort to reverse the trend.


### Hospitalization Rate = # Hospitalized / # of positive cases
### Case Mortality Rate = # Deaths / # of positive cases

- These metrics look at the population of infected cases and measures the ratio of cases with symptoms severe enough to warrant hospitalization or result in death. Due to shortages of test kits and other resources early in the pandemic, only individuals with clear symptoms or who were already hospitalized were tested. Previous fatalities were reviewed for evidence of COVID 19 as well. This skewed the positivity, hospitalization, and death rates in the beginning months. Over time as knowledge of the infection and treatment developed, the rates of death and hospitalization went down even as the numbers of positive cases went down. For the past 4 months, the hospitalization and case mortality rates have remained relatively low and constant. In the next few weeks the recent uptick in the positivity rate may begin to impact the hospitalization and mortality rates but so far they have continued to remain flat or even decline.

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture3.png)

A box and whisker cart along with an Analysis of Variance (ANOVA) test of COVID 19 Deaths by months shows a significant statistical difference between the first 4 months and the sencond four months. 

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture4.png) 


## Chicago Female Versus Male Populations Analysis:

For this analysis we wanted to investigate the difference in the rates of testing, infection, hospitalization and death from COVID-19 between females and males in Chicago. This will tell us if gender plays a role in how the virus is impacting the population. The same analysis as used on the total population was repeated for each gender population. 

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture5.png)

### Positivity, Hospitalization, and Death Rates
Overall the trends for each population track ed very closely to one another over time and their overall rates are within 1-2 percentage points of each other.  

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture6.png)

### T-test Analysis 
Running an independent T-test of the two populations revealed that Females are being tested for COVID-19 at a greater rate than men, but the probability of having a positive test result and subsequent hospitalization are within a 95% statistical confidence level of being the same for both populations while Males have a higher statistical probability of dying from the infection.

![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture7.png) 
***
![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture8.png)
***
![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture9.png) 
***
![alt tag](https://github.com/hema2575/Project-1_Healthcare/blob/main/images/BowenPicture10.png)
***



