# Draw.io Diagrams Enhanced Skill Reference

[English](#english) | [中文](#中文)

---

<a name="english"></a>
## English

### Skill Information

| Property | Value |
|----------|-------|
| Name | `drawio-diagrams-enhanced` |
| Location | `.claude/skills/drawio-diagrams-enhanced/` |
| Main File | `SKILL.md` |
| Reference Files | 7 files in `reference/` |

### Directory Structure

```
.claude/skills/drawio-diagrams-enhanced/
├── SKILL.md                              # Main skill definition
└── reference/
    ├── drawio-shape-reference.md         # Shape styles reference
    ├── pmp-formulas-reference.md         # PMP calculation formulas
    ├── project-wbs-odoo-implementation.md # WBS example
    ├── bir-tax-compliance-workflow.md     # Workflow example
    ├── insightpulse-architecture.md       # Architecture example
    ├── project-charter-template.md        # Charter template
    └── raci-matrix-template.md            # RACI template
```

### Capabilities

#### Standard Diagrams
- Flowcharts
- Cross-Functional Flowcharts (Swimlane)
- BPMN Diagrams
- UML Diagrams
- Network Diagrams
- Org Charts
- Mind Maps
- Entity Relationship Diagrams

#### PMP/PMBOK Diagrams
- Work Breakdown Structure (WBS)
- PERT/CPM Network Diagrams
- Gantt Charts
- RACI Matrices
- Risk Matrices
- Stakeholder Maps
- Resource Histograms
- Communication Plans

### Key Style Definitions

#### Color Scheme

| Level/Type | Fill Color | Stroke Color | Font Color |
|------------|------------|--------------|------------|
| Level 0 (Project) | `#0050ef` | `#001DBC` | `#ffffff` |
| Level 1 (Phase) | `#2e7d32` | `#1b5e20` | `#ffffff` |
| Level 2 (Deliverable) | `#ff9800` | `#e65100` | `#000000` |
| Level 3 (Work Package) | `#7b1fa2` | `#4a148c` | `#ffffff` |
| Start/Success | `#d5e8d4` | `#82b366` | `#000000` |
| Process | `#dae8fc` | `#6c8ebf` | `#000000` |
| Decision | `#fff2cc` | `#d6b656` | `#000000` |
| Error/Critical | `#f8cecc` | `#b85450` | `#000000` |

#### RACI Matrix Colors

| Assignment | Fill Color | Stroke Color |
|------------|------------|--------------|
| R (Responsible) | `#d5e8d4` | `#82b366` |
| A (Accountable) | `#dae8fc` | `#6c8ebf` |
| C (Consulted) | `#fff2cc` | `#d6b656` |
| I (Informed) | `#e1d5e7` | `#9673a6` |

### How to Invoke

```
# Method 1: Direct skill invocation
Use the drawio-diagrams-enhanced skill to create a WBS

# Method 2: Natural language
Create a flowchart for user registration process

# Method 3: Specific diagram request
Generate a RACI matrix for my project team
```

### Output Format

The skill produces `.drawio` files in XML format:

```xml
<mxfile host="app.diagrams.net" modified="[timestamp]" agent="Claude">
  <diagram id="[unique-id]" name="Page-1">
    <mxGraphModel ...>
      <root>
        <mxCell id="0"/>
        <mxCell id="1" parent="0"/>
        <!-- Shapes and connectors -->
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```

### Modifying This Skill

#### Add New Diagram Type

1. Edit `SKILL.md`
2. Add to capabilities section
3. Add style definitions
4. Add example template

#### Update Color Scheme

1. Edit `SKILL.md` color scheme section
2. Update reference/drawio-shape-reference.md

#### Add Reference Material

```bash
# Add new reference file
touch .claude/skills/drawio-diagrams-enhanced/reference/new-template.md
```

---

<a name="中文"></a>
## 中文

### 技能信息

| 属性 | 值 |
|------|-----|
| 名称 | `drawio-diagrams-enhanced` |
| 位置 | `.claude/skills/drawio-diagrams-enhanced/` |
| 主文件 | `SKILL.md` |
| 参考文件 | `reference/` 中有 7 个文件 |

### 目录结构

```
.claude/skills/drawio-diagrams-enhanced/
├── SKILL.md                              # 主技能定义
└── reference/
    ├── drawio-shape-reference.md         # 形状样式参考
    ├── pmp-formulas-reference.md         # PMP 计算公式
    ├── project-wbs-odoo-implementation.md # WBS 示例
    ├── bir-tax-compliance-workflow.md     # 工作流示例
    ├── insightpulse-architecture.md       # 架构示例
    ├── project-charter-template.md        # 项目章程模板
    └── raci-matrix-template.md            # RACI 模板
```

### 能力

#### 标准图表
- 流程图
- 跨职能流程图（泳道图）
- BPMN 图
- UML 图
- 网络图
- 组织结构图
- 思维导图
- 实体关系图

#### PMP/PMBOK 图表
- 工作分解结构 (WBS)
- PERT/CPM 网络图
- 甘特图
- RACI 矩阵
- 风险矩阵
- 利益相关者图
- 资源直方图
- 沟通计划

### 关键样式定义

#### 颜色方案

| 层级/类型 | 填充色 | 边框色 | 字体颜色 |
|-----------|--------|--------|----------|
| Level 0 (项目) | `#0050ef` | `#001DBC` | `#ffffff` |
| Level 1 (阶段) | `#2e7d32` | `#1b5e20` | `#ffffff` |
| Level 2 (交付物) | `#ff9800` | `#e65100` | `#000000` |
| Level 3 (工作包) | `#7b1fa2` | `#4a148c` | `#ffffff` |
| 开始/成功 | `#d5e8d4` | `#82b366` | `#000000` |
| 处理 | `#dae8fc` | `#6c8ebf` | `#000000` |
| 决策 | `#fff2cc` | `#d6b656` | `#000000` |
| 错误/关键 | `#f8cecc` | `#b85450` | `#000000` |

#### RACI 矩阵颜色

| 分配 | 填充色 | 边框色 |
|------|--------|--------|
| R (负责) | `#d5e8d4` | `#82b366` |
| A (批准) | `#dae8fc` | `#6c8ebf` |
| C (咨询) | `#fff2cc` | `#d6b656` |
| I (知会) | `#e1d5e7` | `#9673a6` |

### 调用方法

```
# 方法 1: 直接调用技能
使用 drawio-diagrams-enhanced 技能创建一个 WBS

# 方法 2: 自然语言
为用户注册流程创建一个流程图

# 方法 3: 特定图表请求
为我的项目团队生成一个 RACI 矩阵
```

### 输出格式

该技能生成 XML 格式的 `.drawio` 文件：

```xml
<mxfile host="app.diagrams.net" modified="[timestamp]" agent="Claude">
  <diagram id="[unique-id]" name="Page-1">
    <mxGraphModel ...>
      <root>
        <mxCell id="0"/>
        <mxCell id="1" parent="0"/>
        <!-- 形状和连接器 -->
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```

### 修改此技能

#### 添加新图表类型

1. 编辑 `SKILL.md`
2. 添加到能力部分
3. 添加样式定义
4. 添加示例模板

#### 更新颜色方案

1. 编辑 `SKILL.md` 颜色方案部分
2. 更新 reference/drawio-shape-reference.md

#### 添加参考资料

```bash
# 添加新的参考文件
touch .claude/skills/drawio-diagrams-enhanced/reference/新模板.md
```
