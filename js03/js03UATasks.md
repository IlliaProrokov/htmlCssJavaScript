Звісно, ось переклад файлу завдань (`js03Tasks.md`) на українську мову. Всі блоки коду (code chunks) збережено англійською.

-----

# Урок 03 Завдання: Практика Математичних Операцій

-----

## Завдання 1: КЕРОВАНИЙ ПРИКЛАД - Калькулятор Оцінок

**Виконайте ці кроки, щоб створити калькулятор оцінок.**

### Крок 1: Створіть HTML Файл

Створіть файл під назвою `grade-calculator.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Grade Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .result {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            margin-top: 20px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        h1 {
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Grade Calculator</h1>
    <div class="result" id="output"></div>
    
    <script>
        // Test scores
        let test1 = 85;
        let test2 = 92;
        let test3 = 78;
        let test4 = 88;
        
        // Calculate total
        let total = test1 + test2 + test3 + test4;
        
        // Calculate average
        let average = total / 4;
        
        // Round to 1 decimal place
        let roundedAverage = average.toFixed(1);
        
        // Display the results
        document.getElementById('output').innerHTML = `
            <p>Test Scores: ${test1}, ${test2}, ${test3}, ${test4}</p>
            <p>Total Points: ${total}</p>
            <p>Average Grade: <strong>${roundedAverage}</strong></p>
        `;
        
        // Log to console
        console.log("Total:", total);
        console.log("Average:", average);
        console.log("Rounded Average:", roundedAverage);
    </script>
</body>
</html>
```

### Крок 2: Перевірте Це

1.  Відкрийте файл у вашому браузері.
2.  На сторінці мають відображатися оцінки, загальна сума та середнє значення (наприклад, Average Grade: **85.8**).
3.  Перевірте консоль (F12), щоб побачити залогіровані значення.

### Крок 3: Змініть Це

  - Змініть значення `test1`, `test2` тощо на власні оцінки (наприклад, з уроку математики).
  - Додайте п'яту змінну оцінки тесту (`test5`) та оновіть обчислення як для `total`, так і для `average`, щоб включити її.
  - Збережіть та оновіть, щоб побачити своє нове середнє значення.

**Контрольна Точка:** Переконайтеся, що ваше обчислення середнього значення правильно ділить на кількість тестів (наприклад, 5, якщо ви додали `test5`).

-----

## Завдання 2: Практика Складеного Присвоєння

**Мета:** Використовувати складені оператори присвоєння для керування запасами.

### Інструкції:

1.  Створіть файл під назвою `inventory.html`.
2.  Створіть змінні: `stock` (встановіть на 50), `sales` (встановіть на 15) та `restock` (встановіть на 25).
3.  Використовуйте складені оператори присвоєння для виконання таких операцій:
      - Зменште `stock` на кількість `sales` (`-=`).
      - Збільште `stock` на кількість одиниць `restock` (`+=`).
      - Зменште одиниці `restock` на 5 (наприклад, 5 одиниць було пошкоджено) (`-=`).
4.  Відобразіть кінцеву кількість `stock` та `restock` на сторінці.
5.  Залогіруйте всі три змінні в консоль наприкінці.

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Inventory Tracker</title>
</head>
<body>
    <h1>Warehouse Inventory</h1>
    <p id="stock-output"></p>
    <p id="restock-output"></p>
    
    <script>
        let stock = 50;
        let sales = 15;
        let restock = 25;
        
        // 1. Decrease stock by sales here
        
        // 2. Increase stock by restock here
        
        // 3. Decrease restock by 5 here
        
        // Display results
        document.getElementById('stock-output').textContent = `Final Stock: ${stock}`;
        document.getElementById('restock-output').textContent = `Remaining Restock Units: ${restock}`;
        
        // Log to console
        console.log("Final Stock:", stock);
        console.log("Final Sales (unchanged):", sales);
        console.log("Remaining Restock:", restock);
    </script>
