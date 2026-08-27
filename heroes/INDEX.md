# `heroes/` — указатель героев

Одна папка на героя. Внутри: `README.md` (кто это и что можно) · `anchor/` (копия канон-анкера) ·
`scenes/SCENES.md` (пути к существующим сценам, без дублей) · `avatars/` и `video-masters/` (для Дона).

🔴 **Лица владельцев на любой поверхности — только из этого списка** (LOCKED Валерий 26.08.2026).
Дженерики из `photography/library/people-us/`, `customers/`, `owner-us-*` в роли владельцев бизнеса — **запрещены**.

Raw-база: `https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/`

| Герой | Тип | Анкер (raw-URL) | Статус | Кто рендерит |
|---|---|---|---|---|
| [`marcus-bell`](marcus-bell/README.md) — Marcus Bell | Демо-герой | [`owner-restaurant-m-hero.webp`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/library/owners-us/owner-restaurant-m-hero.webp) | ✅ прод-герой: фото-мастер + видео-аватар + голос приняты | Дон (видео) · Мира (статика) — фиделити-гейт лица за Мирой |
| [`mateo-salgado`](mateo-salgado/README.md) — Mateo Salgado | Демо-герой | [`17-van-start-of-day-mateo.webp`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/demobiz/casa-lista/17-van-start-of-day-mateo.webp) | ✅ прод-герой: фото-мастер + видео-аватар + голос приняты | Дон (видео) · Мира (статика) — фиделити-гейт лица за Мирой |
| [`gerry`](gerry/README.md) — Gerry (Джерри) | Рассказчик сервиса | ⛔ нет в банке | ✅ видео-аватар + голос приняты · ⛔ photo-анкера в банке нет | Дон (видео). Статика — только после снятия photo-мастера и гейта Миры |
| [`yamila-ortiz`](yamila-ortiz/README.md) — Yamila Ortiz (Ямила Ортис) | Учебный герой | [`yamila-ortiz-master.png`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/avatar-masters/yamila-ortiz-master.png) | ✅ мастер принят Валерием 24.08 (фронтал, оба уха, нейтральный тёплый фон) | Мира (статика) · Дон (видео) — фиделити-гейт лица за Мирой |
| [`kayla`](kayla/README.md) — Kayla (Кайла, без фамилии) | Учебный герой | [`kayla-master.png`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/avatar-masters/kayla-master.png) | ⏳ мастер есть, аватар и голос не заведены | Мира (статика). Видео — после заведения аватара |
| [`devon-price`](devon-price/README.md) — Devon Price (Девон Прайс) | Герой ниши (фитнес) | [`owner-fitness-m.webp`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/library/owners-us/owner-fitness-m.webp) | ⏳ только анкер лица; своих сцен нет | Мира (статика) |
| [`carlos-rivera`](carlos-rivera/README.md) — Carlos Rivera | Герой ниши (авто) | [`owner-auto-m.webp`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/library/owners-us/owner-auto-m.webp) | ⏳ только анкер лица; своей сцены нет | Мира (статика) |
| [`margaret-ellison`](margaret-ellison/README.md) — Margaret Ellison | Героиня ниши (антиквариат) | [`owner-antiques-w.webp`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/library/owners-us/owner-antiques-w.webp) | ⏳ только анкер лица; своей сцены нет | Мира (статика) |
| [`grace`](grace/README.md) — Grace (без фамилии) | Сотрудник SmashOne (резерв) | [`grace-master.png`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/staff/grace-master.png) | ✅ мастер + зелёный waist + avatarId (гейт Миры PASS); держим в резерве | Дон (видео, академия) · Мира (статика внутренних материалов) |
| [`nathan`](nathan/README.md) — Nathan (без фамилии) | Сотрудник SmashOne | [`nathan-master.png`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/staff/nathan-master.png) | ✅ мастер снят · ⏳ avatarId и голос не заведены (кастинг за Доном) | Мира (статика витрины фабрики) · Дон (видео после кастинга) |
| [`cole`](cole/README.md) — Коль (Cole) | Маскот (иллюстрация, не фотоперсона) | [`cole-portrait.png`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/mascots/cole/cole-portrait.png) | ➖ иллюстрированный маскот — фото-аватар не применим | Мира (иллюстрация и карточки) |

## Что значит статус

| Значок | Смысл |
|---|---|
| ✅ | материал принят Валерием, герой в работе |
| ⏳ | есть анкер, но аватар / голос / сцены не заведены |
| ⛔ | пробел: нужного файла в банке нет |
| ➖ | не применимо (маскот, не фотоперсона) |

## Гейты, которые нельзя обходить

1. **Фиделити-гейт лиц — Мира.** После тест-рендера Дона живое лицо аватара сверяется с анкером; без PASS аватар в работу не идёт.
2. **avatarId живёт в реестре, не здесь.** Пересоздал аватар — новый id идёт в `characters-registry.md` и в Notion «Видеостудия», старый помечается мёртвым.
3. **Голос закреплён как лицо.** Смена голоса = тот же класс события, что смена лица.
4. **Один герой = одна ниша.** Лицо не переносится между бизнесами.
5. **FTC-рамка** на демо-витринах: «Illustrative example — sample business, not a real customer».

---

🔴 Источник истины по персонам и видеопродакшену — Notion «Видеостудия SmashOne» (`3c786d59-7e20-8082-9b87-ceff1513efc0`), затем `design/knowledge/characters-registry.md`. Ведёт Мира.
