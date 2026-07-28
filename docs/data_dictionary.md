# Data Dictionary 

Definitions for all catalogs used in this project.
For where the data came from and when, see 'data/raw/PROVENANCE.md'.

## TOI Table - NASA Exoplanet Archive

**Source:** NASA Exoplanet Archive TAP service, 'toi' table 
**Official column definitions:** https://exoplanetarchive.ipac.caltech.edu/docs/API_TOI_columns.html

**Grain:** One row = one TESS Object of Interest (one candidate transit signal). A single star may have multiple TOIs, which share one TIC ID. Joins on TIC are therefore many to one.

### Gotchas - Hypatia 
- Lodders09 solar values include Th (0.08) but not U. Uranium cannot be converted from dex to a linear ratio using this scale. Affects Phase 6 radiogenic index - need an alternative solar U value, or drop U and use Th + K only.

### GET /data — two-axis behavior unconfirmed

Date: 2026-07-28

Requested `{"xaxis1": "P", "yaxis1": "Fe"}` against /data.
Response `labels` returned only `{'xaxis': '[P/H]'}` — no yaxis key.
counts = 284, and each entry in `values` contained only
`{'xaxis': ..., 'name': ...}`.

Interpretation unclear. Possible that yaxis1 requires a different
parameter name, or that the endpoint ignores it when unspecified in
some other way. Not blocking: single-axis queries return the counts
and star names needed for the coverage census.

TODO: revisit if two-element joint coverage counts are needed.
Do NOT assume yaxis1 works until verified.
