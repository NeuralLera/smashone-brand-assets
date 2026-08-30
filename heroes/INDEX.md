# `heroes/` — указатель героев

Одна папка на героя. Внутри: `README.md` (кто это и что можно) · `anchor/` (копия канон-анкера) ·
`scenes/SCENES.md` (пути к существующим сценам, без дублей) · `avatars/` и `video-masters/` (для Дона).

🔴 **Лица владельцев на любой поверхности — только из этого списка** (LOCKED Валерий 26.08.2026).
Дженерики из `photography/library/people-us/`, `customers/`, `owner-us-*` в роли владельцев бизнеса — **запрещены**.

Raw-база: `https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/`

⚰️ **Волна BANK-PURGE 30.08.2026 (ГО владельца через Миру):** снесены шесть линий —
`carlos-rivera` · `devon-price` · `grace` · `kayla` · `nathan` · `yamila-ortiz`.
В банке осталось **пять** папок героев: `cole` · `gerry` · `marcus-bell` · `margaret-ellison` · `mateo-salgado`.
Строки снесённых оставлены помеченными, а не удалены, — чтобы ссылка на них читалась как «мёртвая», а не как «потерянная».

| Герой | Тип | Анкер (raw-URL) | Статус | Кто рендерит |
|---|---|---|---|---|
| [`marcus-bell`](marcus-bell/README.md) — Marcus Bell | Демо-герой | [`marcus-bell-master.png`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/avatar-masters/marcus-bell-master.png) | ✅ прод-герой: фото-мастер + видео-аватар + голос приняты | Дон (видео) · Мира (статика) — фиделити-гейт лица за Мирой |
| [`mateo-salgado`](mateo-salgado/README.md) — Mateo Salgado | Демо-герой | [`17-van-start-of-day-mateo.webp`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/demobiz/casa-lista/17-van-start-of-day-mateo.webp) | ✅ прод-герой: фото-мастер + видео-аватар + голос приняты | Дон (видео) · Мира (статика) — фиделити-гейт лица за Мирой |
| [`gerry`](gerry/README.md) — Gerry (Джерри) | Рассказчик сервиса | ⛔ нет в банке | ✅ видео-аватар + голос приняты · ⛔ photo-анкера в банке нет | Дон (видео). Статика — только после снятия photo-мастера и гейта Миры |
| ⚰️ ~~`yamila-ortiz`~~ — Yamila Ortiz (Ямила Ортис) | Учебный герой | ⚰️ снесён | ⚰️ **СНЯТ 30.08.2026 волной BANK-PURGE** — линия закрыта 29.08, папки и мастера в банке больше нет | — |
| ⚰️ ~~`kayla`~~ — Kayla (Кайла, без фамилии) | Учебный герой | ⚰️ снесён | ⚰️ **СНЯТ 30.08.2026 волной BANK-PURGE** — линия заморожена 29.08, папки и мастера в банке больше нет | — |
| ⚰️ ~~`devon-price`~~ — Devon Price (Девон Прайс) | Герой ниши (фитнес) | ⚰️ снесён | ⚰️ **СНЯТ 30.08.2026 волной BANK-PURGE** — не в разрешённой тройке лиц, папки и анкера в банке больше нет | — |
| ⚰️ ~~`carlos-rivera`~~ — Carlos Rivera | Герой ниши (авто) | ⚰️ снесён | ⚰️ **СНЯТ 30.08.2026 волной BANK-PURGE** — снят с поверхностей 29.08, папки и анкера в банке больше нет | — |
| [`margaret-ellison`](margaret-ellison/README.md) — Margaret Ellison | Героиня ниши (антиквариат) | [`owner-antiques-w.webp`](https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/photography/library/owners-us/owner-antiques-w.webp) | ⏳ только анкер лица; своей сцены нет | Мира (статика) |
| ⚰️ ~~`grace`~~ — Grace (без фамилии) | Сотрудник SmashOne | ⚰️ снесён | ⚰️ **СНЯТА 30.08.2026 волной BANK-PURGE** — решение владельца 30.08 (через вопрос-очередь Миры): линия закрыта, «академии» больше нет. Папка и мастера в банке удалены | — |
| ⚰️ ~~`nathan`~~ — Nathan (без фамилии) | Сотрудник SmashOne | ⚰️ снесён | ⚰️ **СНЯТ 30.08.2026 волной BANK-PURGE** — снят с витрины 29.08, папки и мастеров в банке больше нет | — |
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
