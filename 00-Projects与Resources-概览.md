# Projects 与 Resources 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/getting-started/projects-and-resources/

## 概述

**Projects 和 Resources** 是 Palantir 平台的构建块，由 **Compass 应用程序**提供支持。

## Resources（资源）

### 定义和概念

**资源**是平台中的基本单元，类似于传统系统中的"文件"。

在 Palantir 平台中，我们使用"资源"一词以避免混淆，因为某些资源（如数据集或代码存储库）本身可以包含文件。

### 资源类型

资源包括：

| 资源类型 | 说明 |
|---------|------|
| **Datasets（数据集）** | 数据连接或转换的输出，或手动上传的数据 |
| **Repositories（存储库）** | 代码存储库 |
| **Analyses（分析）** | 分析文件 |
| **Reports（报告）** | 报告文件 |
| **Applications（应用程序）** | 应用程序工件 |

### 资源特征

虽然每种资源类型在不同的平台应用程序中打开，但资源共享一些通用信息：

#### 通用信息

- **最后更新者**：谁最后更新了资源
- **更新时间**：何时更新
- **访问控制**：不同级别的用户访问
- **注释**：离开注释
- **收藏**：标记收藏
- **操作**：移动、共享、删除

#### RID（资源标识符）

- **唯一标识符**：每个资源都有一个唯一的 RID
- **标准化**：在应用程序中标准化
- **引用**：用于引用资源

## Projects（项目）

### 定义和概念

**项目**是资源的容器，形成相关资源组之间的边界，并提供支持协作的功能。

```
┌─────────────────────────────────────────────────────────────┐
│                  Project 结构                               │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Project                                                    │
│  ├── Users & Groups（用户和组）                            │
│  ├── Permissions（权限）                                   │
│  │   ├── Viewer（查看者）                                  │
│  │   ├── Editor（编辑者）                                  │
│  │   └── Owner（所有者）                                   │
│  ├── Folders（文件夹）                                     │
│  ├── Resources（资源）                                     │
│  ├── Activity（活动）                                      │
│  └── Metadata（元数据）                                    │
│      ├── Documentation（文档）                             │
│      ├── Key resources（关键资源）                         │
│      └── Data health（数据健康）                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 项目功能

#### 1. 权限管理

- **访问控制**：管理谁可以访问项目资源
- **角色分配**：
  - **Viewer（查看者）**：查看资源
  - **Editor（编辑者）**：编辑资源
  - **Owner（所有者）**：完全控制
- **用户和组**：用户或组列表

#### 2. 协作功能

- **活动跟踪**：显示最新的项目活动
- **使用指标**：关于使用情况的指标
- **元数据管理**：
  - 文档
  - 关键资源
  - 数据健康

#### 3. 组织结构

- **文件夹**：将资源组织到文件夹中
- **层级结构**：提供进一步的结构
- **保持整洁**：保持内容整洁

### 项目类型

#### 1. 协作项目

- **团队协作**：为协作创建的项目
- **共享访问**：多人访问
- **团队资源**：共享团队资源

#### 2. 个人项目

- **自动创建**：每个用户都有一个个人项目
- **默认位置**：创建的资源默认出现在个人项目中
- **访问方式**：
  1. 从工作区导航侧边栏导航到 **Files**
  2. 选择 **Projects**
  3. 找到您的个人项目

## 资源组织

### 文件夹结构

```
Project
├── Folder 1
│   ├── Resource A
│   ├── Resource B
│   └── Subfolder
│       └── Resource C
├── Folder 2
│   └── Resource D
└── Resource E
```

### 组织最佳实践

#### 1. 按功能组织

- **数据管道**：数据相关资源
- **分析**：分析文件
- **应用**：应用程序资源

#### 2. 按团队组织

- **团队 A**：团队 A 的资源
- **团队 B**：团队 B 的资源
- **共享**：共享资源

#### 3. 按生命周期组织

- **开发**：开发中资源
- **测试**：测试资源
- **生产**：生产资源

## 资源操作

### 常见操作

| 操作 | 说明 |
|------|------|
| **创建** | 创建新资源 |
| **查看** | 查看资源详情 |
| **编辑** | 编辑资源内容 |
| **移动** | 移动资源到新位置 |
| **共享** | 与其他用户共享资源 |
| **删除** | 删除资源（移至垃圾箱） |
| **收藏** | 标记为收藏 |
| **评论** | 添加评论 |

## Compass 应用程序

Compass 是管理 Projects 和 Resources 的核心应用程序。

### 功能

- **资源管理**：创建、查看、编辑资源
- **项目管理**：创建和管理项目
- **权限设置**：配置访问权限
- **活动监控**：查看项目活动
- **元数据编辑**：编辑项目元数据

## 安全和权限

### 权限模型

#### 项目级别

- **Owner**：完全控制
  - 管理项目设置
  - 添加/删除用户
  - 分配角色
- **Editor**：编辑资源
  - 创建和编辑资源
  - 查看项目信息
- **Viewer**：仅查看
  - 查看资源
  - 查看项目信息

#### 资源级别

- **继承权限**：从项目继承
- **显式权限**：在资源级别设置
- **受限视图**：支持受限视图

## 使用场景

### 1. 数据管道项目

**结构**：
```
Data Pipeline Project
├── Raw Data/
│   ├── Source A Dataset
│   └── Source B Dataset
├── Transformed Data/
│   ├── Cleaned Dataset
│   └── Aggregated Dataset
├── Code/
│   ├── Transform Repository
│   └── Test Repository
└── Documentation/
    └── Pipeline Docs
```

### 2. 分析项目

**结构**：
```
Analytics Project
├── Data Sources/
├── Analyses/
│   ├── Contour Analysis
│   └── Quiver Dashboard
├── Reports/
└── Notes/
```

### 3. 应用开发项目

**结构**：
```
App Development Project
├── Frontend/
│   ├── Workshop Modules
│   └── Custom Widgets
├── Backend/
│   ├── Functions
│   └── Logic Flows
└── Documentation/
```

## 最佳实践

### 1. 项目规划

- **清晰范围**：定义清晰的项目范围
- **团队结构**：与团队结构对齐
- **命名约定**：使用一致的命名约定

### 2. 权限管理

- **最小权限**：使用最小权限原则
- **角色分离**：分离 Viewer、Editor、Owner
- **定期审查**：定期审查访问权限

### 3. 资源组织

- **文件夹结构**：使用清晰的文件夹结构
- **命名规范**：使用描述性名称
- **版本控制**：对代码资源使用版本控制

### 4. 文档记录

- **项目文档**：维护项目文档
- **关键资源**：标记关键资源
- **数据健康**：监控数据健康

## 与其他功能集成

### Ontology

- **对象类型**：对象类型定义存储在项目中
- **链接类型**：链接类型定义
- **Actions**：Action 定义

### Pipeline Builder

- **管道**：管道存储在项目中
- **转换**：转换逻辑
- **数据集**：输入和输出数据集

### Code Repositories

- **存储库**：代码存储库
- **分支**：代码分支
- **版本**：代码版本

## 相关文档

- [Compass](https://palantir.com/docs/foundry/compass/overview/) - Compass 应用程序
- [Projects and roles](https://palantir.com/docs/foundry/security/projects-and-roles/) - 项目和角色
- [Organizations and spaces](https://palantir.com/docs/foundry/security/orgs-and-spaces/) - 组织和空间
- [Recommended project structure](https://palantir.com/docs/foundry/building-pipelines/recommended-project-structure/) - 推荐的项目结构

---

*本文档基于 Palantir Foundry 官方文档整理*
