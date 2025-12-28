# Functions 概览

> 来源：https://www.palantir.com/docs/foundry/functions/overview/
> 分类：本体构建 / 函数

## 概述

**Functions** 使代码作者能够编写可在运营上下文中快速执行的逻辑，例如旨在赋予决策流程的仪表板和应用程序。此逻辑在隔离环境中的服务器端执行。

值得注意的是，Functions 包括基于 Foundry 本体编写逻辑的一流支持。这包括支持读取各种对象类型的属性、遍历链接以及灵活地进行本体编辑。

Functions 的常见用例包括：

- 返回对象集或变量值以在 Workshop 中使用
- 使用 Workshop 的函数支持列在派生表列中显示转换后的值
- 聚合对象类型值以显示为 Workshop 图表
- 通过函数支持行动表达对本体的复杂编辑，该编辑更新多个对象
- 在后端运行逻辑以返回要在前端 Slate 中显示的信息
- 计算自定义指标或聚合以在 Quiver 中显示
- 查询外部系统以通过外部函数丰富本体中的对象

Functions 支持的语言包括 TypeScript ↗ 和 Python (Beta)↗。

要开始在 Foundry 中使用 Functions，我们建议以下教程：

- [TypeScript 入门](https://www.palantir.com/docs/foundry/functions/getting-started-typescript/)
- (Beta) [Python 入门](https://www.palantir.com/docs/foundry/functions/python-functions-getting-started/)

## 按语言的功能支持

并非所有功能都受两种语言支持。请参阅下表了解特定功能的语言支持。

| Functions 能力 | TypeScript 支持 | Python 支持 | 描述 |
| --- | --- | --- | --- |
| 本体对象支持 | 是 | 是 | 在函数中访问本体的能力 |
| 本体编辑支持 | 是 | 是 | 在函数中编辑本体的能力 |
| 在 Workshop 中可查询 | 是 | 是 | 从 Workshop 应用调用函数 |
| 在 Pipeline Builder 中可用 | 否 | 是 | 从 Pipeline Builder 管道调用函数 |
| 模型函数支持 | 是 | 否 | 编写可嵌入模型内的函数 |
| 语义搜索支持 | 是 | 否 | 使用函数为语义搜索创建向量 |
| 外部 API 调用支持 | 是 | 否 | 从函数内部查询外部服务 |
| 无服务器执行支持 | 是 | 否 | 无服务器函数将在被调用时按需启动 |
| 部署执行支持 | 否 | 是 | 部署的函数将分配专用资源，准备服务请求 |
| 从 API 网关调用函数 | 是 | 是 | 从 API 网关访问查询函数的能力 |
| Marketplace 支持 | 是 | 否 | 通过 Marketplace 打包和运输函数的能力 |

## 无服务器函数超时

目前，每个无服务器函数被分配总共 60 秒的运行时间。这包括 30 秒的 CPU 时间和 30 秒的缓冲时间以应对任何网络延迟。如果超过超时时间，函数将失败。

## 部署函数超时

目前，每个部署的函数被分配总共 60 秒的运行时间。如果超过超时时间，函数将失败。

---

**相关文档导航：**
- Ontology building（本体构建）
  - Functions（完整文档）
    - Getting started（入门）
    - Use Functions in the platform（在平台中使用 Functions）
    - TypeScript basics（TypeScript 基础）
      - Input and output types（输入和输出类型）
      - Decorators（装饰器）
      - Handle undefined values（处理未定义值）
      - Debug Functions（调试 Functions）
      - Add NPM dependencies（添加 NPM 依赖）
    - Python functions [Beta]（Python 函数）
      - Getting started（入门）
      - Types reference（类型参考）
      - Functions on objects（对象上的函数）
      - Make API calls from Python functions（从 Python 函数进行 API 调用）
      - Ontology edits（本体编辑）
      - Use Python functions in Pipeline Builder（在 Pipeline Builder 中使用 Python 函数）
      - Use Python functions in Workshop（在 Workshop 中使用 Python 函数）
      - Advanced usage（高级用法）
    - Functions on models（模型上的函数）
    - Language models within Functions（Functions 中的语言模型）
    - Querying external APIs from functions（从函数查询外部 API）
    - Functions on objects（对象上的函数）
    - Semantic search（语义搜索）
    - Ontology edits（本体编辑）
    - Functions called through the API gateway（通过 API 网关调用的函数）
    - Models and graphs（模型和图形）
    - Unit testing（单元测试）
    - Performance and limits（性能和限制）
    - Permissions（权限）
