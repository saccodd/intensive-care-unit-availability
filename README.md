# Description

The purpose of this initiative is to build an integrated dataset on Intensive Care Units (ICUs) and their availability by country and region (at the highest regional granularity provided by the sources), using a data model standardized across countries.

Currently, ICU data is stored in different country-specific sources, with a wide range of access points (national websites, APIs, excel or csv files, etc.)

Given current COVID-19 crisis, we believe that this information should be provided with the following: 
* common standardized structure
* single point of access
* open to the public 

We hope that these datasets will further benefit research and analysis, and help us in the fight against COVID-19. E.g. data can be used for:
* monitoring of areas at capacity (e.g. [VoiceToData dashboard for Italy](https://www.voicetodata.com) ) 
* hospital capacity planning
* trend forecasting
* *YOUR IDEA* - get in touch with us!


### Data model

Datasets can be found in [/data](https://github.com/saccodd/intensive-care-unit-availability/tree/master/data) and are organised by country.

Glossary:
- *Low Care ICU* = monitoring, non-invasive ventilation (NIV), no organ replacement therapy
- *High Care ICU* = monitoring, invasive ventilation, organ replacement therapy. Complete intensive medical therapy options
- *ECMO* = additional extracorporeal membrane oxygenation

Field description:
* **regionCode** - code of the region within the country
* **region** - name of the region within the country
* **icuTotal** - ICU capacity in the region, i.e. total number of ICU beds
* **lastUpdate** - last update of the dataset on our GitHub repository

If available:
* **icuLowCareFree** - Low Care ICU availability
* **icuLowCareUsed** - Low Care ICU occupancy
* **icuLowCareFreeIn24H** - Low Care ICUs that will be freed in the next 24 hours
* **icuHighCareFree** - High Care ICU availability
* **icuHighCareUsed** - High Care ICU occupancy
* **icuHighCareFreeIn24H** - High Care ICUs that will be freed in the next 24 hours
* **icuEcmoFree** - ECMO availability
* **icuEcmoUsed** - ECMO care occupancy
* **icuEcmoFreeIn24H** - ECMOs that will be freed in the next 24 hours
* **ecmoCasesPerYear** - average number of ECMO cases per year
* **icuOccupancyRate** - average occupancy of ICUs
* **hospitalTotal** - number of hospitals in the region
* **population** - population in the region
* **adultPopulation** - adult (18+) population in the region
* **over65Population** - 65+ population in the region

### Countries and sources:
- Italy (as of 2019 - source: [Ministero della Salute](http://www.dati.salute.gov.it/dati/dettaglioDataset.jsp?menu=dati&idPag=96))
- United Kingdom
  - England (as of 2020 - source: [NHS England](https://www.england.nhs.uk/statistics/statistical-work-areas/critical-care-capacity/critical-care-bed-capacity-and-urgent-operations-cancelled-2019-20-data/))
  - Wales (as of 2019 - source: [StatsWales](https://statswales.gov.wales/Catalogue/Health-and-Social-Care/NHS-Hospital-Activity/NHS-Beds/nhsbeds-by-organisation-site))
  - Scotland (as of 1998, projected on 2020 whole figure - sources: [Scottish Health Directorate](https://www.sehd.scot.nhs.uk/publications/report.PDF) & [Herald Scotland](https://www.heraldscotland.com/news/18295827.coronavirus-scotland-needs-double-intensive-care-beds-says-freeman/))
  - Northern Ireland (as of 2020, w/o sub-area granularity - source: [Derry Journal](https://www.derryjournal.com/health/coronavirus-ni-all-100-critical-care-beds-northern-ireland-could-be-used-fight-covid-19-2048283))
- US (as of 2018 - source: [Harvard Global Health Institute](https://globalepidemics.org/our-data/hospital-capacity/))
- Spain (as of 2013 - source: [Medicina Intensiva](https://www.medintensiva.org/en-pdf-S2173572713000878))
- Germany 
  - static dataset (as of 2017 - [Gesundheitsberichterstattung Des Bundes](http://www.gbe-bund.de/oowa921-install/servlet/oowa/aw92/dboowasys921.xwdevkit/xwd_init?gbe.isgbetol/xs_start_neu/&p_aid=i&p_aid=17903021&nummer=841&p_sprache=D&p_indsp=-&p_aid=81784396))
  - live dataset (not covering all hospitals, pipeline broken to be fixed - source [DIVI Intensiv Register](https://www.intensivregister.de/#/intensivregister))
- France (as of 2018 - [Ministère des Solidarités et de la Santé](https://drees.solidarites-sante.gouv.fr/etudes-et-statistiques/publications/article/nombre-de-lits-de-reanimation-de-soins-intensifs-et-de-soins-continus-en-france))
- Austria (as of 2018 - [Statistik Austria](https://www.statistik.at/web_de/statistiken/menschen_und_gesellschaft/gesundheit/gesundheitsversorgung/einrichtungen_im_gesundheitswesen/index.html))
- Portugal (as of 2016 - [Ministério da Saúde](https://www.sns.gov.pt/wp-content/uploads/2016/05/Avalia%C3%A7%C3%A3o-nacional-da-situa%C3%A7%C3%A3o-das-unidades-de-cuidados-intensivos.pdf))
- Belgium (as of 2012 - [SPF Santé publique](https://www.health.belgium.be/sites/default/files/uploads/fields/fpshealth_theme_file/stathosp2015_feedbackfr.pdf))
