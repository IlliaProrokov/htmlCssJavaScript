Звісно\! Я переклав презентаційні слайди з HTML, залишивши теги, назви файлів та ключові терміни англійською мовою. Я також додав українські пояснення для всіх технічних термінів.

-----

# HTML Урок 2

## Text Formatting (Форматування Тексту) та Semantic Elements (Семантичні Елементи)

### Web Design (Вебдизайн)

Medina County Career Center

-----

## Сьогоднішні Навчальні Цілі

Наприкінці цього уроку ви зможете:

  - Правильно використовувати **heading tags** (`теги заголовків`) (**`<h1>`-`<h6>`**). *Теги заголовків використовуються для структурування вмісту та встановлення ієрархії на вебсторінці.*
  - Застосовувати **text formatting tags** (`теги форматування тексту`) (**bold, italic, emphasis**).
  - Розуміти **semantic HTML elements** (`семантичні елементи HTML`). *Семантичні елементи — це теги, які додають значення (зміст) до вмісту, а не лише його вигляд (наприклад, `<article>` замість `<div>`).*
  - Створювати розриви рядків (**`<br>`**) та горизонтальні лінії (**`<hr>`**).
  - Використовувати **special characters** (`спеціальні символи`) у HTML (**HTML entities**). *HTML entities — це коди, які використовуються для відображення зарезервованих символів (наприклад, `<` або `&`) або спеціальних символів (наприклад, `©`).*
  - Структурувати вміст за допомогою **semantic tags** (`семантичних тегів`).

-----

## Чому Text Formatting (Форматування Тексту) Важливе

**Гарне форматування тексту:**

  - Робить вміст легшим для читання.
  - Покращує **accessibility** (`доступність`) для **screen readers** (`програм зчитування з екрана`).
  - Допомагає **search engines** (`пошуковим системам`) зрозуміти ваш вміст.
  - Створює **visual hierarchy** (`візуальну ієрархію`) на сторінці.

**Пам'ятайте:** HTML описує **meaning** (`значення`), а не **appearance** (`вигляд`)\!

-----

## Heading Tags: `<h1>` to `<h6>` (Теги Заголовків: `<h1>` до `<h6>`)

HTML має шість рівнів заголовків:

```html
<h1>Main Page Title - Use Only Once</h1>
<h2>Major Section Heading</h2>
<h3>Subsection Heading</h3>
<h4>Minor Heading</h4>
<h5>Smallest Heading</h5>
<h6>Tiny Heading</h6>
```

**Best Practices (Найкращі Практики):**

  - Використовуйте лише **ОДИН** **`<h1>`** на сторінці.
  - Не пропускайте рівні (не переходьте від **`<h2>`** до **`<h5>`**).
  - Використовуйте заголовки для **structure** (`структури`), а не для **sizing** (`розміру`).

-----

## Live Demo: Heading Hierarchy (Жива Демонстрація: Ієрархія Заголовків)

Створимо структуру документа:

```html
<h1>My Restaurant Website</h1>

<h2>About Us</h2>
<p>Our story...</p>

<h2>Menu</h2>

<h3>Appetizers</h3>
<p>Delicious starters...</p>

<h3>Main Courses</h3>
<p>Our signature dishes...</p>
```

-----

## Text Formatting: Bold (Форматування Тексту: Жирний)

Два способи зробити текст жирним:

```html
<!-- Use <strong> for content that is important (Використовуйте <strong> для важливого вмісту) -->
<p><strong>Warning:</strong> Do not feed the squirrels.</p> 

<!-- Use <b> only for visual boldness (Використовуйте <b> лише для візуальної жирності) -->
<p>This is a <b>product name</b> in a sentence.</p> 
```

**`<strong>`** — *Семантично позначає текст як важливий або серйозний.*
**`<b>`** — *Візуально робить текст жирним, але не додає семантичного значення.*

-----

## Text Formatting: Italic/Emphasis (Форматування Тексту: Курсив/Наголос)

Два способи зробити текст курсивним:

```html
<!-- Use <em> for emphasized text (Використовуйте <em> для наголошеного тексту) -->
<p>The solution is to <em>never</em> give up.</p>

<!-- Use <i> for visual distinction (Використовуйте <i> для візуального виділення) -->
<p>The scientific name is <i>Homo sapiens</i>.</p>
```

**`<em>`** — *Семантично позначає наголос або акцент (інтонацію).*
**`<i>`** — *Візуально робить текст курсивним, часто використовується для технічних термінів або іноземних слів.*

-----

