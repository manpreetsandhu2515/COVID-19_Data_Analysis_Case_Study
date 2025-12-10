# COVID-19_Data_Analysis_Case_Study
Overview

The COVID-19 pandemic, caused by the SARS-CoV-2 virus, emerged in late 2019 and rapidly spread across the globe, resulting in severe health, economic, and social impacts.
This unprecedented crisis highlighted the importance of data-driven decision making in controlling pandemics.

By tracking and analyzing data on confirmed cases, recoveries, and deaths, policymakers and health professionals can make informed decisions to mitigate the spread of the virus and allocate resources efficiently.

Dataset Details

This case study uses three time-series datasets (from Johns Hopkins CSSE), each providing daily cumulative data for different countries and regions:

1. Confirmed Cases Dataset

Contains cumulative confirmed COVID-19 cases per day.

Covers: Jan 22, 2020 → May 29, 2021

Includes 276+ geographic regions.

2. Deaths Dataset

Contains cumulative COVID-19-related deaths.

Structured similarly to confirmed cases.

3. Recovered Cases Dataset

Contains cumulative recovered patient counts.

Essential for understanding recovery trends and treatment outcomes.

Common Columns

Each dataset includes:

Province/State

Country/Region

Latitude (Lat)

Longitude (Long)

Daily cumulative counts across dates

Objective of the Case Study
1. Practical Application of Python

Use Python libraries (Pandas, NumPy, Matplotlib) for:

Data loading

Data cleaning

Data transformation

Data visualization

2. Insightful Data Analysis

Generate insights into the spread, recovery, and mortality associated with COVID-19 across different countries and timelines.

3. Skill Development

Strengthen knowledge in:

Data manipulation

Handling missing values

Merging datasets

Time-series analysis

Exploratory Data Analysis (EDA)

Analysis Questions
1. Data Loading

Load COVID-19 datasets (confirmed, deaths, recovered) using Pandas.

2. Data Exploration

Examine dataset shape (rows, columns).

Inspect data types.

Display first and last few rows.

Generate:

Plots of confirmed cases over time for top affected countries

Plot of confirmed cases over time for China

3. Handling Missing Data

Identify missing values.

Impute using forward fill (ffill) for time-series continuity.

4. Data Cleaning

Replace blank values in Province/State column with "All Provinces".

Independent Dataset Analysis
5. Daily Peak of New Cases

Analyze Germany, France, Italy:

Compute daily new cases

Identify:

Peak daily increase

Date of occurrence

Determine which country had the highest single-day surge.

6. Recovery Rate Comparison

Recovery Rate = recoveries / confirmed cases
Compare:

Canada

Australia
(as of Dec 31, 2020)
Identify which country performed better.

7. Death Rate Distribution in Canada

Death Rate = deaths / confirmed cases

Compute death rates for all provinces.

Identify:

Province with highest death rate

Province with lowest death rate

Data Transformation
8. Transform Deaths Dataset (Wide → Long Format)

Convert date columns into rows using Pandas melt()
Ensure:

Date column is datetime type

One row = one date per country

9. Total Deaths per Country

Calculate cumulative deaths for every country.

10. Top 5 Countries by Average Daily Deaths

Compute daily deaths → get average → rank top 5.

11. Evolution of Deaths in the United States

Plot cumulative total deaths over time.

Data Merging
12. Merge Datasets

Merge confirmed, deaths, recoveries into a single dataset on:

Country/Region

Date

13. Monthly Aggregation (Global)

For each country:

Monthly sum of:

Confirmed cases

Deaths

Recoveries

14. Monthly Analysis for USA, Italy, Brazil

Repeat the monthly aggregation for:

United States

Italy

Brazil

Combined Data Analysis
15. Highest Average Death Rates in 2020

Identify top 3 countries with maximum:
Death Rate = deaths / confirmed
Interpret what this indicates about healthcare stress, reporting accuracy, or outbreak intensity.

16. South Africa: Recoveries vs Deaths

Compare totals to understand:

Outcome severity

Healthcare success rate

17. US Recovery Ratio (Monthly)

Recovery Ratio = recoveries / confirmed
Analyze from March 2020 → May 2021
Identify:

Month with highest recovery ratio

Potential reasons (e.g., vaccination rollouts, treatment improvements)
