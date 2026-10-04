# Data for https://website.thesignumaverage.workers.dev/articles/what-sanctions-cost-iranians/

The datasets behind this article from The Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## iran_enriched_uranium_iaea.csv

**Iran's enriched-uranium stockpile, with a source for every point.** Iran's stock of enriched uranium as reported by the International Atomic Energy Agency (IAEA), from the start of the Natanz enrichment plant in 2007 to June 2025. Every row cites the IAEA report it comes from. Figures are converted to kilograms of uranium so they can be compared across years.

Coverage: 2007-2025, quarterly. Last updated: 2026-09-29.

| Column | Description |
|---|---|
| `date` | Date of the IAEA figure (YYYY-MM-DD), usually the verification date in the quarterly report. |
| `total_kgU` | Total enriched-uranium stockpile, all enrichment levels and chemical forms, in kilograms of uranium. |
| `heu60_kgU` | Uranium enriched up to 60% U-235, in kilograms of uranium. Empty before Iran began 60% enrichment in 2021. |
| `near20_uf6_kgU` | Uranium enriched up to about 20% U-235 held as uranium hexafluoride (UF6), in kilograms of uranium, where reported. |
| `measure` | What the IAEA figure measures: start (plant start-up), cumulative_production, uf6_stock, jcpoa_cap or total_all_forms. |
| `raw_value` | The figure as the IAEA reported it, before conversion. |
| `raw_unit` | Unit of raw_value: kg UF6 (kilograms of uranium hexafluoride) or kgU (kilograms of uranium). |
| `note` | What the figure covers and any caveat. |
| `source` | The IAEA document the figure comes from, such as a Board of Governors report number (GOV/...). |

Sources:

- IAEA quarterly verification and monitoring reports on Iran, 2008-2025: https://www.iaea.org/newscenter/focus/iran (Figures cited from public IAEA reports)

Notes:

- Before 2016 the IAEA reported uranium hexafluoride; it is converted here at 0.676 kg of uranium per kg of UF6.
- Figures for 2008-10 are cumulative production, so they are upper bounds on the stock.
- No comparable stock figure exists for 2011-13.
- The IAEA has not verified the stockpile since June 2025.

How to cite:

The Signum Average (2026) - "Iran's enriched-uranium stockpile, with a source for every point" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/iran_enriched_uranium_iaea.csv

```bibtex
@misc{signumaverage-iran-enriched-uranium-iaea,
    author = {{The Signum Average}},
    title = {Iran's enriched-uranium stockpile, with a source for every point},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/iran_enriched_uranium_iaea.csv}},
    note = {Dataset}
}
```

## synthetic_control_gaps.csv

**Iran vs "synthetic Iran": GDP per person gap.** Iran's real GDP per person compared with a "synthetic Iran": a weighted blend of oil-producing countries that were not under heavy sanctions or at war. The file gives both paths as indices and the gap between them. A negative gap means Iran was poorer than its twin. There are two versions of the gap, one fitted before the 2012 sanctions and one fitted before the 2018 sanctions.

Coverage: 1995-2025. Last updated: 2026-10-02.

| Column | Description |
|---|---|
| `year` | Calendar year. |
| `iran_index_2011_100` | Iran's real GDP per person, 2011 = 100. |
| `twin_index_2011_100` | The synthetic twin's real GDP per person, 2011 = 100, for the twin fitted on 1995-2011. |
| `gap_2012_model` | Iran minus its synthetic twin, in log points (close to % for small gaps; 14 log points is 13%), for the twin fitted on years before the 2012 EU oil embargo and SWIFT cut-off. |
| `gap_2018_model` | The same gap for the twin fitted on years before the US withdrawal from the nuclear deal in 2018. |

Sources:

- World Bank, World Development Indicators: GDP per capita, constant 2015 US$ (NY.GDP.PCAP.KD): https://data.worldbank.org/indicator/NY.GDP.PCAP.KD (CC BY 4.0)
- The Signum Average: synthetic-control calculations (CC BY 4.0)

Notes:

- The donor pool is 29 oil producers. Iraq, Libya, Syria and Yemen are excluded because of war, and Venezuela and Russia because of heavy sanctions or collapse.
- Donor weights are non-negative, sum to one and minimise the fit error before each episode.
- For the 2012 episode, placebo tests give p of about 0.07. For the 2018 episode measured over 2018-25, p = 0.23.
- Revised on 2 October 2026: the data source changed from the Maddison Project (to 2022) to the World Bank (to 2025). With Maddison data the 2015 gap is 12%.

