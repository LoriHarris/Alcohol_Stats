# Alcohol_Stats

## Final report

### By Brianna, Lori, Rachel

#### We took a look at data related to Alcohol consumption from various data sources on a variety of scales: Global, National, and North Carolina/County Levels. Multi-year data is available and could be used to look for trends and for comparing across different locales. 

##### The sources of data 
We extracted data from publically available data sources including:
 - RWJ Foundation 2018 County Health Rankings (xls/csv)
 - FiveThirtyEight Drug Use by Age Dataset (xls/csv)
 - WHO Recorded alcohol per capita consumption (json)
 - 2016-2017 National Survey on Drug Use and Health (NSDUH) State Prevalence Estimates (xls/csv)
 - International Alliance fo Responsible Drinking (scrape table legal limits)

##### **Extraction**
Data in .xls files were converted to .csv files, manually and with by employing csv code. A table was scraped using BeautifulSoup. JSON data, along with scraped tables and .csv files were read into a pandas DataFrame.


##### **Transform**

Once the DataFrames were created, the data needed to then be transformed before loading into a database. Cleaning the data included dropping columns and renaming column headers (for example, eliminating spaces so columns could be easily referenced). Duplicates were dropped as needed to prevent conflicts. Some data was merged to create new tables with desired database variables. Indices were assigned in tables for referencing and primary keys were set for creating joins between database tables.

##### **Load**

Data was loaded into a final production relational database and MySQL was use to create the database, tables and set schema. Data was loaded into the database by creating a connection and reading data from the DataFrame, utilzing the indices that were previously set during data transformation. We were able to confirm that the data had successfuly been loaded by querying the database. 

