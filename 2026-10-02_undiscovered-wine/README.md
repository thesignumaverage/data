# Data for https://website.thesignumaverage.workers.dev/articles/undiscovered-wine/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## suitable_land_by_country.csv

**Farmland suited to vineyards, and the vines grown on it, by country.** For every country, the farmland whose climate, water and soil match the land today's vineyards occupy, under a strict and a generous test, next to the grapes it grows now. Suitability comes from a model trained on 26 wine countries and checked on continents it never saw.

Coverage: World, about 2020 (wine grapes 2000 and 2023). Last updated: 2026-10-03.

| Column | Description |
|---|---|
| `iso3` | ISO 3166 three-letter country code (Natural Earth). |
| `country` | Country name. |
| `farmland_strict_ha` | Farmland passing the strict test, without vines, hectares. |
| `farmland_generous_ha` | Farmland passing the generous test (includes the strict test), without vines, hectares. |
| `grapes_all_ha_2020` | Area under grapes of every use (wine, table, raisins), 2020, hectares (CROPGRIDS). |
| `vineyards_mapped_osm_ha` | Vineyards mapped in OpenStreetMap, hectares. Coverage varies by country. |
| `wine_grapes_ha_2000` | Wine-grape area in 2000, hectares (Anderson, Nelgen and Puga). Empty if not covered. |
| `wine_grapes_ha_2023` | Wine-grape area in 2023, hectares. Empty if not covered. |
| `wine_share_of_grapes` | Wine grapes as a share of all grapes (2023 over 2020), capped at 1. |
| `used_to_train_model` | True if the country's vineyards were used to train the model; its scores then come from a model that did not see it. |

Sources:

