# Object Explorer 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/object-explorer/overview/

## 概述

**Object Explorer** 是一个搜索和分析工具，用于回答关于 Ontology 中任何内容的问题。

### 核心功能

- **搜索对象**：用户可以通过运行从简单关键词搜索到综合属性过滤的查询来轻松找到感兴趣的对象，所有这些都通过直观的点击式界面完成
- **探索对象集**：从探索视图、结果表格视图或选择特定对象查看其 Object View
- **比较和对比**：比较对象集，对对象集执行批量操作（如写回）
- **跨应用打开**：在兼容的应用程序（如 Quiver）中打开对象集
- **导出数据**：导出对象集
- **保存探索**：保存探索结果，随时重新访问以查看最新结果
- **可视化探索**：探索视图是一组预设和可配置的可视化（如图表或地图），可用于深入挖掘特定对象子集

### 设计特点

- **最小配置**：Object Explorer 需要最少的配置
- **非技术用户友好**：面向非技术用户
- **直观界面**：点按式交互界面

## 主要功能

### 1. 搜索对象

- **全局搜索**：跨所有对象和属性搜索
- **属性过滤**：基于属性值过滤
- **关键词搜索**：简单关键词搜索
- **复杂查询**：综合属性过滤

### 2. 分析和比较

- **结果视图**：以表格形式显示对象
- **图表探索**：使用图表可视化数据
- **过滤结果**：应用过滤器细化结果
- **对象集比较**：比较和对比对象集
- **保存探索**：保存搜索参数和配置

### 3. Actions 应用

- **批量 Actions**：对对象集执行批量操作
- **写回**：批量写回操作
- **参数化输入**：Actions 的参数化输入

### 4. 导出和集成

- **导出对象集**：导出到外部系统
- **兼容应用**：在 Quiver 等兼容应用中打开
- **URL 生成**：生成 Object Explorer URL

## 界面组成

### 搜索界面

- **搜索栏**：全局搜索对象
- **过滤器**：属性过滤器
- **搜索语法**：支持高级搜索语法

### 探索视图

- **可视化图表**：预设和可配置的可视化
- **地图视图**：地理空间探索
- **时间轴**：时间序列探索

### 结果视图

- **表格视图**：对象列表
- **Object View**：单个对象详情
- **分页**：加载更多对象

## 保存探索

**功能**：
- 保存搜索参数
- 保留应用的过滤器
- 保留配置的布局
- 随时重新访问查看最新结果

**用途**：
- 重复分析
- 共享搜索配置
- 标准化报告

## 与其他应用的集成

### Object Views

- 从 Object Explorer 打开单个对象的 Object View
- 查看完整的对象详情

### Quiver

- 在 Quiver 中打开对象集进行深入分析
- 时间序列分析

### Workshop

- 保存的探索可以嵌入 Workshop 模块
- 自定义应用体验

## 配置

Object Explorer 支持各种配置选项：

- **显示/隐藏 Actions**：配置哪些 Actions 显示
- **默认列**：配置结果表格中显示的列
- **权限**：配置访问权限
- **UI 自定义**：配置界面行为

## 使用场景

### 数据探索

- 发现模式
- 理解数据分布
- 识别异常值

### 数据质量

- 检查缺失值
- 验证数据完整性
- 识别数据问题

### 业务分析

- 搜索特定实体
- 比较实体组
- 分析关系

## 性能考虑

- **大型对象集**：处理包含数百万对象的对象集
- **查询优化**：自动优化查询以提高性能
- **分页**：分批加载结果以提高响应速度

## 相关文档

- [Getting started](https://palantir.com/docs/foundry/object-explorer/getting-started/) - 入门指南
- [Search syntax](https://palantir.com/docs/foundry/object-explorer/search-syntax/) - 搜索语法
- [Save explorations](https://palantir.com/docs/foundry/object-explorer/save-explorations/) - 保存探索
- [View results](https://palantir.com/docs/foundry/object-explorer/view-results/) - 查看结果
- [Explore with charts](https://palantir.com/docs/foundry/object-explorer/explore-charts/) - 图表探索
- [Generate URLs](https://palantir.com/docs/foundry/object-explorer/generate-urls/) - 生成 URL

---

*本文档基于 Palantir Foundry 官方文档整理*
