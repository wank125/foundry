# Action Types 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/action-types/overview/

## 概述

在 Ontology 中，用户可以通过应用 **Actions** 来更改对象、属性和链接。**Action** 是基于用户定义的逻辑更改一个或多个对象属性的单个事务。Actions 使用户能够处理和管理数据，同时考虑总体目标而不是特定的属性编辑。

**Action type** 是用户可以一次性执行的一组对象、属性值和链接更改的定义。它还包括 Action 提交时发生的副作用行为。

## 示例说明

假设创建一个 `Assign Employee` Action type：

**功能**：定义用户如何更改给定 `Employee` 对象的 `role` 属性值

**配置可能包括**：
- 参数定义：允许用户以标准化形式输入新角色
- 自动链接创建：在 `Employee` 对象和新 `Manager` 对象之间自动创建链接
- 通知副作用：通知旧经理和新经理更改
- 权限验证：确保授权员工（如人力资源部门）可以执行 Action

**使用示例**：
HR 员户可以执行 Action 将 "Melissa Chang" 切换为 "Product Manager" `role`。

## 核心概念

### Action vs Action Type

| 概念 | 说明 |
|------|------|
| **Action** | 单个事务，根据用户定义的逻辑更改一个或多个对象的属性 |
| **Action type** | Action 的定义，包括可以进行的更改集、参数、提交标准和副作用 |

### 事务性

对对象、属性值和链接的任何更改都将在用户执行 Action 时提交到 Ontology，并反映在所有用户应用程序中。

### 一致性

相同的 Action 逻辑和验证可以在所有面向用户的应用程序中使用，确保对 Ontology 的一致编辑。

### 写回数据集

对象数据与用户编辑合并的最新版本将捕获在对象类型的写回数据集中。

## Action Type 组成部分

### 1. Parameters（参数）

定义 Action 的输入：
- 用户需要提供的值
- 参数类型和验证规则
- 默认值

### 2. Rules（规则）

定义 Action 的逻辑：
- 对象和链接的创建/修改/删除
- 属性值更新
- 条件逻辑

### 3. Submission Criteria（提交标准）

验证 Action 是否可以执行：
- 权限检查
- 数据验证
- 业务规则

### 4. Side Effects（副作用）

Action 提交时发生的额外行为：
- **Notifications**：发送通知给用户
- **Webhooks**：向外部系统发送数据
- **其他效果**：自定义副作用行为

## Action Types 类型

### 1. Simple Rules Actions

使用简单规则定义：
- 创建、修改、删除对象
- 创建和删除对象之间的链接
- 适用于大多数常见场景

### 2. Function-Backed Actions

使用 TypeScript/Python 函数支持：
- 复杂业务逻辑
- 外部 API 调用
- 高级验证

### 3. Actions on Interfaces

创建适用于接口的所有对象的通用 Action：
- 跨多个对象类型的复用
- 接口级别的操作定义

### 4. Actions on Structs

对结构类型执行 Action：
- 复杂数据结构的操作

## 应用中的 Actions

Actions 可以在整个 Foundry 平台中的应用程序中使用：

### Object Explorer
- 应用预定义的 Actions
- 参数化输入
- 批量执行

### Workshop
- 集成 Action 小部件
- 自定义 Action 触发方式
- 场景支持

### Object Views
- 对象详情页面中的 Action
- 内联编辑
- 面板 Actions

### Slate
- 自定义 Action 触发
- 事件驱动的 Actions

## 权限

Action type 的能力取决于其编辑的对象类型和链接类型的配置：

- **对象权限**：用户对对象类型的权限
- **链接权限**：用户对链接类型的权限
- **Action 特定权限**：可以为 Action 类型配置特定权限

## 监控和日志

### Action Log
- 将所有 Action 提交建模为对象类型
- 可在对象感知的 Foundry 工具中分析和显示
- 完整的审计追踪

### Action Metrics
- 执行统计
- 性能指标
- 使用情况分析

## 撤销和恢复

- **Undo Actions**：撤销最近的 Action
- **Revert Actions**：恢复到以前的状态

## 配置部分

可以为 Action types 配置不同的部分以组织用户界面：
- 自定义表单布局
- 分组相关参数
- 条件显示部分

## 媒体上传

Action types 支持：
- **Upload media**：将媒体文件附加到对象
- **Upload attachments**：上传文档和其他附件

## 规模和属性限制

- 对象和链接的规模限制
- 属性数量限制
- 性能考虑因素

## 内联编辑

支持对象的内联编辑：
- 快速编辑属性
- 即时验证
- 简化的用户界面

## 相关文档

- [Getting started with Action types](https://palantir.com/docs/foundry/action-types/getting-started/) - 入门指南
- [Rules](https://palantir.com/docs/foundry/action-types/rules/) - 规则详解
- [Parameters](https://palantir.com/docs/foundry/action-types/parameters/) - 参数配置
- [Function-backed actions](https://palantir.com/docs/foundry/action-types/function-actions-overview/) - 函数支持的 Actions
- [Side effects](https://palantir.com/docs/foundry/action-types/side-effects-overview/) - 副作用配置

---

*本文档基于 Palantir Foundry 官方文档整理*
