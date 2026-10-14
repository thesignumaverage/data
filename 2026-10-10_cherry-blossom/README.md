# Data for https://signumaverage.com/articles/cherry-blossom/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## bloom_dates.csv

**Japan's cherry blossom: first and full bloom by station and year.** The date of first bloom and of full bloom of the Somei Yoshino cherry at each weather station with 30 or more years of records, tidied from the agency's files.

Coverage: 80 weather stations, 1953-2026. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `station` | The station's international number. |
| `name, region` | Station name and the agency's forecast region. |
| `year` | Year of the spring. |
| `event` | first = five or six flowers open on the index tree; full = 80% of buds open. |
| `date` | Date declared. |
| `day_of_year` | The same as a day of the year (1 January = 1). |
| `source` | file = the agency's yearly file; page = its web page of recent dates (2026). |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- Substitute species (in northern and eastern Hokkaido, Okinawa and Amami) are left out.
- Changed from the original: reshaped to one row a date, station names in English.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: first and full bloom by station and year" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/bloom_dates.csv

```bibtex
@misc{signumaverage-bloom-dates,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: first and full bloom by station and year},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/bloom_dates.csv}},
    note = {Dataset}
}
```

## stations.csv

**Japan's cherry blossom: the weather stations.** The stations used, with their position and whether they still observe the cherry.

Coverage: 80 stations. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `station` | The station's international number. |
| `name, name_ja` | Name in English and Japanese. |
| `region` | The agency's forecast region. |
| `lat, lon, height_m` | Position in degrees and height in metres. |
| `last_year` | Last year with a full-bloom date. |
| `observing` | True if the station recorded full bloom in 2025 or 2026. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- Only observations of the regular species, Somei Yoshino, are used. A day of the season counts from 1 October, with 29 February left out.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: the weather stations" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/stations.csv

```bibtex
@misc{signumaverage-stations,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: the weather stations},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/stations.csv}},
    note = {Dataset}
}
```

## station_trends.csv

**Japan's cherry blossom: the trend at each station.** A straight-line trend in the date of full bloom and of first bloom at each station, in days a decade, with a 95% range. The article's map shows the 48 stations still observing.

Coverage: 75 stations with 40 or more years, 1953 to their last year. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `station, name, lat` | The station. |
| `years, last_year` | Years of full-bloom dates and the last of them. |
| `full_days_per_decade` | Trend in full bloom, days a decade. Negative = earlier. |
| `full_low, full_high` | 95% range of that trend. |
| `first_days_per_decade, first_low, first_high` | The same for first bloom. |
| `still_observing` | True if the record runs to 2025 or later. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- Closed stations end between 1997 and 2012, before the fastest years, so their trends are not comparable with the rest.
- Only observations of the regular species, Somei Yoshino, are used. A day of the season counts from 1 October, with 29 February left out.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: the trend at each station" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/station_trends.csv

```bibtex
@misc{signumaverage-station-trends,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: the trend at each station},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/station_trends.csv}},
    note = {Dataset}
}
```

## decade_averages.csv

**Japan's cherry blossom: 1956-65 against 2016-25.** The average date of full bloom at each station in the two decades, and the change between them.

Coverage: 46 stations with seven or more years in both decades. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `station, name, region, lat, lon` | The station. |
| `average_1956_65, average_2016_25` | Average date of full bloom, written as a date in a non-leap year. |
| `day_1956_65, day_2016_25` | The same as a day of the season (1 October = 0, so 1 April = 182). |
| `change_days` | Change in days. Negative = earlier. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- Only observations of the regular species, Somei Yoshino, are used. A day of the season counts from 1 October, with 29 February left out.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: 1956-65 against 2016-25" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/decade_averages.csv

```bibtex
@misc{signumaverage-decade-averages,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: 1956-65 against 2016-25},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/decade_averages.csv}},
    note = {Dataset}
}
```

## ranges.csv

