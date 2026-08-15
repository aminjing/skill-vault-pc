# 抖音视频下载（无水印）

## 用途

解析抖音分享链接（`v.douyin.com` 短链），获取无水印原画质视频并下载到本地。基于 JoeanAmier/TikTokDownloader 核心库 + **ttwid 匿名 cookie 方案**——无需用户登录抖音、无需手动提供 cookie。

## 触发场景

- 用户发来抖音分享链接/口令（`复制打开抖音... @url:https://v.douyin.com/xxx/`）
- 用户说"下载这个抖音视频""抖音视频存下来"

## 执行步骤

1. 提取分享链接（正则 `https?://v\.douyin\.com/[A-Za-z0-9_\-]+/?`）
2. 运行 `python Z:\chang-yong\.tools\download_douyin.py <分享链接> <输出目录>`（Python 环境：`Z:\chang-yong\.tools\TikTokDownloader` 的 uv venv，命令 `cd Z:\chang-yong\.tools\TikTokDownloader && uv run python ../download_douyin.py ...`）
3. 视频自动存为 `<日期>_<标题>_<video_id>.mp4`（标题自动清洗非法字符）

## 依赖

- 本机部署：`Z:\chang-yong\.tools\TikTokDownloader`（uv sync 完成）+ `download_douyin.py`（ttwid 匿名 cookie + Detail API）
- 网络：www.douyin.com 可达（响应慢，约 12s；脚本已设 timeout=30）
- 下载 CDN（douyinvod.com）可达，实测 2-6MB/s

## 原理（防失效备忘）

- 抖音 2025+ 全面风控：无 cookie 的 SSR/API 均返回空壳
- 破解：`ttwid.bytedance.com/ttwid/union/register/` 匿名注册 ttwid → 作为 cookie 随 `aweme/v1/web/aweme/detail/`（带 a_bogus 签名）请求 → 拿到 play_addr 无水印 URL
- 若失效：更新 TikTokDownloader 库（签名算法 a_bogus 会随抖音升级而失效）；备选方案见 SOURCE.md

## 示例

```
$ uv run python ../download_douyin.py "https://v.douyin.com/-nBTmIIR66g/" "Z:/chang-yong/video/2026-08-15"
[解析] 【非遗傩舞】... (id=7524971455848959290) 30.3s
[下载] 2026-08-15_【非遗傩舞】..._7524971455848959290.mp4
[统计] 20.4MB / 3.5s / 5.9MB/s
```

## 备选方案

- **res-downloader**（`Z:\chang-yong\.tools\res-downloader.exe`，3.1.3）：抓包式 GUI，浏览器播放时抓取，不依赖抖音 API（改版免疫），适合手动日常下载
- **douyin-mcp-server**：❌ 已失效（iesdouyin 页面结构改版，`_ROUTER_DATA` 消失），勿用
