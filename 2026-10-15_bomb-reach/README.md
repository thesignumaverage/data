# Data for https://signumaverage.com/articles/bomb-reach/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## pk.csv

**Bomb reach: chance of destroying a buried hall.** The chance that one weapon, dropped once, destroys a hardened hall at the reported depth of three Iranian sites, from 60,000 simulated strikes per weapon and site.

Coverage: Four weapons, three sites. Last updated: 2026-10-15.

| Column | Description |
|---|---|
| `weapon, weapon_name` | Weapon key and name. |
| `site, site_name` | Site key and name. |
| `depth_lo, depth_hi` | Reported depth range of the halls, metres; each trial draws a depth within it. |
| `ground` | Ground reported at the site. The simulation treats every site as granite. |
| `p_destroy` | Share of trials in which the hall lies inside the severe-shock zone (0 to 1). |
| `mc_error` | Sampling error of p_destroy (binomial standard error). |

Sources:

- National Research Council, Effects of Nuclear Earth-Penetrator and Other Weapons (2005): https://nap.nationalacademies.org/catalog/11282 (Figures cited)
- P.-A. Persson, R. Holmberg and J. Lee, Rock Blasting and Explosives Engineering (1994) (Figures cited)
- C. W. Young, Penetration equations, Sandia National Laboratories SAND97-2426 (1997): https://www.osti.gov/biblio/562498 (Public domain (US government work))
- Public weapon specifications (one source per row of weapons.csv) (Figures cited)
- Signum Average calculations (CC BY 4.0)

Notes:

- One weapon dropped once. Repeated strikes down one shaft are not modelled.
- An effects estimate good to about a factor of two, for hypothetical halls; not an assessment of any real site.

How to cite:

Signum Average (2026) - "Bomb reach: chance of destroying a buried hall" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/pk.csv

```bibtex
@misc{signumaverage-pk,
    author = {{Signum Average}},
    title = {Bomb reach: chance of destroying a buried hall},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/pk.csv}},
    note = {Dataset}
}
```

## zones.csv

**Bomb reach: crushed, cracked and severe-shock zones.** Radius around the burst point, in granite, inside which rock is crushed, newly cracked, or shaken hard enough to wreck a hardened room, for four weapons.

Coverage: Four weapons, granite. Last updated: 2026-10-15.

| Column | Description |
|---|---|
| `weapon, weapon_name` | Weapon key and name. |
| `zone` | pulverised (crushed), fractured (cracked) or severe shock (a hardened room wrecked). |
| `radius_p10, radius_p50, radius_p90` | Radius from the burst point, metres: 10th, 50th and 90th percentiles across 60,000 trials. |
| `depth_reached_p50` | Median depth below the surface that the zone reaches (digging depth plus radius), metres. |

Sources:

- National Research Council, Effects of Nuclear Earth-Penetrator and Other Weapons (2005): https://nap.nationalacademies.org/catalog/11282 (Figures cited)
- P.-A. Persson, R. Holmberg and J. Lee, Rock Blasting and Explosives Engineering (1994) (Figures cited)
- C. W. Young, Penetration equations, Sandia National Laboratories SAND97-2426 (1997): https://www.osti.gov/biblio/562498 (Public domain (US government work))
- Public weapon specifications (one source per row of weapons.csv) (Figures cited)
- Signum Average calculations (CC BY 4.0)

Notes:

- The crushed (pulverised) radius stretches an elastic relation into the near field and is the least certain.

How to cite:

Signum Average (2026) - "Bomb reach: crushed, cracked and severe-shock zones" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/zones.csv

```bibtex
@misc{signumaverage-zones,
    author = {{Signum Average}},
    title = {Bomb reach: crushed, cracked and severe-shock zones},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/zones.csv}},
    note = {Dataset}
}
```

## reach.csv

**Bomb reach: how deep each weapon reaches in five kinds of ground.** How far each of eleven weapons digs into five kinds of ground, and how deep below the surface its shock causes severe or light damage to an underground room.

Coverage: Eleven weapons, five kinds of ground. Last updated: 2026-10-15.

