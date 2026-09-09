---
title: "SiliconFlow 硅基流动"
date: 2026-09-05T23:20:00+08:00
provider: "硅基流动"
api_base: "https://api.siliconflow.cn/v1"
model: "Qwen3-8B、DeepSeek-R1-Distill 等"
signup: "https://cloud.siliconflow.cn/account/ak"
weight: 5
expired: false
---

## 免费内容

模型广场中价格标注为 0 的模型可免费调用（受固定限速）。2026 年 8 月的免费模型包括 Qwen/Qwen3-8B、deepseek-ai/DeepSeek-R1-Distill-Qwen-7B、THUDM/GLM-Z1-9B-0414、BAAI/bge-m3（向量）等，具体清单以官方实时页面为准。新注册用户另有赠送额度。国内直连。

## 调用示例（OpenAI 兼容）

```bash
curl https://api.siliconflow.cn/v1/chat/completions \
  -H "Authorization: Bearer 你的API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "Qwen/Qwen3-8B",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

## 注意事项

- 免费模型清单会变动，以模型广场实时价格为准
- 免费模型限速固定，高频调用请用付费模型

## 官方文档

- https://docs.siliconflow.cn
