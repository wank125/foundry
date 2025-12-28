# Dynamic Scheduling 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/dynamic-scheduling/scheduling-overview/

## 概述

**Dynamic Scheduling（动态调度）** 是 Palantir Foundry 的能力，使构建者能够创建调度和资源分配工作流，反映其组织的现实世界复杂性，并根据其特定需求进行定制。

## 核心价值

### 主要功能

| 功能 | 说明 |
|------|------|
| **交互式调度** | 通过拖放界面修改调度 |
| **约束建模** | 对资源和约束进行编码 |
| **推荐引擎** | 基于机器学习的调度推荐 |
| **实时响应** | 实时处理调度变更 |
| **可视化** | 可视化调度和约束 |

### 解决的挑战

动态调度功能可以帮助解决以下挑战：

- **员工调度优化**：平衡优先级和约束，随时间变化优化员工调度
- **运输和物流**：通过机器学习支持的实时解决方案，构建运输和物流网络的弹性
- **制造输出**：通过改进生产计划和调度提高制造输出效率

## 核心原则

动态调度基于三个原则：

```
┌─────────────────────────────────────────────────────────────┐
│           Dynamic Scheduling 核心原则                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. 利用 Foundry Ontology 建模资源                          │
│     ├── 资源对象                                           │
│     ├── 资源属性                                           │
│     └── 资源关系                                           │
│                                                             │
│  2. 对资源的条件和约束进行编码                              │
│     ├── 约束规则                                           │
│     ├── 验证规则                                           │
│     └── 条件逻辑                                           │
│                                                             │
│  3. 建模资源与约束之间的关系和相互依赖性                    │
│     ├── 关系映射                                           │
│     ├── 依赖关系                                           │
│     └── 影响分析                                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## Workshop 集成

### Scheduling Gantt Chart Widget

Workshop 中的 Scheduling Gantt Chart 小部件允许构建交互式调度应用，用户可以：

```
┌─────────────────────────────────────────────────────────────┐
│         Scheduling Gantt Chart Widget 功能                   │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  可视化                                                      │
│  ├── 可视化调度和约束                                       │
│  ├── 显示时间线                                            │
│  └── 显示资源分配                                          │
│                                                             │
│  交互                                                        │
│  ├── 拖放界面修改调度                                      │
│  ├── 调整时间范围                                          │
│  └── 重新分配资源                                          │
│                                                             │
│  推荐                                                        │
│  ├── 查找调度推荐                                          │
│  ├── 应用建议                                              │
│  └── 优化方案                                              │
│                                                             │
│  执行                                                        │
│  ├── 执行 Ontology Actions                                 │
│  ├── 更新调度对象                                          │
│  └── 触发工作流                                            │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Scheduling Calendar Widget

日历小部件提供：

- 日历视图的调度
- 月份/周/日视图
- 交互式编辑

## 核心概念

### 1. Schedule Object（调度对象）

**定义**：调度对象是 Ontology 对任务或活动的表示。

**属性**：
- 开始时间
- 结束时间
- 分配的资源
- 约束条件

### 2. Resource Modeling（资源建模）

**功能**：
- 使用 Ontology 对象建模资源
- 定义资源属性
- 建立资源关系

### 3. Constraints（约束）

**类型**：
- **时间约束**：开始/结束时间限制
- **资源约束**：资源可用性限制
- **顺序约束**：任务执行顺序
- **容量约束**：资源容量限制

### 4. Validation Rules（验证规则）

**功能**：
- 检查调度是否连续
- 检查调度是否重叠
- 验证人员分配
- 验证约束满足

## 主要功能

### 1. Schedule Layer Styling

**功能**：
- 自定义调度层外观
- 颜色编码
- 图标和标签

### 2. Suggestion Functions

**功能**：
- 提供调度建议
- 优化资源分配
- 解决约束冲突

### 3. Search Functions

**功能**：
- 搜索可用资源
- 查找调度间隙
- 发现优化机会

### 4. Validation Rules

**检查项**：
- 调度是否连续（无间隙）
- 调度是否重叠
- 分配的人员具有必要技能
- 约束是否满足

### 5. Inline Metrics

**功能**：
- 实时指标显示
- 性能监控
- 利用率跟踪

## 交互功能

### Row-level Interactions（行级交互）

**功能**：
- 触发 Actions 和事件
- 行级操作
- 上下文菜单

### Schedule Layer-level Interactions（调度层级交互）

**Drag to Create**：
- 拖动创建新调度
- 自动设置时间范围
- 智能资源分配

**Drag and Drop**：
- 拖放移动调度
- 自动重新计算
- 约束验证

## 使用场景

### 1. 员工调度

**场景**：优化员工排班

