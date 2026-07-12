# Idea to Pilot Kit: командный плагин Codex для workflow идей

Дата создания: 2026-07-12
Статус: research
Автор: пользователь, NI-Core delegation
Куратор: не назначен
Slug: idea-to-pilot-kit
Теги: codex, chatgpt-work, plugins, skills, team-marketplace, agent-workflows, alpha-ideas
Чувствительность: internal

## Исходный импульс

Новая командная идея к проработке для Alpha Ideas: создать собственный плагин для Codex / ChatGPT Work, который упаковывает повторяемые агентские workflow команды. Идею нужно развивать как командный проект, а не личный: первый целевой контур — Alpha Ideas / департаментская команда и распространение через repo/team marketplace. Personal marketplace допустим только как dev-smoke для разработки, не как целевой канал.

Источник делегации: Codex thread `019f328e-27e9-7920-9ece-5b88dc5e8748`.

## Короткое описание

`idea-to-pilot-kit` — рабочее имя командного `skills-only` плагина для Codex / ChatGPT Work. Плагин должен упаковать повторяемый pipeline команды: принять сырую идею, обогатить ее, провести research sprint и подготовить handoff в самостоятельный проект или пилот.

Публичная публикация не считается принятым решением. Первый осмысленный канал — repo/team marketplace внутри Alpha Ideas; personal marketplace нужен только для локальной технической проверки.

## Для кого

- Департаментская команда, которая работает с потоком идей и проектных гипотез.
- Участники Alpha Ideas, которым нужен единый способ доводить идеи от intake до research и handoff.
- Агентные фасилитаторы, тимлиды и архитекторы, которые хотят переиспользовать workflow без ручного копирования правил между репозиториями.
- Учебная песочница или вебинарный контур, если команда решит показать упаковку агентских практик как продуктовый артефакт.

## Почему это может быть ценно

- Повторяемые агентские практики можно превратить в устанавливаемый bundle, а не держать их только в отдельных чатах и локальных правилах.
- Alpha Ideas может стать не только каталогом идей, но и носителем воспроизводимых agent operating procedures.
- Команда получит единый pipeline `intake -> enrichment -> research -> prioritization -> handoff`.
- Repo/team marketplace позволит версионировать workflow вместе с командным репозиторием.
- Skills-only MVP дает пользу без преждевременной разработки MCP-сервера, app UI, auth-flow, CSP и публичного listing package.

## Контекст

Идея перенесена из личного контура `NI-Core / New Ideas` в командный контур Alpha Ideas. Пользователь уточнил, что развивать ее нужно как командный проект.

Связанные исходные материалы из `New-Ideas`:

- `C:\PetProjects\New-Ideas\ideas\2026-07-12-codex-plugin-product.md`
- `C:\PetProjects\New-Ideas\artefacts\codex-plugin-product\README.md`
- `C:\PetProjects\New-Ideas\artefacts\codex-plugin-product\mvp-evaluation.md`

Дополнительные внешние материалы из исходного чата:

- `C:/Заметки/Проекты/Департамент/РазныеВопросы/01_Вопросы/2026/2026-07-12__001__razrabotka-plagina-codex/output/требования_к_плагину_codex.md`
- `C:/Заметки/Проекты/Департамент/РазныеВопросы/01_Вопросы/2026/2026-07-12__003__publikatsiya-plagina-codex/output/процесс_публикации_плагина_codex.md`
- `C:/Заметки/Проекты/Департамент/РазныеВопросы/01_Вопросы/2026/2026-07-12__003__publikatsiya-plagina-codex/references/источники.md`

Технические сведения по разработке и публикации плагинов должны перепроверяться перед реализацией по актуальной документации OpenAI и через валидатор/flow `plugin-creator`.

## Team-First MVP

