# LocalAI Studio

一个完整的 AI 内容生成平台，包含用户端、管理端、云端服务和本地 AI 处理四个子项目。

## 语言选择

[English](../README.md) | 简体中文 | [繁體中文](./README_zh-TW.md) | [日本語](./README_ja-JP.md) | [한국어](./README_ko-KR.md)

## 项目简介

LocalAI Studio 是一个现代化的 AI 内容创作平台，支持文本生成图像、文本生成视频等功能，采用分布式架构，利用本地计算资源进行 AI 处理，既节省成本又保护隐私。

## 子项目列表

| 序号 | 子项目名称 | 技术栈 | 主要功能 | GitHub 地址 |
|------|-----------|--------|---------|------------|
| 1 | user-web-clint | React 18.2 + TypeScript 5.5 + Vite 5.0 + Ant Design 5.10 + Tailwind CSS 3.4 | 用户端，提供 AI 图像/视频生成、作品管理、素材库、积分系统等功能 | [php-chen/LocalAI-Studio--user-web-clint](https://github.com/php-chen/LocalAI-Studio--user-web-clint) |
| 2 | user-admin-server-clint | React 19 + TypeScript + Vite + Ant Design 6 + Tailwind CSS | 管理后台，提供用户管理、作品管理、积分管理、任务管理、AI 模型配置等功能 | [php-chen/LocalAI-Studio--user-admin-server-clint](https://github.com/php-chen/LocalAI-Studio--user-admin-server-clint) |
| 3 | cloud-sever-clint-python | Flask + SQLite + JWT | 云端服务，提供企业级安全认证、任务队列、分布式 AI 处理调度等核心后端服务 | [php-chen/LocalAI-Studio--cloud-sever-clint-python](https://github.com/php-chen/LocalAI-Studio--cloud-sever-clint-python) |
| 4 | local-AI-server-clint-python | Flask + ComfyUI | 本地 AI 服务，提供 ComfyUI 远程控制 API、工作流管理、任务队列、状态监控等功能 | [php-chen/LocalAI-Studio--local-AI-server-clint-python](https://github.com/php-chen/LocalAI-Studio--local-AI-server-clint-python) |

## 系统架构

```
┌─────────────────────────────────────────────────────────────────────┐
│                         LocalAI Studio 架构                          │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌─────────────────┐         ┌─────────────────┐                     │
│  │  user-web-clint │◄───────►│ cloud-sever-    │                     │
│  │   (用户端)      │         │ clint-python    │                     │
│  └─────────────────┘         │   (云端服务)    │                     │
│  ┌─────────────────┐         └────────┬────────┘                     │
│  │ user-admin-     │◄─────────────────┘                              │
│  │ server-clint    │                                                  │
│  │  (管理后台)     │                                                  │
│  └─────────────────┘         ┌─────────────────┐                     │
│                              │ local-AI-server-│                     │
│                              │ clint-python    │                     │
│                              │  (本地AI服务)   │◄───────────────────┐│
│                              └─────────────────┘                    ││
│                                                                      ││
│                              ┌─────────────────┐                    ││
│                              │     ComfyUI     │◄───────────────────┘│
│                              │   (AI 引擎)     │                     │
│                              └─────────────────┘                     │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

## 核心特性

- 🔐 企业级安全：RSA-OAEP 密码加密、JWT 双令牌认证、SHA-256 密码哈希
- 🤖 AI 模型集成：支持文本到图像、图像到图像、文本到视频、图像到视频等多种模型
- 🚀 分布式处理：利用本地计算资源，降低云端成本，保护数据隐私
- 📊 完整管理：用户管理、作品管理、积分系统、任务监控、AI 模型配置

## 许可证

MIT License
