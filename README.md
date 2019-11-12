# Spark_Project


Project Overview

Customer churn (also known as customer attrition, customer turnover or customer defection) is a term used especially in the world of subscription-based businesses to describe loss of customers. It is a major concern for many businesses because it directly affects  service’s profitability. This project is analyze an  Sparkify online user log dataset to build a model for churn prediction. This project is utilized Spark to do the data wrangling and modeling to make prediction. 


Project Components

1.	Load and Clean Dataset

In the Project , first read a  tiny sparkify log files  subset (128MB) of the full dataset available (12GB).  File name is  "mini_sparkify_event_data.json" to work faster while exploring  data and develop  model. Necessary steps include load and clean the dataset, checking for invalid or missing data. 

2.	Exploratory Data Analysis

Perform EDA by doing basic manipulations within Spark. create a column Churn to use as the label for model. Use  Cancellation Confirmation events to define churn, which happen for both paid and free users. Then perform some exploratory data analysis to observe the behavior for users who stayed vs users who churned by exploring aggregates on these two groups of users, observing how much of a specific action they experienced per a certain time unit , number of songs played, songs played distribution in hour, most played artist, gender difference with churn, level difference with churn, distribution of length between two groups of users, event/page visit frequency difference with churn

3.	Feature Engineering and Scaling

create necessary features found promising in EDA stage to train your model on to use machine learning algorithms. the final features generated are downgraded, visited_downgrade, roll_advert, dailyHelpVisits, dailyErrors, free, paid, male, female, avgThumbsUp,avgThumbsDown,numFriends,DaysSinceRegistration,avg_songplaylength.

4.	Modeling

Split the dataset into train, test, and validation sets. Test out the machine learning methods like logistic regression model, SVM, random forest classifier model and gradient boosted trees . Evaluate the accuracy of each models, determine winning model based on test accuracy and report results on the test set. My winning model is Gradient boosted trees . I also did feature importances analysis from it to analyze most important features for prediction.



Instructions:

To run this script, necessary pyspark packages need to be included like pyspark.sql, pyspark.sql.functions, pyspark.sql.types, pyspark.ml.feature , pyspark.ml.linalg, pyspark.ml.classification, pyspark.mllib.evaluation


Detail Report found here

https://medium.com/@yujingfeng/spark-project-churn-prediction-6fa0fb12fdbf?sk=3c284e1a866396220a6f4f08bf708064
