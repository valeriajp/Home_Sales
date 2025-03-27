# Home_Sales

![2211 i105 038 S m005 c13 isometric family moving illustration](https://github.com/user-attachments/assets/b884f200-a35b-436c-9f52-ea062294d4f8)

In this challenge, you'll use your knowledge of SparkSQL to determine key metrics about home sales data. Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

# **Before You Begin**
Create a new repository for this project called, ![image](https://github.com/user-attachments/assets/72b81464-1ed1-4851-bd89-cb5d8bf5d230). Do not add this homework to an existing repository.

Clone the new repository to your computer.

Push your changes to GitHub.

# **Instructions**
1. Rename the ![image](https://github.com/user-attachments/assets/0f6ecfce-6b7c-45ca-ac1b-e8277bf50601) file as ![image](https://github.com/user-attachments/assets/d12b1b76-43fb-4b50-bfcc-74baace01506).

2. Import the necessary PySpark SQL functions for this assignment.

3. Read the ![image](https://github.com/user-attachments/assets/b5d08747-bd9c-4a0a-b258-1ae4947d8022) from the provided AWS S3 bucket location into a PySpark DataFrame.

4. Create a temporary table called ![image](https://github.com/user-attachments/assets/21819165-0d79-4c0e-adca-c12b7fcd500a).

5. Answer the following questions using SparkSQL:

  - What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
  - What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
  - What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
  - What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

6. Cache your temporary table ![image](https://github.com/user-attachments/assets/a3315b7e-85bc-4f03-8f79-db297ea321f4).
7. Check if your temporary table is cached.
8. Using the cached data, run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
9. Partition by the "date_built" field on the formatted parquet home sales data.
10. Create a temporary table for the parquet data.
11. Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
12. Uncache the ![image](https://github.com/user-attachments/assets/64fac1e1-9090-47e2-bf64-a33e555e7ed9) temporary table.
13. Verify that the ![image](https://github.com/user-attachments/assets/c1c63b31-3809-4b53-994b-f0d73997cdd3) temporary table is uncached using PySpark.
14. Download your ![image](https://github.com/user-attachments/assets/730cf0b1-554a-46c9-8b59-da17e6ca07f9) file and upload it into your "Home_Sales" GitHub repository.

# **Support and Resources**
Your instructional team will provide support during classes and office hours. You will also have access to learning assistants and tutors to help you with topics as needed. Make sure to take advantage of these resources as you collaborate with your partner on this project.

# **Requirements**

1. A Spark DataFrame is created from the dataset. (5 points)
2. A temporary table of the original DataFrame is created. (10 points)
3. A query is written that returns the average price, rounded to two decimal places, for a four-bedroom house that was sold in each year. (5 points)
4. A query is written that returns the average price, rounded to two decimal places, of a home that has three bedrooms and three bathrooms for each year the home was built. (5 points)
5. A query is written that returns the average price of a home with three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet for each year the home was built rounded to two decimal places. (5 points)
6. A query is written that returns the average price of a home per "view" rating having an average home price greater than or equal to $350,000, rounded to two decimal places. (The output shows the run time for this query.) (10 points)
7. A cache of the temporary "home_sales" table is created and validated. (10 points)
8. The query from step 6 is run on the cached temporary table, and the run time is computed. (10 points)
9. A partition of the home sales dataset by the "date_built" field is created, and the formatted parquet data is read. (10 points)
10. A temporary table of the parquet data is created. (10 points)
11. The query from step 6 is run on the parquet temporary table, and the run time is computed. (10 points)
12. The "home_sales" temporary table is uncached and verified. (10 points)

# **References**
Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
