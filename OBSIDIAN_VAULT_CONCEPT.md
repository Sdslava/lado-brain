# КОНЦЕПЦИЯ НОВОГО OBSIDIAN VAULT — LADO EMPIRE 2.0

## Проблема текущей структуры (Kerry/Paul)

После изучения существующего Obsidian vault выявлены критические проблемы:

1. **Смешение источников**: Логи Kerry, проектные файлы и ресурсы в одной куче — невозможно понять, чья это мысль
2. **Нет атрибуции**: Не ясно, где идея Славы, а где — агента
3. **Пересечение проектов**: Kazantip и LadoDesign используют разные логики, но файлы смешаны
4. **Нет версионирования**: История изменений теряется
5. **Конфликты синхронизации**: rclone может перезаписать изменения

---

## НОВАЯ СТРУКТУРА (разграниченная)

```
LADO_BRAIN_2.0/
│
├── 00_META/
│   ├── README.md                 # Общее описание структуры
│   ├── CHANGELOG.md              # История изменений структуры
│   └── DATA_POLICY.md            # Правила атрибуции и разграничения
│
├── 10_SLAVA/                     # 💡 МЫСЛИ И ИДЕИ СЛАВЫ (только Слава)
│   ├── IDEAS_RAW/                # Сырые идеи (голосовые, заметки)
│   ├── DECISIONS/                # Принятые решения (датированные)
│   ├── VISION_2026/              # Видение на год
│   └── DAILY_REFLECTIONS/        # Ежедневные размышления
│
├── 20_AGENTS/                    # 🤖 ДАННЫЕ АГЕНТОВ (по агентам)
│   ├── JIM/                      # Jim — storytelling, marketing
│   │   ├── LOGS/                 # Ежедневные логи
│   │   ├── OUTPUTS/              # Готовые материалы
│   │   └── MEMORY.md             # Долгосрочная память Jim
│   │
│   ├── KERRY/                    # Kerry — tech, visual
│   │   ├── LOGS/
│   │   ├── OUTPUTS/
│   │   ├── CODE/                 # Код и скрипты
│   │   └── MEMORY.md
│   │
│   ├── PAUL/                     # Paul — аналитика
│   │   ├── LOGS/
│   │   ├── OUTPUTS/
│   │   └── MEMORY.md
│   │
│   └── KIMICLAW/                 # KimiClaw — стратегия (я)
│       ├── LOGS/
│       ├── OUTPUTS/
│       ├── ANALYSIS/             # Критический анализ и сценарии
│       └── MEMORY.md
│
├── 30_PROJECTS/                  # 📁 ПРОЕКТЫ (по проектам)
│   ├── LADOPREMIUM/
│   │   ├── STATUS.md             # Текущий статус
│   │   ├── OBJECTS/
│   │   │   ├── KISLOVODSK_SERGEY_MARIA/
│   │   │   ├── PYATIGORSK/
│   │   │   └── ZHELEZNOVODSK/
│   │   ├── TEAM/
│   │   ├── FINANCE/
│   │   └── DOCUMENTS/
│   │
│   ├── MYCIYQUEST/
│   │   ├── STATUS.md
│   │   ├── ROADMAP.md
│   │   ├── TASKS/
│   │   ├── CODE/
│   │   └── TEAM/
│   │
│   ├── LADODESIGN/
│   │   ├── STATUS.md
│   │   ├── CONCEPTS/
│   │   ├── STANDARDS/
│   │   ├── CONFIGURATORS/
│   │   └── CATALOGS/
│   │
│   ├── KAZANTIP/
│   │   ├── STATUS.md
│   │   ├── SIGNAL/
│   │   ├── DREEMZ/
│   │   ├── TECH/
│   │   └── MARKETING/
│   │
│   ├── LADOCAFE/
│   ├── HEYEYE/
│   ├── TRIPY/
│   └── LADOARCHITECTS/
│
├── 40_KNOWLEDGE/                 # 📚 БАЗА ЗНАНИЙ (общая)
│   ├── STANDARDS/
│   │   ├── VISUAL/
│   │   ├── TECH/
│   │   └── BRAND/
│   ├── SOPs/                     # Стандартные процедуры
│   ├── RESEARCH/                 # Исследования
│   └── TROUBLESHOOTING/          # Решение проблем
│
├── 50_RESOURCES/                 # 🔧 РЕСУРСЫ
│   ├── TOOLS/
│   ├── API_KEYS/
│   ├── CONTACTS/
│   └── LINKS/
│
├── 60_ARCHIVE/                   # 📦 АРХИВ
│   ├── 2026_Q1/
│   ├── 2026_Q2/
│   └── COMPLETED_PROJECTS/
│
└── 90_SYNC/
    ├── rclone_config.md
    ├── sync_log.md
    └── CONFLICT_RESOLUTION.md
```

---

## ПРАВИЛА АТРИБУЦИИ

### Каждая заметка ДОЛЖНА содержать в начале:

```yaml
---
author: [SLAVA | JIM | KERRY | PAUL | KIMICLAW | MULTI]
date: YYYY-MM-DD
project: [PROJECT_NAME | META]
type: [IDEA | DECISION | LOG | OUTPUT | ANALYSIS]
status: [DRAFT | REVIEW | APPROVED | ARCHIVED]
source: [ORIGIN_DESCRIPTION]
---
```

### Примеры:

**Идея Славы:**
```yaml
---
author: SLAVA
date: 2026-04-22
project: KAZANTIP
type: IDEA
status: DRAFT
source: "Голосовое сообщение в Telegram"
---
```

