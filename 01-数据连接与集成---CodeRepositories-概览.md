# Code Repositories 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/code-repositories/overview/

## 概述

**Code Repositories** 提供了一个**基于 Web 的集成开发环境 (IDE)**，用于在 Foundry 中编写和协作编写生产就绪代码。

## VS Code 替代方案

要在熟悉的 IDE 中编辑和管理代码，请尝试：
- **VS Code workspaces**：VS Code 工作区
- **Palantir extension for Visual Studio Code**：适用于 Visual Studio Code 的 Palantir 扩展

## 核心功能

### 1. Web IDE

- **基于 Web 的 IDE**：无需本地安装
- **协作编辑**：实时协作编写代码
- **用户友好界面**：易于使用的 Web UI

### 2. Git 版本控制

所有常见的 Git 版本控制任务都可以通过 Web UI 执行：

- **分支**：创建和管理分支
- **提交**：提交代码更改
- **标签发布**：标记版本发布
- **合并**：合并代码更改
- **拉取请求**：代码审查和协作

### 3. 代码审查和协作

- **Pull Requests**：集成代码审查支持
- **权限控制**：高度可配置的权限
- **代码质量**：确保代码库高质量
- **评论和反馈**：内联评论和反馈

### 4. 代码编写支持

每个存储库类型都包含集成的功能以帮助代码编写体验：

- **IntelliSense**：智能代码补全
- **代码检查**：代码检查和错误检测
- **错误检查**：实时错误检查
- **帮助对话框**：丰富的帮助对话框

## 存储库类型

Code Repositories 支持创建多种类型的存储库：

### 1. Transforms 存储库

**用途**：编写数据转换逻辑

**支持语言**：
- Python
- Java
- SQL

**功能**：
- 预览转换
- 调试转换
- 单元测试
- 项目引用

### 2. Functions 存储库

**用途**：编写可以在操作上下文中以低延迟执行的业务逻辑

**支持语言**：
- TypeScript
- Python [Beta]

**功能**：
- 访问 Foundry Ontology 中的数据
- 基于 Ontology 数据类型的自动完成
- 在编写时预览 Functions
- 对象查询和聚合
- Ontology 编辑
- 外部 API 调用

### 3. 模型开发

**用途**：在 Code Repositories 中开发模型

**功能**：
- 训练模型
- 模型评估
- 模型部署
- 模型版本控制

## 工作流程

```
┌─────────────────────────────────────────────────────────────┐
│              Code Repositories 工作流程                       │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. 创建存储库                                               │
│     ↓                                                        │
│  2. 编写代码                                                 │
│     - IntelliSense 自动补全                                │
│     - 实时错误检查                                          │
│     - 代码检查和质量保证                                    │
│     ↓                                                        │
│  3. 预览和调试                                               │
│     - Transforms: 预览转换结果                             │
│     - Functions: 预览 Functions                            │
│     - 单元测试                                              │
│     ↓                                                        │
│  4. 提交代码                                                 │
│     - Git 版本控制                                         │
│     - 分支管理                                             │
│     ↓                                                        │
│  5. 代码审查                                                 │
│     - Pull Requests                                        │
│     - 代码审查                                              │
│     - 权限控制                                              │
│     ↓                                                        │
│  6. 合并和发布                                               │
│     - 合并到主分支                                          │
│     - 标签发布                                              │
│     - 部署到生产                                            │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 导航

### 主界面

- **存储库列表**：查看所有存储库
- **存储库详情**：查看存储库详情
- **代码编辑器**：编写和编辑代码
- **Git 历史**：查看提交历史
- **Pull Requests**：管理拉取请求

### 配置

在 Control Panel 中配置 Code Repositories 设置：
- **存储库设置**：配置全局存储库设置
- **权限**：配置存储库权限
- **资源限制**：配置计算资源使用

## 高级功能

### 1. 项目引用

- **跨项目引用**：引用其他项目的代码
- **依赖管理**：管理代码依赖关系

### 2. 单元测试

- **测试框架集成**：集成测试框架
- **测试执行**：运行单元测试
- **测试报告**：查看测试结果

### 3. 库管理

- **共享库**：共享代码库
- **版本控制**：管理库版本
- **依赖注入**：注入依赖项

### 4. Artifact Repositories

- **发布 Artifacts**：发布构建产物
- **版本管理**：管理 Artifact 版本
- **依赖解析**：解析 Artifact 依赖

### 5. CI/CD

- **自动构建**：代码提交时自动构建
- **自动测试**：自动运行测试
- **自动部署**：自动部署到生产

## 安全和治理

### 权限管理

- **存储库级别权限**：控制存储库访问
- **分支权限**：控制分支操作
- **Pull Request 权限**：控制代码审查权限

### 代码质量

- **代码检查**：自动代码检查
- **质量门禁**：质量标准检查
- **安全扫描**：安全漏洞扫描

## 最佳实践

### 1. 存储库组织

- **按项目组织**：按项目组织存储库
- **按功能组织**：按功能模块组织代码
- **命名约定**：使用一致的命名约定

### 2. 分支策略

- **主分支保护**：保护主分支
- **功能分支**：使用功能分支
- **发布分支**：使用发布分支

### 3. 代码审查

- **强制审查**：要求代码审查
- **审查者**：指定代码审查者
- **审查标准**：定义审查标准

### 4. 测试

- **单元测试**：编写单元测试
- **集成测试**：编写集成测试
- **测试覆盖率**：监控测试覆盖率

## 与其他工具集成

### Pipeline Builder

- 导出管道逻辑到 Code Repositories
- 使用 Code Repositories 中的自定义转换

### Functions

- 在 Functions 存储库中编写函数
- 发布 Functions 到 Ontology

### VS Code Workspaces

- 在本地 VS Code 中编辑代码
- 使用 Palantir 扩展进行集成

## 相关文档

- [Navigation](https://palantir.com/docs/foundry/code-repositories/navigation/) - 导航指南
- [Transforms](https://palantir.com/docs/foundry/code-repositories/transforms/) - 转换详解
- [Unit tests](https://palantir.com/docs/foundry/code-repositories/unit-tests/) - 单元测试
- [Libraries](https://palantir.com/docs/foundry/code-repositories/libraries/) - 库管理
- [AIP features](https://palantir.com/docs/foundry/code-repositories/aip-features/) - AIP 功能

---

*本文档基于 Palantir Foundry 官方文档整理*
