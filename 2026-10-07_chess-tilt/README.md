# Data for https://website.thesignumaverage.workers.dev/articles/chess-tilt/

The datasets behind this article from Signum Average. Each CSV in this folder is described below: what it covers, every column, its sources and how to cite it. Please also cite the original sources.

## after_previous_result.csv

**Chess: score after a win, a draw and a loss.** How players score, compared with what the ratings predict, by the result of their previous game.

Coverage: Lichess, September 2026; pairs of games in a row in one sitting. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `previous_result` | Result of the player's previous game: win, draw or loss. |
| `split, group` | Which games: all; by speed (bullet, blitz, rapid); or by the player's rating. |
| `games` | Number of games (each game counts once for each player). |
| `excess_score_pp` | Mean score minus the score the two ratings predict, percentage points. A win is 100, a draw 50. |
| `se_pp` | Standard error, percentage points (jackknife over 50 groups of players). |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Both games are ordinary pairings in the same speed, started at most 30 minutes apart. The rating is the one shown at the start of the game.
- A description, not a cause: a player in poor form loses both games.
- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: score after a win, a draw and a loss" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/after_previous_result.csv

```bibtex
@misc{signumaverage-after-previous-result,
    author = {{Signum Average}},
    title = {Chess: score after a win, a draw and a loss},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/after_previous_result.csv}},
    note = {Dataset}
}
```

## after_losing_streak.csv

**Chess: score by number of losses in a row.** How players score, compared with what the ratings predict, by the number of losses in a row just before the game.

Coverage: Lichess, September 2026; pairs of games in a row in one sitting. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `losses_in_a_row` | Losses in a row immediately before the game, in one sitting (games started at most 30 minutes apart). 5 means five or more. |
| `split, group` | Which games: all; by speed (bullet, blitz, rapid); or by the player's rating. |
| `games` | Number of games (each game counts once for each player). |
| `excess_score_pp` | Mean score minus the score the two ratings predict, percentage points. |
| `se_pp` | Standard error, percentage points (jackknife over 50 groups of players). |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- A description, not a cause: a player in poor form loses game after game.
- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: score by number of losses in a row" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/after_losing_streak.csv

```bibtex
@misc{signumaverage-after-losing-streak,
    author = {{Signum Average}},
    title = {Chess: score by number of losses in a row},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/after_losing_streak.csv}},
    note = {Dataset}
}
```

## tilt_v12.csv

**Chess: what a loss does to the next game (published estimates).** The effect of a loss, instead of a win, on the next game: score, time spent on early moves, blunders, length, losing on time and playing again; with the placebo and balance checks.

Coverage: Lichess, September 2026; pairs of games in a row against different opponents who met once in the month. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `what` | The outcome in the second game (or the check being run). |
| `group` | all; a speed (bullet, blitz, rapid); or a band of the player's rating. |
| `pairs` | Pairs of games in a row used. |
| `mean` | Mean of the outcome. |
| `first_stage` | Change in the score of the first game per unit of the opponent's hidden strength. |
| `per_unit_of_hidden_strength, se` | Change in the outcome per unit of the first opponent's hidden strength, and its standard error. For scores and percentages, in points per unit (the coefficient times 100). |
| `effect_of_a_loss, effect_se` | What losing the first game, instead of winning it, does to the outcome, and its standard error. Negative means lower after a loss. |
| `losers_minus_winners, losers_minus_winners_se` | The same gap measured naively, without the luck of the draw. It mixes tilt with form. |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- The published estimates (specification 1.2): only pairs in which the player and the first opponent met once in the month.
- Hidden strength: the opponent's results over the month against everyone else, set against the rating they showed in the game. Estimates hold speed and the player's rating (25-point bands) fixed; time outcomes also hold the time control fixed.
- Blunders, mistakes and winning chances come from the tenth of games with a computer analysis, which is not a random tenth.
- The placebo rows should be zero: the following opponent's hidden strength cannot affect the game before it.
- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: what a loss does to the next game (published estimates)" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/tilt_v12.csv

```bibtex
@misc{signumaverage-tilt-v12,
    author = {{Signum Average}},
    title = {Chess: what a loss does to the next game (published estimates)},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/tilt_v12.csv}},
    note = {Dataset}
}
```

## loss_effect.csv

**Chess: the effect of losing a game on the next one (first version, superseded).** The first version of the test (specification 1.1), on all pairs. It was found to be biased by rematches and gives 0.79 points where the published estimate is 1.27 (see tilt_v12.csv and followup.csv). Kept for the record, with its planned splits and placebo.

