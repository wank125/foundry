# FoundryTS 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/foundryts/overview/

## 概述

**FoundryTS** 是一个用于对时间序列数据运行可扩展查询的 Python 库。FoundryTS 库提供了 Foundry 高效时间序列存储的接口，并使用 Foundry 的 Spark 集群来分布式执行计算。

## 核心价值

### 主要功能

| 功能 | 说明 |
|------|------|
| **可扩展查询** | 对大规模时间序列数据运行查询 |
| **分布式计算** | 使用 Foundry Spark 集群进行分布式计算 |
| **高效存储** | 利用 Foundry 的高效时间序列存储 |
| **Python 接口** | 提供 Python API 接口 |

### 技术特点

- **Spark 集成**：利用 Foundry Spark 集群进行分布式计算
- **高效存储**：直接访问 Foundry 时间序列存储
- **可扩展**：支持大规模时间序列数据查询
- **Python 原生**：纯 Python 库，易于使用

## 核心概念

### 1. 时间序列数据

**定义**：时间序列数据是随时间变化的一系列测量值，通常以规则间隔采集。

**示例**：
- 传感器读数
- 股票价格
- 温度测量
- 设备状态

### 2. FoundryTS API

**API 结构**：

```
┌─────────────────────────────────────────────────────────────┐
│              FoundryTS API 结构                              │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  FoundryTS                                                  │
│  ├── 核心类                                                │
│  │   ├── FoundryTS                                        │
│  │   ├── Interval                                          │
│  │   └── NodeCollection                                    │
│  ├── 函数                                                  │
│  │   ├── 聚合函数                                          │
│  │   │   ├── cumulative_aggregate                         │
│  │   │   ├── periodic_aggregate                           │
│  │   │   ├── rolling_aggregate                            │
│  │   │   └── statistics                                    │
│  │   ├── 转换函数                                          │
│  │   │   ├── derivative                                    │
│  │   │   ├── integral                                      │
│  │   │   ├── interpolate                                   │
│  │   │   ├── time_shift                                    │
│  │   │   └── value_shift                                   │
│  │   ├── 搜索函数                                          │
│  │   │   ├── time_series_search                            │
│  │   │   └── where                                         │
│  │   ├── 回归函数                                          │
│  │   │   ├── linear_regression                             │
│  │   │   ├── exponential_regression                        │
│  │   │   └── polynomial_regression                         │
│  │   └── 其他函数                                          │
│  │       ├── distribution                                  │
│  │       ├── scatter                                       │
│  │       ├── scale                                         │
│  │       └── unit_conversion                               │
│  ├── 节点                                                  │
│  │   ├── FunctionNode                                      │
│  │   └── SummarizerNode                                    │
│  ├── 对象                                                  │
│  │   ├── FoundryObject                                     │
│  │   └── Object                                            │
│  └── 搜索                                                  │
│      ├── Search                                            │
│      ├── Property                                          │
│      └── ontology                                          │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 主要功能

### 1. 查询时间序列

**功能**：
- 直接从时间序列查询数据
- 从附加的本体属性查询时间序列
- 过滤时间序列

### 2. 数据聚合

**聚合函数**：

| 函数 | 说明 |
|------|------|
| `cumulative_aggregate` | 累积聚合 |
| `periodic_aggregate` | 周期聚合 |
| `rolling_aggregate` | 滚动聚合 |
| `statistics` | 统计函数 |
| `sum` | 求和 |
| `mean` | 平均值 |

### 3. 数据转换

**转换函数**：

| 函数 | 说明 |
|------|------|
| `derivative` | 导数（变化率） |
| `integral` | 积分 |
| `interpolate` | 插值 |
| `time_shift` | 时间偏移 |
| `value_shift` | 值偏移 |
| `scale` | 缩放 |

### 4. 搜索功能

**搜索函数**：

| 函数 | 说明 |
|------|------|
| `time_series_search` | 时间序列搜索 |
| `where` | 条件过滤 |
| `points` | 数据点提取 |

### 5. 回归分析

**回归函数**：

| 函数 | 说明 |
|------|------|
| `linear_regression` | 线性回归 |
| `exponential_regression` | 指数回归 |
| `polynomial_regression` | 多项式回归 |

### 6. 分布和散点

**分析函数**：

| 函数 | 说明 |
|------|------|
| `distribution` | 分布分析 |
| `scatter` | 散点图 |

## 使用场景

### 1. 时间序列分析

**场景**：分析传感器数据趋势。

**用法**：
```python
# 查询时间序列
ts = foundryts.FoundryTS()

