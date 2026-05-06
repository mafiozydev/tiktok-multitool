# TikTok Multitool

Telegram-бот + Web App для анализа TikTok-видео.

**Главное преимущество:** вся тяжёлая обработка (анализ аудио, распознавание музыки, описание видео) происходит **на устройстве пользователя** (телефон/ПК), а не на серверах.

## Архитектура
- **Telegram Bot** — лёгкий, только принимает ссылку и открывает Web App
- **Telegram Mini App (Web App)** — вся логика анализа здесь (client-side)
- Модульная структура для лёгкого расширения

## Текущий функционал (планируется)
- Принять ссылку на TikTok видео
- Распознавание музыки (сначала через metadata, позже client-side fingerprinting)
- В будущем: транскрипция речи, описание видео (LLaVA.js / ONNX и т.д.)

## Структура проекта
```bash
/tiktok-multitool
├── bot/              # Лёгкий Telegram бот (Node.js / Python)
├── webapp/           # Telegram Mini App (Vite + React/TS + WebAudio)
├── shared/           # Общие типы и утилиты
├── docs/
└── README.md
```
