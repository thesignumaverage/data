# Data for https://website.thesignumaverage.workers.dev/articles/america-in-2075/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## probability_us.csv

**Share of Americans counted as white to 2075, with ranges.** Percentiles of the white share of the US population across 4,000 simulated futures, under three definitions of white.

Coverage: United States; 2025-2075, every five years; three definitions of white. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `definition` | white_alone_not_hispanic; white_alone_or_mixed (adds part-white non-Hispanic people); white_incl_hispanic_white (adds Hispanics classed as white in the 2025 estimates). |
| `year` | Year (1 July). |
| `p2.5 ... p97.5` | Percentiles of the share, %. p50 is the median; p10 to p90 is the 80% range; p2.5 to p97.5 the 95% range. |

Sources:

- US Census Bureau, population estimates (intercensal 2000-2010, Vintage 2020, Vintage 2025): https://www.census.gov/programs-surveys/popest.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Ranges assume the next 50 years vary as 2010-2025 did, stretched by 8% after a test against the method's errors in 1995-2020. A harsher reading of the tests gives much wider ranges (probability_us_harsh.csv): a 76% chance, not 92%, that the non-Hispanic white share is below half by 2050.
- The method ran fast in past tests: the white share fell more slowly than projected in most states.
- They leave out changes in how people describe themselves and in official categories.

How to cite:

Signum Average (2026) - "Share of Americans counted as white to 2075, with ranges" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/probability_us.csv

```bibtex
@misc{signumaverage-probability-us,
    author = {{Signum Average}},
    title = {Share of Americans counted as white to 2075, with ranges},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/probability_us.csv}},
    note = {Dataset}
}
```

## probability_states.csv

**Chance that each US state's white share falls below half.** For each state: the non-Hispanic white share in 2050 and 2075 with 80% ranges, the chance it is below half by 2050 and by 2075, and the likely year, from 4,000 simulated futures.

Coverage: 50 states, DC and the United States. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `state` | State, District of Columbia, or United States. |
| `white_share_2025` | Non-Hispanic white alone, % of population in 2025 (Census Bureau estimate). |
| `share_2050_median / _low / _high` | Share in 2050: median and the 80% range (10th and 90th percentiles), %. |
| `share_2075_median / _low / _high` | The same for 2075. |
| `prob_below_half_by_2050 / _by_2075` | Share of simulated futures in which the share has fallen below 50% by that year (1 = all). |
| `below_half_median / _early / _late` | Median, 10th and 90th percentile of the year the share falls below 50%; 'before 2025' or 'not by 2075'. |
| `alone_or_mixed_prob_below_half_by_2075` | The chance, counting part-white non-Hispanic people as white. |
| `alone_or_mixed_below_half_median` | Median year on that count. |

Sources:

- US Census Bureau, population estimates (intercensal 2000-2010, Vintage 2020, Vintage 2025): https://www.census.gov/programs-surveys/popest.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Ranges assume the next 50 years vary as 2010-2025 did, stretched by 8% after a test against the method's errors in 1995-2020. A harsher reading of the tests gives much wider ranges (probability_us_harsh.csv): a 76% chance, not 92%, that the non-Hispanic white share is below half by 2050.
- The method ran fast in past tests: the white share fell more slowly than projected in most states.
- They leave out changes in how people describe themselves and in official categories.
- Ranges for small states are very wide.

How to cite:

Signum Average (2026) - "Chance that each US state's white share falls below half" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/probability_states.csv

```bibtex
@misc{signumaverage-probability-states,
    author = {{Signum Average}},
    title = {Chance that each US state's white share falls below half},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/probability_states.csv}},
    note = {Dataset}
}
```

## projection_by_state.csv

**Population by group for every US state, projected to 2075 (scenarios).** A projection of each state's population by race and Hispanic origin under low, central and high migration, and a central scenario in which birth rates converge. 2025 is the Census Bureau's estimate; later years are scenarios without probabilities. For odds, see probability_us.csv and probability_states.csv.

Coverage: 50 states, DC and the United States; 2025-2075, every five years; four scenarios. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `scenario` | low (cohort change as in 2015-20), high (as in 2020-25), central (their mean), central_fertility_converges. |
| `year` | Year (1 July). |
| `state` | State, District of Columbia, or United States. |
| `population` | Total population. |
| `share_white` | Non-Hispanic white alone, % of population. |
| `share_black` | Non-Hispanic Black alone, %. |
| `share_native` | Non-Hispanic American Indian or Alaska Native alone, %. |
| `share_asian_pacific` | Non-Hispanic Asian or Pacific Islander alone, %. |
| `share_two_or_more` | Non-Hispanic, two or more races, %. |
| `share_hispanic` | Hispanic of any race, %. |
| `white_alone_or_mixed` | Non-Hispanic white alone or part-white, %. |
| `white_incl_hispanic_white` | White alone or part-white including Hispanics classed as white in the 2025 estimates, %. |