How to cite:

The Signum Average (2026) - "Iran vs "synthetic Iran": GDP per person gap" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/synthetic_control_gaps.csv

```bibtex
@misc{signumaverage-synthetic-control-gaps,
    author = {{The Signum Average}},
    title = {Iran vs "synthetic Iran": GDP per person gap},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/synthetic_control_gaps.csv}},
    note = {Dataset}
}
```

## iran_inflation_vs_peers.csv

**Inflation, Iran vs peer oil producers.** Annual consumer-price inflation in Iran compared with the median of peer oil-producing countries, 2000-2025.

Coverage: 2000-2025. Last updated: 2026-10-02.

| Column | Description |
|---|---|
| `Year` | Calendar year. |
| `iran_inflation_pct` | Iran's consumer-price inflation, % change on the previous year. |
| `peer_median_pct` | Median consumer-price inflation across the peer oil exporters with data that year, %. |
| `n_peers` | Number of peer countries with data that year. |

Sources:

- World Bank, World Development Indicators: inflation, consumer prices (FP.CPI.TOTL.ZG): https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG (CC BY 4.0)

Notes:

- Peers are the oil producers used for the synthetic Iran that have at least 20 years of inflation data in the World Bank series (26 countries).

How to cite:

The Signum Average (2026) - "Inflation, Iran vs peer oil producers" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/iran_inflation_vs_peers.csv

```bibtex
@misc{signumaverage-iran-inflation-vs-peers,
    author = {{The Signum Average}},
    title = {Inflation, Iran vs peer oil producers},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/iran_inflation_vs_peers.csv}},
    note = {Dataset}
}
```

## spec_curve_results.csv

**Oil revenue, sanctions and household consumption: 60 model estimates.** Estimates of how oil revenue and heavy multilateral sanctions affected the growth of household consumption per person in Iran, from 60 versions of the same time-series model. Each row is one distinct combination of reasonable modelling choices, so readers can see how much the answer depends on them.

Coverage: 1981-2025. Last updated: 2026-10-02.

| Column | Description |
|---|---|
| `coding` | How sanctions are dated: baseline (fraction of each year in force), full-year from announcement, the 2014-15 interim deal counted as partial easing, 2018 counted as fully sanctioned, or 2021-25 counted as half-enforced. |
| `start` | First year of the estimation sample (1981 or 1990). |
| `drop2020` | True if 2020 (the pandemic year) is excluded. |
| `drop_war` | True if the Iran-Iraq war years are excluded. |
| `lag` | True if last year's consumption growth is included as a control. |
| `s` | Estimated effect of heavy sanctions being in force, over and above lost oil revenue, on annual household consumption growth per person, in percentage points a year. |
| `p` | p-value for that estimate, from heteroskedasticity- and autocorrelation-robust standard errors. |
| `oil` | Estimated elasticity of household consumption growth to real oil revenue: percentage points of growth per 1% change in revenue. |
| `p_oil` | p-value for the oil-revenue estimate. |
| `gap2020` | Implied shortfall in household consumption per person by 2020 compared with a world where 2017 conditions continued, %. |
| `n` | Number of years in the estimation sample. |

Sources:

- World Bank, World Development Indicators: household final consumption expenditure per capita growth (NE.CON.PRVT.PC.KD.ZG): https://data.worldbank.org/indicator/NE.CON.PRVT.PC.KD.ZG (CC BY 4.0)
- IMF Regional Economic Outlook: crude oil exports for Iran, via FRED (IRNNXGOCMBD); Energy Institute Statistical Review via Our World in Data for years before 2000; EIA Brent prices: https://fred.stlouisfed.org/series/IRNNXGOCMBD (Public data; see the source for terms)
- The Signum Average: model estimates (CC BY 4.0)

Notes:

- The oil-revenue effect is positive and statistically significant at the 5% level in all 60 versions. The effect of sanctions being in force, over and above lost oil revenue, is negative in 57% of versions and significant in none.
- Revised on 2 October 2026: the consumption series was updated to the World Bank's current figures and extended to 2025, oil revenue now uses the IMF's crude-export series, and duplicate versions were removed. The earlier file reported 64 rows, of which 48 were distinct.
- The model is described in the article's Data and methods section.

How to cite:

The Signum Average (2026) - "Oil revenue, sanctions and household consumption: 60 model estimates" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/spec_curve_results.csv

```bibtex
@misc{signumaverage-spec-curve-results,
    author = {{The Signum Average}},
    title = {Oil revenue, sanctions and household consumption: 60 model estimates},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/spec_curve_results.csv}},
    note = {Dataset}
}
```

