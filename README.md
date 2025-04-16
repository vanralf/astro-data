# astro-data
# NASA Habitable Planets Finder

This Python script connects to NASA's Exoplanet Archive and prints a list of potentially habitable exoplanets.

It uses the public NASA API to search for planets with temperatures between 200–300 Kelvin which is roughly the range where liquid water could exist.

## What It Does

- Sends a request to the NASA Exoplanet Archive API
- Filters planets with temperatures that might support life
- Displays:
  - Name
  - Orbital period
  - Radius
  - Estimated temperature
