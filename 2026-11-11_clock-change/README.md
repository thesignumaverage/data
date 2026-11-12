# Data for https://signumaverage.com/articles/clock-change/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## clock-by-day.csv

**Pedestrian deaths by day around the autumn clock change.** Pedestrians killed on each day from three weeks before the autumn clock change to three weeks after, by hour band, all years 1975-2024 added together.

Coverage: 1975-2024. Last updated: 2026-11-11.

| Column | Description |
|---|---|
| `rel_fall` | Days from the change (0 = the Sunday the clocks go back). |
| `morning` | Killed 06:00-07:59. |
| `evening` | Killed 17:00-18:59. |
| `control` | Killed 20:00-23:59 (dark before and after). |
| `other` | Killed at any other hour. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian (code 3 in 1975-1981, 5 from 1982) with a fatal injury. Hours are local clock time. Arizona and Hawaii (no clock change) are kept apart; Indiana is left out before 2006; territories left out.

How to cite:

Signum Average (2026) - "Pedestrian deaths by day around the autumn clock change" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/by_day_fall.csv

```bibtex
@misc{signumaverage-clock-by-day,
    author = {{Signum Average}},
    title = {Pedestrian deaths by day around the autumn clock change},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/by_day_fall.csv}},
    note = {Dataset}
}
```

## clock-by-year.csv

**Pedestrian deaths around the autumn clock change, year by year.** For each year, the date the clocks went back and the pedestrians killed in each hour band in the 21 days before (days -21 to -1) and the 21 days from it (days 0 to 20).

Coverage: 1975-2024. Last updated: 2026-11-11.

| Column | Description |
|---|---|
| `year` | Year. |
| `fall_back` | Date the clocks went back. |
| `evening_after, evening_before` | Killed 17:00-18:59 after and before. |
| `control_after, control_before` | Killed 20:00-23:59 after and before. |
| `morning_after, morning_before` | Killed 06:00-07:59 after and before. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian (code 3 in 1975-1981, 5 from 1982) with a fatal injury. Hours are local clock time. Arizona and Hawaii (no clock change) are kept apart; Indiana is left out before 2006; territories left out.

How to cite:

Signum Average (2026) - "Pedestrian deaths around the autumn clock change, year by year" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/by_year_fall.csv

```bibtex
@misc{signumaverage-clock-by-year,
    author = {{Signum Average}},
    title = {Pedestrian deaths around the autumn clock change, year by year},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/by_year_fall.csv}},
    note = {Dataset}
}
```

## clock-change-dates.csv

**US clock change dates, 1975-2024.** The Sunday the clocks went back in autumn and forward in spring, each year, by the federal rule of the time.

Coverage: 1975-2024. Last updated: 2026-11-11.

| Column | Description |
|---|---|
| `year` | Year. |
| `fall_back` | Autumn change: last Sunday of October to 2006, first Sunday of November from 2007. |
| `spring_forward` | Spring change: 23 February 1975; last Sunday of April 1976-1986; first Sunday of April 1987-2006; second Sunday of March from 2007. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian (code 3 in 1975-1981, 5 from 1982) with a fatal injury. Hours are local clock time. Arizona and Hawaii (no clock change) are kept apart; Indiana is left out before 2006; territories left out.

How to cite:

Signum Average (2026) - "US clock change dates, 1975-2024" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/change_dates.csv

```bibtex
@misc{signumaverage-clock-change-dates,
    author = {{Signum Average}},
    title = {US clock change dates, 1975-2024},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/change_dates.csv}},
    note = {Dataset}
}
```

## clock-light.csv

**Light at the scene, evening pedestrian deaths around the autumn change.** Pedestrians killed 17:00-18:59 in the three weeks before and after the autumn change, by the light condition the police recorded, 1975-2024.

Coverage: 1975-2024. Last updated: 2026-11-11.