# 聚合数据
result = ts.cumulative_aggregate(...)

# 转换数据
result = ts.derivative(...)
```

### 2. 异常检测

**场景**：检测时间序列中的异常值。

**用法**：
```python
# 搜索异常
result = foundryts.time_series_search(...)
```

### 3. 预测分析

**场景**：使用回归进行预测。

**用法**：
```python
# 线性回归预测
result = foundryts.linear_regression(...)
```

### 4. 数据清洗

**场景**：插值处理缺失数据。

**用法**：
```python
# 插值
result = foundryts.interpolate(...)
```

## API 参考

### 核心类

#### FoundryTS

主要接口类，提供所有时间序列操作。

#### Interval

表示时间间隔。

#### NodeCollection

节点集合，用于组合多个时间序列操作。

### 主要函数

#### 聚合函数

- `functions.cumulative_aggregate` - 累积聚合
- `functions.periodic_aggregate` - 周期聚合
- `functions.rolling_aggregate` - 滚动聚合
- `functions.statistics` - 统计函数
- `functions.sum` - 求和
- `functions.mean` - 平均值
- `functions.first_point` - 第一个点
- `functions.last_point` - 最后一个点

#### 转换函数

- `functions.derivative` - 导数
- `functions.integral` - 积分
- `functions.interpolate` - 插值
- `functions.time_shift` - 时间偏移
- `functions.value_shift` - 值偏移
- `functions.scale` - 缩放
- `functions.unit_conversion` - 单位转换

#### 搜索函数

- `functions.time_series_search` - 时间序列搜索
- `functions.where` - 条件过滤
- `functions.points` - 数据点
- `functions.time_range` - 时间范围
- `functions.time_extent` - 时间范围

#### 回归函数

- `functions.linear_regression` - 线性回归
- `functions.exponential_regression` - 指数回归
- `functions.polynomial_regression` - 多项式回归

#### 其他函数

- `functions.distribution` - 分布
- `functions.scatter` - 散点
- `functions.series` - 序列
- `functions.skip_nonfinite` - 跳过非有限值
- `functions.udf` - 用户定义函数

### 节点

- `nodes.FunctionNode` - 函数节点
- `nodes.SummarizerNode` - 汇总节点

### 对象

- `objects.FoundryObject` - Foundry 对象
- `objects.Object` - 通用对象

### 搜索

- `search.Search` - 搜索接口
- `search.Property` - 属性搜索
- `search.ontology` - 本体搜索

## 最佳实践

### 1. 查询优化

- **过滤数据**：尽早过滤数据
- **使用聚合**：使用聚合减少数据量
- **利用 Spark**：利用分布式计算

### 2. 代码组织

- **模块化**：模块化代码
- **重用查询**：重用查询逻辑
- **文档记录**：记录查询目的

### 3. 性能考虑

- **批量操作**：批量执行操作
- **避免循环**：避免在 Python 中循环
- **使用原生函数**：使用 FoundryTS 原生函数

## 与 Functions 的兼容性

**重要提示**：FoundryTS 库与 Functions 不兼容。

### 替代方案

在 Functions 中，Python OSDK 提供了访问时间序列数据的替代方法：

- 使用 Python OSDK 访问时间序列
- 通过 Ontology 对象访问时间序列属性
- 使用 Functions 的内置时间序列支持

## 与其他功能集成

### Time Series

- **时间序列目录**：与时间序列目录集成
- **时间序列属性**：访问本体时间序列属性
- **派生序列**：使用派生序列

### Ontology

- **对象属性**：从对象属性访问时间序列
- **对象集**：查询对象集的时间序列
- **链接**：遍历链接访问相关时间序列

### Workshop

- **可视化**：在 Workshop 中可视化查询结果
- **交互**：创建交互式时间序列应用
- **仪表板**：构建时间序列仪表板

## 限制

### 当前限制

- **Functions 不兼容**：不能在 Functions 中使用
- **Python 专用**：仅支持 Python
- **需要时间序列存储**：需要 Foundry 时间序列存储

## 相关文档

- [API Reference](https://palantir.com/docs/foundry/foundryts/api-reference/) - API 参考
- [Time series overview](https://palantir.com/docs/foundry/time-series/time-series-overview/) - 时间序列概述
- [Work with time series in FoundryTS](https://palantir.com/docs/foundry/time-series/foundryts/) - 在 FoundryTS 中使用时间序列
- [Use time series in Functions](https://palantir.com/docs/foundry/time-series/time-series-in-functions/) - 在 Functions 中使用时间序列

---

*本文档基于 Palantir Foundry 官方文档整理*
