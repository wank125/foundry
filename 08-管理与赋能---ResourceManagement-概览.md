# Resource Management 概览

> 来源：https://www.palantir.com/docs/foundry/resource-management/overview/
> 分类：管理与赋能 / 资源管理

## 概述

**Resource Management** 帮助用户了解以下内容：

- 共享 Foundry 计算使用情况
- Foundry 计算使用的成本
- 计费

![Resource Management 应用程序的概览选项卡](https://www.palantir.com/docs/resources/foundry/resource-management/overview.png)

该应用程序针对两个主要工作流程：

- **使用可见性工作流程**：允许用户查看 Foundry 使用资源在其项目中如何使用的概览
- **资源分配工作流程**：允许管理员定义项目应如何消费共享资源，并在需要时对该消费设置限制

## 使用可见性

用户可以使用 Resource Management 中的可见性工具来监控和分析资源使用情况。

在 Foundry 中，所有可以消费自由资源的项目都在项目中创建。这些项目中每个项目的资源使用都归因于其父项目。反过来，项目属于使用账户。

使用账户是一种将有意义的相关项目分组到语义有意义的组中，以便更好地分析和监控使用情况。默认情况下，注册有两个使用账户：

- **default** 账户包含所有常规项目
- **user folders** 账户包含所有用户主文件夹，无法修改

管理员可以自由创建新的使用账户，并以任何有助于他们推理资源消耗的方式对项目进行分类。例如，按部门、业务单位或组织对项目进行分类可能会有帮助。项目的使用账户在项目创建时指定，但管理员可以随时更改。

Foundry 使用根据工作负载或应用程序以不同方式累积。例如，运行数据转换会产生计算成本（执行分布式计算的服务器成本）和存储成本（结果数据的长期存储成本）。

### 概念层次结构

![资源使用的概念层次结构图](https://www.palantir.com/docs/resources/foundry/resource-management/conceptual-hierarchy.png)

---

**核心功能：**

### 配置访问
- 管理员权限配置
- 资源视图控制

### 生态系统
- 项目管理
- 使用账户
- 组织分配

### 使用类型
- 计算使用
- 存储使用
- 网络使用

### 分析工具
- 概览选项卡
- 异常检测
- 预算
- 监视器
- 资源队列
- 业务指标

---

**相关文档导航：**
- Management & enablement（管理与赋能）
  - Resource Management（完整文档）
    - Overview（概览）
    - Configure access（配置访问）
    - Ecosystem（生态系统）
    - Usage types（使用类型）
    - Analysis（分析）
    - Overview tab（概览选项卡）
    - Anomaly detection（异常检测）
    - Budgets（预算）
    - Monitors（监视器）
    - Resource Queues（资源队列）
    - Business metrics（业务指标）
