# Custom Widgets 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/custom-widgets/overview/

## 概述

**Custom Widgets（自定义小部件）** 使应用程序构建者能够使用**自定义前端代码安全地扩展 Foundry 应用程序**。目前，自定义小部件仅在 **Workshop** 中受支持。

## 核心价值

通过自定义小部件，技术构建者可以：

- **实现开箱即用不可用的功能**
- **为应用用户提供定制体验**
- **无需从头创建完整的独立自定义应用**

## 使用示例

可以使用自定义小部件构建的示例：

### 1. 自定义图表可视化

- **K线图**（Candlestick chart）
- 行业特定的金融图表
- 自定义数据可视化

### 2. 行业特定视图

- **飞行计划**：Ontology 对象的特定行业视图
- **网络拓扑**：IT 基础设施视图
- **供应链可视化**

### 3. 特殊输入小部件

- **签名输入**：签名输入小部件
- **手写注释**：手写注释工具
- **自定义表单控件**

## 核心概念

### Widget Set（小部件集）

**Widget Set** 是代表自定义前端代码版本的 Compass 资源。

**特点**：
- 每个 Widget Set 版本可以包含多个小部件
- 每个小部件具有版本控制
- 安全沙箱执行

### 开发流程

```
┌─────────────────────────────────────────────────────────────┐
│              Custom Widgets 开发流程                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. 创建 Widget Set                                         │
│     ↓                                                        │
│  2. 开发小部件（React/TypeScript）                           │
│     ↓                                                        │
│  3. 配置参数和事件                                          │
│     ↓                                                        │
│  4. 发布新版本                                               │
│     ↓                                                        │
│  5. 在 Workshop 中嵌入                                       │
│     ↓                                                        │
│  6. 测试和迭代                                              │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 小部件组成

### Parameters（参数）

**用途**：允许用户配置小部件行为

**类型**：
- 字符串
- 数字
- 布尔值
- 对象选择器
- 对象集
- 数组

### Events（事件）

**用途**：小部件与主机应用之间的交互

**用途**：
- 触发主机应用中的操作
- 更新变量
- 触发导航

### OSDK 集成

小部件可以使用 **Ontology SDK (OSDK)**：

- 访问 Ontology 对象
- 查询数据
- 应用 Actions
- 调用 Functions

## Workshop 集成

### 嵌入小部件

在 Workshop 模块中嵌入自定义小部件：

1. 从小部件面板中选择自定义小部件
2. 配置小部件参数
3. 连接事件到操作
4. 测试小部件

### 与 Workshop 变量集成

- **输入变量**：从 Workshop 接收数据
- **输出事件**：更新 Workshop 变量
- **双向绑定**：实时数据同步

## 安全性

### 沙箱执行

- **隔离环境**：小部件在隔离环境中执行
- **资源限制**：CPU 和内存使用限制
- **网络控制**：受控的网络访问

### 权限管理

- **OSDK 权限**：小部件继承用户权限
- **数据访问**：基于用户数据访问权限
- **操作权限**：基于用户操作权限

## 开发工具

### 本地开发

- **Code Repositories**：使用 Foundry Code Repositories
- **版本控制**：Git 集成
- **CI/CD**：自动构建和发布

### 测试

- **Widget Playground**：测试小部件
- **预览模式**：实时预览
- **调试工具**：浏览器开发工具

## 发布和管理

### 版本控制

- **语义版本控制**：版本号管理
- **变更日志**：跟踪更改
- **回滚**：回滚到以前的版本

### 发布流程

1. **创建标签**：在 Code Repository 中创建标签
2. **自动构建**：Foundry CI/CD 自动构建
3. **发布**：发布新版本
4. **通知**：通知用户更新

## 最佳实践

### 1. 小部件设计

- **单一职责**：每个小部件做一件事
- **可重用**：设计为可重用组件
- **配置驱动**：通过参数配置行为

### 2. 性能优化

- **懒加载**：延迟加载资源
- **代码分割**：分割代码以减少初始加载
- **缓存**：缓存计算结果

### 3. 错误处理

- **优雅降级**：失败时提供备用 UI
- **错误边界**：捕获 React 错误
- **日志记录**：记录错误以便调试

## 权限和访问

### Widget Set 权限

- **查看权限**：查看 Widget Set
- **编辑权限**：修改 Widget Set
- **发布权限**：发布新版本
- **使用权限**：在 Workshop 中使用小部件

### Marketplace 分发

- **添加到 Marketplace 产品**：将 Widget Set 添加到 Marketplace 产品
- **版本管理**：管理产品中的 Widget Set 版本
- **访问控制**：控制谁可以安装 Widget Set

## 限制

### 当前限制

- **仅 Workshop**：目前仅在 Workshop 中支持
- **前端代码**：仅限前端代码，不能执行服务器端代码
- **语言**：主要支持 TypeScript/React

## 相关文档

- [Core concepts](https://palantir.com/docs/foundry/custom-widgets/core-concepts) - 核心概念
- [Create a widget set](https://palantir.com/docs/foundry/custom-widgets/create/) - 创建小部件集
- [Develop a widget set](https://palantir.com/docs/foundry/custom-widgets/development/) - 开发小部件集
- [Parameters and events](https://palantir.com/docs/foundry/custom-widgets/parameters-and-events/) - 参数和事件
- [Publish a widget set](https://palantir.com/docs/foundry/custom-widgets/publish/) - 发布小部件集
- [Use OSDK in widget set](https://palantir.com/docs/foundry/custom-widgets/use-osdk/) - 在小部件集中使用 OSDK

---

*本文档基于 Palantir Foundry 官方文档整理*
