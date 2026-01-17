# Claude Code Skills System Overview

[English](#english) | [中文](#中文)

---

<a name="english"></a>
## English

### What are Skills?

Skills are modular knowledge packages that extend Claude's capabilities within Claude Code. They provide specialized domain knowledge, workflows, and tool integrations that Claude can use when helping users with specific tasks.

### How Skills Work

1. **Automatic Loading**: When you invoke a skill (e.g., `drawio-diagrams-enhanced`), Claude Code loads the skill's instructions
2. **Context Injection**: The skill's SKILL.md content is injected into Claude's context
3. **Reference Materials**: Additional reference files in the skill's directory provide supplementary knowledge
4. **Task Execution**: Claude uses this combined knowledge to complete the requested task

### Skill Directory Structure

```
.claude/
└── skills/
    └── <skill-name>/
        ├── SKILL.md              # Main skill definition (required)
        └── reference/            # Optional reference materials
            ├── template-1.md
            ├── example-1.md
            └── ...
```

### SKILL.md Format

The SKILL.md file has two parts:

#### 1. YAML Frontmatter (Metadata)
```yaml
---
name: skill-name
description: A brief description of what this skill does and when to use it.
---
```

#### 2. Markdown Content (Instructions)
The rest of the file contains detailed instructions, examples, templates, and best practices that Claude will follow when executing the skill.

### Skill Invocation Methods

1. **Direct Command**: Use the Skill tool with the skill name
2. **User Request**: Ask Claude to use a specific skill
3. **Automatic Trigger**: Claude may automatically invoke relevant skills based on task description

### Best Practices for Skills

1. **Clear Description**: Write a description that clearly states when the skill should be used
2. **Comprehensive Instructions**: Include all necessary information in SKILL.md
3. **Reference Materials**: Add supplementary files for complex domains
4. **Examples**: Provide concrete examples of inputs and outputs
5. **Error Handling**: Document common issues and solutions

---

<a name="中文"></a>
## 中文

### 什么是技能 (Skills)?

技能是扩展 Claude Code 中 Claude 能力的模块化知识包。它们提供专业领域知识、工作流程和工具集成，Claude 可以在帮助用户完成特定任务时使用这些功能。

### 技能工作原理

1. **自动加载**: 当调用技能时（如 `drawio-diagrams-enhanced`），Claude Code 加载技能的指令
2. **上下文注入**: 技能的 SKILL.md 内容被注入到 Claude 的上下文中
3. **参考资料**: 技能目录中的额外参考文件提供补充知识
4. **任务执行**: Claude 使用这些综合知识来完成请求的任务

### 技能目录结构

```
.claude/
└── skills/
    └── <技能名称>/
        ├── SKILL.md              # 主技能定义文件（必需）
        └── reference/            # 可选的参考资料
            ├── template-1.md
            ├── example-1.md
            └── ...
```

### SKILL.md 格式

SKILL.md 文件有两部分：

#### 1. YAML 前置元数据
```yaml
---
name: 技能名称
description: 简要描述该技能的功能以及何时使用它。
---
```

#### 2. Markdown 内容（指令）
文件的其余部分包含详细的指令、示例、模板和最佳实践，Claude 在执行技能时会遵循这些内容。

### 技能调用方法

1. **直接命令**: 使用 Skill 工具和技能名称
2. **用户请求**: 要求 Claude 使用特定技能
3. **自动触发**: Claude 可能根据任务描述自动调用相关技能

### 技能最佳实践

1. **清晰描述**: 编写明确说明何时应使用该技能的描述
2. **全面指令**: 在 SKILL.md 中包含所有必要信息
3. **参考资料**: 为复杂领域添加补充文件
4. **示例**: 提供具体的输入和输出示例
5. **错误处理**: 记录常见问题和解决方案
