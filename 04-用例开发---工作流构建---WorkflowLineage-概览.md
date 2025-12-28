# Workflow Lineage 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/workflow-lineage/overview/

## 概述

**Workflow Lineage**（前身为 Workflow Builder）是一个交互式工作区，用于理解和管理应用程序及其底层流程。

```
┌─────────────────────────────────────────────────────────────┐
│                   Workflow Lineage                          │
├─────────────────────────────────────────────────────────────┤
│  对象 → Actions → Functions → LLMs → 应用程序               │
│         ↓                                                    │
│   可视化血缘关系                                             │
└─────────────────────────────────────────────────────────────┘
```

## 核心功能

### 1. 探索工作流

探索工作流以查看详细信息：

- **对象（Objects）**：对象类型和实例
- **Actions**：Action 类型和配置
- **Functions**：函数版本和代码
- **大语言模型（LLMs）**：AI 模型集成
- **应用程序**：Workshop 和 Slate 应用

**详细信息包括**：
- API 名称
- 输入参数
- Ontology 编辑
- 提交标准
- 代码片段

### 2. 使用分析

对于对象中的特定列，查看所有下游使用情况：
- 依赖的 Actions
- Workshop 应用
- Slate 应用
- 其他依赖项

### 3. 颜色图例

使用颜色图例轻松查看：
- 过期的 Functions
- 资源权限问题
- Ontology 权限问题
- 应用视图问题

### 4. 批量更新

批量选择 Actions 以同时更新到特定版本：
- 选择多个 Actions
- 更新到相同版本
- 保存更改

## 目标用户

### 应用构建者

创建、调试或维护工作流的应用构建者：

**用途**：
- 血缘图：了解数据流
- 深度属性血缘：跟踪属性如何被使用
- Workshop 小部件/变量血缘：理解 UI 依赖关系
- 升级工具：更新 Functions 和 Actions

### 新构建者

希望从现有工作流中学习的新构建者：

**用途**：
- 回答问题："此工作流使用了 Ontology 的哪些部分，以及如何使用？"
- 学习最佳实践
- 理解现有架构

### 演示者

向他人展示现有工作流的用户：

**用途**：
- 高层次概述
- 演示和教学工具
- 分享工作流

## 与其他工具的关系

Workflow Lineage 与其他 Foundry 工具互补：

```
┌─────────────────────────────────────────────────────────────┐
│                    Foundry 工具链                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Pipeline Builder → 数据集成到 Ontology                     │
│       ↓                                                     │
│  Workflow Lineage → 管理 Ontology 上的工作流                │
│       ↓                                                     │
│  Data Lineage → 数据从源头到工作流的端到端视图              │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Pipeline Builder

- **用途**：将原始数据源集成到 Ontology
- **关系**：Workflow Lineage 构建在 Pipeline Builder 创建的数据基础之上

### Data Lineage

- **用途**：端到端的数据流视图
- **关系**：提供从源头到 Ontology 再到工作流的完整数据流
- **集成**：可以在 Workflow Lineage 中右键单击并在 Data Lineage 中打开

### Workshop & Slate

- **用途**：构建用户应用程序
- **关系**：Workflow Lineage 显示应用程序如何使用 Ontology 资源

## 启用 Workflow Lineage

要启用 Workflow Lineage，请联系平台管理员在 **Control Panel** 中修改应用程序访问权限。

## 主要功能

### 1. 血缘可视化

- **图形视图**：可视化的血缘图
- **依赖关系**：清晰的依赖关系显示
- **流向**：数据和控制流向

### 2. 资源详情

- **对象类型**：查看对象类型定义
- **属性**：查看属性详情
- **链接类型**：查看对象之间的关系
- **Functions**：查看函数代码和版本

### 3. 应用集成

- **Workshop**：查看 Workshop 应用如何使用资源
- **Slate**：查看 Slate 应用依赖关系
- **Functions**：查看函数调用关系

### 4. 版本管理

- **函数版本**：查看不同函数版本
- **更新工具**：批量更新函数版本
- **兼容性检查**：检查版本兼容性

## 使用场景

### 调试工作流

- **问题识别**：快速识别问题根源
- **影响分析**：了解更改的影响范围
- **修复验证**：验证修复是否有效

### 升级和维护

- **版本升级**：升级 Functions 和 Actions
- **依赖检查**：检查依赖关系
- **兼容性验证**：验证更改的兼容性

### 文档和培训

- **工作流文档**：可视化工作流文档
- **培训材料**：用于培训的材料
- **知识共享**：与团队共享知识

## 最佳实践

### 命名约定

- 使用一致的命名约定
- 描述性的名称
- 包含版本信息

### 文档

- 记录关键决策
- 记录业务逻辑
- 记录依赖关系

### 维护

- 定期审查工作流
- 更新过期资源
- 优化依赖关系

## 相关文档

- [Getting started](https://palantir.com/docs/foundry/workflow-lineage/getting-started/) - 入门指南
- [Perform refactors](https://palantir.com/docs/foundry/workflow-lineage/refactor-and-understand-workflows/) - 重构和理解工作流
- [AIP usage metrics](https://palantir.com/docs/foundry/workflow-lineage/aip-metrics/) - AIP 使用指标
- [Manage security](https://palantir.com/docs/foundry/workflow-lineage/manage-security/) - 安全管理
- [Keyboard shortcuts](https://palantir.com/docs/foundry/workflow-lineage/keyboard-shortcuts/) - 键盘快捷键

---

*本文档基于 Palantir Foundry 官方文档整理*
