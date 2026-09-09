---
title: "Google Gemini API（AI Studio）"
date: 2026-09-05T23:20:00+08:00
provider: "Google AI Studio"
api_base: "https://generativelanguage.googleapis.com/v1beta/openai/"
model: "gemini-3.8-flash 等 Flash 系列"
signup: "https://aistudio.google.com/api-keys"
weight: 1
expired: false
---

## 免费内容

Gemini Flash 系列模型在免费层下输入、输出均不收费。免费层无需绑卡，用 Google 账号登录即可创建 API Key。

## 速率限制

免费层限制按项目和模型动态生效，没有固定公示值，以 AI Studio 控制台的 Rate Limits 页面为准。

## 调用示例（OpenAI 兼容）

```bash
curl https://generativelanguage.googleapis.com/v1beta/openai/chat/completions \
  -H "Authorization: Bearer 你的API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gemini-3.8-flash",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

## 注意事项

- 免费层的请求数据会被 Google 用于改进产品，不要发送敏感信息
- 需要能访问 Google 服务的网络环境

## 官方文档

- 定价：https://ai.google.dev/gemini-api/docs/pricing
- 速率限制：https://ai.google.dev/gemini-api/docs/rate-limits
