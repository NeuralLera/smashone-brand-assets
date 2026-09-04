# `channels/youtube/corp/` — кит корп-канала YouTube `@SmashOneUS` (v1, 03.09.2026, Мира)

Наряд GA 03.09 (для Джея: верификация Google под VIDEO-5, оформление канала ставит он). Дизайн прогнан через
Claude Design (канвас «SmashOne YouTube Channel Kit»), сборка детерминированная — `SMM-Hub/design/scripts/youtube-kit/`
(`build.py` → артборды, `render.py` → PNG точного размера). 🔴 Наружу — только после «да» Валерия (O19, гейт через GA).

Raw-база: `https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/`

| Файл | sha256 | raw |
|---|---|---|
| `avatar-800.png` | `ee1cd479daa6da3a…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/avatar-800.png |
| `banner-2560x1440.png` | `fe9f352ca4537a69…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/banner-2560x1440.png |
| `thumb-template-article-bl1-1280x720.png` | `ad56f720db723ddd…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/thumb-template-article-bl1-1280x720.png |
| `thumb-template-persona-sloane-1280x720.png` | `01214c3f9328a431…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/thumb-template-persona-sloane-1280x720.png |
| `thumb-template-lesson-1280x720.png` | `ff0e37a604b81452…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/thumb-template-lesson-1280x720.png |
| `thumb-template-demo-tampa-1280x720.png` | `faaa85ef93142beb…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/thumb-template-demo-tampa-1280x720.png |
| `thumb-template-demo-casa-1280x720.png` | `597479381048b9d6…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/thumb-template-demo-casa-1280x720.png |
| `card-aiwatch-1280x720.png` | `452ff0cecdc583d7…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/card-aiwatch-1280x720.png |
| `card-aiwatch-1080x1080.png` | `48492af56614e0f6…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/card-aiwatch-1080x1080.png |
| `card-aiwatch-photo-1280x720.png` | `92e392765779d02c…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/card-aiwatch-photo-1280x720.png |
| `card-aiwatch-photo-1080x1080.png` | `bc7c1aabc90e4477…` | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/card-aiwatch-photo-1080x1080.png |
| `ABOUT.txt` | — | https://raw.githubusercontent.com/smashone-corp/smashone-brand-assets/main/channels/youtube/corp/ABOUT.txt |

## Токены (дизайн-система SmashOne)
Крем `#F7F6F2` · чернила `#1A1917` · золото `#B08930` (≤10% площади: знак, линия, плашка; текст золотом не набирается) ·
Onest 800/700 (display) · Inter 500 (служебные строки). Лица — только реестр (`knowledge/characters-registry.md`);
Слоан = референс Дона `heroes/sloane/reference/sloane-reference-v1.jpeg`.

## 1. Баннер `banner-2560x1440.png`
- Загрузка 2560×1440. Весь смысл внутри **text-safe 1235×338** (x 662–1897, y 551–889): знак 132 px + крючок Onest 800 78 px
  в две строки + золотая линия 164×4 + служебная строка Inter 500 28 px. Проверено в трёх кропах (ТВ · десктоп 2560×423 ·
  мобайл/universal 1546×423). Правый нижний угол 300×100 (зона ссылок YouTube) пуст.
- Текст дословно (паспорт канала §4): **«Hire an AI employee — before you hire a human.»** + «Set it up by talking to the AI
  you already use. Watch it work before you pay.» Адреса, handle, цен, дат и чисел ростера на баннере нет.
- Декор ТВ-краёв: два тонких золотых кольца + тёплый градиент; ничего смыслового вне universal safe.

## 2. Аватар `avatar-800.png`
- 800×800, кремовый диск `#F7F6F2` на прозрачном, золотой знак ≈64% кадра (в круге Ø700), без текста, без чёрной плашки,
  без тени/свечения (LOCKED Валерий 25.08: фавикон без чёрного квадрата). Приёмка: читается как «S с молнией» на 48×48.