## Line Breaks and Horizontal Rules (Розриви Рядків та Горизонтальні Лінії)

Ці теги є **self-closing** (`самозакривними`) — вони не мають кінцевого тегу.

  - **`<br>`** (**Line Break** / *Розрив рядка*): Переносить наступний вміст на новий рядок.

<!-- end list -->

```html
<p>123 Main Street<br>
Suite 100<br>
Kyiv, Ukraine</p>
```

  - **`<hr>`** (**Horizontal Rule** / *Горизонтальна лінія*): Малює горизонтальну лінію, що позначає тематичний розрив у вмісті.

<!-- end list -->

```html
<p>This is the end of the article section.</p>
<hr>
<p>Start of the comments section.</p>
```

-----

## HTML Entities (HTML-сутності)

Використовуються для відображення символів, які інакше були б інтерпретовані як код HTML, або для спеціальних символів.

| Entity | Output | Description (Опис) |
|:---|:---|:---|
| `&lt;` | \< | Less than (Менше ніж) |
| `&gt;` | \> | Greater than (Більше ніж) |
| `&amp;` | & | Ampersand (Амперсанд) |
| `&nbsp;` | *Space* | Non-breaking space (Нервучий пробіл) |
| `&copy;` | © | Copyright sign (Знак авторського права) |
| `&trade;` | ™ | Trademark sign (Знак торгової марки) |
| `&euro;` | € | Euro sign (Знак євро) |

```html
<p>To write a paragraph tag, you must use &lt;p&gt; and &lt;/p&gt;.</p>
<p>&copy; 2024 My Website &mdash; All rights reserved.</p>
```

-----

## Quick Review: Text Formatting (Швидкий Огляд: Форматування Тексту)

| Tag | Purpose (Призначення) | Example (Приклад) |
|:---|:---|:---|
| **`<strong>`** | Important text (Важливий текст) | `<strong>Required!</strong>` |
| **`<em>`** | Emphasized text (Текст із наголосом) | `<em>Please note</em>` |
| **`<mark>`** | Highlighted (Виділений) | `<mark>Key term</mark>` |
| **`<sub>`** | Subscript (Підрядковий індекс) | `H<sub>2</sub>O` |
| **`<sup>`** | Superscript (Надрядковий індекс) | `E=mc<sup>2</sup>` |
| **`<del>`** | Deleted (Видалений) | `<del>$20</del>` |
| **`<ins>`** | Inserted (Вставлений) | `<ins>$15</ins>` |

-----

## Quick Review: Semantic Elements (Швидкий Огляд: Семантичні Елементи)

**Семантичні елементи** допомагають **screen readers** та **search engines** зрозуміти структуру та призначення частин вашої сторінки, значно покращуючи **accessibility**.

| Element (Елемент) | Purpose (Призначення) |
|:---|:---|
| **`<header>`** | Page or section header (Заголовок сторінки або розділу) |
| **`<nav>`** | Navigation links (Навігаційні посилання) |
| **`<main>`** | Main content (Основний вміст, один на сторінку) |
| **`<article>`** | Self-contained content (Автономний вміст, наприклад, запис у блозі) |
| **`<section>`** | Thematic grouping (Тематичне групування вмісту) |
| **`<aside>`** | Sidebar content (Вміст бічної панелі, пов'язаний з основним вмістом) |
| **`<footer>`** | Page or section footer (Нижній колонтитул сторінки або розділу) |

-----

## Today's Tasks (Сьогоднішні Завдання)

Ви створите два HTML-файли:

1.  **Recipe Page** (**`recipe.html`**) - Використання тегів форматування тексту.
2.  **Blog Post** (**`blog.html`**) - Використання семантичної структури HTML.

**Requirements (Вимоги):**

  - Правильна структура **HTML5**.
  - **Semantic elements** (`Семантичні елементи`) там, де це доречно.
  - **Text formatting tags** (`Теги форматування тексту`).
  - **HTML entities** (`HTML-сутності`).
  - Добре прокоментований **code** (`код`).

-----

## Questions? (Запитання?)

Перш ніж ми почнемо завдання, чи є запитання щодо:

  - Ієрархії заголовків?
  - Тегів форматування тексту?
  - HTML-сутностей?
  - Семантичних елементів?

-----

## Let's Code\! (Почнемо Кодувати\!)

Відкрийте **VS Code** (Visual Studio Code, *популярний редактор коду*) і почнемо...

-----

Чи хочете ви, щоб я почав генерувати перший файл завдання, **`recipe.html`**, чи, можливо, у вас є запитання щодо використання якогось із цих тегів?