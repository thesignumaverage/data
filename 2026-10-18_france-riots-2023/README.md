# Data for https://signumaverage.com/articles/france-riots-2023/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## riot-towns-2023.csv

**France's 2023 riots: towns and nights with a riot incident reported in the press.** One row per town and night with a riot incident reported in a news article, with the article's link. Built from 3,654 articles; each entry was read in its source; an independent check of a random tenth found 8% wrong.

Coverage: 264 communes, 27 June-5 July 2023. Last updated: 2026-10-21.

| Column | Description |
|---|---|
| `insee_code` | INSEE commune code (2023 geography). |
| `commune` | Commune name. |
| `departement` | Département code. |
| `night` | Date of the evening the night began. |
| `night_basis` | stated: the night is given in the text; inferred: the night before a same-day or next-morning report. |
| `incident` | Short description of the incident, in our words. |
| `source_url` | Article reporting it. |

Sources:

- GDELT Project (links to articles): https://www.gdeltproject.org/ (Open, with citation)
- Signum Average list (CC BY 4.0)

Notes:

- The list misses many small towns: the French Senate counted 672 communes with incidents. It shows where riots were reported, not every place they happened.
- No people are named; the list holds places and dates only.

How to cite:

Signum Average (2026) - "France's 2023 riots: towns and nights with a riot incident reported in the press" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-18_france-riots-2023/riot_towns_2023.csv

```bibtex
@misc{signumaverage-riot-towns-2023,
    author = {{Signum Average}},
    title = {France's 2023 riots: towns and nights with a riot incident reported in the press},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-18_france-riots-2023/riot_towns_2023.csv}},
    note = {Dataset}
}
```

## riot-waves-2005-2023.csv

**Vehicles burned and arrests each night, French riots of 2005 and 2023.** The nightly national counts behind the chart of the two waves.

Coverage: 21 nights of 2005, 9 nights of 2023. Last updated: 2026-10-21.

| Column | Description |
|---|---|
| `episode` | 2005 or 2023. |
| `night_index` | Night of the riots, from 1. |
| `night_start` | Date of the evening the night began. |
| `vehicles_burned` | Vehicles burned that night. |
| `arrests` | Arrests that night (blank where not reported). |
| `source` | Source. |

Sources:

- Émeutes de 2005 dans les banlieues françaises (fr.wikipedia): https://fr.wikipedia.org/wiki/%C3%89meutes_de_2005_dans_les_banlieues_fran%C3%A7aises (CC BY-SA 4.0)
- Émeutes consécutives à la mort de Nahel Merzouk (fr.wikipedia): https://fr.wikipedia.org/wiki/%C3%89meutes_cons%C3%A9cutives_%C3%A0_la_mort_de_Nahel_Merzouk (CC BY-SA 4.0)

Notes:

- Counts may include ordinary car fires, about 100 a night in the mid-2000s.
- Other official totals differ: the Senate counts 12,031 vehicles and 4,282 people in custody for 27 June-10 July 2023.

How to cite:

Signum Average (2026) - "Vehicles burned and arrests each night, French riots of 2005 and 2023" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-18_france-riots-2023/national_waves.csv

```bibtex
@misc{signumaverage-riot-waves-2005-2023,
    author = {{Signum Average}},
    title = {Vehicles burned and arrests each night, French riots of 2005 and 2023},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-18_france-riots-2023/national_waves.csv}},
    note = {Dataset}
}
```

## riot-towns-census.csv

**French towns of 10,000 people or more: poverty, immigrant share and 2023 riots.** The towns behind the grid chart: each with its poverty rate, share of immigrants, whether it has a priority neighbourhood and whether it is on our riot list.

Coverage: 993 communes. Last updated: 2026-10-21.

| Column | Description |
|---|---|
| `insee_code` | INSEE commune code (2023 geography). |
| `commune` | Commune name. |
| `departement` | Département code. |
| `population` | Legal population, 2020 census. |
| `poverty_rate` | Share of people below 60% of median income, %, Filosofi 2021. |
| `immigrant_share` | Share of residents who are immigrants, %, census 2020. |
| `has_priority_neighbourhood` | 1 if the commune contains a priority neighbourhood (QPV, 2015 list). |
| `poverty_third, immigrant_third` | Third of the 993 towns on each measure. |
| `on_riot_list` | 1 if the town is on our 2023 riot list. |

Sources:

- INSEE: https://www.insee.fr/ (Licence Ouverte 2.0)
- ANCT priority neighbourhoods (data.gouv.fr): https://www.data.gouv.fr/datasets/5a561801c751df42d7fca9b6 (Licence Ouverte 2.0)

Notes:

- About places, not people.
- Twenty overseas towns without a published poverty rate are left out.

How to cite:

Signum Average (2026) - "French towns of 10,000 people or more: poverty, immigrant share and 2023 riots" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-18_france-riots-2023/towns_10000.csv

```bibtex
@misc{signumaverage-riot-towns-census,
    author = {{Signum Average}},
    title = {French towns of 10,000 people or more: poverty, immigrant share and 2023 riots},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-18_france-riots-2023/towns_10000.csv}},
    note = {Dataset}
}
```

## unrest-2026.csv

**France's protest movement of autumn 2026: Interior Ministry figures by protest day.** Marchers, arrests, police and gendarmes injured, fire call-outs, shops damaged and police deployed on each national protest day, with the source of each figure. The figures for 5 and 7 November are provisional.

Coverage: Five national protest days, 17 October-7 November 2026. Last updated: 2026-11-11.

| Column | Description |
|---|---|
| `date` | Protest day. |
| `day_index` | Day of the movement, counting 17 October as day 1. |
| `day` | Day of the week and kind of day. |
| `marchers_ministry, marchers_organisers` | Marchers counted by the Interior Ministry and claimed by the organisers. |
| `arrests` | Arrests (interpellations) across France. |
| `arrests_status` | final, or provisional with the hour of the count. |
| `police_injured` | Police and gendarmes injured (blank where not published). |
| `fire_callouts` | Call-outs to fires (the ministry does not count vehicles burned on protest days). |
| `shops_damaged` | Shops and businesses damaged or looted, where published. |
| `police_deployed` | Police and gendarmes deployed, where published. |
| `source` | Source of the figures and earlier counts. |

Sources:

- Interior Ministry press releases (interieur.gouv.fr): https://www.interieur.gouv.fr/actualites/communiques-de-presse (Figures cited)

Notes:

- Counts were revised after each day: 17 October's arrests went from 1,200 to 1,800, 2,397 and finally 2,628.

How to cite:

Signum Average (2026) - "France's protest movement of autumn 2026: Interior Ministry figures by protest day" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-18_france-riots-2023/unrest_2026.csv

```bibtex
@misc{signumaverage-unrest-2026,
    author = {{Signum Average}},
    title = {France's protest movement of autumn 2026: Interior Ministry figures by protest day},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-18_france-riots-2023/unrest_2026.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
