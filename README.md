# Amazon_Vine_Analysis
 Overview of the analysis: The Amazon Vine program is a service that allows  manufacturers and  publishers to receive product reviews. Sellby is a small company that provides products to Amazon and is required to publish a review.  The project task is to provide review analysis written by members of the paid Amazon Vine Program. On this project 50 datasets can be accessed and we have to select one of the datasets and use Spypark to perform ETL to process and extract a and connect to an AWS RDS database  and transform data into PGAdmin database. Once transformed,  we'll use any of the 3 methods using Pyspark, Pandas, or SQL to determine any bias on reviews from Vine members in the dataset.

# Results:
Below are the image results from the selected dataset per deliverable requirements. 

## Deliverable 1  - Performing  ETL on Amazon Product Reviews

Selected or  dataset used:   https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Digital_Video_Games_v1_00.tsv.gz

The dataset has total count of 145,431.
![Del_dataframe count](https://user-images.githubusercontent.com/92903447/155860684-3d61f9f2-4d76-4bb2-956e-1902ef845f22.png)

A new DataFrame or table was created to filter and retrieve all the rows where the total_votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful.

# Deliverable1 - PGAdmin  Tables
## customers_table DataFrame 
![customers table_del1](https://user-images.githubusercontent.com/92903447/155858478-54674473-9f05-4fca-818c-dd42505afae3.png)
![image](https://user-images.githubusercontent.com/92903447/155861716-b6dffdd9-e267-4979-9bc6-ce7ca07af742.png)


## products_table DataFrame 
![Del1_Products_table](https://user-images.githubusercontent.com/92903447/155858558-bd096309-7541-4fc7-ab0b-fe66335cdfe7.png)
![image](https://user-images.githubusercontent.com/92903447/155861737-01febab1-6a70-43da-95f1-fc470856cee7.png)


## review_id_table DataFrame 
![Del1_review_id_table](https://user-images.githubusercontent.com/92903447/155858564-7f3c7bf2-d956-4163-b302-3cb969d113e2.png)
![image](https://user-images.githubusercontent.com/92903447/155861757-6c0b9ae5-83f9-4b84-86a6-84e2124f4e15.png)


## vine_id_table DataFrame 
![Del1_vine_table](https://user-images.githubusercontent.com/92903447/155858571-2c3ba950-4be1-4cdb-b783-7cd7b0e03665.png)
![image](https://user-images.githubusercontent.com/92903447/155861768-81af84df-9db7-4f0c-9779-f264f0f7d475.png)



## Deliverable 2 - Determine Bias of Vine Reviews
![Del 2 _dataset_dataframe](https://user-images.githubusercontent.com/92903447/155858879-9371a77d-036c-46be-a406-1a157827cfa3.png)
![helpful_votes_50 -_plus](https://user-images.githubusercontent.com/92903447/155858884-9f2b39f4-3777-4976-aee0-cfc63e846e61.png)

### How many Vine reviews and non-Vine reviews were there?

![Del2_filtered DataFrame_paid vine program](https://user-images.githubusercontent.com/92903447/155858865-247194e8-68b6-4d28-b8c6-4e2acb4fc0f7.png)

### How many Vine reviews were 5 stars? 0 count of vine review . 
### How many non-Vine reviews were 5 stars?  631

![total number of reviews, nmber of star reviews of paid and unpaid](https://user-images.githubusercontent.com/92903447/155859089-aa68e43f-b2b4-4ca6-af1e-d05c0fda1925.png)


### What percentage of Vine reviews were 5 stars?  Vine review shows 0 percent of  5 star rating  for paid vine program .
### What percentage of non-Vine reviews were 5 stars? The unpaid vine reviews shows 37.4 of unpaid vine program.

![5 star paid reviews](https://user-images.githubusercontent.com/92903447/155859105-0956dc98-57e4-4af8-bbaa-f6ea55fea9e6.png)

![5 star percentage unpaid vine program](https://user-images.githubusercontent.com/92903447/155859110-087ec607-54d5-4581-aedc-734f8dba0307.png)


# Summary: 

After narrowing down the dataset, the paid vine program has resulted to zero percent review that cause to falter to a zero division error in  running script and therefore reviews for paid and unpaid vine programs are uncomparable.  The analysis is biased towards unpaid Vine reviews which has total count of 1685 unpaid vine program. Another key measure to check is the comparative percentage run of unpaid 5-star vine reviews,  that has  total count of 631 which resulted to 37.4% vs. the 0 percent paid reviews which makes the unpaid Vine biased as well.

We could take a test sample of adjusting 50% of helpful  or 2O likes and see if we can reconsider using this dataset.





