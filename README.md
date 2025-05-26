# BIG-DATA-ANALYSIS

COMPANY: CODTECH IT SOLUTIONS

NAME: NITHIKA GUNDU

INTERN ID: CT04DN1596

DOMAIN: DATA ANALYTICS

DURATION: 4 WEEKS

MENTOR: NEELA SANTHOSH

DESCRIPTION OF THE TASK:  The exponential growth of data in recent years has made traditional data processing tools inadequate for handling large-scale datasets. To tackle this challenge, we employ PySpark, a powerful big data processing framework that leverages distributed computing for scalability and efficiency. This project demonstrates how to perform big data analysis on a large dataset using PySpark, focusing on data exploration, cleaning, scalable analytics, and insight extraction.

The analysis begins by importing essential libraries from the PySpark ecosystem. These include SparkSession, which manages the Spark context, and various functions from pyspark.sql.functions for data manipulation and aggregation. A Spark session is then initialized with specified memory configurations to ensure sufficient resources for handling the large dataset.

Next, we load a large dataset, typically in CSV format, into a Spark DataFrame. This is done using the spark.read.csv method with parameters like header=True to recognize the first row as column names and inferSchema=True to automatically detect data types. This step transforms a static data file into a distributed structure capable of being processed across multiple nodes.

Data exploration follows, where we examine the dataset’s schema, preview sample records, count the total number of records, and list available columns. This step helps in understanding the data’s structure, identifying key columns for analysis, and planning subsequent cleaning and processing steps.

In the data cleaning phase, we address missing or invalid data by dropping rows with null values in crucial columns such as passenger_count, trip_distance, and total_amount. The cleaned dataset is cached in memory to speed up further transformations and actions. We also count the remaining records after cleaning to assess data quality.

Scalable analysis is performed in three parts. First, we compute average trip distances and average total amounts grouped by the number of passengers using the groupBy and agg functions. This aggregation provides insights into typical trip characteristics across different passenger counts. Second, we identify the top 10 trips with the highest earnings by sorting the cleaned data in descending order of the total_amount column. This highlights the most lucrative trips in the dataset. Third, we analyze the distribution of trip distances by categorizing them into buckets such as <1 mile, 1-5 miles, 5-10 miles, and 10+ miles. The withColumn and when functions are used to create a new categorical column, and we then group and count the number of trips in each bucket.

The results of these analyses are saved to disk as CSV files for further use or reporting. The write.csv method ensures the outputs are stored in a structured format with headers.

Finally, the Spark session is stopped to release resources and terminate the job gracefully.

This project demonstrates the end-to-end process of performing scalable big data analysis with PySpark, including data ingestion, exploration, cleaning, aggregation, and insight extraction. It highlights PySpark's strengths in handling large datasets efficiently and producing meaningful results from complex data at scale.
