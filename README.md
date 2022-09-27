# Inflation Report: 1993-2022
Hello ! Nice to see you here. Read the qoute below !

![](https://github.com/shakhscode/Inflation_Report-1993-2022/blob/main/extraimagefiles/inflation2.jpg)

Did you know this before ?
You may beleive these or not, but you can't deny that all countries are facing economic consequences due to high inflation in 2022. Well, as I studied two major reason for high inflation all over the world in 2022 are - 
- Covid 19 pandemic.
- Russia vs. Ukraine war.

The second reason affected me badly (that's my personal story, how I survived in Russia). 

So, as a normal consumer and  **as a data analyst** I decided to make a report on inflation of world's leading countries by GDP share. I gathered some data and now want to make a report to see the inflation in top 20 countries from 1993 to 2022.

Below is the final report. See the interactive dashboard in Tableau Public.

after image

This dashboard basically shows the following insights
- 
- Inflation of a selected country from 1993 to 2021.
- Inflation of G20 countries in a selected year. 
- Recent inflation of a country in 2022. Is it higher than all time average ? Is it higher than expected ? 
- Countries having higher inflation than expected. 

**Note: The inflation data shows % of annual inflation in CPI(Consumer price index)**

## Well, now lets move to technical reports- how I did it?
The project is completed in 4 steps using 
- **Excel Power Query** - for data extraction and cleaning.
- **Python and Pandas** - for data transformation.
- **Tableau Desktop** - for designing the dashboard.

Let's discuss the processes step by step.
### 1. Data extraction and cleaning.
### Data extraction
- The 1st dataset is extracted from [Trading Economics, GDP of G20 Countries:2021](https://tradingeconomics.com/country-list/gdp?continent=g20)
- The 2nd data set used for this report is collected from [The World Bank Data](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG?end=2021&start=1960&view=chart) which contains the data of inflation for all countries from 1960 to 2021.
- The second data
- The 3rd dataset that contains % of inflation in 2022 (till August 2022) of G20 world's countries. The data set is extracted from [Trading Economics Recent inflation dataset](https://tradingeconomics.com/country-list/inflation-rate)
- The 1st and 3rd dataset is extracted using Excel Power Query. To extract data using Excel power query
```
Step 1: Go to Data tab > New Query> From Other Sources> From web
Step 2: Enter the url of the website and Excel will extract live data from the website.
```
### Data Cleaning. 
- The 2nd dataset contains some null values for some years and for some countries all values are null. So rows and columns are filtered not to select null column or row using **Power Query Editor**.
- In the report we need to visualize inflation of G20 countries and only for the years 1993 to 2021. So only useful columns and rows are selected using **Power Query Editor**
Now our dataset is ready.
- 1st and 3rd dataset is already cleaned and well formated, so we don't need to anything to them.
### 2. Data Transformation.
### 3. Time Series forecasting.
### 4. Dashboarding.
