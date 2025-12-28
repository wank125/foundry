# Palantir Foundry 中文文档

> Palantir Foundry 平台核心组件中文概览文档

## 项目简介

本项目是 Palantir Foundry 平台的中文文档集合，涵盖了平台的核心组件和功能模块。文档基于 Palantir Foundry 官方文档整理，帮助中文用户快速了解和使用 Foundry 平台。

## 目录结构

```
foundry/
├── 00-*                          # 平台概览
│   ├── 00-Foundry-平台概览.md
│   ├── 00-Foundry-组件概览.md
│   ├── 00-AIP-技术架构.md
│   ├── 00-Projects与Resources-概览.md
│   └── 00-公司定位与产品体系.md
│
├── 01-数据连接与集成---*/          # 数据连接与集成
│   ├── DataConnection-概览.md
│   ├── CodeRepositories-概览.md
│   ├── PipelineBuilder-概览.md
│   └── HyperAuto-概览.md
│
├── 02-模型连接与开发---*/          # 模型连接与开发
│   ├── AIPAgentStudio-概览.md
│   ├── AIPLogic-概览.md
│   ├── ModelCatalog-概览.md
│   ├── ModelingObjectives-概览.md
│   └── CodeWorkspaces-概览.md
│
├── 03-本体构建---*/                # Ontology 构建
│   ├── OntologyManager-概览.md
│   ├── ActionTypes-概览.md
│   ├── Functions-概览.md
│   ├── FoundryRules-概览.md
│   ├── ObjectExplorer-概览.md
│   ├── ObjectViews-概览.md
│   ├── Vertex-概览.md
│   ├── Map-概览.md
│   ├── Machinery-ProcessMining-概览.md
│   └── DynamicScheduling-概览.md
│
├── 04-用例开发---*/                # 用例开发
│   ├── 应用构建---*/
│   │   ├── Workshop-概览.md
│   │   ├── Slate-概览.md
│   │   ├── OSDK-概览.md
│   │   ├── OSDK-React-概览.md
│   │   ├── CustomWidgets-概览.md
│   │   └── CrossAppInteractivity-概览.md
│   ├── 工作流构建---*/
│   │   ├── WorkflowLineage-概览.md
│   │   ├── SolutionDesigner-概览.md
│   │   ├── Automate-概览.md
│   │   └── Carbon-概览.md
│   └── 开发者工具链---*/
│       ├── APIs-概览.md
│       └── FoundryTS-概览.md
│
├── 05-分析---*/                    # 分析
│   ├── Contour-概览.md
│   ├── Quiver-核心概念.md
│   ├── Fusion-概览.md
│   ├── Notepad-概览.md
│   ├── Forms-[Sunset]-概览.md
│   └── CodeWorkbook-[Legacy]-概览.md
│
├── 06-产品交付---*/                # 产品交付
│   └── Marketplace-概览.md
│
├── 07-安全与治理---*/              # 安全与治理
│   ├── DataLineage-概览.md
│   ├── DataHealth-概览.md
│   ├── HealthChecks-概览.md
│   ├── AccessControl-概览.md
│   └── Linter-概览.md
│
├── 08-管理与赋能---*/              # 管理与赋能
│   ├── ControlPanel-概览.md
│   ├── ResourceManagement-概览.md
│   ├── AIPAssist-概览.md
│   └── UpgradeAssistant-概览.md
│
└── images/                        # 架构图
    └── foundry/platform-overview/
```

## 文档统计

| 模块 | 文档数量 | 说明 |
|------|----------|------|
| 00 - 平台概览 | 5 | 平台整体介绍和架构 |
| 01 - 数据连接与集成 | 4 | 数据连接、管道构建 |
| 02 - 模型连接与开发 | 5 | AI/ML 模型开发 |
| 03 - 本体构建 | 10 | Ontology 核心组件 |
| 04 - 用例开发 | 11 | 应用和工作流开发 |
| 05 - 分析 | 6 | 数据分析应用 |
| 06 - 产品交付 | 1 | Marketplace |
| 07 - 安全与治理 | 5 | 安全、治理、监控 |
| 08 - 管理与赋能 | 4 | 平台管理和支持 |
| **总计** | **54** | |

## 快速导航

### 平台概览
- [Foundry 平台概览](00-Foundry-%E5%B9%B3%E5%8F%B0%E6%A6%82%E8%A7%88.md)
- [Foundry 组件概览](00-Foundry-%E7%BB%84%E4%BB%B6%E6%A6%82%E8%A7%88.md)

### 核心组件
- [Ontology Manager](03-%E6%9C%AC%E4%BD%93%E6%9E%84%E5%BB%BA---OntologyManager-%E6%A6%82%E8%A7%88.md) - 本体管理
- [Workshop](04-%E7%94%A8%E4%BE%8B%E5%BC%80%E5%8F%91---%E5%BA%94%E7%94%A8%E6%9E%84%E5%BB%BA---Workshop-%E6%A6%82%E8%A7%88.md) - 应用构建
- [Pipeline Builder](01-%E6%95%B0%E6%8D%AE%E8%BF%9E%E6%8E%A5%E4%B8%8E%E9%9B%86%E6%88%90---PipelineBuilder-%E6%A6%82%E8%A7%88.md) - 数据管道
- [AIP Agent Studio](02-%E6%A8%A1%E5%9E%8B%E8%BF%9E%E6%8E%A5%E4%B8%8E%E5%BC%80%E5%8F%91---AIPAgentStudio-%E6%A6%82%E8%A7%88.md) - AI 代理开发

## 功能模块

### 1. 数据连接与集成
- **Data Connection** - 连接 200+ 数据源
- **Pipeline Builder** - 构建数据转换管道
- **Code Repositories** - 代码版本管理
- **HyperAuto** - 自动化数据集成 (ERP/CRM)

### 2. 模型连接与开发
- **AIP Agent Studio** - 构建 AI 代理
- **AIP Logic** - LLM 驱动的函数
- **Model Catalog** - 发现和管理模型
- **Modeling Objectives** - ML 模型生命周期管理

### 3. Ontology 构建
- **Ontology Manager** - 定义业务概念
- **Object Types** - 对象类型定义
- **Link Types** - 关系类型定义
- **Action Types** - 操作定义
- **Functions** - 对象函数

### 4. 用例开发
- **Workshop** - 无代码应用构建
- **Slate** - 拖放式应用开发
- **OSDK** - 开发者工具包
- **Automate** - 工作流自动化
- **Workflow Lineage** - 工作流管理

### 5. 分析
- **Contour** - 表格数据分析
- **Quiver** - 对象和时间序列分析
- **Fusion** - 类 Excel 体验
- **Notepad** - 文档和报告

### 6. 安全与治理
- **Data Lineage** - 数据血缘
- **Access Control** - 访问控制
- **Health Checks** - 数据质量监控

## 贡献指南

欢迎提交问题和改进建议！

## 许可证

本文档基于 Palantir Foundry 官方文档整理，仅供学习参考。

## 相关链接

- [Palantir Foundry 官方文档](https://palantir.com/docs/foundry/)
- [Palantir 官方网站](https://www.palantir.com/)

---

*最后更新：2025-12-28*