</body>
</html>
```

### Очікуваний Вивід:

```
Final Stock: 60
Remaining Restock Units: 20
```

-----

## Завдання 3: Модуль та Інкремент/Декремент

**Мета:** Попрактикуватися з операторами Модуля, Інкременту та Декременту.

### Інструкції:

1.  Створіть файл під назвою `counter-math.html`.
2.  Створіть змінну `count` і встановіть її значення на 10.
3.  Використовуйте оператор **інкременту** для збільшення `count` на 1.
4.  Використовуйте оператор **декременту** для зменшення `count` на 1.
5.  Створіть змінну `checkEven` і встановіть її значення на 17.
6.  Використовуйте **оператор Модуля**, щоб знайти залишок при діленні `checkEven` на 2.
7.  Відобразіть усі результати в елементі `div`.

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Modulo & Increment Practice</title>
</head>
<body>
    <h1>Quick Math Check</h1>
    <div id="results"></div>
    
    <script>
        // Increment/Decrement
        let count = 10;
        
        // 1. Increment count by 1 here
        
        // 2. Decrement count by 1 here
        
        // Modulo
        let checkEven = 17;
        let remainder = 0; // Find the remainder of checkEven / 2 here
        
        // Display results
        document.getElementById('results').innerHTML = `
            <p>Original Count: 10</p>
            <p>Count after ++ and --: ${count}</p>
            <p>Number ${checkEven} divided by 2 has a Remainder of: ${remainder}</p>
            <p>Is ${checkEven} an even number? ${remainder === 0}</p>
        `;
        
        console.log("Final Count:", count);
        console.log("Remainder:", remainder);
    </script>
</body>
</html>
```

### Очікуваний Вивід:

```
Original Count: 10
Count after ++ and --: 10
Number 17 divided by 2 has a Remainder of: 1
Is 17 an even number? false
```

-----

## Завдання 4: Виклик - Конвертер Валют

**Мета:** Виконати кілька математичних операцій та використати `toFixed()` для валюти.

### Інструкції:

1.  Створіть файл під назвою `converter.html`.
2.  Створіть змінну для ціни в USD (`usdPrice = 55.75`).
3.  Створіть константу для обмінного курсу (`const CAD_RATE = 1.35;`).
4.  Обчисліть ціну в CAD (`cadPrice`).
5.  Обчисліть суму податку для ціни в CAD, використовуючи канадську ставку податку (`const TAX_RATE = 0.13;`).
6.  Обчисліть остаточну загальну ціну в CAD (ціна + податок).
7.  Відобразіть ціну в USD, ціну в CAD (округлену до 2 десяткових знаків), суму податку (округлену) та остаточну загальну суму (округлену) на сторінці.

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Currency Converter</title>
    <style>
        .output-box {
            border: 1px solid #ccc;
            padding: 15px;
            margin-top: 20px;
            font-size: 1.1em;
        }
    </style>
</head>
<body>
    <h1>USD to CAD Converter</h1>
    <div id="output" class="output-box"></div>
    
    <script>
        // Variables and Constants
        let usdPrice = 55.75;
        const CAD_RATE = 1.35;
        const TAX_RATE = 0.13; // 13% tax
        
        // 1. Calculate cadPrice
        let cadPrice = 0; // Calculation here
        
        // 2. Calculate tax amount
        let taxAmount = 0; // Calculation here
        
        // 3. Calculate final total
        let finalTotal = 0; // Calculation here
        
        // Display Results
        let display = `
            <p>USD Price: $${usdPrice.toFixed(2)} USD</p>
            <p>CAD Exchange Rate: ${CAD_RATE}</p>
            <p>CAD Price (Pre-Tax): $${cadPrice.toFixed(2)} CAD</p>
            <p>Tax Amount (13%): $${taxAmount.toFixed(2)} CAD</p>
            <p><strong>Total Price: $${finalTotal.toFixed(2)} CAD</strong></p>
        `;
        
        document.getElementById('output').innerHTML = display;
    </script>
