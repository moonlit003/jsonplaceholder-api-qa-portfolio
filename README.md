# QA Portfolio: Тестирование REST API (JSONPlaceholder)

Пет-проект по тестированию REST API публичного сервиса [JSONPlaceholder](https://jsonplaceholder.typicode.com/). Коллекция запросов и автопроверок собрана в **Bruno**, экспортирована в формат **Postman Collection v2.1** и дополнена тестовой документацией.

## Структура проекта

```text
jsonplaceholder-api-qa-portfolio/
├── collection/
│   └── jsonplaceholder-api-qa-portfolio.json   # Коллекция запросов и JS-тестов (Postman v2.1)
├── docs/
│   ├── checklist.md                            # Чек-лист проверок
│   ├── test-cases.md                           # Тест-кейсы
│   └── bug-reports.md                          # Найденные баги и несоответствия API
└── README.md
```

## Инструменты
* **Bruno / Postman** — составление запросов, работа с переменными (`{{baseUrl}}`, `:id`, `postId`) и написание автопроверок на JavaScript.
* **Markdown** — ведение тестовой документации.
* **Git / GitHub** — контроль версий.

## Что протестировано
В коллекции **8 запросов** по эндпоинтам `/posts` и `/comments`:
* **CRUD-операции:** `GET`, `POST`, `PUT`, `PATCH`, `DELETE` для ресурса `/posts`.
* **Фильтрация:** выборка комментариев по параметру `?postId=1`.
* **Негативные и граничные проверки:** запрос несуществующего ID (`404 Not Found`), граничные значения ID, проверка валидации при отправке пустого тела `{}` и обновлении несуществующей записи (`500 Internal Server Error`).
* **Автопроверки (Tests):** валидация HTTP статус-кодов, структуры JSON и типов данных.

## Как запустить

**В Postman:**
1. Скачайте файл `collection/jsonplaceholder-api-qa-portfolio.json`.
2. Нажмите **Import** в Postman и выберите скачанный файл.
3. Откройте меню коллекции (`...`) $\rightarrow$ **Run collection**.

**В Bruno:**
1. Нажмите **Import Collection** $\rightarrow$ **Postman Collection**.
2. Выберите файл `collection/jsonplaceholder-api-qa-portfolio.json` и запустите прогон через **Run**.
