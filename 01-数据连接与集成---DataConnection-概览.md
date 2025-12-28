# Data Connection 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/data-connection/overview/

## 概述

**Data Connection** 是 Foundry 中用于同步外部系统数据的应用程序。用户可以使用 Data Connection 将数据同步到 Foundry，用于数据集成、建模和本体层。此外，Data Connection 还支持设置出站连接，通过 Webhook 和数据导出实现向外部系统的写回。

## 访问方式

Data Connection 应用可以通过以下方式访问：

1. 从工作区导航栏选择 Data Connection 图标
2. 在应用程序门户（Applications Portal）中搜索

## 设计原则

Foundry 通过以下三个原则标准化数据连接过程：

### 1. 健壮性 (Robustness)

- **自动重试**：失败时自动重试
- **小批量处理**：使用简单函数从源系统拉取数据
- **数据健康监控**：集成监控系统，在关键故障时发出警报
- **原样摄取**：数据以最原始的形式摄取，无需外部预处理
- **版本控制管道**：Foundry 管道是原始数据变更的单一来源

### 2. 可扩展性 (Extensibility)

- **开箱即用集成**：支持常见系统类型（关系数据库、FTPS、HDFS、S3、SFTP、本地目录）
- **灵活连接**：支持新系统类型的连接
- **插件复用**：新系统可重用现有插件或稍作修改
- **标准化核心功能**：调度和上传等功能标准化

### 3. 易用性 (Ease of use)

- **简化复杂性**：后端服务承担大部分工作
- **简单前端界面**：用户通过简单的前端 UI 设置和管理管道
- **降低准入门槛**：使更多用户能够执行数据连接

## 核心概念

### Sources（源）

Source 代表与外部系统的单个连接，包括：
- 配置必要的连接信息（通常是 URL）
- 成功认证所需的凭据
- 必须配置特定的 worker 定义计算运行位置

### Workers（工作器）

| Worker 类型 | 说明 | 适用场景 |
|------------|------|----------|
| **Foundry worker** | 默认选项，计算在 Foundry 中运行 | 首选方法，受益于容器化和可扩展的作业执行 |
| **Agent worker** | 高级选项，计算在客户提供的宿主上运行 | 特定文件同步、大型数据过滤或本地系统微批处理 |

### Networking（网络）

**Foundry worker 网络配置**：
- **Direct connection policies**：用于可直接从 Foundry 访问的系统
- **Agent proxy policies**：用于与 Foundry 不同网络中的外部系统（需要代理设置）

**Agent worker 网络配置**：
- 直接在代理宿主上手动配置

### Capabilities（能力）

Source 支持多种能力：

| 能力 | 描述 |
|------|------|
| **Batch syncs** | 从外部源同步数据到数据集 |
| **Streaming syncs** | 从外部消息队列同步数据到流 |
| **CDC syncs** | 通过 CDC 元数据从数据库同步数据到流 |
| **Media syncs** | 同步媒体数据到媒体集 |
| **HyperAuto** | 自动同步整个系统（仅限 SAP） |
| **File exports** | 将数据作为文件从数据集推送到外部系统 |
| **Table exports** | 将带模式的数据从数据集推送到外部数据库 |
| **Streaming exports** | 将数据从流推送到外部消息队列 |
| **Webhooks** | 交互式地向外部系统发起结构化请求 |
| **Virtual tables** | 将外部数据仓库的数据注册为虚拟表 |
| **Virtual media** | 将外部系统的媒体注册为虚拟媒体集 |
| **Exploration** | 在使用其他能力之前交互式探索外部系统的数据 |
| **Use in code** | 在代码中使用源连接（仅限 Foundry worker） |

## 连接器类型

Data Connection 支持 **200+ 连接器**，包括：

### 数据库
- PostgreSQL, MySQL, Microsoft SQL Server
- Oracle Database, SAP HANA
- Snowflake, Databricks, BigQuery
- Cassandra, MongoDB, Redis

### 云存储
- Amazon S3, Azure Blob Storage
- Google Cloud Storage, HDFS

### SaaS 应用
- Salesforce, SAP, NetSuite
- Microsoft Dynamics 365
- ServiceNow, Zendesk

### 文件系统
- SFTP, FTPS, FTP
- SMB, SharePoint

### 消息队列
- Kafka, Amazon Kinesis
- Google Pub/Sub

### 其他
- REST APIs, GraphQL
- LDAP, OData

## 代码中的连接使用

开发者可以通过以下方式扩展和自定义连接：

| 选项 | 描述 |
|------|------|
| **External transforms** | Python 转换与外部系统通信 |
| **External functions (webhooks)** | TypeScript 导入源以调用现有 webhook |
| **External functions (direct)** | TypeScript `fetch` 或 Python `requests` 直接调用 |
| **Compute modules** | 长时间运行计算，支持任意语言 |
| **External models** | 需要使用网络出口策略 |

## Agent（代理）

Agent 是一个可下载的程序，安装在企业组织网络内并从 Foundry 的 Data Connection 界面管理。Agent 具有连接到组织网络内不同外部系统的能力。

## 初始设置

如果是首次为组织连接 Foundry 与数据，请参考初始设置指南。

## 相关文档

- [Core concepts](https://palantir.com/docs/foundry/data-connection/core-concepts/) - 核心概念详情
- [Architecture](https://palantir.com/docs/foundry/data-connection/architecture/) - 架构详情
- [Available connectors](https://palantir.com/docs/foundry/data-integration/connector-type-reference/) - 连接器参考
- [HyperAuto (SDDI)](https://palantir.com/docs/foundry/hyper-auto/overview/) - SAP 自动化集成

---

*本文档基于 Palantir Foundry 官方文档整理*
