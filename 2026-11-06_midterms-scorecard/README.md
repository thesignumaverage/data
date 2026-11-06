# Data for https://signumaverage.com/articles/midterms-scorecard/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## midterms_senate_scorecard.csv

**Our 2026 Senate forecast against the results.** Every 2026 Senate race: our final forecast of 3 November, the polling average, and the result as called.

Coverage: 2026. Last updated: 2026-11-06.

| Column | Description |
|---|---|
| `state, special` | The race; special is true for the Florida and Ohio special elections. |
| `dem_side_candidate, rep_candidate` | The candidates our model compared. The Democratic side is an independent in Idaho, Nebraska and South Dakota. |
| `our_chance_dem` | Our final chance that the Democratic side wins, %. |
| `poll_average_margin` | Our average of the polls: Democratic side minus Republican share of the two-candidate vote, points (blank: no polls). |
| `forecast_margin, forecast_low80, forecast_high80` | Our forecast margin, points, and the range we gave as 80% likely. |
| `result_margin` | The result's margin on the same basis, points, where Wikipedia lists vote counts (blank otherwise). Not certified. |
| `result` | Who won as called by the news networks: Democratic side, Republican, or not yet called. |

Sources:

- Signum Average midterms forecast of 3 November 2026 and calculations (CC BY 4.0)
- Wikipedia, 2026 United States Senate and House of Representatives election pages (race calls and vote counts as of 6 November 2026): https://en.wikipedia.org/wiki/2026_United_States_elections (CC BY-SA 4.0)

Notes:

- Results are the networks' calls and unofficial counts as of 6 November 2026; Mississippi and Alaska were still counting.
- Polymarket prices quoted in the article are not included.

How to cite:

Signum Average (2026) - "Our 2026 Senate forecast against the results" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-06_midterms-scorecard/senate_scorecard.csv

```bibtex
@misc{signumaverage-midterms-senate-scorecard,
    author = {{Signum Average}},
    title = {Our 2026 Senate forecast against the results},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-06_midterms-scorecard/senate_scorecard.csv}},
    note = {Dataset}
}
```

## midterms_house_scorecard.csv

**Our 2026 House forecast against the results.** Every House district on the 2026 maps: our final forecast of 3 November and the winning party as called.

Coverage: 2026. Last updated: 2026-11-06.

| Column | Description |
|---|---|
| `district` | State and district number (at-large for single-seat states). |
| `pvi` | The district's partisan lean: positive leans Democratic, negative Republican, points. |
| `member` | The member before the election, or a new seat. |
| `d_cand, r_cand` | The Democratic and Republican candidates (blank where a party had none). |
| `our_chance_dem` | Our final chance of a Democratic win, %. |
| `forecast_margin` | Our expected Democratic minus Republican margin, points. |
| `result` | The winning party as called by the news networks, or not yet called. |

Sources:

- Signum Average midterms forecast of 3 November 2026 and calculations (CC BY 4.0)
- Wikipedia, 2026 United States Senate and House of Representatives election pages (race calls and vote counts as of 6 November 2026): https://en.wikipedia.org/wiki/2026_United_States_elections (CC BY-SA 4.0)

Notes:

- Calls as recorded on Wikipedia's 2026 House overview page on 6 November 2026; 24 seats were still open, Louisiana's 5th and 6th in a December runoff.
- Where both finalists were from one party (California's and Washington's top-two system), that party is recorded as the winner.

How to cite:

Signum Average (2026) - "Our 2026 House forecast against the results" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-06_midterms-scorecard/house_scorecard.csv

```bibtex
@misc{signumaverage-midterms-house-scorecard,
    author = {{Signum Average}},
    title = {Our 2026 House forecast against the results},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-06_midterms-scorecard/house_scorecard.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
