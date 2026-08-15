# Skill Vault · 个人技能仓

收集、阅读、打包、调用第三方 skill 项目的个人技能库。

## 这是什么

从 GitHub（或用户提供）收集的 skill 项目——Claude Code / OpenCode / Cursor / 各类 Agent Skill 格式均可。每个 skill 打包为一个独立子目录，包含：**用途说明 + 来源元数据 + 原项目文件**。

## 目录结构

```
├── README.md              # 本文件：仓库说明与索引
├── docs/
│   └── 调用协议.md          # agent 入库与调用规则（唯一事实源）
└── skills/                # 每个子目录 = 一个打包好的 skill
    ├── <skill-name>/
    │   ├── SKILL.md       # 打包后的 skill 定义：用途 / 触发场景 / 步骤 / 示例
    │   ├── SOURCE.md      # 来源元数据：原仓库 URL / 作者 / 许可 / 入库日期
    │   └── ...            # 原项目关键文件（按需拷贝）
    └── README.md          # 全部 skill 的索引清单
```

## 已收录 skill

| Skill | 用途 | 来源 | 入库日期 |
|-------|------|------|----------|
| _（暂无，等待第一个入库）_ | | | |

## 工作流程（由 agent 执行）

### 入库流程

1. 获取来源：用户提供下载好的 skill，或 agent 从 GitHub 主动寻找合适的 skill
2. **通读原项目**，理解它做什么、怎么用、依赖什么
3. **向用户汇报**：这个 skill 是做什么用的、适用场景、质量评估
4. 打包入库：写 `SKILL.md`（用途/触发场景/步骤/示例）+ `SOURCE.md`（来源/作者/许可/入库日期），按需拷贝原项目文件
5. 更新 `skills/README.md` 索引，提交

### 调用流程

用户提出需求（如"做个 PPT""画个架构图"）时：

1. agent 列出仓内**相关 skill 清单及其用途**给用户看
2. **主动询问具体需求**（如"要什么风格？"——瑞士风格 / 极简 / 商务……）
3. 读取对应 `SKILL.md`，按其步骤执行
4. 完成后把产物交付用户

## 维护约定

- 仓库工作分支：`skill`（worktree: `Z:\chang-yong\.worktrees\skill`），主分支 `master` 保持干净
- 每个 skill 入库一个独立 commit，commit message 含 skill 名与来源
- 许可遵守原项目 license；来源不清的不入库
