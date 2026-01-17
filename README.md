# Draw.io Diagrams Enhanced Skill

[English](#english) | [中文](#中文) | [Documentation](docs/index.md)

---

<a name="english"></a>
## English

### Overview

This skill enables Claude to create professional Draw.io diagrams in native XML format (`.drawio` files) with enterprise-grade capabilities including PMP/PMBOK project management methodologies and extensive icon libraries.

### How to Use

Simply ask Claude to create a diagram:

```
# Basic flowchart
"Create a flowchart for user registration process"

# Swimlane diagram
"Draw a cross-functional flowchart for order processing"

# Project management
"Generate a WBS for software development project"
"Create a RACI matrix for my team"
"Draw a risk matrix heat map"
```

### Supported Diagram Types

#### Standard Diagrams
| Type | Description | Use Case |
|------|-------------|----------|
| Flowchart | Basic process flows, decision trees | Business processes, algorithms |
| Swimlane (CFF) | Cross-functional flowcharts | Multi-department workflows |
| BPMN | Business Process Model and Notation | Enterprise process modeling |
| UML | Class, sequence, use case diagrams | Software design |
| Network | Infrastructure, cloud architecture | System design |
| Org Chart | Organizational hierarchies | Team structures |
| Mind Map | Conceptual mapping | Brainstorming |
| ERD | Entity Relationship Diagrams | Database design |

#### PMP/PMBOK Project Management Diagrams
| Type | Description | Use Case |
|------|-------------|----------|
| WBS | Work Breakdown Structure | Project scope decomposition |
| PERT/CPM | Project network diagrams | Activity sequencing, critical path |
| Gantt | Timeline-based schedules | Project scheduling |
| RACI | Responsibility matrix | Role assignment |
| Risk Matrix | Probability-impact grid | Risk assessment |
| Stakeholder Map | Power-interest grid | Stakeholder analysis |

### Shape & Color Standards

#### Colors
| Purpose | Fill Color | Stroke Color |
|---------|------------|--------------|
| Start/Success | `#d5e8d4` | `#82b366` |
| Process Step | `#dae8fc` | `#6c8ebf` |
| Decision | `#fff2cc` | `#d6b656` |
| Warning | `#ffe6cc` | `#d79b00` |
| Error/Reject | `#f8cecc` | `#b85450` |
| End/Archive | `#e1d5e7` | `#9673a6` |

#### Shapes
| Shape | Usage |
|-------|-------|
| Ellipse | Start/End nodes |
| Rounded Rectangle | Process steps |
| Diamond | Decision points |
| Parallelogram | Data I/O |
| Document | Documents/Reports |
| Swimlane | Department/Role lanes |

### Opening Diagrams

- **Online**: [app.diagrams.net](https://app.diagrams.net/)
- **VS Code**: Install [Draw.io Integration](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)
- **Desktop**: Download [Draw.io Desktop](https://github.com/jgraph/drawio-desktop/releases)

### Custom Icon Libraries

Load additional icons in draw.io:
```
https://app.diagrams.net/?clibs=Uhttps://jgraph.github.io/drawio-libs/libs/templates.xml
```

Available libraries:
- Material Design Icons / Font Awesome
- AWS / Azure / GCP cloud icons
- Kubernetes icons
- Network device icons (Cisco, Fortinet, etc.)

### Resources

- [Draw.io Documentation](https://www.drawio.com/doc/)
- [Example Diagrams](https://www.drawio.com/example-diagrams)
- [Custom Libraries](https://github.com/jgraph/drawio-libs)
- [PMBOK Guide](https://www.pmi.org/)

---

<a name="中文"></a>
## 中文

### 概述

此技能使 Claude 能够创建专业的 Draw.io 格式流程图（`.drawio` 文件），支持企业级项目管理图表（PMP/PMBOK）和丰富的图标库。

### 使用方法

直接向 Claude 描述您需要的图表：

```
# 基本流程图
"画一个用户注册流程图"

# 泳道图
"画一个跨部门的订单处理流程"

# 项目管理图表
"生成一个软件开发项目的 WBS"
"创建团队的 RACI 矩阵"
"画一个风险矩阵热力图"
```

### 支持的图表类型

#### 标准图表
| 类型 | 描述 | 使用场景 |
|------|------|----------|
| 流程图 | 基本流程、决策树 | 业务流程、算法 |
| 泳道图 (CFF) | 跨职能流程图 | 多部门工作流 |
| BPMN | 业务流程建模标记法 | 企业流程建模 |
| UML | 类图、序列图、用例图 | 软件设计 |
| 网络图 | 基础设施、云架构 | 系统设计 |
| 组织结构图 | 组织层级 | 团队结构 |
| 思维导图 | 概念映射 | 头脑风暴 |
| ER 图 | 实体关系图 | 数据库设计 |

#### PMP/PMBOK 项目管理图表
| 类型 | 描述 | 使用场景 |
|------|------|----------|
| WBS | 工作分解结构 | 项目范围分解 |
| PERT/CPM | 项目网络图 | 活动排序、关键路径 |
| 甘特图 | 时间线进度表 | 项目排程 |
| RACI | 责任分配矩阵 | 角色分配 |
| 风险矩阵 | 概率-影响矩阵 | 风险评估 |
| 利益相关者图 | 权力-利益矩阵 | 干系人分析 |

### 图形与颜色规范

#### 颜色
| 用途 | 填充色 | 边框色 |
|------|--------|--------|
| 开始/成功 | `#d5e8d4` | `#82b366` |
| 处理步骤 | `#dae8fc` | `#6c8ebf` |
| 决策判断 | `#fff2cc` | `#d6b656` |
| 警告提示 | `#ffe6cc` | `#d79b00` |
| 错误/驳回 | `#f8cecc` | `#b85450` |
| 结束/归档 | `#e1d5e7` | `#9673a6` |

#### 形状
| 形状 | 用途 |
|------|------|
| 椭圆 | 开始/结束节点 |
| 圆角矩形 | 处理步骤 |
| 菱形 | 决策/判断点 |
| 平行四边形 | 数据输入/输出 |
| 文档形状 | 文档/报告 |
| 泳道 | 部门/角色分区 |

### 打开图表

- **在线**: [app.diagrams.net](https://app.diagrams.net/)
- **VS Code**: 安装 [Draw.io Integration](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio) 插件
- **桌面应用**: 下载 [Draw.io Desktop](https://github.com/jgraph/drawio-desktop/releases)

### 自定义图标库

在 draw.io 中加载额外图标：
```
https://app.diagrams.net/?clibs=Uhttps://jgraph.github.io/drawio-libs/libs/templates.xml
```

可用图标库：
- Material Design 图标 / Font Awesome
- AWS / Azure / GCP 云服务图标
- Kubernetes 图标
- 网络设备图标 (Cisco, Fortinet 等)

### 参考资源

- [Draw.io 官方文档](https://www.drawio.com/doc/)
- [示例图表](https://www.drawio.com/example-diagrams)
- [自定义库仓库](https://github.com/jgraph/drawio-libs)
- [PMBOK 指南](https://www.pmi.org/)
