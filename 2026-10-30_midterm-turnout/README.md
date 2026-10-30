# Data for https://signumaverage.com/articles/midterm-turnout/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## turnout_by_age.csv

**Reported turnout by age, every November election.** Share of each age group who said they voted, of all adults and of citizens, with the group's size.

Coverage: 1976-2022. Last updated: 2026-10-30.

| Column | Description |
|---|---|
| `year` | Election year (midterms 1978-2022, presidential years 1976-2020). |
| `turnout_all_<group>` | Share of all adults in the group who said they voted, %. Groups: total, 18-24, 25-44, 45-64, 65+. |
| `turnout_citizens_<group>` | The same among citizens, % (blank where the table does not give it). |
| `population_thousands_<group>` | People in the group, thousands. |

Sources:

- US Census Bureau, Current Population Survey, November voting supplement: Table A-1 (1964-2020) and Table 1 (2014, 2018, 2022): https://www.census.gov/library/visualizations/time-series/demo/voting-historical-time-series.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Turnout is the share who told the survey they voted; people who gave no answer count as not voting, as in the Census Bureau's own tables. Surveys overstate turnout.
- 2022 is built from the 2022 Table 1 by adding its finer age groups; the same method reproduces Table A-1's 2018 figures within 0.04 points.

How to cite:

Signum Average (2026) - "Reported turnout by age, every November election" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/turnout_by_age.csv

```bibtex
@misc{signumaverage-turnout-by-age,
    author = {{Signum Average}},
    title = {Reported turnout by age, every November election},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/turnout_by_age.csv}},
    note = {Dataset}
}
```

## electorate_shares.csv

**Who makes up the midterm electorate, by age.** Each age group's share of reported midterm voters and of all adults.

Coverage: Midterms 1978-2022. Last updated: 2026-10-30.

| Column | Description |
|---|---|
| `year` | Midterm year. |
| `share_of_voters_<group>` | Share of reported voters, %. |
| `share_of_adults_<group>` | Share of people aged 18 and over, %. |

Sources:

- US Census Bureau, Current Population Survey, November voting supplement: Table A-1 (1964-2020) and Table 1 (2014, 2018, 2022): https://www.census.gov/library/visualizations/time-series/demo/voting-historical-time-series.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Turnout is the share who told the survey they voted; people who gave no answer count as not voting, as in the Census Bureau's own tables. Surveys overstate turnout.

How to cite:

Signum Average (2026) - "Who makes up the midterm electorate, by age" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/electorate_shares.csv

```bibtex
@misc{signumaverage-electorate-shares,
    author = {{Signum Average}},
    title = {Who makes up the midterm electorate, by age},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/electorate_shares.csv}},
    note = {Dataset}
}
```

## drop.csv

**How much each age group falls away in midterms.** Midterm turnout divided by turnout in the presidential election two years before, by age.

Coverage: Midterms 1978-2022. Last updated: 2026-10-30.

| Column | Description |
|---|---|
| `midterm` | Midterm year. |
| `total, 18-24, 25-44, 45-64, 65+` | Ratio of midterm to presidential turnout (1 = no drop). |

Sources:

- US Census Bureau, Current Population Survey, November voting supplement: Table A-1 (1964-2020) and Table 1 (2014, 2018, 2022): https://www.census.gov/library/visualizations/time-series/demo/voting-historical-time-series.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Turnout is the share who told the survey they voted; people who gave no answer count as not voting, as in the Census Bureau's own tables. Surveys overstate turnout.

How to cite:

Signum Average (2026) - "How much each age group falls away in midterms" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/drop.csv

```bibtex
@misc{signumaverage-drop,
    author = {{Signum Average}},
    title = {How much each age group falls away in midterms},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/drop.csv}},
    note = {Dataset}
}
```

## single_ages_2022.csv

**Reported turnout by single year of age, 2022.** Share who said they voted in the 2022 midterms, by single year of age (80 and over grouped).

Coverage: November 2022. Last updated: 2026-10-30.

| Column | Description |
|---|---|
| `age` | Age. |
| `population, citizens, voted` | People, citizens and reported voters, thousands. |
| `turnout_all, turnout_citizens` | Share of everyone and of citizens who said they voted, %. |
| `no_answer_pct` | Share of citizens who gave no answer on voting, %. |

Sources:

