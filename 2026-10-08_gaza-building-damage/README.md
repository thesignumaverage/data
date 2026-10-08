# Data for https://website.thesignumaverage.workers.dev/articles/gaza-building-damage/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## unosat_damage_timeseries.csv

**Buildings destroyed and damaged in Gaza, six satellite assessments.** Structures destroyed, severely, moderately and possibly damaged in the Gaza Strip at each of six UNOSAT comprehensive damage assessments, with the share of all structures affected and the estimated damaged housing units, as UNOSAT reported them.

Coverage: 7 Nov 2023 to 16 Jun 2026. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `assessment_date` | Date of the satellite imagery (YYYY-MM-DD). |
| `destroyed` | Structures classed as destroyed. |
| `severely_damaged` | Structures classed as severely damaged. |
| `moderately_damaged` | Structures classed as moderately damaged; empty where not reported. |
| `possibly_damaged` | Structures classed as possibly damaged; empty where not reported. |
| `total_affected` | All affected structures, the sum of the four classes. |
| `pct_of_prewar_structures` | Share of all structures in the Gaza Strip affected, as a fraction, as UNOSAT reported it. |
| `housing_units_damaged` | Estimated damaged housing units, where reported (the June 2026 figure is from a joint UN, EU and World Bank assessment). |
| `source_file` | The UNOSAT document in the study's raw-data folder, where downloaded. |
| `source_url` | Where the figures were published. |

Sources:

- UNOSAT Gaza Strip comprehensive damage assessments: https://unosat.org/products/3984 (UN public reports)

Notes:

- The implied pre-war total of structures drifts across reports (about 207,000 in the first, 245,000 to 248,000 later); use the reported percentages, not one denominator.
- Counts are cumulative structures, not strikes: a building destroyed by ground combat or demolition counts the same as one destroyed from the air.

How to cite:

Signum Average (2026) - "Buildings destroyed and damaged in Gaza, six satellite assessments" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/unosat_damage_timeseries.csv

```bibtex
@misc{signumaverage-unosat-damage-timeseries,
    author = {{Signum Average}},
    title = {Buildings destroyed and damaged in Gaza, six satellite assessments},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/unosat_damage_timeseries.csv}},
    note = {Dataset}
}
```

## idf_claimed_figures.csv

**The Israeli army's own figures: targets struck, operatives killed, tunnel shafts, depots.** Every cumulative or period figure the Israel Defense Forces gave for the Gaza war that this study uses, with the date, the outlet that reported it and a note on what it does and does not say.

Coverage: Feb 2024 to Dec 2025. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `statement_date` | Date of the statement or report. |
| `months_since_2023-10-07` | Months from the start of the war, used to align with the satellite series. |
| `figure` | What is counted, such as targets_struck_cumulative or operatives_killed_cumulative. |
| `value` | The figure as stated. |
| `scope` | Gaza, or the operation or year the figure covers. |
| `source` | Who reported it. |
| `source_url` | Link to the report. |
| `notes` | The wording used and any caveat. |

Sources:

- IDF figures as reported by Breaking Defense, Times of Israel and Ynet: https://www.timesofisrael.com/a-year-of-war-idf-data-shows-726-troops-killed-over-26000-rockets-fired-at-israel/ (Figures cited from press reports)

Notes:

- The army does not define a 'target'. It can be a person, a vehicle, a launcher in open ground or a tunnel route under several buildings.
- Targets struck in October to December 2024 are unreported.

How to cite:

Signum Average (2026) - "The Israeli army's own figures: targets struck, operatives killed, tunnel shafts, depots" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/idf_claimed_figures.csv

```bibtex
@misc{signumaverage-idf-claimed-figures,
    author = {{Signum Average}},
    title = {The Israeli army's own figures: targets struck, operatives killed, tunnel shafts, depots},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/idf_claimed_figures.csv}},
    note = {Dataset}
}
```

## hamas_fighter_estimates.csv

**Estimates of Hamas's fighting strength, with their sourcing.** Every estimate of the number of Hamas fighters found with any sourcing, kept apart by type (government statement, intelligence estimate reported by the press, analyst commentary) with a note on reliability. None is independently verifiable.

Coverage: Oct 2023 to Jan 2025. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `as_of_date` | Date the estimate refers to or was made. |
| `estimate_low` | Lower end of a range, where given. |
| `estimate_high` | Upper end of a range, where given. |
| `point_estimate` | A single figure, where given. |
| `source_type` | government_statement, analysis, us_intelligence_via_press or press_report. |
| `source_name` | Who said it. |
| `primary_or_secondary` | Whether a primary document was located. |
| `source_url` | Link. |
| `reliability_notes` | What the figure does and does not measure. |

