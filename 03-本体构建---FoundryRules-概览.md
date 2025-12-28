# Foundry Rules 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/foundry-rules/overview/

## 概述

**Foundry Rules**（以前称为 Taurus）使用**点击式低代码界面**使用户能够在 Foundry 中主动管理复杂的业务逻辑。通过 Foundry Rules，用户可以创建规则并将这些规则应用于数据集、对象和时间序列，用于各种用例，例如警报生成或数据分类。

## 核心概念

### Rule（规则）

**规则**是一组**条件**，这些条件组合在一起可以指定数据集中的特定行

### Conditions（条件）

形成规则的条件应用于数据集的列，范围可以从简单过滤器到复杂聚合、连接或其他运算符

```
┌─────────────────────────────────────────────────────────────┐
│                    Foundry Rules 结构                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Rule                                                        │
│  ├── Condition Group 1                                     │
│  │   ├── Simple Filter (e.g., amount > 1000)              │
│  │   └── Complex Aggregation (e.g., avg(price) > threshold) │
│  ├── Condition Group 2 (OR logic)                           │
│  └── Actions/Outputs                                        │
│      ├── Alert generation                                  │
│      ├── Data categorization                               │
│      └── Property updates                                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 主要功能

### 1. 点按式低代码界面

- **可视化规则构建器**：无需编码即可创建复杂规则
- **拖放操作**：直观的拖放界面
- **实时预览**：即时查看规则效果

### 2. 规则类型

#### 简单过滤器

- 列值比较
- 范围检查
- 模式匹配

#### 复杂运算符

- **聚合**：聚合函数（SUM、AVG、COUNT 等）
- **连接**：跨表连接
- **子查询**：嵌套查询

### 3. 规则应用

规则可以应用于：

| 目标 | 说明 |
|------|------|
| **数据集** | 表格数据 |
| **对象** | Ontology 对象 |
| **时间序列** | 时间序列数据 |

## 使用场景

### 1. 反洗钱 (AML)

**用途**：标记可疑交易

**规则示例**：
- 单笔交易超过阈值
- 聚合指标异常（如短时间内多笔大额交易）
- 跨境交易模式

### 2. 设备监控

**用途**：基于传感器数据发出潜在设备降级警报

**规则示例**：
- 温度超过阈值
- 压力异常
- 振动超标

### 3. 队列分组

**用途**：根据规则将实体分类为组或"队列"

**规则示例**：
- 客户细分（高价值、中价值、低价值）
- 产品分类
- 风险评分分组

## 组件架构

### Workflow Configuration Editor

Foundry Rules 使用工作流配置编辑器进行配置：

- **工作流所有者**：自定义 Foundry Rules
- **规则作者**：编写业务规则
- **规则操作**：执行规则结果

### Object Model

- **对象类型**：定义规则应用的对象
- **属性映射**：将规则结果映射到对象属性
- **写回**：将结果写回数据源

### Workshop Application

- **规则配置界面**：在 Workshop 中配置规则
- **规则执行界面**：用户执行规则的界面

### Rule Logic

规则逻辑的三个部分：

1. **Inputs（输入）**：Foundry 规则的数据输入
2. **Logic Blocks（逻辑块）**：规则的业务逻辑
3. **Outputs（输出）**：规则的结果

## 部署和配置

### Deploy Workflow

部署规则工作流：
1. 从侧边栏选择 Foundry Rules 应用
2. 选择 Rule-based data pipeline
3. 配置工作流参数
4. 部署工作流

### Configure Workflow

配置工作流：
1. 访问现有规则
2. 配置规则参数
3. 设置执行计划
4. 配置输出

## 最佳实践

### 1. 规则设计

- **模块化**：将复杂规则分解为更小的部分
- **可重用**：创建可重用的规则组件
- **命名约定**：使用一致的命名约定

### 2. 性能优化

- **索引**：确保适当的索引
- **缓存**：缓存频繁访问的数据
- **批量处理**：批量处理规则执行

### 3. 测试和验证

- **单元测试**：测试单个规则
- **集成测试**：测试规则组合
- **用户验收测试**：与业务用户验证

## 与其他应用集成

### Workshop

- 在 Workshop 应用中嵌入规则配置
- 规则执行界面
- 规则结果可视化

### Automate

- 通过 Automate 触发规则执行
- 基于规则结果执行后续操作
- 定期规则评估

### Object Views

- 在对象视图中显示规则结果
- 规则触发的警报
- 数据分类标签

## 设置和自定义

### 可选功能

- **自定义属性**：添加自定义属性
- **权限**：配置规则编辑权限
- **输出值**：配置允许和默认输出值

### Pipeline 自定义

- **自定义转换**：自定义规则管道
- **性能调优**：优化规则执行性能

## 故障排除

### 常见问题

- 规则不触发
- 性能问题
- 数据不一致

### 调试工具

- 规则预览
- 执行日志
- 性能分析

## 相关文档

- [Core concepts](https://palantir.com/docs/foundry/foundry-rules/core-concepts/) - 核心概念
- [Rule logic](https://palantir.com/docs/foundry/foundry-rules/rule-logic/) - 规则逻辑
- [Deploy workflow](https://palantir.com/docs/foundry/foundry-rules/deploy-workflow/) - 部署工作流
- [Configure workflow](https://palantir.com/docs/foundry/foundry-rules/configure-workflow/) - 配置工作流
- [Troubleshooting](https://palantir.com/docs/foundry/foundry-rules/common-issues/) - 故障排除

---

*本文档基于 Palantir Foundry 官方文档整理*
