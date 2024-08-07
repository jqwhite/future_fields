<!-----



Conversion time: 0.397 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β37
* Wed Aug 07 2024 12:04:16 GMT-0700 (PDT)
* Source doc: README.md
----->



# Future Fields

Assessing crops for fields based on weather, water, sun, and soil: now and mid-century.


## Summary

The Future Fields Project assesses the suitability of crops for fields in four states of the US Southwest for medium carbon and high carbon climate scenarios. Each field in the [ Crop Sequence Boundary ](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/) 2016-2023 dataset was assessed for each crop in the [FAO EcoCrop database](https://gaez.fao.org/pages/ecocrop).

For each field and crop species, scores were calculated for:



* growing season
* temperature
* photoperiod
* rainfall
* soil pH
* Köppen-Geiger climate zone
* USDA Plant Hardiness Zone

Scores were calculated for three scenarios:



* recent past (1970-2005)
* mid-century medium carbon (2039-2065, RCP 4.5)
* mid-century high carbon (2039-2065, RCP 8.5)

Climate-dependent changes in ground and surface water sources were not taken into account, so only crops that are suitable without irrigation were assessed.  

Crop species with the highest overall score are deemed suitable for the field.


## Overview

The most reliable predictor of what crop will be planted in a particular field for a growing season (the crop profile for the field) is what crops were planted in previous seasons.  However, climate change will force crop profiles into regimes outside of the historical context. The goal of this project is to assess which crops are suitable for fields in the Southwest United States given a set of climate-dependent conditions: weather, water, sun, and soil. 

The conditions of each agricultural field are matched to the growth requirements of 2,580 plant species based on three scenarios: current conditions, and projections for mid-century under mid-level and high-level CO<sub>2</sub> emissions.  The best-matching crops for each set of conditions represent the suitable crops. To evaluate the matching crops, three sets of suitable crops (recent past, mid-century medium carbon, and mid-century high carbon) are compared to known crop sequences for each field. A feedback layer enables stakeholders to indicate whether suitable crops are relevant or not; relevance feedback is used to adjust scoring based on human expertise.   

The suitable crops, known crop sequences, and representative data sources are presented as map layers to facilitate comparison, reveal spatial patterns, promote stakeholder engagement, and provide feedback.  Overall, the patterns of recommended crops profoundly shift in distribution and content depending on climate scenario.


## Data requirements


* Agricultural field data: The [Crop Sequence Boundary](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/) file for the 2016-2023 growing seasons from the [National Agricultural Statistics Service](https://www.nass.usda.gov/i) [ ~[5.6Gb .zip file](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/datasets/NationalCSB_2016-2023_rev23.zip) ].  This dataset contains field location, shape, and attributes for agricultural fields in the Continental United States [ [CSB Viewer](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/Viewer/i) ] .
* Crop characteristics data: The [EcoCrop Crop Database](https://gaez.fao.org/pages/ecocrop) [(Brown ; Heaivilin ; Food and Agricultural Organization of...)](https://paperpile.com/c/IkePR6/Y9Kd+6jz7+fB0j).  The version for this study is was combined from two sources [(Heaivilin ; Brown )](https://paperpile.com/c/IkePR6/6jz7+Y9Kd), and scraped USDA climate zone data. It is available as `EcoCrop_Complete.csv`.
* Climate Zone Data: [High-resolution (1 km) Köppen-Geiger maps for 1901–2099](https://figshare.com/articles/dataset/High-resolution_1_km_K_ppen-Geiger_maps_for_1901_2099_based_on_constrained_CMIP6_projections/21789074/1) based on constrained CMIP6 projections [[ ~90Mb .zip file](https://figshare.com/ndownloader/articles/21789074/versions/1) ] [(Beck et al. 2023)](https://paperpile.com/c/IkePR6/rihb).
* Climate data for temparature and growing season:
* A translation file of Cropland Data Layer / Crop Sequence Boundary crop codes to likely EcoCrop species.
* A translation file of from Köppen-Geiger Climate Zones (Climate Model) to Trewartha Climate Zones (EcoCrop).
* 



## System requirements


## Methods

gd2md-html: xyzzy Wed Aug 07 2024











<!-- watermark --><div style="background-color:#FFFFFF"><p style="color:#FFFFFF; font-size: 1px">gd2md-html: xyzzy Wed Aug 07 2024</p></div>

