# CS61A - The Game of Hog (伯克利 CS61A 实验项目 / UC Berkeley CS61A Lab Project)

本项目来源于 UC Berkeley 经典入门课程 CS61A 的第一个大作业。通过 Python 深入探索函数式编程范式与高阶函数的应用逻辑。

This project originates from the first major assignment of UC Berkeley's classic introductory course, CS61A. It deeply explores the functional programming paradigm and the application logic of higher-order functions through Python.

## 核心实践 / Core Practices

- 高阶函数应用 (Higher-Order Functions):
    - 实践函数作为一等公民的传递与返回。 / Passing and returning functions as first-class citizens.
    - 构建复杂的逻辑闭包。 / Building complex logical closures.

- 博弈策略模拟 (Strategy Simulation):
    - 开发能够根据比分反馈自动决策的策略函数。 / Developing strategy functions that make automated decisions based on score feedback.
    - 实现最大期望值策略 (Always Roll n)。 / Implementing expected value maximization strategies.

- 概率期望计算 (Probability & Expectation):
    - 通过万次仿真实验分析不同策略的获胜概率。 / Analyzing win probabilities via massive simulation runs.

## 项目结构 / Project Structure

```text
cs616161/
├── hog.py          # 核心游戏引擎与策略逻辑 / Core engine and strategies
├── dice.py         # 随机骰子生成器 / Randomized dice generator
└── tests/          # 基于 OK 系统构建的单元测试集 / OK autograder tests
```

## 运行方式 / Running

### 1. 运行测试 / Run Tests
```bash
python3 ok -q 01
```

### 2. 图形化对战 / GUI Mode
```bash
python3 hog_gui.py
```

## 许可证 / License
本项目采用 [MIT License](LICENSE) 协议。 / This project is licensed under the MIT License.
