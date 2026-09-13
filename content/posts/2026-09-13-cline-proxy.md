---
title: "0成本反代cline教程"
date: 2026-09-13T23:14:19+08:00
description: "Cline 免费模型反代统一使用的完整教程：前期准备、项目部署、OAuth 登录、可用模型与 curl 调用示例。"
tags: ["免费", "教程", "Cline", "反代"]
---
# 0成本反代cline教程

说明：文中示例的服务器地址、端口与 API Key 均使用占位符展示，发布前请替换为你自己的实际配置。

## 背景

Cline 现在提供一些免费模型，不过使用的人并不多；每个 agent 都有一定的免费额度，每次都切换 agent 实在不方便，所以考虑把 Cline 的免费模型通过反代 API 的方式统一使用。

## 前期准备

- 一个 Google 账户
- 一台云服务器（本地搭建也可以；为了方便多设备都能使用 API，推荐部署在服务器上）
- 一个 Code Agent（Codex、CC 都可以）

## 反代 GitHub 项目

项目地址：https://github.com/YuJunZhiXue/Cline-proxy（网上找到的项目，作者修 bug 比较慢）

项目有两个 bug，作者已修复并提了 PR，可以直接使用 fork 版本：https://github.com/Tokenfree216/Cline-proxy

部署方式：把代码仓库告诉 AI，让它将项目部署到指定端口即可。

![](/images/UXdCbX0zzoVecexVkvJchO86nxh.png)

部署完成后，直接通过 OAuth 登录，有 Google 账号即可直接登录，按提示操作即可。

登录后新建一个 Key，就可以愉快地使用免费模型了。

![](/images/YeIAbPcHvodBnkxH30xc6kNyn5e.png)

可用的模型：

```Plain Text
cline-free/muse-spark-1.3-contributor
z-ai/glm-5.3-flash
deepseek/deepseek-v4-flash
```

主要使用以上三个模型，其他模型没有测试，有兴趣的可以自行测试，都是免费的。

```Bash
cline-free/longcat-2.0
cline-free/muse-spark-1.3-contributor
cline-free/solar-pro4
deepseek/deepseek-v4-flash
poolside/laguna-s-2.1:free
stepfun/step-3.7-flash
z-ai/glm-5.3-flash
```

![](/images/UMRUbs1SQoHScfxy8Ahce2vknJf.png)

据说 muse-spark-1.3-contributor 非常强大，大家可以体验体验。

## curl 命令

查看有哪些可用模型：

```Bash
curl -X GET http://<服务器IP>:<端口>/models \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <你的API Key>"
```

测试 OpenAI Completions 协议：

```Bash
curl -X POST http://<服务器IP>:<端口>/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <你的API Key>" \
  -d '{
    "model": "cline-free/muse-spark-1.3-contributor",
    "messages": [
      {"role": "user", "content": "讲个冷笑话"}
    ],
    "stream": true
  }'
```

## 接入到 new-api（非必要）

可以把反代 API 接入到 new-api 中作为渠道统一管理，并在 new-api 中测试渠道连通性（可选步骤）。

## 额度和并发测试

这一块后续补充。
