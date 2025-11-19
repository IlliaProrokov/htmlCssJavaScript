Звісно\! Я переклав завдання, залишивши коди, назви файлів та ключові терміни англійською мовою. Додатково я надав пояснення до цих технічних термінів українською.

-----

## Завдання Уроку 03: Практика Математичних Операцій

-----

## Task 1: GUIDED EXAMPLE - Grade Calculator (Керований Приклад - Калькулятор Оцінок)

**Виконайте ці кроки, щоб створити калькулятор оцінок.**

### Step 1: Create the HTML File (Крок 1: Створіть HTML-файл)

Створіть файл під назвою **`grade-calculator.html`**:

http://googleusercontent.com/immersive_entry_chip/0

### Step 2: Test and Modify (Крок 2: Тестування та Модифікація)

1.  Відкрийте файл у своєму браузері.
2.  Перегляньте обчислені результати.
3.  Змініть оцінки за тести на інші значення.
4.  Оновіть сторінку та перегляньте нові обчислення.

**✅ Checkpoint (Контрольна точка):** Середнє значення має оновлюватися правильно, коли ви змінюєте оцінки за тести.

-----

## Task 2: Basic Calculator (Базовий Калькулятор)

**Goal (Мета):** Практика всіх основних математичних операцій.

### Instructions (Інструкції):

1.  Створіть файл під назвою **`calculator.html`**
2.  Створіть дві **variables** (`змінні`): **`num1`** та **`num2`** (використовуйте будь-які числа). *Змінна — це контейнер для зберігання даних у пам'яті програми.*
3.  Виконайте всі п'ять операцій: **`+`** (додавання), **`-`** (віднімання), **`*`** (множення), **`/`** (ділення), **`%`** (залишок від ділення).
4.  Відобразіть кожен **result** (`результат`) на сторінці з підписом.
5.  Також запишіть кожен результат у **console** (`консоль`).

### Starter Code (Початковий Код):

````html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Basic Calculator</title>
</head>
<body>
    <h1>Math Operations Practice</h1>
    
    <!-- Create paragraph elements for each operation (Створіть елементи абзацу для кожної операції) -->
    <p id="addition"></p>
    <p id="subtraction"></p>
    <p id="multiplication"></p>
    <p id="division"></p>
    <p id="remainder"></p>
    
    <script>
        // Your two numbers (Ваші два числа)
        let num1 = 10;
        let num2 = 5;
        
        // Perform calculations (Виконайте обчислення)
        let sum = num1 + num2;
        let difference = num1 - num2;
        let product = num1 * num2;
        // Add division here (Додайте ділення тут)
        // Add remainder here (Додайте залишок від ділення тут)
        
        // Display results using template literals (Відобразіть результати, використовуючи шаблонні літерали)
        // Шаблонний літерал — це спосіб створення рядка в JavaScript, який дозволяє легко вставляти змінні (наприклад, ${sum}) всередину рядка.
        document.getElementById('addition').textContent = `Addition: ${num1} + ${num2} = ${sum}`;
        document.getElementById('subtraction').textContent = `Subtraction: ${num1} - ${num2} = ${difference}`;
        // Add the rest of your displays here (Додайте решту ваших відображень тут)
        
        // Log to console (Запишіть у console)
        console.log('Sum:', sum);
        console.log('Difference:', difference);
        // Add the rest of your console.log statements (Додайте решту ваших console.log інструкцій)
    </script>
</body>
</html>

### Expected Output on Page (Очікуваний Вивід на Сторінці):
Addition: 10 + 5 = 15
Subtraction: 10 - 5 = 5
Multiplication: 10 * 5 = 50
Division: 10 / 5 = 2
Remainder: 10 % 5 = 0

**💡 Hint (Підказка):** Оператор **modulo** (`%`) дає вам **remainder** (`залишок`) від ділення. Наприклад, `10 % 3 = 1`, тому що 10 ÷ 3 = 3 і залишок 1.

---

## Task 3: Shopping Cart Total (Загальна Сума Кошика Покупок)

**Goal (Мета):** Обчислити загальну суму кошика покупок з податком.

