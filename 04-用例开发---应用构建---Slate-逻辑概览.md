# Slate 逻辑概览

> 来源：https://www.palantir.com/docs/foundry/slate/logic-overview/
> 分类：用例开发 / 应用构建 / Slate

## 概述

应用程序通常需要先修改或丰富数据，然后才能向用户展示或以其他方式可视化。同样，应用程序可能需要额外的信息才能按预期方式运行。例如，您可能希望指示小部件必须具有适当的配置才能成功运行，或者某些信息根据应用程序状态显示。

Slate 提供了多个原语来管理和操纵状态和数据。

### 函数 (Functions)

**函数** 是可以读取 Handlebars 并返回任何类型输出的 JavaScript 代码片段。函数可以处理来自查询的数据、获取小部件或变量的状态并构造新值，或为小部件准备类。

了解有关 Slate 中函数的更多信息。

### Handlebars

**Handlebars** 使用小部件中的函数或事件中的查询中的值从一个组件传递到另一个组件。Handlebars 通过两个花括号 `{{ }}` 让您访问当前在应用程序中流动的所有信息。

了解有关在 Slate 中使用 Handlebars 的更多信息。

### 变量 (Variables)

**变量** 存储值以保存特定状态、存储用户输入或设置默认值。通过 URL 参数设置变量的值，或通过事件更新它们。

了解有关 Slate 中变量的更多信息。

### 事件 (Events)

**事件** 由单个事件和用户操作组成。事件触发应用程序中的活动；例如，您可以配置事件以在选择按钮时提交查询或在对话框关闭后显示提示。事件和操作处理 Slate 内部的所有类型的自动交互。

了解有关 Slate 中事件和操作的更多信息。

---

**Slate 是什么？**

Slate 为构建者提供了一套灵活的工具，用于快速创建运营应用程序和交互式仪表板。

**主要特点：**
- 拖放式界面
- 与 Foundry 本体无缝集成
- 使用 HTML、CSS 和 JavaScript 完全自定义
- 快速开发和部署
- 支持动态和响应式应用程序
- 内置数据读写能力
- 支持函数和事件处理

---

**相关文档导航：**
- Use case development（用例开发）
  - Slate（完整文档）
    - Overview（概览）
    - Navigation（导航）
    - FAQ（常见问题）
    - Manage Slate applications（管理 Slate 应用程序）
      - Application types（应用程序类型）
      - Create applications（创建应用程序）
      - Pages（页面）
      - Manage application versions（管理应用程序版本）
      - Merge application changes（合并应用程序更改）
      - Import, export, and duplicate applications（导入、导出和复制应用程序）
      - Enable user interaction（启用用户交互）
    - Read and write data（读写数据）
      - Write back data with Actions（使用操作写回数据）
      - Read and write to data systems（读写数据系统）
      - Create or retrieve object sets（创建或检索对象集）
      - Retrieve individual objects（检索单个对象）
      - Ontology and Actions using OSDK（使用 OSDK 的本体和操作）
      - Use Foundry Functions in Slate（在 Slate 中使用 Foundry 函数）
      - Upload data for public applications（为公共应用程序上传数据）
      - Write back data to Phonograph（将数据写回 Phonograph）
    - Logic（逻辑）
      - Overview（概览）
      - View application dependencies（查看应用程序依赖项）
      - Understand dependencies（理解依赖项）
      - Define and run Slate functions（定义和运行 Slate 函数）
      - Convert between row and column schemas（在行和列架构之间转换）
      - Store values in variables（将值存储在变量中）
      - Access values with Handlebars（使用 Handlebars 访问值）
      - Handlebar helpers（Handlebars 助手）
      - Configure Events and Actions（配置事件和操作）
      - Events and actions index（事件和操作索引）
    - Styles（样式）
      - Overview（概览）
      - Custom styles on widgets（小部件上的自定义样式）
      - Configure and apply styles（配置和应用样式）
      - Global stylesheets（全局样式表）
      - Build complex layouts（构建复杂布局）
    - Widgets（小部件）
      - Chart（图表）
      - Container（容器）
      - Control（控件）
      - Platform（平台）
      - Text（文本）
      - Time（时间）
      - Visualization（可视化）
      - Advanced（高级）
    - Troubleshooting（故障排除）
      - Debug applications（调试应用程序）
      - Optimize indexes and schema design（优化索引和架构设计）
      - Optimize queries in Postgres（优化 Postgres 中的查询）
    - Add Slate application to Marketplace product [Beta]（将 Slate 应用程序添加到 Marketplace 产品）
