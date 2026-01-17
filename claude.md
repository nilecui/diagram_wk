# Claude Guide - Draw.io Diagrams Enhanced Skill

[English](#english) | [中文](#中文)

---

<a name="english"></a>
## English

### Skill Overview

This skill enables Claude to create professional Draw.io diagrams in native XML format (`.drawio` files) with:
- Standard flowcharts and business process diagrams
- PMP/PMBOK project management diagrams
- Enterprise-grade visual assets and icon libraries

### Core Capabilities

| Category | Diagram Types |
|----------|---------------|
| Standard | Flowchart, Swimlane, BPMN, UML, Network, Org Chart, Mind Map, ERD |
| PMP/PMBOK | WBS, PERT/CPM, Gantt, RACI, Risk Matrix, Stakeholder Map |

### Draw.io XML Format

#### Basic Structure
```xml
<mxfile host="app.diagrams.net" modified="[timestamp]" agent="Claude" version="24.7.17">
  <diagram id="[unique-id]" name="Page-1">
    <mxGraphModel dx="1434" dy="759" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="850" pageHeight="1100" math="0" shadow="0">
      <root>
        <mxCell id="0"/>
        <mxCell id="1" parent="0"/>
        <!-- Diagram elements here -->
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```

#### Element Templates

**Rectangle (Process Step):**
```xml
<mxCell id="2" value="Process" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#dae8fc;strokeColor=#6c8ebf;" vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="120" height="60" as="geometry"/>
</mxCell>
```

**Diamond (Decision):**
```xml
<mxCell id="3" value="Decision?" style="rhombus;whiteSpace=wrap;html=1;fillColor=#fff2cc;strokeColor=#d6b656;" vertex="1" parent="1">
  <mxGeometry x="100" y="200" width="120" height="80" as="geometry"/>
</mxCell>
```

**Ellipse (Start/End):**
```xml
<mxCell id="4" value="Start" style="ellipse;whiteSpace=wrap;html=1;fillColor=#d5e8d4;strokeColor=#82b366;" vertex="1" parent="1">
  <mxGeometry x="100" y="40" width="120" height="60" as="geometry"/>
</mxCell>
```

**Connector:**
```xml
<mxCell id="5" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=0.5;exitY=1;entryX=0.5;entryY=0;endArrow=classic;endFill=1;" edge="1" parent="1" source="2" target="3">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

### Style Reference

#### Standard Colors
| Purpose | Fill | Stroke |
|---------|------|--------|
| Start/Success | `#d5e8d4` | `#82b366` |
| Process | `#dae8fc` | `#6c8ebf` |
| Decision | `#fff2cc` | `#d6b656` |
| Warning | `#ffe6cc` | `#d79b00` |
| Error/Reject | `#f8cecc` | `#b85450` |
| End/Archive | `#e1d5e7` | `#9673a6` |
| Neutral | `#f5f5f5` | `#666666` |

#### Connector Styles
```
# Standard orthogonal
edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;endArrow=classic;endFill=1;

# Dashed (return/optional path)
dashed=1;dashPattern=5 5;

# Bold (critical path)
strokeWidth=3;strokeColor=#b85450;

# With label
value="Yes" or value="No"
```

#### Size Standards
| Element | Size |
|---------|------|
| Small node | 80x40 |
| Standard node | 120x60 |
| Large node | 160x80 |
| Decision diamond | 120x80 |
| Swimlane height | 120-150px |
| Element spacing | 20-40px |

### ID Management Rules

1. `id="0"` and `id="1"` are reserved root elements
2. Diagram elements start from `id="2"` incrementally
3. Each element must have a unique ID
4. Connector `source` and `target` must reference valid element IDs

### Best Practices

1. **Alignment**: Use multiples of 10 for coordinates
2. **Consistency**: Same size and color for similar elements
3. **Readability**: Keep labels concise (1-5 words)
4. **Logic**: Ensure all paths have endpoints
5. **Semantics**: Follow color conventions
6. **Spacing**: Maintain 20-40px between elements

### Validation Checklist

- [ ] All IDs are unique
- [ ] Root elements (0, 1) exist
- [ ] Connectors have valid source/target
- [ ] Coordinates are positive numbers
- [ ] Style strings are properly formatted
- [ ] XML structure is complete

---

<a name="中文"></a>
## 中文

### 技能概述

此技能使 Claude 能够创建专业的 Draw.io 格式流程图（`.drawio` 文件），包括：
- 标准流程图和业务流程图
- PMP/PMBOK 项目管理图表
- 企业级可视化资源和图标库

### 核心能力

| 类别 | 图表类型 |
|------|----------|
| 标准图表 | 流程图、泳道图、BPMN、UML、网络图、组织结构图、思维导图、ER图 |
| PMP/PMBOK | WBS、PERT/CPM、甘特图、RACI、风险矩阵、利益相关者图 |

### Draw.io XML 格式

#### 基本结构
```xml
<mxfile host="app.diagrams.net" modified="[timestamp]" agent="Claude" version="24.7.17">
  <diagram id="[unique-id]" name="Page-1">
    <mxGraphModel dx="1434" dy="759" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="850" pageHeight="1100" math="0" shadow="0">
      <root>
        <mxCell id="0"/>
        <mxCell id="1" parent="0"/>
        <!-- 图表元素放在这里 -->
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```

#### 元素模板

**矩形（处理步骤）：**
```xml
<mxCell id="2" value="处理步骤" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#dae8fc;strokeColor=#6c8ebf;" vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="120" height="60" as="geometry"/>
</mxCell>
```

**菱形（决策点）：**
```xml
<mxCell id="3" value="判断?" style="rhombus;whiteSpace=wrap;html=1;fillColor=#fff2cc;strokeColor=#d6b656;" vertex="1" parent="1">
  <mxGeometry x="100" y="200" width="120" height="80" as="geometry"/>
</mxCell>
```

**椭圆（开始/结束）：**
```xml
<mxCell id="4" value="开始" style="ellipse;whiteSpace=wrap;html=1;fillColor=#d5e8d4;strokeColor=#82b366;" vertex="1" parent="1">
  <mxGeometry x="100" y="40" width="120" height="60" as="geometry"/>
</mxCell>
```

**连接线：**
```xml
<mxCell id="5" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=0.5;exitY=1;entryX=0.5;entryY=0;endArrow=classic;endFill=1;" edge="1" parent="1" source="2" target="3">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

### 样式参考

#### 标准颜色
| 用途 | 填充色 | 边框色 |
|------|--------|--------|
| 开始/成功 | `#d5e8d4` | `#82b366` |
| 处理步骤 | `#dae8fc` | `#6c8ebf` |
| 决策判断 | `#fff2cc` | `#d6b656` |
| 警告提示 | `#ffe6cc` | `#d79b00` |
| 错误/驳回 | `#f8cecc` | `#b85450` |
| 结束/归档 | `#e1d5e7` | `#9673a6` |
| 中性/容器 | `#f5f5f5` | `#666666` |

#### 连接线样式
```
# 标准正交连接
edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;endArrow=classic;endFill=1;

# 虚线（返回/可选路径）
dashed=1;dashPattern=5 5;

# 粗线（关键路径）
strokeWidth=3;strokeColor=#b85450;

# 带标签
value="是" 或 value="否"
```

#### 尺寸规范
| 元素 | 尺寸 |
|------|------|
| 小型节点 | 80x40 |
| 标准节点 | 120x60 |
| 大型节点 | 160x80 |
| 决策菱形 | 120x80 |
| 泳道高度 | 120-150px |
| 元素间距 | 20-40px |

### ID 管理规则

1. `id="0"` 和 `id="1"` 是保留的根元素
2. 图形元素从 `id="2"` 开始递增
3. 每个元素必须有唯一 ID
4. 连接线的 `source` 和 `target` 必须引用有效的元素 ID

### 最佳实践

1. **对齐**: 使用 10 的倍数作为坐标值
2. **一致性**: 同类元素使用相同尺寸和颜色
3. **可读性**: 标签简洁（1-5 个词）
4. **逻辑完整**: 确保所有路径都有终点
5. **语义化**: 遵循颜色规范传达含义
6. **间距均匀**: 元素之间保持 20-40px 间距

### 验证清单

- [ ] 所有 ID 唯一
- [ ] 根元素（0, 1）存在
- [ ] 连接线有有效的 source/target
- [ ] 坐标为正数
- [ ] 样式字符串格式正确
- [ ] XML 结构完整
