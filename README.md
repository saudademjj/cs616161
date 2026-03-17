<div align="center">
  <a href="./README.md">简体中文</a> | <a href="./README_en.md">English</a>
</div>

# CS61A - The Game of Hog (计算机科学基础实验项目 / UC Berkeley CS61A Lab)

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python)
![CS61A](https://img.shields.io/badge/Course-UC_Berkeley_CS61A-yellow?style=flat-square)

本项目来源于加州大学伯克利分校 (UC Berkeley) 的计算机科学入门核心课程 CS61A 的首个大作业。通过实现 Hog 游戏的完整引擎与自动化博弈策略，本项目深入实践了函数式编程范式、高阶函数应用以及基于概率仿真的决策优化。

This project originates from the first major assignment of UC Berkeley's introductory computer science course, CS61A. By implementing the complete engine and automated game strategies for the Hog game, this project deeply practices functional programming paradigms, higher-order function applications, and decision optimization based on probability simulation.

## 核心技术实践 / Core Engineering Practices

### 1. 函数式编程范式 (Functional Programming Paradigm)
- **高阶函数组合**: 深度应用函数作为一等公民的特性，构建了复杂的控制流闭包与动态规则引擎。 / Deep application of HOFs to build complex closures and dynamic rule engines.
- **逻辑抽象**: 将游戏规则抽象为可插拔的函数模块，确保了引擎的高度可扩展性。 / Abstracting game rules into pluggable function modules.

### 2. 博弈策略与概率仿真 (Game Strategy & Simulation)
- **启发式决策**: 开发能够根据当前比分实时调整投掷数量的策略函数，追求长期期望值的最大化。 / Heuristic strategies to maximize long-term expected values based on real-time scores.
- **蒙特卡洛仿真**: 构建百万次量级的模拟对局引擎，通过统计学方法验证不同博弈策略的鲁棒性与理论获胜率。 / Million-scale simulations to verify strategy robustness and theoretical win rates.

## 项目结构分析 / Project Structure

```text
cs616161/
├── hog.py          # 核心游戏引擎实现与启发式博弈策略开发 / Core engine & strategies
├── dice.py         # 包含确定性与随机性逻辑的骰子模拟器 / Dice logic simulator
├── hog_gui.py      # 用于本地调试的可视化图形交互界面 (外部驱动) / Visualization GUI
├── tests/          # 基于 OK Autograder 构建的精细化单元测试集 / OK autograder tests
└── README.md       # 项目技术规范说明 / Project technical specification
```

## 运行与验证 / Usage

### 自动化评测 (Autograding)
```bash
# 执行特定的逻辑校验用例 / Run specific logic verification
python3 ok -q 01
```

### 交互式运行 (GUI)
```bash
# 启动图形化界面进行策略调试 / Launch GUI for debugging
python3 hog_gui.py
```

## 许可证 / License
本项目采用 MIT License 协议。 / Licensed under the MIT License.
