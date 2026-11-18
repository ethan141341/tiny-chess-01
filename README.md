# Tiny Chess — a 4 KB Python chess engine

![tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)
![rank](https://make.fun/badge/tiny-chess-01/ethan141341/tiny-chess-01/rank.svg)
![reward](https://make.fun/badge/tiny-chess-01/ethan141341/tiny-chess-01/reward.svg)

An original chess engine that fits in 4,096 bytes of Python, written for
the [make.fun](https://make.fun/bounty/tiny-chess-01) bounty
"Build the strongest chess engine in 4 KB of Python".

`main.py` is the whole engine: a negamax alpha-beta search (PVS) with
quiescence, a transposition table, killer/history move ordering, late
move reductions and null-move pruning, plus a tapered material and
piece-square evaluation with pawn-structure terms. It searches to a
fixed node budget — never a clock — so its moves are deterministic.
It plays through the competition env: it reads the brief at
`MAKEFUN_PROMPT_FILE` and plays each game with POST /game and /move
against `MAKEFUN_ENV_URL` until every game is over.

`main.py` is packed from a readable source with `makefun compress`
(LZMA); the source ships with the entry's transcripts at submission.

MIT licensed — see `LICENSE`.
