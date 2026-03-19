<div align="center">
  English | <a href="./README.md">简体中文</a>
</div>

# CS61 Hog -- Dice Game Strategy & Monte Carlo Simulation

![Python](https://img.shields.io/badge/Python-3-3776AB?style=flat-square&logo=python)
![Functional](https://img.shields.io/badge/Paradigm-Functional-blueviolet?style=flat-square)
![Monte Carlo](https://img.shields.io/badge/Simulation-Monte_Carlo-orange?style=flat-square)

Hog is a two-player dice game strategy project originating from the UC Berkeley CS61 course series. Players decide how many dice to roll each turn to accumulate points, with the goal of being the first to reach 100. Beyond implementing a complete game engine, the project deeply explores functional programming paradigms, automated game strategy design, and million-scale Monte Carlo simulation validation.

## Game Rules

The game includes the following special scoring rules that add rich strategic dimensions:

### Sow Sad
If any die rolled in a turn shows a 1, the turn score is forced to 1 regardless of other dice values. This rule penalizes greedy strategies -- the more dice rolled, the higher the probability of triggering this rule.

### Pig Tail
Triggered when a player chooses to roll 0 dice. The turn score is calculated based on digit characteristics of the opponent's current score: the absolute difference of digits at specific positions plus 1. This provides a deterministic guaranteed return for "not rolling."

### Square Swine
If the cumulative score after a turn is a perfect square (e.g., 1, 4, 9, 16, 25...), the score automatically promotes to the next perfect square. This rule introduces the concept of "landing on targets" -- precisely controlling scores to land on perfect squares yields bonus jumps.

## Core Engineering Practices

### 1. Functional Programming Paradigm

The project extensively employs functional programming concepts, serving as an excellent practice ground for Python higher-order functions and closures:

- Higher-Order Function Composition: The system implements numerous "functions that return functions." By dynamically composing different strategy functions, game logic achieves a high degree of decoupling. For example, dice generators, turn processors, and strategy selectors all use functions as both parameters and return values
- Closure Application: Python closures maintain game state (current scores, turn counts, etc.), avoiding global variable abuse. Each strategy function captures its runtime environment through closures, enhancing testability and composability
- Pure Function Design: Core game logic is designed as side-effect-free pure functions wherever possible, facilitating unit testing and formal verification

### 2. Automated Game Strategy

The project implements a multi-layered automated decision system:

- Heuristic Decision Making: Strategy functions that adjust the number of dice rolled in real-time based on both players' current scores. Strategies comprehensively consider score differentials, probabilities of triggering special rules, and risk-reward ratios
- EV Maximization: A `final_strategy` based on probability statistics that calculates win probability expectations for different decisions (rolling 0-10 dice) and automatically selects the action with the optimal risk-reward ratio
- Opponent Modeling: Strategy design accounts for possible opponent behavior patterns, implementing basic game-theoretic adversarial logic

### 3. Million-Scale Monte Carlo Simulation

- Simulation Engine: A high-performance match simulator supporting automated confrontation between any two strategy functions
- Large-Scale Experiments: Executing 1,000,000+ strategy confrontation experiments to obtain theoretical win rates for different strategies
- Robustness Validation: Using statistical significance tests to verify stable performance of heuristic algorithms against various opponent strategies
- Strategy Iteration: Repeatedly tuning strategy parameters based on simulation results, approaching theoretically optimal solutions

## Directory Structure

```text
cs616161/
├── hog.py          # Core game engine: rule definitions, turn processing, strategy development, EV calculation
├── dice.py         # Dice logic: deterministic dice (for testing) and randomized dice implementations
├── hog_gui.py      # GUI: native Python visual strategy battle and debugging tool
├── tests/          # Test suite: granular unit test cases built on the OK Autograder framework
└── README.md       # Project documentation
```

## Usage

### Prerequisites

- Python >= 3.6

### Automated Verification

The project uses UC Berkeley's OK autograder system for logic verification:

```bash
# Verify correctness of a specific phase (e.g., Phase 1)
python3 ok -q 01

# Verify all phases
python3 ok

# View detailed test output
python3 ok -v
```

### Interactive Execution

```bash
# Launch the GUI for manual play or strategy observation
python3 hog_gui.py
```

### Strategy Simulation

Run Monte Carlo simulations in a Python interactive environment:

```python
from hog import *

# Run 1 million match simulations comparing two strategies' win rates
win_rate = average_win_rate(final_strategy, baseline_strategy)
print(f"Final strategy win rate: {win_rate:.4f}")
```

## Technical Highlights

- Pure Functional Architecture: The entire game engine is built on higher-order functions and closures with no class definitions, showcasing the expressiveness of Python's functional programming capabilities
- Probability-Driven Decisions: final_strategy is based on precise probability calculations rather than simple if-else rules, embodying data-driven engineering thinking
- Statistical Verification Loop: Strategy design -> Monte Carlo simulation -> statistical analysis -> parameter tuning, forming a complete experimental verification pipeline
- Composability: Strategy functions can be freely combined like building blocks, enabling rapid experimentation with different decision logic

## License

MIT License
