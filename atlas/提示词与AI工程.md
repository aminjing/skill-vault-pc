---
tags: [atlas, moc, 提示词, AI工程]
---

# 🧠 提示词与 AI 工程

> Prompt 设计、优化与 skill 创作类 skill。返回 [[atlas/🏠 技能仓主页.md|🏠 主页]]

| Skill | 用途 | 来源 |
|-------|------|------|
| [[skills/anysearch/SKILL.md\|anysearch]] | **统一实时搜索（本仓主要搜索源）**：web 通用 + 17 垂直域 + 批量并行 + 网页提取；CLI 调用，中文友好 | anysearch-ai · Apache-2.0 · v3.0.1 |
| [[skills/prompt-engineer/SKILL.md\|prompt-engineer]] | 系统化提示词工程：角色设定模板、少样本学习、思维链、结构化输出 | 用户提供 |
| [[skills/skill-creator/SKILL.md\|skill-creator]] | Kimi 官方 skill 创作指南：简洁性、自由度分级、SKILL.md 结构规范 | Kimi 官方模板 |

## 使用要点

- anysearch：`python skills/anysearch/scripts/anysearch_cli.py search "查询" --max_results 5`；垂直域先 `get_sub_domains --domain <域>` 拿 sub_domain/params（tag=sub_domain）；key 存 `skills/anysearch/.env`（gitignored）
- prompt-engineer：触发词 `/prompt`，适合优化任何 prompt
- skill-creator：**写新 skill / 评估入库质量时先读它**——本仓所有打包应遵循其规范

## 相关分类

- [[atlas/人格与社交.md|人格与社交]]（人设 prompt 可用 prompt-engineer 优化）
- [[atlas/视频制作.md|视频制作]]（生成类 prompt 均适用）
