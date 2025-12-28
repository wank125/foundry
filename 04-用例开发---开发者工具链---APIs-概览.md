# Foundry APIs 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/api/general/overview/introduction//

## 概述

**Foundry API** 是一个面向开发者的 REST API，用于与 Palantir Foundry 平台交互。它可以用于在 Palantir 产品之上构建应用程序。

## API 架构

### RESTful 设计

Foundry API 是一个 **REST API（Representational State Transfer）**，由 HTTP 端点组成。

**特点**：
- 使用 HTTP 标准方法（GET、POST、PUT、DELETE 等）
- 基于 JSON 的请求和响应
- 资源导向的 URL 结构
- 无状态架构

### 认证

API 端点使用 **OAuth 2.0 协议**进行认证。

**认证方式**：
- 授权码授予（Authorization Code Grant）
- 客户端凭据授予（Client Credentials Grant）
- 刷新令牌（Refresh Tokens）

## API 版本

Foundry API 有两个主要版本：

| 版本 | 说明 |
|------|------|
| **Version 2.0** | 当前版本，推荐使用 |
| **Version 1.0** | 旧版本，维护模式 |

## API 端点分类

### 1. General（通用）

- **Overview** - API 概览
- **Introduction** - 介绍
- **Authentication** - 认证
- **Getting started** - 入门指南
- **SDK** - 软件开发工具包
- **Paging** - 分页
- **Versioning** - 版本控制
- **Limits** - 限制
- **Errors** - 错误处理

### 2. Admin（管理）

#### Users（用户管理）
- List Users, Get User, Search Users
- Delete User, Revoke Tokens
- Group Memberships
- Profile Pictures

#### Groups（组管理）
- Create Group, Delete Group
- List Groups, Get Group
- Group Members
- Group Memberships Expiration Policies

#### Markings（标记管理）
- Marking Categories
- Markings
- Marking Members
- Marking Role Assignments

#### Organizations（组织管理）
- Get/Replace Organization
- Organization Role Assignments

#### Authentication Providers
- List Providers, Get Provider
- Preregister Users/Groups

### 3. AIP Agents（AI 代理）

#### Agents
- Get Agent, List Agent Versions
- Get Agent Version

#### Sessions
- Create/Delete Session
- List/Get Sessions
- Continue Session (Blocking/Streaming)
- Cancel Session
- Get RAG Context

#### Session Traces
- Get Session Trace

### 4. Connectivity（连接）

#### Connections
- Create/Get/Update Connection
- Get Configuration
- Upload Custom JDBC Drivers

#### Imports
- File Imports, Table Imports
- Virtual Tables

### 5. Datasets（数据集）

#### Dataset Operations
- Create/Get Dataset
- Read Table Dataset
- Get Dataset Schema
- Get Dataset Jobs/Schedules/Health Checks

#### Branches
- Create/Delete/List Branches
- Get Branch, Get Transaction History

#### Transactions
- Create/Get Transaction
- Commit/Abort Transaction

#### Files
- Upload/Get/Delete File
- Get File Content

#### Views
- Create/Get View
- Manage Backing Datasets
- Add/Remove Primary Key

### 6. Filesystem（文件系统）

#### Resources
- Get/Delete Resource
- Get By Path
- Restore/Permanently Delete
- Add/Remove Markings
- Get Access Requirements

#### Resource Roles
- Add/Remove Resource Roles

#### Folders
- Create/Get Folder
- List Children

#### Projects
- Get/Create Project
- Add/Remove Organizations
- List Spaces

### 7. Media Sets（媒体集）

- Create/Commit/Abort Media Transaction
- Get Media Item Info/Reference
- Upload Media
- Read Media Item

### 8. Ontologies（本体）

#### Ontology Operations
- List/Get Ontologies
- Get Full Metadata

#### Action Types
- List/Get Action Types

#### Object Types
- List/Get Object Types
- List Outgoing Link Types

#### Ontology Objects
- List/Get Objects
- Search/Aggregate Objects

#### Linked Objects
- List/Get Linked Objects

#### Properties
- Attachment Properties
- Media Reference Properties
- Time Series Properties
- Cipher Text Properties

#### Interfaces
- List/Get Interface Types

#### Actions
- Apply Action (Single/Batch)

#### Queries
- Execute Query

#### Object Sets
- Create Temporary Object Set
- Load/Aggregate Object Set

#### Value Types
- List/Get Value Types

### 9. Orchestration（编排）

#### Schedules
- Create/Delete/Get Schedule
- Run/Pause/Unpause Schedule
- List Runs
- Get Schedule Version

#### Builds
- Get/Cancel Build
- List Jobs

### 10. SQL Queries

- Execute SQL Query
- Get Status/Results
- Cancel Query

### 11. Streams（流）

- Create Streaming Dataset
- Create Stream
- Publish Records
- Reset Stream

### 12. Third Party Applications

#### Websites
- Get/Deploy/Undeploy Website
- Upload Version

## 开发工具

### Software Development Kit (SDK)

Palantir 提供多种语言的 SDK：

| 语言 | SDK | 用途 |
|------|-----|------|
| **TypeScript** | OSDK NPM 包 | 前端和后端开发 |
| **Python** | Pip/Conda 包 | 数据科学和后端 |
| **Java** | Maven 包 | 企业级应用 |
| **OpenAPI** | 规范 | 任何支持 OpenAPI 的语言 |

### API Gateway

通过 API Gateway 发布和调用查询函数：
- **安全性**：集中认证和授权
- **监控**：API 使用监控
- **限流**：请求限流

## 分页

API 支持分页以处理大型结果集：

- **基于游标的分页**：用于大型数据集
- **基于偏移量的分页**：用于小型数据集
- **页面大小限制**：可配置的页面大小

## 限制

为了确保平台稳定性，API 有以下限制：

- **速率限制**：每分钟请求数限制
- **并发限制**：并发请求数限制
- **数据大小限制**：请求/响应大小限制
- **超时**：请求超时限制

## 错误处理

API 使用标准 HTTP 状态码：

| 状态码 | 含义 |
|--------|------|
| 200 | 成功 |
| 201 | 已创建 |
| 400 | 错误请求 |
| 401 | 未授权 |
| 403 | 禁止访问 |
| 404 | 未找到 |
| 429 | 请求过多 |
| 500 | 服务器错误 |

## 数据导出考虑

如果需要从 Foundry 导出数据，**Data Connection exports** 可能更适合您的用例。

## 最佳实践

### 认证

- 使用 OAuth 2.0 进行安全认证
- 安全存储访问令牌
- 使用刷新令牌避免频繁重新认证

### 错误处理

- 始终检查 HTTP 状态码
- 实现重试逻辑
- 记录错误以便调试

### 性能

- 使用分页处理大型数据集
- 缓存频繁访问的数据
- 批量操作以提高效率

### 安全

- 验证所有输入
- 使用 HTTPS
- 遵循最小权限原则

## 相关文档

- [Getting started](https://palantir.com/docs/foundry/api/general/overview/getting-started//) - API 入门指南
- [Authentication](https://palantir.com/docs/foundry/api/general/overview/authentication//) - 认证详解
- [Query Functions](https://palantir.com/docs/foundry/functions/query-functions/) - 查询函数
- [OSDK](https://palantir.com/docs/foundry/ontology-sdk/overview/) - Ontology SDK
- [API Reference](https://palantir.com/docs/foundry/api/) - 完整 API 参考

---

*本文档基于 Palantir Foundry 官方文档整理*
