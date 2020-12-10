# Starbucks Data Science Challenge

<b> Table of content<br>
- 1 Project Definition
- 1.1 Project Overview 
- 1.2 Problem Statement
- 1.3 Metrics
- 2 Exploratory Data Analysis<
- 2.1 Data Exploration and Visualization
- 2.1.A Portfolio Dataset
- 2.1.B Profile Dataset
- 2.1.C Transcript Dataset
- 2.2 Data Analysis
- 3 Data Preprocessing (Wrangling/Cleaning)
- 3.A Portfolio Dataset
- 3.B Profile Dataset
- 3.C Transcript Dataset
- 4 Data Modeling
- 4.1 Modeling
- 4.2 Model Evaluation
- 4.3 Model Refinement
- 5 Conclusion
- 6 Improvement

## Project Overview
We all know the customer satisfaction drives business success and data analytics provides insight into what customers think. for e.g."360-degree customer view" refers to aggregating data describing a customer's purchases and customer service interactions.

The "Starbucks" George Washington University Data Science Capstone challenge data set is a simulation of customer behavior on the Starbucks rewards mobile application. Starbucks sends offers to its customers periodically that may be different mode of advertisements, discount offer, or buy one get one free (BOGO) promotion. 

The unique and important characteristics of this dataset is that not all users receive the same offer.


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

### Results Summary

Following accuracy results have been recieved from the testing datasets.
- SVM model accuracy: 73.14%
- Decision Classifier : 97.55%
- Naive Bayse: 60.46%
- Knn : 82.41%.
- RandomForestClassifier model accuracy: 87.5%.
- Adaboostclassifer: 75.38%
- LogisticRegression model: 73.36%.

### Conclusions
The first step we went through was clustering the demographic information, which resulted in 6 clusters to work from. A 7th cluster was added where there was no demographic data present.
- Where there as no data present (segment 7), they had lower representations in the completed and viewed population, ann higher representation in the completed and not viewed population. We would therefore recommend that costly offers such as discounts or BOGO are not sent to these customers.

- When using logistic regression on both the demographic and offer data, by far the biggest impact was the type of offer (holding all other factors constant, an informational offer would decrease the chance of completeing by 99.7%, compared with a discount which would increase it by around 7 times. The biggest demographic impact was the income, and the longer a customer had been a member the more likely they are to complete.

- Most of the clusters got similar regression values, with the main exception of group 4 (younger male, lower income) who reacted negatively instead of positively to mobile advertisements.

- Ultimatly this was on simulated data, which did show in some of the scatter plots. It would be more interesting to try this on real world data, which would also add more depth to the reccomendations. It was however interesting how the different models generalised well to the test data, even though the test data contained recent data with (in theory) a different mix of customers.

### Future Improvements
1. This data set has more potential to solving many queries and it can be utilized to answer many posed questions related customer interaction based on the Age and income as a whole too.
2. Testing additional machine learning models.
3. Making a web app

### Python Libraries Used
- Python Data Analysis Library
- Numpy
- Matplotlib
- seaborn: Statistical Data Visualization
- re: Regular expression operations
- os — Miscellaneous operating system interfaces
- scikit-learn: Machine Learning in Python
- Joblib: running Python functions as pipeline jobs
