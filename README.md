# Project 1: Deforestation Exploration 🪓🌲🌳🌴🪚
This project demonstrates the practical use of SQL for data analysis.

Project overview
Global deforestation is an increasingly growing concern. This project includes data from the World Bank 🌍 on global deforestation from the year 1990 to 2016. Results of the analysis are presented in this report.

Running queries on local machine (Mac)
Install PostgreSQL: https://www.postgresql.org
Open terminal and change directory where the project is located:
shell cd local_path/Deforestation-Exploration

Update file path in ForestDDL.sql for the following files:
'/absolute_path/Deforestation-Exploration/db_files/forest_area.csv'
'/absolute_path/Deforestation-Exploration/db_files/land_area.csv'
'/absolute_path/Deforestation-Exploration/db_files/regions.csv'
Run the command for creating a database, loading data from CSV files and creating a view:
shell sh create_db.sh

If the command was successful you should receive the following response:

CREATE DATABASE
CREATE TABLE
CREATE TABLE
CREATE TABLE
COPY 5886
COPY 5886
COPY 219
CREATE VIEW
Now you are ready to run queries!
psql -d deforestation -f ForestQuery.sql
Project tasks
JOIN TABLES AND CREATE VIEW

Create a View called “forestation” by joining all three tables - forest_area, land_area and regions in the workspace.

The forest_area and land_area tables join on both country_code AND year.

The regions table joins these based on only country_code.

In the ‘forestation’ View, include the following:

All of the columns of the origin tables
A new column that provides the percent of the land area that is designated as forest.
Keep in mind that the column forest_area_sqkm in the forest_area table and the land_area_sqmi in the land_area table are in different units (square kilometers and square miles, respectively), so an adjustment will need to be made in the calculation you write (1 sq mi = 2.59 sq km).

PART 1 - GLOBAL SITUATION

What was the total forest area (in sq km) of the world in 1990? Please keep in mind that you can use the country record denoted as “World" in the region table.
What was the total forest area (in sq km) of the world in 2016? Please keep in mind that you can use the country record in the table is denoted as “World.”
What was the change (in sq km) in the forest area of the world from 1990 to 2016?
What was the percent change in forest area of the world between 1990 and 2016?
If you compare the amount of forest area lost between 1990 and 2016, to which country's total area in 2016 is it closest to?
PART 2 - REGIONAL OUTLOOK

What was the percent forest of the entire world in 2016? Which region had the HIGHEST percent forest in 2016, and which had the LOWEST, to 2 decimal places?

What was the percent forest of the entire world in 1990? Which region had the HIGHEST percent forest in 1990, and which had the LOWEST, to 2 decimal places?

Based on the table you created, which regions of the world DECREASED in forest area from 1990 to 2016?

PART 3 COUNTRY-LEVEL DETAIL

Which 5 countries saw the largest amount decrease in forest area from 1990 to 2016? What was the difference in forest area for each?

Which 5 countries saw the largest percent decrease in forest area from 1990 to 2016? What was the percent change to 2 decimal places for each?

If countries were grouped by percent forestation in quartiles, which group had the most countries in it in 2016?

List all of the countries that were in the 4th quartile (percent forest > 75%) in 2016.

How many countries had a percent forestation higher than the United States in 2016?

