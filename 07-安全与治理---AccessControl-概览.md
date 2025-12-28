# Access Control 概览

> 更新时间：2025-12-28
> 文档来源：https://palantir.com/docs/foundry/object-permissioning/overview/

## 概述

Foundry Ontology 允许对所有 Ontology 实体进行**细粒度、强大且灵活的安全控制**。这些实体包括：

- **对象类型** (Object Types)
- **链接类型** (Link Types)
- **行动类型** (Action Types)
- **对象** (Objects) - 实际数据
- **链接** (Links) - 实际数据

## 授权结构

Ontology 的授权结构可以在两个层面上概念化：

```
┌─────────────────────────────────────────────────────────────┐
│                    Ontology 授权结构                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  Ontology 资源（架构层）                            │   │
│  │  - 对象类型定义                                      │   │
│  │  - 链接类型定义                                      │   │
│  │  - 行动类型定义                                      │   │
│  │  - 显示名称、属性名称、属性数据类型、描述            │   │
│  └─────────────────────────────────────────────────────┘   │
│                          ↓                                  │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  对象和链接（数据层）                                │   │
│  │  - 实际的主键值                                     │   │
│  │  - 实际的属性值                                     │   │
│  │  - 例如：Plane ID = "my_plane_id1"                  │   │
│  │        Maximum Occupancy = 240                      │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 1. Ontology 资源权限

### 什么是 Ontology 资源

Ontology 资源定义了 Ontology 的**架构（Schema）**：

| 资源类型 | 说明 | 示例 |
|----------|------|------|
| **对象类型** | 定义对象的属性和结构 | 飞机对象类型包含 ID、最大载客量等属性 |
| **链接类型** | 定义对象之间的关系 | 飞机-机场链接类型 |
| **行动类型** | 定义可执行的操作 | 更新飞机状态行动 |

**资源定义内容**：
- 显示名称
- 属性名称
- 属性数据类型
- 描述和元数据
- 验证规则

**重要区别**：
- 这些资源**不包含**实际的属性值或主键值
- 实际的属性值和主键值包含在对象和链接中

### Ontology 资源权限

**权限类型**：
- **查看权限**：查看资源定义
- **编辑权限**：修改资源定义
- **管理权限**：管理资源和其元数据
- **删除权限**：删除资源

**权限范围**：
- 项目级权限
- 组织级权限
- 资源特定权限

## 2. 对象和链接权限

### 什么是对象和链接

对象和链接是 Ontology 中的**实际数据**：

**对象示例**：
```
飞机对象类型的一个对象：
- Plane ID 属性值：my_plane_id1
- Maximum Occupancy 属性值：240
- Model 属性值：Boeing 747
```

**链接示例**：
```
飞机-机场链接：
- 源对象：my_plane_id1（飞机）
- 目标对象：JFK（机场）
- 链接类型：位于
```

### 对象和链接权限

**权限类型**：
- **查看权限**：查看对象/链接及其属性值
- **编辑权限**：修改对象/链接的属性值
- **创建权限**：创建新对象/链接
- **删除权限**：删除对象/链接

**权限粒度**：
- **对象类型级别**：对某种类型的所有对象的权限
- **单个对象级别**：对特定对象的权限
- **属性级别**：对特定属性的权限

## 安全模型

### 基于角色的访问控制 (RBAC)

- **角色**：定义一组权限
- **用户/组**：分配角色
- **资源**：角色应用于资源

### 基于标记的访问控制

- **标记**：应用于资源的标签
- **标记策略**：定义标记如何影响访问
- **动态权限**：基于标记动态确定访问权限

### 基于目的的访问控制

- **目的**：定义数据使用的目的
- **目的策略**：控制数据如何用于不同目的
- **访问决策**：基于目的做出访问决策

## 特殊权限类型

### 1. 受限视图支持的对象类型 (MDO)

**MDO (Multi-Datasource Object Types)**：
- 跨多个数据源的对象类型
- 细粒度的源级别权限
- 用户只能看到他们有权限访问的源的数据

### 2. 编辑权限控制

**对象编辑控制**：
- Allow users to edit objects and links
- 配置哪些用户可以编辑哪些对象
- 行动级别的权限控制

### 3. 行动类型权限

**Action Types**：
- 谁可以应用行动类型
- 行动参数的权限
- 副作用权限（通知、Webhook）

## 权限继承

### 从资源继承

- 对象继承对象类型的权限设置
- 链接继承链接类型的权限设置
- 可以被对象级别的权限覆盖

### 项目和组织

- 项目权限：项目内资源的权限
- 组织权限：跨项目的权限
- 权限组合：最终权限是所有权限的组合

## 安全最佳实践

### 最小权限原则

- 只授予必要的权限
- 定期审查和撤销不需要的权限
- 使用角色简化权限管理

### 权限分层

- **架构层**：控制谁可以定义和修改 Ontology 结构
- **数据层**：控制谁可以访问和修改实际数据
- **应用层**：控制谁可以在应用中执行操作

### 审计和监控

- **审计日志**：记录所有权限更改
- **访问日志**：记录对象和链接的访问
- **监控**：监控异常访问模式

## 相关文档

- [Ontology permissions](https://palantir.com/docs/foundry/object-permissioning/ontology-permissions/) - Ontology 权限详解
- [Legacy ontology permissions](https://palantir.com/docs/foundry/object-permissioning/legacy-ontology-permissions/) - 旧版 Ontology 权限
- [Managing object security](https://palantir.com/docs/foundry/object-permissioning/managing-object-security/) - 管理对象安全
- [Restricted-view-backed object types](https://palantir.com/docs/foundry/object-permissioning/configuring-restricted-view-backed-object-types/) - 受限视图支持的对象类型
- [Multi-datasource object types (MDOs)](https://palantir.com/docs/foundry/object-permissioning/multi-datasource-object-types/) - 多数据源对象类型
- [Object security policies](https://palantir.com/docs/foundry/object-permissioning/object-security-policies/) - 对象安全策略

---

*本文档基于 Palantir Foundry 官方文档整理*