- Рабочее имя: `idea-to-pilot-kit`.
- Тип MVP: `skills-only`.
- Версия MVP: `0.1.0`.
- Первый целевой пользователь: команда Alpha Ideas / департаментская команда, работающая с потоком идей.
- Первый канал распространения: repo/team marketplace внутри Alpha Ideas.
- Personal marketplace: только dev-smoke для локальной разработки.
- Не входит в MVP: публичная публикация, production MCP server, app UI, domain verification, privacy/terms/support package.

Предлагаемые workflow для `0.1.0`:

- `idea-intake` — принять сырую идею, сохранить импульс, выделить контекст, риски, аудитории, первые вопросы и артефакты.
- `research-sprint` — подготовить план исследования: гипотезы, источники, критерии адекватности идеи, карта альтернатив/конкурентов, decision gate.
- `project-handoff` — собрать пакет выноса идеи в самостоятельный проект: README, AGENTS, memory/localization, artefacts, backlog, критерии MVP.

Черновая структура:

```text
idea-to-pilot-kit/
  .codex-plugin/
    plugin.json
  skills/
    idea-intake/
      SKILL.md
      references/
    research-sprint/
      SKILL.md
      references/
    project-handoff/
      SKILL.md
      references/
  assets/
    icon.png
  README.md
```

## Гипотезы

- Командный `skills-only` плагин быстрее даст пользу, чем MCP/app-first вариант.
- Repo/team marketplace лучше соответствует Alpha Ideas, чем personal marketplace.
- Плагин будет полезен, если workflow не привязаны к локальным путям конкретного участника и явно используют слой локализации.
- Первый набор skills должен повторять уже принятый pipeline Alpha Ideas, а не изобретать параллельный процесс.
- Публичная публикация имеет смысл только после подтверждения командного использования и generic use case.

## Риски и ограничения

- Требования к Codex/ChatGPT Work plugins могут меняться, поэтому manifest, marketplace и submission детали нельзя считать зафиксированными без свежей проверки.
- Есть риск сделать методический плагин слишком общим: без реальных командных кейсов он не будет нужен.
- Если workflow будут зависеть от локальных путей, SSH aliases или личных каталогов, командное распространение быстро сломается.
- MCP/app-фаза добавит вопросы доступа, секретов, destructive actions и поддержки внешних сервисов.
- Публичная публикация потребует отдельной зрелости: listing materials, identity, support/privacy/terms, test cases и review process.

## Что нужно узнать

- Первый командный пользователь: Alpha Ideas как GitHub-репозиторий, департаментская команда или учебная песочница?
- Делаем название, descriptions и skill names сразу на английском или пока ведем русскоязычный MVP?
- Какие 2-3 workflow действительно должны войти в `0.1.0`?
- Нужно ли включать в MVP отдельный `localization`-skill для пользовательских путей, SSH, каталогов и персональных настроек?
- Нужна ли совместимость с несколькими проектными профилями: New Ideas, Alpha Ideas, департаментский репозиторий?
- Есть ли смысл сразу готовить вебинарный сценарий вокруг плагина?
- Какие интеграции будут первыми кандидатами для MCP/app-фазы: GitHub, Google Drive, Slack, Teams, Notion, локальная файловая база?

## Связанные материалы

- Research: [../research/idea-to-pilot-kit/research.md](../research/idea-to-pilot-kit/research.md)
- Plan:
- Artefacts:

## Следующий маленький шаг

- Согласовать первый командный контур, язык MVP и состав `0.1.0`: `idea-intake`, `research-sprint`, `project-handoff` или более узкий набор. После этого можно скаффолдить локальный prototype через `plugin-creator` и проверить его в personal marketplace только как dev-smoke перед repo/team marketplace.

## Журнал статуса

| Дата | Статус | Кто | Причина |
| --- | --- | --- | --- |
| 2026-07-12 | inbox | пользователь, NI-Core delegation | Идея передана из New Ideas в Alpha Ideas как командная. |
| 2026-07-12 | research | агент | Зафиксирован team-first MVP и создан research brief для проверки scope, каналов распространения и технических требований. |
