# Workshop 概览

> 来源：https://www.palantir.com/docs/foundry/workshop/overview/
> 分类：用例开发 / 应用程序构建

## 概述

**Workshop** 使应用程序构建者能够为运营用户创建交互式和高质量的应用程序。

![示例 Workshop 模块](https://www.palantir.com/docs/resources/foundry/workshop/object-apps-workshop-module.png)

Workshop 遵循三个关键原则：

### 对象数据

Workshop 通过使用对象层作为主要构建块，降低了应用程序构建者的准入门槛。Workshop 应用程序中的所有数据都从对象数据层读取，允许应用程序创建者利用丰富特性，例如对象类型之间的链接。Workshop 利用 Actions 进行对象数据写回，利用 Functions 进行对象数据的业务逻辑处理。

### 一致的设计

所有 Workshop 组件都遵循统一的设计系统，旨在清晰地交互，具有一致的外观和感觉，并提供高质量的最终用户体验。

### 交互性和复杂性

在 Workshop 中构建的应用程序比在其他点击式工具中创建的典型仪表板更加动态和交互。通过利用高质量的布局和易于使用但复杂的事件系统，Workshop 应用程序旨在像自定义 React 应用程序一样用户友好和高质量。

Workshop 是一个灵活的应用程序构建器，支持广泛可能的用例。Workshop 支持的一些常见应用程序模式包括：

### 收件箱警报和任务管理

收件箱通常用于使运营用户能够分类、确定优先级和完成任务。例如，您可能使用 Workshop 应用程序来分类新传入的保修索赔，或分类和调查警报。

### 通用作战图 (COP)

通用作战图 (COP) 是跨多个组织共享的相关运营信息的显示，以促进意识和协作。例如，您可能构建一个 Workshop 应用程序来作为当前情况的"上墙"大屏视图，包含地图、相关统计信息和图表、过滤或向下钻取数据的方法，以及连接到其他视图或工作流。

---

**相关文档导航：**
- Use case development（用例开发）
  - Overview（概览）
  - What is an operational application?（什么是运营应用程序？）
  - Connecting analytics to operations（将分析连接到运营）
  - Curating apps in Applications Portal（在应用程序门户中策划应用程序）
  - Application building（应用程序构建）
  - Workshop（详尽文档）
    - Getting started（入门）
    - Example applications（示例应用程序）
    - Core concepts（核心概念）
      - Layouts（布局）
      - Widgets（小部件）
      - Variables（变量）
      - Events（事件）
      - Permissions（权限）
    - Actions（行动）
    - Functions（函数）
    - Formatting（格式化）
    - Publishing and Versioning（发布和版本控制）
    - Module interface（模块接口）
    - Routing（路由）
    - State saving（状态保存）
    - 等等...
