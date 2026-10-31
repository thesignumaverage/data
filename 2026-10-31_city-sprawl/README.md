# Data for https://signumaverage.com/articles/city-sprawl/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## top25.csv

**The 25 largest metro areas of the US, Canada and Mexico, 1975-2025.** Built-up land and residents in each of the 25 largest metros, with growth, the UN's land-to-population ratio and land per resident.

Coverage: 1975, 1990, 2000, 2010, 2020, 2025. Last updated: 2026-10-31.

| Column | Description |
|---|---|
| `efua_id, name, country` | The metro (country code of the outline's main part). |
| `built_km2_<year>, residents_<year>` | Built-up land, km2, and residents. |
| `built_growth_<from>, residents_growth_<from>` | 2025 as a multiple of 1975 or 1990. |
| `un_ratio_<from>` | Rate of land growth divided by rate of population growth (UN indicator 11.3.1). Above 1: land grew faster. Negative where residents fell. |
| `land_per_resident_m2_<year>` | Built-up land per resident, m2. |
| `volume_per_resident_m3_<year>` | Built volume per resident, m3. Heights are measured only around 2018; other years are estimates. |

Sources:

- European Commission, Joint Research Centre, Global Human Settlement Layer: GHS-BUILT-S, GHS-BUILT-V and GHS-POP (R2023A, 1 km) and GHS-FUA (R2019A): https://human-settlement.emergency.copernicus.eu/ (CC BY 4.0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Each metro is measured inside one fixed outline (the Global Human Settlement Layer's functional urban area: a city and the area that commutes to it). Built-up land is ground covered by buildings. Residents are spread from census counts onto the map.
- San Diego-Tijuana crosses the border and is listed as US. The area labelled San Jose in the source is shown as the San Francisco Bay Area.

How to cite:

Signum Average (2026) - "The 25 largest metro areas of the US, Canada and Mexico, 1975-2025" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-31_city-sprawl/top25.csv

```bibtex
@misc{signumaverage-top25,
    author = {{Signum Average}},
    title = {The 25 largest metro areas of the US, Canada and Mexico, 1975-2025},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-31_city-sprawl/top25.csv}},
    note = {Dataset}
}
```

## metros_by_year.csv

**Every metro area of the US, Canada and Mexico, 1975-2025.** Built-up land, built volume and residents inside every functional urban area of the three countries.

Coverage: 443 metros, six years. Last updated: 2026-10-31.

| Column | Description |
|---|---|
| `efua_id, name, country, year` | The metro and year. |
| `built_km2, built_volume_km3, residents` | Built-up land (km2), built volume (km3) and residents. |
| `land_per_resident_m2, volume_per_resident_m3` | Per resident. |

Sources:

- European Commission, Joint Research Centre, Global Human Settlement Layer: GHS-BUILT-S, GHS-BUILT-V and GHS-POP (R2023A, 1 km) and GHS-FUA (R2019A): https://human-settlement.emergency.copernicus.eu/ (CC BY 4.0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Each metro is measured inside one fixed outline (the Global Human Settlement Layer's functional urban area: a city and the area that commutes to it). Built-up land is ground covered by buildings. Residents are spread from census counts onto the map.

How to cite:

Signum Average (2026) - "Every metro area of the US, Canada and Mexico, 1975-2025" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-31_city-sprawl/metros_by_year.csv

```bibtex
@misc{signumaverage-metros-by-year,
    author = {{Signum Average}},
    title = {Every metro area of the US, Canada and Mexico, 1975-2025},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-31_city-sprawl/metros_by_year.csv}},
    note = {Dataset}
}
```

## countries.csv

**Largest metros by country, 1975-2025.** Built-up land, volume and residents summed over each country's metros among the 25 largest.

Coverage: The 25 largest metros grouped by country. Last updated: 2026-10-31.

| Column | Description |
|---|---|
| `country, year` | Country and year. |
| `built_km2, residents, built_volume_km3` | Totals. |
| `land_per_resident_m2` | Built-up land per resident, m2. |

Sources:

- European Commission, Joint Research Centre, Global Human Settlement Layer: GHS-BUILT-S, GHS-BUILT-V and GHS-POP (R2023A, 1 km) and GHS-FUA (R2019A): https://human-settlement.emergency.copernicus.eu/ (CC BY 4.0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Each metro is measured inside one fixed outline (the Global Human Settlement Layer's functional urban area: a city and the area that commutes to it). Built-up land is ground covered by buildings. Residents are spread from census counts onto the map.

How to cite:

Signum Average (2026) - "Largest metros by country, 1975-2025" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-31_city-sprawl/countries.csv

```bibtex
@misc{signumaverage-countries,
    author = {{Signum Average}},
    title = {Largest metros by country, 1975-2025},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-31_city-sprawl/countries.csv}},
    note = {Dataset}
}
```

## check_census.csv

**Satellite-based residents against the 2020 census, US metros.** Residents inside each US outline (GHSL) against the census count of the nearest metropolitan statistical area.

Coverage: 2020. Last updated: 2026-10-31.

| Column | Description |
|---|---|
| `name, census_area` | Our metro and the census metro compared. |
| `census_2020, ghsl_2020` | Residents by each source. |
| `ratio` | GHSL divided by census. |

Sources:

- European Commission, Joint Research Centre, Global Human Settlement Layer: GHS-BUILT-S, GHS-BUILT-V and GHS-POP (R2023A, 1 km) and GHS-FUA (R2019A): https://human-settlement.emergency.copernicus.eu/ (CC BY 4.0)
- US Census Bureau, metropolitan statistical area population, estimates base 2020: https://www2.census.gov/programs-surveys/popest/datasets/2020-2023/metro/totals/ (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Outlines differ, so this checks size, not an exact match.

How to cite:

Signum Average (2026) - "Satellite-based residents against the 2020 census, US metros" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-31_city-sprawl/check_census.csv

```bibtex
@misc{signumaverage-check-census,
    author = {{Signum Average}},
    title = {Satellite-based residents against the 2020 census, US metros},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-31_city-sprawl/check_census.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