**Japan's cherry blossom: ranges for the headline numbers.** 95% ranges for the comparisons between the two decades, from resampling years within each decade 2,000 times (the same years for every station).

Coverage: 1956-65 and 2016-25. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `measure` | What is measured: the change in days by band of latitude; the slope of full-bloom date on latitude south of 35°N, days per degree, then and now; Tokyo's date minus Kagoshima's; Kagoshima's change. |
| `low, middle, high` | The 2.5th, 50th and 97.5th percentiles. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- Only observations of the regular species, Somei Yoshino, are used. A day of the season counts from 1 October, with 29 February left out.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: ranges for the headline numbers" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/ranges.csv

```bibtex
@misc{signumaverage-ranges,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: ranges for the headline numbers},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/ranges.csv}},
    note = {Dataset}
}
```

## other_decades.csv

**Japan's cherry blossom: the same comparison with other decades.** How the comparison of decades changes with the decades chosen.

Coverage: Twelve pairings of an early and a late decade. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `early, late` | The two decades. |
| `stations` | Stations with seven or more years in both. |
| `slope_south_then, slope_south_now` | Days of full-bloom date per degree of latitude, south of 35°N. |
| `change_south_of_33, change_33_to_35, change_35_to_38, change_north_of_38` | Mean change in days by band of latitude. |
| `kagoshima` | Kagoshima's change in days. |
| `stations_later` | Stations whose average moved later. |
| `first_now` | The station with the earliest average in the late decade. |
| `tokyo_minus_kagoshima_now` | Tokyo's average day minus Kagoshima's in the late decade. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- The north's large gain appears only with the latest decade.
- Only observations of the regular species, Somei Yoshino, are used. A day of the season counts from 1 October, with 29 February left out.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: the same comparison with other decades" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/other_decades.csv

```bibtex
@misc{signumaverage-other-decades,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: the same comparison with other decades},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/other_decades.csv}},
    note = {Dataset}
}
```

## winter_effect_by_station.csv

**Japan's cherry blossom: what a warmer winter does, by station.** For each station, a regression of the day of first bloom on mean December-January and February-March temperature.

Coverage: 76 stations with 40 or more seasons, 1954-2026. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `station, name, region` | The station. |
| `seasons` | Seasons used. |
| `normal_dec_jan` | Mean December-January temperature, 1991-2020, °C. |
| `winter_coef, winter_se` | Days by which first bloom moves per degree of December-January warmth, and its standard error. Positive = later. |
| `spring_coef, spring_se` | The same for February-March. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- Neighbouring stations share weather, so the stations are not independent tests; the full report, sent on request, gives the ranges.
- Only observations of the regular species, Somei Yoshino, are used. A day of the season counts from 1 October, with 29 February left out.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: what a warmer winter does, by station" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/winter_effect_by_station.csv

```bibtex
@misc{signumaverage-winter-effect-by-station,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: what a warmer winter does, by station},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/winter_effect_by_station.csv}},
    note = {Dataset}
}
```

## model_scores.csv

**Japan's cherry blossom: how well each model dates the bloom.** The mean miss, in days, of three bloom models and three naive guesses when the weather is known.

Coverage: Fitted on 1954-2000, scored on 2001-2026. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `event` | full or first bloom. |
| `model` | The model or naive guess. |
| `sample` | training; hidden years (2001-26); or hidden years in the warmest third of stations and in the rest. |
| `station_springs` | Number of station-springs scored. |
| `mean_miss_days` | Mean absolute error, days. |
| `bias_days` | Mean error, days. Positive = predicted too late. |
| `share_within_2_days` | Share of predictions within two days. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- The models' fitted numbers are not published.
- Only observations of the regular species, Somei Yoshino, are used. A day of the season counts from 1 October, with 29 February left out.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: how well each model dates the bloom" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/model_scores.csv

