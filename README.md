# Crowdfunding_ETL
-Keegan Nair
-Mandeep Sohi

Run code in ETL_Mini_project


We have used option 1 for extracting and transforming the data from contact excel file.


Once code has been run and CSV files have been exported (there should be 4), go into pg-admin.


Run the code in the file crowdfunding_db_schema. Do not run the sections with constraints to avoid error issues. Instead run the code to make the tables then import the csv files per table.


Then run constraint code to show how each table connects eg; one to many.


The Schema code came from the ERD application and example of how it looks can be found in QuickDBD-diagram.



# ETL  Crowdfunding Mini Project

Overview

This project involves building an ETL (Extract, Transform, Load) pipeline using Python, Pandas, and either Python dictionary methods or regular expressions. The goal is to process crowdfunding data from Excel files, transform the data into structured CSV files, and load it into a PostgreSQL database.

Technologies Used

- Python

- Pandas

- Regular Expressions (Regex)

- PostgreSQL

- QuickDBD (for ERD visualization)

- GitHub

## Project Workflow

- The project is divided into four main steps:


## 1. Create the Category and Subcategory DataFrames

Extract and transform data from crowdfunding.xlsx to create a category DataFrame with:

category_id: Sequential entries from cat1 to catn (where n is the number of unique categories).

category: Category titles.

Save the category DataFrame as category.csv and upload it to GitHub.

Extract and transform data to create a subcategory DataFrame with:

subcategory_id: Sequential entries from subcat1 to subcatn (where n is the number of unique subcategories).

subcategory: Subcategory titles.

Save the subcategory DataFrame as subcategory.csv and upload it to GitHub.


## 2. Create the Campaign DataFrame

Extract and transform data from crowdfunding.xlsx to create a campaign DataFrame with:

cf_id

contact_id

company_name

description (renamed from blurb)

goal (converted to float)

pledged (converted to float)

outcome

backers_count

country

currency

launch_date (converted from UTC timestamp)

end_date (converted from UTC timestamp)

category_id (matching the category_id from the category DataFrame)

subcategory_id (matching the subcategory_id from the subcategory DataFrame)

Save the campaign DataFrame as campaign.csv and upload it to GitHub.

## 3. Create the Contacts DataFrame

Python Dictionary Method

Import contacts.xlsx into a DataFrame.

Iterate through the DataFrame, converting each row to a dictionary.

Extract dictionary values using list comprehension and create a new DataFrame.

Split name column into first_name and last_name.

Clean and export the DataFrame as contacts.csv.

Save the contacts.csv file to GitHub.


## 4. Create the Crowdfunding Database

Inspect the four CSV files and sketch an ERD using QuickDBD.

Create a PostgreSQL database schema with:

Data types, primary keys, foreign keys, and constraints.

Save the schema as crowdfunding_db_schema.sql and upload it to GitHub.

Create a PostgreSQL database (crowdfunding_db).

Create tables in the correct order to handle foreign keys.

Verify table creation with SELECT statements.

Import CSV files into respective tables.

Run SELECT statements to verify the imported data.



## Contributors

- Keegan Nair

- Mandeep Sohi
