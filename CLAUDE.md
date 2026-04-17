# adspower

Проект для работы с AdsPower Local API.

## Credentials

Ключ и URL локального API лежат в `.env` (не коммитится):

- `ADSPOWER_API_URL` — базовый URL локального API AdsPower
- `ADSPOWER_API_KEY` — API-ключ

## AdsPower Local API

Официальная документация: https://localapi-doc-en.adspower.com/

API работает только когда запущено локальное приложение AdsPower. Все запросы идут на `ADSPOWER_API_URL`, ключ передаётся как query-параметр `serial_number` или в заголовке по требованию конкретного эндпоинта.
