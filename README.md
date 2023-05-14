# First data science project - clusterisation of gym users

## Introduction

**Project description**

The fitness center network, 'Bodybuilder-Data Scientist,' is working on a strategy to engage users based on analytical data. One of the most common problems facing fitness clubs and similar services is customer churn. It's not always clear when a user has stopped using the service, as they may not always leave in an obvious way.

For a fitness center, a client is considered to have churned if they haven't visited the gym at least once in the last month. While it's possible that they went on vacation and will return to the gym upon their arrival, it's more likely that they won't. If a client starts going to the gym but then suddenly stops, they are unlikely to return.

Your task is to analyze the data and develop an action plan to retain customers.

Specifically, the objectives are to:

1. Learn how to predict the probability of customer churn (for the following month) for each client.
2. Create typical user profiles: identify several of the most prominent groups and characterize their key attributes.
3. Analyze the main features that have the greatest impact on churn.
4. Formulate key conclusions and develop recommendations to improve customer relationship management, including:
  1. Identifying target customer groups;
  2. Proposing measures to reduce churn;
  3. Determining other nuances of customer interactions.

**Data description**

We have a dataset gym_churn.csv containing information about the month prior to churn and the fact of churn for a specific month. The dataset includes the following fields:

1. `Churn` - indicating whether the customer churned in the current month.

The current fields in the dataset contain user data for the month prior to the churn check, such as:

2. `Gender` - the gender of the customer.
3. `Near_Location` - whether the customer lives or works in the area where the fitness center is located.
4. `Partner` - indicating whether the customer is an employee of a club partner company, in which case the fitness center stores information about the customer's employer.
5. `Promo_friends` - indicating whether the customer registered under the "bring a friend" promotion, using a promo code from an acquaintance when paying for the first subscription.
6. `Phone` - indicating whether the customer provided a contact phone number.
7. `Age` - the age of the customer.
8. `Lifetime` - the time since the customer's first visit to the fitness center (in months).

The dataset also includes information based on the client's visit log, purchases, and current subscription status, such as:

9. `Contract_period` - the duration of the customer's current active subscription, which can be a month, 3 months, 6 months, or a year.
10. `Month_to_end_contract` - the time until the end of the customer's current active subscription (in months).
11. `Group_visits` - indicating whether the customer attends group classes.
12. `Avg_class_frequency_total` - the average frequency of visits per week for the entire duration of the subscription.
13. `Avg_class_frequency_current_month` - the average frequency of visits per week for the previous month.
14. `Avg_additional_charges_total` - the total revenue from other fitness center services, such as cafes, sports goods, beauty, and massage salon.

**Project plan**

1. Load the data.
2. Conduct an exploratory data analysis (EDA):
  a. Examine the dataset for missing features and study the mean values and standard deviations.
  b. Analyze the mean values of features in two groups: those who churned and those who stayed.
  c. Construct bar and feature distributions for those who churned and those who stayed.
  d. Create a correlation matrix and display it.

3. Build a binary classification model for customers, where the target feature is customer churn in the next month:
  1. Split the data into training and validation sets.
  2. Train the model in two ways:
    1. Logistic regression.
    2. Random forest.
  3. Evaluate the accuracy, precision, and recall metrics for both models. Compare the models based on the metrics. Which model performed better based on the metrics?

4. Perform customer clustering:
  1. Standardize the data.
  2. Build a distance matrix on the standardized feature matrix and draw a dendrogram.
  3. Train the clustering model based on the K-Means algorithm and predict customer clusters. Let's agree to use n = 5 as the number of clusters.
  4. Examine the mean values of features for the clusters. Can any immediate observations be made?
  5. Construct feature distributions for the clusters. Can any observations be made from them?
  6. Calculate the churn rate for each obtained cluster. Are they different in terms of churn rate? Which clusters are prone to churn, and which are reliable?

5. Formulate conclusions and make basic recommendations for working with customers.
