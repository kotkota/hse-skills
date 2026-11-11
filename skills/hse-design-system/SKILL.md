---
name: hse-design-system
description: Проектирование и верстка новых веб-страниц, лендингов мероприятий, промо-сайтов подразделений и интерактивных компонентов для Национального исследовательского университета «Высшая школа экономики» (НИУ ВШЭ / HSE University). Обеспечивает строгое соблюдение Дизайн-системы v1.5.0, брендбука ВШЭ, русской и английской редполитики и стандартов доступности (a11y).
---

# HSE Design System & Portal Experience Skill

Этот навык обучает ИИ-ассистента создавать чистые, современные, адаптивные веб-страницы и интерфейсы, строго соответствующие визуальной идентичности НИУ ВШЭ.

---

## Когда использовать этот навык

Активируйте или применяйте данный навык, если пользователь просит:
- Сверстать новую страницу, лендинг программы, промо-раздел мероприятия или сервис для НИУ ВШЭ (Вышки, hse.ru).
- Создать компонент или блок интерфейса в фирменном стиле Высшей школы экономики.
- Проверить или адаптировать существующий HTML/CSS-код под брендбук и Дизайн-систему ВШЭ.
- Подключить официальные логотипы, шрифты или токены дизайн-системы.

---

## Архитектура ресурсов навыка

- **Токены стилей**: [`assets/styles/hse-tokens.css`](assets/styles/hse-tokens.css) — CSS Custom Properties цветов, шрифтов, отступов.
- **Шрифты**: [`assets/styles/fonts.css`](assets/styles/fonts.css) — подключение `HSE Sans` и `HSE Slab`.
- **Векторные логотипы (12 официальных вариантов в `assets/logos/`, интерактивное демо `demo.html`)**:
  - **Русскоязычные**:
    - [`assets/logos/hse-logo-ru_w_descriptor-blue.svg`](assets/logos/hse-logo-ru_w_descriptor-blue.svg) — с дескриптором (синий для светлого фона).
    - [`assets/logos/hse-logo-ru_w_descriptor-white.svg`](assets/logos/hse-logo-ru_w_descriptor-white.svg) — с дескриптором (белый для темного фона).
    - [`assets/logos/hse-logo-ru_full-blue.svg`](assets/logos/hse-logo-ru_full-blue.svg) — круглая академическая печать (синяя).
    - [`assets/logos/hse-logo-ru_full-white.svg`](assets/logos/hse-logo-ru_full-white.svg) — круглая академическая печать (белая).
  - **Англоязычные (HSE University)**:
    - [`assets/logos/hse-logo-en_one_line-blue.svg`](assets/logos/hse-logo-en_one_line-blue.svg) — в одну строку (синий).
    - [`assets/logos/hse-logo-en_one_line-white.svg`](assets/logos/hse-logo-en_one_line-white.svg) — в одну строку (белый).
    - [`assets/logos/hse-logo-en_two_lines-blue.svg`](assets/logos/hse-logo-en_two_lines-blue.svg) — в две строки (синий).
    - [`assets/logos/hse-logo-en_two_lines-white.svg`](assets/logos/hse-logo-en_two_lines-white.svg) — в две строки (белый).
    - [`assets/logos/hse-logo-en_full-blue.svg`](assets/logos/hse-logo-en_full-blue.svg) — круглая печать EST 1992 (синяя).
    - [`assets/logos/hse-logo-en_full-white.svg`](assets/logos/hse-logo-en_full-white.svg) — круглая печать EST 1992 (белая).
  - **Фирменные знаки (монограмма «В» в круге)**:
    - [`assets/logos/hse-sign-blue.svg`](assets/logos/hse-sign-blue.svg) — синий знак.
    - [`assets/logos/hse-sign-white.svg`](assets/logos/hse-sign-white.svg) — белый знак.
- **Справочники**:
  - [`references/tokens.md`](references/tokens.md) — подробные спецификации дизайн-токенов.
  - [`references/brandbook.md`](references/brandbook.md) — охранные зоны, правила использования логотипов.
  - [`references/editorial-ru.md`](references/editorial-ru.md) — русская типографика («ёлочки», длинное тире `—`, неразрывные пробелы `&nbsp;`).
  - [`references/editorial-en.md`](references/editorial-en.md) — английская редполитика (British English, одинарные ‘...’, тире, должности, даты).

---

## Правила разрешения путей к ассетам (Asset Resolution)

Чтобы агент однозначно и безошибочно находил и подключал логотипы и стили:

1. **Каноническое расположение ассетов в скилле**:
   - Логотипы: `<каталог_скилла>/assets/logos/`
   - Стили: `<каталог_скилла>/assets/styles/`
