# COVID-19 Analysis  
## Data Exploration (SQL) and Data Visualization (Tableau)

### Project Overview

This project explores COVID-19 data using SQL to analyze various metrics such as infection rates, death rates, and vaccination progress. It applies key SQL techniques including:

- Joins (to combine data from different tables)  
- Common Table Expressions (CTEs) for readability and reusability  
- Temporary Tables to store intermediate results  
- Window Functions for rolling calculations  
- Aggregate Functions to compute totals and averages  
- Data Type Conversion to ensure proper calculations  
- Views for efficient data retrieval in visualization tools like Tableau

This project was inspired by Alex The Analyst’s COVID Portfolio Projects (1 & 2).

---

### Dataset

The data is sourced from two primary tables:

**1. CovidDeath** – Contains COVID-19 case and death statistics by country and date.  
**2. CovidVaccinations** – Contains vaccination data by country and date.

---

### SQL Queries for Data Exploration

**1. Data Exploration**  
Retrieves all available data from the `CovidDeath` table where the `continent` field is not null, excluding aggregated global statistics.

**2. Initial Data Selection**  
Extracts key columns such as location, date, total_cases, new_cases, total_deaths, and population.

**3. Total Cases vs Total Deaths**  
Calculates the death percentage per country to assess the likelihood of dying after contracting COVID-19.

**4. Total Cases vs Population**  
Determines the percentage of each country’s population infected with COVID-19.

**5. Countries with Highest Infection Rates**  
Identifies the countries with the highest total infection rates relative to their populations.

**6. Countries with Highest Death Count per Population**  
Determines the total number of deaths per country, sorted in descending order.

**7. Death Count Breakdown by Continent**  
Aggregates the highest death count per continent.

**8. Global Statistics**  
Computes total new cases and deaths worldwide, along with the global death percentage.

**9. Total Population vs Vaccinations**  
Uses window functions to calculate rolling vaccination numbers per country.

**10. Using CTEs for Vaccination Calculations**  
Creates a Common Table Expression (PopvsVac) to calculate the rolling number of vaccinated individuals by country.

**11. Using Temporary Tables for Vaccination Calculations**  
Implements a temporary table (`#PercentPopulationVaccinated`) to compute the percentage of vaccinated individuals.

**12. Creating a View for Tableau Visualization**  
Defines a view (`PercentPopulationVaccinated`) to facilitate data access and integration with Tableau.

---

### SQL Queries for Tableau Data Visualization

**1. Global COVID-19 Impact**  
Calculates total cases, total deaths, and the death percentage worldwide.

**2. Total Death Count per Location**  
Aggregates the total number of deaths per location while excluding continents and global summary rows.

**3. Highest Infection Rates**  
Identifies locations with the highest infection rates relative to their populations.

**4. Infection Trends Over Time**  
Tracks infection rate changes by location over time.

**5. Vaccination Progress**  
Joins vaccination data with case statistics to analyze the proportion of vaccinated individuals in each country.

**6. Population vs Vaccination Analysis**  
Uses CTEs to calculate rolling vaccination rates and assess their impact on infection trends.

**7. Death Rate Trends**  
Analyzes how death rates have evolved over time across different regions.

---

### Results

- Infection and death rates vary widely across countries and continents, reflecting diverse pandemic impacts.  
- Certain countries exhibit high infection rates relative to population size, indicating significant spread.  
- Death rates show disparities influenced by healthcare capacity and demographics.  
- Vaccination progress has steadily increased, with rolling calculations highlighting trends in vaccine uptake by country.  
- Integration of vaccination data with infection trends provides insights into pandemic control effectiveness.

---

### Recommendations

- Use rolling vaccination metrics to prioritize countries or regions for targeted vaccination campaigns.  
- Monitor infection and death trends to allocate healthcare resources effectively.  
- Enhance data automation through stored procedures and triggers for timely updates.  
- Incorporate advanced analytics with Python to forecast future waves and vaccination needs.

---

### Technologies Used

- SQL Server Management Studio (SSMS) or any SQL-based RDBMS  
- Tableau for interactive dashboards and data visualizations

---

### How to Use

- Run the SQL queries in your SQL environment.  
- Use the final view (`PercentPopulationVaccinated`) as a data source in Tableau.  
- Analyze the derived insights and visualize them through dashboards.

---

### Future Improvements

- Enhance the project with stored procedures for automation.  
- Implement database triggers for real-time updates.  
- Integrate Python for advanced statistical analysis and forecasting.

---

**Author:** Abdelrahman Elkeshky  
**Inspired by:** Alex The Analyst (COVID Portfolio Project 1 & 2)
