# Amazon_Vine_Analysis

## Overview of Analysis
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Sellby is one of the many companies that pays a small fee to Amazon and provides products to Amazon Vine members, who are required to publish a review. The purpose of this analysis is to take a closer look at Amazon reviews written by Vine members and non-Vine members to determine whether there is a positivity bias for reviews in the Vine program.

Out of approximately 50 datasets, a dataset containing reviews for home improvement products was chosen for analysis. An ETL process was performed on the product reviews to extract the home improvement dataset into a DataFrame and transform the data into 4 separate Dataframes: customers, products, review ID's, and Vine. The DataFrames were loaded into pgAdmin by connecting to an AWS RDS instance and loading the DataFrames into their corresponding tables.

Determining if there is any bias towards reviews that were written as part of the Vine program required calculating the total number of reviews, the number of 5 star reviews (Vine and non-Vine), and the percentage of 5 star reviews (Vine and non-Vine). Evidence or lack of evidence of positivity bias is specific to this dataset and analysis and does not reflect other categories of products.

Deliverable 1: Perform ETL on Amazon Product Review
Deliverable 2: Determine Bias of Vine Reviews

## Results

![deliverable 2 summary](https://user-images.githubusercontent.com/90656004/152694201-e044b023-d2be-48ce-a04c-728656222218.PNG)

- There were a total of 39,095 Vine and non-Vine reviews. Broken down, there were 266 Vine reviews and 38,829 non-Vine reviews
- Out of 266 Vine review, 125 (46.99%) were 5 stars and out of 38,829 non-Vine review, 18,246 (46.99%) were 5 stars.
- There is no difference between Vine and non-Vine members leaving higher reviews.
 
## Summary
Based on this dataset and the results, there is no sufficient evidence of positivity bias for reviews in the Vine program. Approximately 47% of each user type left 5-star reviews for home improvement products. However, this may be a bit misleading given that the total number of Vine reviews (266) may not be an accurately representative sample to compare against such a large number of non-Vine reviews (38,829). To achieve a 95% confidence level with a 5% margin of error, there would need to be at least 381 Vine reviews to compare against non-Vine reviews. Taking the results at face-value, however, it cannot be concluded that paid reviewers of home improvement products on Amazon leave more positive reviews than those who were unpaid.

Other analyses that can be done to determine if there is positivity bias include:
- Analyzing the statisical distribution of the star ratings by members and non-members
- Analyzing 1, 2, 3, and 4 star reviews for Vine and non-Vine members.
