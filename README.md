# Machine learning methods for county and state level healthcare capacity data in relation to COVID-19 cases 

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
* Feature importance from sklearn RandomForest was performed to select top significant variables. Top 5 important features were selected.      


## 2.  Model Prediction
* linear regression, lasso regression, random forest regression, and gradient boosting regression are performed on selected variables for predicted deaths across counties in the US.    

## 3. Clustering
*    

## 4. Future Steps 
* maybe use graphical models to test for confounding factors, latent variables    
