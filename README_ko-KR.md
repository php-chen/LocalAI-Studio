# LocalAI Studio

사용자 클라이언트, 관리 백엔드, 클라우드 서비스, 로컬 AI 처리의 네 가지 하위 프로젝트를 포함하는 완전한 AI 콘텐츠 생성 플랫폼입니다.

## 언어 선택

[English](../README.md) | [简体中文](./README_zh-CN.md) | [繁體中文](./README_zh-TW.md) | [日本語](./README_ja-JP.md) | 한국어

## 프로젝트 소개

LocalAI Studio는 텍스트 이미지 생성, 텍스트 비디오 생성 등의 기능을 지원하는 최신 AI 콘텐츠 제작 플랫폼입니다. 분산 아키텍처를 채택하여 로컬 컴퓨팅 리소스를 사용해 AI 처리를 수행하므로 비용을 절약하면서 개인정보를 보호할 수 있습니다.

## 하위 프로젝트 목록

| 번호 | 하위 프로젝트명 | 기술 스택 | 주요 기능 | GitHub 주소 |
|------|--------------|----------|---------|-----------|
| 1 | user-web-clint | React 18.2 + TypeScript 5.5 + Vite 5.0 + Ant Design 5.10 + Tailwind CSS 3.4 | 사용자 클라이언트, AI 이미지/비디오 생성, 작품 관리, 소재 라이브러리, 포인트 시스템 등 기능 제공 | [php-chen/LocalAI-Studio--user-web-clint](https://github.com/php-chen/LocalAI-Studio--user-web-clint) |
| 2 | user-admin-server-clint | React 19 + TypeScript + Vite + Ant Design 6 + Tailwind CSS | 관리 백엔드, 사용자 관리, 작품 관리, 포인트 관리, 작업 관리, AI 모델 설정 등 기능 제공 | [php-chen/LocalAI-Studio--user-admin-server-clint](https://github.com/php-chen/LocalAI-Studio--user-admin-server-clint) |
| 3 | cloud-sever-clint-python | Flask + SQLite + JWT | 클라우드 서비스, 기업급 보안 인증, 작업 큐, 분산 AI 처리 스케줄링 등 핵심 백엔드 서비스 제공 | [php-chen/LocalAI-Studio--cloud-sever-clint-python](https://github.com/php-chen/LocalAI-Studio--cloud-sever-clint-python) |
| 4 | local-AI-server-clint-python | Flask + ComfyUI | 로컬 AI 서비스, ComfyUI 원격 제어 API, 워크플로우 관리, 작업 큐, 상태 모니터링 등 기능 제공 | [php-chen/LocalAI-Studio--local-AI-server-clint-python](https://github.com/php-chen/LocalAI-Studio--local-AI-server-clint-python) |

## 시스템 아키텍처

```
┌─────────────────────────────────────────────────────────────────────┐
│                         LocalAI Studio 아키텍처                      │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌─────────────────┐         ┌─────────────────┐                     │
│  │  user-web-clint │◄───────►│ cloud-sever-    │                     │
│  │  (사용자 클라이언트)     │ clint-python    │                     │
│  └─────────────────┘         │   (클라우드 서비스) │                │
│  ┌─────────────────┐         └────────┬────────┘                     │
│  │ user-admin-     │◄─────────────────┘                              │
│  │ server-clint    │                                                  │
│  │  (관리 백엔드)    │                                               │
│  └─────────────────┘         ┌─────────────────┐                     │
│                              │ local-AI-server-│                     │
│                              │ clint-python    │                     │
│                              │ (로컬 AI 서비스) │◄───────────────────┐│
│                              └─────────────────┘                    ││
│                                                                      ││
│                              ┌─────────────────┐                    ││
│                              │     ComfyUI     │◄───────────────────┘│
│                              │   (AI 엔진)     │                     │
│                              └─────────────────┘                     │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

## 핵심 기능

- 🔐 기업급 보안：RSA-OAEP 비밀번호 암호화, JWT 이중 토큰 인증, SHA-256 비밀번호 해시
- 🤖 AI 모델 통합：텍스트 → 이미지, 이미지 → 이미지, 텍스트 → 비디오, 이미지 → 비디오 등 다양한 모델 지원
- 🚀 분산 처리：로컬 컴퓨팅 리소스 활용, 클라우드 비용 절감, 데이터 개인정보 보호
- 📊 완전한 관리：사용자 관리, 작품 관리, 포인트 시스템, 작업 모니터링, AI 모델 설정

## 라이선스

MIT License
