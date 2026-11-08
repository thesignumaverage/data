# Data for https://signumaverage.com/articles/iran-nuclear/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## iran-iaea-stock.csv

**Iran's enriched uranium, every IAEA report, 2003-2026.** Iran's enriched uranium stock by level, or the cumulative amount produced where the reports give only that (2007-2015), at each IAEA report, with the figures as printed, the paragraph and the link.

Coverage: 96 IAEA reports, 2003 to 2026. Last updated: 2026-11-07.

| Column | Description |
|---|---|
| `report, report_date, as_of` | The IAEA document, its date and the date the figures refer to. |
| `leu5_kgU, leu20_kgU, heu60_kgU, total_kgU` | Stock enriched up to 5%, up to 20% and up to 60%, and the total in all forms, kg of uranium. |
| `cumulative_produced_kgU, cumulative_produced_leu20_kgU` | Amount produced since enrichment began, up to 5% and up to 20%, kg of uranium (2007-2015 reports). |
| `units_in_report, raw_values` | The unit and figures as the report prints them; kg of UF6 converted at 0.676 where no uranium figure is given. |
| `paragraph, url, notes` | Where the figure is, and anything to know (estimates by Iran, sums of printed figures, changes of definition). |

Sources:

- IAEA, reports of the Director General to the Board of Governors on Iran (GOV/ series): https://www.iaea.org/newscenter/focus/iran/iaea-and-iran-iaea-reports (Public documents of the IAEA, quoted with attribution)

Notes:

- Rows marked 'SUM COMPUTED BY US' add an Agency-verified amount and Iran's estimate printed separately.
- From June 2025 the IAEA cannot report the stock; those rows are blank.

How to cite:

Signum Average (2026) - "Iran's enriched uranium, every IAEA report, 2003-2026" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/iaea_stock.csv

```bibtex
@misc{signumaverage-iran-iaea-stock,
    author = {{Signum Average}},
    title = {Iran's enriched uranium, every IAEA report, 2003-2026},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/iaea_stock.csv}},
    note = {Dataset}
}
```

## iran-iaea-centrifuges.csv

**Iran's centrifuges by site and type, IAEA reports.** Centrifuges and cascades installed and being fed with uranium, by site (Natanz, Natanz pilot plant, Fordow) and type, as the IAEA reported them.

Coverage: IAEA reports, 2003 to 2026. Last updated: 2026-11-07.

| Column | Description |
|---|---|
| `report, as_of` | The IAEA document and the date the figures refer to. |
| `site, type` | The plant and the centrifuge model (IR-1, IR-2m, IR-4, IR-6, mixed or total). |
| `installed, operating` | Centrifuges installed and centrifuges being fed with uranium; blank where the report gives only cascades. |
| `cascades_installed, cascades_operating` | Cascades installed and being fed. |
| `paragraph, url, notes` | Where the figure is, and notes. |

Sources:

- IAEA, reports of the Director General to the Board of Governors on Iran (GOV/ series): https://www.iaea.org/newscenter/focus/iran/iaea-and-iran-iaea-reports (Public documents of the IAEA, quoted with attribution)

How to cite:

Signum Average (2026) - "Iran's centrifuges by site and type, IAEA reports" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/iaea_centrifuges.csv

```bibtex
@misc{signumaverage-iran-iaea-centrifuges,
    author = {{Signum Average}},
    title = {Iran's centrifuges by site and type, IAEA reports},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/iaea_centrifuges.csv}},
    note = {Dataset}
}
```

## iran-iaea-milestones.csv

**Iran's nuclear milestones as first reported by the IAEA.** The first IAEA report of each step in Iran's programme: enrichment levels, new plants and centrifuge models, uranium metal, and the agency's findings.

Coverage: 2006 to 2025. Last updated: 2026-11-07.

| Column | Description |
|---|---|
| `date, milestone` | When it happened and what. |
| `report, paragraph, url` | Where the IAEA reported it. |

Sources:

- IAEA, reports of the Director General to the Board of Governors on Iran (GOV/ series): https://www.iaea.org/newscenter/focus/iran/iaea-and-iran-iaea-reports (Public documents of the IAEA, quoted with attribution)

How to cite:

Signum Average (2026) - "Iran's nuclear milestones as first reported by the IAEA" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/iaea_milestones.csv

```bibtex
@misc{signumaverage-iran-iaea-milestones,
    author = {{Signum Average}},
    title = {Iran's nuclear milestones as first reported by the IAEA},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/iaea_milestones.csv}},
    note = {Dataset}
}
```

## iran-nuclear-timeline.csv

**Iran's nuclear programme: a sourced timeline, 2002-2026.** Dated events in six kinds: technical milestones, sanctions, diplomacy, sabotage and strikes, intelligence assessments and statements, each with a source.

Coverage: 2002 to 2026. Last updated: 2026-11-07.

| Column | Description |
|---|---|
| `date, kind` | Date (day 01 where only the month is known; see notes) and kind of event. |
| `title, detail` | What happened, in a phrase and in one or two sentences. |
| `source_url, source_name, notes` | The source, and any conflicts between sources. |

