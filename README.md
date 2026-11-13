# Odds

Prematch odds from fon.bet and 1xbet, collected every evening (~21:20 Tallinn time) for the next day, 00:00 to 24:00
Tallinn time, plus the games starting that evening after the collection (`window.from`).

`<day>/<bookmaker>.json`, e.g. `2026-11-14/1xbet.json`:

- `events`: the matches, each with `sport`, `league`, `home`, `away`, `start` (UTC), `fetched_at` (when its odds came
  in) and `odds`: rows of `[market, outcome, line, odds]`
- `home`, `away`: the same spelling in both files (1xbet's); where fon.bet spells a team otherwise, its own name is in
  `site_home`, `site_away`
- `market`: `1x2`, `double_chance`, `total`, `both_score`, `home_total`, `away_total`, `winner_incl_ot` (with
  overtime and shootouts), `1x2_regular_time`
- `outcome`: `1`, `X`, `2`, `1X`, `12`, `X2`, `over`, `under`, `yes`, `no`
- `line`: the total's line, or null
