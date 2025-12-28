# Data Health 概览

> 来源：https://www.palantir.com/docs/foundry/data-health/overview/
> 分类：数据连接与集成 / 数据治理

## 概述

**Data Health** 是一个 Foundry 服务，用于监控和警报数据集的常见问题。Data Health 附带了针对数据集状态、时间、大小、内容和架构的潜在问题的预构建检查。如果检查失败，Data Health 会发送平台内通知和电子邮件以提醒您注意失败情况。

本文档部分提供了有关 Data Health 中可用选项的详细参考。有关如何设置有效健康检查的高级指导，请尝试阅读维护管道部分。特别是，推荐的健康检查页面可能会有帮助。

![Data Health 概览](https://www.palantir.com/docs/resources/foundry/data-health/overview.png)

## 访问 Data Health

在 Foundry 中有四种方式可以查看健康检查。

### 数据集的健康状况

在数据集预览中查看数据集时，您可以导航到 **Health** 选项卡以添加新检查、修改现有检查并查看历史检查结果。

### 项目范围内的健康状况

在每个 **Project Catalog** 选项卡中，项目维护的第一部分显示应用于项目中任何数据集的所有健康检查，以及有多少检查通过或失败的摘要。

### 管道范围内的健康状况

在数据血缘中，数据集可以按其健康检查状态着色。此外，页面底部的 Data Health 选项卡（在设置中切换）显示血缘图中所有数据集的健康检查及其状态。

### 平台范围内的健康状况

要查看所有数据集的健康检查概览，请从侧边栏选择 **Data Health** 应用程序。在这里，您可以按状态或名称过滤或排序数据集。您还可以切换以仅显示您正在监视的数据集。此页面还允许您通过单击右上角的 **Add health check** 添加新的健康检查。

---

**核心功能：**

### 健康检查类型
- 状态检查
- 时间检查
- 大小检查
- 内容检查
- 架构检查

### 检查管理
- 创建健康检查
- 监视检查
- 检查评估
- 通知和问题
- 检查组

### 集成
- 管道健康检查
- 项目维护
- 数据集预览集成

---

**相关文档导航：**
- Data connectivity & integration（数据连接与集成）
  - Data Health（完整文档）
    - Overview（概览）
    - Builds and checks FAQ（构建和检查常见问题）
    - Health checks（健康检查）
    - Check groups（检查组）
