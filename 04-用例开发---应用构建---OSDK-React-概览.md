# OSDK React Applications 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/ontology-sdk-react-applications/overview/

## 概述

**Developer Console** 使应用程序构建者能够使用 React 构建完全可定制的用户界面，并由 **Ontology Software Development Kit (OSDK)** 提供支持。

通过选择 React 构建应用程序，用户可以：
- 利用现有的开发体验
- 利用 React 社区的巨大投资
- 快速交付一流的 UI
- 将 Foundry 作为后端，利用 Ontology 的大规模查询和编辑能力

## 核心优势

### 1. 完全定制化

- 完全控制用户界面
- 自定义组件和布局
- 灵活的样式和设计

### 2. 类型安全

- 生成的 TypeScript 类型
- 编辑器中的自动完成
- 编译时类型检查

### 3. Foundry 后端

- 无需构建自己的后端
- 利用 Foundry 的查询能力
- 内置权限和治理

### 4. 快速开发

- 热重载
- 本地开发环境
- 快速迭代

## 开发流程

### 1. 创建 Developer Console 应用程序

1. 访问 Developer Console
2. 选择要访问的 Ontology 实体
3. 生成 TypeScript SDK
4. 获取 OAuth 凭据

### 2. 开发和部署

- 在本地开发
- 使用生成的 SDK
- 部署到 Foundry

### 3. 故障排除

- 调试工具
- 日志记录
- 错误处理

## 开发工具

### VS Code

**推荐编辑器**：
- 智能代码完成
- 类型提示
- 调试支持

### Code Workspaces

**平台内开发**：
- JupyterLab 集成
- 直接在 Foundry 中开发

### Local Development

**本地环境**：
- 本地服务器
- 热重载
- 快速反馈

## 学习资源

### 入门教程

**1. Getting started with OSDK: Build a to-do application**

- 分步教程
- 学习创建待办事项应用
- 从环境设置到产品部署

**2. OSDK with AIP Logic: Build a to-do application**

- AIP Logic 集成
- 从 React 或 Python 应用调用 AIP Logic 函数
- 生产环境运行

**3. Custom Workshop Widgets using OSDK**

- 使用 Workshop 中的 **Custom widget via iframe** 小部件
- 嵌入 Foundry 托管的 React 应用
- 双向状态共享

### 高级示例

**Advanced to-do application with OSDK**

- 演示高级 OSDK 功能
- 实用的待办事项应用示例
- 高级功能和实现模式

## OSDK 语言支持

虽然本节专注于 React (TypeScript)，OSDK 也支持其他语言：

| 语言 | 包管理器 | 文档 |
|------|----------|------|
| **Python** | Pip / Conda | [Python OSDK](https://palantir.com/docs/foundry/ontology-sdk/python-osdk/) |
| **Java** | Maven | [Java OSDK](https://palantir.com/docs/foundry/ontology-sdk/java-osdk/) |
| **其他语言** | OpenAPI | OpenAPI 规范 |

## 应用程序架构

### 典型架构

```
┌─────────────────────────────────────┐
│         React Frontend              │
│  (使用 OSDK TypeScript 库)          │
└──────────────┬──────────────────────┘
               │
               │ OAuth Token
               │
┌──────────────▼──────────────────────┐
│         Foundry Platform            │
│  - Ontology API                     │
│  - Functions                        │
│  - Actions                          │
└─────────────────────────────────────┘
```

### 关键组件

1. **OSDK Library**：生成的 TypeScript 库
2. **React Components**：自定义 UI 组件
3. **OAuth 认证**：用户认证
4. **API Gateway**：与 Foundry 通信

## 开发最佳实践

### 1. 项目结构

- 组件组织
- 类型定义
- 样式管理

### 2. 状态管理

- React Hooks
- Context API
- 外部状态管理（如需要）

### 3. 错误处理

- 错误边界
- 用户友好的错误消息
- 日志记录

### 4. 性能优化

- 代码分割
- 懒加载
- 缓存策略

## 部署选项

### Foundry 托管

- 托管在 Foundry 上
- 自动扩展
- 内置安全性

### 自定义托管

- 使用 OAuth
- 自己的基础设施
- 更多控制权

## 相关文档

- [Development environment](https://palantir.com/docs/foundry/ontology-sdk-react-applications/development-environment/) - 开发环境设置
- [Build advanced to-do application](https://palantir.com/docs/foundry/ontology-sdk-react-applications/advanced-todo-application-overview/) - 高级教程
- [Custom Widgets](https://palantir.com/docs/foundry/custom-widgets/) - Workshop 自定义小部件
- [Foundry Functions](https://palantir.com/docs/foundry/functions/) - Functions 文档

---

*本文档基于 Palantir Foundry 官方文档整理*
