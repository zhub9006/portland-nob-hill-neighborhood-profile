# Contributing

Contributions to enhance or correct this neighborhood data are welcome!

## How to Contribute

1. **Verify against OpenStreetMap** — Any updates should be verified against current OSM data
2. **Open an issue** — Discuss proposed changes before submitting
3. **Submit a Pull Request** — Include OSM-verified data updates with source references

## Data Standards

- All data must be sourced from OpenStreetMap
- Include OSM place IDs and feature IDs for verification
- Use metric measurements (meters, kilometers)
- Include date stamps for data collection/enrichment
- Maintain consistent JSON structure across data files

## Adding New Data

To add new data for this neighborhood:

1. Verify features in [OpenStreetMap](https://www.openstreetmap.org/)
2. Update the relevant data file in `data/`
3. Update this README if new categories or significant changes are added
4. Submit a PR with a clear description of changes

## Adding Data for a New Address

To create a neighborhood profile for a different address:

1. Geocode the address to get coordinates
2. Run OSM-based amenity analysis within 1km radius
3. Create a new data file following the existing naming convention: `data/nob-hill-[address-slug].json`
4. Add the file to the Raw Data section in README.md
5. Submit a PR

## Walkability Scoring Methodology

Scores are calculated based on OSM amenity density and proximity:

- **Walk Score (10/10):** Walker's Paradise — daily errands do not require a car
- **Transit Score (9.4/10):** Based on number of transit stops within 1km and walk time to nearest
- **Bike Score (9/10):** Based on bike infrastructure, bike shops, and bike lane connectivity
- **Category Scores:** Based on count of amenities, average distance, and nearest distance
  - Restaurants: 9.8 (89 within 1km, avg 543m)
  - Healthcare: 9.8 (6 within 1km, nearest 38m)
  - Groceries: 7.1 (3 within 1km, avg 668m)
  - Parks: 4.3 (limited formal parks in 1km)
  - Education: 2.9 (2 within 1km)
  - Entertainment: 0 (none within 1km)