Sources:

- Reuters, ACLED, Jerusalem Post, FDD, as linked in each row (Figures cited from public reports)

Notes:

- The '30,000 pre-war fighters' figure often quoted is analyst commentary attached to a ministerial casualty statement, not a count.

How to cite:

Signum Average (2026) - "Estimates of Hamas's fighting strength, with their sourcing" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/hamas_fighter_estimates.csv

```bibtex
@misc{signumaverage-hamas-fighter-estimates,
    author = {{Signum Average}},
    title = {Estimates of Hamas's fighting strength, with their sourcing},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/hamas_fighter_estimates.csv}},
    note = {Dataset}
}
```

## fighter_presence_bounds.csv

**The most that a Hamas fighter in every building could explain, by date and fighter count.** For each satellite assessment date and each fighter count from 15,000 to 40,000: the ceiling on buildings explained by fighter presence if every fighter occupied a different building (Bound 1), its share of the destroyed count, and the number of buildings per fighter at which a cumulative-mobility bound would stop constraining anything (Bound 2).

Coverage: Nov 2023 to Jun 2026. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `assessment_date` | UNOSAT assessment date. |
| `destroyed` | Structures destroyed at that date. |
| `total_affected` | Structures destroyed or damaged at that date. |
| `fighter_estimate` | Fighters assumed. |
| `bound1_ceiling` | Buildings a fighter could occupy at once: equal to the fighter count. |
| `bound1_share_of_destroyed` | bound1_ceiling divided by destroyed, as a fraction (above 1 where the count exceeds the destruction, early in the war). |
| `bound2_min_k_to_cover_destroyed` | Smallest number of buildings per fighter over the war at which fighters times k reaches the destroyed count. |
| `bound2_status_at_k5` | Whether the cumulative bound still constrains at five buildings per fighter. |

Sources:

- UNOSAT Gaza Strip comprehensive damage assessments: https://unosat.org/products/3984 (UN public reports)
- Signum Average calculations (CC BY 4.0)

Notes:

- A ceiling on one explanation, not an error rate: buildings outside it may have been lawful targets for other reasons, or destroyed by ground combat or demolition.

How to cite:

Signum Average (2026) - "The most that a Hamas fighter in every building could explain, by date and fighter count" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/fighter_presence_bounds.csv

```bibtex
@misc{signumaverage-fighter-presence-bounds,
    author = {{Signum Average}},
    title = {The most that a Hamas fighter in every building could explain, by date and fighter count},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/fighter_presence_bounds.csv}},
    note = {Dataset}
}
```

## casualty_demographics.csv

**Who the dead are: children, women and men among Gaza's reported dead, against the population.** Shares of the reported dead who are children, women and (by subtraction) men, set against approximate pre-war population shares.

Coverage: To 7 Oct 2026. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `category` | children (under 18), women (adult), or men implied by subtraction. |
| `count` | Reported dead in the category. |
| `share_of_reported_dead` | count divided by all reported dead, as a fraction. |
| `approx_population_baseline_share` | Approximate share of the pre-war population: the 0 to 14 share for children (understated), half of adults for each sex. |
| `caveat` | What the row does not measure. |

Sources:

- Tech for Palestine, summary of Gaza Ministry of Health casualty reports: https://data.techforpalestine.org/docs/summary/ (Open data, as published)
- CIA World Factbook, Gaza Strip age structure (2017): https://www.cia.gov/the-world-factbook/countries/gaza-strip/ (Public domain)

Notes:

- A higher share of men among the dead is consistent with combatant deaths and with men's greater exposure; it does not identify fighters.

How to cite:

Signum Average (2026) - "Who the dead are: children, women and men among Gaza's reported dead, against the population" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/casualty_demographics.csv

```bibtex
@misc{signumaverage-casualty-demographics,
    author = {{Signum Average}},
    title = {Who the dead are: children, women and men among Gaza's reported dead, against the population},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/casualty_demographics.csv}},
    note = {Dataset}
}
```

## concentration_simulation.csv

**Spatial check: buildings a moving fighter force could touch, by how much of Gaza it occupies.** A grid of 245,025 cells stands in for Gaza's buildings. Fighters placed at random in a share of the grid move each month; every occupied cell is struck at once. The count of distinct cells ever struck is set against the real destroyed count at each UNOSAT date, for each combination of fighter count, share of Gaza, movement pattern, move chance and blast radius.