</body>
</html>
```

### Очікувані Значення (Округлені):

  - `cadPrice`: 75.26
  - `taxAmount`: 9.78
  - `finalTotal`: 85.04

-----

## Завдання-Виклик: Роздільник Рахунку в Ресторані

**Мета:** Створити скрипт, який обчислює розподіл рахунку з чайовими.

### Інструкції:

1.  Створіть файл під назвою `bill-splitter.html`.

2.  Створіть змінні для:

      - `billAmount` (наприклад, 75.50)
      - `tipPercentage` (наприклад, 0.15 для 15%)
      - `numberOfPeople` (наприклад, 4)

3.  Обчисліть наступне:

      - `tipAmount` (billAmount \* tipPercentage)
      - `totalBill` (billAmount + tipAmount)
      - `perPerson` (totalBill / numberOfPeople)

4.  Відобразіть усі результати у відформатованому вигляді на сторінці.

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Bill Splitter</title>
</head>
<body>
    <h1>Restaurant Bill Splitter</h1>
    <div id="summary"></div>
    <div id="details"></div>
    
    <script>
        // Variables
        let billAmount = 75.50;
        let tipPercentage = 0.15; // 15%
        let numberOfPeople = 4;
        
        // Calculations
        let tipAmount = 0;      // Calculation here
        let totalBill = 0;      // Calculation here
        let perPerson = 0;      // Calculation here
        
        // Display Summary
        document.getElementById('summary').innerHTML = `
            <h2>Bill Details:</h2>
            <p>Original Bill: $${billAmount.toFixed(2)}</p>
            <p>Tip Percentage: ${(tipPercentage * 100).toFixed(0)}%</p>
            <p>Number of People: ${numberOfPeople}</p>
        `;
        
        // Display Final Details
        document.getElementById('details').innerHTML = `
            <h3>Final Split:</h3>
            <p>Total Tip: $${tipAmount.toFixed(2)}</p>
            <p>Total Bill (incl. Tip): $${totalBill.toFixed(2)}</p>
            <p style="font-size: 1.5em; color: green;">Each Person Owes: <strong>$${perPerson.toFixed(2)}</strong></p>
        `;
        
        // Log values
        console.log("Tip Amount:", tipAmount.toFixed(2));
        console.log("Total Bill:", totalBill.toFixed(2));
        console.log("Per Person:", perPerson.toFixed(2));
    </script>
</body>
</html>
```

### Очікуваний Вивід (Округлений):

  - `tipAmount`: 11.33
  - `totalBill`: 86.83
  - `perPerson`: 21.71

**Бонус-Виклик:** Додайте трохи CSS - *Ви можете скористатися ШІ, щоб допомогти з цією частиною CSS.*

  - Спробуйте різні початкові значення, щоб протестувати ваші обчислення

-----

## Поради для Успіху

1.  **Спочатку перевірте свої обчислення вручну** - Використовуйте калькулятор для перевірки
2.  **Використовуйте дужки** - Зробіть порядок виконання операцій зрозумілим: `(a + b) / 2`
3.  **Правильно форматуйте валюту** - Завжди використовуйте `.toFixed(2)` для грошей
4.  **Логіруйте значення** - Перевіряйте свої обчислення в консолі по мірі роботи
5.  **Один крок за раз** - Створюйте обчислення поступово
6.  **Перевіряйте порядок виконання операцій** - Множення та ділення відбуваються перед додаванням та відніманням

## Поширені Помилки, Яких Слід Уникати

❌ `let total = 10 + 5 * 2` (дорівнює 20, а не 30\!)
✅ `let total = (10 + 5) * 2` (дорівнює 30)

❌ `let price = 19.99` потім показується `$19.9` на сторінці
✅ `let price = 19.99` потім використання `$${price.toFixed(2)}` показує `$19.99`

❌ Забуття зберегти зміни змінної:

```javascript
let score = 0;
score + 10;  // This doesn't save!
```

✅ Збереження зміни:

```javascript
let score = 0;
score = score + 10;  // or score += 10;
```

❌ Ділення на нуль (спричиняє `Infinity`)
✅ Перевірте, чи ваш дільник не дорівнює нулю перед діленням

-----

## Порядок Виконання Операцій (PEMDAS)

Пам'ятайте: **П**арантези (дужки), **Е**кспоненти (степені), **М**ноження, **Д**ілення, **Д**одавання, **В**іднімання.

```
```