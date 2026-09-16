# 🎲 Rock Paper Scissors: Reproducible Match Simulator

![C++](https://img.shields.io/badge/C%2B%2B-00599C?logo=cplusplus&logoColor=white)

A seeded random simulation of a multi-round match between two players. Because the
random number generator is seeded, any match can be replayed exactly, which is the
same principle that makes larger stochastic simulations reproducible and debuggable.

**Skills shown:** C++ · pseudo-random simulation · reproducibility · input validation

## How it works
1. A user-supplied **seed** initializes the random number generator
2. Each round, both players' moves are generated randomly; ties are re-drawn until
   there's a winner
3. Round results and a final score are printed
4. Invalid round counts (less than 1) are rejected and re-requested

## Example
```
$ ./rps
7 Ana Ben 3
Ana vs Ben for 3 rounds
Tie
Ana wins with scissors
Ben wins with rock
Ana wins with scissors
Ana wins 2 and Ben wins 1
```
Running with seed `7` again produces the identical match.

## Design decisions
- **Named constants** (`ROCK`, `PAPER`, `SCISSORS`) instead of bare numbers make the
  game logic readable
- **Win conditions in a single expression**, so all three winning pairings are
  checked in one place

## Run it
```bash
g++ -o rps "Rock Paper Scissors.cpp"
./rps
```

## What I'd improve next
- Switch from `rand()` to C++11's `<random>` library (e.g., `std::mt19937`) for
  higher-quality randomness
- Add a tally of ties and each player's most-used move
- Refactor move-to-name printing into a helper function to remove duplicated code
