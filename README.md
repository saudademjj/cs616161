# CS61A - The Game of Hog (计算机科学实验项目)

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![Course](https://img.shields.io/badge/Course-CS61A-yellow)](https://cs61a.org/)

本项目源自加州大学伯克利分校 (UC Berkeley) 入门课程 CS61A。通过实现 Hog 游戏的完整逻辑，本项目重点练习了 Python 中的高阶函数应用、控制流管理以及简单的策略模拟。

## 项目内容

- 游戏引擎: 实现基于特定规则的掷骰子系统，包含多个趣味性特殊规则。
- 自动化策略: 编写策略函数，根据当前分值决定掷骰子数量，以优化获胜概率。
- 概率模拟: 构建模拟程序测试不同策略在多次对局中的实际表现。
- 编程范式: 实践函数式编程中的高阶函数组合与控制流抽象。

## 项目结构

```text
.
├── hog.py          # 核心业务逻辑与策略实现
├── hog_gui.py      # 图形化界面 (External)
├── dice.py         # 骰子模拟器
├── tests/          # 单元测试用例
└── README.md
```

## 运行方式

### 1. 环境要求
Python 3.6+

### 2. 交互式运行
`python3 hog_gui.py`

### 3. 评测系统
`python3 ok -q 01`

## 许可证
MIT License
