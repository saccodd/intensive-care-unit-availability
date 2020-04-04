# Description

This initiative intends to build a unique repository where to find consistent datasets about Intensive Care Units (ICUs) and their availability by country and region.

Currently, ICU data lies in different country-specific sources and in a wide range of formats (websites, APIs, excel or csv files, etc.)

Given current COVID-19 crisis, we believe that this information should be provided with a common structure to enable easy processing, and opened to the public for research and analysis.

Available countries:
* Italy (as of 2018 - source: [salute.gov.it](http://www.dati.salute.gov.it/dati/dettaglioDataset.jsp?menu=dati&idPag=96))
* Germany (coming soon)

## Data model

Datasets can be found in [/data](https://github.com/saccodd/intensive-care-unit-availability/tree/master/data) and are organised by country.

Glossary:
* *Low Care ICU* = monitoring, non-invasive ventilation (NIV), no organ replacement therapy
* *High Care ICU* = monitoring, invasive ventilation, organ replacement therapy. Complete intensive medical therapy options
* *ECMO* = additional extracorporeal membrane oxygenation

Field description:
* **region** - name of the region within the country
* **icuLowCareFree** (if available) - Low Care ICU availability
* **icuLowCareUsed** (if available) - Low Care ICU occupancy
* **icuLowCareFreeIn24H** (if available) - Low Care ICUs that will be freed in the next 24 hours
* **icuHighCareFree** (if available) - High Care ICU availability
* **icuHighCareUsed** (if available) - High Care ICU occupancy
* **icuHighCareFreeIn24H** (if available) - High Care ICUs that will be freed in the next 24 hours
* **icuEcmoFree** (if available) - ECMO availability
* **icuEcmoUsed** (if available) - ECMO care occupancy
* **icuEcmoFreeIn24H** (if available) - ECMOs that will be freed in the next 24 hours
* **ecmoCasesPerYear** (if available) - stats on number of ECMO cases a year
* **icuTotal** - ICU capacity in the region, i.e. total number of ICU beds
