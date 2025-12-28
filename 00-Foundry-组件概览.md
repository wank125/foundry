# Palantir Foundry 平台组件概览

> 更新时间：2025-12-28

## 平台架构

Foundry 是 Palantir 的数据运营平台，与 AIP（AI Platform）和 Apollo 共同构成 Palantir 的 AI Mesh。

```
┌─────────────────────────────────────────────────────────┐
│                   AI 驱动产品层                          │
│  ┌──────────┐  ┌──────────┐  ┌──────────────────────┐  │
│  │ AIP Now  │  │  Build   │  │  Custom AI Products  │  │
│  │ (预构建)  │  │ with AIP │  │      (自定义)         │  │
│  └──────────┘  └──────────┘  └──────────────────────┘  │
├─────────────────────────────────────────────────────────┤
│                      AIP + Foundry                       │
│  ┌──────────────────────────────────────────────────┐  │
│  │  Ontology Layer (本体层)                         │  │
│  │  - Objects (对象) - Links (链接)                 │  │
│  │  - Actions (行动) - Functions (函数)            │  │
│  └──────────────────────────────────────────────────┘  │
│  ┌──────────────────────────────────────────────────┐  │
│  │  Core Services (核心服务)                        │  │
│  │  - Data Integration - Analytics                  │  │
│  │  - Application Building - Workflow Automation    │  │
│  └──────────────────────────────────────────────────┘  │
│  ┌──────────────────────────────────────────────────┐  │
│  │  Security & Governance (安全与治理)              │  │
│  └──────────────────────────────────────────────────┘  │
├─────────────────────────────────────────────────────────┤
│              Software Delivery (Apollo)                  │
└─────────────────────────────────────────────────────────┘
```

---

## 1. 数据连接与集成 (Data connectivity & integration)

### 1.1 Pipeline Builder
- **功能**：Foundry 的主要数据集成应用
- **用途**：构建数据管道，转换原始数据源为干净的输出
- **特点**：
  - 点击式和代码式双模式
  - 自动构建路径修剪
  - 类型安全函数
  - 严格输出检查
  - 支持批处理和流式管道
  - LLM 数据转换节点

### 1.2 Data Connection
- **功能**：连接各种企业数据源
- **支持**：200+ 连接器
- **连接方式**：
  - 直接连接
  - Agent 代理
  - Webhook
- **数据类型**：数据库、SaaS 应用、文件系统、流数据等

### 1.3 Code Repositories
- **功能**：代码版本控制和管理
- **支持语言**：Python、Java、SQL、R
- **特点**：Git 工作流、分支管理、单元测试

### 1.4 HyperAuto (SDDI)
- **功能**：SAP 自动化数据集成
- **用途**：快速发现和集成 SAP 数据

### 1.5 数据处理组件
- **External Transforms**：外部转换
- **Source-based Transforms**：基于源的转换
- **External Functions**：外部函数调用

---

## 2. 模型连接与开发 (Model connectivity & development)

### 2.1 建模环境
- **Code Workspaces**：JupyterLab、RStudio Workbench、VS Code
- **Code Workbook**：可视化节点编辑器
- **Python/Java/R 支持**：完整的建模语言支持

### 2.2 模型管理
- **Modeling Objectives**：模型生命周期管理
- **Model Adapters**：模型抽象层
- **Evaluations**：模型评估和基准测试

### 2.3 LLM 集成
- **Language Model Service**：统一的多模态接口
- **AIP Logic**：AI 驱动的逻辑函数
- **Semantic Search**：语义搜索支持

### 2.4 模型部署
- **实时交互**：通过 Functions 绑定
- **批量部署**：管道调度执行
- **模型目标**：生产就绪路径

---

## 3. 本体构建 (Ontology Building)

### 3.1 Ontology Manager
- **对象类型 (Object Types)**：定义企业实体
- **链接类型 (Link Types)**：定义实体关系
- **属性 (Properties)**：对象属性定义
- **值类型 (Value Types)**：数据类型约束
- **结构类型 (Struct Types)**：复杂数据结构

### 3.2 Functions
- **TypeScript 函数**：无服务器执行
- **Python 函数 [Beta]**：部署执行
- **功能**：
  - 对象查询和聚合
  - 本体编辑
  - 外部 API 调用
  - 语义搜索
  - 模型函数

### 3.3 Action Types
- **参数化操作**：定义输入参数
- **提交标准**：操作验证规则
- **函数支持操作**：复杂业务逻辑
- **副作用**：通知、Webhook
- **权限控制**：细粒度访问控制

