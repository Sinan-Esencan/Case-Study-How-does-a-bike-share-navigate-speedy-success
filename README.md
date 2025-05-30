# Case Study: How Does a Bike-Share Navigate Speedy Success?

## Overview

Cyclistic, a bike-share company in Chicago, has two rider types:

1. **Casual riders** (single/day passes)
2. **Annual members** (yearly subscription)

Annual memberships bring more profit. The marketing director, Lily Moreno, tasked me with analyzing how these two user groups behave differently, using **Cyclistic’s trip data from the past 12 months**. The goal is to provide **data-driven insights** to help convert casual riders into members.

## Table of Contents
[Overview](#overview)
[Data Source & Tools](#-data-source--tools)
[Data Cleaning](#-data-cleaning)
[Key Findings](#-key-findings)
[Visualizations (R with ggplot2)](#-visualizations-r-with-ggplot2)
[Recommendations](#-recommendations)
[Repository Structure](#-repository-structure)
[License & Privacy](#-license--privacy)


## Data Source & Tools
- **Data:** Divvy_Trips_2020_Q1.csv (426,887 entries)
- **Format:** Wide format, includes ride_id, timestamps, locations, user type, etc.
- **Tools Used:**
  - **Google Sheets:** Initial calculations (e.g., ride duration, day of week)
  - **R (Posit Cloud):** Data cleaning, analysis, and visualization
  - **Libraries:** `readr`, `ggplot2`, `dplyr`, `janitor`

## Data Cleaning
- Removed rides > 24 hours for casual users (likely outliers)
- Removed rides with negative duration
- Filtered future-dated records (beyond March 2020)
- Used `clean_names()` to standardize column names
- Final dataset: **426,447 rides**

## Key Findings
1. **Average Ride Duration**
   - Casual: ~37 mins
   - Members: ~12 mins

2. **Weekly Usage Patterns**
   - **Casuals:** More active on **weekends**
   - **Members:** More rides during **weekdays**

3. **Top Starting Stations**
   - Canal St & Adams St
   - Clinton St & Madison St
   - Clinton St & Washington Blvd

## Visualizations (R with ggplot2)
- Bar plots of ride count by user type and day
- Avg. ride time by user type and weekday
- Top 10 popular start stations (horizontal bar)

## Recommendations
- **Target Ads** at top 3 stations
- **Offer discounts** for first month of membership
- **Introduce loyalty programs**
- Focus marketing on **Sunday, Saturday, and Wednesday**

## Repository Structure
- `divvy_analysis.R` → R script with code
- `visualizations/` → PNG files for each chart
- `Divvy_Trips_2020_Q1.csv` → Cleaned dataset (optional)

## License & Privacy
Data provided by **Bikeshare (Lyft)** and the **City of Chicago**. Used strictly for **non-commercial analysis**. Personally identifiable information (PII) excluded due to privacy policies.

