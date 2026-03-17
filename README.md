<div align="center">
  <a href="./README_en.md">English</a> | 简体中文
</div>

# CS61A - The Game of Hog (计算机科学基础实验项目)

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python)
![CS61A](https://img.shields.io/badge/Course-UC_Berkeley_CS61A-yellow?style=flat-square)

本项目来源于加州大学伯克利分校 (UC Berkeley) 入门级计算机科学核心课程 CS61A 的首个大作业。通过实现 Hog 游戏的完整逻辑及其自动化博弈策略，本项目深入实践了 Python 环境下的高阶函数应用、控制流抽象以及基于概率统计的决策优化。

## 核心技术实践

### 1. 函数式编程范式 (Functional Programming)
- **高阶函数组合**: 深度应用函数作为“一等公民”的特性，构建了复杂的逻辑闭包与动态规则引擎。
- **纯函数设计**: 确保博弈规则计算的幂等性，便于进行大规模的并行策略仿真。

### 2. 博弈策略与启发式决策
- **自动决策系统**: 开发能够根据当前比分反馈实时调整投掷数量的策略函数，追求长期期望收益的最大化。
- **蒙特卡洛仿真**: 构建百万次量级的模拟对局引擎，通过统计学方法验证不同博弈策略在实际对抗中的获胜概率与鲁棒性。

### 3. 工程化评测体系
- **单元测试驱动**: 基于 OK Autograder 框架，对博弈逻辑中的边界情况（如 "Sow Sad", "Pig Tail" 等特殊规则）进行精确校验。

## 项目结构分析

```text
cs616161/
├── hog.py          # 游戏核心逻辑、规则实现与启发式博弈策略开发
├── dice.py         # 包含确定性与随机性逻辑的骰子模拟器实现
├── hog_gui.py      # 用于策略调试的可视化图形交互界面模块
├── tests/          # 覆盖全量规则的自动化单元测试集
└── README.md       # 项目技术规范与工程说明文档
```

## 运行与验证

### 自动化逻辑校验
```bash
# 执行特定模块的正确性验证
python3 ok -q 01
```

### 交互式博弈调试
```bash
# 启动图形化界面进行策略对战模拟
python3 hog_gui.py
```

## 许可证
本项目遵循 MIT License 协议。
