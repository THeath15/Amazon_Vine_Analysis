# Amazon_Vine_Analysis
 Overview of the analysis: The Amazon Vine program is a service that allows  manufacturers and  publishers to receive product reviews. Sellby is a small company that provides products to Amazon and is required to publish a review.  The project task is to provide review analysis written by members of the paid Amazon Vine Program. On this project 50 datasets can be accessed and we have to select one of the datasets and use Spypark to perform ETL to process and extract a and connect to an AWS RDS database  and transform data into PGAdmin database. Once transformed,  we'll use any of the 3 methods using Pyspark, Pandas, or SQL to determine any bias on reviews from Vine members in the dataset.

# Results:
Below are the image results from the selected dataset per deliverable requirements. 

## Deliverable 1  - Performing  ETL on Amazon Product Reviews

Selected or  dataset used:   https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Digital_Video_Games_v1_00.tsv.gz

The dataset has total count of 145,431.
![Del_dataframe count](https://user-images.githubusercontent.com/92903447/155860684-3d61f9f2-4d76-4bb2-956e-1902ef845f22.png)

   
## customers_table DataFrame 
A new DataFrame or table was created to filter and retrieve all the rows where the total_votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful.

Deliverable1 - PGAdmin - Customer table 
![customers table_del1](https://user-images.githubusercontent.com/92903447/155858478-54674473-9f05-4fca-818c-dd42505afae3.png)

## customers_table DataFrame 
![Del1_Products_table](https://user-images.githubusercontent.com/92903447/155858558-bd096309-7541-4fc7-ab0b-fe66335cdfe7.png)

## review_id_table DataFrame 
![Del1_review_id_table](https://user-images.githubusercontent.com/92903447/155858564-7f3c7bf2-d956-4163-b302-3cb969d113e2.png)

## vine_id_table DataFrame 
![Del1_vine_table](https://user-images.githubusercontent.com/92903447/155858571-2c3ba950-4be1-4cdb-b783-7cd7b0e03665.png)


## Deliverable 2 - Determine Bias of Vine Reviews
![Del 2 _dataset_dataframe](https://user-images.githubusercontent.com/92903447/155858879-9371a77d-036c-46be-a406-1a157827cfa3.png)
![helpful_votes_50 -_plus](https://user-images.githubusercontent.com/92903447/155858884-9f2b39f4-3777-4976-aee0-cfc63e846e61.png)

### How many Vine reviews and non-Vine reviews were there?


![Del2_filtered DataFrame_paid vine program](https://user-images.githubusercontent.com/92903447/155858865-247194e8-68b6-4d28-b8c6-4e2acb4fc0f7.png)


### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
![total number of revies, nmber of star reviews of paid and unpaid](https://user-images.githubusercontent.com/92903447/155859089-aa68e43f-b2b4-4ca6-af1e-d05c0fda1925.png)


### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
![5 star paid reviews](https://user-images.githubusercontent.com/92903447/155859105-0956dc98-57e4-4af8-bbaa-f6ea55fea9e6.png)
ercentage of non-Vine reviews were 5 stars?
![5 star percentage unpaid vine program](https://user-images.githubusercontent.com/92903447/155859110-087ec607-54d5-4581-aedc-734f8dba0307.png)


# Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.

