# Pipeline Builder 概览

> 来源：https://www.palantir.com/docs/foundry/pipeline-builder/overview/
> 分类：数据连接与集成

## 概述

Pipeline Builder 是 Foundry 的主要数据集成应用程序。您可以使用 Pipeline Builder 构建数据集成管道，将原始数据源转换为干净的输出，准备好进行进一步分析。

借助 Pipeline Builder 和强大的后端模型，会编码的用户和不会编码的用户可以在管道工作流上协同工作。Pipeline Builder 允许用户通过简化的构建器界面应用数据转换，而不是编写需要冗长健康检查的代码。

Pipeline Builder 使用下一代数据转换后端，专门设计为逻辑创建和执行之间的中介。当用户描述他们想要构建的管道时，后端会编写转换代码并对管道完整性执行检查，识别重构错误并提供解决方案以确保健康的构建。由于后端充当逻辑创建和执行之间的中间层，构建者可以在管道构建之前解决模式问题，并节省以前花费在计算和代码检查上的时间。

![Pipeline 截图](https://www.palantir.com/docs/resources/foundry/pipeline-builder/pipe-overview@2x.png?width=0.50)

## 功能特性

Pipeline Builder 包含专注于全面管道创建、维护和控制的功能。

- **直观的用户界面**：用户使用图形和基于表单的界面编写管道，这些界面提供反馈，包括连接键和列转换建议。
- **类型安全函数**：函数是强类型的，可以立即标记错误，而不是在构建时。
- **严格的输出检查**：如果未满足预期的输出检查，则会阻止构建以避免意外的下游中断。
- **自动构建路径修剪**：Pipeline Builder 将修剪未连接到输出的转换路径，以避免构建中不必要的计算。
- **抽象实现细节**：用户专注于描述他们的端到端管道和所需的输出。构建、同步和其他编排由 Pipeline Builder 后端自动处理。
- **独立的管道逻辑**：Pipeline Builder 可以连接到不同的逻辑执行引擎，包括 Spark、Flink、Azure 实例等。
- **可重用性**：管道逻辑可以轻松提取并用于不同的管道。
- **完整的版本控制**：用户可以单独起草管道、协作处理一个管道，或恢复到以前的版本。
- **流式处理能力**：Pipeline Builder 提供编写以实时延迟执行的管道的能力。此功能在所有 Foundry 环境中都不可用。如果您的工作流需要流式管道的可用性，请联系您的 Palantir 代表。

## 工作流程

Pipeline Builder 遵循以下步骤组成的工作流程，从导入数据到交付健康的构建。

- **输入**：添加新的数据源或添加其他数据集。
- **转换**：转换、连接或合并数据以实现所需的输出。
- **预览**：应用转换后，预览输出。
- **交付**：管道完成后，构建管道输出。
- **输出**：为管道添加对象类型、链接类型或数据集输出。

![Pipeline 流程图](https://www.palantir.com/docs/resources/foundry/pipeline-builder/overview-flowchart@2x.png?width=0.50)

在 Pipeline Builder 图形上可视化时，这些步骤可能如下所示：

![Pipeline 图形示例](https://www.palantir.com/docs/resources/foundry/pipeline-builder/workflow-graph@2x.png?width=0.50)

了解如何创建简单的批处理管道，或了解有关在 Pipeline Builder 中构建和管理管道的核心概念的更多信息。

## 目录

- 概述
  - 功能特性
  - 工作流程

---

**相关文档导航：**
- Data connectivity & integration（数据连接与集成）
  - Overview（概览）
  - Connecting to data（连接数据）
  - What is a data pipeline?（什么是数据管道？）
  - Application reference（应用程序参考）
  - Core concepts（核心概念）
    - Datasets（数据集）
    - Streams（流）
    - Media sets（非结构化数据）
    - Branching（分支）
    - Builds（构建）
    - Schedules（调度）
    - Health checks（健康检查）
    - Virtual tables（虚拟表）
    - Change data capture（变更数据捕获）
    - Views（视图）