2. **Размещение в целевом проекте**:
   - При создании нового проекта или автономной страницы скопируйте папку `assets/` из состава скилла в корень проекта:
     ```bash
     cp -r <путь_к_скиллу>/assets ./assets
     ```
3. **Относительные пути в коде HTML**:
   - Все пути к стилям и логотипам рассчитываются **строго относительно расположения генерируемого HTML-файла**:
     - **Для страницы в корне проекта (`index.html`)**:
       ```html
       <link rel="stylesheet" href="assets/styles/hse-tokens.css">
       <link rel="stylesheet" href="assets/styles/fonts.css">
       <!-- Русскоязычная страница: -->
       <img src="assets/logos/hse-logo-ru_w_descriptor-blue.svg" alt="НИУ ВШЭ" class="hse-header__logo" width="280" height="44">
       <!-- Или англоязычная страница: -->
       <img src="assets/logos/hse-logo-en_one_line-blue.svg" alt="HSE University" class="hse-header__logo" width="240" height="36">
       ```
     - **Для страницы во вложенной папке (например, `events/ai-school/index.html`)**:
       ```html
       <link rel="stylesheet" href="../../assets/styles/hse-tokens.css">
       <link rel="stylesheet" href="../../assets/styles/fonts.css">
       <img src="../../assets/logos/hse-logo-ru_w_descriptor-blue.svg" alt="НИУ ВШЭ" class="hse-header__logo" width="280" height="44">
       ```
   - ❌ **Запрещено**: подставлять фиксированный путь `../../assets/...` для файлов, находящихся в корне проекта.

---

## Пошаговый алгоритм работы агента

### Шаг 1. Определение структуры и обязательное подключение стилей
- Скопировать или проверить наличие папки `assets/` в проекте.
- **Обязательное требование**: в тег `<head>` любого HTML-документа обязательно подключаются внешние файлы токенов и шрифтов:
  ```html
  <link rel="stylesheet" href="assets/styles/hse-tokens.css">
  <link rel="stylesheet" href="assets/styles/fonts.css">
  ```
  *(Standalone-верстка с инлайновыми блоками `:root` в `<style>` запрещена — единым источником правды являются внешние файлы стилей).*
- Использовать чистый семантический HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`).
- Использовать ванильный ES6 JavaScript для интерактива без сторонних фреймворков.

### Шаг 2. Разметка шапки и айдентики
- В шапке (`<header>`) обязательно разместить официальный логотип в соответствии с языком страницы и фоном:
  - **Для русскоязычной страницы (светлый фон)**:
    ```html
    <a href="https://www.hse.ru/" class="hse-header__logo-link" aria-label="НИУ ВШЭ">
      <img src="assets/logos/hse-logo-ru_w_descriptor-blue.svg" alt="НИУ ВШЭ" class="hse-header__logo" width="280" height="44">
    </a>
    ```
  - **Для англоязычной страницы (светлый фон)**:
    ```html
    <a href="https://www.hse.ru/en/" class="hse-header__logo-link" aria-label="HSE University">
      <img src="assets/logos/hse-logo-en_one_line-blue.svg" alt="HSE University" class="hse-header__logo" width="240" height="36">
    </a>
    ```
  - **На тёмно-синем/брендовом фоне шапки**: использовать белые инверсные версии (`hse-logo-ru_w_descriptor-white.svg` или `hse-logo-en_one_line-white.svg`).
  - **В промо-материалах, сертификатах и академических лендингах**: круглая печать `hse-logo-ru_full-blue.svg` / `hse-logo-en_full-blue.svg`.
  - **В мобильных барах и компактных шапках**: `hse-logo-en_two_lines-blue.svg` или гербовый знак `hse-sign-blue.svg`.
- Обеспечить охранную зону вокруг логотипа (не менее высоты литеры «В»).

### Шаг 3. Осмысленное распределение цветов и ролевая модель (@hse-design/tokens v1.5.0)
- **Строгий запрет**: никаких случайных оттенков (`#0000FF`, `#1E90FF`, `#3B82F6` и др.).
- **Принцип академической сдержанности (правило 60–30–10)**:
  - **60% — поверхности и фон**: белый фон (`#FFFFFF`), карточки и подложки (`var(--hse-color-background-gray-2)` / `#F8F9FB`, `var(--hse-color-background-gray-1)` / `#EDEFF3`).
  - **30% — контент и типографика**:
    - Заголовки (H1–H6) и абзацы на светлом фоне **всегда по умолчанию цвета основного текста** `var(--hse-color-text-primary)` (`#0F0F14`).
    - ❌ **Антипаттерн**: не красьте статические заголовки секций в синий цвет просто ради украшения. Синий цвет в вебе означает кликабельность (аффорданс ссылки). Заголовок может быть синим ТОЛЬКО если это интерактивная ссылка (например, кликабельный заголовок новости в карточке).
    - Второстепенный текст, даты, мета-информация: `var(--hse-color-text-secondary)` (`#6B7A99`).
    - Границы карточек: `var(--hse-color-border)` (`#E1E4EB`).
  - **10% — интерактив и точечные акценты**:
    - **Синий бренд-цвет — это Action Color (цвет действия)**: основные кнопки (`var(--hse-color-brand)` / `#0050CF`), ссылки в тексте, активные табы, радиобаттоны, чекбоксы, фокусные состояния.
    - **Тёмные и брендовые поверхности**: шапки сайта, hero-блоки и промо-баннеры могут иметь тёмно-синий (`var(--hse-color-brand-dark)` / `#002D6E`) или синий фон (`var(--hse-color-brand)`). В этом случае текст и заголовки внутри них становятся **инверсными белыми** (`var(--hse-color-text-inverse)` / `#FFFFFF`).
    - **Цветные карточки и плашки**: допустимы карточки с мягкой пастельной подложкой (например, `--hse-color-brand-5` `#F0F5FF` или `--hse-color-accent-green-5` `#EBF5F1`), где заголовок может быть выдержан в тон карточки (глубокий тёмно-синий или тёмно-зелёный) либо оставаться белым на контрастном тёмном фоне.
    - Акценты: Dodger `var(--hse-color-accent-dodger)` (`#27A3FF`), Red `var(--hse-color-accent-red)` (`#F0522B`), Orange `var(--hse-color-accent-orange)` (`#FA8500`), Green `var(--hse-color-accent-green)` (`#00B86E`) — используются для тегов-категорий, бейджей и статусов, но не для сплошной раскраски.

