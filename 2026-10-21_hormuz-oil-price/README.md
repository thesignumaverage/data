# Data for https://signumaverage.com/articles/hormuz-oil-price/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## hormuz-prices.csv

**Hormuz detour: Brent and WTI spot prices.** Daily spot prices of Brent (sea-borne crude, Europe) and West Texas Intermediate (US inland crude), and the gap between them.

Coverage: Daily, January 2025 to 20 October 2026. Last updated: 2026-10-21.

| Column | Description |
|---|---|
| `date` | Trading day. |
| `brent_usd` | Europe Brent spot price FOB, dollars a barrel (EIA series RBRTE). |
| `wti_usd` | Cushing, Oklahoma WTI spot price FOB, dollars a barrel (EIA series RWTC). |
| `brent_minus_wti_usd` | Brent minus WTI, dollars a barrel. |

Sources:

- US Energy Information Administration, spot prices: https://www.eia.gov/dnav/pet/pet_pri_spt_s1_d.htm (Public domain (US government work))

Notes:

- EIA publishes with a lag of about a week; the last day is the latest available when the study was run.

How to cite:

Signum Average (2026) - "Hormuz detour: Brent and WTI spot prices" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-21_hormuz-oil-price/prices.csv

```bibtex
@misc{signumaverage-hormuz-prices,
    author = {{Signum Average}},
    title = {Hormuz detour: Brent and WTI spot prices},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-21_hormuz-oil-price/prices.csv}},
    note = {Dataset}
}
```

## hormuz-sources.csv

**Hormuz detour: where each reported flow figure comes from.** Every published report of Kpler's oil-flow figures for the Gulf that the study used or checked, with the period, the measure, the pre-war baseline it was compared with, the outlet and a link. The figures themselves are not included: Kpler's data are proprietary, so follow the link to read each one.

Coverage: Press reports, November 2025 to 21 October 2026. Last updated: 2026-10-21.

| Column | Description |
|---|---|
| `period_start, period_end` | Days the figure covers (blank if the report does not say). |
| `measure` | What was measured, e.g. crude_flow, crude_products_flow, tanker_transits. |
| `scope` | hormuz_only (the strait), gulf_incl_bypass (strait plus pipelines to the Gulf of Oman and the Red Sea), gulf_exports, or other. |
| `baseline_definition` | The pre-war level the report compares with, as the report states it. |
| `outlet, publish_date, url` | Where and when the figure was published. |

Sources:

- Kpler media briefings and blog; Wall Street Journal, Al Jazeera, CNBC, CNN, The National, Reuters and others (one link per row) (Figures cited, not reproduced)
- Signum Average compilation (CC BY 4.0)

Notes:

- At least six different pre-war baselines appear in these reports; compare a figure only with its own baseline.
- Kpler warns that its most recent days are minimums and are usually revised up.

How to cite:

Signum Average (2026) - "Hormuz detour: where each reported flow figure comes from" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-21_hormuz-oil-price/sources.csv

```bibtex
@misc{signumaverage-hormuz-sources,
    author = {{Signum Average}},
    title = {Hormuz detour: where each reported flow figure comes from},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-21_hormuz-oil-price/sources.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
