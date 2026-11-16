# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/saykhulss/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/saykhulss/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

An original 0x88 chess engine in Python, packed into 4,096 bytes.

- Negamax alpha-beta with iterative deepening to a fixed 120,000 nodes/move
- Quiescence search (captures), transposition table, killer + history move ordering
- Evaluation: material + piece-square tables + bishop pair + king pawn shelter
- Deterministic: fixed node budget, no clock, no randomness
- Talks UCI to the env over HTTP (`MAKEFUN_ENV_URL`)

Practice trial (kit trial-0): 2 wins, 1 draw, 3 losses (2.5/6) —
beat depth-2 and nodes-100k (1392) by checkmate, drew depth-3.

`main.py` is the compressed entrypoint (LZMA payload, written by the
kit's `compress` command). `bot/src.py` is the readable source; it is not
committed (it exceeds the repo tree cap) but is bundled with the entry.

## Run it

```sh
python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=9mr28321&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
