# Automate 概览

> 来源：https://www.palantir.com/docs/foundry/automate/
> 分类：用例开发 / 工作流构建 / 自动化

## Automate

**Automate** 是一个完全向后兼容的产品，它取代了对象监控，成为平台中所有业务自动化的单一入口点。

**Automate** 是用于设置业务自动化的应用程序。Automate 应用程序允许用户定义条件和效果。条件会持续检查，当满足指定条件时自动执行效果。

条件可以是 _静态时间条件_（"每周一上午 9 点触发"）、基于 Foundry 本体的 _对象数据条件_（"添加优先级为 `high` 的新警报对象时触发"），或静态和对象数据条件的组合。

可配置的效果包括提交 Foundry 操作以及向用户发送带有附件的平台和电子邮件通知。

![Automate 概览](https://www.palantir.com/docs/resources/foundry/automate/automate-overview.png)

## 用例

Automate 可用于各种不同的自动化工作流，包括：

- **定时报告发送和摘要**：指定时间并向预定义的收件人列表发送每周报告。从 Notepad 或 Notepad 模板生成的 PDF 可以自动附加到电子邮件。
- **数据警报**：定义和监视对象集，并在满足特定数据条件时向用户发出警报；例如，当未解决问题对象的总数超过阈值时。
- **工作流自动化**：Automate 可用于自动对符合指定条件的对象数据执行操作。可以自动执行的一些任务包括：
  - 检查数据异常并自动将这些对象传递给具有解决问题逻辑的操作。
  - 监视建议或潜在操作，并在满足预配置的事件和时间条件时自动应用它们。此类操作可能包括通过 Webhooks 向外部系统发出 API 调用，以直接在外部系统中应用更改。
- **监视的搜索**：配置自动化，以便在保存的对象探索有新结果或满足搜索的所有结果中的聚合标准时发出通知；例如，所有传感器对象的最大温度超过阈值。

## 访问 Automate

要访问 Automate 应用程序，请单击 Foundry 导航侧边栏中的名称或图标。按照创建第一个自动化部分中概述的说明开始使用。

Automate 专为业务自动化而设计。如果您正在寻找数据连接和管道构建的健康监控，请参阅健康检查文档。

---

**相关文档导航：**
- Use case development（用例开发）
  - Workflow building（工作流构建）
  - Automate（完整文档）
    - Getting started（入门）
    - Condition（条件）
      - Time condition（时间条件）
      - Object set conditions（对象集条件）
      - Condition settings（条件设置）
      - Automation dependencies（自动化依赖）
      - Streaming（流式传输）
      - Evaluation latency（评估延迟）
    - Effects（效果）
      - Actions effect（操作效果）
      - Notification effect（通知效果）
      - Fallback effect（回退效果）
      - Effect settings（效果设置）
      - Manual execution（手动执行）
    - Settings（设置）
      - Automation administrators（自动化管理员）
      - Muting, pausing, and expiry（静音、暂停和过期）
      - Configuring retries（配置重试）
      - Execution settings（执行设置）
    - Concepts（概念）
      - Activity（活动）
      - Notification settings（通知设置）
      - Security and permissions（安全和权限）
    - Integrations（集成）
    - Examples（示例）
    - Limits（限制）
    - Error reference（错误参考）
    - Add automation to Marketplace product（将自动化添加到 Marketplace 产品）
