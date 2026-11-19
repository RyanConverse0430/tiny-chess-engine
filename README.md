# Tiny Chess Engine

[![make.fun Tiny Chess](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![Rank](https://make.fun/badge/tiny-chess-01/RyanConverse0430/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![Reward](https://make.fun/badge/tiny-chess-01/RyanConverse0430/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A Python 3.13 chess engine for the make.fun gauntlet. It searches legal continuations with bitboards, iterative deepening, alpha-beta pruning and capture search. A fixed node budget and stable move ordering make each move reproducible.

## Run it

With the competition environment serving games at `MAKEFUN_ENV_URL`, run the packed entrypoint using Python's standard library.

```sh
python3 -P -s main.py
```

To play the first practice trial and replay it, run the following from the official competition kit with Docker available.

```sh
node cli/makefun.mjs grade-local --kit . --bot /path/to/tiny-chess-engine --driver docker
```

The engine started from the make.fun Tiny Chess starter and is distributed under the MIT license.
