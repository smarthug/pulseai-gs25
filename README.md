# 🏪 PulseAI for GS25

> **미니 PC + OpenClaw** 기반 편의점 AI 솔루션

[![OpenClaw](https://img.shields.io/badge/Powered%20by-OpenClaw-blue)](https://openclaw.ai)

## 🎯 Overview

GS25 편의점에 설치하는 **PulseAI Box** (미니 PC):
- **🔧 예측 유지보수** - POS/주변장치 고장 2시간 전 경고
- **📦 스마트 발주** - AI 수요예측 기반 자동 제안  
- **🤖 AI 알바** - 24시간 운영 지원

## 📦 Product

**PulseAI Box = 미니 PC + OpenClaw + PulseAI Engine**

| 항목 | 사양 |
|------|------|
| CPU | Intel N100 |
| RAM | 8GB |
| Storage | 256GB SSD |
| OS | Ubuntu + OpenClaw |
| 가격 | 290,000원 |

## 🏗️ Architecture

```
┌─────────────────────────────────────────────┐
│              GS25 매장                       │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐           │
│  │ POS │ │스캐너│ │카드기│ │CCTV │           │
│  └──┬──┘ └──┬──┘ └──┬──┘ └──┬──┘           │
│     └───────┴───────┴───────┘               │
│                  │                          │
│         ┌───────▼───────┐                   │
│         │  PulseAI Box  │ ← 미니 PC         │
│         │ ┌───────────┐ │                   │
│         │ │ OpenClaw  │ │                   │
│         │ │ + ECOD    │ │                   │
│         │ │ + ARIMA   │ │                   │
│         │ └───────────┘ │                   │
│         └───────┬───────┘                   │
└─────────────────┼───────────────────────────┘
                  │
       ┌──────────┼──────────┐
       ▼          ▼          ▼
   ┌───────┐ ┌───────┐ ┌───────┐
   │카카오톡│ │텔레그램│ │웹 대시│
   └───────┘ └───────┘ └───────┘
```

## 📁 Project Structure

```
pulseai-gs25/
├── doc/                    # 문서
│   ├── PRODUCT_PLAN.md     # 기획 문서
│   ├── ARCHITECTURE.md     # 아키텍처 설계
│   └── API.md              # API 명세
├── server/                 # PulseAI 백엔드
│   └── ...
├── edge-agent/             # 매장 설치 에이전트 (C#)
│   └── ...
├── web-dashboard/          # React 대시보드
│   └── ...
└── openclaw-skills/        # OpenClaw 스킬
    └── ...
```

## 🚀 Features

### 1. 예측 유지보수
- ECOD 다변량 이상탐지
- AutoARIMA 미래예측
- 주변장치 모니터링 (스캐너, 카드리더기 등)

### 2. 스마트 발주
- 판매 데이터 기반 수요 예측
- 날씨/시즌/이벤트 반영
- 자동 발주 제안

### 3. AI 알바
- 직원 업무 지원 (택배, 유통기한 등)
- 점주 비서 (매출 리포트, 알림)
- 자연어 질의응답

## 💰 Pricing

| Plan | 월 가격 | 기능 |
|------|---------|------|
| Basic | ₩29,000 | 장비 모니터링 + 알림 |
| Standard | ₩59,000 | + 자동발주 제안 |
| Premium | ₩99,000 | + AI 알바 + 매출분석 |

## 📅 Roadmap

- [x] Phase 0: PoC (webrtc-hub-uv-sample)
- [ ] Phase 1: MVP (2개월)
- [ ] Phase 2: 핵심 기능 (3개월)
- [ ] Phase 3: 정식 출시 (6개월)

## 📄 Documentation

- [기획 문서](doc/PRODUCT_PLAN.md)

## 🤝 Team

- 호석 (Hoseok) - Founder
- richbot - AI Assistant

---

*Powered by OpenClaw 🤖*
