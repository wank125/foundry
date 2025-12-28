# Map 概览

> 来源：https://www.palantir.com/docs/foundry/map/overview/
> 分类：本体构建 / 地理空间分析

## 概述

**Map** 应用程序提供强大的地理空间和时间分析与可视化功能，允许您将 Foundry 中的数据集成到连贯的地理空间体验中：

- 探索地理空间对象之间的连接，遍历物理网络
- 使用边界框和多边形相交查询，对点和多边形数据进行地理空间搜索
- 可视化来自各种来源的上下文地理空间数据，包括大规模矢量数据和卫星图像，以及对象随时间移动的路径和时间数据等时间数据
- 通过绘制形状和执行地理空间操作进行交互
- 使用地图模板构建地理空间应用程序

![Map 应用程序](https://www.palantir.com/docs/resources/foundry/map/map-overview.png)

## 地图上的地理空间数据

Map 应用程序使用 Web Mercator 投影 (EPSG:3857) 渲染地图，并期望以 WGS 84 度 (EPSG:4326) 表示纬度/经度坐标。有关在 Foundry 中转换地理空间数据的更多信息，请参阅 Foundry 中的地理空间数据。

---

**核心功能：**

### 地图交互
- 地图界面概述
- 创建和保存地图
- 向地图添加数据
- 图层管理
- 导航
- 选择
- 注释
- 快照
- 形状
- 直方图和过滤
- 操作

### 时间功能
- 概述
- 时间选择
- 时间线
- 事件
- 时间序列

### 可视化本体数据
- 概述
- 点（图标和圆圈）
- 线和多边形
- 轨迹（移动对象）
- 大规模对象集

### 地图数据集成
- 地图的本体对象
- 地图的 Search Around 函数
- 地图的本体操作
- 地图图层编辑器

### 模板和 Workshop 小部件
- 地图模板
- 在 Workshop 模块中嵌入地图模板

### 配置
- 设置
- 控制面板

---

**相关文档导航：**
- Ontology building（本体构建）
  - Map（完整文档）
    - Overview（概览）
    - Getting started（入门）
    - Core concepts（核心概念）
    - Interact with maps（与地图交互）
    - Time（时间）
    - Visualize Ontology data（可视化本体数据）
    - Integrate data for the map（集成地图数据）
    - Templates & Workshop widget（模板和 Workshop 小部件）
    - Configuration（配置）
