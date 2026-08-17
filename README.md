# Skill Vault · 个人技能仓

收集、阅读、打包、调用第三方 skill 项目的个人技能库。

## 这是什么

从 GitHub（或用户提供）收集的 skill 项目——Claude Code / Codex / OpenClaw / 各类 Agent Skill 格式均可。每个 skill 打包为一个独立子目录，包含：**用途说明 + 来源元数据 + 原项目文件**。

## 目录结构

```
├── README.md              # 本文件：仓库说明与索引
├── docs/
│   └── 调用协议.md          # agent 入库与调用规则（唯一事实源）
├── atlas/                 # Obsidian 分类导航层（MOC）
│   ├── 🏠 技能仓主页.md     # 主页：分类导航（含全部 6 个分类）
│   ├── 💗 伴侣相关类.md     # AI 伴侣专属（人像/情绪/人格/互动）
│   ├── 设计创作.md          # 前端 / 视觉 / 界面
│   ├── 人像写真.md          # 人像生成 / 真人感 / 肌理
│   ├── 视频制作.md          # 分镜 / 镜头 / 转场
│   ├── 提示词与AI工程.md     # Prompt / Skill 创作
│   └── 人格与社交.md        # 人格扮演 / 互动玩法
├── image/                 # 设计素材（民间美术等，二进制不入 atlas）
└── skills/                # 每个子目录 = 一个打包好的 skill
    ├── _staging/          # 测试区：新 skill 先测后录（见调用协议）
    ├── <skill-name>/
    │   ├── SKILL.md       # 打包后的 skill 定义：用途 / 触发场景 / 步骤 / 示例
    │   ├── SOURCE.md      # 来源元数据：原仓库 / 作者 / 许可 / 入库日期 / 实测结论
    │   └── ...            # 原项目关键文件（按需拷贝，大二进制不入库）
    └── README.md          # 全部 skill 的索引清单（24 个，实时维护）
```

## Obsidian 使用

本仓库本身就是一个 Obsidian vault（`.obsidian/` 为本地配置，不入库）：

1. Obsidian → **打开文件夹作为仓库** → 选择 `Z:\chang-yong`
2. 从 **atlas/🏠 技能仓主页** 开始浏览：分类导航 → 点进分类 → 打开 skill 的 SKILL.md
3. 分类笔记（MOC）之间、skill 之间已用 `[[wikilink]]` 双向链接，可用**关系图谱**查看网状结构
4. 新 skill 入库后，在对应分类笔记补一行链接（agent 会顺手做）
5. 调整 skill 内容直接编辑 SKILL.md / SOURCE.md，Obsidian 保存即改文件

## 已收录 skill（24 个）

> 完整清单与实时更新见 [[skills/README.md]]；按领域分类见 [[atlas/🏠 技能仓主页.md]]。

| 领域 | Skill 数 | 代表 |
|------|---------|------|
| 💗 伴侣相关（人像生成） | 7 | nuyoah-xiezhen-prompt（审美第 1）、wanxiang-portrait-skill、real-image、image2-realistic-texture-skill、skill-prompt-generator、restore-my-beauty-punch、image-prompt-reverse |
| 💗 伴侣相关（情绪人格） | 5 | talk-human、freud-skill、dr-frankenstein（激素节律）、human-chat-operit、code-abyss |
| 💗 伴侣相关（互动） | 1 | lover-gacha |
| 设计创作 | 4 | frontend-design、gc-minimal-zine-poster、photo-to-zine-postcard、zine-summary-collection |
| 图片设计 | 3 | cc2image、power-design、blcaptain-style |
| 视频制作 | 3 | storyboard-prompting、director-shot-prompt、gathered-scenes-zine |
| 提示词工程 | 2 | prompt-engineer、skill-creator |
| 素材/工具 | 2 | douyin-downloader、folk-art-materials |

> 已移除：ex-xiaoxiaoting、shot-transition-script（2026-08-15）、image2-prompt（2026-08-17 两次测试被否）

## 工作流程（由 agent 执行）

### 入库流程（详见 docs/调用协议.md）

1. 获取来源：用户提供下载好的 skill，或 agent 从 GitHub 主动寻找合适的 skill
2. **通读原项目**，理解它做什么、怎么用、依赖什么
3. **向用户汇报**：这个 skill 是做什么用的、适用场景、质量评估
4. **先入 `skills/_staging/` 测试区**：按 SKILL.md 实测功能，测试通过才正式入库
5. 打包入库：写 `SKILL.md` + `SOURCE.md`（含实测结论），按需拷贝原项目文件
6. 更新 `skills/README.md` 索引 + 对应 atlas 分类笔记

### 调用流程

用户提出需求（如"做个 PPT""画个架构图""给芷雨生成照片"）时：

1. agent 列出仓内**相关 skill 清单及其用途**给用户看
2. **主动询问具体需求**（如"要什么风格？"——瑞士风格 / 极简 / 商务……）
3. 读取对应 `SKILL.md`，按其步骤执行
4. 完成后把产物交付用户

## 维护约定

- 开发分支：`skill`（worktree: `Z:\chang-yong\.worktrees\skill`）；主分支 `master`（Obsidian 打开的工作区）
- **PR 流程**（2026-08-15 起）：skill 分支提交 → `git push origin skill` → 开 PR `skill → master`（GitHub API）→ 验证 clean 后合并
- 每次入库/修改后：推送 skill 分支 + 合并 master（Obsidian 与远程都看 master）
- 每个 skill 入库一个独立 commit，commit message 含 skill 名与来源
- 许可遵守原项目 license；来源不清的不入库
