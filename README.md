# Starbucks promotion Strategy using Machine Learning Algorithm

## Project Overview
We all know the customer satisfaction drives business success and data analytics provides insight into what customers think. for e.g."360-degree customer view" refers to aggregating data describing a customer's purchases and customer service interactions.

The "Starbucks" George Washington Data Science Capstone challenge data set is a simulation of customer behavior on the Starbucks rewards mobile application. Starbucks sends offers to its customers periodically that may be different mode of advertisements, discount offer, or buy one get one free (BOGO) promotion. The unique and important characteristics of this dataset is that not all users receive the same offer.


### Datasets
The given datasets contain three files. 

Here is the schema and explanation of each variable in the files:
### Portfolio.json
The first file describes the characteristics of each offer, including its duration and the amount a customer needs to spend to complete it (difficulty). <br>
1. id (string) - offer id 
2. offer_type (string) - type of offer ie BOGO, discount, informational
3. difficulty (int) - minimum required spend to complete an offer
4. reward (int) - reward given for completing an offer
5. duration (int) - time for offer to be open, in days
6. channels (list of strings)

### Profile.json
The second file contains customer demographic data including their age, gender, income, and when they created an account on the Starbucks rewards mobile application.
1. age (int) - age of the customer
2. became_member_on (int) - date when customer created an app account
3. gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
4. id (str) - customer id
5. income (float) - customer's income

### Transcript.json
The third file describes customer purchases and when they received, viewed, and completed an offer. An offer is only successful when a customer both views an offer and meets or exceeds its difficulty within the offer's duration.

1. event (str) - record description (ie transaction, offer received, offer viewed, etc.)
2. person (str) - customer id
3. time (int) - time in hours since start of test. The data begins at time t=0
4. value - (dict of strings) - either an offer id or transaction amount depending on the record


### Future Improvements
1. This data set has more potential to solving many queries and it can be utilized to answer many posed questions related customer interaction based on the Age and income as a whole too.
2. Testing additional machine learning models.
3. Making a web app


