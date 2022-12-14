# Phone Price Predictor: Project Overview 
* **Objective**<br/>
This project aims to build an optimal classification machine learning model to predict a phone's price range given the phone's features. 
In the context of the competitive mobile phone market, knowing the associations between the features of a phone and its selling price, and being able to accurately predict the phones' selling prices are beneficial.  

* **Walkthrough**
  - Define the question and collect the data
  - Exploratory Data Analysis
  - Data Cleaning 
  - Fit Machine Learning Models & Compare their performances 
  - Hyperparameter Tuning for Final Machine Learning Model

* **Data & Coding Language Used** 
  - Data: collected from various mobile phone companies 
  - Python Version: 3.9
  - Packages : numpy, pandas, matplotlib, seaborn, sklearn
  
### Exploratory Data Analysis 
* The distribution of each numerical feature was checked<br/>
(includes a plot that was stratified by the outcome variable and a plot that was not stratified)<br/>
&#8594; Battery power, pixel resolution width, and ram each seemed to have a clear association with phone price range

<img src = "viz1.png" style = "width: 30%"> <img src = "viz2.png" style = "width: 30%"> <img src = "viz3.png" style = "width: 30%">

* Battery power, pixel resolution width, and ram indeed showed the strongest correlation coefficients with phone price range 
* The counts of each categorical feature were checked as well<br/>
(includes a plot that was stratified by the outcome variable and a plot that was not stratified) <br/> 
&#8594; It could be seen that among the phones that have either bluetooth, dual sim, 4G, or wifi, the phones in the highest price range are the most common


### Data Cleaning & Feature Engineering
* Data were scaled 
* Skewed features underwent log transformation 
* Heavily correlated features were handled: features that were very redundant and less important were dropped
* There were no missing or duplicated values 
* One-hot encoding was done for the categorical variables 
* Data had balanced outcome classes  


### Fit Machine Learning Models & Compare their Performances 
* The data were split into train and test sets with a test size of 20%
* Four models (KNN, SVM, Naive Bayes, Random Forest) were trained with default parameters 
* Each model's accuracy was compared: Random Forest and SVM showed the highest accuracies 

### Hyperparameter Tuning for Final Machine Learning Model 
* The hyperparameters of Random Forest and SVM were tuned, which increased both models' accuracies
* SVM was selected as the final model because its accuracy was higher
* The accuracy, precision, and recall of the final model were checked with test data (accuracy = 0.91) 
<img src = "viz5.png" style = "width: 30%" title = "confusion matrix"> <img src = "viz4.png" style = "width: 50%">
