<div align="center">
  English | <a href="./README.md">简体中文</a>
</div>

# CS61A - The Game of Hog (Foundational Computer Science Lab Project)

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python)
![CS61A](https://img.shields.io/badge/Course-UC_Berkeley_CS61A-yellow?style=flat-square)

This project originates from the first major assignment of UC Berkeley's foundational computer science course, CS61A. By implementing the complete logic of the Hog game and its automated game strategies, this project deeply explores higher-order function applications, control flow abstraction, and decision optimization based on probability and statistics within the Python environment.

## Core Technical Practices

### 1. Functional Programming Paradigm
- **HOF Composition**: Extensive application of functions as "first-class citizens" to build complex logical closures and a dynamic rules engine.
- **Pure Function Design**: Ensures idempotency in game rule calculations, facilitating large-scale parallel strategy simulations.

### 2. Game Strategy & Heuristic Decision Making
- **Automated Decision System**: Development of strategy functions capable of real-time roll-count adjustments based on score feedback, aiming to maximize long-term expected returns.
- **Monte Carlo Simulation**: Construction of a million-scale match simulation engine to verify the win probability and robustness of various game strategies in actual competitive scenarios.

### 3. Engineering Evaluation Framework
- **Unit Test Driven**: Built upon the OK Autograder framework to precisely validate edge cases in game logic (e.g., special rules like "Sow Sad" and "Pig Tail").

## Project Structure

```text
cs616161/
├── hog.py          # Core game logic, rule implementation, and heuristic strategy development
├── dice.py         # Dice simulator implementation including deterministic and randomized logic
├── hog_gui.py      # Visual graphical interface module for strategy debugging
├── tests/          # Automated unit test suite covering all rules
└── README.md       # Project technical specifications and engineering documentation
```

## Usage & Verification

### Automated Logic Verification
```bash
# Verify the correctness of specific modules
python3 ok -q 01
```

### Interactive Game Debugging
```bash
# Launch the graphical interface for strategy battle simulation
python3 hog_gui.py
```

## License
This project is licensed under the MIT License.
