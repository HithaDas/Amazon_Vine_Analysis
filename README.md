# Amazon_Vine_Analysis

# Background 

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

Use ETL, AWS and Spark to analyze Big Data on an Amazon dataset.

Deliverable 1: Perform ETL on Amazon Product Reviews
Deliverable 2: Determine Bias of Vine Reviews
Deliverable 3: A Written Report on the Analysis


In this module challenge we use Big Data and Amazon Web Services to gather and analyze a dataset on Amazon reviews for video games. 
Link to Amazon dataset used for this challenge - https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz

- For Deliverable 1, I performed ETL process using Google Colaboratory, notebook named "Amazon_Reviews_ETL,ipynb". The amazon dataset was extracted from an S3 bucket using Spark into a PySpark dataframe. 
Cleansed and transformed the raw data so that it fits the tables according to the deliverable 1 requirements.
Finally loaded the transformed data into an Amazon RDS instance which is connected to Postgress. 

- For Deliverable 2, Using the same steps performed in Deliverable 1 created a new Collab file - "Vine_Review_Analysis.ipynb".
Used PySpark to perform statistical analysis and determine if the vine reviews were biased.

# Results

1. There seems to be a bias among "Star Ratings", as there are 40,471 records that did not have vine reviews, on the other hand 94 records have vine reviews.
2. 51.06% of the Vine program gave a 5-star rating, whereas 38.70% of who had no review also gave a 5-star rating. Based on these numbers there is the possibility of biased in the Vine/Star-Rating reviews.
3. Filetered Data showing vine reviews where total votes are greater than 20.

# Summary 

Summary statistics analysis it shows that there could be bias among "Star Ratings" given the quantities of "viner" and "non-viner". 
only 94 records that did have vine reviews compred to high number about 40,471 records that did not have vine reviews.
Next, I calculated the percentage of 5-star ratings for both groups. 
51.06% of reviews that were part of the vine program gave a 5-star rating. In comparison, 38.70% of reviewers that were not part of the vine program also gave a 5-star rating. 
Based on these numbers there is the possibility of biased in the Vine/Star-Rating reviews.
