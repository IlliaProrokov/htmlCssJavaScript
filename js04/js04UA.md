Звісно. Ось переклад четвертого файлу (`js04.md`), присвяченого маніпулюванню DOM, на українську мову. Всі блоки коду (code chunks) збережено англійською.

-----

# Урок 04: Маніпулювання DOM - Взаємодія з HTML

## Що таке DOM?

**DOM** означає **Document Object Model** (Об'єктна Модель Документа). Це спосіб JavaScript "**спілкуватися**" та маніпулювати HTML-елементами на вашій веб-сторінці.

### Уявіть це Так:

  - **HTML** створює **структуру** вашої сторінки
  - **DOM** — це **представлення** цієї структури у JavaScript
  - **JavaScript** може використовувати DOM, щоб **знаходити, змінювати, додавати** або **видаляти** HTML-елементи

### Що Ви Можете Робити за Допомогою DOM?

  - Змінювати текстовий вміст
  - Модифікувати стилі елементів (кольори, розміри, тощо)
  - Додавати або видаляти HTML-елементи
  - Реагувати на дії користувача (кліки, набір тексту, тощо)

-----

## Вибір HTML-Елементів

Перш ніж ви зможете змінити елемент, вам потрібно його **вибрати** (знайти). Є кілька способів це зробити:

### Метод 1: getElementById()

Найпоширеніший спосіб — вибрати елемент за його атрибутом `id`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>DOM Example</title>
</head>
<body>
    <h1 id="title">Original Title</h1>
    <p id="message">Original message</p>
    
    <script>
        // Select elements by ID
        let titleElement = document.getElementById('title');
        let messageElement = document.getElementById('message');
        
        console.log(titleElement);
        console.log(messageElement);
    </script>
</body>
</html>
```

**Ключові Моменти:**

  - Використовуйте `document.getElementById('idName')`
  - Назва `id` повинна збігатися точно (чутливий до регістру)
  - Повертає **ОДИН** елемент (ID мають бути унікальними)
  - Зберігайте елемент у змінній для подальшого використання

### Метод 2: querySelector()

Цей метод є більш гнучким і використовує **синтаксис CSS-селекторів**. Він повертає **ПЕРШИЙ** елемент, який відповідає селектору:

```javascript
// Select the first element with the ID 'title'
let title = document.querySelector('#title');

// Select the first element with the class 'container'
let container = document.querySelector('.container');

// Select the first <p> tag
let paragraph = document.querySelector('p');
```

**Чому використовувати `querySelector()`?** Це дуже зручно, коли ви вже знаєте синтаксис CSS.

-----

## Зміна Вмісту Елемента

Після того, як ви вибрали елемент, ви можете змінити те, що він показує, використовуючи властивості:

### 1\. textContent

Властивість `textContent` дозволяє вам **отримати** або **встановити** вміст елемента як **простий текст**.

```javascript
let titleElement = document.getElementById('title');

// Get content
console.log(titleElement.textContent);  // Shows: Original Title

// Set content (replace the text)
titleElement.textContent = "New JavaScript Title!";
```

**Найкраща Практика:** Використовуйте `textContent` завжди, коли ви працюєте з простим текстом, оскільки це запобігає проблемам безпеки.

### 2\. innerHTML

Властивість `innerHTML` дозволяє вам отримати або встановити вміст, включаючи **HTML-теги**.

```html
<p id="message"></p>

<script>
    let messageElement = document.getElementById('message');
    
    // Set content (and include HTML tags)
    messageElement.innerHTML = "This message is <strong>important!</strong>";
</script>
```

**Увага:** Використовуйте `innerHTML` з обережністю, оскільки він може становити загрозу безпеці (Cross-Site Scripting, XSS), якщо ви вставляєте неперевірений вміст від користувача.

-----

## Зміна Стилів (CSS)

Ви можете змінювати стилі елемента безпосередньо за допомогою властивості `.style`.

```html
<h1 id="header">Hello World</h1>

<script>
    let header = document.getElementById('header');
    
    // Change the color
    header.style.color = 'blue';
    
    // Change the background color
    header.style.backgroundColor = '#f0f0f0';
    
    // Change font size (Note: use camelCase for CSS properties)
    header.style.fontSize = '24px';
</script>
```

**Ключові Моменти для Стилів:**

  - CSS властивості, які містять дефіс (наприклад, `background-color`), повинні бути перетворені на **camelCase** у JavaScript (`backgroundColor`).
  - Завжди включайте одиницю вимірювання (наприклад, `'24px'`, а не `'24'`).

-----

## Керування Класами CSS

Найкращий спосіб керування стилями — це додавати або видаляти класи CSS, а не змінювати `.style` безпосередньо. Для цього використовуйте властивість `.classList`.

```html
<style>
.highlight {
    background-color: yellow;
    border: 2px solid orange;
}
.hidden {
    display: none;
}
</style>

<p id="status">Current Status</p>

<script>
    let status = document.getElementById('status');
    
    // Add a class (e.g., to highlight the element)
    status.classList.add('highlight');
    
    // Remove a class
    status.classList.remove('highlight');
    
    // Toggle a class (adds if absent, removes if present)
    status.classList.toggle('hidden');
    
    // Check if a class exists (returns true/false)
    console.log(status.classList.contains('highlight'));
</script>
```

**Чому використовувати `classList`?**

  - **Clean Code (Чистий Код):** Відокремлює стилі (CSS) від поведінки (JavaScript).
  - **Flexibility (Гнучкість):** Один клас може містити багато правил стилів.

-----

## Керування Атрибутами

Ви можете отримувати та встановлювати будь-який HTML-атрибут (наприклад, `href` для посилань, `src` для зображень) за допомогою методів `getAttribute()` та `setAttribute()`.

```html
<!DOCTYPE html>
<html>
<body>
    <img id="logo" src="old-logo.png" alt="Company Logo">
    <a id="site-link" href="https://oldsite.com">Visit Site</a>
    
    <script>
        let img = document.getElementById('logo');
        let link = document.getElementById('site-link');
        
        // Get attributes
        console.log(img.src);   // Current image source
        console.log(link.href); // Current link URL
        
        // Set attributes
        img.src = 'new-photo.jpg';
        img.alt = 'New profile picture';
        
        link.href = 'https://newsite.com';
        link.textContent = 'Visit New Site';
    </script>
</body>
</html>
```

-----

## Підсумок

На цьому уроці ви дізналися:

  - ✅ **DOM** дозволяє JavaScript взаємодіяти з HTML-елементами
  - ✅ Вибирайте елементи за допомогою **`getElementById()`** або **`querySelector()`**
  - ✅ Змінюйте вміст за допомогою **`textContent`** (простий текст) або **`innerHTML`** (HTML)
  - ✅ Змінюйте стилі за допомогою **`.style.property`**
  - ✅ Додавайте/видаляйте класи CSS за допомогою **`.classList`**
  - ✅ Отримуйте та модифікуйте атрибути елементів

### Найкращі Практики:

  - Зберігайте вибрані елементи у змінних
  - Використовуйте `classList` замість прямих змін стилю, коли це можливо
  - Використовуйте `textContent` для простого тексту, `innerHTML` лише за необхідності
  - Надавайте елементам змістовні ID

### Анонс Наступного Уроку:

На наступному уроці ми дізнаємося про **події** — як реагувати на дії користувача, такі як кліки, наведення курсора та набір тексту\!

-----

## Ключові Терміни

  - **DOM**: Document Object Model - спосіб JavaScript взаємодіяти з HTML
  - **getElementById()**: Вибирає елемент за його атрибутом `id`
  - **querySelector()**: Вибирає елемент, використовуючи синтаксис CSS-селекторів
  - **textContent**: Властивість для отримання/встановлення простого текстового вмісту
  - **innerHTML**: Властивість для отримання/встановлення HTML-вмісту
  - **style**: Властивість для прямої зміни стилів CSS
  - **classList**: Властивість для додавання/видалення класів CSS

<!-- end list -->

```
```