# Inflation Report: 1998-2022
Hello ! Nice to see you here. Read the qoute below !

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

## Well, now lets move to technical parts.
### Used tools: **Excel Power Query, Pivot tables, Pivot charts.**
All the stages of the are discussed below step by step.
### 1. Data Collection and Extraction.
#### Dataset 1: 
Data set 1 contains annual GDP growth rate of all the countries from 1960 to 2021. This data set is collected from [The World Bank Data:GDP Growth](https://data.worldbank.org/indicator/NY.GDP.MKTP.KD.ZG).

#### Dataset 2:
Data set 2 contains annual inflation rate in all the countries of the world. It is donwloaded from [The World Bank Data: Inflation](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG).

#### Dataset 3: 
This data set contains the total GDP of G20 countris in 2021. This dataset is extracted using **Excel Power Query** from the website [Trading Economics: GDP G20 2021](https://tradingeconomics.com/country-list/gdp?continent=g20).

#### Data set 4:
This dataset contains the inflation of G20 countries in 2022. It is extracted using **Excel Power Query** from the website [Trading Economics Inflation G20 2022](https://tradingeconomics.com/country-list/inflation-rate?continent=g20).

Both dataset 3 and Dataset 4 is extracted in the same [excel file](https://github.com/shakhscode/Inflation_Report-1993-2022/blob/main/GDPandRecent.xlsx)


> To extract data from websites using **Excel Power Query**:
- Go to **Data** tab in excel. Then select **New Query > From Other Sources > From web**.
- Enter the link of the website and click 'Ok' and then extract the data as required.

After extracting they are merged using **Excel Power Query**.
> To merge(join) two tables from the same workbook using Power Query 
- Go to **Data> New Query > Combine Queries > Merge**.

### 2. Data cleaning 
Dataset 3 and 4 are already in clean format. But dataset 1 and 2 are messy and not cleaned.

The raw data looks like this.
![Uncleaned Dataset]()
Now its time to clean dataset 1 and dataset 2.
- Open a blank excel workbook. Go to **Data > New Query > From File > From Excel Workbook** and open the raw dataset.
- Using Power Query editor dataset is cleaned and only data for G20 countries from year 1998 to 2021 are loaded.
- Similarly clean the data set 2 and load in the same [excel workbook]

![Queries for data cleaning]
![Cleaned dataset]
### 3. Forecasting and other calculations.
In order to compare the expected inflation and real inflation in 2022, a time series forecasting is carried out using the Excel formula
```
FORECAST.ETS(target_date, values, timeline, [seasonality], [data_completion], [aggregation])
```
Other caculations include 'Average GDP growth rate and average inflation rate.

### 4. Data transformation and final join.
- Using Power Query 'Unpivot columns' option GDP data and inflation data are unpivoted and transformed separately in the same workbook.
> To unpivot a table first select the table and then go to **Data> From Table** then selects the columns to unpivot.
- Now 'RecentGDP_Inflation.xlxs' file is  loaded to the same workbook. 
- Now all the unpivoted tables are merged together and  dataset is ready to visualize.

### 5. Designing the dashboard.
