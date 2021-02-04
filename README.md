# DataScienceCapstone2

# Introduction:
Will studying the area of NYC during 2020 and the pandemic help to determine how a TLC yellow cab driver can maximize their daily earnings? Since the start of the pandemic, taxi drivers in NYC have not had the same foot traffic as before. Tourists stopped traveling and a majority of local people have been forced to commute less. Between the months of March and June, NYC was hit at its hardest in the pandemic and so were all daily workers. With enough unique data about a taxi’s trip I can generalize a model to predict the highest amount of money a taxi driver can make.

# What is in the data:
The problem I am trying to solve is the one about predicting a maximized hourly earning for yellow cab drivers. My client would be the yellow cab drivers because this model should help reveal which features affect their ability to make the most amount of money on any given day. The data I will be using consists of TLC data from January 2020 to June 2020. This data also contains features like, surcharge, location, pick up date and time, drop off date and time, and additional columns that I have added from studying the data. The data contains types in datetime , continuous, and categorical.

# Feature Engineering:
Through the use of Exploratory Data Analysis I came to find that there were certain features from the original data that had a better correlation to the total amount of a trip. These features include: trip_distance, fare_amount, tolls_amount, tip_amount. In addition, I included the pick up areas and the drop off areas as the locations also impacted how much money a trip would make.

# Trying different models for price prediction:

| Model             | RMSE_train | RMSE_test | r2_train | r2_test | alpha | n_neighbors | max_depth | n_estimators |
|-------------------|:----------:|----------:|---------:|--------:|------:|------------:|----------:|--------------|
| Linear Regression |  1.268635  | 1.040149  | 0.604423 | 0.676428|  NaN  |     NaN     |    NaN    |      NaN     |
| Rdige Regression  |  1.275546  | 1.038297  | 0.602268 | 0.677579|  0.1  |     NaN     |    NaN    |      NaN     | 
| Lasso Regresssion |  1.296831  | 1.033434  | 1.296831 | 0.680592| 0.001 |     NaN     |    NaN    |      NaN     |
| KNearest Neighbors|  0.749192  | 0.908528  | 0.766392 | 0.753136|  NaN  |      8      |    NaN    |      NaN     |
|Single DecisionTree|  0.392672  | 0.832889  | 0.877560 | 0.792530|  NaN  |     NaN     |     7     |      NaN     |
| Random Forest     |  0.246644  | 0.704695  | 0.923093 | 0.851480|  NaN  |     NaN     |     9     |       5      |
| Gradient Boosting |  0.616607  | 0.942479  | 0.807734 | 0.734341|  NaN  |     NaN     |     9     |       9      |
| Ada Boosting      |  0.785707  | 0.829604  | 0.755006 | 0.751886|  NaN  |     NaN     |    NaN    |       6      |



