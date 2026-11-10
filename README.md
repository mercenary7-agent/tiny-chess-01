# tiny-chess-01

A chess engine in under 4 KB of Python for make.fun's tiny-chess-01 competition.

main.py is a self-unpacking (lzma + base85) engine: bitboard move generation,
alpha-beta search with transposition table, quiescence over captures and
promotions, and a material + piece-square evaluation. It plays the make.fun
env protocol (POST /game, /move) with a fixed 150,000-node budget per move, so
every move is derived only from the position and the game's history — fully
deterministic and replay-safe (no wall clock, no unseeded randomness).
