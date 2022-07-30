# Amazon_Vine_Analysis

## Overview
The purpose of the this project is to  analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
In this project, the dataset contains reviews of a specific product, from books. 
- PySpark is used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 
- Next, PySpark is used to determine if there is any bias toward favorable reviews from Vine members in the dataset.

## Dataset
Dataset can be found here: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz

## Software Used:
- PySpark
- AWS RDS
- Google Colab

## Results
Important filter note: reviews were filtered to only look at reviews that had 20 or more total votes and then we only look at reviews that had greater than 50% of their total votes ranked as helpful votes.
- **How many Vine reviews and non-Vine reviews were there?**
	- There were no vine reviews with 20 or more total votes. So for this book review dataset the Vine paid program doesn't seem to add any value to the review experience.
- **How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?**
	- There was zero 5 star Vine reviews and 241,836 5 star non-Vine reviews.
- **What percentage of Vine reviews were 5 stars?**
	- There were none after the filtered requirements.
- **What percentage of non-Vine reviews were 5 stars?**
	- This question was not answer during the review, but the precentage of non-Vine 5 stars reviews that were paid versus unpaid is 24,719/214,417 or 11.528%.

## Summary
More Vine datasets should be analyzed before making a conclusion on the Vine review program but for this dataset on book reviews:
- Vine program view had no affect on the product reviews.
- Paid subscribers were only ~11.5% of the 5 star reviews.
- Removing the filter of having 20 or more votes and lowering or removing the 50% helpful filter may provide a bigger picture and allow Vine reviews to make it into the analysis for this dataset.

