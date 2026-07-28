# Data Provenance 

Log of every download here: URL/query, date, catalog version, row count.

## Downloads 

### TOI catalog
- Source: NASA Exoplanet Archive TAP service, 'toi' table
- URL: https://exoplanetarchive.ipac.caltech.edu/TAP/sync?query=select+*+from+toi&format=csv
- Downloaded: (7/27/26)
- Rows: (8064)
- Columns: (91)
- File: data/raw/toi_20260727.csv

 #### Disposition breakdown as of: (7/27/26)
 - PC - 4898 Planet Candidate
 - FP - 1247 False Positive
 - CP - 740 Confirmed Planet
 - KP - 593 Known Planet
 - APC - 483 Ambiguous Planet Candidate
 - FA - 100 False Alarm
 - NaN - 3 No disposition assigned 

### Hypatia Catalog
- API: https://hypatiacatalog.com/hypatia/api/v2/
- Solar normalization: lodders09 (Lodders et al. 2009), API default
- Retrieved: (7/28/26)

#### Findings: (Add to paper)
Of the elements relevant to assessing rocky planet habitability, iron, magnesium, and silicon are measured in over 10,000 Hypatia stars, while phosphorus is measured in 284, thorium in one, and uranium in none. The elements that govern biological viability and long-term geological activity are precisely those that remain unmeasured. (7/28/26)
