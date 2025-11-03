Звісно, ось переклад лише першого файлу (`js02.md`) на українську мову. Всі блоки коду (code chunks) збережено англійською.

-----

````markdown
# Урок 02: Змінні та Типи Даних

## Навіщо ми це вивчаємо?
На цьому уроці ми дізнаємося, як комп'ютери **запам'ятовують та використовують інформацію** — це ключова навичка, що забезпечує роботу веб-сайтів, ігор та навіть розумних систем на базі ШІ.

## Що таке Змінні?

Змінні схожі на **марковані контейнери**, які зберігають інформацію у вашій програмі. Уявіть їх як коробки з етикетками, куди ви можете класти різні речі.

### Аналогія з Реального Світу
Уявіть, що у вас є коробка з етикеткою "**firstName**" — всередині цієї коробки ви можете помістити значення "**Sarah**". Пізніше ви можете заглянути в цю коробку, щоб побачити, що там, або замінити її вміст на щось інше.

```javascript
let firstName = "Sarah";
console.log(firstName);  // Shows: Sarah
````

-----

## Створення Змінних

У сучасному JavaScript ми використовуємо `let` та `const` для створення змінних.

### Використання `let`

Використовуйте `let`, коли **значення може змінитися** пізніше:

```javascript
let age = 25;
console.log(age);  // Shows: 25

age = 26;  // Changed the value
console.log(age);  // Shows: 26
```

### Використання `const`

Використовуйте `const`, коли **значення НІКОЛИ не повинно змінюватися** (константа):

```javascript
const birthYear = 1998;
console.log(birthYear);  // Shows: 1998

birthYear = 1999;  // ❌ ERROR! Can't change a const
```

### Уникайте `var` (Старий Спосіб)

Ви можете побачити `var` у старому коді, але **замість нього використовуйте `let` та `const`**:

```javascript
var x = 5;  // ❌ Old way - don't use this
let y = 5;  // ✅ Modern way - use this
```

-----

## Давайте Повторимо Це...

### `const` (константа)

Ви використовуєте **`const`**, коли значення **ніколи не повинно змінюватися**.

**Приклади ситуацій:**

  - **Рік народження** (не може змінитися після народження).
  - **Кількість днів на тиждень**.
  - Фіксований **ключ API** або налаштування конфігурації.

Якщо ви спробуєте переприсвоїти його, ви отримаєте помилку:

```js
const birthYear = 1998;
birthYear = 1999;  // ❌ Not allowed
```

-----

### `let` (змінна)

Використовуйте **`let`**, коли значення **може змінюватися з часом**.

**Приклади ситуацій:**

  * **Рахунок** в грі:

    ```js
    let score = 0;
    score = score + 10; // Now score = 10
    ```

  * **Лічильник** в циклі - ми незабаром розглянемо цикли (`loops`).

  * **Поточний вік** користувача (вік змінюється щороку, навіть якщо `birthYear` не змінюється):

    ```js
    const birthYear = 1998;
    let currentYear = 2025;
    let age = currentYear - birthYear; // 27
    ```

-----

### Основне Правило

  * За замовчуванням використовуйте **`const`** (безпечніше, запобігає випадковим змінам).
  * Використовуйте **`let`**, коли ви *знаєте*, що значення зміниться.

<br>
<br>
---

## Правила Іменування Змінних

### Правила, яких ви ПОВИННІ дотримуватися:

1.  Змінні можуть містити літери, цифри, `_`, та `$`
2.  Змінні **ПОВИННІ** починатися з літери, `_`, або `$` (не з цифри)
3.  Змінні чутливі до регістру (`name` та `Name` — це різні змінні)
4.  Не можна використовувати зарезервовані слова (`let`, `const`, `if`, `function`, тощо)

### Приклади:

```javascript
// ✅ Valid variable names
let firstName = "John";
let age2 = 25;
let _private = true;
let $price = 19.99;

// ❌ Invalid variable names
let 2age = 25;        // Can't start with number
let first-name = "John";  // Can't use dashes
let let = 5;          // Can't use reserved word
```

### Найкращі Практики (Конвенції):

  - Використовуйте **camelCase** для назв змінних: `firstName`, `userAge`, `totalPrice`
  - Робіть назви описовими: `userName` краще, ніж `un`
  - Починайте з малої літери (велика літера призначена для класів, які будуть пізніше)
  - За замовчуванням використовуйте `const`, `let` використовуйте, лише якщо ви знаєте, що значення зміниться

<!-- end list -->

```javascript
// ❌ Poor naming
let x = "John";
let y = 25;

// ✅ Good naming
let userName = "John";
let userAge = 25;
```

-----

## Типи Даних

JavaScript має кілька типів даних. Ось три найважливіші для початківців:

### 1\. Рядки (Strings / Текст)

Рядки — це текст, взятий у лапки. Ви можете використовувати одинарні `'` або подвійні лапки `"`:

```javascript
let firstName = "Alice";
let lastName = 'Smith';
let message = "Hello, World!";

console.log(firstName);  // Shows: Alice
```

**Важливо:** Лапки на початку та в кінці повинні збігатися\!

