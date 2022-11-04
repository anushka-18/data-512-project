# Data 512 Project Part 1 - Common Analysis 
## Analysis of COVID-19 Cases in Monroe, NY

### Motivation 
This project aims at analysing the rate of infection of COVID-19 in Monroe County, NY, over a period of February 2020 to October 2021. Through this, we try to understand how the number of COVID cases changes in this county, the effect and periods of mask mandate, and possible future outcomes.

### Datasets
We use the following datasets:
* [U.S. State and Territorial Public Mask Mandates From April 10, 2020 through August 15, 2021 by County by Day](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i) - The CDC dataset of masking mandates by county.
* [COVID-19 data from John Hopkins University](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv) - The RAW_us_confirmed_cases.csv file from the Kaggle repository of John Hopkins University COVID-19 data. This data is updated daily. 
* [Mask-Wearing Survey Data](https://github.com/nytimes/covid-19-data/tree/master/mask-use) - The New York Times mask compliance survey data where participants indicated their mask usage

### Repository Structure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.
├── Analysis-COVID-Cases-Monroe.ipynb
├── README.md
├── LICENSE
├── data
│   ├── RAW_us_confirmed_cases.csv
│   ├── RAW_us_deaths.csv
│   └── mask-use-by-county.csv
├── Reflection on Collaboration.pdf
├── Visualization Explanation.pdf
├── images
│   ├── Derivative of Rate of Infection Method 2.png
│   ├── Effect of masking policies on rate of infection.png
│   ├── Effect of masking policies on rate of infection second method.png
│   └── intermediate visualizations and EDA
│       ├── Daily Active Cases.png
│       ├── Daily death rate time series.png
│       ├── Daily total death count.png
│       └── Derivative of rate of infection.png

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
### Intermediary Visualizations

* **Daily Active Cases.png** - This shows the total active cases in a day and the mask policy in effect on the particular day
* **Daily death rate time series.png** - This shows the daily death rate (calculated by taking the gradient change in number of deaths per day) and the mask policy in effect on the particular day
* **Daily total death count.png** - This shows the daily death count and the mask policy in effect on the particular day
* **Derivative of rate of infection.png** - This shows the change in rate of infection from a day to day basis plotted along with he mask policy in effect on the particular day coded by colour


### Final visualizations 

* **Effect of masking policies on rate of infection.png**
![image](https://user-images.githubusercontent.com/40142355/199908484-155e6625-4be8-40d4-914b-8b898791c717.png)

This plot shows the rate of infection of COVID-19 in Monroe County from February 2020 to October 2021 while indicating the masking policy that was in effect at the time. The x-axis shows the time progression and is labelled with months over this period, and the y-axis shows the change in daily confirmed cases.

* **Derivative of Rate of Infection Method 2.png**
![image](https://user-images.githubusercontent.com/40142355/199908652-b595b3cf-875c-4bf0-be73-21820924417b.png)

This plot shows the derivative of rate of infection. It is calculated on a weekly basis (by taking the difference of 7-day average of new daily cases divided by 7). The x-axis shows the time progression and is labelled with months over this period, and the y-axis shows the change in rate of infection in a week.

### Inferences
* While arriving at a direct impact of masking policies on the rate of infection is difficult, it is clear to see that the masking mandate was removed after a significant drop in cases, and the cases began to rise once again after the mandate was removed.
* There are several change points in the rate of infection graph - these do overlap with the beginning and the end of masking mandate, but do not show a clear rise and fall with its implementation.
*	There is a lot of variation in the rate of infection – this cannot be attributed to masking policies alone. There have to be other stronger factors at play here which include vaccinations, natural immunity after first infection, increase or decrease in testing.
*	There is no one method of calculating the rate of infection – it can be calculated in multiple ways – but the broader analysis remains the same.




