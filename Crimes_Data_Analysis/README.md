# Crimes Data Analysis

## Objective
Analyze crime records to identify key patterns:
1. Which hour has the highest frequency of crimes?
2. Which area has the largest frequency of night crimes (10pm–3:59am)?
3. How many crimes were committed against victims of different age groups?

## Method
- **Data source:** crimes.csv (not included in repo due to size limits; available from [source if you have a link])
- **Steps:**
  1. Extract crime hour from the `TIME OCC` column.
  2. Count crimes per hour and identify the peak (`peak_crime_hour`).
  3. Filter crimes between 10pm–3:59am and find the area with the largest frequency (`peak_night_crime_location`).
  4. Bin victim ages into categories (`0-17`, `18-25`, `26-34`, `35-44`, `45-54`, `55-64`, `65+`) and count crimes per group (`victim_ages`).

## Results
- **Peak crime hour:** stored in `peak_crime_hour` (int).
- **Peak night crime location:** stored in `peak_night_crime_location` (string).
- **Crimes by victim age group:** stored in `victim_ages` (pandas Series).

## Visualizations
- Bar chart of crime frequency by hour of day.
- Distribution of victim ages grouped into brackets.

## Skills Demonstrated
- Data wrangling with pandas
- Data visualization with Matplotlib/Seaborn
- Grouping and binning techniques
- Extracting actionable insights from raw data