```bibtex
@misc{signumaverage-model-scores,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: how well each model dates the bloom},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/model_scores.csv}},
    note = {Dataset}
}
```

## forecast_by_issue_date.csv

**Japan's cherry blossom: how early can full bloom be forecast.** The mean miss of our forecast of full bloom by the date it is issued, against two naive guesses.

Coverage: 1,449 station-springs, 2001-2026. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `issued` | Issue date. |
| `days_of_season_known` | Days of real weather the forecast had, counted from 1 October. |
| `miss_trend_only` | Mean miss in days when past seasons are drawn evenly. |
| `miss_with_el_nino` | Mean miss when past seasons are weighted by their El Niño index. |
| `miss_ten_year_average, miss_station_trend` | Mean miss of the two naive guesses. |
| `in_80_range` | Share of springs in which the forecast's 80% range held the truth. |
| `station_springs` | Number scored. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- US National Oceanic and Atmospheric Administration, relative Oceanic Niño Index: https://www.cpc.ncep.noaa.gov/data/indices/RONI.ascii.txt (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Each forecast uses only what was known on its date. The later issue dates were added after the October result was seen.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: how early can full bloom be forecast" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/forecast_by_issue_date.csv

```bibtex
@misc{signumaverage-forecast-by-issue-date,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: how early can full bloom be forecast},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/forecast_by_issue_date.csv}},
    note = {Dataset}
}
```

## spring_2027.csv

**Japan's cherry blossom: full bloom in spring 2027.** The date of full bloom each station's own trend points to for 2027, with the range that held 80% of its past misses.

Coverage: 48 stations still observing. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `station, name, region` | The station. |
| `trend_date` | The station's straight-line trend, read at 2027. |
| `low_date, high_date` | 80% range. |
| `ten_year_average_date` | Mean of 2017-26. |
| `model_date_for_reference` | The median of our model's forecast issued on 10 October 2026. It did not beat the trend in tests and is shown for the record only. |
| `average_1991_2020` | The 1991-2020 average. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- Signum Average calculations (CC BY 4.0)

Notes:

- To be checked against the dates the agency declares in spring 2027.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: full bloom in spring 2027" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/spring_2027.csv

```bibtex
@misc{signumaverage-spring-2027,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: full bloom in spring 2027},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/spring_2027.csv}},
    note = {Dataset}
}
```

## el_nino_winters.csv

**Japan's cherry blossom: El Niño winters.** Winter temperature and the date of full bloom in El Niño, La Niña and neutral winters, each measured against the station's own previous 15 years.

Coverage: Winters of 1953-54 to 2025-26. Last updated: 2026-10-11.

| Column | Description |
|---|---|
| `region` | Japan, or one of the agency's regions. |
| `state` | Strong El Niño (October-December index 1.5 or more), El Niño (0.5 or more), La Niña (minus 0.5 or less) or neutral. |
| `winters` | Number of winters. |
| `winter_temp_gap, temp_low, temp_high` | December-February temperature against the previous 15 years, °C, with a 90% range from resampling winters. |
| `bloom_gap_days, bloom_low, bloom_high` | Day of full bloom against the previous 15 years, days, with a 90% range. Negative = earlier. |

Sources:

- Japan Meteorological Agency, phenological observations and past weather data: https://www.data.jma.go.jp/sakura/data/index.html (Public Data License 1.0 (reuse with the source named and changes noted))
- US National Oceanic and Atmospheric Administration, relative Oceanic Niño Index: https://www.cpc.ncep.noaa.gov/data/indices/RONI.ascii.txt (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Bloom dates are trending earlier, so every group sits a little below zero; compare the groups with each other.

How to cite:

Signum Average (2026) - "Japan's cherry blossom: El Niño winters" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/el_nino_winters.csv

```bibtex
@misc{signumaverage-el-nino-winters,
    author = {{Signum Average}},
    title = {Japan's cherry blossom: El Niño winters},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-10_cherry-blossom/el_nino_winters.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