## 3. Шаблоны обложек видео 1280×720 (мобильная проверка 168×94 — крючок читается)
- **A · статья** `thumb-template-article-bl1-1280x720.png` (образец BL1): знак 76 px · киккер `BLOG` (Onest 700, 30 px,
  разрядка .14em, `#6D5310`) · полный заголовок Inter 600 44 px · **крючок ≤5 слов Onest 800 158 px** · золотая линия.
  Новая статья = те же слоты: `build.py` → `thumb_article(hook, title)`.
- **B · самопрезентация** `thumb-template-persona-sloane-1280x720.png`: справа лицо героя из референса (кроп по плечи,
  объект-позиция 50% 18%, кремовый градиент слева) · киккер `MEET THE STAFF` · крючок «Meet <Name>.» Onest 800 124 px ·
  золотая плашка имя/роль (Onest 700 44 / 500 24, `#1A1917`, r=28, h=118) · чип «AI-generated presenter» (белый, золотые
  буквы) — маркировка ИИ-ведущего обязательна. Новый герой = `thumb_persona(name, role, img)` с его референсом из банка.

## 4. «О канале» — `ABOUT.txt` (вставлять дословно)
Первые 150 знаков = сообщение №1 (найм ИИ-сотрудника раньше человека). Проверено на канон: цен, дат, чисел ролей,
«MCP», «chatbot», сравнений с агентствами нет; демо-бизнесы помечены illustrative sample.

## Чего в ките нет и почему
- Фото-герой на баннере (паспорт §4 предлагал сцену с владельцем демо): требует свежей генерации сцены под 2560×1440 по
  identity-анкеру Маргарет и концепт-одобрения владельца ДО генерации (стандарт обложки §0). v1 — типографика на ДС;
  фото-вариант — отдельным прогоном после «да».

## 4. Обложки полос плейлистов (v2, 04.09.2026 — «да» владельца по канвасу)

🔴 **У плейлиста нет своего постера** — площадка показывает обложку ПЕРВОГО видео. Поэтому полосе нужен не постер,
а параметризуемый шаблон обложки. Сборка: `SMM-Hub/design/scripts/youtube-kit/build_lanes.py` → `render_lanes.py`.

| Полоса | Файл | Что параметризуется |
|---|---|---|
| Lessons | `thumb-template-lesson-1280x720.png` | номер урока · название · крючок; имена ассистентов подписью **текстом** (чужих логотипов нет) |
| Demo businesses | `thumb-template-demo-tampa-1280x720.png` · `thumb-template-demo-casa-1280x720.png` | кадр товара/результата услуги · название бизнеса на золотой плашке · плашка честности |
| Meet the staff | `thumb-template-persona-sloane-1280x720.png` (v1) | лицо героя из `heroes/<slug>/reference/` — новый герой = новый путь, не новый макет |
| SmashOne updates | `thumb-template-article-bl1-1280x720.png` (v1) | заголовок и крючок; проверено другим текстом — параметризуется |
| AI at work | `card-aiwatch-*` (см. ниже) | заголовок · суть · источник |

🔴 **Рамка кадра (LOCKED 31.08):** в кадре демо-полосы только товар, результат услуги или место оказания — людей,
лиц и рук нет. На самопрезентации персон рамка не распространяется: там лицо героя и есть предмет разговора.

### Рубрика «AI at work» — вариант A принят владельцем 04.09

**A (основа, без изображения):** `card-aiwatch-1280x720.png` · `card-aiwatch-1080x1080.png` ·
`channels/tiktok/card-aiwatch-1080x1920.png`. Ничего не иллюстрирует сверх источника и физически не может
принести псевдотекст; карточка собирается из одного текста, кадр к каждой новости не нужен.

**B (исключение — когда предметный кадр уже есть):** `card-aiwatch-photo-*` в тех же трёх кадрах.
Кадр лентой сверху, поверх него букв нет. Кадр в файлах — подстановочный (блюдо Tampa): для реальной новости
подставляется свой предметный кадр, людей в нём быть не должно.

🔴 В вертикальных форматах текст стоит **по центру свободного поля**, а не под лентой: первый прогон 9:16 оставлял
нижние две трети сторис пустыми. Знак всегда на кремовом — на тёмном кадре золото по золоту не читается.

Гейты речи на всех шаблонах: без цен, без дат, без числа ролей, без слова «MCP».
