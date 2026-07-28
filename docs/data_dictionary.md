# Data Dictionary 

Definitions for all catalogs used in this project.
For where the data came from and when, see 'data/raw/PROVENANCE.md'.

## TOI Table - NASA Exoplanet Archive

**Source:** NASA Exoplanet Archive TAP service, 'toi' table 
**Official column definitions:** https://exoplanetarchive.ipac.caltech.edu/docs/API_TOI_columns.html

**Grain:** One row = one TESS Object of Interest (one candidate transit signal). A single star may have multiple TOIs, which share one TIC ID. Joins on TIC are therefore many to one.

### Gotchas - Hypatia 
- Lodders09 solar values include Th (0.08) but not U. Uranium cannot be converted from dex to a linear ratio using this scale. Affects Phase 6 radiogenic index - need an alternative solar U value, or drop U and use Th + K only. 
