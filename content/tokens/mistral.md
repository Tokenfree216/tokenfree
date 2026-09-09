---
title: "Mistral AI Studio"
date: 2026-09-05T23:20:00+08:00
provider: "Mistral AI"
api_base: "https://api.mistral.ai/v1"
model: "mistral-small、magistral 等"
signup: "https://console.mistral.ai"
weight: 8
expired: false
---

## 免费内容

官方提供 Free/Experiment 计划（免费模式），激活后即可生成 API Key 调用模型，适合测试和评估。限速较严格，具体数值以官方控制台为准。

## 调用示例（OpenAI 兼容）

```bash
curl https://api.mistral.ai/v1/chat/completions \
  -H "Authorization: Bearer 你的API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "mistral-small-latest",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

## 注意事项

- 免费层的请求数据默认可能被用于训练，不要发送敏感信息
- 需要能访问海外服务的网络环境

## 官方文档

- https://docs.mistral.ai/getting-started/quickstart/
