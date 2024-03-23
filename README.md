# crowdfunding_ETL
## Project Description:
We will execute an ETL pipeline on a crowdfunding dataset containing backer information. This dataset will be migrated from an Excel file format into a PostgreSQL relational database management system (RDBMS). The ETL process will leverage Python for data extraction and transformation tasks. This includes procedures like reading the Excel file, handling potential data inconsistencies, and performing necessary data cleaning. Subsequently, SQL will be employed to load the transformed data into the PostgreSQL database. 

## Crowdfunding ETL pipeline objectives:
1.	Extract data by using Python and Pandas.
2.	Transform and clean data by using Python and Pandas.
3.	Parse string data into a Python dictionary.
4.	Use list comprehensions to make code more readable.
5.	Use regular expressions to manipulate string data.
6.	Using transformed data create four .csv files create an ERD table schema.
7.	Upload .csv files data into a Postgres database.

### Instructions:
* Create the Category and Subcategory DataFrames
* Create the Campaign DataFrame
* Create the Contacts DataFrame
* Create the Crowdfunding Database



## Creating the Category and Subcategory DataFrames

-- import crowdfunding.xlsx
--make a "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories.
--make a "category" column that contains only the category titles.
--export DataFrame as category.csv
--do the same actions for “subcategory”
--export DataFrame as subcategory.csv

## Create the Campaign DataFrame:
--rename column titles, convert data type to “float”, convert UTC times to “datetime” format, merge Category and Subcategory Dataframes into the Campaign DataFrame.
--export DataFrame as campaign.csv.

## Create the Contacts DataFrame
--import contacts.xlsx
--iterate through the Dataframe, converting each row to a dictionary
--iterate through each dictionary to:
		-extract dictionary values from the keys using Python list comprehension
		-add the values for each row to a new list
--create new DataFrame that contains extracted data.
--split each “name” column value into a first and last name and place each in a new column.
--clean Dataframe, by reordering and dropping columms
--export DataFrame as contacts.csv

## Create the Crowdfunding Database:
--inspect the four .csv files create and sketch an ERD of the tables using QuickDBD
--Use information from the ERD to create table schema for each .csv file
--Upload ERD table schema to Postgres 
--using the database schema create tables in the correct order to handle the foreign keys
--verify table creation by running a “select” statement
--import each .csv file into It’s corresponding SQL table
--verify each table has the correct data by running a “select” statement.
