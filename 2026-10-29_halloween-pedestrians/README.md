# Data for https://signumaverage.com/articles/halloween-pedestrians/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## evenings_october_november.csv

**Children killed on foot each evening of October and November.** Pedestrians aged 4 to 17 killed between 5pm and midnight on each day from 1 October to 30 November, and pedestrians of all ages on the same evenings.

Coverage: 1975-2024, all years added together. Last updated: 2026-10-29.

| Column | Description |
|---|---|
| `month, day` | The date. |
| `child_deaths` | Pedestrians aged 4 to 17 killed between 5pm and midnight, 1975-2024. |
| `all_ages` | Pedestrians of any age killed on the same evenings. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian with a fatal injury. Evening: 5pm to midnight, local time. Children: aged 4 to 17.

How to cite:

Signum Average (2026) - "Children killed on foot each evening of October and November" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/evenings_october_november.csv

```bibtex
@misc{signumaverage-evenings-october-november,
    author = {{Signum Average}},
    title = {Children killed on foot each evening of October and November},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/evenings_october_november.csv}},
    note = {Dataset}
}
```

## evenings_ranked.csv

**Every evening of the year ranked by children killed on foot.** The 365 evenings of the year (29 February left out) ranked by pedestrians aged 4 to 17 killed between 5pm and midnight.

Coverage: 1975-2024, all years added together. Last updated: 2026-10-29.

| Column | Description |
|---|---|
| `month, day` | The date. |
| `child_deaths` | Children killed, 1975-2024. |
| `rank` | 1 = the deadliest evening. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian with a fatal injury. Evening: 5pm to midnight, local time. Children: aged 4 to 17.

How to cite:

Signum Average (2026) - "Every evening of the year ranked by children killed on foot" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/evenings_ranked.csv

```bibtex
@misc{signumaverage-evenings-ranked,
    author = {{Signum Average}},
    title = {Every evening of the year ranked by children killed on foot},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/evenings_ranked.csv}},
    note = {Dataset}
}
```

## halloween_by_year.csv

**Halloween and ordinary evenings, year by year.** Pedestrian deaths on Halloween evening and on the two control evenings a week before and after, each year, with the year's totals.

Coverage: 1975-2024. Last updated: 2026-10-29.

| Column | Description |
|---|---|
| `year` | Year. |
| `halloween_all, controls_all` | Pedestrians of all ages killed on Halloween evening and on the two control evenings together. |
| `halloween_children, controls_children` | The same for ages 4 to 17. |
| `children_all_year, pedestrians_all_year` | All pedestrian deaths in the year: ages 4 to 17, and all ages. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian with a fatal injury. Evening: 5pm to midnight, local time. Children: aged 4 to 17.
- Control evenings: 24 October and 7 November, the same day of the week as Halloween. The 2024 figures may be revised.

How to cite:

Signum Average (2026) - "Halloween and ordinary evenings, year by year" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/halloween_by_year.csv

```bibtex
@misc{signumaverage-halloween-by-year,
    author = {{Signum Average}},
    title = {Halloween and ordinary evenings, year by year},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/halloween_by_year.csv}},
    note = {Dataset}
}
```

## halloween_ratios.csv

**How much deadlier Halloween evening is, by age and period.** Pedestrian deaths on Halloween evening for every death on the average control evening, with an exact 95% range.

Coverage: 1975-2016, 2017-2024, 1975-2024 and by decade. Last updated: 2026-10-29.

| Column | Description |
|---|---|
| `period` | Years compared. 1975-2016 repeats the 2018 study by Staples, Yip and Redelmeier. |
| `group` | All ages, children 4-17, or an age band. |
| `halloween_deaths, control_deaths` | Deaths on Halloween evenings and on the control evenings (two a year). |
| `ratio, low, high` | Halloween deaths divided by half the control deaths, and its 95% range. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian with a fatal injury. Evening: 5pm to midnight, local time. Children: aged 4 to 17.
- Small counts give wide ranges, especially for 2017-2024.

How to cite:

Signum Average (2026) - "How much deadlier Halloween evening is, by age and period" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/halloween_ratios.csv

```bibtex
@misc{signumaverage-halloween-ratios,
    author = {{Signum Average}},
    title = {How much deadlier Halloween evening is, by age and period},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/halloween_ratios.csv}},
    note = {Dataset}
}
```

## halloween_by_decade.csv

**Children killed on Halloween evening, decade by decade.** Average deaths a year on Halloween evening and on an ordinary evening, and all pedestrian deaths a year, by decade.

Coverage: 1975-2024 in five decades. Last updated: 2026-10-29.

| Column | Description |
|---|---|
| `decade, years` | The decade and the years in it. |
| `halloween_child_deaths_a_year, control_child_deaths_a_year` | Children 4-17 killed on Halloween evening, and on the average control evening, a year. |
| `child_pedestrian_deaths_a_year` | All pedestrians aged 4-17 killed in the year, any day or hour. |
| `halloween_deaths_all_ages_a_year, control_deaths_all_ages_a_year, pedestrian_deaths_all_ages_a_year` | The same for all ages. |

Sources:

- US National Highway Traffic Safety Administration, Fatality Analysis Reporting System (FARS), 1975-2024: https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- A pedestrian death: a person of type pedestrian with a fatal injury. Evening: 5pm to midnight, local time. Children: aged 4 to 17.

How to cite:

Signum Average (2026) - "Children killed on Halloween evening, decade by decade" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/halloween_by_decade.csv

```bibtex
@misc{signumaverage-halloween-by-decade,
    author = {{Signum Average}},
    title = {Children killed on Halloween evening, decade by decade},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-29_halloween-pedestrians/halloween_by_decade.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
