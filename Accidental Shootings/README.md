### Using the script and things to consider:

### Added python jypter notebook file for accidental shooting from query

The [script](https://github.com/kschnippel/GVA/blob/master/Accidental%20Shootings/GVA%20accidental%20shooting%20scraper.ipynb) collects data from GVA database filtering for accidental shootings. The scraper gets data for accidental shootings for a given year from the GVA website. 
The data currently is scraped on both accidental injuries and accidental killings, due to an accidental shooting. It updates the data by feeding these two URLS to beautiful soup: 
```python
url = [f"https://www.gunviolencearchive.org/accidental-deaths?page={page}&year={year}", f"https://www.gunviolencearchive.org/accidental-injuries?page={page}&year={year}" ]
### The script replaces the {page} and {year} in the links to iterate through the accidental shootings in a year.
```
The limitation is that it does not account for the GVA 500 incidents query limit. Thus it loses out on data due to the query limit. This script can be improved using selenium for webautomation. Look at how the [GVA all shootings scraper](https://github.com/kschnippel/GVA/blob/master/All%20shootings/Scripts/GVA%20query%20scrap%20using%20selenium.ipynb) accounts for the query limit to get daily shooting data. Selenium can be used again in this case to select accidental shootings as a characteristic rule.
[Jason Lim](https://github.com/jasonjklim) will be able to help with the Selenium script. 

### Accidental Shooting Data available:

File Name | Scraping date
-- | --
accidental_shootings.json | 03/26/2020

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



Data collected from GVA:
Update script written by: https://github.com/chanind

Minor fixes by: https://github.com/calremmel

Updated to collect accidental shootings data instead of mass shooting data by: https://github.com/shahaan123 

The main data file is accidental_shootings.json, example of data in file is below:

```js
[
  {
    "id": 92563,
    "date": "2014-01-01",
    "state": "Mississippi",
    "city": "Bogue Chitto",
    "address": "1347 Brumfield Rd SW",
    "killed": 1,
    "injured": 0,
    "source": "http://www.wapt.com/news/central-mississippi/jackson/Girl-shot-killed-with-pellet-gun/23747080"
  },
  ...
]
```


Requirements: 

Requirements to run the code:
You will need Anaconda and Jupyter Notebook installed on your machine to run the scripts mentioned above. You will also need the following packages installed from the anaconda prompt command line:

pip intall pandas

pip install DateTime

pip install requests

pip install beautifulsoup4

pip install python-dateutil

pip install selenium (in case improving script with Selenium)

So if you do not have any of these packages installed use the pip install package_name command in command prompt.
