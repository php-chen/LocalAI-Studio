# LocalAI Studio

一個完整的 AI 內容生成平台，包含用戶端、管理端、雲端服務和本地 AI 處理四個子專案。

## 語言選擇

[English](../README.md) | [简体中文](./README_zh-CN.md) | 繁體中文 | [日本語](./README_ja-JP.md) | [한국어](./README_ko-KR.md)

## 專案簡介

LocalAI Studio 是一個現代化的 AI 內容創作平台，支援文字生成圖像、文字生成影片等功能，採用分散式架構，利用本地計算資源進行 AI 處理，既節省成本又保護隱私。

## 子專案列表

| 序號 | 子專案名稱 | 技術棧 | 主要功能 | GitHub 地址 |
|------|-----------|--------|---------|------------|
| 1 | user-web-clint | React 18.2 + TypeScript 5.5 + Vite 5.0 + Ant Design 5.10 + Tailwind CSS 3.4 | 用戶端，提供 AI 圖像/影片生成、作品管理、素材庫、積分系統等功能 | [php-chen/LocalAI-Studio--user-web-clint](https://github.com/php-chen/LocalAI-Studio--user-web-clint) |
| 2 | user-admin-server-clint | React 19 + TypeScript + Vite + Ant Design 6 + Tailwind CSS | 管理後台，提供用戶管理、作品管理、積分管理、任務管理、AI 模型配置等功能 | [php-chen/LocalAI-Studio--user-admin-server-clint](https://github.com/php-chen/LocalAI-Studio--user-admin-server-clint) |
| 3 | cloud-sever-clint-python | Flask + SQLite + JWT | 雲端服務，提供企業級安全認證、任務佇列、分散式 AI 處理排程等核心後端服務 | [php-chen/LocalAI-Studio--cloud-sever-clint-python](https://github.com/php-chen/LocalAI-Studio--cloud-sever-clint-python) |
| 4 | local-AI-server-clint-python | Flask + ComfyUI | 本地 AI 服務，提供 ComfyUI 遠端控制 API、工作流管理、任務佇列、狀態監控等功能 | [php-chen/LocalAI-Studio--local-AI-server-clint-python](https://github.com/php-chen/LocalAI-Studio--local-AI-server-clint-python) |

## 系統架構

```
┌─────────────────────────────────────────────────────────────────────┐
│                         LocalAI Studio 架構                          │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌─────────────────┐         ┌─────────────────┐                     │
│  │  user-web-clint │◄───────►│ cloud-sever-    │                     │
│  │   (用戶端)      │         │ clint-python    │                     │
│  └─────────────────┘         │   (雲端服務)    │                     │
│  ┌─────────────────┐         └────────┬────────┘                     │
│  │ user-admin-     │◄─────────────────┘                              │
│  │ server-clint    │                                                  │
│  │  (管理後台)     │                                                  │
│  └─────────────────┘         ┌─────────────────┐                     │
│                              │ local-AI-server-│                     │
│                              │ clint-python    │                     │
│                              │  (本地AI服務)   │◄───────────────────┐│
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

- 🔐 企業級安全：RSA-OAEP 密碼加密、JWT 雙令牌認證、SHA-256 密碼雜湊
- 🤖 AI 模型整合：支援文字到圖像、圖像到圖像、文字到影片、圖像到影片等多種模型
- 🚀 分散式處理：利用本地計算資源，降低雲端成本，保護資料隱私
- 📊 完整管理：用戶管理、作品管理、積分系統、任務監控、AI 模型配置

## 許可證

MIT License