Coverage: 32 simulated months. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `area_fraction` | Share of the grid in which fighters are placed and move: 1.0, 0.25 or 0.05. |
| `fighters` | Fighters: 20,000, 30,000 or 40,000. |
| `movement_mode` | global (anywhere in the area each move) or local (within ten cells). |
| `p_move` | Chance a fighter moves in a month. |
| `r_blast` | 0: only the struck cell is destroyed; 1: its four neighbours too. |
| `assessment_date` | UNOSAT date compared with. |
| `sim_destroyed` | Distinct cells struck by that date. |
| `real_destroyed` | UNOSAT's destroyed count at that date. |
| `sim_share_of_real` | sim_destroyed divided by real_destroyed. |

Sources:

- UNOSAT Gaza Strip comprehensive damage assessments: https://unosat.org/products/3984 (UN public reports)
- Signum Average calculations (CC BY 4.0)

Notes:

- Illustrative: a square grid, no real geography, perfect and instant detection. It can rule a mechanism out, not in.

How to cite:

Signum Average (2026) - "Spatial check: buildings a moving fighter force could touch, by how much of Gaza it occupies" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/concentration_simulation.csv

```bibtex
@misc{signumaverage-concentration-simulation,
    author = {{Signum Average}},
    title = {Spatial check: buildings a moving fighter force could touch, by how much of Gaza it occupies},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/concentration_simulation.csv}},
    note = {Dataset}
}
```

## attrition_scenarios.csv

**Chasing fighters who die: three named scenarios on the real monthly destruction.** Each month the real number of buildings destroyed is handed out, found fighters first; a struck fighter dies with some chance; survivors move and recruits arrive. Three scenarios: an army that finds and kills fast with no recruits; middle assumptions; a slow army against a force spread over all Gaza.

Coverage: Nov 2023 to Jun 2026. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `scenario` | worst, reasonable or best, for the hypothesis that fighter presence explains the destruction. |
| `month` | Months since 7 October 2023. |
| `date` | The UNOSAT date the row is compared with. |
| `sim_destroyed` | Distinct buildings struck for a fighter by that date. |
| `real_destroyed` | UNOSAT's destroyed count. |
| `n_alive_fighters` | Fighters alive at that date. |
| `cumulative_fighter_deaths` | Fighters killed by strikes to that date. |
| `sim_share_of_real` | sim_destroyed divided by real_destroyed. |

Sources:

- UNOSAT Gaza Strip comprehensive damage assessments: https://unosat.org/products/3984 (UN public reports)
- Signum Average calculations (CC BY 4.0)

Notes:

- The 'worst' scenario is a bound, not an estimate: it kills every fighter by month nine, which no report supports.
- Parameters per scenario are listed in the study's MODEL_SPEC.md (v3, v3.1).

How to cite:

Signum Average (2026) - "Chasing fighters who die: three named scenarios on the real monthly destruction" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/attrition_scenarios.csv

```bibtex
@misc{signumaverage-attrition-scenarios,
    author = {{Signum Average}},
    title = {Chasing fighters who die: three named scenarios on the real monthly destruction},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/attrition_scenarios.csv}},
    note = {Dataset}
}
```

## abc_calibration_draws.csv

**Calibration of the chasing model: 3,000 random parameter draws and the 150 that fit.** Each row is one draw of the five unknowns (initial fighters, recruits a month, share of Gaza, chance of being found, lethality) from wide priors, the summary statistics of one simulation run, the distance from three real-data bands and the share of destroyed buildings the run explains. Rows with distance 0 are the kept posterior sample.

Coverage: 32 simulated months. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `draw` | Draw number. |
| `f0` | Initial fighters. |
| `recruit_per_month` | Recruits a month. |
| `area_fraction` | Share of Gaza occupied. |
| `detect_p` | Chance a living fighter is found in a month. |
| `lethality` | Chance a struck fighter dies. |
| `alive_month12` | Fighters alive at month 12 (target: 20,000 to 23,000). |
| `alive_month15_ratio_f0` | Fighters alive at month 15 over f0 (target: 0.7 to 1.3). |
| `cum_fighter_deaths_month32` | Fighters killed by month 32 (target: 6,000 to 25,000). |
| `distance` | Normalised distance outside the three bands; 0 means all three satisfied. |
| `explained_share_2025-10-11` | Share of buildings destroyed by 11 Oct 2025 the run explains. |
| `explained_share_2026-06-16` | The same at 16 Jun 2026. |

