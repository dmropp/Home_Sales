# Home_Sales

README for the Home Sales Spark challenge. The purpose of the project is to evaluate run times of Spark SQL queries for uncached, cached, and partitioned tables. The project was completed in Google Colab.

Home sales data was ready into a Spark data frame and a temporary table was created to evaluate the following questions utilizing Spark SQL queries:

* What is the average price of a four bedroom home grouped by year sold?
* What is the average price for homes with 3 beds and 3 baths grouped by year built?
* What is the average price for homes with 3 beds, 3 baths, 2 floors, and has 2000 square feet or more of living space, grouped by year built?
* What is the average price homes costing $350,000 or more, grouped by view rating?

The temporary table was then cached and the runtime for the last query was evaluated and compared against the unchached table run time. The data was then parquetted and partitioned by the date_built columnn. The last query was then run again to evaluate the run time for the parquet data vs cached vs uncached. 

## Run Times

* Uncached - 0.89 seconds
* Cached - 0.31 seconds
* Partitioned - 0.51 seconds
