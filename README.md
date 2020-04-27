# BINF_final

## Data Sources:
USDA Rural-Urban Continuum Codes    
https://www.ers.usda.gov/data-products/rural-urban-continuum-codes.aspx   
US census income and poverty data   
https://www.census.gov/data/tables/2019/demo/income-poverty/p60-266.html   
Covid-19 health system capacity   
https://github.com/covidcaremap/covid19-healthsystemcapacity/tree/master/data       
NY times covid-19 cases/deaths count   
https://github.com/nytimes/covid-19-data      
There are some reported cases/deaths in unknown/unavailable counties areas.


## 1. Feature Selection   
* Stepwise selection and feature importance from sklearn RandomForest was performed to select top significant variables. Feature importance showed better results, so we selected top 5 important features from cases and deaths separately.      

Cases: all_bed_occupancy_rate, peopleinpoverty2018, population_65, medianhouseholdincome, icu_bed_occupancy_rate   

Deaths: population_20, icu_bed_occupancy, population, population_65, all_bed_occupancy_rate.    

## 2.  Model Prediction
* random forest regression, logistic regression, and gradient boosting regression performed on selected variables.   


## 3. Refining features
* since population related variables have high scores in importance, we decided to try modeling without such related variables to see if the model would perform better. 


## 4. Future Steps
* maybe use graphical models to test for confounding factors