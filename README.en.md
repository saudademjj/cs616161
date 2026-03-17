# CS61A Hog Implementation

[中文说明](./README.md)

This repository contains an implementation of the UC Berkeley CS61A `Hog` project, with the core logic stored in `hog.py`. It is useful as a course review artifact, a Python rules-engine exercise, and a reference for strategy-based simulation code.

## Covered Topics

- Dice simulation and turn scoring: `roll_dice`, `take_turn`
- Game rule logic: `boar_brawl`, `sus_points`, `sus_update`
- Full gameplay simulation: `play`
- Strategy helpers: `always_roll`, `catch_up`, `boar_strategy`, `sus_strategy`
- Statistics helpers: `make_averaged`, `max_scoring_num_rolls`, `average_win_rate`

## Requirements

`hog.py` depends on the course support files:

- `dice.py`
- `ucb.py`

To run this project outside the official course scaffold, place those files in the same directory or another importable path.

## Run

```bash
git clone https://github.com/saudademjj/cs616161.git
cd cs616161
python3 hog.py -r
```

The `-r` flag triggers `run_experiments()` and prints strategy comparison results.

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE).
