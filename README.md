# Seattle-NYC-Weather Analysis
## Description
Does it rain *more* in Seattle or New York City? 

To answer this question, rainfall data from weather stations in both cities was gathered, cleaned, and analyzed. The NOAA National Centers for Environmental Information website was used to request records of daily precipitation/rainfall from Seattle and New York for the 3 year period from January 2020 to January 2024. The data was analyzed using a variety of methods, such as comparing the overall average rainfall of each city over various time periods like monthly, quarterly, etc. Furthermore, the intensity of the rain was considered. Overall, New York City recieves slightly more average daily rainfall than Seattle, but there are many nuances. See seattle_weather_report.docx for the full report.

## Report
seattle_weather_report.docx contains the full report on the results of the analysis.

## Analysis
Seattle_NYC_Analysis is the notebook that contains the full analysis and data preparation.

## Data Preparation
The notebook Seattle_NYC_Analysis.ipynb was used to determine that both the Seattle and New York data sets are appropriate to investigate which city gets more rain. The clean data set consists of a daily average precipitation per city from January 2020 to January 2024. Note that a few days were missing for Seattle. The following changes/preperations were made:
*   'DATE' was changed to be datetime.
*   All columns other than 'STATION', 'NAME', 'DATE', and 'PRCP' were dropped.
*   Following the drop of the previously states columns, NaNs were dropped.
*   Columns were renamed to be lowercase and more clear.
*   The 'precipitation' column was averaged by each day.
*   A 'city' column was added that was either 'Seattle' or 'New York City'.
*   The following time columns were added: quarter, year, month, cumulative_month (0 indexed), and cumulative_quarter (0 indexed).
*   The dates are only in the years from 2020 to 2023, but some days for Seattle are missing.

## Clean Data
clean_seattle_nyc_weather.csv is the clean data file created by Seattle_NYC_Analysis.ipynb

## Data Source
Source: https://www.ncei.noaa.gov/cdo-web/search

Documentation: https://www.ncei.noaa.gov/pub/data/cdo/documentation/GHCND_documentation.pdf

### Seattle Rain Data
seattle_rain.csv contains rain data obverved by various weather stations in Seattle, WA.

Downloaded From: https://github.com/galenegan/DATA-3320/blob/main/weather/seattle_rain.csv

### New York City Rain Data
ny_rain.csv contains rain data obverved by various weather stations in New York City, NY.

Downloaded From: https://github.com/galenegan/DATA-3320/blob/main/weather/ny_rain.csv