**Анализ KimiClaw:**
```yaml
---
author: KIMICLAW
date: 2026-04-22
project: LADOPREMIUM
type: ANALYSIS
status: REVIEW
source: "Критический анализ предложения Славы"
---
```

**Вывод Kerry:**
```yaml
---
author: KERRY
date: 2026-04-22
project: MYCIYQUEST
type: OUTPUT
status: APPROVED
source: "Генерация кода по ТЗ Славы"
---
```

---

## ПРОТОКОЛ РАБОТЫ

### 1. Слава высказывает идею
- Записывается в `10_SLAVA/IDEAS_RAW/YYYY-MM-DD_idea_title.md`
- Автоматически: `author: SLAVA`, `type: IDEA`

### 2. KimiClaw анализирует
- Читает идею из `10_SLAVA/`
- Создает анализ в `20_AGENTS/KIMICLAW/ANALYSIS/YYYY-MM-DD_analysis_title.md`
- Автоматически: `author: KIMICLAW`, `type: ANALYSIS`
- Ссылается на оригинал: `[[10_SLAVA/IDEAS_RAW/YYYY-MM-DD_idea_title|Исходная идея]]`

### 3. Генерация сценариев
- KimiClaw создает `20_AGENTS/KIMICLAW/ANALYSIS/YYYY-MM-DD_10_scenarios.md`
- Каждый сценарий — отдельный блок с оценкой

### 4. Выбор лучшего сценария
- Слава подтверждает (или предлагает правки)
- Решение записывается в `10_SLAVA/DECISIONS/YYYY-MM-DD_decision.md`
- Автоматически: `author: SLAVA`, `type: DECISION`

### 5. Декомпозиция
- KimiClaw создает задачи в `30_PROJECTS/[PROJECT]/TASKS/`
- Каждая задача — отдельный файл с:
  - `author: KIMICLAW`
  - `type: TASK`
  - `status: PENDING`
  - `assignee: [JIM | KERRY | PAUL | KIMICLAW]`

### 6. Ежедневный чек-ин
- KimiClaw генерирует `30_PROJECTS/[PROJECT]/STATUS.md`
- Слава подтверждает или корректирует

### 7. Исполнение
- Агент берет задачу, выполняет
- Результат в `20_AGENTS/[AGENT]/OUTPUTS/`
- Обновление статуса в `30_PROJECTS/[PROJECT]/TASKS/`

---

## РАЗГРАНИЧЕНИЕ ПРОЕКТОВ

### LadoPremium vs LadoDesign
| Критерий | LadoPremium | LadoDesign |
|----------|-------------|------------|
| Суть | Строительство под ключ | Дизайн интерьеров |
| Клиент | Инвестор, владелец | ЖК, девелопер |
| Логика | Проект → Смета → Стройка | Стандарт → Конфигуратор |
| Команда | Прорабы, инженеры | Дизайнеры, архитекторы |
| Данные | Объекты, сметы, Teamly | Конфигураторы, каталоги |

### Kazantip vs Dreemz
| Критерий | Kazantip | Dreemz |
|----------|----------|--------|
| Суть | Фестиваль | Платформа |
| Фаза | Signal (приглашения) | Public (массовая) |
| Стиль | Glitch + Ethereal | Clean + Minimal |
| Технологии | Three.js + Shaders | React + API |

---

## СИНХРОНИЗАЦИЯ

### Метод: Git (рекомендуется)
```bash
# Инициализация
cd ~/LADO_BRAIN_2.0
git init
git add .
git commit -m "Initial vault structure"

# Ежедневный backup
git add .
git commit -m "$(date +%Y-%m-%d) daily sync"
git push origin main
```

### Альтернатива: rclone (как сейчас)
```bash
# Kerry запускает каждый час
rclone sync ~/LADO_BRAIN_2.0 yandex:Lado_Brain_2.0 --backup-dir=yandex:Lado_Brain_2.0_archive/$(date +%Y%m%d)
```

### Конфликт-резолюция
1. Git merge с разрешением конфликтов
2. Time-stamped append (если rclone)
3. Никаких перезаписей без подтверждения

---

## РЕКОМЕНДАЦИИ ПО МИГРАЦИИ

### Этап 1: Создание структуры (1 день)
- [ ] Создать директории
- [ ] Настроить шаблоны frontmatter
- [ ] Создать README и DATA_POLICY

### Этап 2: Миграция существующих данных (3 дня)
- [ ] Разобрать `obsidian_vault/01_Projects/` по проектам
- [ ] Разобрать `obsidian_vault/05_Agents_Logs/` по агентам
- [ ] Добавить frontmatter ко всем файлам
- [ ] Архивировать дубли

### Этап 3: Настройка синхронизации (1 день)
- [ ] Настроить git или rclone
- [ ] Проверить конфликты
- [ ] Обучить агентов новой структуре

### Этап 4: Тестирование (2 дня)
- [ ] Создать тестовую задачу
- [ ] Прогнать полный цикл
- [ ] Исправить ошибки

---

## ПРЕИМУЩЕСТВА НОВОЙ СТРУКТУРЫ

1. **Ясность**: Сразу видно, чья мысль и к какому проекту
2. **Отслеживание**: Git history показывает, кто что менял
3. **Масштабирование**: Новый агент = новая папка в `20_AGENTS/`
4. **Безопасность**: Нельзя случайно перезаписать чужие данные
5. **Аналитика**: Можно посчитать вклад каждого агента
6. **Контекст**: Каждый проект изолирован, нет пересечений

---

*Подготовлено: KimiClaw*
*Дата: 2026-04-22*
*Статус: Предложение для обсуждения*
