# E-Factory Memory Repo

Назначение: канонический репозиторий проектной памяти для E-Factory / ISO Template Factory — Master Line.

## Что хранится здесь
- архитектура памяти
- активное состояние проекта
- решения и инциденты
- line-state по WEBOPS / AGENTOPS / LMOPS
- правила и навигация по памяти

## Что НЕ хранится здесь
- runtime-логи агента
- временные эксперименты
- chat transcripts
- validator evidence
- код сайта и код агента

## Базовый порядок чтения
1. `00__START_HERE.md`
2. `00__PROJECT_DNA.md`
3. `00__FAST_STATE.md`
4. `00__PROJECT_SNAPSHOT.md`
5. `00__ACTIVE_STATE.md`
6. `AI_NAVIGATION.md`

## Канонический контур
- bootstrap: `00__*`
- core: `MEMORY__*`, `KERNEL_INDEX.md`, `PROJECT_RULES.md`, `CONTRACTS.md`, `DECISIONS.md`, `CONTROL_LOOP.md`, `incidents.md`
- line files: `WEBOPS__*`, `AGENTOPS__*`, `LMOPS__*`
- dedicated agent memory fragments may exist as standalone `*_STATE_*`, `*_MEMORY_UPDATE*`, `*_RULEPACK*`, `*_BRIDGE_CARD*` files when a line needs targeted fixation

## Правило обновления
Приоритет обновлений:
1. `00__ACTIVE_STATE.md`
2. `CONTROL_LOOP.md`
3. `DECISIONS.md`
4. `incidents.md`
5. line files

## Импорт в GitHub
1. Создать пустой репозиторий `e-factory-memory`
2. Загрузить содержимое этого пакета в корень репозитория
3. Сверить README с фактической структурой пакета; не оставлять ссылок на несуществующие папки
4. Не переносить сюда runtime-логи и код из SITE/AGENT repo
