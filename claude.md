# Claude 使用指南 - Draw.io 流程图生成

## 技能概述

本技能使 Claude 能够创建专业的 Draw.io 格式流程图 (`.drawio` 文件)，支持企业级项目管理图表和标准业务流程图。

## 核心能力

### 1. 标准流程图
- 基本流程图、决策树
- 跨职能流程图 (泳道图)
- BPMN 业务流程图
- UML 图 (类图、序列图、用例图)

### 2. 项目管理图表 (PMP/PMBOK)
- WBS 工作分解结构
- PERT/CPM 网络图
- 甘特图
- RACI 责任矩阵
- 风险矩阵热力图
- 利益相关者分析图

### 3. 技术架构图
- 网络拓扑图
- 云架构图 (AWS/Azure/GCP)
- 系统设计图

## Draw.io 文件格式

### 基本结构

```xml
<mxfile host="app.diagrams.net" modified="[timestamp]" agent="Claude" version="24.7.17">
  <diagram id="[unique-id]" name="Page-1">
    <mxGraphModel dx="1434" dy="759" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="850" pageHeight="1100" math="0" shadow="0">
      <root>
        <mxCell id="0"/>
        <mxCell id="1" parent="0"/>
        <!-- 图形元素放在这里 -->
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```

### 图形元素 (mxCell)

**矩形/处理步骤:**
```xml
<mxCell id="2" value="处理步骤" style="rounded=1;whiteSpace=wrap;html=1;fillColor=#dae8fc;strokeColor=#6c8ebf;" vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="120" height="60" as="geometry"/>
</mxCell>
```

**菱形/决策点:**
```xml
<mxCell id="3" value="判断?" style="rhombus;whiteSpace=wrap;html=1;fillColor=#fff2cc;strokeColor=#d6b656;" vertex="1" parent="1">
  <mxGeometry x="100" y="200" width="120" height="80" as="geometry"/>
</mxCell>
```

**椭圆/开始结束:**
```xml
<mxCell id="4" value="开始" style="ellipse;whiteSpace=wrap;html=1;fillColor=#d5e8d4;strokeColor=#82b366;" vertex="1" parent="1">
  <mxGeometry x="100" y="40" width="120" height="60" as="geometry"/>
</mxCell>
```

**连接线:**
```xml
<mxCell id="5" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=0.5;exitY=1;entryX=0.5;entryY=0;endArrow=classic;endFill=1;" edge="1" parent="1" source="2" target="3">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

## 样式规范

### 标准颜色

| 用途 | 填充色 | 边框色 |
|------|--------|--------|
| 开始/成功 | `#d5e8d4` | `#82b366` |
| 处理步骤 | `#dae8fc` | `#6c8ebf` |
| 决策判断 | `#fff2cc` | `#d6b656` |
| 警告提示 | `#ffe6cc` | `#d79b00` |
| 错误/驳回 | `#f8cecc` | `#b85450` |
| 结束/归档 | `#e1d5e7` | `#9673a6` |
| 中性/容器 | `#f5f5f5` | `#666666` |

### 连接线样式

```
# 标准正交连接
edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;endArrow=classic;endFill=1;

# 虚线 (用于返回/可选路径)
dashed=1;dashPattern=5 5;

# 粗线 (用于关键路径)
strokeWidth=3;strokeColor=#b85450;

# 带标签
value="是"或value="否"
```

### 尺寸规范

| 元素 | 尺寸 |
|------|------|
| 小型节点 | 80x40 |
| 标准节点 | 120x60 |
| 大型节点 | 160x80 |
| 决策菱形 | 120x80 或 140x80 |
| 泳道高度 | 120-150px |
| 元素间距 | 20-40px |

## ID 管理规则

1. `id="0"` 和 `id="1"` 是保留的根元素
2. 图形元素从 `id="2"` 开始递增
3. 每个元素必须有唯一 ID
4. 连接线的 `source` 和 `target` 必须引用有效的图形 ID

## 常用用户请求示例

### 请求示例 1: 基本流程图
> "画一个用户注册流程图"

生成包含: 开始 → 填写信息 → 验证 → 判断是否有效 → 成功/失败 → 结束

### 请求示例 2: 审批流程
> "画一个请假审批流程"

生成包含: 提交申请 → 直属领导审批 → 判断 → HR确认 → 结果通知

### 请求示例 3: 泳道图
> "画一个跨部门的订单处理流程"

生成包含: 多个泳道 (客户、销售、仓库、财务) + 各部门的处理步骤

### 请求示例 4: RACI 矩阵
> "生成一个项目 RACI 矩阵"

生成包含: 表格结构 + 任务行 + 角色列 + R/A/C/I 标记

## 最佳实践

1. **布局对齐**: 使用 10 的倍数作为坐标值
2. **一致性**: 同类元素使用相同尺寸和颜色
3. **可读性**: 标签简洁 (1-5 个词)
4. **逻辑完整**: 确保所有路径都有终点
5. **颜色含义**: 遵循颜色规范传达语义
6. **间距均匀**: 元素之间保持 20-40px 间距

## 输出格式

生成的文件应:
1. 使用 `.drawio` 扩展名
2. 包含完整的 XML 结构
3. 所有 ID 唯一且顺序递增
4. 样式字符串以分号结尾
5. XML 格式正确 (标签正确嵌套)

## 验证清单

- [ ] 所有 ID 唯一
- [ ] 根元素 (0, 1) 存在
- [ ] 连接线有有效的 source/target
- [ ] 坐标为正数
- [ ] 样式字符串格式正确
- [ ] XML 结构完整
