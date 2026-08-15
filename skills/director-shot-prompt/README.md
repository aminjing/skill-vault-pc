# 导演镜头提示词 Skill

这是一个用于把“已生成图片 + 脚本”快速转化为导演式视频生成提示词（shot prompt）的 Skill 项目。

## 核心思路

参考主流图生视频模型（如可灵、Runway、Pika 等）的“参考图 + 描述”模式，将上传的若干图片按镜头角色分类：

- **微距/材质**：建立感官触碰
- **交互/动作**：驱动叙事
- **全景/空间**：完成空间跨越
- **状态/氛围**：保持视觉一致

## 项目结构

```
director-shot-prompt/
├── README.md            # 项目说明
├── SKILL.md             # Skill 定义（可注册到 .trae/skills）
├── prompt-framework.md  # 提示词框架与示例
└── .trae/skills/director-shot-prompt/SKILL.md  # 实际注册文件
```

## 使用方式

1. 将 `.trae/skills/director-shot-prompt/SKILL.md` 注册到 TRAE 的 skills 目录后，当你上传图片+脚本时即可自动触发。
2. 或直接把图片和脚本发给我，并说“用导演镜头提示词 skill 生成提示词”。

## 后续使用流程

当你上传图片和脚本时，我会：

1. 识别每张图片的镜头角色（材质 / 动作 / 全景 / 氛围）。
2. 按脚本拆分为 2-5 个 scene beat。
3. 生成每段镜头的中文视频 prompt，并保证镜头间转场流畅。
4. 输出完整的导演镜头提示词序列与转场建议。
