# Home_Sales
Overview

used home sales data as a csv file from AWS S3 bucket
In this assignment home sale prices were compared in different years. Prices have changed with number of bedrooms, number of bathrooms, living space and lot size.
Used spark sql, temporaryview, parquet concept to perform this analysis.

Data analysis using SQL Queries

1. average price for a four-bedroom house sold for each year 
2. average price of a home for each year the home was built, that has three bedrooms and three bathrooms
3. average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet
4. average price of a home per "view" rating having an average home price greater than or equal to $350,000


caching and checking the status of temporary table whether it is cached.

Ran one of the sql query(average price of a home per "view" rating having an average home price greater than or equal to $350,000) to determine the runtime

Partioned using date_built field on the formatted parquet home sale data

Created temporary table for the parquet data

Ran the same query to determine and compare the runtime

Uncashed the temporary table and varified is it uncached.

Conclusion

Caching and partitioning the table reduce runtime compared to run on tempviews. This is because when we cache data saved on our local memory so every time it does not go to cloud to extract data.
In this example runtime is slightly reduced becuase of the size the data if this is a scenario in a bigdata like size of terrabite or pentabite it will considerably save time as well as resources.