- US Census Bureau, Current Population Survey, November voting supplement: Table A-1 (1964-2020) and Table 1 (2014, 2018, 2022): https://www.census.gov/library/visualizations/time-series/demo/voting-historical-time-series.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Turnout is the share who told the survey they voted; people who gave no answer count as not voting, as in the Census Bureau's own tables. Surveys overstate turnout.

How to cite:

Signum Average (2026) - "Reported turnout by single year of age, 2022" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/single_ages_2022.csv

```bibtex
@misc{signumaverage-single-ages-2022,
    author = {{Signum Average}},
    title = {Reported turnout by single year of age, 2022},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/single_ages_2022.csv}},
    note = {Dataset}
}
```

## check_overreport.csv

**How far the survey overstates turnout.** Survey turnout and its gap to turnout counted from votes cast against the voting-eligible population (University of Florida Election Lab). The Election Lab's own figures are not republished; see its site.

Coverage: Midterms 1982-2022. Last updated: 2026-10-30.

| Column | Description |
|---|---|
| `year` | Midterm year. |
| `survey_citizens, survey_all` | Survey turnout among citizens and among all adults, %. |
| `gap_to_counted_turnout` | Survey turnout (citizens) minus counted turnout, points. |

Sources:

- US Census Bureau, Current Population Survey, November voting supplement: Table A-1 (1964-2020) and Table 1 (2014, 2018, 2022): https://www.census.gov/library/visualizations/time-series/demo/voting-historical-time-series.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Turnout is the share who told the survey they voted; people who gave no answer count as not voting, as in the Census Bureau's own tables. Surveys overstate turnout.

How to cite:

Signum Average (2026) - "How far the survey overstates turnout" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/check_overreport.csv

```bibtex
@misc{signumaverage-check-overreport,
    author = {{Signum Average}},
    title = {How far the survey overstates turnout},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/check_overreport.csv}},
    note = {Dataset}
}
```

## check_no_answer.csv

**Turnout with and without the people who gave no answer.** Share of citizens who gave no answer on voting, turnout as the Census Bureau counts it, and turnout among those who answered, by age.

Coverage: Midterms 2014, 2018, 2022. Last updated: 2026-10-30.

| Column | Description |
|---|---|
| `year, group` | Midterm and age group. |
| `no_answer_pct` | Citizens who gave no answer on voting, %. |
| `turnout_census` | Reported voters as a share of all citizens, %. |
| `turnout_answered` | Reported voters as a share of citizens who answered, %. |

Sources:

- US Census Bureau, Current Population Survey, November voting supplement: Table A-1 (1964-2020) and Table 1 (2014, 2018, 2022): https://www.census.gov/library/visualizations/time-series/demo/voting-historical-time-series.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Turnout is the share who told the survey they voted; people who gave no answer count as not voting, as in the Census Bureau's own tables. Surveys overstate turnout.

How to cite:

Signum Average (2026) - "Turnout with and without the people who gave no answer" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/check_no_answer.csv

```bibtex
@misc{signumaverage-check-no-answer,
    author = {{Signum Average}},
    title = {Turnout with and without the people who gave no answer},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/check_no_answer.csv}},
    note = {Dataset}
}
```

## check_citizens.csv

**The age gap on citizens and on all adults.** Turnout of over-65s minus turnout of 18-to-24s, measured among all adults and among citizens.

Coverage: Midterms 2002-2022. Last updated: 2026-10-30.

| Column | Description |
|---|---|
| `year` | Midterm year. |
| `gap_all, gap_citizens` | Gap in points. |

Sources:

- US Census Bureau, Current Population Survey, November voting supplement: Table A-1 (1964-2020) and Table 1 (2014, 2018, 2022): https://www.census.gov/library/visualizations/time-series/demo/voting-historical-time-series.html (Public domain)
- Signum Average calculations (CC BY 4.0)

Notes:

- Turnout is the share who told the survey they voted; people who gave no answer count as not voting, as in the Census Bureau's own tables. Surveys overstate turnout.

How to cite:

Signum Average (2026) - "The age gap on citizens and on all adults" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/check_citizens.csv

```bibtex
@misc{signumaverage-check-citizens,
    author = {{Signum Average}},
    title = {The age gap on citizens and on all adults},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-30_midterm-turnout/check_citizens.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
