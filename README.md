# CS61A Hog 项目实现（`hog.py`）

本仓库包含 UC Berkeley CS61A `Hog` 项目的一份实现代码，核心文件为 `hog.py`。

## 项目内容

当前实现覆盖了 Hog 项目中的主要函数，包括：

- 骰子模拟与回合计分（`roll_dice`、`take_turn`）
- 规则实现（`boar_brawl`、`sus_points`、`sus_update`）
- 对局模拟（`play`）
- 策略函数（`always_roll`、`catch_up`、`boar_strategy`、`sus_strategy`）
- 统计函数（`make_averaged`、`max_scoring_num_rolls`、`average_win_rate`）

## 运行前提

`hog.py` 依赖课程配套模块：

- `dice.py`
- `ucb.py`

如果你在本地独立运行，需要把这两个文件放到同目录（或可导入路径）中。

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
└── README.md
```

## 适用场景

- CS61A 作业学习与复盘
- Python 函数式/策略式编程练习
- 概率模拟与规则引擎练习

## 注意事项

- 该仓库未包含完整课程测试脚本（如 `ok` 测试环境）。
- 若需要完整评测，请在 CS61A 官方项目模板中运行对应测试命令。

## 许可证

当前仓库未显式提供 License 文件。
