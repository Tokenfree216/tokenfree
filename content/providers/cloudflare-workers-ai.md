---
title: "Cloudflare Workers AI"
date: 2026-09-05T23:20:00+08:00
provider: "Cloudflare"
api_base: "https://api.cloudflare.com/client/v4/accounts/{ACCOUNT_ID}/ai/v1"
model: "Llama、Qwen、gpt-oss-120b 等"
signup: "https://dash.cloudflare.com"
weight: 7
expired: false
---

## 免费内容

官方定价页确认：免费额度为每天 10000 Neurons（Cloudflare 的计量单位），超出后需升级 Workers Paid（$5/月起）。模型库含 Llama、Qwen、gpt-oss-120b、GLM Flash 等。

## 调用示例（OpenAI 兼容）

需要先在 Cloudflare 控制台获取 Account ID 并创建 API Token：

```bash
curl "https://api.cloudflare.com/client/v4/accounts/你的ACCOUNT_ID/ai/v1/chat/completions" \
  -H "Authorization: Bearer 你的API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "@cf/openai/gpt-oss-120b",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

## 注意事项

- 需要绑信用卡验证身份（免费额度内不扣费）
- Neurons 与 token 的换算关系见官方定价页

## 官方文档

- 定价：https://developers.cloudflare.com/workers-ai/platform/pricing/
