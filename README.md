# Skill Vault · 个人技能仓

收集、阅读、打包、调用第三方 skill 项目的个人技能库。

## 这是什么

从 GitHub（或用户提供）收集的 skill 项目——Claude Code / OpenCode / Cursor / 各类 Agent Skill 格式均可。每个 skill 打包为一个独立子目录，包含：**用途说明 + 来源元数据 + 原项目文件**。

## 目录结构

```
├── README.md              # 本文件：仓库说明与索引
├── docs/
│   └── 调用协议.md          # agent 入库与调用规则（唯一事实源）
├── atlas/                 # Obsidian 分类导航层（MOC）
│   ├── 🏠 技能仓主页.md     # 主页：分类导航 + 协作组合
│   ├── 设计创作.md          # 前端 / 视觉 / 界面
│   ├── 视频制作.md          # 分镜 / 镜头 / 转场
│   ├── 提示词与AI工程.md     # Prompt / Skill 创作
│   └── 人格与社交.md        # 人格扮演 / 互动玩法
└── skills/                # 每个子目录 = 一个打包好的 skill
    ├── <skill-name>/
    │   ├── SKILL.md       # 打包后的 skill 定义：用途 / 触发场景 / 步骤 / 示例
    │   ├── SOURCE.md      # 来源元数据：原仓库 URL / 作者 / 许可 / 入库日期
    │   └── ...            # 原项目关键文件（按需拷贝）
    └── README.md          # 全部 skill 的索引清单
```

## Obsidian 使用

本仓库本身就是一个 Obsidian vault（`.obsidian/` 为本地配置，不入库）：

1. Obsidian → **打开文件夹作为仓库** → 选择 `Z:\chang-yong`
2. 从 **atlas/🏠 技能仓主页** 开始浏览：分类导航 → 点进分类 → 打开 skill 的 SKILL.md
3. 分类笔记（MOC）之间、skill 之间已用 `[[wikilink]]` 双向链接，可用**关系图谱**查看网状结构
4. 新 skill 入库后，在对应分类笔记补一行链接（agent 会顺手做）
5. 调整 skill 内容直接编辑 SKILL.md / SOURCE.md，Obsidian 保存即改文件

## 已收录 skill

| Skill | 用途 | 来源 | 入库日期 |
|-------|------|------|----------|
| skill-creator | 教 agent 如何写出高质量 SKILL.md（简洁性/自由度分级/结构规范），可反哺本仓打包质量 | Kimi 官方模板（用户提供） | 2026-08-15 |
| lover-gacha | 恋人扭蛋机：MBTI+星盘+命盘三维匹配生成专属恋人，含反向恋人测评、双人匹配 | 虾评平台 · Echo · v2.0.0 | 2026-08-15 |
| frontend-design | 高设计质量前端界面生成（网页/落地页/组件），避免 AI 通用审美，要求先定大胆美学方向 | Apache-2.0（用户提供） | 2026-08-15 |
| prompt-engineer | 系统化提示词工程：角色模板、少样本、思维链、结构化输出 | 未知 | 2026-08-15 |
| storyboard-prompting | 分镜帧图片提示词（Midjourney/DALL-E/SD），六段式结构保证电影感 | 未知 · SK-FTV-005 | 2026-08-15 |
| director-shot-prompt | 导演镜头提示词：图片映射四类镜头角色，生成流畅转场视频 prompt | 本地项目 xxs-xs | 2026-08-15 |

> 已移除：ex-xiaoxiaoting、shot-transition-script（2026-08-15 用户要求下架）

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