| Column | Description |
|---|---|
| `weapon, weapon_name` | Weapon key and name. |
| `ground, ground_name` | Kind of ground (see ground.csv). |
| `pen_p10, pen_p50, pen_p90` | Depth the weapon digs before it goes off, metres (10th, 50th and 90th percentiles across 4,000 random draws of the uncertain inputs). |
| `severe_p10, severe_p50, severe_p90` | Depth below the surface to which ground shock does severe damage to a hardened room (peak particle velocity 5-15 m/s), metres (10th, 50th and 90th percentiles across 4,000 random draws of the uncertain inputs). |
| `light_p10, light_p50, light_p90` | Depth to which it causes light damage: rock falls, cracked linings, equipment knocked over (0.5-2 m/s), metres (10th, 50th and 90th percentiles across 4,000 random draws of the uncertain inputs). |

Sources:

- C. W. Young, Penetration equations, Sandia National Laboratories SAND97-2426 (1997): https://www.osti.gov/biblio/562498 (Public domain (US government work))
- National Research Council, Effects of Nuclear Earth-Penetrator and Other Weapons (2005): https://nap.nationalacademies.org/catalog/11282 (Figures cited)
- P.-A. Persson, R. Holmberg and J. Lee, Rock Blasting and Explosives Engineering (1994) (Figures cited)
- Public weapon specifications (one source per row of weapons.csv) (Figures cited)
- Signum Average calculations (CC BY 4.0)

How to cite:

Signum Average (2026) - "Bomb reach: how deep each weapon reaches in five kinds of ground" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/reach.csv

```bibtex
@misc{signumaverage-reach,
    author = {{Signum Average}},
    title = {Bomb reach: how deep each weapon reaches in five kinds of ground},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/reach.csv}},
    note = {Dataset}
}
```

## horizontal.csv

**Bomb reach: how far blast, heat and radiation travel.** Distance from a surface burst at which each weapon's air blast reaches 20, 5 and 1 psi, and for nuclear settings the radii for burns and prompt radiation.

Coverage: Eleven weapons. Last updated: 2026-10-15.

| Column | Description |
|---|---|
| `weapon, weapon_name` | Weapon key and name. |
| `kind` | conventional or nuclear. |
| `mode` | How it is designed to go off: penetrate, surface or airburst. |
| `tnt_tonnes` | Explosive power as tonnes of TNT (central value; for nuclear weapons the yield). |
| `r20psi_m, r5psi_m, r1psi_m` | Distance at which peak overpressure falls to 20 psi (reinforced concrete destroyed), 5 psi (most buildings flattened) and 1 psi (windows broken), metres. |
| `burns_m` | Nuclear only: distance for a 50% chance of third-degree burns, metres. |
| `rad500_m` | Nuclear only: distance for a prompt radiation dose of 500 rem, metres. |

Sources:

- G. F. Kinney and K. J. Graham, Explosive Shocks in Air (1985) (Figures cited)
- S. Glasstone and P. J. Dolan, The Effects of Nuclear Weapons (1977): https://www.osti.gov/biblio/6852629 (Public domain (US government work))
- Public weapon specifications (one source per row of weapons.csv) (Figures cited)
- Signum Average calculations (CC BY 4.0)

Notes:

- Surface-burst radii. A weapon that has dug itself in makes less air blast.

How to cite:

Signum Average (2026) - "Bomb reach: how far blast, heat and radiation travel" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/horizontal.csv

```bibtex
@misc{signumaverage-horizontal,
    author = {{Signum Average}},
    title = {Bomb reach: how far blast, heat and radiation travel},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/horizontal.csv}},
    note = {Dataset}
}
```

## weapons.csv

**Bomb reach: weapon inputs.** Public figures for the eleven weapons in the study: mass, diameter, explosive filling, yield, impact speed and the maker's or press claims, with a source for each row.

Coverage: Eleven weapons and settings. Last updated: 2026-10-15.

| Column | Description |
|---|---|
| `key, name` | Weapon key and name. |
| `kind` | conventional or nuclear. |
| `mass_kg, diam_m` | Mass (kg) and diameter (m). |
| `fill_kg, fill` | Explosive filling, kg, and its type. |
| `re_lo, re_hi` | TNT equivalence of the filling, range. |
| `yield_kt` | Nuclear yield, kilotons. |
| `mode` | penetrate, surface or airburst. |
| `v_lo, v_hi` | Impact speed range, m/s. |
| `burst_h_lo, burst_h_hi` | Height of burst above the ground, metres (MOAB). |
| `claim` | Published claim of penetration, where there is one. |
| `source` | Sources for the row. |

