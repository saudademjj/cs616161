<div align="center">
  English | <a href="./README.md">简体中文</a>
</div>

# CS61A - The Game of Hog (Foundational Computer Science Lab)

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python)
![CS61A](https://img.shields.io/badge/Course-UC_Berkeley_CS61A-yellow?style=flat-square)

This project originates from the first major assignment of UC Berkeley's **CS61A**, a core introductory computer science course. By implementing the complete engine and automated game strategies for the Hog game, this project deeply explores functional programming paradigms, control flow abstraction, and decision optimization based on probability and expected values.

## 🎲 Game Rules & Logic Implementation

Hog is a two-player dice game. Players compete to reach 100 points first by deciding how many dice to roll each turn. The project implements several special scoring rules:
- **Sow Sad**: If any of the dice rolled are 1, the score for the turn is 1.
- **Pig Tail**: Scoring is based on the digits of the opponent's current score (absolute difference of specific digits plus 1).
- **Square Swine**: If a score resulting from a turn is a perfect square, it is automatically boosted to the next perfect square.

## 🧠 Core Engineering Practices

### 1. Functional Programming Paradigm
- **Higher-Order Function Composition**: Implements numerous functions that return other functions. By dynamically combining different strategy functions, the game logic remains highly decoupled.
- **Closure Usage**: Leverages Python's closures to maintain game states without global variables, enhancing modularity and testability.

### 2. Automated Game Strategy
- **Heuristic Decision Making**: Developed strategy functions that real-time adjust the number of dice rolled based on score feedback.
- **EV Maximization**: Implemented a `final_strategy` based on probability statistics. It calculates the win probability for various actions and chooses the one with the highest expected utility.

### 3. Million-Scale Monte Carlo Simulation
- **Simulation Engine**: Built a high-performance match simulator. By executing 1,000,000+ match iterations, the project gathers theoretical win rates to validate the robustness of different heuristic algorithms.

## 📂 Project Structure

```text
cs616161/
├── hog.py          # Core game engine, rule definitions, and strategy development
├── dice.py         # Implementation of both Deterministic and Randomized dice logic
├── hog_gui.py      # Native Python graphical interface for manual play and strategy debugging
├── tests/          # Granular unit test cases built on the OK Autograder framework
└── README.md       # This document: Rules and technical breakdown
```

## 🚀 Usage

### Automated Verification
Verification is performed via the Berkeley-developed OK system:
```bash
# Verify the correctness of a specific phase (e.g., Phase 1)
python3 ok -q 01
```

### Interactive Execution
```bash
# Launch the GUI for manual play or strategy observation
python3 hog_gui.py
```

## License
MIT License
