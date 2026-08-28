# Marcus Bell — `marcus-bell`

| | |
|---|---|
| **Тип** | Демо-герой |
| **Бизнес** | Tampa Pasta House — ресторан, Tampa FL (демо-бизнес в проде) |
| **Статус** | ✅ прод-герой: фото-мастер + видео-аватар + голос приняты |
| **Кто рендерит** | Дон (видео) · Мира (статика) — фиделити-гейт лица за Мирой |

## Роль в видео и на сайте

**Сайт:** туры по демо-витрине, демо-блок центральной, карточки корпканалов, демо-контексты кабинета.
**Видео:** боевой видео-аватар AI Studios — рендеры Ad001v5 / Ad003 / Ad005 / VO (серия s178).

## Анкер

🔴 **Анкер лица:** `photography/avatar-masters/marcus-bell-master.png`

Копия — `heroes/marcus-bell/anchor/marcus-bell-master.png`  
Raw: `https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/avatar-masters/marcus-bell-master.png`

**Дополнительно:**
- `photography/avatar-masters/marcus-bell-master.png`
- `photography/avatar-masters/marcus-bell-green-waist.png`

## Голос, аватары, провенанс

**Голос (LOCKED, Валерий 20.08):** «Gavin» `google/en-US/MALE_en-US-Studio-Q` — Studio-тир, тёплый/образовательный.
Смена голоса приравнена к смене лица.

**avatarId фото (AI Studios, v2 зелёный waist-up):** `6a8724e16b883ee251ee7343` — гейт Миры PASS.
**avatarId видео:** `6a8934e26186c7afb16bc765` «Marcus Bell Video».
🔴 Чистая зона видео-мастера — 0–8 с; поздние сегменты постеризованы. Перегенерация мастера = НОВЫЙ avatarId в реестр.

## Разрешено

- Демо-витрина Tampa Pasta House, демо-блок главной, карточки и коллажи корпканалов.
- Ролики серии «демо-бизнес в деле» (Дон, по одобренной Мирой раскадровке).
- На клиентских витринах — с FTC-рамкой sample-business: «Illustrative example — sample business, not a real customer».

## Запрещено

- НЕ подставлять его лицо под другую нишу или другой бизнес: один герой = одна ниша.
- НЕ генерировать сцены без identity-режима от анкера.
- НЕ выдавать за реального клиента или отзыв.

## Сцены

Перечень путей — `heroes/marcus-bell/scenes/SCENES.md` (ссылки, не копии).

## Банк видео (`D:\SmashOne-Video\`)

| Дата | Файл | Формат | Сюжет | Речь | Статус |
|---|---|---|---|---|---|
| 2026-08-28 | `bank/heroes/marcus-bell/916/marcus-bell_pass_work_evening_916.mp4` | 9:16 · 720×1280 · 10.0 s | пасс вечером: тикет → зелень в пасту → тарелка вперёд → полотенце → следующий тикет | нет; только среда | ✅ принят глазами; container `[ ok ]`; повторная дифф-проверка руки `NO ISSUES` |
| 2026-08-28 | `bank/heroes/marcus-bell/916/marcus-bell_dining_open_morning_916.mp4` | 9:16 · 720×1280 · 10.0 s | зал утром: стул на место → салфетка → стакан → проверка сервировки | нет; только среда | ✅ принят глазами по contact + high-res bodycheck; container `[ ok ]`; прибор дал false-positive по elbows/forearms — три high-res кадра подтверждают, что они внутри кадра |

## Куда что кладут

| Папка | Кто пишет | Что |
|---|---|---|
| `anchor/` | Мира | копии канон-анкеров; правится только вместе с реестром |
| `scenes/` | Мира | `SCENES.md` — перечень путей к существующим сценам |
| `avatars/` | Дон | аватары героя (photo/video), по одному файлу на версию |
| `video-masters/` | Дон | видео-мастера и боевые рендеры |

---

🔴 **Источник истины по персоне — Notion «Видеостудия SmashOne»** (`3c786d59-7e20-8082-9b87-ceff1513efc0`), затем `design/knowledge/characters-registry.md`. Этот README — витрина банка; при расхождении прав Notion.
