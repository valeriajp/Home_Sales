SparkSQL is used to identify important metrics related to home sales data, after which Spark is used to generate temporary views, split the data, cache and uncache a temporary table, and confirm that the table has been uncached.


![20945159](https://github.com/user-attachments/assets/d8bc57c3-d5bf-4b06-82ed-54b03c4afcf6)

What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

+----+-------------+
|YEAR|AVERAGE_PRICE|
+----+-------------+
|2022|    296363.88|
|2021|    301819.44|
|2020|    298353.78|
|2019|     300263.7|
+----+-------------+

What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
+----+-------------+
|YEAR|AVERAGE_PRICE|
+----+-------------+
|2017|    292676.79|
|2016|    290555.07|
|2015|     288770.3|
|2014|    290852.27|
|2013|    295962.27|
|2012|    293683.19|
|2011|    291117.47|
|2010|    292859.62|
+----+-------------+


What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
+----------+-------------+
|YEAR_BUILT|AVERAGE_PRICE|
+----------+-------------+
|      2017|    280317.58|
|      2016|     293965.1|
|      2015|    297609.97|
|      2014|    298264.72|
|      2013|    303676.79|
|      2012|    307539.97|
|      2011|    276553.81|
|      2010|    285010.22|
+----------+-------------+


What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

+----+-------------+
|view|AVERAGE_PRICE|
+----+-------------+
|  99|   1061201.42|
|  98|   1053739.33|
|  97|   1129040.15|
|  96|   1017815.92|
|  95|    1054325.6|
|  94|    1033536.2|
|  93|   1026006.06|
|  92|    970402.55|
|  91|   1137372.73|
|  90|   1062654.16|
|  89|   1107839.15|
|  88|   1031719.35|
|  87|    1072285.2|
|  86|   1070444.25|
|  85|   1056336.74|
|  84|   1117233.13|
|  83|   1033965.93|
|  82|    1063498.0|
|  81|   1053472.79|
|  80|    991767.38|
+----+-------------+
only showing top 20 rows

--- 1.1311416625976562 seconds ---

5. Execute the query that eliminates view ratings with an average price of $350,000 or more using the cached data. Measure the runtime and compare it to uncached runtime. Divide the structured parquet house sales data by the "date_built" field.

+----+-------------+
|view|AVERAGE_PRICE|
+----+-------------+
|  99|   1061201.42|
|  98|   1053739.33|
|  97|   1129040.15|
|  96|   1017815.92|
|  95|    1054325.6|
|  94|    1033536.2|
|  93|   1026006.06|
|  92|    970402.55|
|  91|   1137372.73|
|  90|   1062654.16|
|  89|   1107839.15|
|  88|   1031719.35|
|  87|    1072285.2|
|  86|   1070444.25|
|  85|   1056336.74|
|  84|   1117233.13|
|  83|   1033965.93|
|  82|    1063498.0|
|  81|   1053472.79|
|  80|    991767.38|
+----+-------------+
only showing top 20 rows

--- 0.7106127738952637 seconds ---

parquet data 

+----------+
|avg_price |
+----------+
|403005.77 |
|788128.21 |
|404673.3  |
|798684.82 |
|399548.12 |
|397771.65 |
|750537.94 |
|396964.5  |
|1072285.2 |
|752861.18 |
|767036.67 |
|398867.6  |
|397862.0  |
|401419.75 |
|791453.0  |
|398592.71 |
|402124.62 |
|402022.68 |
|1056336.74|
|399586.53 |
+----------+
only showing top 20 rows

--- 0.7597565650939941 seconds --

Runtimes for both the cached and Parquet-formatted data are quicker than those of the original data.

To sum up, out of the three possibilities (run time for original data, cached data, and parquet prepared data), parquet formatted data exhibits the best runtime.
