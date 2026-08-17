<p align="center">
  <img src="docs/logo-xiaoyu-hd.png" width="72" alt="小语 AI">
  <br>
  <b style="color:#c8a44a">小语 · AI</b>
</p>

# 万像人物 · AI 人物写真提示词生成技能

> 专业 AI 人物写真提示词生成体系，蒸馏自《万像人物写真提示词生成系统》（267 页），适配 Midjourney / Stable Diffusion / 即梦 Dreamina / Imagen 3。

## 这是什么

一套**专业的人物写真提示词生成规则包**。当 AI 需要生成人物写真提示词（证件照/商务肖像/古风/情绪写真/集体照等）时，按这套体系输出**纯净自然语言提示词**，通用四大主流绘画平台。

## 安装

```bash
# 方式一：clone 到技能目录（pi / Claude Code / Codex 通用）
git clone https://github.com/xueshao1716/wanxiang-portrait-skill.git ~/.agents/skills/wanxiang-portrait-skill

# 方式二：pi-web 工作台内置（已含此技能，左侧 ⚡ 技能面板可见）
```

## 技能内容

- **提示词五要素**：主体/服饰/构图/光影/风格（完整填写，不可空缺）
- **5 套场景模板**：古风华丽 / 情绪电影感 / 创意概念 / 专业环境人像 / 系列叙事
- **专项场景参数**：证件照（35×45mm 画幅/三点布光）、商务肖像（85mm/杜乡微笑）、集体照、深色肖像、零器材模式、超高清协议
- **去AI化真实感**：肤色光学/生物痕迹/精确描述优先
- **平台适配**：MJ / SD / Imagen3 / 即梦 各自格式
- **完整文档**：wx_full.txt（37 章全文，含内部协议翻译手册）

## 使用

在对话中说：
```
用万像人物生成一个古风女子肖像的 Midjourney 提示词
生成商务男士形象照提示词（即梦平台）
```

AI 会按五要素 + 场景模板 + 平台格式输出专业提示词。

## 目录结构

```
wanxiang-portrait-skill/
├── README.md
└── wanxiang-portrait/
    ├── SKILL.md      # 技能定义（核心）
    └── wx_full.txt   # 完整系统文档（37 章）
```

## License

MIT
