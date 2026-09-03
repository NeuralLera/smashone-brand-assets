# `channels/corp/` — обложки корпканалов SmashOne (ревизия 03.09.2026, Мира; наряд GA)

Один визуальный язык с YouTube-баннером (`channels/youtube/corp/`): крем `#F7F6F2`, чернила `#1A1917`, золотой знак,
крючок Onest 800 **«Hire an AI employee — before you hire a human.»** + служебная строка Inter 500
«Set it up by talking to the AI you already use. Watch it work before you pay.» Золото ≤10%. Без лиц ростера
(счётный ростер = нарушение канона), без цен, дат, «Opening», «autopilot», TikTok как товара, «MCP».
Сборка детерминированная: `SMM-Hub/design/scripts/corp-covers/` (build.py → render.py). Канвас CD: «SmashOne Corp Covers Revision».
🔴 Наружу — после «да» Валерия (O19); ставит Джей одним заходом, скрин до/после.

| Файл (v2, действующие) | sha256 | raw |
|---|---|---|
| `smashone-corp-fb-cover-1640x624.png` | `894c8291cd91258d…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/corp/smashone-corp-fb-cover-1640x624.png |
| `smashone-corp-x-header-1500x500.png` | `670bff3323b9a8f2…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/corp/smashone-corp-x-header-1500x500.png |
| `smashone-corp-linkedin-banner-4200x700.png` | `e355068a0c36185e…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/corp/smashone-corp-linkedin-banner-4200x700.png |

## Зоны (проверены в артбордах «zones»)
- **Facebook Page cover** 1640×624 (@2x 820×312): весь смысл в центральных **1280×624** (≥180 px от краёв — мобильный кроп);
  диск профиля десктопа (низ-лево ~340×340) пуст. Блок: знак 112 px · крючок 66 px две строки · линия · строка 24 px.
- **X header** 1500×500: мобильная полоса y 50–450; диск аватара десктопа (низ-лево ~400×200) пуст. Блок: знак 104 · крючок 60 · строка 22.
- **LinkedIn company banner** — загрузка 4200×700 (показ ≈1128×191, 6:1): смысл в центральных ~2600 px; зона лого низ-лево пуста.
  Блок: знак 170 · крючок 108 · строка 40. ⚠️ Страницы компании на LinkedIn на 03.09 не найдено (только профиль Дмитрия) —
  баннер лежит наготове к её заведению.

## Аватары (без изменений)
Действующий аватар всех корпканалов = золотой знак на кремовом (`logos/avatars-corp/avatar-{320,400,720,1024}.png`,
поставлены Джеем 26.08; живьём проверено 03.09 на FB и Telegram) — канон фавикона 25.08 (без чёрной плашки).

## ⚰️ Мёртвые файлы этой папки (не использовать; удаление — по списку GA)
- `smashone-corp-channel-cover-1640x624.png` — «Social media on autopilot for small business» + TikTok в ряду каналов как товар (рамка инструмента, мертва с 30.07).
- `smashone-corp-x-cover-1500x500.png` — счётная сетка из 12 лиц старого ростера (запрет счётного ростера 05.08).
- `smashone-corp-channel-avatar-US-640.png` — чёрный знак на золотом диске с флагом US (эпоха US/EU; канон аватара 25.08 — золотой знак на кремовом).