Sources:

- Signum Average (CC BY 4.0)

Notes:

- Each row cites its own source; the table is Signum Average's compilation.

How to cite:

Signum Average (2026) - "Iran's nuclear programme: a sourced timeline, 2002-2026" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/timeline.csv

```bibtex
@misc{signumaverage-iran-nuclear-timeline,
    author = {{Signum Average}},
    title = {Iran's nuclear programme: a sourced timeline, 2002-2026},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/timeline.csv}},
    note = {Dataset}
}
```

## iran-breakout-estimates.csv

**Official estimates of Iran's breakout time, 2012-2026.** Public estimates by US and Israeli officials and the IAEA's director general of how long Iran would need to make enough weapon-grade uranium for one weapon, or a weapon.

Coverage: 2012 to 2026. Last updated: 2026-11-07.

| Column | Description |
|---|---|
| `date, speaker, role` | Who said it and when. |
| `estimate, estimate_weeks` | The estimate as said, and in weeks where a number was given (midpoint of a range). |
| `what` | Whether the estimate is of enough weapon-grade uranium or of a weapon. |
| `source_url, notes` | Source and notes. |

Sources:

- Signum Average (CC BY 4.0)

How to cite:

Signum Average (2026) - "Official estimates of Iran's breakout time, 2012-2026" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/breakout_estimates.csv

```bibtex
@misc{signumaverage-iran-breakout-estimates,
    author = {{Signum Average}},
    title = {Official estimates of Iran's breakout time, 2012-2026},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/breakout_estimates.csv}},
    note = {Dataset}
}
```

## iran-fatwa-statements.csv

**The fatwa against nuclear weapons: statements, doubts and signals of change, 2003-2026.** Every public statement we could source on Ayatollah Ali Khamenei's ruling against nuclear weapons: its citations, reaffirmations, the doubts about its form, and the calls to change it, to November 2026.

Coverage: 2003 to 2026. Last updated: 2026-11-07.

| Column | Description |
|---|---|
| `date, speaker` | Who and when. |
| `what` | What was said, with brief quotes. |
| `kind` | issued_or_cited, reaffirmed, doubt_or_question, signal_of_change or unknown. |
| `source_url, notes` | Source and notes. |

Sources:

- Signum Average (CC BY 4.0)

How to cite:

Signum Average (2026) - "The fatwa against nuclear weapons: statements, doubts and signals of change, 2003-2026" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/fatwa.csv

```bibtex
@misc{signumaverage-iran-fatwa-statements,
    author = {{Signum Average}},
    title = {The fatwa against nuclear weapons: statements, doubts and signals of change, 2003-2026},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/fatwa.csv}},
    note = {Dataset}
}
```

## iran-weapon-steps.csv

**The steps to a nuclear weapon: where Iran stands, by public assessment.** For each of four steps (weapon-grade uranium, metal, weapon design, delivery), the public assessments of Iran's status, by whom and when. No assessment is Signum Average's.

Coverage: 2007 to 2026. Last updated: 2026-11-07.

| Column | Description |
|---|---|
| `step` | The step. |
| `status_summary` | The assessment, in one sentence at the source's level of detail. |
| `assessed_by, date, source_url` | Who made it, when, and where. |

Sources:

- Signum Average (CC BY 4.0)

How to cite:

Signum Average (2026) - "The steps to a nuclear weapon: where Iran stands, by public assessment" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/weapon_steps.csv

```bibtex
@misc{signumaverage-iran-weapon-steps,
    author = {{Signum Average}},
    title = {The steps to a nuclear weapon: where Iran stands, by public assessment},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/weapon_steps.csv}},
    note = {Dataset}
}
```

## iran-enrichment-periods.csv

**Iran's enrichment output and oil exports by sanctions period.** For each period fixed in advance (UN sanctions, EU oil embargo, interim deal, 2015 deal, maximum pressure), enriched uranium made a month (to 2015) or added to the stock (from 2017), the reports used, the stock enriched to 20% or more, and average crude exports.

Coverage: 2007 to 2025. Last updated: 2026-11-07.

| Column | Description |
|---|---|
| `period, name, start, end` | The period as fixed in the study's specification. |
| `oil_bpd` | Iran's average crude exports, barrels a day (IMF, annual, weighted by days). |
| `measure, from_report, from_date, from_kgU, to_report, to_date, to_kgU` | The two IAEA readings used and what they measure. |
| `kgU_per_month` | Enriched uranium made or added a month, kg of uranium. |
| `high_from, high_to, high_from_date, high_to_date` | Stock enriched to 20% or more at the start and end. |

Sources:

- Signum Average (CC BY 4.0)
- IMF, Iran crude oil exports, via FRED (IRNNXGOCMBD): https://fred.stlouisfed.org/series/IRNNXGOCMBD (Public)

How to cite:

Signum Average (2026) - "Iran's enrichment output and oil exports by sanctions period" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/periods.csv

```bibtex
@misc{signumaverage-iran-enrichment-periods,
    author = {{Signum Average}},
    title = {Iran's enrichment output and oil exports by sanctions period},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-11-07_iran-nuclear/periods.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
