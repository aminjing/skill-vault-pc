# 来源

- 原仓库: https://github.com/ElmerAlan-an/human_chat_operit (2⭐)
- 作者: ElmerAlan-an
- 许可: LICENSE 随附
- 入库日期: 2026-08-17
- 归档 commit: 3316e2e
- 原项目版本: main 最新 (clone 2026-08-17)
- 备注: **真人聊天增强（Operit 版）**——双版本：Skill（轻量 Prompt）/ ToolPkg（JS 硬检测引擎）。核心规则：短句口语化（2-4 句微信体）、**禁止词清单**（作为AI助手/综上所述/希望以上信息对您有所帮助等）、**反重复**（连续两条回复不得高度相似，重复≥2 次强制换话题）、4 种人格风格（natural/humorous/warm/serious）+ **auto 情绪映射**（开心→幽默/伤心→温暖/愤怒→理性/疲惫→温暖）。**已实测**（2026-08-17）：按规则生成"加班晚归"warm 回复，口语自然无 AI 腔（"明儿还这么顶就吱声，咖啡我包"）。**与 crush 契合**：反重复+情绪映射可并入"她"的回复策略；ToolPkg 硬检测（ngram 反重复/AI 味黑名单）思路可参考。原项目面向 Operit 手机 App，本仓只入 Skill 版规则（prompt 思想可移植）。
