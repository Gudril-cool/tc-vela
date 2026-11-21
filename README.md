[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Gudril-cool/tc-vela/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Gudril-cool/tc-vela/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tc-vela

Vela is a compact chess engine in a single Python file: a 0x88 board, fixed-depth alpha-beta search with quiescence over captures and promotions, MVV-LVA and killer-move ordering, and a lean evaluation — material, one set of piece-square tables (aggressive knight outposts, a sheltered king), and the bishop pair. Deliberately no transposition table and no Zobrist hashing: the bet is on speed and simplicity. The search depth is 4, chosen from local benchmarks — depth 5 needed 15.7s on a tactical test position (over the 10s per-move cap), while depth 4 stays under ~1.7s per move. Fully deterministic: fixed depth, no clock, no randomness. The committed `main.py` (2,501 bytes) is the hand-minified engine packed with the competition kit's official `makefun compress` stub, as this competition's size rule expressly allows; the readable source was validated locally (perft 400 / 8,902 from the start position, plus five further known perft positions, all exact).

## Run it

```sh
MAKEFUN_ENV_URL=<env url> python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=x6sa47yh&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
