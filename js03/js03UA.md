Зрозуміло. Ось переклад третього файлу (`js03.md`) на українську мову. Весь код залишено без змін, як і в попередніх запитах.

-----

````markdown
# Урок 03: Математичні Операції та Обчислення

## Основні Математичні Оператори

JavaScript може виконувати математичні обчислення, як звичайний калькулятор. Ось основні оператори:

### П'ять Основних Операцій

```javascript
let a = 10;
let b = 3;

console.log(a + b);  // Addition: 13
console.log(a - b);  // Subtraction: 7
console.log(a * b);  // Multiplication: 30
console.log(a / b);  // Division: 3.333...
console.log(a % b);  // Remainder (Modulo): 1
````

### Розуміння Кожного Оператора

**Додавання (+)**

```javascript
let total = 5 + 3;
console.log(total);  // 8

let score = 10;
score = score + 5;   // Add 5 to score
console.log(score);  // 15
```

**Віднімання (-)**

```javascript
let difference = 10 - 4;
console.log(difference);  // 6

let lives = 3;
lives = lives - 1;  // Lose a life
console.log(lives);  // 2
```

**Множення (\*)**

```javascript
let product = 6 * 7;
console.log(product);  // 42

let price = 19.99;
let quantity = 3;
let total = price * quantity;
console.log(total);  // 59.97
```

**Ділення (/)**

```javascript
let quotient = 20 / 4;
console.log(quotient);  // 5

let average = (80 + 90 + 85) / 3;
console.log(average);  // 85
```

**Залишок/Поділ за модулем (%)**
Оператор модуля дає **залишок** після ділення:

```javascript
console.log(10 % 3);   // 1 (10 ÷ 3 = 3 remainder 1)
console.log(15 % 4);   // 3 (15 ÷ 4 = 3 remainder 3)
console.log(20 % 5);   // 0 (20 ÷ 5 = 4 remainder 0)

// Common use: Check if a number is even or odd
let number = 7;
console.log(number % 2);  // 1 (odd)

let number2 = 8;
console.log(number2 % 2);  // 0 (even)
```

-----

## Порядок Виконання Операцій

Як і в математиці, JavaScript дотримується порядку дій (спочатку дужки, потім множення/ділення, потім додавання/віднімання):

```javascript
let result1 = 2 + 3 * 4;
console.log(result1);  // 14 (not 20!)
// Multiplication happens first: 3 * 4 = 12, then 2 + 12 = 14

let result2 = (2 + 3) * 4;
console.log(result2);  // 20
// Parentheses first: 2 + 3 = 5, then 5 * 4 = 20
```

**Завжди використовуйте дужки, коли хочете забезпечити однозначність:**

```javascript
// Calculating average - use parentheses!
let test1 = 85;
let test2 = 90;
let test3 = 78;

let average = (test1 + test2 + test3) / 3;
console.log(average);  // 84.333...
```

-----

## Інкремент та Декремент

Спеціальні скорочення для додавання або віднімання 1:

### Інкремент (++)

Додати 1 до змінної:

```javascript
let count = 5;
count++;  // Same as: count = count + 1
console.log(count);  // 6
```

### Декремент (--)

Відняти 1 від змінної:

```javascript
let lives = 3;
lives--;  // Same as: lives = lives - 1
console.log(lives);  // 2
```

### Практичний Приклад

```javascript
let score = 0;

// Player scores a point
score++;
console.log(score);  // 1

score++;
console.log(score);  // 2

// Player loses a point
score--;
console.log(score);  // 1
```

-----

## Складені Оператори Присвоєння

Скорочення для поширених операцій:

```javascript
let x = 10;

// Long way
x = x + 5;

// Short way (compound assignment)
x += 5;  // Same as: x = x + 5

console.log(x);  // 15
```

### Усі Складені Оператори

```javascript
let num = 10;

num += 5;   // num = num + 5  → 15
num -= 3;   // num = num - 3  → 12
num *= 2;   // num = num * 2  → 24
num /= 4;   // num = num / 4  → 6
num %= 4;   // num = num % 4  → 2

console.log(num);  // 2
```

**Коли використовувати складені оператори:**

  - При оновленні змінної на основі її поточного значення
  - Робить код коротшим та легшим для читання
  - Дуже поширені в лічильниках та накопичувачах

<!-- end list -->

```javascript
let total = 0;
let price1 = 19.99;
let price2 = 29.99;
let price3 = 9.99;

total += price1;  // Add first price
total += price2;  // Add second price
total += price3;  // Add third price

console.log(total);  // 59.97
```

-----

## Робота з Десятковими Дробами

JavaScript обробляє десяткові числа, але будьте обережні з точністю:

```javascript
let price = 19.99;
let tax = 0.08;

let totalTax = price * tax;
console.log(totalTax);  // 1.5992

// Round to 2 decimal places
let rounded = totalTax.toFixed(2);
console.log(rounded);  // "1.60" (note: this is a string!)

// Convert back to number if needed
let roundedNumber = Number(totalTax.toFixed(2));
console.log(roundedNumber);  // 1.60
```

### Метод toFixed()

`.toFixed()` округлює до певної кількості десяткових знаків:

```javascript
let num = 3.14159;

