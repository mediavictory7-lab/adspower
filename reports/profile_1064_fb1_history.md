# Профиль 1064 (fb1) — анализ истории и активности

- **Serial:** 1064
- **user_id:** k18rxxs3
- **Имя:** DanteTraf 9
- **API ключ:** fb1 (`ADSPOWER_FB1_API_KEY`)
- **Дата анализа:** 2026-04-17
- **Источники:** `~/Library/Application Support/adspower_global/cwd_global/source/cache/k18rxxs3_h16exk8/Default/` (History, Cookies, Login Data, Local Storage)

## Важно: реальная история недоступна

Локальный Chrome `History` SQLite содержит **всего 10 записей, все датированы 2026-04-17 17:25** — это момент, когда профиль только что был открыт и AdsPower засеял стартовые вкладки из своего облачного cache. Визиты имеют transition core=6 (`START_PAGE`), т.е. это не реальные переходы пользователя, а инициализационные.

**Полной истории за неделю (2026-04-10 … 2026-04-17) в локальном профиле нет.** Либо она была очищена, либо AdsPower не сохраняет её локально между сессиями, а хранит только «стартовые вкладки». Чтобы получить настоящую историю, нужен доступ к облачному cache AdsPower или нужно снимать историю в течение использования профиля.

## URL из локального History (снимок при открытии)

| Время (17:25) | URL | Title |
|---|---|---|
| :35 | https://yopmail.com/wm | Inbox |
| :35 | https://www.facebook.com/ | Facebook |
| :35 | https://smit.vn/smit-connect/settings | SMIT — Thiết lập SMIT Connect |
| :35 | https://eventsmanager.facebook.com/events_manager2/list/dataset/1510086913782243/overview | Events Manager |
| :34 | https://adsmanager.facebook.com/…act=886800917684999 | Ads Manager — Campaigns |
| :34 | https://business.facebook.com/latest/leads_center?asset_id=192231753971811 | Meta Business Suite |
| :34 | https://adsmanager.facebook.com/…act=1404325997818518 | Ads Manager — Campaigns |
| :34 | https://adsmanager.facebook.com/…act=1964308337486417 | Ads Manager — Campaigns |
| :34 | https://adsmanager.facebook.com/…act=1453635922975231 | Ads Manager — Campaigns |
| :33 | https://start.adspower.net/?id=k18rxxs3 | DanteTraf 9 start page |

## Дополнительные сигналы (cookies, login, local storage)

### Сайты с реальным присутствием (не ad-tracking)
По cookies и Local Storage восстанавливаются **сайты, где профиль реально был залогинен / активно работал**:

- **facebook.com / adsmanager.facebook.com / business.facebook.com / eventsmanager.facebook.com** — основная активность
- **login.microsoftonline.com / outlook.live.com / login.live.com / www.microsoft.com** — Microsoft/Outlook аккаунт
- **google.com / chromewebstore.google.com** — Google, Chrome Web Store
- **linkedin.com**
- **yopmail.com** — одноразовая почта
- **smit.vn** — сервис SMIT Connect (виртуальные номера/SMS, VN)
- **adspower.net**

### Ad-tracking домены (фоновый шум)
56 уникальных хостов в cookies, большая часть — cookies рекламных сетей (adnxs, bidswitch, casalemedia, doubleclick, mookie1, rfihub, stackadapt, adform, adkernel, adsrvr, bidr, contextweb, creativecdn, flashtalking, quantserve, 360yield, mfadsrvr и т.д.). Эти cookies ставятся автоматически сторонними скриптами на любом посещённом сайте, где крутится реклама, — **не означают прямого визита пользователя** на эти домены.

### Сохранённые логины
- Facebook: **user id 61575027671692** (один сохранённый логин)

### Рекламные аккаунты Facebook (из URL)
Видны 4 разных ad account ID:
- `act=886800917684999`
- `act=1404325997818518`
- `act=1964308337486417`
- `act=1453635922975231`

И минимум 2 Business Manager ID:
- `business_id=8944658...`
- `business_id=1403310834085...` / `1403310...`

Asset ID в Leads Center: `192231753971811`
Pixel/Dataset ID в Events Manager: `1510086913782243`

## Анализ действий пользователя

По агрегату имени профиля (`DanteTraf 9`), набору посещённых сайтов и паттернам это **профиль медиабайера / «фермера» Facebook-рекламы**:

1. **Основная работа — Facebook Ads**: заходит в несколько ad accounts через Business Manager, работает с Events Manager (пиксель/dataset для конверсий), смотрит Leads Center (лидогенерация). Минимум 4 рекламных кабинета под одним профилем.
2. **Использует одноразовые инструменты верификации**: `yopmail` (disposable email) и `smit.vn` (SMS-верификация / виртуальные номера, сервис из Вьетнама). Классический стек для регистрации/восстановления FB-аккаунтов.
3. **Microsoft/Outlook и LinkedIn** присутствуют как backup-каналы аутентификации или рабочая почта.
4. Имя `DanteTraf` + связка с SMIT (VN) — соответствует профилю traffic/arbitrage команды из VN-экосистемы.

## Ограничения анализа

- Это снимок **состояния кэша**, а не реальная timeline за неделю.
- «Реклама за спиной» (cookies ad-сетей) не = явный визит.
- Чтобы получить фактическую недельную историю, нужно: либо попросить AdsPower сохранять полный history файл, либо снимать History после живого использования профиля, либо тянуть из их cloud backup.
