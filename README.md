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


## Impact

[Discussion of the projects impact/findings here]

For most fields the actual crop sequences are not in the set of crops with a high suitability score.  This may be due to the fact that the suitability score does not take irrigation into account.  Only crops that grow with the predicted rainfall conditions for a field–without irrigation–will have a high suitability score. 


## Data sources

* **Agricultural field data:** The [Crop Sequence Boundary](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/) file for the 2016-2023 growing seasons from the [National Agricultural Statistics Service](https://www.nass.usda.gov/i) [ ~[5.6Gb .zip file](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/datasets/NationalCSB_2016-2023_rev23.zip) ].  This dataset contains field location, shape, and attributes for agricultural fields in the Continental United States [ [CSB Viewer](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/Viewer/i) ] .
* **Crop characteristics data:** The [EcoCrop Crop Database](https://gaez.fao.org/pages/ecocrop) [1–3].  The version for this study was combined from two sources [1,2], and scraped USDA climate zone data. It is available as `EcoCrop_Complete.csv`.
* **Climate Zone Data:** [High-resolution (1 km) Köppen-Geiger maps for 1901–2099](https://figshare.com/articles/dataset/High-resolution_1_km_K_ppen-Geiger_maps_for_1901_2099_based_on_constrained_CMIP6_projections/21789074/1) based on constrained CMIP6 projections [[ ~90Mb .zip file](https://figshare.com/ndownloader/articles/21789074/versions/1) ] [4].
* **Climate data for temperature and growing season:** [The  Localized Constructed Analogs (LOCA) Derived Variables](https://atlas.globalchange.gov/pages/nca4archive) from the [4th National Climate Assessment](https://atlas.globalchange.gov/pages/nca4archive) [ [~2.8 Gb .zip file](https://downloads.globalchange.gov/scenarios/LOCA_data_all.tar.gz) ] [5,6].
* **Climate data for spring and summer temperature and precipitation:** The Climate Toolbox [Climate Mapper](https://climatetoolbox.org/tool/Climate-Mapper) datasets for mean and minimum summer temperatures, minimum annual temperatures, and annual precipitation for recent and mid-century climate scenarios. [7]
* **Crop translator:** A translation file of Cropland Data Layer / Crop Sequence Boundary crop codes to likely EcoCrop species: `cdl_to_ecocrop_code_translator.csv`
* **Climate zone translator:** A translation file of from Köppen-Geiger Climate Zones (Climate Model) to Trewartha Climate Zones (EcoCrop): 
* **Elevation:** Digital Elevation Model from the [PRISM Climate Group](https://prism.oregonstate.edu/downloads/) [ [835 Kb zip](https://prism.oregonstate.edu/downloads/data/PRISM_us_dem_4km_bil.zip) ] [8].
* 


## System requirements

A `python` environment with `xarray`, `rioxarray`, `dask`, `netcdf4`, `pandas`, `geopandas`, and `folium`. 

`altair`, `matplotlib`, `shapely`, `rasterio`, 

A full example environment is provided in `requirements.txt`


## Methods


## Notebooks


## License information

The code here is provided under the MIT License. Details are in the `LICENSE` file. Terms-of-use for the data sources in this project are specified by the owners of the original data sources.  Refer to  the citations for each data source. 


## References

    1. 	Brown M. ecocrop: Crop suitability model using the FAO EcoCrop crop characteristic database. Github; Available: [https://github.com/OpenCLIM/ecocrop](https://github.com/OpenCLIM/ecocrop)


    2. 	Heaivilin H. EcoCrop-ScrapeR: Using R to scrape the FAO EcoCrop database. Github; Available: [https://github.com/supersistence/EcoCrop-ScrapeR](https://github.com/supersistence/EcoCrop-ScrapeR)


    3. 	Food and Agricultural Organization of the United Nations. Crop ecological requirements database (ECOCROP). In: Food and Agricultural Organization of the United Nations | Land & Water | Land Resources Planning Toolbox [Internet]. 2015 [cited 10 Jun 2024]. Available: [https://www.fao.org/land-water/land/land-governance/land-resources-planning-toolbox/category/details/en/c/1027491/](https://www.fao.org/land-water/land/land-governance/land-resources-planning-toolbox/category/details/en/c/1027491/)


    4. 	Beck HE, McVicar TR, Vergopolan N, Berg A, Lutsko NJ, Dufour A, et al. High-resolution (1 km) Köppen-Geiger maps for 1901-2099 based on constrained CMIP6 projections. Sci Data. 2023;10: 724. doi:[10.1038/s41597-023-02549-6](http://dx.doi.org/10.1038/s41597-023-02549-6)


    5. 	U.S. Global Change Research Program (2009- ). Fourth National Climate Assessment: Impacts, Risks, and Adaptation in the United States. Summary findings and overview. U.S. Global Change Research Program; 2017. Available: [https://play.google.com/store/books/details?id=RlVFxwEACAAJ](https://play.google.com/store/books/details?id=RlVFxwEACAAJ)


    6. 	U.S. Global Change Research Program (2009- ). Fourth National Climate Assessment: Impacts, risks, and adaptation in the United States. Report-in-brief. U.S. Global Change Research Program; 2018. Available: [https://play.google.com/store/books/details?id=l0cBvwEACAAJ](https://play.google.com/store/books/details?id=l0cBvwEACAAJ)


    7. 	Hegewisch KCAJTA. “Climate Mapper” web tool. In: Climate Toolbox [Internet]. [cited 7 Aug 2024]. Available: [https://climatetoolbox.org/](https://climatetoolbox.org/)


    8. 	PRISM Climate Group, Oregon State University. PRISM Spatial Climate Datasets for the Conterminous United States. 2014. Available: [https://prism.oregonstate.edu,](https://prism.oregonstate.edu,)


