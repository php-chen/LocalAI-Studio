# LocalAI Studio

A complete AI content generation platform consisting of four sub-projects: user client, admin backend, cloud service, and local AI processing.

## Language Selection

English | [简体中文](./README_zh-CN.md) | [繁體中文](./README_zh-TW.md) | [日本語](./README_ja-JP.md) | [한국어](./README_ko-KR.md)

## Project Overview

LocalAI Studio is a modern AI content creation platform supporting text-to-image and text-to-video generation. It adopts a distributed architecture that leverages local computing resources for AI processing, saving costs while protecting privacy.

## Sub-Project List

| No. | Sub-Project Name | Tech Stack | Main Features | GitHub URL |
|-----|-----------------|-----------|--------------|-----------|
| 1 | user-web-clint | React 18.2 + TypeScript 5.5 + Vite 5.0 + Ant Design 5.10 + Tailwind CSS 3.4 | User client, providing AI image/video generation, works management, material library, points system, and more | [php-chen/LocalAI-Studio--user-web-clint](https://github.com/php-chen/LocalAI-Studio--user-web-clint) |
| 2 | user-admin-server-clint | React 19 + TypeScript + Vite + Ant Design 6 + Tailwind CSS | Admin backend, providing user management, works management, points management, task management, AI model configuration, and more | [php-chen/LocalAI-Studio--user-admin-server-clint](https://github.com/php-chen/LocalAI-Studio--user-admin-server-clint) |
| 3 | cloud-sever-clint-python | Flask + SQLite + JWT | Cloud service, providing enterprise-grade security authentication, task queue, distributed AI processing scheduling, and other core backend services | [php-chen/LocalAI-Studio--cloud-sever-clint-python](https://github.com/php-chen/LocalAI-Studio--cloud-sever-clint-python) |
| 4 | local-AI-server-clint-python | Flask + ComfyUI | Local AI service, providing ComfyUI remote control API, workflow management, task queue, status monitoring, and more | [php-chen/LocalAI-Studio--local-AI-server-clint-python](https://github.com/php-chen/LocalAI-Studio--local-AI-server-clint-python) |

## System Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                       LocalAI Studio Architecture                    │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌─────────────────┐         ┌─────────────────┐                     │
│  │  user-web-clint │◄───────►│ cloud-sever-    │                     │
│  │  (User Client)  │         │ clint-python    │                     │
│  └─────────────────┘         │  (Cloud Service)│                     │
│  ┌─────────────────┐         └────────┬────────┘                     │
│  │ user-admin-     │◄─────────────────┘                              │
│  │ server-clint    │                                                  │
│  │ (Admin Backend) │                                                  │
│  └─────────────────┘         ┌─────────────────┐                     │
│                              │ local-AI-server-│                     │
│                              │ clint-python    │                     │
│                              │  (Local AI Svc) │◄───────────────────┐│
│                              └─────────────────┘                    ││
│                                                                      ││
│                              ┌─────────────────┐                    ││
│                              │     ComfyUI     │◄───────────────────┘│
│                              │   (AI Engine)   │                     │
│                              └─────────────────┘                     │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

## Core Features

- 🔐 Enterprise-grade Security: RSA-OAEP password encryption, JWT dual-token authentication, SHA-256 password hashing
- 🤖 AI Model Integration: Support for text-to-image, image-to-image, text-to-video, image-to-video, and more
- 🚀 Distributed Processing: Leverage local computing resources, reduce cloud costs, protect data privacy
- 📊 Complete Management: User management, works management, points system, task monitoring, AI model configuration

## License

MIT License
