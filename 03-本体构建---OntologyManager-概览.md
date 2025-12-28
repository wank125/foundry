# Ontology Manager 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/ontology-manager/overview/

## 概述

**Ontology Manager**（有时称为本体管理应用程序，或 OMA）允许用户构建和维护组织的 Ontology。Ontology Manager 可用于与 Ontology 相关的广泛活动，从创建新的对象类型和定义新的行动类型，到将数据连接到 Ontology，以及调查数据是否在用户应用程序中更新。

## 访问应用

可以通过三种方式访问应用：

1. 从工作区侧边栏的 **Apps** 部分选择 **Ontology Manager** 图标
2. 在 Data Lineage 中右键单击对象类型并选择 **Configure object type**
3. 在 Foundry 主页 URL 末尾添加 `/workspace/ontology`

## 用户界面

Ontology Manager 界面分为以下元素：

### 1. Ontology Manager 导航

顶部栏和侧边栏是持久的导航元素：

**顶部栏**功能：
- 搜索 Ontology 资源
- 创建新的 Ontology 资源
- 在分支之间导航或创建新分支

**侧边栏**：
- 提供对不同资源、页面或应用程序的导航

### 2. Discover 视图

高度可定制的主页，默认显示：
- 收藏的对象类型
- 最近查看的对象类型
- 收藏的组

**自定义功能**：
- 配置页面上显示的部分
- 控制每个部分中显示的项目数量
- 为特定组添加单独的部分

### 3. Object type 视图

选择对象类型时打开对象类型视图，包含：

**Overview 页面部分**：
1. **Object type metadata** - 对象类型元数据
2. **Properties** - 属性
3. **Action types** - 行动类型
4. **Link type graph** - 链接类型图
5. **Dependents** - 依赖项
6. **Data** - 数据
7. **Usage** - 使用情况

### 4. Property editor 视图

从对象类型的 **Overview** 页面的 **Properties** 部分选择属性时打开。

### 5. Link type 视图

从对象类型的 **Overview** 选项卡的链接类型图选择链接类型时打开，包含：
- **Overview** 页面
- **Datasources** 页面

### 6. Action type 视图

从对象类型的 **Overview** 选项卡的行动类型部分选择行动类型时打开，包含：
- **Overview** 页面
- **Logic** 页面

### 7. Function type 视图

从对象类型的 **Overview** 选项卡的函数类型部分选择函数类型时打开。

**功能**：
- **Usage History** - 记录使用任何版本函数的应用程序
- **版本选择** - 使用版本下拉选择器查看其他版本
- **Code Repository 导航** - 通过 **Open in Code Repository** 按钮导航到 Functions Code Repository

## 核心功能

### 对象类型管理

- **创建对象类型**：定义企业实体
- **编辑对象类型**：修改对象类型配置
- **复制配置**：复制对象类型配置
- **属性管理**：添加、编辑和管理对象属性
- **值类型**：创建和管理值类型

### 链接类型管理

- **创建链接类型**：定义实体之间的关系
- **编辑链接类型**：修改链接类型配置
- **链接类型图**：可视化对象之间的关系

### 行动类型管理

- **定义行动**：定义用户可以对对象执行的操作
- **参数配置**：配置行动的输入参数
- **提交标准**：设置行动验证规则
- **副作用**：配置通知、Webhook 等

### 函数类型管理

- **函数版本**：管理不同版本的函数
- **使用历史**：查看函数使用情况
- **代码管理**：链接到 Functions Code Repository

## 分支管理

Ontology Manager 支持分支功能：
- 创建新分支
- 在分支间切换
- 合并分支更改

## 权限管理

- **项目级权限**：管理对 Ontology 资源的访问
- **角色迁移**：从旧权限系统迁移
- **权限配置**：配置不同用户和组的权限

## 使用情况查看

Ontology Manager 可以配置为显示对象类型和链接类型的使用指标：
- **Reads**：应用程序加载对象类型时记录读取
- **其他指标**：写入、更新等操作统计

## 导出和导入

- **导出 Ontology**：将 Ontology 导出为 JSON 文件
- **编辑**：使用代码编辑器或文本编辑器编辑
- **导入**：将编辑后的 Ontology 导回 Foundry

## 相关文档

- [Object types](https://palantir.com/docs/foundry/object-and-link-types/object-types/) - 对象类型详解
- [Action types](https://palantir.com/docs/foundry/action-types/overview/) - 行动类型详解
- [Properties](https://palantir.com/docs/foundry/object-and-link-types/properties/) - 属性详解
- [Link types](https://palantir.com/docs/foundry/object-and-link-types/link-types/) - 链接类型详解
- [Value types](https://palantir.com/docs/foundry/object-and-link-types/value-types/) - 值类型详解

---

*本文档基于 Palantir Foundry 官方文档整理*