Sources:

- US Census Bureau, population estimates (intercensal 2000-2010, Vintage 2020, Vintage 2025): https://www.census.gov/programs-surveys/popest.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Scenarios carry the patterns of 2015-25 forward; single-state figures late in the period are very uncertain.
- The broad definition uses the Bureau's race classification of Hispanics, which counts far more of them as white than they report themselves.

How to cite:

Signum Average (2026) - "Population by group for every US state, projected to 2075 (scenarios)" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/projection_by_state.csv

```bibtex
@misc{signumaverage-projection-by-state,
    author = {{Signum Average}},
    title = {Population by group for every US state, projected to 2075 (scenarios)},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/projection_by_state.csv}},
    note = {Dataset}
}
```

## crossing_years.csv

**Year each US state's white share falls below half.** The year the white share of each state's population falls below 50% in each scenario, under three definitions of white. Scenarios carry no probabilities; see probability_states.csv for odds.

Coverage: 50 states, DC and the United States; three scenarios. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `state` | State, District of Columbia, or United States. |
| `white_share_2025` | Non-Hispanic white alone, % of population in 2025. |
| `white_share_2075_low / _central / _high` | The same in 2075 under each scenario. |
| `below_half_low / _central / _high` | Year the non-Hispanic white alone share falls below 50%, 'before 2025' or 'not by 2075'. |
| `alone_or_mixed_below_half_...` | The same counting part-white non-Hispanic people as white. |
| `broad_below_half_...` | The same also counting Hispanics classed as white. |

Sources:

- US Census Bureau, population estimates (intercensal 2000-2010, Vintage 2020, Vintage 2025): https://www.census.gov/programs-surveys/popest.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Years between the five-year projection points are interpolated in a straight line.

How to cite:

Signum Average (2026) - "Year each US state's white share falls below half" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/crossing_years.csv

```bibtex
@misc{signumaverage-crossing-years,
    author = {{Signum Average}},
    title = {Year each US state's white share falls below half},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/crossing_years.csv}},
    note = {Dataset}
}
```

## backtest_scores.csv

**How well the projection method would have called 2015 and 2020.** Errors of the projection method when started in 2010 and in 2015 and compared with what happened, alongside two naive guesses.

Coverage: Two tests, four versions of the method and two naive guesses. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `test` | test1: started in 2010; test2: started in 2015. |
| `launch` | Starting year. |
| `year` | Year projected. |
| `model` | A or B: ratios only, or ratios and differences; 1 or 2: how mixed-race births are counted. B2 is the published version. Or a naive guess. |
| `mae_white_pp` | Mean absolute error across states in the non-Hispanic white share, percentage points. |
| `mae_all_groups_pp` | The same averaged over all six groups. |
| `worst_state_white_pp` | Largest state error in the white share, percentage points. |
| `national_white_error_pp` | Projected minus actual national white share, percentage points. |
| `total_pop_error_pct` | Projected against actual total population, %. |

Sources:

- US Census Bureau, population estimates (intercensal 2000-2010, Vintage 2020, Vintage 2025): https://www.census.gov/programs-surveys/popest.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- The test covers ten years; the projection runs for fifty.

How to cite:

Signum Average (2026) - "How well the projection method would have called 2015 and 2020" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/backtest_scores.csv

```bibtex
@misc{signumaverage-backtest-scores,
    author = {{Signum Average}},
    title = {How well the projection method would have called 2015 and 2020},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/backtest_scores.csv}},
    note = {Dataset}
}
```

## arrivals_by_state.csv

**Who moves to each US state from abroad.** People whose home a year earlier was abroad, by group, for each state, with the foreign-born population by group and net international migration for scale.