Coverage: Lichess, September 2026; pairs of games in a row against different opponents. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `split, group` | all; by speed; by rating; by thirds of the time between the two starts; the placebo; and the first version of the specification. |
| `pairs` | Pairs of games in a row. |
| `first_stage, first_stage_se` | Change in the score of the first game per unit of the opponent's hidden strength (both on a 0 to 1 scale). |
| `reduced_form, reduced_form_se` | Change in the excess score of the second game per unit of the first opponent's hidden strength. For the placebo: change in the excess score of a game per unit of the following opponent's hidden strength, which should be zero. |
| `loss_effect_pp, loss_effect_se` | Effect of losing the first game, instead of winning it, on the score in the second, percentage points. Negative means a loss hurts. |
| `loss_gap_no_instrument_pp, loss_gap_no_instrument_se` | The same gap measured naively, without the luck of the draw. It mixes tilt with form. |
| `median_gap_s, median_rest_s` | For the thirds: median seconds between the two starts, and between the end of the first game and the start of the second. |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Hidden strength: the opponent's results over the month against everyone else, set against the rating they showed in the game.
- Standard errors are jackknife over 50 groups of players. Estimates hold speed and the player's rating (25-point bands) fixed.
- The specification was written before any result was computed and changed once, before the full data were built; the first version's estimate is in the rows marked 'specification 1.0'.
- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: the effect of losing a game on the next one (first version, superseded)" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/loss_effect.csv

```bibtex
@misc{signumaverage-loss-effect,
    author = {{Signum Average}},
    title = {Chess: the effect of losing a game on the next one (first version, superseded)},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/loss_effect.csv}},
    note = {Dataset}
}
```

## loss_effect_august.csv

**Chess: the first version of the estimate, August 2026.** The first version of the estimate (specification 1.1) on the second month. Same columns as loss_effect.csv.

Coverage: Lichess, August 2026. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `split, group` | all; by speed; by rating; by thirds of the time between the two starts; the placebo; and the first version of the specification. |
| `pairs` | Pairs of games in a row. |
| `first_stage, first_stage_se` | Change in the score of the first game per unit of the opponent's hidden strength (both on a 0 to 1 scale). |
| `reduced_form, reduced_form_se` | Change in the excess score of the second game per unit of the first opponent's hidden strength. For the placebo: change in the excess score of a game per unit of the following opponent's hidden strength, which should be zero. |
| `loss_effect_pp, loss_effect_se` | Effect of losing the first game, instead of winning it, on the score in the second, percentage points. Negative means a loss hurts. |
| `loss_gap_no_instrument_pp, loss_gap_no_instrument_se` | The same gap measured naively, without the luck of the draw. It mixes tilt with form. |
| `median_gap_s, median_rest_s` | For the thirds: median seconds between the two starts, and between the end of the first game and the start of the second. |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- The first version only. The published version (tilt_v12.csv) has not yet been run on August.
- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: the first version of the estimate, August 2026" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/loss_effect_august.csv

```bibtex
@misc{signumaverage-loss-effect-august,
    author = {{Signum Average}},
    title = {Chess: the first version of the estimate, August 2026},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/loss_effect_august.csv}},
    note = {Dataset}
}
```

## followup.csv

**Chess: balance tests and how the first version failed.** The tests that showed the first version of the estimate was biased by rematches: whether a player's earlier form depends on the hidden strength of the opponent they then met, on all pairs, without immediate rematches, and on pairs who met once in the month; with the main estimate under each.

Coverage: Lichess, September 2026; all pairs, and pairs with rematches left out. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `test` | The outcome or check. |
| `sample` | all: every first game with a hidden-strength opponent and any later game; stay: those in the main estimate. |
| `where` | Restriction: a speed; NOT first_was_rematch (the first game was not against the opponent of the game before); met_n = 1 (the two players met once in the month). |
| `pairs, mean` | Pairs used and the mean of the outcome. |
| `per_unit_of_hidden_strength, se` | Change in the outcome per unit of the first opponent's hidden strength, and its standard error (times 100 for scores and percentages). For a balance test it should be zero. |
| `effect_of_a_loss, effect_se` | What a loss in place of a win does to the outcome, by the luck of the draw. |
| `losers_minus_winners` | The naive gap. |
| `time_control_held_fixed` | Whether the first game's exact time control is held fixed. |
| `note` | What to expect. |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Rows without a restriction reproduce the first version (0.79 points), which failed this test.
- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: balance tests and how the first version failed" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/followup.csv

```bibtex
@misc{signumaverage-followup,
    author = {{Signum Average}},
    title = {Chess: balance tests and how the first version failed},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/followup.csv}},
    note = {Dataset}
}
```

## loss_effect_extras.csv

**Chess: the effect of a loss, checks added after the results.** Estimates that were not in the list fixed in advance: the placebo by speed, and the loss effect by the length of the first game and by the rest between the two games.