### 3.4 本体应用
- **Object Explorer**：搜索和探索对象
- **Object Views**：对象详情中心枢纽
- **Vertex**：图形关系分析
- **Map**：地理空间可视化
- **Process Mining (Machinery)**：流程挖掘
- **Dynamic Scheduling**：动态调度
- **Foundry Rules**：业务规则引擎

### 3.5 AIP Logic
- **核心概念**：AI 驱动的逻辑函数
- **Automate AIP Logic**：自动化 AI 逻辑
- **Evaluations**：AI 逻辑评估套件

---

## 4. 用例开发 (Use case development)

### 4.1 应用构建工具

#### Workshop
- **定位**：灵活的面向对象应用构建工具
- **特点**：
  - 无代码/低代码/代码小部件
  - 对象和链接驱动
  - Actions 和 Functions 集成
  - 响应式设计和交互
  - 场景支持
  - 移动端支持

#### Slate
- **定位**：拖拽式应用构建器
- **特点**：
  - 拖放界面
  - HTML/CSS/JavaScript 自定义
  - Handlebars 模板
  - 事件和动作系统
  - 多页面应用
  - 全局样式表

#### OSDK React Applications
- **定位**：完全自定义应用开发
- **特点**：
  - TypeScript/Python/Java SDK
  - 本地开发环境
  - OAuth 认证
  - 完整平台访问

#### Custom Widgets
- **定位**：自定义小部件开发
- **特点**：
  - 参数和事件
  - Workshop 嵌入
  - OSDK 集成

### 4.2 工作流构建

#### Automate
- **功能**：业务自动化
- **特点**：
  - 条件触发（时间/对象数据）
  - 效果执行（Actions/通知）
  - 持续监控
  - Webhook 集成

#### Workflow Builder [Beta]
- **功能**：AI 应用、操作和代理构建
- **特点**：
  - LLM 集成
  - 错误处理和重试
  - 输出架构保证
  - 生产级工具链

#### Carbon
- **功能**：工作空间配置
- **特点**：
  - 定制平台体验
  - 应用集合
  - 导航配置
  - 用户组定制

#### Solution Designer
- **功能**：解决方案架构设计
- **特点**：
  - 交互式图表
  - 集成点表示
  - 文档链接

#### Use Cases [Beta]
- **功能**：用例组织界面
- **特点**：
  - 文件系统视图
  - 本体管理视图
  - 资源管理

### 4.3 开发者工具链

#### Ontology SDK (OSDK)
- **TypeScript SDK**：NPM 包
- **Python SDK**：Pip/Conda 包
- **Java SDK**：Maven/Gradle
- **功能**：
  - 对象类型访问
  - Actions 应用
  - Functions 调用
  - AIP Logic 函数

#### APIs
- **API Gateway**：REST API 接口
- **Query Functions**：查询端点
- **OAuth 认证**：公共/保密客户端

#### FoundryTS
- **功能**：TypeScript 时间序列库
- **API**：
  - 时间序列操作
  - 聚合函数
  - 滚动窗口
  - 预测和插值

#### Cross-application Interactivity
- **拖放**：跨应用数据传输
- **App Pairing**：应用配对
- **Commands**：命令系统

---

## 5. 分析 (Analytics)

### 5.1 Contour
- **定位**：点击式表格分析
- **功能**：
  - 无代码数据转换
  - 分析路径组织
  - 参数化分析
  - 交互式仪表板
  - 数据集导出
  - Contour 表达式语言

### 5.2 Quiver
- **定位**：时间序列和对象数据分析
- **功能**：
  - 时间序列分析
  - 对象数据探索
  - 卡片系统
  - 画布和图形模式
  - 仪表板和模板
  - 批量分析
  - 预测功能

### 5.3 Code Workbook
- **定位**：可视化节点编辑器
- **功能**：
  - 多语言支持
  - 可视化数据流
  - 交互式构建
  - 模板系统
  - 环境配置

### 5.4 Code Workspaces
- **定位**：第三方 IDE 集成
- **支持**：
  - JupyterLab®
  - RStudio® Workbench
  - VS Code
- **功能**：
  - 本体集成
  - 模型训练
  - 数据交互
  - 安全隔离

### 5.5 Notepad
- **定位**：文档和报告生成
- **功能**：
  - 富文本编辑
  - 小部件嵌入
  - 模板系统
  - PDF 导出
  - Workshop 集成

### 5.6 Fusion
- **定位**：电子表格分析
- **功能**：
  - 类 Excel 界面
  - 公式库
  - 数据集同步
  - 实时更新