Coverage: 50 states, DC and the United States; yearly average 2021-2024; foreign-born residents in 2024. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `state` | State, District of Columbia, or United States. |
| `arrivals_per_year` | People aged one and over who lived abroad a year earlier, yearly average 2021-24. |
| `white` | Of whom white alone, not Hispanic. |
| `white_margin` | 90% margin of error of that four-year average. |
| `hispanic` | Of whom Hispanic, any race. |
| `other` | Everyone else (arrivals less the two groups above). |
| `asian_alone / black_alone` | Asian alone and Black alone, including the few who are Hispanic; blank where the survey suppresses a year. |
| `white_share_of_arrivals / hispanic_share_of_arrivals` | % of arrivals. |
| `arrivals_per_1000_residents` | Arrivals a year per 1,000 residents in 2024. |
| `white_arrivals_per_1000_white_residents` | White arrivals a year per 1,000 white residents. |
| `white_share_of_residents` | Non-Hispanic white alone, % of residents, 2024 survey. |
| `foreign_born_2024` | Foreign-born residents, 2024. |
| `foreign_born_share_of_residents` | % of residents. |
| `white_share_of_foreign_born / hispanic_share_of_foreign_born` | % of foreign-born residents. |
| `foreign_born_share_of_white_residents` | % of non-Hispanic white residents born abroad. |
| `net_international_migration_per_year_2021_25` | Net international migration, yearly average of the years to mid-2021 to mid-2025, from the population estimates (no race detail). |

Sources:

- US Census Bureau, American Community Survey one-year estimates, 2021-2024 (tables B07003, B07004A-I, B05003): https://www.census.gov/programs-surveys/acs (Public domain)
- US Census Bureau, population estimates (intercensal 2000-2010, Vintage 2020, Vintage 2025): https://www.census.gov/programs-surveys/popest.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Gross arrivals, including Americans returning from abroad; not net migration. The survey misses some recent migrants.
- Figures for small states have wide margins even after pooling four years.

How to cite:

Signum Average (2026) - "Who moves to each US state from abroad" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/arrivals_by_state.csv

```bibtex
@misc{signumaverage-arrivals-by-state,
    author = {{Signum Average}},
    title = {Who moves to each US state from abroad},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/arrivals_by_state.csv}},
    note = {Dataset}
}
```

## arrivals_us.csv

**Who moves to the United States from abroad, by year.** People whose home a year earlier was abroad, by group and year.

Coverage: United States; 2021-2024. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `year` | Survey year. |
| `arrivals` | People aged one and over who lived abroad a year earlier. |
| `white` | White alone, not Hispanic. |
| `hispanic` | Hispanic, any race. |
| `other` | Everyone else. |
| `asian_alone / black_alone` | Asian alone and Black alone, including the few who are Hispanic. |
| `..._share` | Each as % of arrivals. |

Sources:

- US Census Bureau, American Community Survey one-year estimates, 2021-2024 (tables B07003, B07004A-I, B05003): https://www.census.gov/programs-surveys/acs (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Gross arrivals, including Americans returning from abroad; not net migration. The survey misses some recent migrants.

How to cite:

Signum Average (2026) - "Who moves to the United States from abroad, by year" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/arrivals_us.csv

```bibtex
@misc{signumaverage-arrivals-us,
    author = {{Signum Average}},
    title = {Who moves to the United States from abroad, by year},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/arrivals_us.csv}},
    note = {Dataset}
}
```

## births_needed_by_state.csv

**Children per white woman needed to hold each state's white population steady.** A what-if on the central projection. Only white births per woman change, from 2025 on; deaths, immigration, moves between states and mixed-race births continue as in 2015-2025. Each state row is solved on its own (what that state's white women would need for that state's white population, or share, in 2075 to equal 2025's). The United States row applies one factor in every state and holds the national total.

Coverage: 50 states, DC and the United States. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `state` | State, District of Columbia, or United States. |
| `white_population_2025` | Non-Hispanic white alone, 2025. |
| `white_share_2025` | % of the state's population. |
| `white_population_2075_no_change` | The same in 2075 in the central projection. |
| `white_population_change_pct` | Change 2025-2075, %. |
| `white_share_2075_no_change` | Share in 2075 in the central projection, %. |
| `children_per_woman_now` | Total fertility rate in 2025 counting children classed as white alone and not Hispanic: the rate that, with the age pattern of the Census Bureau's 2023 projection, yields the state's white infants from its white women by single year of age. |
| `factor_to_hold_population` | Factor on white births per woman that holds the white population of 2075 at the 2025 level (below 1: it grows anyway). |
| `children_to_hold_population` | That factor times children_per_woman_now. |
| `factor_to_hold_share / children_to_hold_share` | The same for holding the white share of the state's population. |

Sources:

- US Census Bureau, population estimates (intercensal 2000-2010, Vintage 2020, Vintage 2025): https://www.census.gov/programs-surveys/popest.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- State figures do not add up to the national one: moves between states cancel nationally, but each state on its own must replace those who leave.
- The state figures carry the moves between states of 2015-2025 forward for fifty years; they are what that pattern implies, not forecasts.
- Children per woman counts only children classed as white alone and not Hispanic, so it is below the official rate for white mothers, more so where mixed families are common.
- Births are one lever of several; immigration, mortality and how people are counted are not solved for.

How to cite:

Signum Average (2026) - "Children per white woman needed to hold each state's white population steady" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/births_needed_by_state.csv

```bibtex
@misc{signumaverage-births-needed-by-state,
    author = {{Signum Average}},
    title = {Children per white woman needed to hold each state's white population steady},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/births_needed_by_state.csv}},
    note = {Dataset}
}
```

## no_immigration_us.csv

**The white share of Americans with and without immigration, to 2075.** A national projection in three groups in which net migration from abroad after 2025 continues as in 2015-2025, halves, or stops.

Coverage: United States; 2025-2075, every five years; three scenarios. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `scenario` | as_2015_25, half, or none (zero net migration from abroad after 2025). |
| `year` | Year (1 July). |
| `population` | Total population. |
| `white_population` | Non-Hispanic white alone. |
| `share_white / share_hispanic / share_other` | % of population: non-Hispanic white alone, Hispanic, everyone else. |

Sources:

- US Census Bureau, population estimates (Vintage 2020, Vintage 2025) and components of change by race and Hispanic origin: https://www.census.gov/programs-surveys/popest.html (Public domain)
- US Census Bureau, 2023 National Population Projections (age and sex pattern of net migration): https://www.census.gov/programs-surveys/popproj.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- 'None' means zero net migration, not zero arrivals; the Census Bureau's own no-immigration scenario assumes no arrivals while people keep leaving.
- A simpler model than the state projection (national, three groups); with migration left in it puts the 2075 white share about one point lower.
- Scenarios, not forecasts with probabilities.

How to cite:

Signum Average (2026) - "The white share of Americans with and without immigration, to 2075" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/no_immigration_us.csv

```bibtex
@misc{signumaverage-no-immigration-us,
    author = {{Signum Average}},
    title = {The white share of Americans with and without immigration, to 2075},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/no_immigration_us.csv}},
    note = {Dataset}
}
```

## components_by_group_us.csv

**Births, deaths and net migration from abroad by group, United States.** The Census Bureau's components of population change, regrouped as non-Hispanic white, Hispanic and everyone else.

Coverage: United States; April 2010 to July 2019, April 2020 to July 2025, and the year to July 2025. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `period` | Period covered. |
| `group` | white (white alone, not Hispanic), hispanic (any race), other (everyone else). |
| `births / deaths` | Number in the period. |
| `natural_change` | Births less deaths. |
| `net_migration` | Net migration from abroad. |
| `share_of_net_migration` | The group's % of all net migration from abroad in the period. |

Sources:

- US Census Bureau, population estimates (Vintage 2020, Vintage 2025) and components of change by race and Hispanic origin: https://www.census.gov/programs-surveys/popest.html (Public domain)

Notes:

- The two periods come from different vintages of estimates with different race bases.

How to cite:

Signum Average (2026) - "Births, deaths and net migration from abroad by group, United States" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/components_by_group_us.csv

```bibtex
@misc{signumaverage-components-by-group-us,
    author = {{Signum Average}},
    title = {Births, deaths and net migration from abroad by group, United States},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/components_by_group_us.csv}},
    note = {Dataset}
}
```

## long_backtest_scores.csv

**The projection method tested on 1990-2020.** Errors of the projection method and two naive guesses when started in each year and compared with what happened, every five years to 2020.

Coverage: Four start years (1995, 2000, 2005, 2010), each run to 2020; three models. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `launch` | Start year. |
| `year` | Year projected. |
| `years_ahead` | Years after the start. |
| `model` | projection, or a naive guess (shares unchanged; trend continues). |
| `mae_white_pp` | Mean absolute error across 51 states in the non-Hispanic white share, percentage points. |
| `worst_state_white_pp` | Largest state error, percentage points. |
| `national_white_error_pp` | Projected less actual national white share, percentage points. |

Sources:

- National Center for Health Statistics, bridged-race population estimates, 1990-2020: https://www.cdc.gov/nchs/nvss/bridged_race.htm (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Uses bridged-race categories (four races by Hispanic origin, no two-or-more group), not the categories of the published projection: a test of the method.

How to cite:

