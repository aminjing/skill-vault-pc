# 测试区（Staging）

新 skill 入库前的暂存目录。流程见 `docs/调用协议.md` 第一节：

1. 新 skill 先放这里（`_staging/<skill-name>/`，含 SKILL.md + SOURCE.md + 原文件）
2. 按 SKILL.md 实际测试功能（依赖就绪、典型场景跑通）
3. **测试通过 → 移入 `../<skill-name>/` 正式目录**（同时更新 skills/README.md 索引 + atlas 分类）
4. 测试失败 → 修复或留在测试区并记录原因

> 此目录不参与 Obsidian 正式导航，仅作过渡。
