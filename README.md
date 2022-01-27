# Amazon Vine Analysis

## Overview
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

The **goal** of this project is to analyze Amazon reviews written by individuals either are members or not members, of the paid Amazon Vine program.

## Method
#### Technologies used: 

 - AWS RDS and S3
 - PostgreSQL 12.9, pgAdmin 4.
 - PySpark 
 - Google Colab Notebook  
 
We first used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 

Next, we used PySpark to determine if there is any bias toward favorable reviews from Vine members in your dataset. 

#### Data used:
In this project, we have access to approximately 50 datasets from [Amazon](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) and picked [the book review list] (https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_00.tsv.gz) for analysis.

## Results
For review was written as part of the Vine program (paid), the total number of reviews is 5333, the number of 5-star reviews is 2069, and the percentage of 5-star reviews vine_number is 38.8%. As for the review that was not part of the Vine program (unpaid), the total number of reviews is 156262, the number of 5-star reviews is 56733, and the percentage of 5-star reviews vine number is 36.3%. 

## Summary
From our analysis, members from the Vine program only provided a small portion (3.4%) of all useful review. There aren't obvious bias in the 5-star reviews (38.8% vs 36.3%).
