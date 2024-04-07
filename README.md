# Seattle-Weather for DATA-3320
## Description
First repository/assignment for DATA-3320 to investigate whether it rains more in Seattle, WA than in New York City, NY.

## Data Preparation
The collab notebook Seattle_NYC_Weather.ipynb was used to determine that both the Seattle and New York data sets are appropriate to investigate which city gets more rain. The following changes/preperations were made:
*   'DATE' was changed to be datetime.
*   All columns other than 'STATION', 'NAME', 'DATE', and 'PRCP' were dropped.
*   Following the drop of the previously states columns, duplicates were removed and NaNs were dropped as well.
*   The tables were changed so each row was a unique date and the precipitation for that city was the average precipitaion among all the weather stations.
*   The two data sets were merged/joined together to create a table with just three columns, 'date', 'seattle_precipitation', and 'ny_precipitation'. Note that table only contains the dates where data was present for both Seattle and New York City.

## Clean Data
clean_seattle_nyc_weather.csv is the clean data file created by Seattle_NYC_Weather.ipynb

## Data Source
Source: https://www.ncei.noaa.gov/cdo-web/search

Documentation: https://www.ncei.noaa.gov/pub/data/cdo/documentation/GHCND_documentation.pdf

### Seattle Rain
seattle_rain.csv contains rain data obverved by various weather stations in Seattle, WA.

Downloaded From: https://github.com/galenegan/DATA-3320/blob/main/weather/seattle_rain.csv

### New York Rain
ny_rain.csv contains rain data obverved by various weather stations in New York, NY.

Downloaded From: https://github.com/galenegan/DATA-3320/blob/main/weather/ny_rain.csv
