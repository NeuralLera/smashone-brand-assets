# `logos/` — знаки бренда и демо-бизнесов

Raw-база: `https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/`

---

## 🔴 Канон — один файл

```
logos/smashone-logo/smashone-logo.svg
```

Золотой знак SmashOne (`#b08930`), theme-agnostic — один и тот же файл работает на светлом
и на тёмном фоне. Это **единственный источник логотипа**: header, hero, footer, промпты
Claude Design, презентации, обложки.

Raw: `https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/logos/smashone-logo/smashone-logo.svg`

### ⚰️ Мёртвое имя, которое до сих пор встречается в наших файлах

`logos/smashone-logo/smashone-logo-potrace.svg` — **не существует** (удалён коммитом `83d8a04`).
На него бьют сотни исторических ссылок, включая пакеты кампаний. Такой промпт приходит
в Claude Design **без логотипа**: auto-fetch получает 404 и молча рисует пустой слот.

Встретил `smashone-logo-potrace.svg` в промпте или наряде — **замени на `smashone-logo.svg`**.
Файл сюда не возвращаем: правится ссылка, а не банк.

Так же мертвы (в репозитории их нет):

| Мёртвый путь | Живая замена |
|---|---|
| `logos/smashone-logo.svg` (без подпапки) | `logos/smashone-logo/smashone-logo.svg` |
| `logos/smashone-corp/smashone-logo-potrace.svg` | `logos/smashone-corp/smashone-logo.svg` |
| `logos/smashone-tile-light/smashone-logo-potrace.svg` | `logos/smashone-logo/smashone-logo.svg` |

---

## `smashone-corp/` — копия канона под корп-сущность

```
logos/smashone-corp/smashone-logo.svg
```

Байт-в-байт тот же знак, что в `smashone-logo/`. Зеркало намеренное: корпоративные материалы
(документы, письма, аккаунты SMASHONE CORPORATION) ссылаются на свой путь. Обе копии обновляются
вместе — разошлись значит дефект.

---

## `favicon/` — фавикон-канон (LOCKED Валерий 25.08.2026)

**Золотой знак БЕЗ чёрного квадрата.** SVG — на прозрачном фоне, растр — на кремовом
круге `#F7F6F2`. Чёрная плашка под знаком = дефект, а не вариант.

Применяется на **всех** поверхностях: сайт, кабинеты, MCP, OAuth, каталоги.

| Файл | Где применяется |
|---|---|
| `favicon.svg` | основной, современные браузеры |
| `favicon-circle.svg` | вариант со знаком в круге |
| `favicon.ico` | легаси-браузеры |
| `favicon-16x16.png` · `favicon-32x32.png` · `favicon-48x48.png` | растровые размеры вкладки |
| `apple-touch-icon.png` | iOS home screen |
| `icon-192.png` · `icon-512.png` | PWA-манифест |
| `smashone-app-icon-512.png` | иконка приложения |
| `mark-512-transparent.png` | знак на прозрачном, для наложений |

---

## `avatars-corp/` — аватары корпоративных каналов

`avatar-{320,400,640,720,1024}.png` и та же линейка с суффиксом `-v2`.
Действующая — **`-v2`**; версия без суффикса оставлена как предшественник и не перезаписывается.

Ставится на аккаунты компании: Telegram `@smashone_us`, Facebook-страница, Instagram
`@smashone.app`, LinkedIn, X.

🔴 **На личные профили учредителей единый знак бренда НЕ ставится** — логотип вместо лица
читается как компания, притворяющаяся человеком. Там деловой портрет человека.

---

## `usa-emblem/` — маркер юрисдикции

`flag-us.svg` — единственная живая сущность SMASHONE CORPORATION (Florida).

⚰️ `logos/eu-emblem/flag-eu.svg` уехал в `_archive/2026-08-28/logos/eu-emblem/` — европейское
направление закрыто окончательно 22.08.2026, второй сущности нет.

---

## `demobiz/` — логотипы демо-бизнесов

Живой в проде — один:

```
logos/demobiz/tampa-pasta-house/
  avatar.png · avatar.svg            — аватар канала
  mark.png · mark.svg                — знак
  wordmark.png · wordmark.svg        — наборный логотип
  lockup-horizontal.svg              — знак + текст в строку
  lockup-vertical.svg                — знак + текст в столбец
  assistant-avatar.png · .svg        — аватар ассистента бизнеса
```

Канон аватара демо-канала = **`avatar.svg`, знак БЕЗ текста**.

Второй живой демо-бизнес **Casa Lista Home Repair** отдельной папки логотипов не имеет —
его оформление лежит целиком в `channels/demobiz/casa-lista/` (там же `avatar.png`
и обложка канала).

Учебный бизнес **Ortiz Nails & Brows** — знак в `channels/training/ortiz-nails-brows/brand/`.

### ⚰️ Ретайрнутые демо-бизнесы

| Бизнес | Где теперь | Почему |
|---|---|---|
| Evans Auto Sales | `_archive/2026-08-28/logos/demobiz/evans-auto-sales/` (кроме `avatar.png`, оставленного на месте живой ссылкой) | название мертво; лицо Carlos Rivera живо под именем **Orange Grove Auto** |
| High Cotton Antiques | `_archive/2026-08-28/logos/demobiz/high-cotton-antiques/` | название мертво; лицо Margaret Ellison живо под именем **Ellison Antiques** |
| Lumière · Maison Dorée · Atelier Nord | `_archive/2026-08-28/logos/demobiz/` | европейское направление закрыто 22.08.2026 |

Демо-бизнесы в проде = **только Tampa Pasta House + Casa Lista**.

---

## ⚰️ Deprecated: вордмарк-композиты и плиточные наборы

Убраны из репозитория, обратно не возвращаются:

| Набор | Что было | Почему снят |
|---|---|---|
| `smashone-wordmark-dark/` · `smashone-wordmark-light/` | растровые PNG «SmashOne» текстом, размеры 64…1254 | композит «знак + надпись» отвергнут Валерием (19.05.2026). Слово «SmashOne» набирается **текстом** шрифтом Onest Variable, а не картинкой — так оно масштабируется, ищется и переносится по строке |
| `smashone-tile-dark/` · `smashone-tile-light/` | плиточные фоны и фавикон-варианты по темам | фон-плитка снята из дизайн-системы 19.05.2026; фавикон переехал в `favicon/` каноном 25.08.2026 |

🔴 Одна ссылка на мёртвый вордмарк ещё жива в скиле `mira-claude-design-prompt-authoring`
(`logos/smashone-wordmark-light/smashone-wordmark-light-512.png`) — её нужно снять в скиле,
а не восстанавливать файл.

**Не путать deprecated с архивом:** архив (`_archive/`) — материал закрытых направлений,
он лежит целиком и может вернуться. Deprecated здесь — снятые **приёмы** дизайна; их файлы
удалены сознательно и восстановлению не подлежат.

---

## Чек-лист перед тем, как поставить логотип

1. Путь ровно `logos/smashone-logo/smashone-logo.svg` — не `-potrace`, не без подпапки.
2. Фавикон — из `logos/favicon/`, без чёрной плашки.
3. Аватар корпканала — `avatars-corp/avatar-<размер>-v2.png`.
4. На личном профиле человека — портрет, не знак.
5. Демо-бизнес — только Tampa или Casa; остальные названия мертвы.
6. Ссылку перед выдачей промпта проверить: `curl -sI <raw-url>` должен вернуть `200`.
