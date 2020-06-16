#### The scripts have inline explanations as comments on how to use them (Very important to read through all the inline comments in the script).

```python
### This is what the inline comments look like in jupyter notebook running python
```
### GVA Scrap using Selenium script
#### Requirements to run GVA Scrap using Selenium script:

You will need _Anaconda_ and _Jupyter Notebook_ installed on your machine to run the scripts mentioned above.
The script needs the shootings.json and shootings_compact.json files in the same directory to run (These files can be empty but need to still be in the same directory for scripting). 
You will also need the following packages installed from the anaconda prompt command line:

pip install jsonlib 

pip intall pandas

pip install DateTime

pip install requests

pip install beautifulsoup4

pip install python-dateutil

pip install selenium

pip install regex

So if you do not have any of these packages installed use the pip install _package_name_ command in command prompt. 


### Geocoding script:
Geocoding is done using the [Open Cage geocoder](https://opencagedata.com/tutorials/geocode-in-python)

#### Address cleaing:
The following strings when they appear on their own in an address are removed from the address. This helps the geocoder from getting a consistent latitude and longitude and avoids the geocoding from failing.
```python
 split_param = ", | # | SUITE | RM | P.O. | STE | UNIT | P O | STE. | SUITES | APT | BOX | block of | corner of | of | blk "
 
 ```
 Any address that contains " and " or " & " are also split and the first half of the address is what is kept as these are present when the address contains an intersection and Open Cage geocoder does not handle road intersections well. 
 
 The city field also is cleaned before geocoding as some of the entries contain an entry in parenthesis aswell for city for example:
 New York City (Manhattan). The part in parenthesis needs to be removed for the geocoder to work properly so that is also removed in the address cleaning steps. 
 
#### Requirements to run the script:

The geocoder needs the data to be in JSON format. So the data that is collected from the GVA webscraping script can be directly geocoded by this script.The script has a portion to turn the geocoded JSON file into a CSV file. 

If you only have a CSV file availble that needs to be geocoded then it needs to be converted into a json file first. There is a script available to perform that though the steps involved are a little convulted. As it would need the CSV file to be in the raw output format(text) that is available on Github. 





