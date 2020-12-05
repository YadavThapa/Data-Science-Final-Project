# Starbucks promotion Strategy using Machine Learning Algorithm

## Project Overview
We all know the customer satisfaction drives business success and data analytics provides insight into what customers think. for e.g."360-degree customer view" refers to aggregating data describing a customer's purchases and customer service interactions.

The "Starbucks" George Washington Data Science Capstone challenge data set is a simulation of customer behavior on the Starbucks rewards mobile application. Starbucks sends offers to its customers periodically that may be different mode of advertisements, discount offer, or buy one get one free (BOGO) promotion. The unique and important characteristics of this dataset is that not all users receive the same offer.


### Datasets
The given datasets contain three files. 

Here is the schema and explanation of each variable in the files:
### portfolio.json
The first file describes the characteristics of each offer, including its duration and the amount a customer needs to spend to complete it (difficulty). 
id (string) - offer id
offer_type (string) - type of offer ie BOGO, discount, informational
difficulty (int) - minimum required spend to complete an offer
reward (int) - reward given for completing an offer
duration (int) - time for offer to be open, in days
channels (list of strings)

### profile.json
The second file contains customer demographic data including their age, gender, income, and when they created an account on the Starbucks rewards mobile application.
age (int) - age of the customer
became_member_on (int) - date when customer created an app account
gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
id (str) - customer id
income (float) - customer's income

### transcript.json
The third file describes customer purchases and when they received, viewed, and completed an offer. An offer is only successful when a customer both views an offer and meets or exceeds its difficulty within the offer's duration.

event (str) - record description (ie transaction, offer received, offer viewed, etc.)
person (str) - customer id
time (int) - time in hours since start of test. The data begins at time t=0
value - (dict of strings) - either an offer id or transaction amount depending on the record