### Шаг 4. Редактура и типографика текста
Определить язык контента и строго соблюдать соответствующий справочник:

- **Для русскоязычного контента ([`references/editorial-ru.md`](references/editorial-ru.md))**:
  - Заменять все кавычки `"..."` на французские «ёлочки» `«...»` (вложенные — „лапки“ `„...“`).
  - Заменять тире в предложениях на длинное тире `—` с пробелами.
  - В числовых диапазонах использовать короткое тире `–` без пробелов (`2025–2026`).
  - Проставлять неразрывные пробелы `&nbsp;` после коротких союзов и предлогов (`в`, `на`, `с`, `к`, `из`, `по`, `о`, `от`, `и`, `а`, `но`), а также между числами и существительными (`10&nbsp;дней`, `100&nbsp;%`).
  - Название университета: «Национальный исследовательский университет «Высшая школа экономики»», «НИУ ВШЭ», «Вышка».

- **Для англоязычного контента ([`references/editorial-en.md`](references/editorial-en.md))**:
  - Британский английский (UK spelling): *programme*, *centre*, *honour*, *-ise* (*organise*, *realise*).
  - Одинарные кавычки ‘...’ как основные, двойные “...” как вложенные. Никаких «ёлочек»!
  - Длинное тире `—` без пробелов внутри предложений (`results—they were`).
  - Короткое тире `–` без пробелов в диапазонах (`1920–29`, `2025–2026`) и кампусах (`HSE University–St Petersburg`).
  - Название вуза: строго **`HSE University`** (не использовать аббревиатуру HSE без слова University в заголовках).
  - Даты: `March 15, 2025`; время: `8:30 am`, `6:15 pm`.

### Шаг 5. Адаптивность и интерактивность
- Добавить `<meta name="viewport" content="width=device-width, initial-scale=1.0">`.
- Ограничить ширину контента: `max-width: var(--hse-container-max); margin: 0 auto;`.
- Проверить читаемость на мобильных экранах (от 320px).
- Для меню-бургера, аккордеонов и табов реализовать доступный ванильный JS с атрибутами `aria-expanded` и `aria-controls`.

### Шаг 6. Валидация через скрипт
Запустить автоматический линтер для проверки верстки:
```bash
python3 scripts/check_hse_compliance.py <путь_к_файлу.html>
```
Флаг `--json` выводит результат в формате JSON (для CI/CD-пайплайнов).
Линтер проверяет: цвета не из палитры ВШЭ, посторонние шрифты, прямые кавычки, дефисы вместо тире (` - ` и числовые диапазоны), отсутствие `alt` у `<img>`, отсутствие `hse-tokens.css` и `fonts.css`.
Если скрипт находит ошибки — немедленно исправить их.