console.log(num.toFixed(0));  // "3"
console.log(num.toFixed(1));  // "3.1"
console.log(num.toFixed(2));  // "3.14"
console.log(num.toFixed(3));  // "3.142"
```

**Важливо:** `toFixed()` повертає **рядок**, а не число\!

-----

## Створення Простого Калькулятора

Об'єднаймо математичні операції з HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Price Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 400px;
            margin: 50px auto;
            padding: 20px;
        }
        .result {
            background-color: #f0f0f0;
            padding: 15px;
            margin-top: 20px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <h1>Shopping Cart Calculator</h1>
    <div class="result" id="output"></div>
    
    <script>
        // Item prices
        let itemPrice = 19.99;
        let quantity = 3;
        let taxRate = 0.08;  // 8% tax
        
        // Calculate subtotal
        let subtotal = itemPrice * quantity;
        
        // Calculate tax
        let tax = subtotal * taxRate;
        
        // Calculate total
        let total = subtotal + tax;
        
        // Display results (formatted to 2 decimal places)
        let output = `
            Item Price: $${itemPrice.toFixed(2)}
            Quantity: ${quantity}
            Subtotal: $${subtotal.toFixed(2)}
            Tax (8%): $${tax.toFixed(2)}
            Total: $${total.toFixed(2)}
        `;
        
        document.getElementById('output').textContent = output;
        
        // Also log to console
        console.log('Subtotal:', subtotal);
        console.log('Tax:', tax);
        console.log('Total:', total);
    </script>
</body>
</html>
```

-----

## Поширені Математичні Шаблони

### Пошук Середнього Значення

```javascript
let grade1 = 85;
let grade2 = 90;
let grade3 = 78;

let average = (grade1 + grade2 + grade3) / 3;
console.log(average);  // 84.333...
console.log(average.toFixed(1));  // "84.3"
```

### Обчислення Відсотків

```javascript
let score = 45;
let maxScore = 50;

let percentage = (score / maxScore) * 100;
console.log(percentage);  // 90
console.log(`You scored ${percentage}%`);
```

### Конвертація Одиниць

```javascript
// Celsius to Fahrenheit
let celsius = 20;
let fahrenheit = (celsius * 9/5) + 32;
console.log(`${celsius}°C = ${fahrenheit}°F`);  // 20°C = 68°F

// Miles to Kilometers
let miles = 10;
let kilometers = miles * 1.60934;
console.log(`${miles} miles = ${kilometers.toFixed(2)} km`);
```

### Розподіл Рахунку

```javascript
let totalBill = 87.50;
let numberOfPeople = 4;
let tipPercentage = 0.20;  // 20% tip

let tip = totalBill * tipPercentage;
let totalWithTip = totalBill + tip;
let perPerson = totalWithTip / numberOfPeople;

console.log(`Each person pays: $${perPerson.toFixed(2)}`);
// Each person pays: $26.25
```

-----

## Об'єкт Math (Бонус)

JavaScript має вбудований об'єкт `Math` з корисними методами:

```javascript
// Round numbers
console.log(Math.round(4.7));   // 5
console.log(Math.round(4.4));   // 4

// Round up or down
console.log(Math.ceil(4.1));    // 5 (ceiling - rounds up)
console.log(Math.floor(4.9));   // 4 (floor - rounds down)

// Get absolute value
console.log(Math.abs(-10));     // 10

// Find minimum and maximum
console.log(Math.min(5, 2, 8, 1));   // 1
console.log(Math.max(5, 2, 8, 1));   // 8

// Generate random number (0 to 1)
console.log(Math.random());     // 0.742... (random)

// Random number in a range (1 to 6, like a dice)
let dice = Math.floor(Math.random() * 6) + 1;
console.log(dice);  // Random number from 1 to 6
```

-----

## Підсумок

На цьому уроці ви дізналися:

  - ✅ Основні математичні оператори: `+`, `-`, `*`, `/`, `%`
  - ✅ Порядок виконання операцій (використовуйте дужки\!)
  - ✅ Інкремент (`++`) та декремент (`--`)
  - ✅ Складені оператори присвоєння: `+=`, `-=`, `*=`, `/=`
  - ✅ Робота з десятковими дробами за допомогою `toFixed()`
  - ✅ Поширені математичні шаблони (середні значення, відсотки, конвертації)
  - ✅ Основні методи об'єкта Math

### Анонс Наступного Уроку:

На наступному уроці ми навчимося **взаємодіяти з елементами HTML** — вибирати їх, змінювати їхній вміст та модифікувати їхні стилі.

-----

## Ключові Терміни

  - **Operator (Оператор)**: Символ, що виконує операцію (+, -, \*, /, %)
  - **Modulo (%) (Поділ за модулем)**: Повертає залишок після ділення
  - **Increment (++) (Інкремент)**: Додати 1 до змінної
  - **Decrement (--) (Декремент)**: Відняти 1 від змінної
  - **Compound Assignment (Складене Присвоєння)**: Оператори-скорочення (+=, -=, тощо)
  - **toFixed()**: Метод для округлення десяткових дробів до певних місць
  - **Math Object (Об'єкт Math)**: Вбудований об'єкт з математичними функціями

<!-- end list -->

```
```