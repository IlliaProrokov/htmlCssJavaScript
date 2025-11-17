Чудово, ось переклад українською мовою. Я залишив ключові терміни, ключові слова мови (`let`, `const`, `String`, `Number`, `Boolean`, `typeof` тощо), та всі блоки коду англійською, як ви просили, а також переклав визначення, зберігши в них англійські терміни для ідентифікації.

-----

# Урок 02: Змінні (`Variables`) та Типи Даних (`Data Types`)

## Навіщо ми це вивчаємо?

На цьому уроці ми дізнаємося, як комп'ютери **запам'ятовують та використовують інформацію** — це основна навичка, що забезпечує роботу вебсайтів, ігор і навіть розумного прийняття рішень у системах ШІ.

-----

## Що таке Змінні (`Variables`)?

Змінні (`Variables`) схожі на **марковані контейнери**, які зберігають інформацію у вашій програмі. Уявіть їх як коробки з написами, куди ви можете класти різні речі.

### Аналогія з Реального Світу

Уявіть, що у вас є коробка з написом "**firstName**" (ім'я) — всередину цієї коробки ви можете помістити значення "**Sarah**". Пізніше ви можете зазирнути в цю коробку, щоб побачити, що всередині, або замінити вміст чимось іншим.

```javascript
let firstName = "Sarah";
console.log(firstName);  // Shows: Sarah
```

-----

## Створення Змінних

У сучасному JavaScript ми використовуємо ключові слова **`let`** та **`const`** для створення змінних.

### Використання `let`

Використовуйте `let`, коли значення може змінитися пізніше:

```javascript
let age = 25;
console.log(age);  // Shows: 25

age = 26;  // Changed the value
console.log(age);  // Shows: 26
```

### Використання `const`

Використовуйте `const`, коли значення **НІКОЛИ** не повинно змінюватися (константа):

```javascript
const birthYear = 1998;
console.log(birthYear);  // Shows: 1998

birthYear = 1999;  // ❌ ERROR! Can't change a const
```

### Уникайте `var` (Старий Спосіб)

Ви можете побачити `var` у старому коді, але **використовуйте `let` та `const` замість нього**:

```javascript
var x = 5;  // ❌ Old way - don't use this
let y = 5;  // ✅ Modern way - use this
```

-----

## Повторимо Це Ще Раз...

### `const` (Константа)

Ви використовуєте **`const`**, коли значення **ніколи не повинно змінюватися**.

**Приклади ситуацій:**

  * **Рік народження** (не може змінитися після народження людини).  
  * **Кількість днів у тижні**.  
  * Фіксований **API key** або налаштування конфігурації.  

Якщо ви спробуєте переприсвоїти його, ви отримаєте помилку:  

```js
const birthYear = 1998;
birthYear = 1999;  // ❌ Not allowed
```

-----

### `let` (Змінна)

Використовуйте **`let`**, коли значення **може змінюватися з часом**.

**Приклади ситуацій:**

  * **Рахунок (`score`)** у грі:

  ` js   let score = 0;   score = score + 10; // Now score = 10    `

  * **Лічильник (`counter`)** у циклі — ми розглянемо цикли (`loops`) пізніше.
  * **Поточний вік** користувача (вік змінюється щороку, навіть якщо `birthYear` не змінюється):

  ` js   const birthYear = 1998;   let currentYear = 2025;   let age = currentYear - birthYear; // 27    `

-----

### Золоте Правило

  * За замовчуванням використовуйте **`const`** (це безпечніше, запобігає випадковим змінам).
  * Використовуйте **`let`**, лише коли ви *точно знаєте*, що значення буде змінюватися.

-----

## Правила Іменування Змінних

### Правила, Яких НЕОБХІДНО дотримуватись:

1.  Змінні можуть містити літери, цифри, `_` та `$`
2.  Змінні **ПОВИННІ** починатися з літери, `_` або `$` (не з цифри)
3.  Змінні чутливі до регістру (`name` та `Name` — це різні змінні)
4.  Не можна використовувати зарезервовані слова (`let`, `const`, `if`, `function` тощо)

### Приклади:

```javascript
// ✅ Valid variable names
let firstName = "John";
let age2 = 25;
let _private = true;
let $price = 19.99;

// ❌ Invalid variable names
let 2age = 25;        // Can't start with number
let first-name = "John";  // Can't use dashes
let let = 5;          // Can't use reserved word
```

### Найкращі Практики (Конвенції):

  * Використовуйте **camelCase** для імен змінних: `firstName`, `userAge`, `totalPrice`
  * Робіть імена описовими: `userName` краще, ніж `un`
  * Починайте з малої літери (велика літера використовується пізніше для класів)
  * Використовуйте `const` за замовчуванням, використовуйте `let` лише якщо ви знаєте, що значення зміниться

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

## Типи Даних (`Data Types`)

JavaScript має декілька типів даних. Ось три найважливіші для початківців:

### 1\. Рядки (`Strings`) (Текст)

Рядки (`Strings`) — це текст, який береться в лапки. Можна використовувати одинарні `'` або подвійні лапки `"`:

```javascript
let firstName = "Alice";
let lastName = 'Smith';
let message = "Hello, World!";

console.log(firstName);  // Shows: Alice
```

**Важливо:** Лапки на початку та в кінці мають збігатися\!

```javascript
let wrong = "Hello';  // ❌ ERROR - quotes don't match
let right = "Hello";  // ✅ Correct
```

### 2\. Числа (`Numbers`)

Числа (`Numbers`) не використовують лапки. Це можуть бути цілі числа або дробові:

```javascript
let age = 25;
let price = 19.99;
let temperature = -5;

console.log(age);     // Shows: 25
console.log(price);   // Shows: 19.99
```

### 3\. Булеві Значення (`Booleans`) (Правда/Хиба)

Булеві значення (`Booleans`) прості: це або `true` (правда), або `false` (хиба) (без лапок):

```javascript
let isStudent = true;
let isLoggedIn = false;
let hasAccount = true;

console.log(isStudent);  // Shows: true
```

`Booleans` використовуються для ситуацій "так/ні", "увімкнено/вимкнено", "правда/хиба".

-----

## Перевірка Типів Даних

Ви можете перевірити, який тип даних містить змінна, використовуючи оператор `typeof`:

```javascript
let name = "John";
let age = 30;
let isStudent = true;

console.log(typeof name);      // Shows: string
console.log(typeof age);       // Shows: number
console.log(typeof isStudent); // Shows: boolean
```

-----

## Робота з Рядками (`Strings`)

### Конкатенація Рядків (`String Concatenation`) (Об'єднання Рядків)

Використовуйте оператор `+`, щоб об'єднати рядки:

```javascript
let firstName = "John";
let lastName = "Smith";

let fullName = firstName + " " + lastName;
console.log(fullName);  // Shows: John Smith
```

### Шаблонні Літерали (`Template Literals`) (Сучасний Спосіб)

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

  * Легше читати
  * Можуть включати будь-який вираз всередині `${}`
  * Можуть займати кілька рядків

<!-- end list -->

```javascript
let price = 19.99;
let quantity = 3;

let message = `The total cost is $${price * quantity}`;
console.log(message);  // Shows: The total cost is $59.97
```

-----

## Відображення Змінних у HTML

Тепер підключимо змінні до вебсторінки:

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

**Ключові моменти:**

  * Використовуйте `document.getElementById()` для вибору елементів HTML
  * Використовуйте `.textContent` для зміни тексту всередині елемента
  * Шаблонні літерали (Template literals) спрощують вставку змінних

-----

## Переприсвоєння Змінних (`Variable Reassignment`)

За допомогою `let` ви можете змінити значення змінної:

```javascript
let score = 0;
console.log(score);  // Shows: 0

score = 10;
console.log(score);  // Shows: 10

score = score + 5;
console.log(score);  // Shows: 15
```

За допомогою `const` — ні:

```javascript
const maxScore = 100;
console.log(maxScore);  // Shows: 100

maxScore = 200;  // ❌ ERROR! Cannot reassign a constant
```

-----

## Підсумок

На цьому уроці ви дізналися:

  * ✅ Змінні (`Variables`) зберігають інформацію в маркованих контейнерах
  * ✅ Використовуйте **`let`** для значень, які змінюються, **`const`** для значень, які не змінюються
  * ✅ Імена змінних повинні відповідати певним правилам (без пробілів, не починаються з цифр)
  * ✅ Три основні типи даних: **strings** (текст), **numbers** (числа), **booleans** (правда/хиба)
  * ✅ Використовуйте **`typeof`** для перевірки типів даних
  * ✅ Об'єднуйте рядки за допомогою `+` або використовуйте **template literals** зі зворотними лапками
  * ✅ Відображайте змінні в HTML за допомогою `getElementById()` та `.textContent`

### Анонс Наступного Уроку:

На наступному уроці ми вивчимо **основні математичні операції** та як виконувати обчислення за допомогою JavaScript.

-----

## Ключові Терміни

  * **Variable**: Маркований контейнер, який зберігає дані
  * **let**: Ключове слово для створення змінної, яка може змінюватися
  * **const**: Ключове слово для створення константи, яка не може змінюватися
  * **String**: Тип даних для тексту (використовує лапки)
  * **Number**: Тип даних для числових значень (без лапок)
  * **Boolean**: Тип даних для значень `true` або `false`
  * **Template Literal**: Сучасний формат рядка з використанням зворотних лапок (`` ` ``)
  * **Concatenation**: Об'єднання рядків докупи

-----

Бажаєте, щоб я переклав наступний урок про математичні операції?