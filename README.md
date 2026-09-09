# TokenFree

> 汇聚全球 AI 提供商资源，让开发者自由调用

🌐 **网站**: [https://tokenfree.news](https://tokenfree.news)

---

## 📰 最新文章

<!-- 每次发布新文章后，手动更新这个列表 -->

| 日期 | 文章 |
|------|------|
| 2026-09-10 | [测试自动部署](/posts/test-auto-deploy/) |
| 2026-09-06 | [文章标题](/posts/2026-09-06/) |
| 2026-09-06 | [文章标题](/posts/2026-09-06-/) |
| 2026-09-05 | [Hello World](/posts/hello-world/) |

---

## 🔑 提供商列表

- [OpenRouter](/providers/openrouter/) — 多模型聚合
- [SiliconFlow](/providers/siliconflow/) — 中文模型
- [Groq](/providers/groq/) — 超高速推理
- [Google Gemini](/providers/google-gemini/) — Gemini 系列
- [Cerebras](/providers/cerebras/) — 专用推理加速
- [Mistral](/providers/mistral/) — 欧洲开源模型
- [BigModel GLM](/providers/bigmodel-glm/) — 智谱 GLM
- [NVIDIA NIM](/providers/nvidia-nim/) — GPU 加速
- [Cloudflare Workers AI](/providers/cloudflare-workers-ai/) — 边缘推理

---

## 📝 提交新文章

在 `content/posts/` 目录下新建 `.md` 文件，格式如下：

```markdown
---
title: "文章标题"
date: 2026-09-10T12:00:00+08:00
provider: "OpenRouter"      # 关联的提供商（可选）
models: ["gpt-4o", "claude-3"]  # 涉及的模型（可选）
tags: ["免费", "教程"]      # 标签
---

正文内容...
```

### 提交提供商

在 `content/providers/` 目录下新建 `.md` 文件：

```markdown
---
title: "提供商名称"
date: 2026-09-10T00:00:00+08:00
provider: "官方名称"
api_base: "https://api.example.com/v1"
model: "gpt-4o"
signup: "https://example.com/signup"
weight: 1
expired: false
---

## 简介

简要介绍。

## 使用方法

\`\`\`bash
curl https://api.example.com/v1/chat/completions \\
  -H "Authorization: Bearer YOUR_TOKEN" \\
  -H "Content-Type: application/json" \\
  -d \x27{"model": "model-name", "messages": [{"role": "user", "content": "Hello"}]}\x27
\`\`\`
```

---

## 🚀 自动部署

```bash
git add . && git commit -m "add post" && git push
```

Push 后 GitHub Actions 自动部署，约 13 秒生效。

---

📧 tokenfree@126.com
