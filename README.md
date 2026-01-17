# Draw.io 流程图工作区

本工作区用于创建和管理 Draw.io 格式的专业流程图和项目管理图表。

## 文件说明

| 文件名 | 描述 |
|--------|------|
| `approval_flowchart.drawio` | 业务审批流程图示例 |

## 支持的图表类型

### 标准图表
- **流程图** - 基本流程、决策树、业务流程
- **跨职能流程图 (泳道图)** - 跨部门/角色的流程展示
- **BPMN 图** - 业务流程建模标记法
- **UML 图** - 类图、序列图、用例图
- **网络拓扑图** - 基础设施、云架构、系统设计
- **组织结构图** - 团队层级和汇报关系
- **思维导图** - 概念映射和头脑风暴
- **ER 图** - 数据库实体关系

### PMP/PMBOK 项目管理图表
- **WBS (工作分解结构)** - 项目可交付成果的层级分解
- **PERT/CPM 网络图** - 活动依赖和关键路径分析
- **甘特图** - 基于时间线的项目进度
- **RACI 矩阵** - 责任分配矩阵
- **风险矩阵** - 概率-影响热力图
- **利益相关者地图** - 权力-利益矩阵

## 图形规范

### 颜色编码

| 元素类型 | 颜色 | 用途 |
|----------|------|------|
| 开始/成功 | 绿色 `#d5e8d4` | 起始节点、成功状态 |
| 处理步骤 | 蓝色 `#dae8fc` | 常规处理流程 |
| 决策判断 | 黄色 `#fff2cc` | 条件分支、判断点 |
| 警告/退回 | 橙色 `#ffe6cc` | 需要注意的步骤 |
| 错误/驳回 | 红色 `#f8cecc` | 失败、拒绝状态 |
| 结束/归档 | 紫色 `#e1d5e7` | 结束节点、归档 |

### 形状规范

| 形状 | 用途 |
|------|------|
| 椭圆 | 开始/结束节点 |
| 圆角矩形 | 处理步骤 |
| 菱形 | 决策/判断点 |
| 平行四边形 | 数据输入/输出 |
| 文档形状 | 文档/报告 |
| 泳道 | 部门/角色分区 |

## 打开和编辑

### 在线编辑
访问 [app.diagrams.net](https://app.diagrams.net/) 打开 `.drawio` 文件

### VS Code
安装 [Draw.io Integration](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio) 插件

### 桌面应用
下载 [Draw.io Desktop](https://github.com/jgraph/drawio-desktop/releases)

## 自定义图标库

如需使用额外图标，可在 draw.io 中加载自定义库：

```
https://app.diagrams.net/?clibs=Uhttps://jgraph.github.io/drawio-libs/libs/templates.xml
```

可用图标库：
- Material Design Icons
- Font Awesome
- AWS/Azure/GCP 云服务图标
- Kubernetes 图标
- 网络设备图标 (Cisco, Fortinet 等)

## 参考资源

- [Draw.io 官方文档](https://www.drawio.com/doc/)
- [示例图表](https://www.drawio.com/example-diagrams)
- [自定义库仓库](https://github.com/jgraph/drawio-libs)
- [PMBOK 指南](https://www.pmi.org/)
