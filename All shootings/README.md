Scraping of incident-level data done using code [gva scraping script](https://github.com/kschnippel/GVA/blob/master/All%20shootings/GVA%20query%20scrap%20using%20selenium.ipynb)

File Name | Scraping or Geocoding date
-- | --
2014_GVA_shootings.csv | 04/25/2020
2015_GVA_shootings.csv | 04/24/2020
2016_GVA_shootings.csv | 04/23/2020
2017_GVA_shootings.csv | 04/22/2020
2018_GVA_shootings.csv | 04/21/2020
2019_GVA_shootings.csv | 04/16/2020
2020_GVA_shootings.csv | 05/21/2020
2014_GVA_shootings_geocoded.csv | 05/21/2020
2015_GVA_shootings_geocoded.csv | 05/21/2020
2016_GVA_shootings_geocoded.csv | 05/21/2020
2017_GVA_shootings_geocoded.csv | 05/21/2020
2019_GVA_shootings_geocoded.csv | 05/08/2020
2020_GVA_shootings_geocoded.csv | 05/16/2020



Data Field | Data type | Description
-- | -- | --
address | general (string) | e.g. 1400 NW 23rd Street
city | General (string) | city or county, e.g. Indianapolis
date | date | format mm/dd/yyyy
id | general (number) | unique id for the incident
injured | general (number) | number injured in incident, could include shooter
killed | general (number) | number killed in incident, could include shooter
source | general (string) | URL of websites, could be multiple sources
state | general (string) | name, spelled out
lat (geocoded files only) | general(number) | e.g. 39.799480
lng (geocoded files only) | general (number) | e.g. -86.187580


