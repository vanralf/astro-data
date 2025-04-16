# astro-data
import requests

# Data from NASA Exoplanet Archive
url = "https://exoplanetarchive.ipac.caltech.edu/TAP/sync"
params = {
    "query": "SELECT pl_name, pl_orbper, pl_rade, pl_eqt FROM ps WHERE pl_eqt BETWEEN 200 AND 300",
    "format": "json"
}

# Send request to the API
response = requests.get(url, params=params)

# Convert response to JSON
data = response.json()

# Print basic info about each planet
for planet in data:
    print(f"Name: {planet['pl_name']}, Orbital Period: {planet['pl_orbper']} days, Radius: {planet['pl_rade']} Earths, Temp: {planet['pl_eqt']} K")
