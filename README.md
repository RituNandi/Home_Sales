# Home_Sales


## Project Description

In this project, SparkSQL was employed to determine key metrics about home sales data. The utilization of SparkSQL involved various operations such as creating temporary views, partitioning the data, caching and uncaching a temporary table, and verifying that the table has been uncached.

## Data

Dataset used in this project - [Home Sales Data](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv)

## Analysis

**Query 1**: Average price for a four-bedroom house sold for each year

`+----+---------+<br>
|year|avg_price|<br>
+----+---------+<br>
|2019| 300263.7|<br>
|2020|298353.78|<br>
|2021|301819.44|<br>
|2022|296363.88|<br>
+----+---------+<br>`

**Query 2**: Average price of a home for each year it was built that has three bedrooms and three bathrooms

+----------+---------+<br>
|year_built|avg_price|<br>
+----------+---------+<br>
|      2010|292859.62|<br>
|      2011|291117.47|<br>
|      2012|293683.19|<br>
|      2013|295962.27|<br>
|      2014|290852.27|<br>
|      2015| 288770.3|<br>
|      2016|290555.07|<br>
|      2017|292676.79|<br>
+----------+---------+<br>

**Query 3**: Average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet

+----------+---------+<br>
|year_built|avg_price|<br>
+----------+---------+<br>
|      2010|285010.22|<br>
|      2011|276553.81|<br>
|      2012|307539.97|<br>
|      2013|303676.79|<br>
|      2014|298264.72|<br>
|      2015|297609.97|<br>
|      2016| 293965.1|<br>
|      2017|280317.58|<br>
+----------+---------+<br>

**Query 4**: Average price of a home per "view" rating having an average home price greater than or equal to $350,000

+----+----------+<br>
|view| avg_price|<br>
+----+----------+<br>
|  99|1061201.42|<br>
|  98|1053739.33|<br>
|  97|1129040.15|<br>
|  96|1017815.92|<br>
|  95| 1054325.6|<br>
|  94| 1033536.2|<br>
|  93|1026006.06|<br>
|  92| 970402.55|<br>
|  91|1137372.73|<br>
|  90|1062654.16|<br>
|  89|1107839.15|<br>
|  88|1031719.35|<br>
|  87| 1072285.2|<br>
|  86|1070444.25|<br>
|  85|1056336.74|<br>
|  84|1117233.13|<br>
|  83|1033965.93|<br>
|  82| 1063498.0|<br>
|  81|1053472.79|<br>
|  80| 991767.38|<br>
+----+----------+<br>
only showing top 20 rows<br>
<br>
<br>
**Compare Run Times on Query 4**

1. Uncache Runtime: 1.2677862644195557 seconds<br>
2. Cached Runtime: 0.6058557033538818 seconds<br>
3. Runtime with the parquet (Partition by the "date_built" field) DataFrame: 1.1717925071716309 seconds<br>
