# Research Brief: Idea to Pilot Kit

Дата: 2026-07-12
Slug: idea-to-pilot-kit
Связанная карточка: [../../ideas/2026-07-12-idea-to-pilot-kit.md](../../ideas/2026-07-12-idea-to-pilot-kit.md)

## Цель Research

Понять, стоит ли развивать `idea-to-pilot-kit` как командный `skills-only` плагин для Codex / ChatGPT Work, который упаковывает повторяемые workflow Alpha Ideas: intake идеи, research sprint и project handoff.

Отдельная цель: зафиксировать границы MVP так, чтобы personal marketplace не стал целевым каналом, а публичная публикация не считалась уже принятым решением.

## Гипотезы

- `skills-only` MVP даст командную пользу быстрее, чем MCP/app-first.
- Repo/team marketplace — правильный первый канал распространения для Alpha Ideas.
- Personal marketplace нужен только как dev-smoke перед командной установкой.
- Плагин должен использовать локализацию окружения и не хранить персональные пути в публичных workflow.
- Публичная публикация оправдана только после подтвержденного командного использования.

## Вопросы

- Какой контур считать первым пользователем: Alpha Ideas, департаментская команда или учебная песочница?
- Какие 2-3 workflow входят в `0.1.0`?
- Нужен ли отдельный `localization`-skill в MVP?
- На каком языке делать первый bundle: английский manifest и skill names, русские инструкции, смешанный вариант?
- Какие критерии покажут, что плагин реально помогает: скорость intake, качество research, меньше потери контекста, проще handoff?
- Какие интеграции могут стать MCP/app-фазой позже?

## Источники

| Источник | Тип | Дата проверки | Зачем нужен |
| --- | --- | --- | --- |
| `C:\PetProjects\New-Ideas\ideas\2026-07-12-codex-plugin-product.md` | исходная карточка New Ideas | 2026-07-12 | Сохранить исходный импульс, рабочее имя и первичную оценку формата. |
| `C:\PetProjects\New-Ideas\artefacts\codex-plugin-product\README.md` | исходный индекс артефактов | 2026-07-12 | Понять, какие материалы уже были собраны в личном контуре. |
| `C:\PetProjects\New-Ideas\artefacts\codex-plugin-product\mvp-evaluation.md` | исходная оценка MVP | 2026-07-12 | Перенести team-first MVP, сценарии распространения и вопросы пользователя. |
| [Build plugins](https://developers.openai.com/codex/plugins/build) | официальная документация OpenAI | 2026-07-12 | Проверить структуру плагина, repo/personal marketplace и workspace sharing. |
| [Plugins](https://developers.openai.com/codex/plugins) | официальная документация OpenAI | 2026-07-12 | Проверить общий способ установки, использования и распространения плагинов. |
| [Submit plugins](https://learn.chatgpt.com/docs/submit-plugins) | официальная документация OpenAI | 2026-07-12 | Отделить публичную публикацию от team-first MVP и понять будущие требования submission. |

## Наблюдения

- Официальная документация описывает plugin как устанавливаемый bundle, который может включать skills, app integrations, MCP configuration, hooks и assets.
- Для минимального ручного плагина нужен manifest `.codex-plugin/plugin.json`; skills располагаются отдельно в `skills/`.
- Repo-scoped marketplace документирован как `$REPO_ROOT/.agents/plugins/marketplace.json`, personal marketplace — как `~/.agents/plugins/marketplace.json`.
- Workspace sharing внутри ChatGPT desktop app не равно публичной публикации: shared plugins остаются внутри workspace/org boundary.
- Публичная публикация идет через plugin submission portal и является отдельной поздней фазой: нужны listing materials, verified identity, test cases, availability и review.
- Входные материалы NI-Core уже предлагают правильный для Alpha Ideas уклон: `skills-only`, repo/team marketplace, personal marketplace только для dev-smoke.

## Что Подтвердилось

- Team-first канал через repo marketplace соответствует официальной модели распространения plugins.
- `skills-only` plugin — допустимый формат, в том числе для будущей публичной submission-фазы.
- Personal marketplace можно использовать как локальную техническую проверку, но для Alpha Ideas он не должен быть целевым распространением.
- MCP/app-only не нужен для первого MVP, пока нет устойчивого live action и модели доступа.

## Что Не Подтвердилось

- Не подтверждено, что публичная публикация нужна или полезна сейчас.
- Не подтвержден окончательный состав `0.1.0`: три workflow выглядят логично, но их нужно сверить с реальными задачами команды.
- Не подтверждена финальная форма manifest для `idea-to-pilot-kit`; перед scaffolding нужно прогнать актуальный `plugin-creator` / валидатор.

## Что Осталось Неизвестным

- Кто первый конкретный командный пользователь и где будет первичная установка.
- Нужен ли отдельный localization workflow внутри плагина или достаточно ссылаться на правила проекта.
- Нужно ли поддерживать несколько профилей: New Ideas, Alpha Ideas, департаментский репозиторий.
- Должен ли MVP сразу включать учебный/вебинарный сценарий.
- Какие интеграции попадут в фазу 2: GitHub, Google Drive, Slack, Teams, Notion или локальная файловая база.

## Вывод

Продолжать как командную идею Alpha Ideas. Первый MVP формулировать как `skills-only` plugin `idea-to-pilot-kit` с распространением через repo/team marketplace. Personal marketplace использовать только как dev-smoke. Публичную публикацию оставить поздней опцией после подтверждения командной ценности.

## Следующий Шаг

- Согласовать с пользователем первый контур, язык MVP и состав `0.1.0`.
- После этого подготовить prototype plugin bundle через `plugin-creator`, проверить manifest/skills локально и только затем оформить repo/team marketplace entry.
