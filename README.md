<div align="center">
  <a href="./README_en.md">English</a> | 简体中文
</div>

# CS61A - The Game of Hog (计算机科学基础实验项目)

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python)
![CS61A](https://img.shields.io/badge/Course-UC_Berkeley_CS61A-yellow?style=flat-square)

本项目来源于加州大学伯克利分校 (UC Berkeley) 入门级计算机科学核心课程 **CS61A** 的首个大作业。通过实现 Hog 游戏的完整逻辑及其自动化博弈策略，本项目深入实践了 Python 环境下的高阶函数应用、控制流抽象以及基于概率期望的决策优化。

## 🎲 博弈规则与逻辑实现

Hog 是一个双人掷骰子博弈游戏。玩家通过决策投掷骰子的数量来获取积分，目标是率先达到 100 分。项目中实现了一系列特殊的积分修正规则：
- **Sow Sad**: 如果投掷出的骰子中包含 1，则本轮积分为 1。
- **Pig Tail**: 本轮得分基于对手当前积分的数字特征（特定位置数字差的绝对值加 1）。
- **Square Swine**: 如果得分后的积分是一个完全平方数，则积分自动提升为下一个完全平方数。

## 🧠 核心工程实践

### 1. 函数式编程范式 (Functional Programming)
- **高阶函数组合**: 系统实现了大量返回函数的函数（Higher-Order Functions）。通过动态组合不同的策略函数，实现了博弈逻辑的高度解耦。
- **闭包应用**: 利用 Python 的闭包特性维护博弈状态，避免了全局变量的滥用，增强了代码的可测试性。

### 2. 自动化博弈策略 (Automated Strategy)
- **启发式决策**: 开发了能够根据当前比分反馈实时调整投掷数量的策略函数。
- **期望值最大化 (EV Maximization)**: 编写了基于概率统计的 `final_strategy`。该策略通过计算不同决策下的获胜概率期望，自动选择风险收益比最优的动作。

### 3. 百万级蒙特卡洛仿真
- **仿真引擎**: 构建了高性能的模拟对局引擎。通过进行 1,000,000 次级别的策略对抗实验，获取不同策略的理论获胜率，用于验证启发式算法的鲁棒性。

## 📂 项目结构图

```text
cs616161/
├── hog.py          # 核心游戏引擎、规则定义与自动化策略开发
├── dice.py         # 包含确定性 (Deterministic) 与随机性骰子逻辑的实现
├── hog_gui.py      # 基于原生 Python 实现的图形化策略对战与调试界面
├── tests/          # 基于 OK Autograder 框架的精细化单元测试用例集
└── README.md       # 本文档：包含规则说明与技术细节拆解
```

## 🚀 开发者验证

### 自动化评测
本项目采用伯克利自研的 OK 评测系统进行逻辑校验：
```bash
# 执行特定阶段的正确性校验 (例如阶段 1)
python3 ok -q 01
```

### 交互式运行
```bash
# 启动图形化界面进行手动博弈或策略观察
python3 hog_gui.py
```

## 许可证
本项目采用 MIT License 协议。
