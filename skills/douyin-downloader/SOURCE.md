# 来源

- 原仓库: https://github.com/JoeanAmier/TikTokDownloader (15.4k⭐, Python)
- 作者: JoeanAmier
- 许可: Apache-2.0
- 入库日期: 2026-08-15
- 归档 commit: 待提交后补
- 原项目版本: master 最新 (clone 于 2026-08-15)
- 备注: 打包为 skill 时采用**核心库直调 + ttwid 匿名 cookie** 方案（绕过官方 TUI 交互，无需登录）。同时实测对比过:
  - putyy/res-downloader 3.1.3 (19k⭐, Go GUI 抓包): 可用但需手动 GUI
  - yzfly/douyin-mcp-server (1.2k⭐): 已失效 (iesdouyin 页面改版, _ROUTER_DATA 消失)
- 本地部署: Z:\chang-yong\.tools\TikTokDownloader (uv sync) + download_douyin.py + get_douyin_cookie.py
