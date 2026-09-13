# TokenFree

> 汇聚全球 AI 提供商资源，让开发者自由调用

🌐 **网站**: [https://tokenfree.news](https://tokenfree.news)

---

## 📰 最新文章

<!-- 每次发布新文章后，手动更新这个列表 -->

| 日期 | 文章 |
|------|------|
| 2026-09-13 | [0成本反代cline教程](/posts/2026-09-13-cline-proxy/) |
| 2026-09-10 | [测试自动部署](/posts/test-auto-deploy/) |
| 2026-09-06 | [文章标题](/posts/2026-09-06/) |
| 2026-09-06 | [文章标题](/posts/2026-09-06-/) |
| 2026-09-05 | [Hello World](/posts/hello-world/) |

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

标准发布流程：**创建文章 → 配图 → 安全审查 → 更新最新文章列表 → push 自动部署**。

### 1. 创建文章文件

文章统一放在 `content/posts/` 下，两种结构：

- **纯文字文章**（单文件）：`content/posts/<slug>.md`
- **带图文章**（page bundle，推荐带图时使用）：`content/posts/<slug>/index.md`，图片放同一目录

`slug` 命名规范：`日期-英文描述`，例如 `2026-09-13-cline-proxy`。

### 2. Front Matter 格式

```markdown
---
title: "文章标题"
date: 2026-09-10T12:00:00+08:00    # 使用 UTC+8
description: "文章简介（可选）"
provider: "OpenRouter"              # 关联的提供商（可选）
models: ["gpt-4o", "claude-3"]      # 涉及的模型（可选）
tags: ["免费", "教程"]              # 标签（可选）
---

正文内容...
```

### 3. 图片处理（page bundle）

- 图片放进文章自己的目录 `content/posts/<slug>/`，正文用相对路径引用：`![](./图片名.png)`
- ⚠️ **不要**把图片放到 `static/images/`——部署流水线只同步 `content/`，放 static 的图片会 404

```
content/posts/2026-09-13-cline-proxy/
├── index.md
└── 截图1.png
```

### 4. 安全审查（发布前必查）

对外发布前检查正文，禁止出现以下内容，敏感信息用占位符替代（如 `<服务器IP>`、`<端口>`、`<你的API Key>`）：

- 服务器 IP / 域名 / 端口号
- API Key / Token / 密码
- 内部链接与内部项目名

### 5. 更新最新文章列表

在 README「📰 最新文章」表**顶部**插入新行，列表最多保留 8 行：

```markdown
| 日期 | 文章 |
|------|------|
| 2026-09-13 | [文章标题](/posts/<slug>/) |
```

### 6. 推送发布

```bash
git add . && git commit -m "add post: 文章标题" && git push
```

Push 后 GitHub Actions 自动部署，约 13 秒生效。

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
