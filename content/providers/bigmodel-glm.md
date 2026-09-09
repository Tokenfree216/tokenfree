---
title: "智谱 BigModel（GLM Flash 系列）"
date: 2026-09-05T23:20:00+08:00
provider: "智谱 AI"
api_base: "https://open.bigmodel.cn/api/paas/v4"
model: "GLM-4.7-Flash、GLM-4.6V-Flash 等"
signup: "https://open.bigmodel.cn"
weight: 4
expired: false
---

## 免费内容

GLM Flash 系列永久免费调用（GLM-4.7-Flash 于 2026 年 1 月发布并开源，1 并发限制）。旧模型 ID（如 GLM-4.5-Flash）会自动路由到新版。新注册用户另赠 2000 万 tokens 额度。国内直连，无需特殊网络。

## 调用示例（OpenAI 兼容）

```bash
curl https://open.bigmodel.cn/api/paas/v4/chat/completions \
  -H "Authorization: Bearer 你的API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "glm-4.7-flash",
    "messages": [{"role": "user", "content": "你好"}]
  }'
```

## 注意事项

- 免费模型并发限制为 1，不适合批量任务
- 国际版请使用 https://z.ai ，API Base 为 `https://api.z.ai/api/paas/v4`

## 官方文档

- https://docs.bigmodel.cn
