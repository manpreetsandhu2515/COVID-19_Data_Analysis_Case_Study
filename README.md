<img width="300" height="150" alt="image" src="https://github.com/user-attachments/assets/b29fddb6-0191-4a34-81d0-91437d143a54" />

# COVID-19_Data_Analysis_Case_Study

## Overview
The COVID-19 pandemic, caused by the SARS-CoV-2 virus, emerged in late 2019 and rapidly spread worldwide, causing severe health, economic, and social disruption. This crisis emphasized the importance of data analysis for tracking disease spread, understanding trends, and supporting government and healthcare decisions.

By analyzing confirmed cases, recoveries, and deaths, this project demonstrates how data can guide policy-making and resource allocation during a global health emergency.
---
## Dataset Details

This project uses three daily-updated global datasets from the Johns Hopkins University CSSE repository:

### 1. Confirmed Cases Dataset
- Cumulative confirmed COVID-19 cases per day  
- Time period: **January 22, 2020 → May 29, 2021**  
- 276+ geographic entries  

### 2. Deaths Dataset
- Cumulative COVID-19 deaths per day  
- Same structure as the confirmed dataset  

### 3. Recovered Cases Dataset
- Cumulative recovered cases per day  
- Used to analyze recovery performance and disease outcomes  

### Common Columns
All datasets include:
- Province/State  
- Country/Region  
- Latitude (Lat)  
- Longitude (Long)  
- Date-wise cumulative counts  
--
## Objectives of the Case Study

### 1. Practical Python Application
Use:
- **Pandas** for data manipulation  
- **NumPy** for numerical operations  
- **Matplotlib** for visualizations  

### 2. Insightful Data Analysis
Understand:
- Spread trends  
- Mortality variations  
- Recovery performance across countries  

### 3. Skill Development
Hands-on practice with:
- Data cleaning  
- Handling missing values  
- Time-series analysis  
- Merging datasets  
- Exploratory Data Analysis (EDA)  
---
# Analysis Questions
## 1. Data Loading
- Load confirmed, deaths, and recovered datasets using Pandas.
---
## 2. Data Exploration
- View dataset shape, columns, and datatypes  
- Display sample rows  
- Generate:
  - Confirmed cases over time for **top countries**
  - Confirmed cases over time for **China**
---
## 3. Handling Missing Data
- Identify NaN values  
- Apply **forward fill (ffill)** for time-series imputation  
---
## 4. Data Cleaning
- Replace empty values in `Province/State` with **"All Provinces"**
---
# Independent Dataset Analysis

### 5. Peak Daily New Cases (Germany, France, Italy)
- Compute daily new cases  
- Identify the largest single-day spike  
- Determine which country had the **highest surge** and on which date  
---
### 6. Recovery Rate Comparison
**Recovery Rate = recoveries / confirmed cases**

Compare:
- **Canada vs Australia**
As of **December 31, 2020**
---
### 7. Death Rate Distribution in Canada
**Death Rate = deaths / confirmed cases**

Find:
- Province with **highest** death rate  
- Province with **lowest** death rate  
---
# Data Transformation

### 8. Wide → Long Format Conversion (Deaths Dataset)
Use Pandas `melt()` to convert date columns into rows:
- Columns: Country/Region, Province/State, Date, Death Count  
- Convert `Date` to `datetime` format  
---
### 9. Total Deaths per Country
Calculate cumulative deaths for all countries.
---
### 10. Top 5 Countries by Average Daily Deaths
- Compute daily deaths  
- Calculate averages  
- Pick top 5 countries  
---
### 11. Total Deaths Over Time in the United States
- Plot cumulative deaths over time  
---
# Data Merging

### 12. Merge Datasets
Merge confirmed, deaths, and recovered datasets on:
- `Country/Region`
- `Date`

Result: A unified dataset showing complete pandemic statistics.
---
### 13. Monthly Aggregation (All Countries)
For each country:
- Monthly **confirmed cases**  
- Monthly **deaths**  
- Monthly **recoveries**  
---
### 14. Monthly Analysis for USA, Italy, Brazil
Repeat the above monthly aggregation for:
- United States  
- Italy  
- Brazil  
---
# Combined Data Analysis

### 15. Highest Average Death Rates in 2020
**Death Rate = deaths / confirmed cases**

- Identify 3 countries with the highest average death rates  
- Interpret what this indicates about outbreak severity, healthcare stress, or reporting accuracy  
---
### 16. South Africa: Recoveries vs Deaths
Compare:
- Total recoveries  
- Total deaths  

Interpret what this reveals about case outcomes.
---
### 17. United States Monthly Recovery Ratio
**Recovery Ratio = recoveries / confirmed cases**

Analyze from **March 2020 → May 2021**:
- Identify month with **highest recovery ratio**
- Discuss potential reasons (e.g., vaccination, treatment improvements)
---
