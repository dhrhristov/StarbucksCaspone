# StarbucksCaspone
UdaCity Starbucks Caspone

# Starbucks Capstone Challenge
Udacity Data Scientist Capstone project

### Table of Contents

1. [Project Introduction](#objectives)
2. [Data Sets](#datasets)
3. [Problem Conclusion](#conclusion)



## Caspone Project Introduction <a name="objectives"></a>

Starbucks Capstone Challenge: This project will reach customer via a smartphone application from Starbucks. Based on artifical dataset, we will perform analysis and send offers to specific users who has the highest chance to use it.

Initially we will explore the dataset and collect metrics like information for income, age, provided personal data and more. Then based on the current offer will be created a prediction model per user. The model will provide us witha analysis for:

    Which offer will be successful and profitable?
    How factors like gender/income/average purchase/offer completion time reflect on the prediction?
    Structure users per user groups and what promotions to sent them via Starbucks app.
	

## Data Sets <a name="datasets"></a>

Data Sets

The data is contained in three files:

    portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
    profile.json - demographic data for each customer
    transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

portfolio.json

    id (string) - offer id
    offer_type (string) - type of offer ie BOGO, discount, informational
    difficulty (int) - minimum required spend to complete an offer
    reward (int) - reward given for completing an offer
    duration (int) - time for offer to be open, in days
    channels (list of strings)

profile.json

    age (int) - age of the customer
    became_member_on (int) - date when customer created an app account
    gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
    id (str) - customer id
    income (float) - customer's income

transcript.json

    event (str) - record description (ie transaction, offer received, offer viewed, etc.)
    person (str) - customer id
    time (int) - time in hours since start of test. The data begins at time t=0
    value - (dict of strings) - either an offer id or transaction amount depending on the record

Note: If you are using the workspace, you will need to go to the terminal and run the command conda update pandas before reading in the files. This is because the version of pandas in the workspace cannot read in the transcript.json file correctly, but the newest version of pandas can. You can access the terminal from the orange icon in the top left of this notebook. 

## Problem Conclusion <a name="conclusion"></a>

Starbucks Customers gender distribution is 60/40 % males/females where more than 60% of with age between 45-60 years. The average income is around 65K per year. Customers who didn't provide income and detailed personal information, also did not respond to offers.

Based on the prediction Models we can see that customers have

    1) highest interested in Discount Offers
    2) next in BOGO offers
    3) least interested into Informational Offers

Analysis per Cluster

    0) the second lagest group of customers. These customers are on higher Age but they have reacted very well on discounted offers. These are people with highest income hence they respond better to an offer and will more likely to spend more on Starbucks products where BOGO and Discount offers will be well received.
    1) the third/fourth group of customers. These customer have average income and has shown interest in BOGO offers.
    2) the highest number of customers ~41%. But those customers will probably buy anyway even without offers.
    3) the third/fourth group of customers. This group has shown the lowest number of transactions and they have lowest income. The chances to get Discounted offer here are better.
