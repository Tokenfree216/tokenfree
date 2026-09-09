---
title: "Cerebras（$5 试用额度，非常驻免费）"
date: 2026-09-05T23:20:00+08:00
provider: "Cerebras"
api_base: "https://api.cerebras.ai/v1"
model: "gpt-oss-120b、qwen 系列"
signup: "https://cloud.cerebras.ai"
weight: 9
expired: false
---

## 免费内容

**注意：Cerebras 已取消永久免费层。**官方 FAQ 明确回答 "Is there a permanently free tier? No." 目前只有 Free Trial：新账号绑定支付方式后赠送 $5 额度，30 天过期，过期即停。推理速度极快（自研 WSE 芯片）。

## 试用限速

gpt-oss-120b / qwen 系列：5 RPM、30K TPM、1M TPD（以官方文档为准）。

## 调用示例（OpenAI 兼容）

```bash
curl https://api.cerebras.ai/v1/chat/completions \
  -H "Authorization: Bearer 你的API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-oss-120b",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

## 注意事项

- 需绑定支付方式才能领取试用额度
- 想要长期免费的请用本页其他渠道（Groq、Gemini 等）

## 官方文档

- 速率限制：https://inference-docs.cerebras.ai/support/rate-limits