```javascript
let wrong = "Hello';  // ❌ ERROR - quotes don't match
let right = "Hello";  // ✅ Correct
```

### 2\. Числа (Numbers)

Числа не використовують лапок. Це можуть бути цілі числа або десяткові дроби:

```javascript
let age = 25;
let price = 19.99;
let temperature = -5;

console.log(age);     // Shows: 25
console.log(price);   // Shows: 19.99
```

### 3\. Булеві (Booleans / True/False)

Булеві значення прості: або `true` (істина), або `false` (хибність) (без лапок):

```javascript
let isStudent = true;
let isLoggedIn = false;
let hasAccount = true;

console.log(isStudent);  // Shows: true
```

Булеві значення використовуються для ситуацій так/ні, увімкнено/вимкнено, істина/хибність.

-----

## Перевірка Типів Даних

Ви можете перевірити, який тип даних містить змінна, використовуючи `typeof`:

```javascript
let name = "John";
let age = 30;
let isStudent = true;

console.log(typeof name);      // Shows: string
console.log(typeof age);       // Shows: number
console.log(typeof isStudent); // Shows: boolean
```

-----

## Робота з Рядками

### Конкатенація Рядків (Об'єднання Рядків)

Використовуйте оператор `+`, щоб об'єднати рядки:

```javascript
let firstName = "John";
let lastName = "Smith";

let fullName = firstName + " " + lastName;
console.log(fullName);  // Shows: John Smith
```

### Шаблонні Літерали (Template Literals / Сучасний Спосіб)

Використовуйте зворотні лапки `` ` `` та `${}` для вставки змінних у рядки:

```javascript
let name = "Alice";
let age = 25;

// Old way
let message1 = "My name is " + name + " and I am " + age + " years old.";

// New way (better!)
let message2 = `My name is ${name} and I am ${age} years old.`;

console.log(message2);
// Shows: My name is Alice and I am 25 years old.
```

**Чому шаблонні літерали кращі:**

  - Легше читати
  - Можна включати будь-який вираз всередину `${}`
  - Можуть займати кілька рядків

<!-- end list -->

```javascript
let price = 19.99;
let quantity = 3;

let message = `The total cost is $${price * quantity}`;
console.log(message);  // Shows: The total cost is $59.97
```

-----

## Відображення Змінних в HTML

Тепер підключимо змінні до веб-сторінки:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Variables Demo</title>
</head>
<body>
    <h1 id="greeting"></h1>
    <p id="info"></p>
    
    <script>
        // Create variables
        let userName = "Sarah";
        let userAge = 22;
        let userCity = "New York";
        
        // Put variables into HTML elements
        document.getElementById('greeting').textContent = `Hello, ${userName}!`;
        
        document.getElementById('info').textContent = 
            `You are ${userAge} years old and live in ${userCity}.`;
    </script>
</body>
</html>
```

**Ключові Моменти:**

  - Використовуйте `document.getElementById()` для вибору HTML-елементів
  - Використовуйте `.textContent` для зміни тексту всередині елемента
  - Шаблонні літерали полегшують вставку змінних

-----

## Переприсвоєння Змінних

За допомогою `let` ви можете змінити значення змінної:

```javascript
let score = 0;
console.log(score);  // Shows: 0

score = 10;
console.log(score);  // Shows: 10

score = score + 5;
console.log(score);  // Shows: 15
```

За допомогою `const` ви не можете:

```javascript
const maxScore = 100;
console.log(maxScore);  // Shows: 100

maxScore = 200;  // ❌ ERROR! Cannot reassign a constant
```

-----

## Підсумок

На цьому уроці ви дізналися:

  - ✅ Змінні зберігають інформацію в маркованих контейнерах
  - ✅ Використовуйте `let` для значень, що змінюються, `const` для значень, що не змінюються
  - ✅ Назви змінних повинні відповідати певним правилам (без пробілів, не починатися з цифр)
  - ✅ Три основні типи даних: **рядки** (текст), **числа**, **булеві** (істина/хибність)
  - ✅ Використовуйте `typeof` для перевірки типів даних
  - ✅ Об'єднуйте рядки за допомогою `+` або використовуйте шаблонні літерали зі зворотними лапками
  - ✅ Відображайте змінні в HTML за допомогою `getElementById()` та `.textContent`

### Анонс Наступного Уроку:

На наступному уроці ми дізнаємося про **основні математичні операції** та як виконувати обчислення за допомогою JavaScript.

-----

## Ключові Терміни

  - **Variable (Змінна)**: Маркований контейнер, який зберігає дані
  - **let**: Ключове слово для створення змінної, яку можна змінювати
  - **const**: Ключове слово для створення константи, яку не можна змінювати
  - **String (Рядок)**: Тип даних для тексту (використовує лапки)
  - **Number (Число)**: Числовий тип даних (без лапок)
  - **Boolean (Булевий)**: Тип даних істина/хибність
  - **Template Literal (Шаблонний Літерал)**: Сучасний формат рядка, що використовує зворотні лапки
  - **Concatenation (Конкатенація)**: Об'єднання рядків

<!-- end list -->

```
```