### 5.7 Forms
- **定位**：表单数据收集
- **功能**：
  - 表单构建器
  - 验证器
  - 数据支持字段
  - 附件上传

### 5.8 BI 连接
- **Power BI®**
- **Tableau**
- **Microsoft Report Builder**
- **Excel**
- **Qlik Sense**
- **MicroStrategy**
- **ODBC & JDBC 驱动**

---

## 6. 产品交付 (Product delivery)

### 6.1 Marketplace
- **功能**：产品发现和安装
- **特点**：
  - 产品打包
  - 版本管理
  - 自动升级
  - 权限控制

### 6.2 产品打包
- **资源集合**：管道、本体、应用、模型
- **Beta 功能**：
  - 添加管道到产品
  - 添加同步到产品
  - 添加虚拟表到产品
  - 添加健康检查到产品
  - 添加工作流到产品
  - 添加本体类型到产品
  - 添加 Workshop 应用到产品
  - 添加 Slate 应用到产品
  - 添加 Carbon 工作空间到产品
  - 添加函数到产品
  - 添加仪表板到产品
  - 添加模板到产品
  - 添加文档到产品
  - 添加自动化到产品

---

## 7. 安全与治理 (Security & governance)

### 7.1 核心安全模型
- **传输中和静态时加密**：全数据加密
- **身份验证**：身份保护控制
- **授权**：基于角色/标记/目的的混合范式
- **审计日志**：健全的安全审计
- **信息治理**：可扩展的管理和隐私控制

### 7.2 数据治理
- **Data Lineage**：数据血缘追踪
- **Data Health**：数据健康检查
- **Linter**：代码质量检查
- **Resource Management**：资源管理

### 7.3 权限管理
- **对象权限**：细粒度对象访问控制
- **受限视图支持**：MDO 对象类型
- **多数据源对象类型**：跨源权限

### 7.4 合规性
- **FedRAMP**：联邦风险和授权管理项目
- **GxP**：良好实践规范
- **SOC 2**：服务组织控制报告

---

## 8. 管理与赋能 (Management & enablement)

### 8.1 平台管理

#### Control Panel
- **功能**：平台配置中心
- **配置**：
  - 组织设置
  - 用户管理
  - 权限配置
  - 平台设置

#### Resource Management
- **功能**：计算和存储资源管理
- **特点**：
  - 资源分配
  - 使用监控
  - 成本优化

#### Upgrade Assistant
- **功能**：平台升级助手
- **特点**：
  - 版本升级
  - 兼容性检查
  - 回滚支持

### 8.2 用户赋能

#### AIP Assist
- **功能**：AI 驱动的助手
- **特点**：
  - 上下文感知建议
  - 代码补全
  - 文档检索
  - 最佳实践指导

#### AIP Bootcamps
- **功能**：加速训练营
- **特点**：
  - 实践操作
  - 数小时内实现 AI 成果
  - 专家指导

---

## 9. 平台能力总结

### 9.1 数据能力
- 200+ 数据源连接器
- 批处理和流式处理
- 零拷贝数据访问
- 自动扩展架构

### 9.2 分析能力
- 点击式和代码式分析
- 时间序列专业分析
- 地理空间分析
- AI/ML 模型集成

### 9.3 应用能力
- 无代码/低代码/全代码
- 响应式设计
- 移动端支持
- 自定义小部件

### 9.4 自动化能力
- 条件触发自动化
- AI 驱动工作流
- 代理编排
- 批量调度

### 9.5 安全能力
- 企业级安全
- 细粒度权限控制
- 完整审计追踪
- 合规性认证

---

## 10. 相关文档索引

| 文档 | 描述 |
|------|------|
| Palantir-Foundry-平台概览.md | 平台整体架构和决策组件 |
| Palantir-PipelineBuilder-概览.md | 数据集成管道构建 |
| Palantir-Workshop-概览.md | 面向对象应用构建 |
| Palantir-Slate-逻辑概览.md | 拖拽式应用构建和逻辑 |
| Palantir-Contour-概览.md | 点击式表格分析 |
| Palantir-Quiver-核心概念.md | 时间序列分析 |
| Palantir-CodeWorkspaces-概览.md | IDE 集成开发环境 |
| Palantir-Functions-概览.md | 业务逻辑函数 |
| Palantir-ObjectViews-概览.md | 对象详情视图 |
| Palantir-Automate-概览.md | 业务自动化 |

---

*本文档基于 Palantir Foundry 官方文档整理*
*文档来源：https://www.palantir.com/docs/foundry/*
