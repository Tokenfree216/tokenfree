---
title: "NVIDIA NIM（build.nvidia.com）"
date: 2026-09-05T23:20:00+08:00
provider: "NVIDIA"
api_base: "https://integrate.api.nvidia.com/v1"
model: "100+ 托管开源模型"
signup: "https://build.nvidia.com"
weight: 6
expired: false
---

## 免费内容

注册免费的 NVIDIA Developer Program 账号即可生成 `nvapi-` 开头的 Key，无需信用卡，可调用 100 多个托管开源模型（Llama、DeepSeek、Qwen 等）。免费层约 40 RPM，定位开发和测试。Key 有效期 1 年。

## 调用示例（OpenAI 兼容）

```bash
curl https://integrate.api.nvidia.com/v1/chat/completions \
  -H "Authorization: Bearer 你的API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "meta/llama-3.3-70b-instruct",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

## 注意事项

- 免费层用于开发测试，生产环境需申请提升限额或自建 NIM
- 需要能访问海外服务的网络环境

## 官方文档

- https://docs.api.nvidia.com
