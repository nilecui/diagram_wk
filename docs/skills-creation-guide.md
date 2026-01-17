# Claude Code Skills Creation & Modification Guide

[English](#english) | [中文](#中文)

---

<a name="english"></a>
## English

### Creating a New Skill

#### Step 1: Create Directory Structure

```bash
mkdir -p .claude/skills/<your-skill-name>
mkdir -p .claude/skills/<your-skill-name>/reference  # optional
```

#### Step 2: Create SKILL.md

Create the main skill definition file:

```bash
touch .claude/skills/<your-skill-name>/SKILL.md
```

#### Step 3: Write SKILL.md Content

```markdown
---
name: your-skill-name
description: A comprehensive description of your skill. Include:
  - What the skill does
  - When to use it (trigger conditions)
  - What outputs it produces
---

# Skill Title

## Overview
Describe the skill's purpose and capabilities.

## Instructions
Detailed instructions for Claude to follow.

## Templates
Code templates, format examples, etc.

## Examples
Input/output examples.

## Best Practices
Guidelines for optimal results.

## Common Issues
Known issues and solutions.
```

### SKILL.md Template

```markdown
---
name: my-custom-skill
description: Use this skill when users ask to [specific task]. This skill provides [capabilities] and produces [outputs].
---

# My Custom Skill

## Overview

This skill enables Claude to [main capability].

## Core Capabilities

1. **Capability 1**: Description
2. **Capability 2**: Description
3. **Capability 3**: Description

## Instructions

### When to Use
- Condition 1
- Condition 2

### Step-by-Step Process
1. First, do this
2. Then, do that
3. Finally, produce output

## Output Format

Describe the expected output format:

\`\`\`
[output template]
\`\`\`

## Examples

### Example 1: Basic Usage

**User Request**: "Do X"

**Expected Output**:
\`\`\`
[example output]
\`\`\`

## Best Practices

1. **Practice 1**: Explanation
2. **Practice 2**: Explanation

## Limitations

- Limitation 1
- Limitation 2

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Error 1 | Cause | Solution |
| Error 2 | Cause | Solution |
```

### Adding Reference Files

Reference files provide supplementary knowledge:

```
.claude/skills/my-skill/
├── SKILL.md
└── reference/
    ├── templates.md       # Reusable templates
    ├── examples.md        # Detailed examples
    ├── api-reference.md   # API documentation
    └── troubleshooting.md # Common issues
```

### Modifying Existing Skills

#### 1. Edit SKILL.md

```bash
# Edit the main skill file
nano .claude/skills/<skill-name>/SKILL.md
```

#### 2. Update Metadata

Change the frontmatter if needed:

```yaml
---
name: updated-skill-name
description: Updated description with new capabilities.
---
```

#### 3. Add/Update Sections

Common sections to modify:
- Add new capabilities
- Update templates
- Add more examples
- Improve error handling

#### 4. Add Reference Files

```bash
# Add new reference file
touch .claude/skills/<skill-name>/reference/new-reference.md
```

### Skill Description Best Practices

The `description` field is critical for automatic skill selection:

```yaml
# Good - Specific triggers
description: Use this skill when users ask to create flowcharts,
  swimlane diagrams, WBS, RACI matrices, or any draw.io format diagrams.

# Bad - Too vague
description: A skill for making diagrams.
```

### Testing Your Skill

1. **Invoke the skill**: Ask Claude to use your skill
2. **Check context**: Verify skill content is loaded
3. **Test edge cases**: Try various inputs
4. **Iterate**: Refine based on results

### Skill Organization Tips

```
.claude/skills/
├── skill-a/
│   ├── SKILL.md
│   └── reference/
│       └── ...
├── skill-b/
│   └── SKILL.md
└── skill-c/
    ├── SKILL.md
    └── reference/
        └── ...
```

---

<a name="中文"></a>
## 中文

### 创建新技能

#### 步骤 1: 创建目录结构

```bash
mkdir -p .claude/skills/<你的技能名称>
mkdir -p .claude/skills/<你的技能名称>/reference  # 可选
```

#### 步骤 2: 创建 SKILL.md

创建主技能定义文件：

```bash
touch .claude/skills/<你的技能名称>/SKILL.md
```

#### 步骤 3: 编写 SKILL.md 内容

```markdown
---
name: 你的技能名称
description: 技能的全面描述，包括：
  - 技能的功能
  - 何时使用（触发条件）
  - 产生什么输出
---

# 技能标题

## 概述
描述技能的目的和能力。

## 指令
Claude 需要遵循的详细指令。

## 模板
代码模板、格式示例等。

## 示例
输入/输出示例。

## 最佳实践
获得最佳结果的指南。

## 常见问题
已知问题和解决方案。
```

### SKILL.md 模板

```markdown
---
name: 我的自定义技能
description: 当用户要求 [特定任务] 时使用此技能。此技能提供 [能力] 并产生 [输出]。
---

# 我的自定义技能

## 概述

此技能使 Claude 能够 [主要能力]。

## 核心能力

1. **能力 1**: 描述
2. **能力 2**: 描述
3. **能力 3**: 描述

## 指令

### 何时使用
- 条件 1
- 条件 2

### 分步流程
1. 首先，执行此操作
2. 然后，执行该操作
3. 最后，生成输出

## 输出格式

描述预期的输出格式：

\`\`\`
[输出模板]
\`\`\`

## 示例

### 示例 1: 基本用法

**用户请求**: "执行 X"

**预期输出**:
\`\`\`
[示例输出]
\`\`\`

## 最佳实践

1. **实践 1**: 解释
2. **实践 2**: 解释

## 限制

- 限制 1
- 限制 2

## 错误处理

| 错误 | 原因 | 解决方案 |
|------|------|----------|
| 错误 1 | 原因 | 解决方案 |
| 错误 2 | 原因 | 解决方案 |
```

### 添加参考文件

参考文件提供补充知识：

```
.claude/skills/我的技能/
├── SKILL.md
└── reference/
    ├── templates.md       # 可重用模板
    ├── examples.md        # 详细示例
    ├── api-reference.md   # API 文档
    └── troubleshooting.md # 常见问题
```

### 修改现有技能

#### 1. 编辑 SKILL.md

```bash
# 编辑主技能文件
nano .claude/skills/<技能名称>/SKILL.md
```

#### 2. 更新元数据

如需更改前置元数据：

```yaml
---
name: 更新的技能名称
description: 包含新能力的更新描述。
---
```

#### 3. 添加/更新章节

常见的修改章节：
- 添加新能力
- 更新模板
- 添加更多示例
- 改进错误处理

#### 4. 添加参考文件

```bash
# 添加新的参考文件
touch .claude/skills/<技能名称>/reference/新参考.md
```

### 技能描述最佳实践

`description` 字段对于自动技能选择至关重要：

```yaml
# 好 - 具体的触发条件
description: 当用户要求创建流程图、泳道图、WBS、RACI 矩阵或任何 draw.io 格式图表时使用此技能。

# 差 - 太模糊
description: 用于制作图表的技能。
```

### 测试你的技能

1. **调用技能**: 要求 Claude 使用你的技能
2. **检查上下文**: 验证技能内容已加载
3. **测试边界情况**: 尝试各种输入
4. **迭代**: 根据结果进行优化

### 技能组织建议

```
.claude/skills/
├── 技能-a/
│   ├── SKILL.md
│   └── reference/
│       └── ...
├── 技能-b/
│   └── SKILL.md
└── 技能-c/
    ├── SKILL.md
    └── reference/
        └── ...
```
