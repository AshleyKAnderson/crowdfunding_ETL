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

* import crowdfunding.xlsx
* make a "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories.
* make a "category" column that contains only the category titles.
* export DataFrame as **[category.csv](https://github.com/AshleyKAnderson/crowdfunding_ETL/blob/0d4abb8dcdccb92665dd0449f13e404afc3f4412/Resources/category.csv)**
* do the same actions for “subcategory”
* export DataFrame as **[subcategory.csv](https://github.com/AshleyKAnderson/crowdfunding_ETL/blob/d4170d535a4de3e6e28d1d01528f91b4cf34da45/Resources/subcategory.csv)**.

## Create the Campaign DataFrame:
* rename column titles, convert data type to “float”, convert UTC times to “datetime” format, merge Category and Subcategory Dataframes into the Campaign DataFrame.
* export DataFrame as **[campaign.csv](https://github.com/AshleyKAnderson/crowdfunding_ETL/blob/0d4abb8dcdccb92665dd0449f13e404afc3f4412/Resources/campaign.csv)**.

## Create the Contacts DataFrame
* import contacts.xlsx
* iterate through the Dataframe, converting each row to a dictionary
* iterate through each dictionary to:
  * extract dictionary values from the keys using Python list comprehension
  * add the values for each row to a new list
* create new DataFrame that contains extracted data.
* split each “name” column value into a first and last name and place each in a new column.
* clean Dataframe, by reordering and dropping columms
* export DataFrame as **[contacts.csv](https://github.com/AshleyKAnderson/crowdfunding_ETL/blob/0d4abb8dcdccb92665dd0449f13e404afc3f4412/Resources/contacts.csv)**

## Create the Crowdfunding Database:
* inspect the four .csv files create and sketch an ERD of the tables using QuickDBD
* Use information from the ERD to create table schema for each .csv file
* ![ERD_snapshot](https://github.com/AshleyKAnderson/crowdfunding_ETL/assets/153468339/873a6d58-8593-4b66-beba-a2fbfcdba2ff)
* Upload ERD table schema to Postgres 
* using the database schema create tables in the correct order to handle the foreign keys
* <img width="732" alt="Screenshot 2024-03-21 211714" src="https://github.com/AshleyKAnderson/crowdfunding_ETL/assets/153468339/9eac77ff-1baa-482a-8af2-e621a9b99722">
* verify table creation by running a “select” statement
* import each .csv file into It’s corresponding SQL table
* verify each table has the correct data by running a “select” statement.
* CATEGORY TABLE VERIFY SCREENSHOT
<img width="732" alt="Screenshot 2024-03-21 211714" src="https://github.com/AshleyKAnderson/crowdfunding_ETL/assets/153468339/9deccab2-24a6-4ba5-987e-9b4e8a67658b">
* SUBCATEGORY TABLE VERIFY SCREENSHOT
<img width="727" alt="Screenshot 2024-03-21 211826" src="https://github.com/AshleyKAnderson/crowdfunding_ETL/assets/153468339/6b92e934-3554-448c-8140-3daaac085645">
* CAMPAIGN TABLE VERIFY SCREENSHOT
<img width="960" alt="Screenshot 2024-03-21 211925" src="https://github.com/AshleyKAnderson/crowdfunding_ETL/assets/153468339/dd5698dc-203f-4e2e-b270-d70983d93e13">
* CONTACTS TABLE VERIFY SCREENSHOT
<img width="725" alt="Screenshot 2024-03-21 212015" src="https://github.com/AshleyKAnderson/crowdfunding_ETL/assets/153468339/fbf12ab3-8eb7-4c85-9fcb-242317913200">

