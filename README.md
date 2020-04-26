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
* knn, random forest regression, and logistic regression performed on selected variables.   
* accuracy scores are low, but slightly better in deaths prediction (~ 25-30% in all three models). Cases showed 2-3% accuracy. In either case, Knn performed best.     

## 3. Refining features
* since population related variables have high scores in importance, we decided to try modeling without such related variables to see if the model would perform better. 


## 4. Ensemble Learning Model
* created a voting classifier with knn, random forest, and logistic regression using the deaths model. The voting classifier did perform better. But accuracy is still low, thus these variables are not great predictors for cases/deaths. 


## 5. Future Steps
* maybe use graphical models to test for confounding factors