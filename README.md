# Los Angeles Crime Trends An Exploratory Data Analysis

## Overview

This project explores a dataset of reported crimes. The goal is to understand crime trends over time, look at victim demographics (age, gender, descent), and find the areas with the most crimes.

## Dataset

The dataset is sourced from the crimes.csv file and contains over 185,000 records.

### Columns included:

- **DR_NO**: Division of Records Number (Official file number)
- **Date Rptd**: Date the crime was reported
- **DATE OCC**: Date the crime occurred
- **TIME OCC**: Time the crime occurred
- **AREA NAME**: The Geographic Area or Patrol Division
- **Crm Cd Desc**: Crime Code Description
- **Vict Age**: Victim's age
- **Vict Sex**: Victim's gender
- **Vict Descent**: Victim's descent/ethnicity
- **Weapon Desc**: Description of the weapon used (if any)
- **Status Desc**: Status of the case
- **LOCATION**: Street address of the crime

## Data Cleaning

To prepare the data for analysis, the following steps were taken:

1. **Handling Missing Values**: Empty values in the Victim Sex and Victim Descent columns were filled with 'Unknown'.
2. **Standardizing Categories**: In the Victim Sex column, the values 'X' and 'H' were replaced with 'Not prefere to say'.
3. **Date and Time Formatting**:
   - Converted `Date Rptd` and `DATE OCC` into standard date formats.
   - Added leading zeros to `TIME OCC` and converted it into a readable time format.
4. **Feature Engineering**: Created new columns for `month` and `year` from the occurrence date to help with time-based analysis.

## Exploratory Data Analysis (EDA)

The notebook includes several visual charts to show key findings:

- **Crime by Year and Month**: Bar charts showing how the number of crimes changes over different years and months.
- **Victim Demographics**:
  - A horizontal bar chart showing the descent of victims.
  - A bar chart showing the gender of victims (Color-coded: Male=Cyan, Female=Pink, Unknown/Other=Yellow).
  - A histogram showing the age distribution of victims.
- **Top Crime Areas**: A bar chart highlighting the top 10 areas with the highest number of reported crimes.
