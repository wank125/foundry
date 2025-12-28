# Notepad 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/notepad/overview/

## 概述

**Notepad** 是一个**对象感知的协作富文本编辑器**。除了添加和格式化文本和图像等内容外，还可以集成来自其他 Foundry 应用程序（如 Contour、Quiver、Code Workbook 和 Object Explorer）的小部件（如图表或对象）。

## 核心功能

### 1. 嵌入内容

- **嵌入图表、表格和图形**：从其他 Foundry 应用程序嵌入
- **集成小部件**：支持多种 Foundry 应用小部件
- **动态链接**：与嵌入的对象和资源保持结构化链接

### 2. 导出和打印

- **导出控制**：对导出展示进行细粒度控制
- **嵌入外观**：控制嵌入内容的显示方式
- **分页符**：精确控制打印布局
- **PDF 导出**：导出为 PDF 格式

### 3. 对象感知

- **链接到对象**：自动丰富底层 Ontology
- **对象属性**：嵌入对象属性和卡片
- **媒体预览**：对象媒体预览

### 4. 内容冻结

- **快照**：捕获特定时间点的内容
- **版本历史**：跟踪文档更改
- **锁定数据**：锁定小部件数据以防止更改

### 5. 模板化

- **文档模板**：创建文档模板
- **模板输入**：定义模板输入参数
- **批量生成**：基于新输入生成新文档

## 使用场景

### 适合的场景

#### 1. 临时笔记 (Ad-hoc note taking)

- 在调查工作流程中捕获笔记
- 在嵌入内容旁边添加注释
- 快速记录想法和观察

#### 2. 平台内文档 (In-platform documentation)

- 记录数据管道
- 记录数据集
- 记录应用程序
- 创建技术文档

#### 3. 定期报告 (Periodic reporting)

- 生成月度状态报告
- 使用模板创建标准化报告
- 自动化报告生成

#### 4. 模板化导出 (Templated exports)

- 按需创建文档模板的新副本
- 基于选定对象生成文档
- 批量文档生成

### 不适合的场景

#### 1. 创建仪表板

**原因**：Notepad 不支持基于用户输入或图表选择的动态过滤

**推荐替代方案**：
- 对象或时间序列数据：**Quiver Dashboards**
- 表格数据：**Contour Dashboards**
- 高级操作应用：**Workshop**

#### 2. 复杂的基于页面的富文本编辑

**原因**：Notepad 不提供典型桌面文本编辑器的可配置性

**说明**：Notepad 旨在成为一个易于接近的文本编辑器，针对与 Foundry 平台其余部分的集成进行了优化

## 集成能力

### 与 Foundry 应用集成

| 应用 | 集成方式 |
|------|----------|
| **Contour** | 嵌入图表 |
| **Quiver** | 嵌入图表和仪表板 |
| **Code Workbook** | 嵌入图表 |
| **Object Explorer** | 嵌入对象属性和卡片 |
| **Vertex** | 嵌入图形 |
| **Map** | 嵌入地图 |

### 与 Workshop 集成

- **嵌入文档**：在 Workshop 模块中嵌入文档
- **显示链接文档**：显示链接到选定对象的所有文档
- **生成和导出文档**：从模板或 Workshop 字符串变量创建和导出文档
- **导出现有文档**：导出现有 Notepad 文档

## 小部件

Notepad 支持多种小部件：

### 导航和链接

- **Anchor link**：锚点链接
- **Resource link**：资源链接
- **Command**：命令

### 内容

- **Image**：图像
- **Table**：表格
- **Horizontal rule**：水平线
- **Page break**：分页符

### 对象相关

- **Object property**：对象属性
- **Object card**：对象卡片
- **Object media preview**：对象媒体预览
- **Object property Markdown editor**：对象属性 Markdown 编辑器

### Foundry 应用集成

- **Contour chart**：Contour 图表
- **Code Workbook chart**：Code Workbook 图表
- **Quiver chart**：Quiver 图表
- **Quiver dashboard**：Quiver 仪表板
- **Vertex graph**：Vertex 图形
- **Map**：地图

### 动态内容

- **Value embed**：值嵌入
- **Functions**：函数
- **Section generator**：部分生成器
- **Table row generator**：表格行生成器
- **Conditional section**：条件部分

### 协作

- **Current date**：当前日期
- **User mention**：用户提及
- **LaTeX**：LaTeX 公式

## 模板功能

### 模板创建

- **蓝图**：作为生成新文档的蓝图
- **输入**：接受字符串、对象等输入
- **连接**：将输入连接到小部件

### 模板发布

- **发布模板**：发布模板以供使用
- **版本控制**：管理模板版本
- **权限**：控制模板访问权限

## 文档管理

### 版本历史

- **跟踪更改**：查看文档的所有版本
- **比较版本**：比较不同版本的差异
- **恢复**：恢复到以前的版本

### 协作

- **共享**：与其他用户共享文档
- **评论**：添加评论和反馈
- **共同编辑**：实时协作编辑

## 相关文档

- [Getting started](https://palantir.com/docs/foundry/notepad/getting-started/) - 入门指南
- [Embed widgets](https://palantir.com/docs/foundry/notepad/embed-widgets/) - 嵌入小部件
- [Templates](https://palantir.com/docs/foundry/notepad/templates-overview/) - 模板概述
- [Workshop integration](https://palantir.com/docs/foundry/notepad/workshop-templates/) - Workshop 集成
- [Export to PDF](https://palantir.com/docs/foundry/notepad/export-to-pdf/) - PDF 导出

---

*本文档基于 Palantir Foundry 官方文档整理*
