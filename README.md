# ashare-quant

A股多因子评分卡选股回测系统。

## 定位

用 **多因子 + 逻辑回归评分卡** 预测「中证500 成分股 T+1 日收盘涨幅 > 3%」的概率，输出「分数 → 胜率」的可解释映射，按分数排序选股。

## 协作模式

| 角色 | 职责 |
|---|---|
| 策略分析师（你） | 策略逻辑、标签口径、评估指标、结果解读、拍板 |
| Coder / 执行（Hermes） | 取数、特征工程、建模、回测、出报告 |

## 本地练手（vibe coding）

```bash
git clone https://github.com/LunaticRedMoon/ashare-quant.git
cd ashare-quant
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## 目录结构

```
src/data/       数据获取与清洗（akshare）
src/factors/    因子计算（动量起步）
src/model/      评分卡建模（分箱/WOE/IV/逻辑回归/分数映射）
src/backtest/   回测引擎与评估
docs/           计划文档
data/           本地数据（不入库）
tests/          测试
```

## 进度

见 [docs/plan.md](docs/plan.md)。
