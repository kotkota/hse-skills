← # HSE University English Style Guide & Editorial Rules

All English-language texts, web pages, promotional materials, and interfaces must adhere to standard British English conventions and the official requirements of the **HSE University Style Guide**:
- RU reference: [hse.ru/thesaurus/style](https://www.hse.ru/thesaurus/style)
- EN reference: [hse.ru/en/thesaurus/style](https://www.hse.ru/en/thesaurus/style/)

---

## 1. British English Standard

The HSE portal uses **British English (UK spelling)** as the university standard.

### Key British Spelling Rules:
- **`programme`**, not `program`.
  *Exception:* use `program` (both noun and verb) strictly in computing, software, and IT contexts.
- **`centre`**, not `center`.
- **`honour`**, not `honor` (and all words ending in `-our`: `behaviour`, `labour`, `favour`).
- **`-ise` and `-isation`** in verbs and nouns: `organise`, `realise`, `recognise`, `capitalise`, `organisation`, `realisation`.
- **Proper names exception**: American spelling is retained in official proper names (e.g., *World Trade Organization*, *Centers for Disease Control and Prevention*).
- **Abbreviations without periods (dots)**: write `vs`, `etc`, `eg`, `ie`, `PhD`, `Dr`, `Mr`, `Ms`, `St` (*St Petersburg*).

---

## 2. Quotation Marks & Direct Speech

### 2.1. Quotation Marks Hierarchy
- **Primary quotation marks**: single quotes (`‘` and `’`).
- **Nested quotation marks**: double quotes (`“` and `”`) inside single quotes.
  - *Example:* `‘It probably also affects them somehow. Then they ask, “Can I bring my girlfriend and friends to show them the school where I study?”’`
- ❌ **Strict Ban**: Never use Russian angle quotes (`«...»` or `„...“`) in English-language text.

### 2.2. Punctuation with Quotes
- All punctuation marks (periods, commas, question marks, exclamation marks) go **inside** the quotation marks, **except** colons, dashes, and semicolons.

### 2.3. Direct Speech Formatting
- **Do not use em-dashes** to introduce direct speech or dialogue. Use a comma, question mark, or exclamation mark instead.
  - *Example:* `‘We are looking forward to seeing many of you in our academic teams,’ said Nikita Anisimov, HSE University President. ‘Their doors are open to you.’`

---

## 3. Hyphens and Dashes

| Punctuation Mark | Character | Rule | Examples |
| :--- | :---: | :--- | :--- |
| **Hyphen** | `-` | Compound words. **No hyphen** after adverbs ending in `-ly`. | `well-read`, `state-of-the-art`<br>*No hyphen:* `internationally recognised` |
| **Short dash (En-dash)** | `–` | Time, year, and numerical intervals. **No spaces around en-dash**. | `1920–29`, `2025–2026`, `pages 15–20` |
| **Long dash (Em-dash)** | `—` | Used within sentences to set off or emphasize information. **No spaces around em-dash**. | `The first two projects took several years to get results—they were long and complicated.` |

> [!NOTE]
> **Interview exception**: When an em-dash is used as a dialogue speaker marker in transcriptions/interviews, it is separated by a space (`— `).

### 3.1. HSE Campus Names
Campus names use an **en-dash with no spaces**:
- `HSE University–St Petersburg`
- `HSE University–Nizhny Novgorod`
- `HSE University–Moscow`
- `HSE University–Perm`

### 3.2. Digital & Technical Terms
- Write in lowercase without spaces or hyphens: `webpage`, `website`, `internet`, `email`.
- Words beginning with the prefix `e` indicating "electronic" are written without a hyphen: `ecommerce`, `eSports`, `eLearning`.

---

## 4. University, Department, and Position Naming

### 4.1. University Name
- **International Name**: **`HSE University`**.
  - This single term translates all Russian variants: *НИУ ВШЭ*, *ВШЭ*, *Высшая школа экономики*, *Вышка*.
- **Legal Name**: `National Research University Higher School of Economics` is reserved **strictly** for official legal contracts, treaties, and formal agreements. All public portal pages, landing pages, news, and promotional materials must use `HSE University`.

### 4.2. Educational Programmes
- **Undergraduate (Бакалавриат)**: `undergraduate programme` or `Bachelor’s programme`.
- **Master’s (Магистратура)**: `Master’s programme`.
- **Doctoral (Аспирантура)**: `doctoral programme`.

### 4.3. Official Administrative & Academic Position Titles

| Russian Title | Official English Title |
| :--- | :--- |
| Ректор | **President** |
| Президент | **Honorary President** |
| Проректор | **Vice President** |
| Заместитель проректора | **Deputy Vice President** |
| Первый проректор | **Chief Vice President** |
| Директор | **Director** |
| Старший директор | **Senior Director** |
| Декан | **Dean** |
| Заведующий кафедрой | **Department Head** |
| Заведующий лабораторией | **Laboratory Head** |
| Руководитель | **Head** |
| Научный руководитель | **Academic Supervisor** |
| Главный научный сотрудник | **Chief Research Fellow** |
| Старший научный сотрудник | **Senior Research Fellow** |
| Научный сотрудник | **Research Fellow** |
| Младший научный сотрудник | **Junior Research Fellow** |
| Лаборант | **Laboratory Assistant** |
| Профессор | **Professor** |
| Доцент | **Associate Professor** |
| Приглашенный профессор | **Visiting Professor** |
| Стажер-исследователь | **Research Assistant** |

### 4.4. Logos for English-Language Materials
(See full specs and previews in [`brandbook.md`](brandbook.md)):
- **Desktop headers & navigation**: `hse-logo-en_one_line-blue.svg` (light background) / `hse-logo-en_one_line-white.svg` (dark background).
- **Mobile headers & compact sidebars**: `hse-logo-en_two_lines-blue.svg` / `hse-logo-en_two_lines-white.svg`.
- **Academic seals, certificates, summer/winter schools**: `hse-logo-en_full-blue.svg` / `hse-logo-en_full-white.svg` (with `EST 1992`).
- **Favicons & app icons**: `hse-sign-blue.svg` / `hse-sign-white.svg`.

---

## 5. Dates and Times

- **Dates**:
  - `March 15, 2025` (month written out, day, comma, four-digit year).
  - If the year is omitted: `March 15`.
- **Time**:
  - **12-hour format**: `8:30 am`, `1 pm`, `6:15 pm`.
  - `am` and `pm` are always lowercase and separated from the number by a space.

---

## 6. CSS Layout & Typography Wrap Guidelines

- `text-wrap: balance` — balanced wrapping on headlines (`<h1>`–`<h4>`) and short leads. Do not use on long body paragraphs.
- `text-wrap: pretty` — eliminates typographic orphans on the last line of body copy.
- `overflow-wrap: break-word` — ensures long URLs, email addresses, or identifiers do not break outside card containers.
- `white-space: nowrap` — badges, numerical labels, and date chips where line breaks are forbidden.
- Always align interface text to `text-align: start`. Avoid justified text (`justify`).

---

## 7. Imagery & Accessibility (a11y)

- All images must include a descriptive, meaningful `alt` attribute in English.
- Strictly adhere to ethical standards: no offensive, violent, or unverified imagery.
- University buildings and facilities depicted must accurately represent genuine HSE University campuses.