**功能**：
- 平衡工作负载
- 考虑技能匹配
- 处理请假和可用性
- 实时调整

### 2. 运输和物流

**场景**：车辆和路线调度

**功能**：
- 车辆分配
- 路线优化
- 实时重路由
- 容量管理

### 3. 制造计划

**场景**：生产计划和调度

**功能**：
- 机器分配
- 生产顺序
- 维护计划
- 产能优化

### 4. 项目管理

**场景**：项目和任务调度

**功能**：
- 任务分配
- 依赖管理
- 里程碑跟踪
- 资源平衡

## 工作流程

### 典型工作流

```
┌─────────────────────────────────────────────────────────────┐
│         Dynamic Scheduling 工作流程                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. 定义 Ontology                                           │
│     ├── 创建调度对象类型                                   │
│     ├── 创建资源对象类型                                   │
│     └── 定义关系                                           │
│     ↓                                                        │
│  2. 配置约束                                                │
│     ├── 定义时间约束                                       │
│     ├── 定义资源约束                                       │
│     └── 定义验证规则                                       │
│     ↓                                                        │
│  3. 构建应用                                                │
│     ├── 添加 Scheduling Gantt Chart                         │
│     ├── 配置调度层                                         │
│     └── 设置交互                                           │
│     ↓                                                        │
│  4. 实现推荐                                                │
│     ├── 创建 Suggestion Functions                          │
│     ├── 配置 Search Functions                              │
│     └── 实现优化逻辑                                       │
│     ↓                                                        │
│  5. 部署和使用                                              │
│     ├── 用户交互                                           │
│     ├── 实时调整                                           │
│     └── 执行 Actions                                       │
│     ↓                                                        │
│  6. 监控和优化                                              │
│     ├── 监控指标                                           │
│     ├── 收集反馈                                           │
│     └── 持续改进                                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 最佳实践

### 1. Ontology 设计

- **清晰对象模型**：设计清晰的对象模型
- **适当属性**：定义适当的属性
- **关系映射**：正确映射关系

### 2. 约束管理

- **简单约束**：从简单约束开始
- **优先级**：设置约束优先级
- **验证**：充分验证约束

### 3. 用户体验

- **直观界面**：创建直观的用户界面
- **即时反馈**：提供即时反馈
- **错误处理**：优雅处理错误

### 4. 性能优化

- **增量更新**：使用增量更新
- **缓存**：缓存推荐结果
- **异步处理**：异步处理复杂计算

## 与其他功能集成

### Ontology

- **对象类型**：使用 Ontology 对象类型
- **链接**：使用链接类型建模关系
- **Actions**：执行 Actions 更新调度

### Foundry Rules

- **规则配置**：使用 Foundry Rules 配置约束
- **验证**：使用规则验证调度
- **工作流**：配置调度工作流

### Functions

- **Suggestion Functions**：实现推荐逻辑
- **Search Functions**：实现搜索逻辑
- **验证函数**：实现自定义验证

### Workshop

- **Gantt Chart**：使用 Gantt Chart 小部件
- **Calendar**：使用 Calendar 小部件
- **交互**：配置用户交互

## 入门指南

### 开始使用

1. **学习核心概念**：了解 Dynamic Scheduling 核心概念
2. **定义 Ontology**：创建调度和资源对象类型
3. **配置约束**：使用 Foundry Rules 配置约束
4. **构建应用**：使用 Workshop 构建应用
5. **实现功能**：实现 Suggestion 和 Search Functions
6. **测试和部署**：测试并部署应用

## 限制

### 当前限制

- **复杂度**：复杂的调度规则可能需要更多配置
- **性能**：大型调度可能影响性能
- **实时性**：实时更新取决于数据源

## 相关文档

- [Getting started](https://palantir.com/docs/foundry/dynamic-scheduling/scheduling-getting-started/) - 入门指南
- [Core concepts](https://palantir.com/docs/foundry/dynamic-scheduling/scheduling-concepts/) - 核心概念
- [Scheduling Gantt Chart widget](https://palantir.com/docs/foundry/dynamic-scheduling/scheduling-gantt-chart/) - Gantt Chart 小部件
- [Scheduling Calendar widget](https://palantir.com/docs/foundry/dynamic-scheduling/scheduling-calendar/) - Calendar 小部件
- [Suggestion Functions](https://palantir.com/docs/foundry/dynamic-scheduling/suggestion-functions/) - Suggestion Functions
- [Search Functions](https://palantir.com/docs/foundry/dynamic-scheduling/search-functions/) - Search Functions
- [Validation rules](https://palantir.com/docs/foundry/dynamic-scheduling/scheduling-validation-rules/) - 验证规则

---

*本文档基于 Palantir Foundry 官方文档整理*
