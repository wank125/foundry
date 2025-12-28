# Code Workspaces 概览

> 来源：https://www.palantir.com/docs/foundry/code-workspaces/overview/
> 分类：分析 / 开发环境

## 概述

Code Workspaces 将 JupyterLab®、RStudio® Workbench 和 VS Code 第三方 IDE 引入 Palantir Foundry，使用户能够通过在其偏好的工具上使用 Foundry 本体的高质量数据来提高生产力并加速数据科学和统计工作流。Code Workspaces 容器与 Foundry 生态系统的其余部分原生集成，将熟悉的 IDE 与 Foundry 平台的优势相结合，例如数据安全、分支、构建调度和资源管理。

Code Workspaces 为平台管理员提供了一种易于部署、完全托管、安全且生产就绪的方式，为用户提供 JupyterLab®、RStudio® Workbench 和 VS Code，并内置 Foundry 的数据治理以及符合 FedRAMP、GxP 和其他标准的合规性。通过 Code Workspaces，用户可以安全地连接到现有内部系统，并使用 Foundry 的访问控制和数据许可在数据上构建分析、转换、模型、应用程序或整个工作流。

## 主要功能

Code Workspaces 的主要功能包括：

- **安全性**：Code Workspaces 构建在 Foundry 安全性的核心组件之上，这些组件支撑整个平台，例如强大的权限和细粒度的访问控制。这为 Code Workspaces 中可用的第三方 IDE 提供了 Foundry 的安全模型。例如，在 Foundry 中限制对数据集的访问也会限制 Code Workspaces IDE 的访问，确保跨工具的一致权限。

- **可自定义环境**：Code Workspaces 允许用户定义自定义环境配置文件，并根据需要增加或减少工作区的计算资源。

- **Git 工作流支持**：Code Workspaces 由 Code Repositories 基础设施支持，该基础设施提供行业标准的版本控制功能，如分支、合并和提交历史记录。这些功能使多个用户能够更轻松、更安全地在同一工作区中操作。

- **应用程序**：Code Workspaces 目前支持 Python 应用程序的 Dash ↗ 和 Streamlit ↗，以及 R 应用程序的 Shiny® ↗。用户可以直接在 Code Workspaces 中创建应用程序工作流，并内置 Foundry 的版本控制、分支和数据治理功能。

- **模型集成（测试版）**：用户可以在 Code Workspace 内创建模型资产，并通过建模目标跟踪这些资产。可以从同一工作区创建多个模型。

- **转换/构建集成（实验性）**：Code Workspaces 充当转换的开发环境。在 Code Workspaces 中编写的逻辑可以作为数据转换管道发布，并与 Foundry 的数据集成工具包无缝集成，包括构建、调度、数据沿袭和健康检查。我们支持 R 转换和 Python/Jupyter® 转换。

## 何时使用 Code Workspaces

Foundry 有多种可用于分析或编码目的的应用程序。例如，如果您是分析师，Contour（Foundry 用于数据集分析的点击式低代码界面）可能最适合您。

如果您需要编写大规模数据管道、设置数据连接或处理流数据，其他 Foundry 工具比 Code Workspaces 具有更多功能；对于这些用例，我们分别建议使用 Pipeline Builder、Data Connection 和 Foundry Streaming。

具体来说，Code Workspaces 在单个节点上运行，而其他 Foundry 应用程序利用 Spark 基础设施。因此，我们建议执行大规模数据转换的用户选择 Pipeline Builder 或 Code Repositories 而不是 Code Workspaces。

Code Workspaces 专为构建机器学习模型或熟悉在 JupyterLab® 或 RStudio® Workbench 中工作的用户而设计。

## 了解更多

Code Workspaces 目前支持三种环境：JupyterLab®、RStudio® 和 VS Code

有关 Code Workspaces 的更多信息可以在 FAQ 中找到。

使用此教程开始使用 Code Workspaces。

---

**第三方商标声明：**
- RStudio® 和 Shiny® 是 Posit™ 的商标。
- Jupyter®、JupyterLab® 和 Jupyter® 徽标是 NumFOCUS 的商标或注册商标。
- 所有引用的第三方商标（包括徽标和图标）仍归其各自所有者所有。不暗示任何关联或认可。