Coverage: Lichess, September 2026; pairs of games in a row against different opponents. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `split, group` | placebo by speed; thirds of the length of the first game; thirds of the rest between the end of the first game and the start of the second; and the nine combinations. Thirds are taken within each speed. |
| `pairs` | Pairs of games in a row. |
| `first_stage, first_stage_se` | Change in the score of the first game per unit of the opponent's hidden strength (both on a 0 to 1 scale). |
| `reduced_form, reduced_form_se` | Change in the excess score of the second game per unit of the first opponent's hidden strength. For the placebo: change in the excess score of a game per unit of the following opponent's hidden strength, which should be zero. |
| `loss_effect_pp, loss_effect_se` | Effect of losing the first game, instead of winning it, on the score in the second, percentage points. Negative means a loss hurts. |
| `loss_gap_no_instrument_pp, loss_gap_no_instrument_se` | The same gap measured naively, without the luck of the draw. It mixes tilt with form. |
| `median_first_game_s, median_rest_s` | Median length of the first game and median rest before the second, seconds. |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- These use the first version of the estimate (all pairs).
- Exploratory: these splits were chosen after the main results were seen.
- The split by the length of the first game is not evidence of anything: a game's length depends on the opponent's strength and on the player's own form, so sorting by it creates a pattern.
- Hidden strength: the opponent's results over the month against everyone else, set against the rating they showed in the game.
- Standard errors are jackknife over 50 groups of players. Estimates hold speed and the player's rating (25-point bands) fixed.
- The specification was written before any result was computed and changed once, before the full data were built; the first version's estimate is in the rows marked 'specification 1.0'.
- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: the effect of a loss, checks added after the results" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/loss_effect_extras.csv

```bibtex
@misc{signumaverage-loss-effect-extras,
    author = {{Signum Average}},
    title = {Chess: the effect of a loss, checks added after the results},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/loss_effect_extras.csv}},
    note = {Dataset}
}
```

## luck_of_the_draw.csv

**Chess: results by the hidden strength of the previous opponent.** Pairs of games in a row, sorted into twenty groups by how much better the first opponent was than their rating says.

Coverage: Lichess, September 2026; twenty equal groups of pairs who met once in the month. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `bin` | Group, 1 (opponent weakest for their rating) to 20 (strongest). |
| `pairs` | Pairs of games. |
| `previous_opponent_hidden_strength_pp` | Mean hidden strength of the first opponent, percentage points of score. |
| `previous_score_pct` | Mean score in the first game, %. |
| `previous_excess_score_pp` | Score in the first game minus what the ratings predict, percentage points, measured from the average for the same speed and rating band. |
| `next_excess_score_pp` | The same for the second game, against a different opponent, using the player's rating from before the first game. |
| `next_se_pp` | Standard error of the second game's figure, percentage points. |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: results by the hidden strength of the previous opponent" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/luck_of_the_draw.csv

```bibtex
@misc{signumaverage-luck-of-the-draw,
    author = {{Signum Average}},
    title = {Chess: results by the hidden strength of the previous opponent},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/luck_of_the_draw.csv}},
    note = {Dataset}
}
```

## winner_and_loser.csv

**Chess: who plays again, the winner or the loser.** What the winner and the loser of the same game do next: whether each starts another rated game within 30 minutes, and who starts first.

Coverage: Lichess, September 2026; decisive games. Last updated: 2026-10-07.

| Column | Description |
|---|---|
| `split, group` | all; by speed; or by the loser's losses in a row including this game (1, 2, 3 or more). |
| `games` | Decisive games. |
| `winner_plays_again_pct, loser_plays_again_pct` | Share who start another rated bullet, blitz or rapid game within 30 minutes of the start of this one, %. |
| `difference_se_pp` | Standard error of the gap between the two, percentage points. |
| `both_play_again` | Games after which both players start another. |
| `loser_starts_first_pct` | Among those, share in which the loser's next game starts before the winner's, % (ties left out). |
| `winner_median_wait_s, loser_median_wait_s` | Median seconds between the end of the game and the start of the player's next one. |

Sources:

- Lichess open database, rated standard games, September 2026: https://database.lichess.org/ (CC0)
- Signum Average calculations (CC BY 4.0)

Notes:

- Games from the last hour of the month are left out. Unrated games and chess variants are not in the data, so 'does not play again' means no rated standard game.
- Rated bullet, blitz and rapid games on Lichess in September 2026 (UTC), without games against bots and games that were abandoned.
- Expected score is the average score of all games in the same speed, colour and 25-point band of rating gap, not the textbook Elo formula.
- No player names or game identifiers are published.

How to cite:

Signum Average (2026) - "Chess: who plays again, the winner or the loser" [Dataset] Published online at website.thesignumaverage.workers.dev. Retrieved from: https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/winner_and_loser.csv

```bibtex
@misc{signumaverage-winner-and-loser,
    author = {{Signum Average}},
    title = {Chess: who plays again, the winner or the loser},
    year = {2026},
    howpublished = {\url{https://github.com/thesignumaverage/data/blob/main/2026-10-07_chess-tilt/winner_and_loser.csv}},
    note = {Dataset}
}
```

## Licence

Our compilations and calculations are published under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): you may copy, adapt and republish them for any purpose, as long as you credit Signum Average. Third-party data keeps its original licence.
