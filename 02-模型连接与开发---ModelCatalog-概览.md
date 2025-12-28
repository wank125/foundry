# Model Catalog 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/model-catalog/overview/

## 概述

**Model Catalog（模型目录）** 是 Foundry 中的 AIP 应用程序，旨在帮助发现和定位所有 Palantir 提供的模型。

## 核心功能

### 1. 模型发现

- **查看可用模型**：查看 AIP 中可用的所有模型
- **发现新模型**：发现新添加的模型
- **模型筛选**：通过多种筛选条件过滤模型

### 2. 模型选择

- **用例匹配**：为您的用例选择正确的模型
- **性能比较**：即将提供更多工具和基准测试用于比较和决策
- **推荐系统**：基于用例的模型推荐

### 3. 快速入门

- **基本模板**：使用基本模板开始工作流
- **Marketplace 模板**：通过 Marketplace 使用完整的用例模板
- **预配置资源**：创建已填充所需内容的资源

### 4. 模型测试

- **沙盒/游乐场**：使用沙盒/游乐场测试不同模型
- **交互式测试**：交互式测试模型
- **比较评估**：比较不同模型的性能

## 模型范围

### 当前包含

- ✅ **LLMs（大语言模型）**：所有大型语言模型

### 当前不包含

- ❌ **自定义 ML/AI 模型**：不在 Model Catalog 中
  - 在 **Modeling Objectives** 中查找 ML/AI 模型

## 界面视图

Model Catalog 有两个主要视图：

```
┌─────────────────────────────────────────────────────────────┐
│              Model Catalog 界面结构                         │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. Model Catalog Homepage（模型目录主页）                  │
│     ├── 模型列表                                           │
│     ├── 筛选器                                             │
│     └── 搜索功能                                           │
│                                                             │
│  2. Model Entity Page（模型实体页面）                       │
│     ├── Playground（游乐场）                               │
│     ├── How to use it（使用指南）                          │
│     └── Model description（模型描述）                      │
│                                                             │
│  3. Model Comparison Page（模型比较页面）                   │
│     ├── 并排比较                                           │
│     ├── 性能测试                                           │
│     └── 基准评估                                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## Model Catalog 主页

主页是一个发现和导航界面，显示用户在 Foundry 注册中可用的所有大语言模型。

### 筛选选项

#### 1. Lifecycle Status（生命周期状态）

| 状态 | 说明 | 用途 |
|------|------|------|
| **Experimental（实验性）** | 提供商或 Palantir 标记为实验性 | 探索和测试，API 可能变化 |
| **Stable（稳定）** | 提供商和 Palantir 认可的可靠模型 | 生产环境长期使用 |
| **Sunset（日落）** | 即将弃用的模型 | 现有工作流，不能创建新工作流 |
| **Deprecated（已弃用）** | 已移除的模型 | 仅保留历史数据和日志 |

**Experimental 模型**：
- API 可能变化
- Token 容量可能受限
- AIP 应用中的行为可能不完全支持
- 其他不稳定行为
- 用于探索和测试

**Stable 模型**：
- 强大的功能
- 保证支持
- 长期生产使用
- 满足 Palantir 的性能和可用性标准

**Sunset 模型**：
- 即将弃用
- 不能支持新工作流
- 可能仍支持现有工作流
- 技术支持水平降低

**Deprecated 模型**：
- 已从 Foundry 移除
- 不能支持现有工作流
- 必须迁移到稳定模型
- 保留历史数据和日志

#### 2. Type（类型）

| 类型 | 说明 | 示例 |
|------|------|------|
| **Completion model（补全模型）** | 通过预测和完成输入文本生成上下文相关文本 | GPT-4 Turbo, Mixtral 8x7B, Llama2 70B Chat |
| **Embedding model（嵌入模型）** | 将离散数据转换为连续向量表示 | text-embedding-ada-002, Instructor Large |
| **Vision model（视觉模型）** | 分析和解释视觉输入 | GPT-4 Vision, Gemini Pro Vision |

#### 3. Model Creator（模型创建者）

模型创建者是负责创建、开发和维护特定 LLM 的组织：

- **OpenAI**：直接或通过 Azure
- **Anthropic**：直接或通过 AWS
- **Google Gemini**：Google 提供
- **Mixtral AI**：Mixtral AI 提供
- **Palantir 托管**：Llama、Mixtral 等

## 模型实体页面

每个模型都有一个实体页面，包含三个主要部分：

### 1. Playground（游乐场）

- **用途**：构建者试用不同模型的界面
- **功能**：
  - 测试模型响应
  - 比较提示词效果
  - 调整参数

### 2. How to use it（使用指南）

- **快速入门**：创建已填充构建工作流所需内容的资源
- **当前支持**：
  - **Functions**：创建 Functions
  - **Transforms**：创建 Transforms

### 3. Model description（模型描述）

- **基本信息**：模型描述
- **法律声明**：法律免责声明
- **技术规格**：
  - **上下文窗口**：Token 限制
  - **训练数据截止**：训练数据截止日期
  - **其他技术细节**

## 模型比较页面

Model Catalog 比较页面允许构建者高效地比较和评估各种 LLM 的性能。

### 功能

- **选择两个 LLM**：选择两个大语言模型
- **相同任务测试**：在相同的补全或视觉任务上测试
- **性能评估**：评估和比较性能
- **决策支持**：做出明智的决策

## 模型启用

### 启用方式

如果模型不可用或显示为灰色，表示该模型未为您的注册启用。

**启用步骤**：
1. 联系平台管理员
2. 或联系 Palantir 代表
3. 请求启用特定模型

### 控制选项

注册管理员可以在 Control Panel 的 **AIP settings** 部分为注册启用或禁用模型：

- **启用/禁用 Experimental 模型**
- **仅显示 Stable 模型**
- **区域可用性控制**

## 模型可用性

### 区域可用性

模型的区域可用性根据模型提供商的产品而异：

- 参考 **supported LLMs 文档**中的模型可用性综合列表
- 在 **Model Selector** 中查看每个模型的状态信息

### 模型弃用

Palantir 通过 **Upgrade Assistant** 通知用户模型变更：

- 从 Stable 移至 Sunset
- 从 Sunset 移至 Deprecated
- 提供迁移指导

## 使用场景

### 1. 内容生成

**推荐模型**：Completion models
- GPT-4 Turbo
- Llama2 70B Chat
- Mixtral 8x7B

**用例**：
- 内容创作
- 自动补全
- 翻译
- 问答

### 2. 语义搜索

**推荐模型**：Embedding models
- text-embedding-ada-002
- Instructor Large

**用例**：
- 语义搜索
- 信息检索
- 文档相似度

### 3. 计算机视觉

**推荐模型**：Vision models
- GPT-4 Vision
- Gemini Pro Vision

**用例**：
- 图像识别
- 图像分类
- 视频分析

## 工作流程

```
┌─────────────────────────────────────────────────────────────┐
│            Model Catalog 工作流程                           │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. 发现模型                                                │
│     ├── 浏览模型列表                                       │
│     ├── 使用筛选器                                         │
│     └── 阅读模型描述                                       │
│     ↓                                                        │
│  2. 比较模型                                                │
│     ├── 选择候选模型                                       │
│     ├── 使用游乐场测试                                     │
│     └── 比较性能                                           │
│     ↓                                                        │
│  3. 选择模型                                                │
│     ├── 确定最佳模型                                       │
│     ├── 检查可用性                                         │
│     └── 启用模型                                           │
│     ↓                                                        │
│  4. 开始构建                                                │
│     ├── 使用快速入门模板                                   │
│     ├── 创建 Functions 或 Transforms                       │
│     └── 集成到工作流                                       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 最佳实践

