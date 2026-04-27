# LocalAI Studio

ユーザークライアント、管理バックエンド、クラウドサービス、ローカルAI処理の4つのサブプロジェクトを含む完全なAIコンテンツ生成プラットフォームです。

## 言語選択

[English](../README.md) | [简体中文](./README_zh-CN.md) | [繁體中文](./README_zh-TW.md) | 日本語 | [한국어](./README_ko-KR.md)

## プロジェクト概要

LocalAI Studio は、テキストから画像生成、テキストから動画生成などの機能をサポートする最新のAIコンテンツ作成プラットフォームです。分散型アーキテクチャを採用し、ローカルコンピューティングリソースを使用してAI処理を行うため、コストを節約しながらプライバシーを保護できます。

## サブプロジェクト一覧

| 番号 | サブプロジェクト名 | 技術スタック | 主な機能 | GitHub アドレス |
|------|------------------|-------------|---------|---------------|
| 1 | user-web-clint | React 18.2 + TypeScript 5.5 + Vite 5.0 + Ant Design 5.10 + Tailwind CSS 3.4 | ユーザークライアント、AI画像/動画生成、作品管理、素材ライブラリ、ポイントシステムなどの機能を提供 | [php-chen/LocalAI-Studio--user-web-clint](https://github.com/php-chen/LocalAI-Studio--user-web-clint) |
| 2 | user-admin-server-clint | React 19 + TypeScript + Vite + Ant Design 6 + Tailwind CSS | 管理バックエンド、ユーザー管理、作品管理、ポイント管理、タスク管理、AIモデル設定などの機能を提供 | [php-chen/LocalAI-Studio--user-admin-server-clint](https://github.com/php-chen/LocalAI-Studio--user-admin-server-clint) |
| 3 | cloud-sever-clint-python | Flask + SQLite + JWT | クラウドサービス、エンタープライズレベルのセキュリティ認証、タスクキュー、分散型AI処理スケジューリングなどのコアバックエンドサービスを提供 | [php-chen/LocalAI-Studio--cloud-sever-clint-python](https://github.com/php-chen/LocalAI-Studio--cloud-sever-clint-python) |
| 4 | local-AI-server-clint-python | Flask + ComfyUI | ローカルAIサービス、ComfyUIリモートコントロールAPI、ワークフロー管理、タスクキュー、状態監視などの機能を提供 | [php-chen/LocalAI-Studio--local-AI-server-clint-python](https://github.com/php-chen/LocalAI-Studio--local-AI-server-clint-python) |

## システムアーキテクチャ

```
┌─────────────────────────────────────────────────────────────────────┐
│                         LocalAI Studio アーキテクチャ                │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌─────────────────┐         ┌─────────────────┐                     │
│  │  user-web-clint │◄───────►│ cloud-sever-    │                     │
│  │  (ユーザークライアント)   │ clint-python    │                     │
│  └─────────────────┘         │   (クラウドサービス) │               │
│  ┌─────────────────┐         └────────┬────────┘                     │
│  │ user-admin-     │◄─────────────────┘                              │
│  │ server-clint    │                                                  │
│  │  (管理バックエンド)  │                                              │
│  └─────────────────┘         ┌─────────────────┐                     │
│                              │ local-AI-server-│                     │
│                              │ clint-python    │                     │
│                              │ (ローカルAIサービス) │◄───────────────────┐│
│                              └─────────────────┘                    ││
│                                                                      ││
│                              ┌─────────────────┐                    ││
│                              │     ComfyUI     │◄───────────────────┘│
│                              │   (AI エンジン) │                     │
│                              └─────────────────┘                     │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

## コア機能

- 🔐 エンタープライズレベルのセキュリティ：RSA-OAEP パスワード暗号化、JWT デュアルトークン認証、SHA-256 パスワードハッシュ
- 🤖 AI モデル統合：テキストから画像、画像から画像、テキストから動画、画像から動画などの多様なモデルをサポート
- 🚀 分散処理：ローカルコンピューティングリソースを活用し、クラウドコストを削減し、データプライバシーを保護
- 📊 完全な管理：ユーザー管理、作品管理、ポイントシステム、タスク監視、AIモデル設定

## ライセンス

MIT License
