# Carbon 概览

> 来源：https://www.palantir.com/docs/foundry/carbon/overview/
> 分类：用例开发 / 工作空间配置

## 概述

**Carbon** 应用程序使您能够为特定用户组配置自定义平台体验，称为工作空间。Carbon 可以为需要执行关键运营工作流程的非技术用户提供专注的体验。

例如，用于飞机零件维护的 Carbon 工作空间可能包括：

- 包含动态更新的需要维护的零件列表的 Workshop 模块
- 一组用于分类每个零件的 Foundry 操作
- 可用于调查每个零件维护问题的模块
- 显示一段时间内维护趋势的 Quiver 分析

管理员可以创建多个针对特定用户配置文件定制的 Carbon 工作空间，并通过强大的权限进行管理。在每个工作空间中，管理员可以突出显示相关的工作流程和应用程序，有选择地隐藏整个平台的复杂性，并在必要时限制在 Carbon 工作空间之外的导航。

Carbon 工作空间具有自定义的着陆页面以及配置的模块集。当通过 Carbon 工作空间访问 Foundry 时，用户将只看到特定工作流程所需的应用程序和资源子集。

![示例 Carbon 工作空间](https://www.palantir.com/docs/resources/foundry/carbon/carbon-workspace.png)

## 访问 Carbon

在 Foundry 中，通过导航到 Applications Portal 并选择 **Carbon 工作空间** 来访问 Carbon。如果您已经创建了 Carbon 工作空间并将其作为可用应用程序推广，您可以在 Application Portal 的 **推广的应用** 部分下搜索工作空间名称。

![从 Application Portal 打开 Carbon](https://www.palantir.com/docs/resources/foundry/carbon/application-portal-carbon.png)

---

**核心功能：**

### 工作空间 (Workspaces)
- 概述
- 创建工作空间
- 编辑工作空间
- 配置工作空间更新
- 查看版本历史
- 配置工作空间之间的导航
- 限制在工作空间之外的导航

### 模块 (Modules)
- 概述
- 配置模块发现
- 配置模块之间的导航

### 权限和访问
- 配置权限
- 设置默认工作空间
- 将 Carbon 设置为 Foundry 着陆页

### 配置参考
- 常规配置
- 主页配置
- 菜单栏配置
- 访问配置
- YAML 配置示例
- YAML 配置参考
- 为组织启用深色模式

---

**相关文档导航：**
- Use case development（用例开发）
  - Carbon（完整文档）
    - Overview（概览）
    - Getting started（入门）
    - Example workspaces（示例工作空间）
    - Workspaces（工作空间）
    - Modules（模块）
    - Permissions and access（权限和访问）
    - Configuration reference（配置参考）
    - Editing with code（使用代码编辑）
