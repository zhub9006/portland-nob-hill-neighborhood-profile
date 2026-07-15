# Contributing to Nob Hill Neighborhood Profile

Thanks for your interest in improving this open-source neighborhood profile!

## How to Contribute

1. **Verify against OSM** — All data should be cross-referenced with current OpenStreetMap data
2. **Open an issue** — Discuss changes before submitting to allow community review
3. **Submit a Pull Request** — Include OSM-verified data updates

## Data Format

- **JSON data:** `data/nob-hill-portland.json` — Structured neighborhood profile with walkability scores, amenities, and raw OSM features
- **Markdown analysis:** `WALKABILITY_ENRICHED.md` — Human-readable walkability analysis with detailed metrics

## Scoring Methodology

- Walkability scores are based on OSM amenity density and proximity analysis
- 1km analysis radius centered on address coordinates
- Scores are calculated based on count of facilities, average distance, and nearest distance
- Ratings: 0-3 (Minimal), 3-5 (Good), 5-8 (Very Good), 8-10 (Excellent)

## Data Fields

- `location` — Address, coordinates, OSM metadata
- `walkability_scores` — Category scores with ratings
- `amenities` — Detailed amenity lists with distances
- `raw_osm_features` — Total counts per category
- `nearest_landmark_distances` — Proximity ranking of nearby places

## License

Open data — feel free to use and distribute under Open Database License (ODbL).
