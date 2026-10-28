# Data for https://signumaverage.com/articles/israel-exit-polls/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## exit-polls-projections.csv

**Israel's exit polls: every channel's projection, 2003-2026.** Seats projected for each list by each television channel's exit poll, at the close of polls (first) and, where one was published, in the revised projection later in the night (updated). 2006 and the 2009 projections of Channels 1 and 10 cover only the largest lists.

Coverage: Knesset elections of 2003, 2006, 2009, 2013, 2015, April 2019, September 2019, 2020, 2021, 2022 and 2026. Last updated: 2026-10-27.

| Column | Description |
|---|---|
| `election` | Election day. |
| `channel` | Kan 11 (Channel 1 before 2017), Channel 12 (Channel 2), Channel 13 (Channel 10), Channel 14, Channel 15, Channel 16. |
| `version` | first: the projection at the close of polls; updated: the revision published later the same night. |
| `pollster` | The polling firm, where reported. |
| `list` | The list, in the study's short English name (see results.csv for the full name). |
| `seats` | Projected seats. 0 where the projection put the list below the threshold. Ranges are recorded as midpoints. |
| `source` | Where the figure was read. |

Sources:

- Wikipedia, election and opinion-polling pages (Hebrew and English): https://he.wikipedia.org/wiki/הבחירות_לכנסת_העשרים_ושש (CC BY-SA 4.0)
- Election-night reports: ynet, mako, walla, the Times of Israel, Al Jazeera (one link per row) (Figures cited)
- Signum Average (CC BY 4.0)

Notes:

- Channel 10's 2003 projection sums to 125 seats as printed by ynet; it is kept as reported.

How to cite:

Signum Average (2026) - "Israel's exit polls: every channel's projection, 2003-2026" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/exit_polls.csv

```bibtex
@misc{signumaverage-exit-polls-projections,
    author = {{Signum Average}},
    title = {Israel's exit polls: every channel's projection, 2003-2026},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/exit_polls.csv}},
    note = {Dataset}
}
```

## exit-polls-results.csv

**Israel's exit polls: final seats by list, 2003-2022.** Final votes, vote share and seats of every list named by a projection or that won seats, with the study's short name and Wikipedia's full name.

Coverage: Knesset elections of 2003 to 2022. Last updated: 2026-10-27.

| Column | Description |
|---|---|
| `election` | Election day. |
| `list` | Short name used in the study. |
| `wikipedia_name` | The list's name on the English Wikipedia results table. |
| `votes, pct, seats` | Valid votes, share of valid votes and seats won. |

Sources:

- Central Elections Committee results, as tabulated on Wikipedia: https://en.wikipedia.org/wiki/2022_Israeli_legislative_election (CC BY-SA 4.0)
- Signum Average (CC BY 4.0)

How to cite:

Signum Average (2026) - "Israel's exit polls: final seats by list, 2003-2022" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/results.csv

```bibtex
@misc{signumaverage-exit-polls-results,
    author = {{Signum Average}},
    title = {Israel's exit polls: final seats by list, 2003-2022},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/results.csv}},
    note = {Dataset}
}
```

## exit-polls-blocs.csv

**Israel's exit polls: how each list was counted on the night.** For each election, which lists the channels and the press counted as the right-religious bloc, the opposition bloc, or neither, with a note on the source. Fixed from the night's reports, not from the coalition formed later.

Coverage: Knesset elections of 2003 to 2026. Last updated: 2026-10-27.

| Column | Description |
|---|---|
| `election, list` | Election day and the list's short name. |
| `bloc` | right, opposition or neither. |
| `note` | The report the definition follows, on the first row of each election. |

Sources:

- Election-night reports: ynet, mako, walla, the Times of Israel, Al Jazeera (one link per row) (Figures cited)
- Signum Average (CC BY 4.0)

How to cite:

Signum Average (2026) - "Israel's exit polls: how each list was counted on the night" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/blocs.csv

```bibtex
@misc{signumaverage-exit-polls-blocs,
    author = {{Signum Average}},
    title = {Israel's exit polls: how each list was counted on the night},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/blocs.csv}},
    note = {Dataset}
}
```

## exit-polls-errors.csv

**Israel's exit polls: the error of every projection.** For each full projection: seats placed with the wrong list, the mean and largest error across lists, the error on each bloc, whether the largest list was called right, and the lists called wrong at the threshold.

Coverage: Knesset elections of 2003 to 2022. Last updated: 2026-10-27.

| Column | Description |
|---|---|
| `election, channel, version` | Which projection. |
| `misallocated` | Seats placed with the wrong list: half the sum of absolute errors across lists. |
| `right_error, opposition_error, neither_error` | Projected minus final seats of each bloc, as counted on the night. |
| `largest_right, largest_list, largest_error` | Whether the projection named the right largest list; the final largest list; the projection's error on it. |
| `false_in, false_out, seats_false_in, seats_false_out` | Lists given seats that won none, lists given none that won seats, and the seats involved. |

Sources:

- Signum Average (CC BY 4.0)

How to cite:

Signum Average (2026) - "Israel's exit polls: the error of every projection" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/by_projection.csv

```bibtex
@misc{signumaverage-exit-polls-errors,
    author = {{Signum Average}},
    title = {Israel's exit polls: the error of every projection},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/by_projection.csv}},
    note = {Dataset}
}
```

## exit-polls-average.csv

**Israel's exit polls: the three channels' average against the count.** The mean of the three main channels' first projections, by bloc, against the final count: the series the article's lead chart and forecast are built on.

Coverage: Knesset elections of 2003 to 2026. Last updated: 2026-10-27.

| Column | Description |
|---|---|
| `election, channels` | Election day and how many of the three channels had a full projection. |
| `right_avg, opposition_avg, neither_avg` | The average projection's seats for each bloc. |
| `right_final, opposition_final, neither_final` | The final count for each bloc. |
| `right_error, opposition_error, gap_error, misallocated` | Projected minus final for the blocs and for the gap between the two largest lists; seats misplaced by the average. |

Sources:

- Signum Average (CC BY 4.0)

How to cite:

Signum Average (2026) - "Israel's exit polls: the three channels' average against the count" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/average.csv

```bibtex
@misc{signumaverage-exit-polls-average,
    author = {{Signum Average}},
    title = {Israel's exit polls: the three channels' average against the count},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/average.csv}},
    note = {Dataset}
}
```

## exit-polls-backtest.csv

**Israel's exit polls: the forecast's backtest.** For each past election, the lean and spread fitted on the other eight, and the log score of the final right-bloc seats with and without the lean correction, with whether the 90% range covered the result.

Coverage: Knesset elections of 2003 to 2022, leave-one-out. Last updated: 2026-10-27.

| Column | Description |
|---|---|
| `election, right_avg, right_final, error` | The election, the average projection, the count, and projected minus final. |
| `lean_fitted, sd_fitted` | Mean and standard deviation of the bloc error on the other elections. |
| `logscore_with_lean, logscore_no_lean` | Log density of the final result under a Student t centred with and without the lean correction. |
| `in_90_with_lean, in_90_no_lean` | Whether the 90% range covered the result. |

Sources:

- Signum Average (CC BY 4.0)

How to cite:

Signum Average (2026) - "Israel's exit polls: the forecast's backtest" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/backtest.csv

```bibtex
@misc{signumaverage-exit-polls-backtest,
    author = {{Signum Average}},
    title = {Israel's exit polls: the forecast's backtest},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-27_israel-exit-polls/backtest.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