### Instructions (Інструкції):
1.  Створіть файл під назвою **`shopping-cart.html`**
2.  Створіть **variables** (`змінні`) для трьох товарів із зазначенням їхніх **prices** (`цін`).
3.  Обчисліть **subtotal** (`проміжну суму`) (суму всіх цін).
4.  Обчисліть **tax** (`податок`) (8% від проміжної суми).
5.  Обчисліть **total** (`загальну суму`) (проміжна сума + податок).
6.  Відобразіть всю інформацію, красиво відформатовану, на сторінці.

### Starter Code (Початковий Код):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Shopping Cart</title>
    <style>
        body {
            font-family: 'Courier New', monospace;
            max-width: 400px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        .receipt {
            background-color: white;
            padding: 20px;
            border: 2px dashed #333;
        }
        h2 {
            text-align: center;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div class="receipt">
        <h2>Shopping Cart Summary</h2>
        <p id="item1"></p>
        <p id="item2"></p>
        <p id="item3"></p>
        <hr>
        <p id="subtotal"></p>
        <p id="tax"></p>
        <hr>
        <p id="total"></p>
    </div>
    
    <script>
        // Item prices (Ціни товарів)
        let item1Price = 29.99;
        let item2Price = 15.50;
        let item3Price = 42.00;
        let taxRate = 0.08;  // 8% tax (Податкова ставка 8%)
        
        // Calculate subtotal (Обчислити проміжну суму)
        let subtotal = item1Price + item2Price + item3Price;
        
        // Calculate tax (Обчислити податок)
        let tax = subtotal * taxRate;
        
        // Calculate total (Обчислити загальну суму)
        let total = subtotal + tax;
        
        // Display items (Відобразити товари)
        document.getElementById('item1').textContent = `Item 1: $${item1Price.toFixed(2)}`;
        // Complete item2 and item3 displays (Доповніть відображення item2 та item3)
        
        // Display calculations (use .toFixed(2) to show 2 decimal places) (Відобразіть обчислення, використовуючи .toFixed(2), щоб показати 2 знаки після коми)
        // .toFixed(2) — це метод JavaScript, який округлює число до заданої кількості знаків після коми (у цьому випадку до 2), що ідеально підходить для відображення грошових сум.
        document.getElementById('subtotal').textContent = `Subtotal: $${subtotal.toFixed(2)}`;
        // Complete tax display (Доповніть відображення податку)
        // Complete total display (Доповніть відображення загальної суми)
        
        console.log('Subtotal:', subtotal);
        console.log('Tax:', tax);
        console.log('Total:', total);
    </script>
</body>
</html>

### Expected Output (Очікуваний Вивід):
Shopping Cart Summary
---------------------
Item 1: $29.99
Item 2: $15.50
Item 3: $42.00
---------------------
Subtotal: $87.49
Tax (8%): $7.00
---------------------
Total: $94.49

**💡 Hint (Підказка):** Метод **`.toFixed(2)`** округлює числа до 2 знаків після коми, що ідеально підходить для грошей!

---

## Task 4: Counter with Increment/Decrement (Лічильник зі Збільшенням/Зменшенням)

**Goal (Мета):** Практика використання операторів **`++`** та **`--`**.

### Instructions (Інструкції):
1.  Створіть файл під назвою **`score-tracker.html`**
2.  Створіть **variable** (`змінну`) під назвою **`score`** (`рахунок`), починаючи з **0**.
3.  Відобразіть початковий рахунок.
4.  Використовуйте **`++`** для збільшення рахунку **5** разів (по одному за раз).
5.  Відобразіть рахунок після кожного збільшення.
6.  Використовуйте **`--`** для зменшення рахунку **2** рази.
7.  Відобразіть остаточний рахунок.

### Starter Code (Початковий Код):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Score Tracker</title>
</head>
<body>
    <h1>Game Score Tracker</h1>
    
    <p id="start"></p>
    <p id="point1"></p>
    <p id="point2"></p>
    <p id="point3"></p>
    <p id="point4"></p>
    <p id="point5"></p>
    <p id="penalty1"></p>
    <p id="penalty2"></p>
    <p id="final"></p>
    
    <script>
        // Starting score (Початковий рахунок)
        let score = 0;
        document.getElementById('start').textContent = `Starting score: ${score}`;
        
        // Increase score 5 times (Збільшити рахунок 5 разів)
        score++;  // This adds 1 to score (Це додає 1 до рахунку)
        // Оператор ++ (Increment) — це скорочений спосіб додати 1 до змінної (score = score + 1).
        document.getElementById('point1').textContent = `After point 1: ${score}`;
        
        score++;
        document.getElementById('point2').textContent = `After point 2: ${score}`;
        
        // You do the next 3 increases... (Ви робите наступні 3 збільшення...)
        
        // Decrease score 2 times (Зменшити рахунок 2 рази)
        score--;  // This subtracts 1 from score (Це віднімає 1 від рахунку)
        // Оператор -- (Decrement) — це скорочений спосіб відняти 1 від змінної (score = score - 1).
        document.getElementById('penalty1').textContent = `After penalty 1: ${score}`;
        
        // You do the second decrease... (Ви робите друге зменшення...)
        
        // Display final (Відобразити остаточний рахунок)
        document.getElementById('final').textContent = `Final Score: ${score}`;
    </script>
</body>
</html>

### Expected Display (Очікуване Відображення):
Starting score: 0
After point 1: 1
After point 2: 2
After point 3: 3
After point 4: 4
After point 5: 5
After penalty 1: 4
After penalty 2: 3
Final Score: 3

**💡 Remember (Пам'ятайте):** - **`score++`** те саме, що й **`score = score + 1`**
- **`score--`** те саме, що й **`score = score - 1`**

---

## Task 5: Temperature Converter (Конвертер Температури)

**Goal (Мета):** Перетворити градуси **Celsius** (`Цельсія`) на **Fahrenheit** (`Фаренгейта`).

### Instructions (Інструкції):
1.  Створіть файл під назвою **`temperature.html`**
2.  Створіть **variables** (`змінні`) для температур у градусах **Celsius**.
3.  Використовуйте **formula** (`формулу`): **`F = (C × 9/5) + 32`**
4.  Обчисліть і відобразіть обидві температури.
5.  Протестуйте щонайменше з **3** різними значеннями **Celsius**.

### Starter Code (Початковий Код):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Temperature Converter</title>
</head>
<body>
    <h1>Temperature Converter</h1>
    <h2>Celsius to Fahrenheit</h2>
    
    <p id="temp1"></p>
    <p id="temp2"></p>
    <p id="temp3"></p>
    
    <script>
        // Temperature in Celsius (Температура в градусах Цельсія)
        let celsius1 = 0;
        let celsius2 = 20;
        let celsius3 = 100;
        
        // Convert to Fahrenheit using formula: F = (C × 9/5) + 32 (Перетворити на Фаренгейт за формулою)
        let fahrenheit1 = (celsius1 * 9/5) + 32;
        let fahrenheit2 = (celsius2 * 9/5) + 32;
        // Calculate fahrenheit3 here... (Обчисліть fahrenheit3 тут...)
        
        // Display conversions (Відобразіть перетворення)
        document.getElementById('temp1').textContent = `${celsius1}°C = ${fahrenheit1}°F`;
        document.getElementById('temp2').textContent = `${celsius2}°C = ${fahrenheit2}°F`;
        // Display temp3 here... (Відобразіть temp3 тут...)
        
        console.log(`${celsius1}°C = ${fahrenheit1}°F`);
    </script>
</body>
</html>

### Example Output (Приклад Виводу):
-   0°C = 32°F
-   20°C = 68°F
-   100°C = 212°F

**💡 Hint (Підказка):** Формула містить множення, ділення **ТА** додавання, тому використовуйте **parentheses** (`дужки`), щоб переконатися, що множення/ділення відбувається першим!

---

## Task 6: Percentage Calculator (Калькулятор Відсотків)

**Goal (Мета):** Обчислити **percentages** (`відсотки`) та практикувати ділення.

### Instructions (Інструкції):
1.  Створіть файл під назвою **`percentages.html`**
2.  Створіть такі **scenarios** (`сценарії`):
    -   Ви набрали 42 з 50 балів за тест – який це відсоток?
    -   Ви правильно відповіли на 18 з 20 запитань – який це відсоток?
    -   Ви виконали 75 зі 100 завдань – який це відсоток?

3.  Відобразіть кожне обчислення з формулою та **result** (`результатом`).

### Starter Code (Початковий Код):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Percentage Calculator</title>
</head>
<body>
    <h1>Percentage Calculator</h1>
    
    <p id="test"></p>
    <p id="quiz"></p>
    <p id="tasks"></p>
    
    <script>
        // Test scenario (Сценарій тесту)
        let testScore = 42;
        let testMax = 50;
        let testPercent = (testScore / testMax) * 100;
        document.getElementById('test').textContent = `Test Score: ${testScore}/${testMax} = ${testPercent.toFixed(1)}%`;
        
        // Quiz scenario - you complete this (Сценарій вікторини - ви доповнюєте це)
        let quizScore = 18;
        let quizMax = 20;
        // Calculate quizPercent here... (Обчисліть quizPercent тут...)
        // Display quiz result here... (Відобразіть результат вікторини тут...)
        
        // Tasks scenario - you complete this (Сценарій завдань - ви доповнюєте це)
        let tasksComplete = 75;
        let tasksTotal = 100;
        // Calculate tasksPercent here... (Обчисліть tasksPercent тут...)
        // Display tasks result here... (Відобразіть результат завдань тут...)
    </script>
</body>
</html>

### Formula (Формула):
```javascript
percentage = (score / maxScore) * 100

### Expected Output (Очікуваний Вивід):
Test Score: 42/50 = 84.0%
Quiz Score: 18/20 = 90.0%
Tasks Completed: 75/100 = 75.0%

**💡 Hint (Підказка):** Використовуйте **`.toFixed(1)`**, щоб показати один знак після коми, або **`.toFixed(0)`** для цілих чисел.

---

## Task 7: Bill Splitter (Роздільник Рахунків)

**Goal (Мета):** Розділити рахунок у ресторані між друзями.

### Instructions (Інструкції):
1.  Створіть файл під назвою **`bill-split.html`**
2.  Створіть **variables** (`змінні`) для **bill amount** (`суми рахунку`), **number of people** (`кількості людей`) та **tip percentage** (`відсотка чайових`).
3.  Обчисліть **tip amount** (`суму чайових`), **total with tip** (`загальну суму з чайовими`) та **amount per person** (`суму на одну особу`).
4.  Відобразіть всі обчислення красиво відформатованими.

### Starter Code (Початковий Код):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Bill Splitter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 400px;
            margin: 50px auto;
            background-color: #f0f0f0;
            padding: 20px;
        }
        .bill {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
    <div class="bill">
        <h2>Bill Split Calculator</h2>
        <p id="bill"></p>
        <p id="tip"></p>
        <p id="total"></p>
        <hr>
        <p id="perPerson"></p>
    </div>
    
    <script>
        // Restaurant bill information (Інформація про рахунок)
        let billAmount = 125.50;
        let numberOfPeople = 4;
        let tipPercent = 0.20;  // 20% tip (20% чайових)
        
        // Calculate tip amount (bill × tip percentage) (Обчислити суму чайових)
        let tipAmount = billAmount * tipPercent;
        
        // Calculate total with tip (bill + tip) (Обчислити загальну суму з чайовими)
        let totalWithTip = billAmount + tipAmount;
        
        // Calculate per person amount (total ÷ number of people) (Обчислити суму на одну особу)
        let perPerson = totalWithTip / numberOfPeople;
        
        // Display everything (Відобразити все)
        document.getElementById('bill').textContent = `Bill Amount: $${billAmount.toFixed(2)}`;
        // Complete the tip display (show tip percentage too!) (Доповніть відображення чайових (покажіть також відсоток чайових!))
        // Complete the total display (Доповніть відображення загальної суми)
        // Complete the per person display (Доповніть відображення суми на одну особу)
        
        console.log('Tip:', tipAmount);
        console.log('Total:', totalWithTip);
        console.log('Per person:', perPerson);
    </script>
</body>
</html>

### Expected Output (Очікуваний Вивід):
Bill Split Calculator
---------------------
Bill Amount: $125.50
Tip (20%): $25.10
Total with Tip: $150.60
---------------------
Split 4 ways: $37.65 per person

**✅ Success (Успіх):** Усі суми мають бути відформатовані до 2 знаків після коми за допомогою **`.toFixed(2)`**

**💡 Challenge (Виклик):** Спробуйте змінити відсоток чайових на 15%, 18% або 25% і подивіться, як це вплине на обчислення!

---

## Task 8: Compound Operators Practice (Практика Складених Операторів)

**Goal (Мета):** Практика використання операторів **`+=`**, **`-=`**, **`*=`**, **`/=`**.
*Складені оператори — це скорочення, які поєднують арифметичну операцію (наприклад, `+`) з оператором присвоєння (`=`). Вони дозволяють змінити значення змінної на основі її поточного значення.*

### Instructions (Інструкції):
1.  Створіть файл під назвою **`compound-ops.html`**
2.  Почніть зі **variable** (`змінної`): **`let total = 100`**
3.  Виконайте ці операції **ПОСЛІДОВНО**:
    -   Додайте **50**, використовуючи **`+=`**
    -   Відніміть **25**, використовуючи **`-=`**
    -   Помножте на **2**, використовуючи **`*=`**
    -   Поділіть на **5**, використовуючи **`/=`**

4.  Відобразіть **total** (`загальну суму`) після **КОЖНОЇ** операції.

### Starter Code (Початковий Код):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Compound Operators</title>
</head>
<body>
    <h1>Compound Operators Practice</h1>
    
    <p id="start"></p>
    <p id="step1"></p>
    <p id="step2"></p>
    <p id="step3"></p>
    <p id="step4"></p>
    
    <script>
        // Starting value (Початкове значення)
        let total = 100;
        document.getElementById('start').textContent = `Starting value: ${total}`;
        
        // Step 1: Add 50 (Крок 1: Додати 50)
        total += 50;  // Same as: total = total + 50 (Те саме, що: total = total + 50)
        document.getElementById('step1').textContent = `After adding 50: ${total}`;
        
        // Step 2: Subtract 25 (Крок 2: Відняти 25)
        // Use -= here (Використовуйте -= тут)
        // Display result (Відобразіть результат)
        
        // Step 3: Multiply by 2 (Крок 3: Помножити на 2)
        // Use *= here (Використовуйте *= тут)
        // Display result (Відобразіть результат)
        
        // Step 4: Divide by 5 (Крок 4: Поділити на 5)
        // Use /= here (Використовуйте /= тут)
        // Display result (Відобразіть результат)
        
        console.log('Final total:', total);
    </script>
</body>
</html>

### Expected Output (Очікуваний Вивід):
Starting value: 100
After adding 50: 150
After subtracting 25: 125
After multiplying by 2: 250
After dividing by 5: 50

**💡 Remember (Пам'ятайте):**
- **`total += 50`** означає **`total = total + 50`**
- **`total -= 25`** означає **`total = total - 25`**
- **`total *= 2`** означає **`total = total * 2`**
- **`total /= 5`** означає **`total = total / 5`**

---

## Challenge Task: Currency Converter (Завдання-Виклик: Конвертер Валют)

**Goal (Мета):** Створити конвертер мультивалют.

### Instructions (Інструкції):
1.  Створіть файл під назвою **`currency-converter.html`**
2.  Почніть із суми в **US Dollars** (`доларах США`).
3.  Конвертуйте щонайменше в **3** інші валюти, використовуючи надані **conversion rates** (`обмінні курси`).
4.  Відобразіть усі перетворення, красиво відформатовані.
5.  Додайте **CSS** (Cascading Style Sheets, *мова для стилізації вебсторінок*), щоб зробити його професійним.

### Starter Code (Початковий Код):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Currency Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        .converter {
            background-color: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        h1 {
            color: #333;
            text-align: center;
            border-bottom: 3px solid #667eea;
            padding-bottom: 10px;
        }
        .amount {
            font-size: 24px;
            color: #667eea;
            text-align: center;
            margin: 20px 0;
        }
        .conversion {
            font-size: 18px;
            padding: 10px;
            margin: 10px 0;
            background-color: #f8f9fa;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="converter">
        <h1>Currency Converter</h1>
        <div class="amount" id="usd"></div>
        
        <p class="conversion" id="euro"></p>
        <p class="conversion" id="pound"></p>
        <p class="conversion" id="yen"></p>
        <p class="conversion" id="cad"></p>
    </div>
    
    <script>
        // Starting amount in USD (Початкова сума в USD)
        let usdAmount = 100;
        
        // Conversion rates (as of example date) (Курси обміну (на дату прикладу))
        let euroRate = 0.92;
        let poundRate = 0.79;
        let yenRate = 149.50;
        let cadRate = 1.36;
        
        // Display USD amount (Відобразити суму USD)
        document.getElementById('usd').textContent = `$${usdAmount.toFixed(2)} USD equals:`;
        
        // Convert to Euros (Конвертувати в Євро)
        let euros = usdAmount * euroRate;
        document.getElementById('euro').textContent = `€${euros.toFixed(2)} EUR`;
        
        // Convert to British Pounds (Конвертувати в Британські Фунти)
        // Calculate and display here... (Обчисліть та відобразіть тут...)
        
        // Convert to Japanese Yen (Конвертувати в Японські Єни)
        // Calculate and display here... (Обчисліть та відобразіть тут...)
        
        // Convert to Canadian Dollars (Конвертувати в Канадські Долари)
        // Calculate and display here... (Обчисліть та відобразіть тут...)
        
        console.log('USD:', usdAmount);
        console.log('EUR:', euros);
    </script>
</body>
</html>

### Example Output (Приклад Виводу):
Currency Converter
==================
$100.00 USD equals:

€92.00 EUR
£79.00 GBP
¥14,950.00 JPY
$136.00 CAD

### Bonus Challenges (Бонусні Виклики):
-   Додайте більше валют (Mexican Peso: 17.25, Indian Rupee: 83.12).
-   Покажіть **conversion rates** (`курси обміну`) на сторінці.
-   Спробуйте різні суми **USD**.
-   Додайте більше стилізації за допомогою кольорів або рамок.

### Grading Yourself (Оцінювання Себе):
-   ✅ Починається з суми **USD**
-   ✅ Конвертує щонайменше в **3** валюти
-   ✅ Усі суми правильно відформатовані за допомогою **`.toFixed(2)`**
-   ✅ Відображення чітке та організоване
-   ✅ Відсутні помилки в **console**
-   ✅ Математика правильна

---

## Challenge Task 2: Fitness Tracker (Завдання-Виклик 2: Трекер Фітнесу)

**Goal (Мета):** Відстежувати прогрес тренувань за допомогою обчислень.

### Instructions (Інструкції):
1.  Створіть файл під назвою **`fitness-tracker.html`**
2.  Відстежуйте дані тренувань за допомогою **variables** (`змінних`).
3.  Обчисліть **progress metrics** (`показники прогресу`).
4.  Відобразіть все організовано.

### Starter Code (Початковий Код):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Fitness Tracker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #e8f5e9;
        }
        .tracker {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #2e7d32;
            text-align: center;
        }
        .stat {
            padding: 10px;
            margin: 10px 0;
            background-color: #f1f8e9;
            border-left: 4px solid #66bb6a;
        }
    </style>
</head>
<body>
    <div class="tracker">
        <h1>Fitness Progress Tracker</h1>
        
        <h3>Current Stats: (Поточна статистика)</h3>
        <div class="stat" id="start"></div>
        <div class="stat" id="current"></div>
        <div class="stat" id="goal"></div>
        
        <h3>Progress: (Прогрес)</h3>
        <div class="stat" id="lost"></div>
        <div class="stat" id="remaining"></div>
        <div class="stat" id="average"></div>
        <div class="stat" id="percent"></div>
        <div class="stat" id="estimate"></div>
    </div>
    
    <script>
        // Your fitness data (Ваші дані про фітнес)
        let startWeight = 200;
        let currentWeight = 185;
        let goalWeight = 170;
        let weeksPassed = 8;
        
        // Calculate weight lost (starting weight - current weight) (Обчислити втрачену вагу)
        let weightLost = startWeight - currentWeight;
        
        // Calculate weight remaining (current weight - goal weight) (Обчислити вагу, що залишилася)
        let weightRemaining = currentWeight - goalWeight;
        
        // Calculate average loss per week (weight lost ÷ weeks passed) (Обчислити середню втрату за тиждень)
        let averageLossPerWeek = weightLost / weeksPassed;
        
        // Calculate percentage complete (weight lost ÷ total needed) × 100 (Обчислити відсоток завершення)
        let totalNeeded = startWeight - goalWeight;
        let percentComplete = (weightLost / totalNeeded) * 100;
        
        // Estimate weeks to goal (weight remaining ÷ average per week) (Оцінити тижні до мети)
        let weeksToGoal = weightRemaining / averageLossPerWeek;
        
        // Display current stats (Відобразити поточну статистику)
        document.getElementById('start').textContent = `Starting Weight: ${startWeight} lbs`;
        document.getElementById('current').textContent = `Current Weight: ${currentWeight} lbs`;
        document.getElementById('goal').textContent = `Goal Weight: ${goalWeight} lbs`;
        
        // Display progress (complete these using .toFixed() where needed) (Відобразити прогрес)
        document.getElementById('lost').textContent = `Lost: ${weightLost} lbs`;
        // Complete the remaining displays... (Доповніть решту відображень...)
        // Use .toFixed(2) for averageLossPerWeek (Використовуйте .toFixed(2) для averageLossPerWeek)
        // Use .toFixed(1) for percentComplete (Використовуйте .toFixed(1) для percentComplete)
        // Use .toFixed(1) for weeksToGoal (Використовуйте .toFixed(1) для weeksToGoal)
        
    </script>
</body>
</html>

### Expected Calculations (Очікувані Обчислення):
Fitness Progress Tracker
========================
Starting Weight: 200 lbs
Current Weight: 185 lbs
Goal Weight: 170 lbs

Progress:
- Lost: 15 lbs (Втрачено: 15 фунтів)
- Remaining: 15 lbs (Залишилося: 15 фунтів)
- Average loss: 1.88 lbs/week (Середня втрата: 1.88 фунтів/тиждень)
- Progress: 50.0% complete (Прогрес: 50.0% завершено)
- Estimated weeks to goal: 8.0 weeks (Оціночні тижні до мети: 8.0 тижнів)

### Bonus Challenges (Бонусні Виклики):
-   Обчисліть, скільки місяців залишилося до мети (тижні ÷ 4).
-   Додайте візуальний індикатор прогресу за допомогою **CSS** - *Ви можете скористатися ШІ для допомоги з цією частиною CSS.*
-   Спробуйте різні початкові значення, щоб перевірити свою математику.

---

## Tips for Success (Поради для Успіху)
1.  **Test your math manually first** (`Спочатку перевірте свої обчислення вручну`) - Використовуйте калькулятор, щоб переконатися.
2.  **Use parentheses** (`Використовуйте дужки`) - Зробіть **order of operations** (`порядок операцій`) чітким: `(a + b) / 2`.
3.  **Format currency properly** (`Правильно форматуйте валюту`) - Завжди використовуйте **`.toFixed(2)`** для грошей.
4.  **Log values** (`Записуйте значення`) - Перевіряйте свої обчислення в **console** під час роботи.
5.  **One step at a time** (`По одному кроку за раз`) - Створюйте обчислення поступово.
6.  **Check order of operations** (`Перевірте порядок операцій`) - Множення та ділення відбуваються перед додаванням та відніманням.

## Common Mistakes to Avoid (Поширені Помилки, Яких Слід Уникати)

❌ `let total = 10 + 5 * 2` (дорівнює **20**, а не **30**!)
✅ `let total = (10 + 5) * 2` (дорівнює **30**)

❌ `let price = 19.99` потім відображається `$19.9` на сторінці
✅ `let price = 19.99` потім використання `$${price.toFixed(2)}` відображає `$19.99`

❌ **Forgetting to save variable changes** (`Забуття зберегти зміни змінної`):
```javascript
let score = 0;
score + 10;  // This doesn't save! (Це не зберігає!)
✅ **Saving the change** (`Збереження зміни`):
```javascript
let score = 0;
score = score + 10;  // or score += 10;

❌ **Dividing by zero** (`Ділення на нуль`) (спричиняє `Infinity`)
✅ **Check your divisor is not zero before dividing** (`Перевірте, що ваш дільник не дорівнює нулю перед діленням`)

---

## Order of Operations (PEMDAS) (Порядок Операцій)
Пам'ятайте: **P**arentheses (Дужки), **E**xponents (Показники), **M**ultiplication (Множення), **D**ivision (Ділення), **A**ddition (Додавання), **S**ubtraction (Віднімання)

```javascript
let result1 = 10 + 5 * 2;        // = 20 (multiply first)
let result2 = (10 + 5) * 2;      // = 30 (parentheses first)
let result3 = 100 / 10 + 5;      // = 15 (divide first)
let result4 = 100 / (10 + 5);    // = 6.67 (parentheses first)

Сподіваюся, цей переклад з поясненнями технічних термінів допоможе вам! Дайте знати, якщо хочете, щоб я розпочав один із цих файлів для вас.
````