# CS61A - The Game of Hog (计算机科学基础实验项目)

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![Course](https://img.shields.io/badge/Course-CS61A-yellow)](https://cs61a.org/)

本项目源自加州大学伯克利分校 (UC Berkeley) 入门级计算机科学核心课程 CS61A。通过实现 Hog 游戏的完整逻辑，本项目深入探讨了 Python 环境下的高阶函数应用、控制流抽象以及启发式策略模拟等核心工程理念。

## 项目核心实践

- 逻辑驱动引擎: 实现基于特定概率规则的掷骰子博弈系统，包含 Sow Sad, Pig Tail, Square Swine 等多种特殊规则。
- 自动化启发式策略: 开发能够根据动态分值反馈进行决策优化的策略函数，实现博弈收益的最大化期望值。
- 概率仿真测试: 构建百万次量级的模拟对局引擎，通过统计学方法验证不同博弈策略的鲁棒性与获胜期望。
- 函数式编程思维: 深度利用闭环、一阶与高阶函数对复杂的博弈逻辑进行模块化拆解与高度重构。

## 项目结构

```text
.
├── hog.py          # 游戏核心业务逻辑与策略实现
├── hog_gui.py      # 图形化交互界面驱动 (External)
├── dice.py         # 概率化骰子模拟器实现
├── tests/          # 自动化单元测试集
└── README.md
```

## 运行与验证

### 1. 运行环境要求
Python 3.6 或更高版本。

### 2. 交互式游戏运行
```bash
python3 hog_gui.py
```

### 3. 自动化逻辑验证
```bash
python3 ok -q 01  # 针对具体模块执行 OK 评测系统
```

## 核心收获

- 掌握了将底层函数作为逻辑契约进行动态组合的工程方法。
- 学习了如何构建符合工业标准的模块化测试与代码自研框架 (OK System)。
- 实践了基于蒙特卡洛模拟原理的简单决策评估方法。

## 许可证
本项目采用 MIT License 协议。

---
Developed by [saudademjj](https://github.com/saudademjj)
