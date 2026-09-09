---
title: "OpenRouter 免费模型"
date: 2026-09-05T23:20:00+08:00
provider: "OpenRouter"
api_base: "https://openrouter.ai/api/v1"
model: "所有 :free 后缀的模型变体"
signup: "https://openrouter.ai/keys"
weight: 3
expired: false
---

## 免费内容

OpenRouter 是模型聚合平台，一个 Key 可以调用 DeepSeek、Qwen、Llama 等几十家模型。模型 ID 带 `:free` 后缀的变体永久免费（官方 FAQ 原话：always provided for free and has low rate limits）。

## 速率限制

第三方一致引用官方口径：20 RPM；未充值账户 50 次/天，累计充值满 $10 后提升至 1000 次/天。以官方 limits 页面为准。

## 调用示例（OpenAI 兼容）

```bash
curl https://openrouter.ai/api/v1/chat/completions \
  -H "Authorization: Bearer 你的API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "deepseek/deepseek-chat-v3-0324:free",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

免费模型列表可在 https://openrouter.ai/models?q=free 实时查询。

## 注意事项

- 免费模型排队较多时延迟偏高
- 免费模型供应商可能记录请求数据，不要发送敏感信息

## 官方文档

- FAQ：https://openrouter.ai/docs/faq
- 限制说明：https://openrouter.ai/docs/api/reference/limits
