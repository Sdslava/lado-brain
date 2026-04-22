# СВОДНАЯ ИНФОРМАЦИЯ - LADO EMPIRE

## Владелец
**Вячеслав Говоров (Слава)**
- Графический дизайнер по образованию
- Основатель LadoDesign, LadoCafe, LadoArchitects, LadoPremium
- Регион: КМВ (Кисловодск, Пятигорск, Железноводск)
- Ценности: "невозможное", честность, свобода, развитие потенциала

## Команда Агентов
- **Jim** (@lado_clawd_bot) — storytelling, UX narrative, marketing
- **Kerry** — tech implementation (Three.js/Shaders), AI generation
- **Paul** (@Paul_lado_bot) — аналитика, стратегия

## Проекты (по приоритету)

### 1. LadoPremium (Активный)
- **Объект:** Кисловодск — "Сергей и Мария" (SPA, лифт, главный дом)
- **Команда:** Екатерина (архитектор), Давид, Денис Юдин (инженер), Влада
- **Проблемы:** водоотведение (заблокировано 4+ недели), отделка SPA, колонны лифта
- **Система:** Teamly для учета, финансовый трекинг

### 2. MyCityQuest (КРИТИЧЕСКИЙ — deadline 1 мая 2026)
- AR-игра в Пятигорске
- **Команда:** Слава + Никита (@frozen_hat) + Kerry
- **Статус:** фазы 1-2 просрочены, осталось 12 дней
- **GitHub:** https://github.com/FrozenHat/MyCityQuest

### 3. LadoDesign (Реконцепция)
- Стандартизированные премиум-интерьеры для ЖК
- Стиль: Minimal Wabi-Sabi (прямые линии, тауп стены)
- Инструменты: Excel-конфигураторы смет, визуальные каталоги

### 4. Kazantip/Dreemz (Phase 1: Signal)
- **Концепция:** "Prestige Round" для избранных
- **Стиль:** Archeology + Ethereal + Glitch + Selective Color
- **Tech:** React + Three.js + GLSL Shaders
- **UX:** Landing (Countdown) → Telegram Bot → SBT Visa

### 5. Другие проекты
- **LadoCafe** — реконцепция Restaurant 312
- **Tripy** — travel planner
- **HeyEye** — AI Agency/Lab
- **LadoArchitects** — архитектурное бюро

## Ключевые наработки (технические)

### Инструменты автоматизации
- Python-скрипты для генерации изображений/видео (batch_generate, batch_veo)
- Excel-конфигураторы для смет (CALCULATOR, PRO, ULTIMATE, UNIVERSAL)
- Конструктор смет (smeta_engine_pro.py, smeta_calculator.py)
- Генератор баз данных (generate_market_db.py, build_mega_excel.py)

### Веб-разработка
- HTML прототипы лендингов (Dreemz, Kazantip, Empire Dashboard)
- React-компоненты (KAZANTIP_REACT_PROTOTYPE.jsx)
- GLSL Shader прототипы
- Web-конфигуратор (web_configurator/)

### AI/ML Pipeline
- "Nano Banana" — генерация визуальных ассетов
- batch_video_gen.py — генерация видео
- process_kazantip_photos.py — обработка фото
- quiz_logic.json — логика квизов

### Данные
- global_construction_db.json — глобальная база строительных данных
- mega_empire_db_v5.json — мега-база данных империи
- master_backlog_db.json — мастер-бэклог (280+ задач)
- LadoDesign_MEGA_DATABASE_v1.xlsx

## Инфраструктура

### Серверы
- **Paul:** 138.124.72.121:3580 (root)
- **Kerry:** 45.151.233.100:3580 (root) + VPN (8443)
- **Jim:** 5.144.181.81 (OFFLINE после apt upgrade)

### VPN
- VLESS + Reality (XTLS-Vision) через sing-box
- Сервер: Kerry (45.151.233.100:8443)

### Боты Telegram
- @Kimi_sd_bot (Kerry)
- @lado_clawd_bot (Jim)
- @Paul_lado_bot (Paul)

### Системы управления
- **Notion:** Master Backlog (280+ задач на русском)
- **Obsidian Vault:** Yandex Disk (Jim Ai/Projects/Lado_Brain_Obsidian)
- **Teamly:** финансовый трекинг
- **rclone:** синхронизация с Yandex Disk

## Визуальные стандарты

### Kazantip Signal Style
- Archeology + Ethereal + Glitch + Selective Color
- Мудборды: Classic, Luxury, Minimal, Modern Classics, Modern Minimalism

### LadoDesign
- Minimal Wabi-Sabi
- Прямые линии (без арок/кривых)
- Taupe стены, современная мебель

## Финансовые инструменты
- LadoDesign_CALCULATOR.xlsx
- LadoDesign_PRO_Calculator.xlsx
- LadoDesign_PREMIUM_Smeta.xlsx
- LadoDesign_ULTIMATE_Configurator.xlsx
- LadoDesign_UNIVERSAL_Configurator.xlsx
- LadoDesign_MASTER_EMPIRE_Configurator.xlsx

## Ключевые документы
- MASTER_LADO_EMPIRE_DOSSIER_RU.md (384KB)
- KAZANTIP_DEVELOPMENT_STRATEGY_2026.md
- LADO_EMPIRE_GROWTH_STRATEGY_2026.md
- GLOBAL_PORTAL_STRATEGY.md
- LADODESIGN_TECH_STANDARD_DEEP_V3.1.md

## Текущие проблемы
1. **MyCityQuest** — критический дедлайн (1 мая), фазы 1-2 просрочены
2. **Jim сервер** — OFFLINE, все порты закрыты после apt upgrade
3. **LadoPremium Кисловодск** — водоотведение заблокировано 4+ недели
4. **VPN** — активен, проверяется каждый heartbeat