| Column | Description |
|---|---|
| `when` | Before or after the change. |
| `dark, dawn or dusk, daylight, unknown` | Deaths by recorded light condition. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian (code 3 in 1975-1981, 5 from 1982) with a fatal injury. Hours are local clock time. Arizona and Hawaii (no clock change) are kept apart; Indiana is left out before 2006; territories left out.
- Light code 6 means dawn or dusk in 1975-1979 and dark with unknown lighting from 2009; it is grouped by year.

How to cite:

Signum Average (2026) - "Light at the scene, evening pedestrian deaths around the autumn change" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/light_evening.csv

```bibtex
@misc{signumaverage-clock-light,
    author = {{Signum Average}},
    title = {Light at the scene, evening pedestrian deaths around the autumn change},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/light_evening.csv}},
    note = {Dataset}
}
```

## clock-winter-hours.csv

**Pedestrian deaths by hour of day, November to February.** Pedestrians killed in November, December, January and February, by hour of the day, 1975-2024 added together.

Coverage: 1975-2024. Last updated: 2026-11-11.

| Column | Description |
|---|---|
| `HOUR` | Hour of the day, local time (17 = 17:00-17:59). |
| `deaths` | Pedestrians killed. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian (code 3 in 1975-1981, 5 from 1982) with a fatal injury. Hours are local clock time. Arizona and Hawaii (no clock change) are kept apart; Indiana is left out before 2006; territories left out.

How to cite:

Signum Average (2026) - "Pedestrian deaths by hour of day, November to February" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/by_hour_winter.csv

```bibtex
@misc{signumaverage-clock-winter-hours,
    author = {{Signum Average}},
    title = {Pedestrian deaths by hour of day, November to February},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/by_hour_winter.csv}},
    note = {Dataset}
}
```

## clock-tests.csv

**Every test of the clock change.** Each comparison in the study: the change in pedestrian deaths in an hour band after a clock change against before, relative to 20:00-23:59, with its 95% range and the counts behind it.

Coverage: 1975-2024. Last updated: 2026-11-11.

| Column | Description |
|---|---|
| `test` | The comparison. |
| `hours` | Hour band. |
| `ratio, low, high` | Ratio of ratios and its 95% range (Poisson). |
| `counts` | The counts used, in the order given in note. |
| `note` | Order of the counts. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian (code 3 in 1975-1981, 5 from 1982) with a fatal injury. Hours are local clock time. Arizona and Hawaii (no clock change) are kept apart; Indiana is left out before 2006; territories left out.

How to cite:

Signum Average (2026) - "Every test of the clock change" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/tests.csv

```bibtex
@misc{signumaverage-clock-tests,
    author = {{Signum Average}},
    title = {Every test of the clock change},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/tests.csv}},
    note = {Dataset}
}
```

## clock-lives-2007.csv

**Lives a year spared by the 2007 rule.** Pedestrian deaths a year spared in the week that moved in 2007 (exploratory): expected under the old rule against observed under the new, 2007-2024, with 95% ranges from 20,000 Poisson draws.

Coverage: 1975-2024. Last updated: 2026-11-11.

| Column | Description |
|---|---|
| `hours` | Hour band, or net for both. |
| `expected_new_rule, observed_new_rule` | Deaths over 2007-2024 in that week: expected had the clocks gone back as before, and observed. |
| `spared_a_year, low, high` | Deaths a year spared (negative: added) and the 95% range. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian (code 3 in 1975-1981, 5 from 1982) with a fatal injury. Hours are local clock time. Arizona and Hawaii (no clock change) are kept apart; Indiana is left out before 2006; territories left out.

How to cite:

Signum Average (2026) - "Lives a year spared by the 2007 rule" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/lives_2007.csv

```bibtex
@misc{signumaverage-clock-lives-2007,
    author = {{Signum Average}},
    title = {Lives a year spared by the 2007 rule},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-11_clock-change/lives_2007.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
