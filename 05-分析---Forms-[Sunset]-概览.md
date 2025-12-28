# Forms [Sunset] 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/forms/overview/
> 状态：**Sunset（日落）** - 已停止开发，建议使用替代方案

## 概述

**Forms** 是一个表单构建界面，与 Foundry 中的其他应用程序无缝集成。Forms 允许在直观的体验和复杂的可配置性之间取得平衡。

## ⚠️ Sunset 状态

**Forms** 处于开发的生命周期日落阶段，将在未来被弃用。完整支持仍然可用。

**Palantir 推荐的替代方案**：

使用 **Ontology** 表示相关数据结构作为对象类型，并配置 **Actions** 和 **Functions** 进行写回交互：

### Actions（行动）

- **强大的权限控制**：对与添加、编辑和删除数据关联的权限进行更强大和细粒度的控制
- **受限视图**：尊重受限视图
- **条件权限**：配置复杂的条件权限
- **Workshop 和 Slate 原生支持**：在 Workshop 和 Slate 中使用完整的应用程序构建工具集构建复杂的数据输入用户体验
- **API 绑定**：自动为平台 API 生成 API 绑定，使您能够将数据写入外部数据系统或触发其他下游效果

### Functions（函数）

- Actions 可以由 Functions 支持，以允许更具表现力和复杂的写回逻辑

## Forms 功能

### 无代码体验

**无需编码经验**即可创建和管理自定义数据输入和存储解决方案

### 工作流配置

用户可以使用 Forms 配置各种工作流：

- **动态字段**：定义动态字段以引导来自响应者的数据
- **嵌入式表单**：将表单作为部分嵌入 Object Explorer 和 Slate
- **数据存储**：将收集的信息存储在 Fusion 中

## 核心概念

### 1. Validators（验证器）

每个表单字段可以有一个或多个验证器，以防止格式错误的输入

### 2. Transforms（转换）

转换表单输入数据

### 3. Multiplicity（多重性）

控制表单响应的重复性

### 4. Permissions（权限）

配置表单的访问权限

## 表单配置

### 创建表单

- 从 Foundry 导航侧边栏打开 Forms 应用
- 创建新表单或打开现有表单

### 字段类型

#### 简单字段 (Simple Fields)

- 文本输入
- 数字输入
- 日期/时间选择器
- 下拉菜单
- 复选框
- 单选按钮

#### 数据支持字段 (Data-backed fields)

- 从数据集填充选项
- 动态选项更新

#### 自动填充字段 (Auto-populating fields)

- 基于其他字段自动填充
- 预填充默认值

#### 附件字段 (Attachments field)

- 文件上传
- 多个附件

#### 代码编辑器 (Code Editor)

- 高级字段配置

#### 生成主键

- 自动生成主键值

### 表单工作表 (Sheets)

组织表单字段到多个工作表/页面

## 表单管理

### 接收通知

- 当有新响应时接收通知

### 共享

- 与其他用户共享表单
- 配置访问权限

### 审查和编辑响应

- 查看所有表单响应
- 编辑提交的响应
- 导出响应数据

### 与其他应用集成

- **Fusion**：存储收集的信息
- **Slate**：嵌入表单作为部分
- **Object Explorer**：嵌入表单作为部分

## 迁移建议

### 从 Forms 迁移到 Actions + Workshop

**步骤**：

1. **定义对象类型**：创建对象类型以表示表单数据结构
2. **创建 Actions**：定义 Actions 以创建和编辑对象
3. **构建 Workshop 应用**：使用 Workshop 构建表单界面
4. **配置权限**：在 Actions 上配置细粒度权限
5. **集成 Functions**：如果需要复杂逻辑，使用 Functions 支持 Actions

**优势**：

- 更强大的权限控制
- 更好的用户体验
- 原生平台集成
- API 支持
- 未来支持保证

## 常见问题

### Forms 会立即消失吗？

不会。Forms 处于 sunset 阶段，完整支持仍然可用。但建议新项目使用 Actions + Workshop。

### 现有表单需要迁移吗？

建议计划迁移，但不是立即需要。可以继续使用现有表单，同时规划迁移策略。

### 如何学习 Actions 和 Workshop？

参考以下文档：
- [Action types overview](https://palantir.com/docs/foundry/action-types/overview/)
- [Workshop overview](https://palantir.com/docs/foundry/workshop/overview/)

## 相关文档

- [Create a form](https://palantir.com/docs/foundry/forms/create-a-form/) - 创建表单
- [Simple fields](https://palantir.com/docs/foundry/forms/simple-fields/) - 简单字段
- [Validators](https://palantir.com/docs/foundry/forms/validators/) - 验证器
- [FAQs](https://palantir.com/docs/foundry/forms/faqs) - 常见问题

---

*本文档基于 Palantir Foundry 官方文档整理*
