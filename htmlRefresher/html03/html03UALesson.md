Звісно, я із задоволенням перекладу ці слайди\! Це урок про **Links and Navigation** (`Покликання та Навігація`) в HTML. Я залишу всі технічні теги та терміни англійською, додаючи українські пояснення.

-----

# HTML Урок 3

## Links (Покликання) та Navigation (Навігація)

### Web Design (Вебдизайн)

Medina County Career Center

-----

## Сьогоднішні Навчальні Цілі

Наприкінці цього уроку ви зможете:

  - Створювати **hyperlinks** (`гіперпокликання`) за допомогою **anchor tag** (`тегу якоря`).
  - Розуміти **absolute** vs. **relative URLs** (`абсолютні проти відносних URL-адрес`).
  - Створювати **links** (`покликання`) на електронну пошту.
  - Створювати **anchor links** (`покликання-якорі`) всередині сторінки.
  - Дотримуватися **link best practices** (`найкращих практик для покликань`) для зручності використання (**usability**).
  - Створювати базові **navigation menus** (`навігаційні меню`).

-----

## Тег Якоря `<a>`

Тег якоря **`<a>`** створює **clickable links** (`покликання, на які можна натискати`):

```html
<a href="destination.html">Click here</a>
```

**Три частини:**

1.  **Opening tag** (`Відкриваючий тег`) з **`href` attribute** (`атрибутом href`).
2.  **Link text** (`Текст покликання`) (що користувачі бачать і на що натискають).
3.  **Closing tag** (`Закриваючий тег`).

**`href` = "hypertext reference"** (*гіпертекстове посилання*) (куди веде покликання)

-----

## Базовий Приклад Покликання

```html
<a href="about.html">About Us</a>
```

**Що відбувається:**

  - Користувач бачить: "**About Us**"
  - Покликання є **clickable** (`клікабельним`)
  - Натискання веде до **`about.html`**

**Спробуйте:** Давайте разом створимо просте покликання\!

-----

## Absolute URLs (Абсолютні URL-адреси)

**Absolute URL** (`Абсолютна URL-адреса`) = Повна вебадреса

```html
<a href="https://www.google.com">Go to Google</a>
<a href="https://www.github.com">Visit GitHub</a>
<a href="https://www.w3schools.com">W3Schools</a>
```

**Використовуйте абсолютні URL-адреси для:**

  - **External websites** (`Зовнішніх вебсайтів`)
  - Покликань на інші **domains** (`домени`)
  - Ресурсів не на вашому **server** (`сервері`)

**Завжди включайте:** **`http://`** або **`https://`**

-----

## Relative URLs (Відносні URL-адреси)

**Relative URL** (`Відносна URL-адреса`) = Шлях **relative to current file** (`відносно поточного файлу`).

| Path (Шлях) | Description (Опис) | Example (Приклад) |
|:---|:---|:---|
| `page.html` | Покликання до файлу в **same folder** (`тій самій папці`) | `<a href="contact.html">Contact</a>` |
| `folder/page.html` | Покликання до файлу всередині **subfolder** (`підпапки`) | `<a href="images/photo.jpg">Photo</a>` |
| `../page.html` | Покликання до файлу на **one level up** (`один рівень вище`) | `<a href="../index.html">Homepage</a>` |

**Використовуйте відносні URL-адреси для:**

  - Покликань між сторінками **your own website** (`вашого власного вебсайту`)
  - Завантаження зображень та інших **local assets** (`локальних активів`)

-----

## Anchor Links (Покликання-Якорі): Навігація всередині сторінки

**Anchor links** дозволяють переходити до **specific section** (`конкретного розділу`) **on the same page** (`на тій самій сторінці`).

### **Step 1: Create the target (Створіть ціль)**

Додайте **`id` attribute** (`атрибут id`) до елемента, до якого ви хочете перейти:

```html
<section id="introduction">
    <h2>1. Introduction</h2>
    <p>... content for the introduction ...</p>
</section>
```

### **Step 2: Create the link (Створіть покликання)**

Використовуйте символ **`#`** перед **`id` name** (`назвою id`) у **`href` attribute**:

```html
<a href="#introduction">Jump to Introduction</a>
```

-----

## Linking to Email and Phone (Покликання на Електронну Пошту та Телефон)

Ви можете ініціювати дії, а не лише переходити до сторінок:

```html
<!-- Email link - Opens the user's default email client (Покликання на Email - Відкриває стандартний поштовий клієнт користувача) -->
<a href="mailto:me@example.com">Email</a>

<!-- Phone link - Initiates a call on mobile devices (Покликання на Телефон - Ініціює виклик на мобільних пристроях) -->
<a href="tel:+14405551234">Call</a>

<!-- Anchor link - Jump to a section (Покликання-якір - Перехід до розділу) -->
<a href="#section">Jump to Section</a>

<!-- New tab - Opens the link in a new browser tab (Нова вкладка - Відкриває покликання в новій вкладці браузера) -->
<a href="page.html" target="_blank">New Tab</a>
```

-----

## Common Link Attributes (Поширені Атрибути Покликань)

| Attribute (Атрибут) | Purpose (Призначення) | Example (Приклад) |
|:---|:---|:---|
| **`href`** | Destination (Пункт призначення) | **`href="page.html"`** |
| **`target`** | Where to open (Де відкрити) | **`target="_blank"`** |
| **`title`** | Tooltip text (Текст підказки) | **`title="More info"`** |
| **`download`** | Force download (Примусове завантаження) | **`download`** |

-----

## Organizing Your Site Files (Організація Файлів Вашого Сайту)

**Good structure** (`Гарна структура`):

```
website/
├── index.html          (homepage - домашня сторінка)
├── about.html
├── css/
│   └── styles.css
├── images/
│   ├── logo.png
│   └── banner.jpg
└── pages/
    ├── services.html
    └── portfolio.html
```

**This makes linking easier and more organized\!** (`Це робить покликання простішими та більш організованими!`)

-----

## Today's Tasks (Сьогоднішні Завдання)

Ви створите **multi-page website** (`багатосторінковий вебсайт`) з:

1.  **Home page** (`Домашня сторінка`) з **navigation** (`навігацією`).
2.  **About page** (`Сторінка про нас`) з **internal links** (`внутрішніми покликаннями`).
3.  **Contact page** (`Сторінка контактів`) з **email/phone links** (`покликаннями на електронну пошту/телефон`).
4.  **All pages** (`Усі сторінки`) з'єднані **navigation** (`навігацією`).

**Focus on** (`Зосередьтеся на`):

  - Робочих покликаннях між сторінками.
  - Як **absolute**, так і **relative URLs** (`абсолютних та відносних URL-адресах`).
  - Покликаннях на електронну пошту та **anchor links** (`покликаннях-якорях`).

-----

## Questions? (Запитання?)

Перш ніж ми почнемо кодувати:

  - **Absolute vs. relative URLs**?
  - **Email links**?
  - **Anchor links** to sections?
  - **Navigation structure**?

-----

## Let's Build\! (Почнемо Будувати\!)

Відкрийте **VS Code** і почнемо...

-----

Чи хотіли б ви, щоб я надав вам приклад структури файлів для цього багатосторінкового сайту, або ви готові розпочати роботу над першим файлом, **`index.html`**?