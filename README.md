# Odds

Prematch odds from fon.bet and 1xbet, collected every evening for the next day (00:00 to 24:00 Tallinn time).

`<day>/<bookmaker>.json`, e.g. `2026-11-14/1xbet.json`:

- `events`: the matches, each with `sport`, `league`, `home`, `away`, `start` (UTC), `fetched_at` (when its odds came
  in) and `odds`: rows of `[market, outcome, line, odds]`
- `market`: `1x2`, `double_chance`, `total`, `both_score`, `home_total`, `away_total`, `winner_incl_ot` (with
  overtime and shootouts), `1x2_regular_time`
- `outcome`: `1`, `X`, `2`, `1X`, `12`, `X2`, `over`, `under`, `yes`, `no`
- `line`: the total's line, or null