Sources:

- UNOSAT Gaza Strip comprehensive damage assessments: https://unosat.org/products/3984 (UN public reports)
- Signum Average calculations (CC BY 4.0)
- ACLED estimate of fighters remaining (Oct 2024); Reuters on US intelligence (Jan 2025); Gaza Ministry of Health lists via Tech for Palestine (Figures cited from public reports)

Notes:

- One stochastic run per draw.
- The share of Gaza is unconstrained by the targets, so the top of the explained range depends on its prior.

How to cite:

Signum Average (2026) - "Calibration of the chasing model: 3,000 random parameter draws and the 150 that fit" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/abc_calibration_draws.csv

```bibtex
@misc{signumaverage-abc-calibration-draws,
    author = {{Signum Average}},
    title = {Calibration of the chasing model: 3,000 random parameter draws and the 150 that fit},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/abc_calibration_draws.csv}},
    note = {Dataset}
}
```

## channel_accounting.csv

**The army's count of targets against the satellite count of destroyed buildings, by date.** Cumulative targets the Israeli army says it struck in Gaza at each statement date, the UNOSAT destroyed count interpolated to that date, and the ratio. The unreported last quarter of 2024 is given as a floor (none) and a proxy (6,400, from the tempo of violence).

Coverage: Feb 2024 to Dec 2025. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `month` | Months since 7 October 2023. |
| `idf_targets_cumulative` | Targets struck, cumulative. |
| `unosat_destroyed_interp` | Destroyed structures, interpolated linearly between UNOSAT dates. |
| `targets_per_destroyed` | The ratio. |
| `note` | reported, or how the last quarter of 2024 was filled. |

Sources:

- IDF figures as reported by Breaking Defense, Times of Israel and Ynet: https://www.timesofisrael.com/a-year-of-war-idf-data-shows-726-troops-killed-over-26000-rockets-fired-at-israel/ (Figures cited from press reports)
- UNOSAT Gaza Strip comprehensive damage assessments: https://unosat.org/products/3984 (UN public reports)
- Signum Average calculations (CC BY 4.0)

Notes:

- One target is taken as one distinct building; the army does not define the term.

How to cite:

Signum Average (2026) - "The army's count of targets against the satellite count of destroyed buildings, by date" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/channel_accounting.csv

```bibtex
@misc{signumaverage-channel-accounting,
    author = {{Signum Average}},
    title = {The army's count of targets against the satellite count of destroyed buildings, by date},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/channel_accounting.csv}},
    note = {Dataset}
}
```

## periods.csv

**The war's tempo by period: targets, destroyed buildings, events and deaths a month.** For the war's first year and the fifteen months after it: targets the army reported, buildings destroyed, and ACLED's counts of political-violence events and fatalities in the Gaza Strip, as totals and per month.

Coverage: Oct 2023 to Dec 2025. Last updated: 2026-10-08.

| Column | Description |
|---|---|
| `period` | The period. |
| `months` | Its length in months. |
| `idf_targets` | Targets reported in the period (the last quarter of 2024 at the proxy). |
| `destroyed` | Buildings newly destroyed in the period, from UNOSAT interpolated. |
| `acled_events` | ACLED political-violence events in the Gaza Strip. |
| `acled_fatalities` | ACLED reported fatalities, all people. |
| `idf_targets_per_month` | Per month. |
| `destroyed_per_month` | Per month. |
| `acled_events_per_month` | Per month. |
| `acled_fatalities_per_month` | Per month. |

Sources:

- IDF figures as reported by Breaking Defense, Times of Israel and Ynet: https://www.timesofisrael.com/a-year-of-war-idf-data-shows-726-troops-killed-over-26000-rockets-fired-at-israel/ (Figures cited from press reports)
- UNOSAT Gaza Strip comprehensive damage assessments: https://unosat.org/products/3984 (UN public reports)
- ACLED, Palestine conflict events by month (HDX extract): https://data.humdata.org/dataset/palestine-acled-conflict-data (ACLED terms of use; attribution required; the monthly file itself is not redistributed here)
- Signum Average calculations (CC BY 4.0)

Notes:

- ACLED's fatality counts come from press reports and undercount in intense periods.

How to cite:

Signum Average (2026) - "The war's tempo by period: targets, destroyed buildings, events and deaths a month" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/periods.csv

```bibtex
@misc{signumaverage-periods,
    author = {{Signum Average}},
    title = {The war's tempo by period: targets, destroyed buildings, events and deaths a month},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-08_gaza-building-damage/periods.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
