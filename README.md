# The Pulse of a State: Diabetes Analytics Across Florida

## Data Warehousing and Analytics Project (2014–2023)

This project analyzes diabetes hospitalization trends across Florida counties using a dimensional data warehouse. It examines how income, education, obesity, smoking, and physical inactivity influence diabetes-related hospitalizations and highlights persistent public health disparities across regions.

Detailed analysis, data modeling, and findings are documented in the final project report. :contentReference[oaicite:0]{index=0}

---

## Project Objectives

- Design and implement a data warehouse
- Apply OLTP and OLAP modeling concepts
- Perform SQL-based analytical queries
- Create analytical dashboards using Tableau
- Identify high-risk counties and long-term trends

---

## Data Sources

- Florida Health CHARTS – Diabetes hospitalization rates  
- U.S. Census Bureau (SAIPE) – Median household income and poverty estimates  
- American Community Survey (ACS) – Educational attainment  
- County Health Rankings – Obesity, smoking, and physical inactivity indicators  

All datasets are standardized at the county–year level (2014–2023).

---

## Data Warehouse Architecture

### OLTP Model
Represents source-system healthcare data:
- Patients
- Visits
- Diagnoses
- Hospitals
- Counties
- Dates
- Income and education attributes

### OLAP Model (Star Schema)

Optimized for analytics and reporting.

**Fact Table**
- FACT_DIABETES  
  - Hospitalization count  
  - Diabetes rate  
  - Rate per 100,000 population  

**Dimension Tables**
- DIM_COUNTY  
- DIM_TIME  
- DIM_INCOME  
- DIM_EDUCATION  
- DIM_HEALTHBEHAVIOR  

Grain: One record per county per year  
Slowly Changing Dimensions: Type 2 (historical tracking by year)

---

## ETL and Data Preparation

- Cleaned and standardized county names and year formats
- Normalized metrics to rates per 100,000 population
- Integrated datasets using county and year as primary keys
- Validated joins, row counts, and data consistency
- Loaded fact and dimension tables using SQL

---

## Analysis and Insights

SQL-based analysis includes:
- Top counties by diabetes hospitalization rates
- Obesity, smoking, and physical inactivity trend analysis
- Correlation between income and hospitalization rate (negative relationship)
- Correlation between education and hospitalization rate (positive but weaker relationship)
- Year-over-year hospitalization rate improvements
- Risk quartile classification using NTILE

---

## Visualization

Tableau dashboards were developed to:
- Compare diabetes hospitalization rates across counties
- Track trends over time
- Identify persistent high-risk regions
- Visualize socioeconomic and lifestyle impacts

---

## Key Findings

- Counties with lower income levels show higher diabetes hospitalization rates
- Obesity and smoking strongly correlate with hospitalization outcomes
- Rural counties frequently appear in the highest-risk quartiles
- Florida’s overall diabetes hospitalization rate has declined over time
- Significant health disparities persist across counties

---

## Tools and Technologies

- SQL (Oracle)
- Data Warehousing and Dimensional Modeling
- Tableau
- Public health open datasets

---

## Future Enhancements

- Integrate insurance coverage and hospital capacity data
- Add predictive modeling for hospitalization trends
- Automate ETL pipelines
- Expand demographic and social determinants data
