COVID-19 Data Exploration

Project Overview

This project explores COVID-19 data using SQL to analyze different metrics such as infection rates, death rates, and vaccination progress. It leverages key SQL techniques, including:

  - Joins (to combine data from different tables)

  - Common Table Expressions (CTEs) (for readability and reusability)

  - Temporary Tables (to store intermediate results)

  - Window Functions (for rolling calculations)

  - Aggregate Functions (to compute totals and averages)

  - Data Type Conversion (to ensure proper calculations)

  - Views (for efficient data retrieval in visualization tools like Tableau)

Dataset

The data comes from two tables:

  1. CovidDeath - Contains COVID-19 case and death statistics per country and date.

  2. CovidVaccinations - Contains vaccination data per country and date.

SQL Analysis

1. Data Exploration

  - Retrieves all available data from CovidDeath where the continent field is not null to exclude aggregated global statistics.

2. Initial Data Selection

  - Extracts key columns such as location, date, total_cases, new_cases, total_deaths, and population.

3. Total Cases vs Total Deaths

  - Calculates the death percentage per country to show the likelihood of dying after contracting COVID-19.

4. Total Cases vs Population

  - Determines the percentage of a country's population infected with COVID-19.

5. Countries with Highest Infection Rates

  - Identifies the countries with the highest total infection rates compared to their populations.

6. Countries with Highest Death Count per Population

  - Determines the total number of deaths per country, sorted in descending order.

7. Death Count Breakdown by Continent

  - Aggregates the highest death count per continent.

8. Global Statistics

  - Computes total new cases and deaths worldwide, along with the global death percentage.

9. Total Population vs Vaccinations

  - Uses window functions to calculate rolling vaccination numbers for each country.

10. Using CTEs for Vaccination Calculations

  - Creates a CTE (PopvsVac) to calculate the rolling number of vaccinated individuals per country.

11. Using Temporary Tables for Vaccination Calculations

  - Implements a temporary table (#PercentPopulationVaccinated) to store vaccination data and compute the percentage of vaccinated individuals.

12. Creating a View for Tableau Visualization

  - Defines a view (PercentPopulationVaccinated) to facilitate data access for visualization in Tableau.

SQL Queries for Tableau Data Visualization

1. Global COVID-19 Impact

  - Calculates total cases, total deaths, and death percentage worldwide.

2. Total Death Count per Location

  - Aggregates the total number of deaths per location while excluding continents and global summaries.

3. Highest Infection Rates

  - Identifies locations with the highest infection rates relative to their populations.

4. Infection Trends Over Time

  - Tracks infection rate changes per location over time.

5. Vaccination Progress

  - Joins vaccination data with case statistics to analyze the proportion of vaccinated individuals per population.

6. Population vs Vaccination Analysis

  - Uses CTEs to calculate rolling vaccination rates and assess their impact on infection trends.

7. Death Rate Trends

  - Analyzes how death rates evolved over time and across different regions.

Technologies Used

  1. SQL Server Management Studio (SSMS) or any SQL database system

  2. Tableau (for visualization, based on the created SQL view)

How to Use

  - Run the SQL queries in a database environment.

  - Use the final View (PercentPopulationVaccinated) as a source for Tableau visualizations.

  - Analyze insights from the queries and use visual dashboards for better representation.

Future Improvements

  - Enhance the project with stored procedures for automation.

  - Implement triggers for real-time updates.

  - Integrate Python for deeper statistical analysis and forecasting.

Author: Abdelrahman ElkeshkyProject <br>
Purpose: Data Analysis & Visualization of COVID-19 Trends
