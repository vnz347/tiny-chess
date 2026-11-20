# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/vnz347/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/vnz347/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine: 0x88 board, alpha-beta with PVS, quiescence, a
transposition table, null-move pruning, late-move reductions, killer +
history move ordering, and PeSTO-style tapered piece-square tables. It plays
to win fast — mate-distance scoring prefers the quickest mate — on a fixed
node budget, so it is fully deterministic: no wall clock, no unseeded
randomness, every trial replays move-for-move. The single `main.py` is the
whole engine, packed with LZMA; the readable source it was packed from is
`engine.py` (kept out of the repo, sent with the entry bundle).

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 -P -s main.py
```

The engine talks to the make.fun trial env only (`POST /game`, `/move`,
`/resign`) and exits when the trial is over.

---

<sub>Entered on [make.fun](https://make.fun/?ref=qa6gng8g&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