Sources:

- Public weapon specifications (one source per row of weapons.csv) (Figures cited)

How to cite:

Signum Average (2026) - "Bomb reach: weapon inputs" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/weapons.csv

```bibtex
@misc{signumaverage-weapons,
    author = {{Signum Average}},
    title = {Bomb reach: weapon inputs},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/weapons.csv}},
    note = {Dataset}
}
```

## ground.csv

**Bomb reach: ground inputs.** Inputs for the five kinds of ground: penetrability, strength, rock quality, reinforcement and shock attenuation, as ranges.

Coverage: Five kinds of ground. Last updated: 2026-10-15.

| Column | Description |
|---|---|
| `key, name` | Ground key and name. |
| `route` | Which ground-shock method applies: soil or rock. |
| `S_lo, S_hi` | Young's penetrability number for soil. |
| `fc_lo, fc_hi` | Unconfined compressive strength, MPa. |
| `Q_lo, Q_hi` | Rock quality, 0 to 1. |
| `rebar_lo, rebar_hi` | Reinforcement, % by volume (concrete). |
| `n_lo, n_hi` | Attenuation exponent for soil (TM 5-855-1). |
| `source` | Sources for the row. |

Sources:

- C. W. Young, Penetration equations, Sandia National Laboratories SAND97-2426 (1997): https://www.osti.gov/biblio/562498 (Public domain (US government work))
- Signum Average calculations (CC BY 4.0)

How to cite:

Signum Average (2026) - "Bomb reach: ground inputs" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/ground.csv

```bibtex
@misc{signumaverage-ground,
    author = {{Signum Average}},
    title = {Bomb reach: ground inputs},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/ground.csv}},
    note = {Dataset}
}
```

## targets.csv

**Bomb reach: reported depths of three Iranian sites.** Public estimates of the depth of the underground halls at Natanz, Fordow and Pickaxe Mountain, as ranges, with sources.

Coverage: Three sites. Last updated: 2026-10-15.

| Column | Description |
|---|---|
| `key, name` | Site key and name. |
| `ground` | Ground reported at the site. |
| `depth_lo, depth_hi` | Reported depth range, metres. |
| `depth_note` | Where the range comes from. |
| `source` | Source. |

Sources:

- Institute for Science and International Security; AP and CNS; press reports: https://isis-online.org/isis-reports/irans-natanz-tunnel-complex-deeper-larger-than-expected (Figures cited)

Notes:

- Estimates, not surveys. No site layout is public.

How to cite:

Signum Average (2026) - "Bomb reach: reported depths of three Iranian sites" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/targets.csv

```bibtex
@misc{signumaverage-targets,
    author = {{Signum Average}},
    title = {Bomb reach: reported depths of three Iranian sites},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/targets.csv}},
    note = {Dataset}
}
```

## damage.csv

**Bomb reach: rock and damage inputs for the simulation.** The ranges drawn in each of the 60,000 simulated strikes: granite properties, damage thresholds, already-broken rock and aim error, with sources.

Coverage: Nine inputs. Last updated: 2026-10-15.

| Column | Description |
|---|---|
| `parameter` | Input. |
| `symbol` | Symbol used in the methods. |
| `lo, hi` | Range drawn. |
| `unit` | Unit. |
| `note` | What it is. |
| `source` | Source. |

Sources:

- National Research Council, Effects of Nuclear Earth-Penetrator and Other Weapons (2005): https://nap.nationalacademies.org/catalog/11282 (Figures cited)
- Signum Average calculations (CC BY 4.0)

Notes:

- The simulation draws the severe-damage threshold from 1.5 to 15 m/s (lower in broken rock); the fail_ppv_hardened row gives the literature's range.

How to cite:

Signum Average (2026) - "Bomb reach: rock and damage inputs for the simulation" [Dataset] Published online at signumaverage.com. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/damage.csv

```bibtex
@misc{signumaverage-damage,
    author = {{Signum Average}},
    title = {Bomb reach: rock and damage inputs for the simulation},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-15_bomb-reach/damage.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
