Datasets used

County-level socioeconomic features
https://github.com/JieYingWu/COVID-19_US_County-level_Summaries/blob/master/data/counties.csv

JHU Time Series confirmed deaths
https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_US.csv

NYC Covid Data Time Series  
https://github.com/nychealth/coronavirus-data/blob/master/boro/boroughs-case-hosp-death.csv


This project attempts to use county-level socioeconomic data, paired with
county-level cumultative COVID-19 confirmed death time-series' to forecast
future county-level cumulative death counts. Although the original aim of this
project was to forecast the death count for multiple days in the future, the
resulting model only predicts one day into the future. However, the resulting
performance of this model is very good. To evaluate the performace of the model,
the R^2, MAE and RMSE are reported.

The final model uses time-series data along with a few static socioeconomic
variables, most importantly population density, to predict cumulative death
counts one day into the future for all counties with at least one registered
confirmed death due to COVID-19. The model is a simple OLS regression that
uses county-level socioeconomic data and death counts of previous days:
Days since March 14 (an arbitrary start date for the death time-series'), Death
count 1 day ago, Death count 2 days ago, Death count 3 days ago, and Death count
4 days ago. The resulting model performance is much better with this additional
data than using only socioeconomic data.  

**Final_Report** shows the data extraction and cleaning along with the best EDA 
and the best performing model. Refer to this notebook to receive a full rundown 
of the project from start to finish.

**DataPrep_EDA** shows all EDA performed.  

**Modeling** shows all tested models.  

**DataPrep_EDA_draft** and **Modeling_2** are notebooks used for testing and exploring ideas.  

**Final_Report_Original** is the original version of the results. The datasets in the 'data' directory  
can be used by Final_Report, however they were last updated May 6th.  