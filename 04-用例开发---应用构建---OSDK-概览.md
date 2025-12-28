# Ontology SDK (OSDK) 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/ontology-sdk/overview/

## 概述

**Ontology Software Development Kit (OSDK)** 允许用户直接从开发环境访问 Ontology 的全部功能。用户可以通过 Developer Console 生成 OSDK，它支持：

- **TypeScript**: NPM (Node Package Manager) 包
- **Python**: Pip 或 Conda
- **Java**: Maven
- **其他语言**: OpenAPI 规范

通过将 Foundry 作为后端，用户可以利用 Ontology 强大的大规模查询能力和 Foundry 写回功能，以及细粒度的治理控制，加速安全应用程序的开发。

## OSDK 优势

### 1. 加速开发 (Accelerated Development)

- 快速开始开发由 Foundry Ontology 支持的应用程序
- 通过对 Ontology API 的人机工程学访问，用最少的代码读取和写回 Ontology

### 2. 强类型安全 (Strong Type-Safety)

- 为用户生成的函数和类型仅基于与用户相关的 Ontology 子集
- 类型和函数从用户的 Ontology 生成
- 可以直接在编辑器中查询和探索 Ontology

### 3. 集中维护 (Centralized Maintenance)

- Ontology 在 Foundry 中集中构建和管理
- 专注于应用程序构建
- 减少构建数据基础所需的典型维护负担

### 4. 安全设计 (Secure by Design)

- OSDK 使用的 token 仅限于用户希望应用程序访问的本体实体
- 加上用户自己对数据的权限

## Developer Console

**Developer Console** 是用于创建 OSDK 应用程序以及 OAuth 客户端的平台。

**访问方式**：在应用程序门户中搜索 `developer console`

**功能**：
- 创建 OSDK 应用程序
- 管理 OAuth 客户端
- 生成特定于 Ontology 的文档

## 支持的语言和框架

### TypeScript

- **NPM 包**：标准 Node.js 包管理
- **React 绑定**：前端开发的便捷方式
- **类型安全**：完整的 TypeScript 类型定义

### Python

- **Pip/Conda**：标准 Python 包管理
- **类型提示**：Python 类型注解支持
- **Jupyter 集成**：在 Notebook 中使用

### Java

- **Maven**：标准 Java 依赖管理
- **类型安全**：完整的 Java 类型定义

### OpenAPI

- **语言无关**：支持任何支持 OpenAPI 的语言
- **规范生成**：自动生成 API 规范

## OSDK 功能

### 对象访问

- 按ID检索单个对象
- 查询对象集
- 过滤和排序对象
- 对象关系导航

### 对象编辑

- 创建新对象
- 更新现有对象
- 删除对象
- 批量操作

### Actions 应用

- 应用预定义的 Actions
- 传递参数
- 处理 Action 结果

### Functions 调用

- 调用查询函数
- 调用聚合函数
- 调用自定义函数

### AIP Logic 集成

- 调用 AIP Logic 函数
- AI 驱动的功能
- 语义搜索

## 开发工作流

### 1. 创建应用程序

在 Developer Console 中：
1. 选择要访问的 Ontology 实体
2. 选择语言（TypeScript/Python/Java）
3. 生成 SDK

### 2. 本地开发

- 使用生成的 SDK 进行开发
- 在编辑器中获取类型提示和自动完成
- 使用 Foundry 作为后端

### 3. 测试

- 单元测试支持
- 存根对象
- Mock 数据

### 4. 部署

- 将应用程序部署到 Foundry
- OAuth 认证
- 权限管理

## OSDK 文档生成

Developer Console 为用户的 Ontology 生成特定文档：

**TypeScript**：
- 完整的 API 参考
- 类型定义
- 代码示例

**Python**：
- API 文档
- 类型提示
- 使用示例

**Java**：
- Javadoc 风格文档
- 类和方法参考

## React 应用程序

OSDK 为 React 开发提供专门的绑定：

**优势**：
- 前端开发的便捷方式
- React Hooks 集成
- 类型安全的 props

**相关文档**：[OSDK React applications](https://palantir.com/docs/foundry/ontology-sdk-react-applications/overview/)

## 安全和权限

### Token 范围

- 仅限于选择的 Ontology 实体
- 与用户的权限结合
- 细粒度访问控制

### OAuth 认证

- 公共客户端
- 保密客户端
- Token 管理

## 相关文档

- [OSDK React applications](https://palantir.com/docs/foundry/ontology-sdk-react-applications/overview/) - React 应用开发
- [Developer Console](https://palantir.com/docs/foundry/ontology-sdk/create-a-new-osdk/) - 控制台使用指南
- [Python OSDK](https://palantir.com/docs/foundry/ontology-sdk/python-osdk/) - Python SDK 参考
- [Java OSDK](https://palantir.com/docs/foundry/ontology-sdk/java-osdk/) - Java SDK 参考
- [Build a to-do application](https://learn.palantir.com/) - 教程示例

---

*本文档基于 Palantir Foundry 官方文档整理*