## outlook_scenarios.csv

**Household consumption in Iran: projections for 2026 and 2027 under three oil scenarios.** Projections of household consumption per person in Iran under three scenarios for 2027: the blockade and the war continue, the blockade leaks while the war continues, or a deal is reached by spring. Published before the outcome is known so that the projections can be checked later.

Coverage: 2026-2027. Last updated: 2026-10-02.

| Column | Description |
|---|---|
| `indicator` | What is projected: household consumption per person. |
| `scenario` | Blockade holds (crude exports 0.15m barrels a day, Brent $90, war all year), Leaky blockade (0.65m, $85, war all year) or Deal by spring (1.2m, $75, war for a quarter of the year). The 2026 row is the same in every scenario. |
| `year` | Calendar year. |
| `growth_p10` | Growth on the previous year, %: 10th percentile of the simulations. |
| `growth_median` | Growth on the previous year, %: median. |
| `growth_p90` | Growth on the previous year, %: 90th percentile. |
| `index_p10` | Level, 2017 = 100: 10th percentile. The 2025 level is 93.7. |
| `index_median` | Level, 2017 = 100: median. |
| `index_p90` | Level, 2017 = 100: 90th percentile. |
| `vs2025_p10` | Change on 2025, %: 10th percentile. |
| `vs2025_median` | Change on 2025, %: median. |
| `vs2025_p90` | Change on 2025, %: 90th percentile. |

Sources:

- World Bank, World Development Indicators: households and NPISHs final consumption expenditure per capita, constant 2015 US$ (NE.CON.PRVT.PC.KD): https://data.worldbank.org/indicator/NE.CON.PRVT.PC.KD (CC BY 4.0)
- IMF World Economic Outlook Update, July 2026: https://www.imf.org/en/Publications/WEO (Figures cited from a public report)
- The Signum Average: projections (CC BY 4.0)

Notes:

- These are conditional projections, not forecasts of which scenario will happen.
- The projection for 2027 includes a war term: the average shortfall of consumption growth in the Iran-Iraq war years, applied to the share of 2027 spent at war.
- The blockade scenario is more likely too mild than too harsh: the fall in oil revenue is capped at the largest in the historical record.
- The method is described in the article's Data and methods section.

How to cite:

The Signum Average (2026) - "Household consumption in Iran: projections for 2026 and 2027 under three oil scenarios" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/outlook_scenarios.csv

```bibtex
@misc{signumaverage-outlook-scenarios,
    author = {{The Signum Average}},
    title = {Household consumption in Iran: projections for 2026 and 2027 under three oil scenarios},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/outlook_scenarios.csv}},
    note = {Dataset}
}
```

## iran_2026_monitor.csv

**Iran's economy in 2026: reported readings, with a source for every figure.** Readings of Iran's exchange rate, inflation, oil exports, oil held at sea and GDP during the war and blockade of 2026, as reported in the press. Every row names its source and links to it.

Coverage: December 2025 to September 2026. Last updated: 2026-10-02.

| Column | Description |
|---|---|
| `date` | Date of the reading (YYYY-MM-DD); for monthly figures, the last day of the period. |
| `indicator` | What is measured, for example rial_open_market, cpi_point_to_point, crude_exports or floating_storage. |
| `value` | The figure. |
| `unit` | Unit of the figure. |
| `note` | What the figure covers and any caveat. |
| `source` | Who reported the figure, and whose data it is. |
| `url` | Link to the report. |

Sources:

- Press reports citing the Statistical Centre of Iran, the Central Bank of Iran, Kpler, Vortexa, TankerTrackers, United Against Nuclear Iran and the IMF (Figures cited from public reports)

Notes:

- These figures were collected from press reports and have not been checked against the original publications.
- Tanker trackers disagree with each other, and loadings differ from deliveries; treat the oil figures as approximate.
- For the exchange rate the article uses the daily open-market series published by Alanchand (alanchand.com), which is not reproduced here; the rial rows in this file are press reports.

How to cite:

The Signum Average (2026) - "Iran's economy in 2026: reported readings, with a source for every figure" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/iran_2026_monitor.csv

```bibtex
@misc{signumaverage-iran-2026-monitor,
    author = {{The Signum Average}},
    title = {Iran's economy in 2026: reported readings, with a source for every figure},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-09-29_what-sanctions-cost-iranians/iran_2026_monitor.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit The Signum Average. Third-party data keeps its original licence.
