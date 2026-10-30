# Путеводитель: js-training-bot

Автономная инструкция: достаточно этой папки, исходников и перечисленных защищённых копий. История чатов и центральный каталог не требуются.

[Восстановление](RECOVERY.md) · [Карта файлов и зависимостей](PROJECT_MAP.json)

## Назначение

По [client/README.md](client/README.md): Learn more about IDE Support for Vue in the Vue Docs Scaling up Guide.

Обнаруженные языки: JavaScript, TypeScript, Vue SFC.

## Порядок чтения

1. Локальные AGENTS.md / CLAUDE.md и документы ниже.
2. Манифесты: версии среды, зависимости, команды.
3. Кандидаты точек входа; фактический запуск проверить по манифесту.
4. PROJECT_MAP.json: imports_local от источника к импортируемому файлу; входящие рёбра — потребители модуля.
5. RECOVERY.md: независимые данные, восстановление среды, запуск и критерии приёмки.

- [client/README.md](client/README.md)

## Манифесты

- [bot/package.json](bot/package.json)
- [client/package.json](client/package.json)

## Кандидаты точек входа

- [client/src/main.js](client/src/main.js)

## Основные файлы по локальным импортам

| Файл | Входящих импортов |
|---|---:|
| [client/src/components/ui/command/index.ts](client/src/components/ui/command/index.ts) | 5 |
| [bot/src/features/training-log/training-log.flow.js](bot/src/features/training-log/training-log.flow.js) | 2 |
| [bot/src/features/training-log/training-log.keyboard.js](bot/src/features/training-log/training-log.keyboard.js) | 2 |
| [client/src/components/ui/button/index.ts](client/src/components/ui/button/index.ts) | 2 |
| [client/src/components/ui/command/Command.vue](client/src/components/ui/command/Command.vue) | 2 |
| [client/src/components/ui/dialog/DialogOverlay.vue](client/src/components/ui/dialog/DialogOverlay.vue) | 2 |
| [client/src/App.vue](client/src/App.vue) | 1 |
| [client/src/style.css](client/src/style.css) | 1 |
| [client/src/shared/dayjs.js](client/src/shared/dayjs.js) | 1 |
| [bot/src/features/training-log/training-log.validators.js](bot/src/features/training-log/training-log.validators.js) | 1 |
| [bot/src/features/training-log/modifier.parser.js](bot/src/features/training-log/modifier.parser.js) | 1 |
| [bot/src/features/training-log/training-log.ui.js](bot/src/features/training-log/training-log.ui.js) | 1 |

## Проверки


## Чтение карты без специальных плагинов

PROJECT_MAP.json — UTF-8 JSON: nodes и edges. Пути файлов относительные. contains обозначает наличие файла; imports_local — статически распознанный импорт; declares_dependency — объявление пакета в манифесте. evidence содержит источник и, где доступно, строку. Карта не исполняет код.

Статус исходного анализа: static-scan-complete; ограничений чтения: 0. Исходный снимок: 2026-10-30T14:47:11.360Z.

После изменения кода перечитайте затронутые файлы: карта является снимком. Отсутствие ребра не доказывает отсутствие зависимости.
