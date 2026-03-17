<a id="readme-top"></a>

# CS61A Hog 项目实现

<p align="right">中文 | <a href="#english-version">English</a></p>

本仓库记录了 UC Berkeley CS61A `Hog` 项目的一份实现，核心代码位于 `hog.py`。它适合作为课程复盘、Python 规则实现练习以及策略函数分析的参考样例。

## 覆盖内容

- 骰子模拟与回合计分：`roll_dice`、`take_turn`
- 游戏规则实现：`boar_brawl`、`sus_points`、`sus_update`
- 对局模拟：`play`
- 策略函数：`always_roll`、`catch_up`、`boar_strategy`、`sus_strategy`
- 统计函数：`make_averaged`、`max_scoring_num_rolls`、`average_win_rate`

## 运行前提

`hog.py` 依赖课程配套文件：

- `dice.py`
- `ucb.py`

如果要在本地单独运行，请先把这些依赖文件放到同目录或 Python 可导入路径中。

## 运行方式

```bash
git clone https://github.com/saudademjj/cs616161.git
cd cs616161
python3 hog.py -r
```

`-r` 会触发 `run_experiments()`，输出策略对比结果。

## 仓库结构

```text
cs616161/
├── hog.py
├── README.md
└── README.en.md
```

## 适合的使用场景

- CS61A 项目复盘
- Python 函数式编程练习
- 策略与概率模拟实验

## 注意事项

- 仓库未包含完整课程测试脚本，例如 `ok` 测试环境
- 如需完整评测，请在 CS61A 官方项目模板中执行对应测试命令

## 许可证

本仓库采用 MIT License，详见 [LICENSE](./LICENSE)。

---

## English Version

<p align="right"><a href="#readme-top">中文</a> | English</p>

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
