# geoaddress (in-progress)
## Description
Code for paper (in progress): The spatial distribution of big science: A methodology for disaggregating and geocoding address fields (Working title).    
Dissagregates and geocodes author addresses from Web of Science (WoS) data and/or any address with the following form:
```
[Authors] Address;  
```
Geocoding done with the geopy package (More info below).    
## More functionality
- distance measurements between addresses and to a point of origin
## Important info
- This package uses geopy for the geocoding module. See [geopy's documentation](https://geopy.readthedocs.io/en/stable/) for more info. 
- This example uses the GoogleV3 API, which needs an API Key. Read [here](https://developers.google.com/maps/documentation/geocoding/). 
- Make sure you include an API key [here](geo_address/API_key.txt) if needed.
- You can also change the geocoder [here](geo_address/processing.py) if you prefer.
## Installation
```
git clone https://github.com/soderstromkr/geoaddress.git
```
or
```
pip install git+https://github.com/soderstromkr/geoaddress.git
```
## Requirements
Uses python 3.x.x
- pandas
- numpy
- tqdm
- geopy
- re
- pickle 
- sklearn
-	haversine
## Example
See [here](example.ipynb) for an example (in-progress).
## Recommendations
- Current geocoder gave the best results in paper.
- begin_geocode() creates a checkpoint folder to keep track of progress, which can be re-started. (Make sure to delete the checkpoint file if doing a new run or project.)
