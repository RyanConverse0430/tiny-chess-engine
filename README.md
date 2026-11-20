# Tiny Chess Engine

[![make.fun Tiny Chess](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![Rank](https://make.fun/badge/tiny-chess-01/RyanConverse0430/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![Reward](https://make.fun/badge/tiny-chess-01/RyanConverse0430/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A deterministic Python 3.13 chess engine for the make.fun gauntlet. Its mailbox search uses iterative deepening, principal variation search and a transposition table. The usual budget is 60,000 nodes. Selected opening and opponent combinations use fixed budgets from 16,000 to 96,000 nodes. Quiescence searches captures, promotions and check evasions.

The engine carries opening moves prepared from the public house positions. Selected continuations check the expected house reply each turn. When a line ends or the house chooses another move, the engine searches the supplied legal moves. All preparation runs offline. During play the only service the engine uses is the competition game environment.

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
