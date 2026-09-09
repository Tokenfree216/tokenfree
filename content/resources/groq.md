---
title: "Groq Cloud"
date: 2026-09-05T23:20:00+08:00
provider: "Groq"
api_base: "https://api.groq.com/openai/v1"
model: "openai/gpt-oss-120b、llama、whisper 等"
signup: "https://console.groq.com/keys"
weight: 2
expired: false
---

## 免费内容

免费计划下所有模型均可调用，无需信用卡。Groq 的特点是推理速度极快（自研 LPU 芯片）。

## 速率限制

按组织和模型分别限制。官方文档示例值：gpt-oss-120b 为 30 RPM / 1000 RPD，whisper-large-v3 为 20 RPM / 2000 RPD。精确数值以控制台 Limits 页面为准。

## 调用示例（OpenAI 兼容）

```bash
curl https://api.groq.com/openai/v1/chat/completions \
  -H "Authorization: Bearer 你的API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "openai/gpt-oss-120b",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

## 注意事项

- 免费层限速较紧，适合学习和低频测试
- 需要能访问海外服务的网络环境

## 官方文档

- 速率限制：https://console.groq.com/docs/rate-limits