### 1. 模型选择

- **用例匹配**：根据用例选择合适的模型类型
- **性能评估**：使用游乐场评估模型性能
- **成本考虑**：考虑 Token 成本
- **区域可用性**：确认模型在您的区域可用

### 2. 测试策略

- **比较测试**：比较多个模型
- **真实数据**：使用真实数据测试
- **边界情况**：测试边界情况
- **性能基准**：建立性能基准

### 3. 迁移规划

- **弃用通知**：关注弃用通知
- **升级助手**：使用 Upgrade Assistant 规划迁移
- **提前迁移**：在弃用前迁移
- **测试验证**：迁移后充分测试

## 与其他功能集成

### AIP Logic

- **LLM 块**：在 AIP Logic 中使用模型
- **函数构建**：构建 LLM 驱动的函数

### Functions

- **快速入门**：创建使用模型的 Functions
- **模板支持**：使用预配置模板

### Transforms

- **数据处理**：在 Transforms 中使用模型
- **批量处理**：批量处理数据

### Marketplace

- **用例模板**：访问完整的用例模板
- **最佳实践**：学习最佳实践

## 限制

### 当前限制

- **LLMs only**：当前仅包含 LLMs
- **自定义模型**：不包含自定义 ML/AI 模型
- **区域限制**：模型可用性受区域限制

## 相关文档

- [Model deprecation](https://palantir.com/docs/foundry/model-catalog/model-deprecation/) - 模型弃用
- [Supported LLMs](https://palantir.com/docs/foundry/aip/supported-llms/) - 支持的 LLMs
- [AIP overview](https://palantir.com/docs/foundry/aip/overview/) - AIP 概述
- [Bring your own model](https://palantir.com/docs/foundry/aip/bring-your-own-model/) - 自带模型

---

*本文档基于 Palantir Foundry 官方文档整理*
