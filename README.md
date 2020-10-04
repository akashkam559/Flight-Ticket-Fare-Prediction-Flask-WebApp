# Flight-Price-Prediction

Table of Content
-----------------
* Demo
* Directory Tree
* Overview
* Motivation
* Installation
* Advantages & Disadvantages
* Phases
* Process
* Deployement on Heroku
* Result/Summary
* Future scope of project

Demo 
------
Link: https://flightfarewebapp.herokuapp.com/

![FLIGHT PRICE PREDICTION-3](https://user-images.githubusercontent.com/41515202/95026175-0fda3680-06ad-11eb-86dc-457fa5ae1ab6.PNG)

![FLIGHT PRICE PREDICTION-2](https://user-images.githubusercontent.com/41515202/95026073-4b283580-06ac-11eb-9129-2bc25d19c15e.png)


Directory Tree
----------------

├── static 

│   ├── css

├── template

│   ├── home.html

├── Procfile

├── README.md

├── app.py

├── flight_model.pkl

├── requirements.txt



Overview / What is it ??
---------------------------
* Flask web app which predict the date of "pricefall" and the date of "cheapest travel" fare of Flight ticket.

* Today we might see a different price, check out the price of the same flight tomorrow

* prices can be something hard to guess

* We might have often heard travelers saying that flight ticket prices are so unpredictable


Movtivation / Why / Reason ??
----------------------------
* What to do when you are at home due to this pandemic situation? I started to learn Machine Learning model to get most out of it. I came to know mathematics behind all supervised models. Finally it is important to work on application (real world application) to actually make a difference.

* Because our airfare predictions were designed to check the price patterns of one airline at a time and this can only mean an increased accuracy prediction

* Due to the high complexity of the pricing models applied by the airlines, it is very difficult for a customer to purchase an air ticket at the lowest price, since the price changes dynamically

* For this reason, several techniques ready to provide the proper time to the customer to buy an air ticket by predicting the airfare price, are proposed recently

* The majority of those methods are making use of sophisticated prediction models from the computational intelligence research field known as Machine Learning (ML)

* User can select their preferences in order to access the web application

* A traveller can access this module to get the future price prediction of individual airlines

* The prediction will help a traveller to decide a specific airline as per his/her budget.

* We simulate various models for computing expected future prices and classifying whether this is the best time to buy the ticket

* Provide different various options to choose flight fare on basis of cheap tickets

* Show price comparison b/w various flight price patterns and show price accurate predictions and show cheap prices

* Find ticket price patterns and predict price changes for many airlines

* For a traveller it is important to know the fare value of a trip, and as prices of flight ticket varies abruptly and it becomes hectic for a user to check different websites, use different deals. A flight fare prediction model will help inform the travellers with the optimal time to buy their flight tickets and understand trends in the airline industry.

* Gonna prove that given the right data anything can be predicted

* Gathered the dataset for prices of flight tickets for various airlines - used two datasets, Train data and Test data - Training data is combination of both categorical and numerical also we can see some special character also being used because of which we have to do data Transformation on it before applying it to our model - predict the air tickets prices,  and  the  performance  of  the  models is  compared  to  each other

* There  are  two  possible alternatives   for   handling   the   problem   of   airfare   pricing prediction.  The  first  approach  tackles  the  prediction  of  air tickets  prices  as  a regression  problem,  while  the  second  one transforms  it  to  a classification  task

* Purpose of this study is to better analyze the features that affect airfare and develop and tune models to predict the airfare well in advance.

Installation / Tech Used
--------------------------
* The Code is written in Python 3.6.10. If you don't have Python installed you can find it here. If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after cloning the repository:

* pip install -r requirements.txt

* Used two datasets, Train data and Test data from Kaggle 

* Language – Python, Anaconda

* Other libraries for analyzing & visualization: Pandas, Numpy, Matplotlib, Seaborn

* AI/ML : Scikit-Learn , ML models

* Web Frameworks : Flask

* Hosting: Heroku (side projects & demos)

* Tracking & SC: GitHub

![pyton](https://user-images.githubusercontent.com/41515202/94375948-e06b7d00-0134-11eb-9559-d078036947f3.png)
![Anaconda](https://user-images.githubusercontent.com/41515202/94375900-7bb02280-0134-11eb-9180-c7cf25272bd4.png)
![flask](https://user-images.githubusercontent.com/41515202/94375852-30960f80-0134-11eb-80ec-34d17cbf4d4f.png)
![sklearn](https://user-images.githubusercontent.com/41515202/94375853-32f86980-0134-11eb-935c-59c70f6db9f1.png)
![gunicorn](https://user-images.githubusercontent.com/41515202/94375855-34c22d00-0134-11eb-9091-7ea412078a07.png)


Advantages
------------
* Traveler get the fare prediction handy using which it’s easy to decide the airlines.

* Saves time in searching / deciding for airlines

Disadvantages
------------
* Improper data will result in incorrect fare predictions


Phases
-------
1). Data  Collection - Importing Dataset

2). EDA - Feature  Engeneering( Dividing data into features and labels), Selection, Explore dataset, Data Cleaning, Convert categorical data into numerical, Concatenate both catagorical and numerical data

FEATURES:

Airline:  The name of the airline.

Date_of_Journey: The date of the journey

Source: The source from which the service begins.

Destination: The destination where the service ends.

Route: The route taken by the flight to reach the destination.

Dep_Time: The time when the journey starts from the source.

Arrival_Time: Time of arrival at the destination.

Duration: Total duration of the flight.

Total_Stops: Total stops between the source and destination.

Additional_Info: Additional information about the flight

Price: The price of the ticket 


3 ). ML  Models  Selection - Building Supervised Machine Learning Models => Xgboost, Random Forest, KNN, Gradientboost

4). Evaluation - Used  in  a  10-fold  cross-validation  procedure to  train the aforementioned ML models. The performance indices used to compare  the  models are  the  prediction accuracy (%  -  MSE between  the  desired  and  predicted  prices)  and  the  time  in seconds, needed to train each model.

5). Deployment - Deployed on Heroku using Flask framework 

Process - Timeline
--------------------
* Since data is in form of excel file we have to use pandas read_excel to load the data

* We will be using train and test data. Test data is similar to train data minus the ‘price’ column. We can do some data pre-processing and remove variables which are not needed 

* After loading it is important to check the complete information of data as it can indication many of the hidden infomation such as null values in a column or a row. Next step is Feature generation, here we mainly work on the data and do some transformations to extract unknown variables or create different bons of particular columns and clean the messy data.

* Check whether any null values are there or not. if it is present then following can be done,

      Imputing data using Imputation method in sklearn
    	Filling NaN values with mean, median and mode using fillna() method
      Describe data, which can give statistical analysis

* Mainly work on the data set and do some transformation like creating different bins of particular columns ,clean the messy data so that it can be used in our ML model . This step is very important because for a high prediction score you need to continuously make changes in it

* Do some EDA, analysis & data visualisation to understand the relationship between different independent variables and the relationship between the independent variables and the dependent variables

* Prepare categorical variables for model using label encoder - convert categorical text data into model-understandable numerical data

* Divide the data set into test and train - all our data is numerical after label encoding so we split the data into test and train & predict the price with our test data set

* Building Model - measure the performance of a better and more tuned algorithm, & using different Regression Technique and comparing them to see which algorithm is giving better performance. Evaluated various models for computing expected future prices and classifying whether this is the best time to buy the ticket. Finally after the above steps. Predict the air tickets prices, and the performance of the models is compared to each other. Later deployed the model and evaluate the efficiency of the predictions. 

* SUPERVISED MODELS USED:
    Random Forest: 90.04%, Xgboost : 87.48%, Gradientboost : 87.59%, ACCURACY SCORE : 93:14%


Deployment on Heroku
-----------------------
Login or signup in order to create virtual app. You can either connect your github profile or download ctl to manually deploy this project.

![heroku](https://user-images.githubusercontent.com/41515202/94375849-2e33b580-0134-11eb-96cb-40a79f8e75b4.png)

Our next step would be to follow the instruction given on Heroku Documentation to deploy a web app.

Result/Summary
---------------
* Developed end-to-end full fleged ML-WebApp to display price accurate predictions with Random Forest 87\% accuracy \&  deployd on heroku

* Applied all various high performance ML models \& compared their best MAE,MSE,RMSE accuracy score to predict the fare

* Evaluated 4 supervised Regression models Xgboost, Random Forest, KNN, Gradientboost \& improved & optimized the Model by HPT Cross validation, GridSearchCV

* Demonstrated EDA, handling categorical data, feature selection & scaling, dimensionality reduction \& feature transformation using PCA Bias-Variance tradeoff, Performance Metrics, Splitting data into train and test set, performed GRidSearchCV to optimize model,cross validated k-fold, trained model using Random Forest Regressor

* Recommended Random Forest, fitted/split the train \& test data, (X\_train, y\_train)score = 94\%, (X\_test, y\_test)score 78\%, Metrices R2 score (y\_test, y\_pred) = 78\%, accuracy = 90.04\% on test data, model tuning using  RandomizedSearchCV


Future Scope
-------------
Use multiple Algorithms.

Optimize Flask app.py.

Front-End.