Signum Average (2026) - "The projection method tested on 1990-2020" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/long_backtest_scores.csv

```bibtex
@misc{signumaverage-long-backtest-scores,
    author = {{Signum Average}},
    title = {The projection method tested on 1990-2020},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/long_backtest_scores.csv}},
    note = {Dataset}
}
```

## long_backtest_ranges.csv

**Test 1 of the ranges: an odds model fitted to the 1990s.** Whether ranges from an odds model fitted to 1990-2000 only held what happened ten and twenty years later.

Coverage: Launched in 2000; checked in 2010 and 2020. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `year / years_ahead` | Year checked and years after the 2000 launch. |
| `range` | 80% or 95%. |
| `states_inside / of` | States whose actual white share fell inside the range. |
| `national_inside` | Whether the national share did. |
| `median_width_pp` | Typical width of a state's range, percentage points. |
| `national_actual / _median / _low / _high` | Actual national white share, and the model's median and range, %. |
| `states_above_range / states_below_range` | States whose actual share was above or below the range. |
| `stretch_needed` | Factor by which every state's range would have had to be stretched for the right share of states to fall inside. |

Sources:

- National Center for Health Statistics, bridged-race population estimates, 1990-2020: https://www.cdc.gov/nchs/nvss/bridged_race.htm (Public domain)
- US Census Bureau, state population estimates by age, sex, race and Hispanic origin, 1990-1999: https://www.census.gov/programs-surveys/popest.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Uses bridged-race categories (four races by Hispanic origin, no two-or-more group), not the categories of the published projection: a test of the method.
- This model was too confident; its stretch factors give the 'harsh reading' in probability_us_harsh.csv.

How to cite:

Signum Average (2026) - "Test 1 of the ranges: an odds model fitted to the 1990s" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/long_backtest_ranges.csv

```bibtex
@misc{signumaverage-long-backtest-ranges,
    author = {{Signum Average}},
    title = {Test 1 of the ranges: an odds model fitted to the 1990s},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/long_backtest_ranges.csv}},
    note = {Dataset}
}
```

## range_check.csv

**Test 2 of the ranges: the published ranges against the method's past errors.** For each past launch, how many states' actual 2020 white share would have fallen inside a range of the published model's width placed around the projection.

Coverage: Four start years, 10 to 25 years ahead. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `launch / years_ahead` | Start year and years to 2020. |
| `states_inside_80 / states_inside_95 / of` | States inside a range of the published width (targets 41 and 48 of 51). |
| `stretch_needed` | Stretch this test calls for; the largest across rows (1.08) is applied to the published ranges. |
| `typical_state_range_80_pp` | Typical width of a state's published 80% range at that horizon, percentage points. |
| `states_projected_too_low` | States where the projection put the white share below what happened. |
| `national_errors_inside_80` | National errors, at every horizon and launch, inside the published national 80% range. |

Sources:

- National Center for Health Statistics, bridged-race population estimates, 1990-2020: https://www.cdc.gov/nchs/nvss/bridged_race.htm (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Uses bridged-race categories (four races by Hispanic origin, no two-or-more group), not the categories of the published projection: a test of the method.

How to cite:

Signum Average (2026) - "Test 2 of the ranges: the published ranges against the method's past errors" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/range_check.csv

```bibtex
@misc{signumaverage-range-check,
    author = {{Signum Average}},
    title = {Test 2 of the ranges: the published ranges against the method's past errors},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/range_check.csv}},
    note = {Dataset}
}
```

## probability_us_harsh.csv

**The harsh reading: US white share to 2075 with wider ranges.** The same simulated futures as probability_us.csv, stretched by what test 1 of the ranges called for instead of test 2. Medians are the same; ranges are much wider.

Coverage: United States; 2025-2075, every five years; three definitions of white. Last updated: 2026-10-05.

| Column | Description |
|---|---|
| `definition` | As in probability_us.csv. |
| `year` | Year (1 July). |
| `p2.5 ... p97.5` | Percentiles of the share, %. |

Sources:

- Signum Average calculations (CC BY 4.0)

Notes:

- The stretch for the nation (up to 2.48 times) rests on a single past outcome; the extreme percentiles are not meaningful.

How to cite:

Signum Average (2026) - "The harsh reading: US white share to 2075 with wider ranges" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/probability_us_harsh.csv

```bibtex
@misc{signumaverage-probability-us-harsh,
    author = {{Signum Average}},
    title = {The harsh reading: US white share to 2075 with wider ranges},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-05_america-in-2075/probability_us_harsh.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
