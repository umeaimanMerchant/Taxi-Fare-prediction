# Data Science Taxi fare Prediction: Project Overview 
* Create a model which can predict taxi fares before the ride to help increase revenue for 'New Yock City TLC'.
* Performed EDA, feature Engineering and hypothesis testing using python
* Optimized Random Forest Regressors and XGBoost Regressor using GridsearchCV to reach the best model. 
 
## Overview on New Yock City TLC-
New York City TLC is an agency responsible for licensing and regulating New York City's taxi cabs and for-hire vehicles. The agency wants to develop a regression model that helps estimate taxi fares before the ride, based on data that TLC has gathered. 

The TLC data comes from over 200,000 taxi and limousine licensees, making approximately one million combined trips per day. 

## Code and Resources Used 
**Packages:** pandas, numpy, datetime, sklearn, matplotlib, seaborn, scipy, xgboost
**For Web Framework Requirements:**  ```pip install -r requirements.txt```  

## Dataset

![alt text](https://github.com/umeaimanMerchant/Taxi-Fare-prediction/blob/main/Images/Dataset%20img.PNG "Description of dataset")

## Part 1- Inspect and Analyse Data

**Purpose** - to investigate and understand the data provided.

**Goal**- to use a dataframe contructed within Python, perform a cursory inspection of the provided dataset.

**Results**- 
1. most expensive rides are not necessarily the longest distance
2. Only for Credit card user we have tip ampunt in the dataset, thus we can't conclude anything about tip's given in cash.
3. Few location for pickup and dropoff are popular amoung users
4. Distance and duration can be key columns for estimating cost

## Part 2- Exploratory data analysis (EDA)

**Purpose** - to conduct exploratory data analysis on a provided data set

**Goal**- to clean data set and create a visualization.

**Results-**
1. Outliers are present for trip_distance, tip_amount, total_amount
2. Used *Feature Engineering* to get Hour, Weekdays and Month from tpep_pickup_datetime column and tried to understand relation between these fields with total_amount, tip_amount and trip_distance. At peak time during the day, total amount is high.
3. total_amount more for a few drop off location?
4. total_amount lower in the months of Jul and Aug month?
3. Created following visualization-

### Visualization

![alt text](https://github.com/umeaimanMerchant/Taxi-Fare-prediction/blob/main/Images/Month%20vs%20amount.PNG "Month V/S Total Amount")
![alt text](https://github.com/umeaimanMerchant/Taxi-Fare-prediction/blob/main/Images/Passenger%20vs%20tip%20amt.PNG "Tip Amount V/S Passengers")
![alt text](https://github.com/umeaimanMerchant/Taxi-Fare-prediction/blob/main/Images/weekday%20vs%20amt%20and%20distance.PNG "Weekdays V/S Total Amount & Tip Amount")

# Part 3: Statistical analysis or Hypothesis Testing

**Purpose** -to prepare, create, and analyze A/B tests, that aims to find ways to generate more revenue for taxi cab drivers.

**Goal** - to analyze whether there is a relationship between payment type (Card or Cash) and fare amount. 

**Results-** - The key business insight is that encouraging customers to pay with credit cards can generate more revenue for taxi cab drivers.

## Part 4: Build a multiple linear regression model

**Purpose**  to estimate fare cost using multiple linear regression.

**Goal** -to build a multiple linear regression model and evaluate the model

# Part 5: Build a machine learning model 

**Purpose**- to find ways to generate more revenue for taxi cab drivers.  
  
**Goal**- to predict whether or not a customer is a generous tipper.  (think?)

**Results**- F1 score

* Random Forest- 0.7086390532544378

* XGBooost Model- 0.6789703739679456
