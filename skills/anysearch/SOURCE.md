# 来源

- 原仓库: https://github.com/anysearch-ai/anysearch-skill
- 作者: AnySearch Team
- 许可: Apache-2.0
- 入库日期: 2026-08-21
- 归档 commit: （提交后补）
- 原项目版本: v3.0.1
- 备注:
  - 统一实时搜索：web 通用搜索 + 垂直域（finance/academic/travel/health/code/legal/gaming/film/business/security/ip/energy/environment/agriculture/resource/social_media）+ 批量并行 + 网页内容提取（extract）
  - 调用：`python skills/anysearch/scripts/anysearch_cli.py <search|batch_search|extract|get_sub_domains|doc> ...`（Python > Node > Shell 自动检测；也可用 runtime.conf 预置）
  - 垂直域搜索前必须先 `get_sub_domains --domain <域>` 拿 sub_domain 和必填参数（tag = sub_domain）
  - **API key 存 `skills/anysearch/.env`（已 gitignore，严禁提交）**；也可用 `--api_key` 或环境变量 `ANYSEARCH_API_KEY`；无 key 可匿名（限流更低）
  - 2026-08-21 拍板：**本仓主要搜索源**（中文效果好，~700ms 返回）；用户 key 由用户提供
  - 本机网络：GitHub 克隆走 gh-proxy（`git clone https://gh-proxy.com/https://github.com/...`）
