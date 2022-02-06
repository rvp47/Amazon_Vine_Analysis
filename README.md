# Amazon_Vine_Analysis

## Overview of Analysis
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Sellby is one of the many companies that pay a small fee to Amazon and provide products to Amazon Vine members, who are required to publish a review. The purpose of this analysis is to take a closer look at Amazon reviews written by Vine members and non-Vine members to determine whether this is a positivity bias for reviews in the Vine program.

Out of approximately 50 datasets, a dataset containing reviews for home improvement products was chosen for analysis. An ETL process was performed on the product reviews to extract the home improvement dataset into a DataFrame and transform the data into 4 separate Dataframes: customers, products, review ID's, and Vine. The DataFrames were loaded into pgAdmin by connecting to an AWS RDS instance and loading the DataFrames into their corresponding tables.

Determining if there is any bias towards reviews that were writtan as part of the Vine program required calculating the total number of reviews, the number of 5 star reviews (Vine and non-Vine), and the percentage of 5 star reviews (Vine and non-Vine). Evidence or lack of evidence of positivity bias is specific to this dataset and analysis and does not reflect on other categories of products.

Deliverable 1: Perform ETL on Amazon Product Reviews
Deliverable 2: Determine Bias of Vine Reviews

## Results

![deliverable 2 summary](https://user-images.githubusercontent.com/90656004/152694201-e044b023-d2be-48ce-a04c-728656222218.PNG)

- There were a total of 39,095 Vine and non-Vine reviews. Broken down, there were 266 Vine reviews and 38,829 of non-vine reviews
- Out of the total reviews, 125 Vine reviews were 5 stars (46.99%) and 18,246 non-Vine reviews were 5 stars (46.99%).
- There is no difference between Vine and non-Vine members leaving higher reviews.
 
## Summary
Based on this dataset and the results, there is no sufficient evidence of positivity bias for reviews in the Vine program. Approximately 47% of each user type left 5-star reviews for home improvement products. However, this is a bit misleading given that there was a significant difference between the total number of Vine reviews (266) and non-Vine reviews (38,829). Those participating in the Vine program accounted for only 125 5-star reviews whereas those not in the Vine program wrote 18,246 5-star reviews. It cannot be concluded that paid reviewers of home improvement products on Amazon leave more positive reviews than those who were unpaid.

Other analyses that can be done to determine if there is positivity bias include:
- Analyzing the statisical distribution of the star ratings by members and non-members
- Analyzing 1, 2, 3, and 4 star reviews for Vine and non-Vine members.