- OpenStreetMap contributors, landuse=vineyard, via Overture Maps release 2026-09-23.1: https://www.openstreetmap.org/copyright (ODbL 1.0; figures here are hectares summed by area)
- CROPGRIDS v1.08 (Tang et al., 2024, Scientific Data): https://doi.org/10.6084/m9.figshare.22491997 (CC BY 4.0)
- TerraClimate monthly normals, 1991-2020 (Abatzoglou et al., 2018): https://www.climatologylab.org/terraclimate.html (Public domain (CC0))
- SoilGrids 2.0 (ISRIC; Poggio et al., 2021): https://soilgrids.org (CC BY 4.0)
- FAO Global Map of Irrigation Areas v5 (Siebert et al., 2013): https://www.fao.org/aquastat/en/geospatial-information/global-maps-irrigated-areas/ (Used as a model input only; not redistributed)
- Anderson, K., S. Nelgen and G. Puga, Database of Regional, National and Global Winegrape Bearing Areas by Variety, 2000 to 2023, University of Adelaide, December 2025: https://economics.adelaide.edu.au/wine-economics/databases (Free to use with citation)
- Natural Earth admin 0 and admin 1 boundaries: https://www.naturalearthdata.com (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Strict test: land scoring at least as high as the vineyards that hold three-quarters of today's vineyard hectares in the countries the model learned from. Generous test: nine-tenths.
- Farmland means a cell where at least 5% of the land is cropland (CROPGRIDS, all 173 crops); cells that already hold vines are not counted as suitable farmland.
- Countries with under 1,000 hectares of either suitable farmland or grapes are left out.
- The map itself is in vineyard_suitability_5arcmin.tif in the same folder: band 1 is the score x 250 (strict test 198 or more, generous 122 or more), band 2 the class (0 other land, 1 generous only, 2 strict, 3 vines today); 255 is no data.
- Licence for this file: it contains data derived from OpenStreetMap, (c) OpenStreetMap contributors, and is released under the Open Database License (ODbL 1.0, https://opendatacommons.org/licenses/odbl/), not CC BY. You may reuse it with that credit; databases you build from it must also be shared under the ODbL.

How to cite:

Signum Average (2026) - "Farmland suited to vineyards, and the vines grown on it, by country" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/suitable_land_by_country.csv

```bibtex
@misc{signumaverage-suitable-land-by-country,
    author = {{Signum Average}},
    title = {Farmland suited to vineyards, and the vines grown on it, by country},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/suitable_land_by_country.csv}},
    note = {Dataset}
}
```

## suitable_land_by_province.csv

**Farmland suited to vineyards, by province.** The same measures as the country table for first-level divisions (provinces, states, regions), as drawn by Natural Earth.

Coverage: World, about 2020. Last updated: 2026-10-03.

| Column | Description |
|---|---|
| `iso3` | Country code. |
| `country` | Country name. |
| `province` | First-level division (Natural Earth name). |
| `farmland_strict_ha` | Farmland passing the strict test, without vines, hectares. |
| `farmland_generous_ha` | Farmland passing the generous test, without vines, hectares. |
| `vines_ha` | Vines grown today: the larger of mapped vineyards (OpenStreetMap) and all grapes (CROPGRIDS), hectares. |

Sources:

- OpenStreetMap contributors, landuse=vineyard, via Overture Maps release 2026-09-23.1: https://www.openstreetmap.org/copyright (ODbL 1.0; figures here are hectares summed by area)
- CROPGRIDS v1.08 (Tang et al., 2024, Scientific Data): https://doi.org/10.6084/m9.figshare.22491997 (CC BY 4.0)
- TerraClimate monthly normals, 1991-2020 (Abatzoglou et al., 2018): https://www.climatologylab.org/terraclimate.html (Public domain (CC0))
- SoilGrids 2.0 (ISRIC; Poggio et al., 2021): https://soilgrids.org (CC BY 4.0)
- Natural Earth admin 0 and admin 1 boundaries: https://www.naturalearthdata.com (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Strict test: land scoring at least as high as the vineyards that hold three-quarters of today's vineyard hectares in the countries the model learned from. Generous test: nine-tenths.
- Farmland means a cell where at least 5% of the land is cropland (CROPGRIDS, all 173 crops); cells that already hold vines are not counted as suitable farmland.
- Divisions with under 1,000 hectares of suitable farmland are left out.
- Licence for this file: it contains data derived from OpenStreetMap, (c) OpenStreetMap contributors, and is released under the Open Database License (ODbL 1.0, https://opendatacommons.org/licenses/odbl/), not CC BY. You may reuse it with that credit; databases you build from it must also be shared under the ODbL.

How to cite:

Signum Average (2026) - "Farmland suited to vineyards, by province" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/suitable_land_by_province.csv

```bibtex
@misc{signumaverage-suitable-land-by-province,
    author = {{Signum Average}},
    title = {Farmland suited to vineyards, by province},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/suitable_land_by_province.csv}},
    note = {Dataset}
}
```

## wine_market_share_forgone.csv

**Wine market share and sales forgone by countries that plant little of their vineyard land.** For the 21 countries that grow wine grapes on less than 2.6% of their strict-test farmland (the lower quartile of established wine countries), the wine and sales each forgoes compared with holding a share of the world market equal to its share of the world's suitable farmland. Also the physical capacity of the land, which far exceeds what the market can absorb.

Coverage: 21 countries; market of 2025 (low case 2035). Last updated: 2026-10-03.

| Column | Description |
|---|---|
| `iso3` | Country code. |
| `country` | Country name. |
| `farmland_strict_ha` | Farmland passing the strict test, hectares. |
| `wine_grapes_ha_2023` | Wine grapes today, hectares (0 where the database has no entry). |
| `share_of_world_strict_farmland` | The country's share of the world's strict-test farmland. |
| `share_of_world_wine_grapes` | The country's share of the world's wine-grape area, 2023. |
| `wine_forgone_mhl_low` | Wine forgone a year, million hectolitres, low case. |
| `wine_forgone_mhl_central` | Central case. |
| `wine_forgone_mhl_high` | High case. |
| `sales_forgone_usd_bn_low` | Sales forgone a year at export prices, US$bn, low case. |
| `sales_forgone_usd_bn_central` | Central case. |
| `sales_forgone_usd_bn_high` | High case. |
| `capacity_new_wine_grapes_ha_low` | Physical capacity: extra wine-grape hectares if the land were planted as densely as wine countries plant theirs, low case. |
| `capacity_new_wine_grapes_ha_central` | Central case. |
| `capacity_new_wine_grapes_ha_high` | High case. |

Sources:

- OIV, State of the World Wine Sector in 2025 (May 2026): https://www.oiv.int/node/4879 (Figures cited from a public report)
- Anderson, K. and V. Pinilla, Annual Database of Global Wine Markets, 1835 to 2024, University of Adelaide, April 2025: https://economics.adelaide.edu.au/wine-economics/databases (Free to use with citation)
- Anderson, K., S. Nelgen and G. Puga, Database of Regional, National and Global Winegrape Bearing Areas by Variety, 2000 to 2023, University of Adelaide, December 2025: https://economics.adelaide.edu.au/wine-economics/databases (Free to use with citation)
- Signum Average calculations (CC BY 4.0)

Notes:

- Low: share of strict-test farmland, world consumption in 2035 if the 2018-25 decline continues (168m hl), lower-quartile export price of 20 wine countries in 2018-22 (US$1.85 a litre). Central: share of strict-test farmland, 2025 consumption (208m hl), median price (US$2.84). High: the larger of the strict and generous land shares, 2025 consumption, median price.
- A benchmark, not a forecast: it says what land endowment implies, and ignores law, religion, capital, skills and reputation, which explain much of where wine is made.
- Sales are valued at export prices, which are well below what drinkers pay.

How to cite:

Signum Average (2026) - "Wine market share and sales forgone by countries that plant little of their vineyard land" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/wine_market_share_forgone.csv

```bibtex
@misc{signumaverage-wine-market-share-forgone,
    author = {{Signum Average}},
    title = {Wine market share and sales forgone by countries that plant little of their vineyard land},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/wine_market_share_forgone.csv}},
    note = {Dataset}
}
```

## world_wine_market.csv

**World wine production and consumption.** World wine production and consumption in million hectolitres. 2023 is left out because the two sources measure it differently.

Coverage: 1961-2022, 2024-2025. Last updated: 2026-10-03.

| Column | Description |
|---|---|
| `year` | Calendar year. |
| `consumption_mhl` | World wine consumption, million hectolitres. |
| `production_mhl` | World wine production, million hectolitres. |
| `source` | Where the row comes from. |

Sources:

- Anderson, K. and V. Pinilla, Annual Database of Global Wine Markets, 1835 to 2024, University of Adelaide, April 2025: https://economics.adelaide.edu.au/wine-economics/databases (Free to use with citation)
- OIV, State of the World Wine Sector in 2025 (May 2026): https://www.oiv.int/node/4879 (Figures cited from a public report)

Notes:

- 2024 is derived from the OIV's 2025 figures and their change on 2024 (consumption -2.7%, production +0.6%).

How to cite:

Signum Average (2026) - "World wine production and consumption" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/world_wine_market.csv

```bibtex
@misc{signumaverage-world-wine-market,
    author = {{Signum Average}},
    title = {World wine production and consumption},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/world_wine_market.csv}},
    note = {Dataset}
}
```

## wine_grape_area_change.csv

**Wine-grape area by country, 2000-2023.** Wine-grape area by country in four census years and the change from each country's first recorded year to 2023, with a flag for emerging producers.

Coverage: 2000, 2010, 2016, 2023. Last updated: 2026-10-03.

| Column | Description |
|---|---|
| `country` | Country name as in the source. |
| `wine_grapes_ha_2000` | Hectares, 2000. |
| `wine_grapes_ha_2010` | Hectares, 2010. |
| `wine_grapes_ha_2016` | Hectares, 2016. |
| `wine_grapes_ha_2023` | Hectares, 2023. |
| `first_year` | First year the country appears. |
| `change_ha` | Change from the first year to 2023, hectares. |
| `change_pct` | Change from the first year to 2023, %. |
| `emerging` | True if the area at least doubled and grew by 1,000+ hectares, or first appears after 2000 with 1,000+ hectares. |

Sources:

- Anderson, K., S. Nelgen and G. Puga, Database of Regional, National and Global Winegrape Bearing Areas by Variety, 2000 to 2023, University of Adelaide, December 2025: https://economics.adelaide.edu.au/wine-economics/databases (Free to use with citation)

Notes:

- Countries that first appear after 2000 may have had vineyards earlier that the database did not cover.

How to cite:

Signum Average (2026) - "Wine-grape area by country, 2000-2023" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/wine_grape_area_change.csv

```bibtex
@misc{signumaverage-wine-grape-area-change,
    author = {{Signum Average}},
    title = {Wine-grape area by country, 2000-2023},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/wine_grape_area_change.csv}},
    note = {Dataset}
}
```

## model_holdout_test.csv

**Vineyard-suitability model: continent hold-out test.** How well the model finds the vineyards of a continent it was not trained on, against a textbook rule based on growing-season temperature.

Coverage: Six continents. Last updated: 2026-10-03.

| Column | Description |
|---|---|
| `continent` | Continent hidden from the model. |
| `vineyard_cells` | Vineyard cells (about 9 km) on that continent in the training countries. |
| `auc_model` | Area under the ROC curve for the model: 0.5 is a coin toss, 1 is perfect. |
| `auc_rule` | The same for the rule: distance of growing-season temperature from 17C. |
| `top10_model` | Share of the continent's vine hectares in its best-scoring tenth of land, model. |
| `top10_rule` | The same for the rule. |

Sources:

- Signum Average calculations (CC BY 4.0)

Notes:

- Asia has too few vineyard cells with a trustworthy map (69, all in Armenia) for the test to mean much.

How to cite:

Signum Average (2026) - "Vineyard-suitability model: continent hold-out test" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/model_holdout_test.csv

```bibtex
@misc{signumaverage-model-holdout-test,
    author = {{Signum Average}},
    title = {Vineyard-suitability model: continent hold-out test},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/model_holdout_test.csv}},
    note = {Dataset}
}
```

## model_known_places.csv

**Vineyard-suitability model: scores of known wine regions and control places.** The model's score for the 9 km cell at well-known wine regions and at places that should fail (desert, rainforest, Siberia, the US corn belt). Wine-country cells are scored by models that never saw that country.

Coverage: 29 places. Last updated: 2026-10-03.

| Column | Description |
|---|---|
| `place` | Place. |
| `lat` | Latitude of the point looked up. |
| `lon` | Longitude. |
| `score` | Suitability score, 0-1. |
| `share_of_wine_country_land_scoring_lower` | Share of all land in the training countries that scores lower. |
| `test` | Which test the cell passes: strict, generous or neither. |

Sources:

- Signum Average calculations (CC BY 4.0)

Notes:

- One cell per place, so a single point can miss a region whose vineyards lie a few kilometres away.

How to cite:

Signum Average (2026) - "Vineyard-suitability model: scores of known wine regions and control places" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/model_known_places.csv

```bibtex
@misc{signumaverage-model-known-places,
    author = {{Signum Average}},
    title = {Vineyard-suitability model: scores of known wine regions and control places},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/model_known_places.csv}},
    note = {Dataset}
}
```

## rated_regions_climate_soil.csv

**Wine regions: consumer ratings with the climate and soil of their vineyards.** Every wine region with at least 300 consumer ratings that we could locate and that has vines nearby, with its rating against the average for wines of the same type and the climate and soil of its vineyards. Used to test whether land predicts quality; it does not, at this scale.

Coverage: 694 regions in 42 countries; ratings 2012-2021. Last updated: 2026-10-03.

| Column | Description |
|---|---|
| `country` | Country, as in X-Wines. |
| `region` | Region name, as in X-Wines. |
| `lat` | Latitude found by OpenStreetMap's geocoder. |
| `lon` | Longitude. |
| `wines` | Number of wines rated. |
| `ratings` | Number of ratings. |
| `rating_vs_type_average` | Average rating minus the average for wines of the same type, stars, pulled towards zero for regions with few ratings (300 ratings' worth). |
| `suitability_score` | The vineyard-suitability model's score for the region's land, 0-1. |
| `gst` | Growing-season average temperature, C. |
| `huglin` | Huglin heat index. |
| `cool_night` | Night temperature in the ripening month, C. |
| `tmin_coldest` | Night temperature in the coldest month, C. |
| `prec_gs` | Rain in the growing season, mm. |
| `prec_ripening` | Rain in the two months before harvest, mm. |
| `srad_gs` | Sunshine at the ground in the growing season, W/m2. |
| `aridity` | Rain over potential evaporation, year. |
| `soil_phh2o` | Soil pH x 10, 15-30cm. |
| `soil_clay` | Clay, g/kg, 15-30cm. |
| `soil_sand` | Sand, g/kg, 15-30cm. |
| `elev` | Elevation, m. |

Sources:

- X-Wines (Azambuja, Morais and Filipe, 2023): https://github.com/rogerioxavier/X-Wines (CC0 1.0)
- OpenStreetMap Nominatim geocoder: https://nominatim.openstreetmap.org (ODbL 1.0)
- TerraClimate (1991-2020) and SoilGrids 2.0: https://www.climatologylab.org/terraclimate.html (Public domain; CC BY 4.0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Climate and soil are averages over grid squares within the region's outline, weighted by vine hectares.
- Geocoding can place a region at a town or administrative area of the same name; regions without vines nearby were dropped for that reason.
- Licence for this file: it contains data derived from OpenStreetMap, (c) OpenStreetMap contributors, and is released under the Open Database License (ODbL 1.0, https://opendatacommons.org/licenses/odbl/), not CC BY. You may reuse it with that credit; databases you build from it must also be shared under the ODbL.

How to cite:

Signum Average (2026) - "Wine regions: consumer ratings with the climate and soil of their vineyards" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/rated_regions_climate_soil.csv

```bibtex
@misc{signumaverage-rated-regions-climate-soil,
    author = {{Signum Average}},
    title = {Wine regions: consumer ratings with the climate and soil of their vineyards},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-02_undiscovered-wine/rated_regions_climate_soil.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
