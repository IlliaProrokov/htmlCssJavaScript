Це завдання складається з практичних вправ, тому переклад буде максимально структурований, зберігаючи всі інструкції та код англійською мовою.

-----

# Завдання Уроку 02: Змінні (`Variables`) та Типи Даних (`Data Types`) 🛠️

-----

## Завдання 1: ПРИКЛАД З ІНСТРУКЦІЯМИ — Сторінка Профілю

**Виконайте наступні кроки для створення сторінки профілю, використовуючи змінні.**

### Крок 1: Створіть HTML

Створіть файл під назвою **`profile.html`**:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Profile</title>
</head>
<body>
    <h1 id="name"></h1>
    <p id="bio"></p>
    <p id="details"></p>
    
    <script>
        // Store profile information in variables
        let firstName = "Alex";
        let lastName = "Johnson";
        let age = 20;
        let city = "Seattle";
        let isStudent = true;
        
        // Display the full name
        document.getElementById('name').textContent = `${firstName} ${lastName}`;
        
        // Display bio
        document.getElementById('bio').textContent = `I am ${age} years old and live in ${city}.`;
        
        // Display student status
        document.getElementById('details').textContent = `Student: ${isStudent}`;
        
        // Also log everything to console
        console.log('Name:', firstName, lastName);
        console.log('Age:', age);
        console.log('City:', city);
        console.log('Is Student:', isStudent);
    </script>
</body>
</html>
```

### Крок 2: Перевірте

1.  Відкрийте файл у вашому браузері
2.  Ви повинні побачити інформацію профілю
3.  Відкрийте консоль (F12), щоб побачити залогіровані дані

### Крок 3: Змініть

Тепер змініть значення змінних на **вашу власну інформацію**:

  * Змініть `firstName` на ваше ім'я
  * Змініть `lastName` на ваше прізвище
  * Змініть інші змінні відповідно до вашої інформації
  * Збережіть та оновіть сторінку, щоб побачити зміни

**Контрольна Точка:** Сторінка повинна відображати **ВАШУ** інформацію.

-----

## Завдання 2: Практика Типів Даних (`Data Types`)

**Мета:** Попрактикуватися у створенні змінних з різними типами даних.

### Інструкції:

1.  Створіть файл під назвою **`data-types.html`**

2.  Створіть вебсторінку, використовуючи початковий код нижче.

3.  Використовуючи Javascript, створіть змінні для:
       - Вашої улюбленої їжі (**string**)
       - Вашого щасливого числа (**number**)
       - Чи подобається вам піца (**boolean**)
       - Вашої мрії (роботи) (**string**)
       - Кількість ваших братів і сестер (**number**)

4.  Залогіруйте кожну змінну у консоль із підписом

5.  Використовуйте **`typeof`** для перевірки та логування **типу даних** кожної змінної

### Початковий Код (`Starter Code`):

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Data Types Practice</title>
</head>
<body>
    <h1>Data Types Practice</h1>
    <p>Check the console (F12) to see your output!</p>
    
    <script>
        // Create your variables here
        let favoriteFood = "Pizza";
        let luckyNumber = 7;
        let likesPizza = true;
        let dreamJob = ""; // Fill this in
        let numSiblings = 0; // Fill this in
        
        // Log each variable with a label
        console.log("Favorite food:", favoriteFood);
        console.log("Type:", typeof favoriteFood);
        
        console.log("Lucky number:", luckyNumber);
        console.log("Type:", typeof luckyNumber);
        
        // Add the rest of your console.log statements here
        
    </script>
</body>
</html>
```

### Очікуваний Вивід у Консолі:

```
Favorite food: Pizza
Type: string
Lucky number: 7
Type: number
Likes pizza: true
Type: boolean
Dream job: Barber
Type: string
Number of siblings: 2
Type: number
```

-----

## Завдання 3: Виклик Конкатенації Рядків (`String Concatenation Challenge`)

**Мета:** Попрактикуватися в об'єднанні рядків.

### Інструкції:

1.  Створіть файл під назвою **`story.html`**

2.  Створіть такі змінні:
       - **`character`** (ім'я персонажа)
       - **`place`** (місцезнаходження)
       - **`item`** (об'єкт)
       - **`action`** (дієслово, наприклад "ran", "jumped", "found")

3.  Використовуйте **конкатенацію (`+`)**, щоб створити речення та відобразити його в елементі `h1`

4.  Використовуйте **шаблонний літерал** (`template literal`), щоб створити інше речення та відобразити його в елементі `p`

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Story Builder</title>
</head>
<body>
    <h1 id="sentence1"></h1>
    <p id="sentence2"></p>
    
    <script>
        // Create your variables here
        let character = "Luna";
        let place = "forest";
        let item = "key";
        let action = "discovered";
        
        // Use + to concatenate (join strings together)
        let firstSentence = character + " went to the " + place + ".";
        document.getElementById('sentence1').textContent = firstSentence;
        
        // Use template literals with ${}
        let secondSentence = `She ${action} a magical ${item}!`;
        document.getElementById('sentence2').textContent = secondSentence;
    </script>
</body>
</html>
```

-----

## Завдання 4: Відображення Особистої Інформації

**Мета:** Створити відформатоване відображення інформації.

### Інструкції:

1.  Створіть файл під назвою **`info-card.html`**

2.  Створіть змінні для:
       - Повного імені (`Full name`)
       - Електронної адреси (`Email address`)
       - Номеру телефону (`Phone number`)
       - Міста (`City`)
       - Улюбленого хобі (`Favorite hobby`)

3.  Використовуйте JavaScript, щоб заповнити кожен параграф відформатованою інформацією

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Info Card</title>
</head>
<body>
    <h1>Personal Information</h1>
    
        <p id="name"></p>
    <p id="email"></p>
    <p id="phone"></p>
    <p id="location"></p>
    <p id="hobby"></p>
    
    <script>
        // Create your variables here
        let fullName = "Your Name Here";
        let emailAddress = "your.email@example.com";
        let phoneNumber = "555-0123";
        let city = "Your City";
        let favoriteHobby = "Your Hobby";
        
        // Use template literals to format and display
        document.getElementById('name').textContent = `Name: ${fullName}`;
        document.getElementById('email').textContent = `Email: ${emailAddress}`;
        
        // Complete the rest here...
        
    </script>
</body>
</html>
```

### Очікуваний Формат Виводу:

```
Name: [Your Name]
Email: [Your Email]
Phone: [Your Phone]
Location: [Your City]
Hobby: [Your Hobby]
```

-----

## Завдання 5: Переприсвоєння Змінних (`Variable Reassignment`)

**Мета:** Зрозуміти, як змінні `let` можуть змінюватися.

### Інструкції:

1.  Створіть файл під назвою **`counter.html`**
2.  Створіть змінну **`score`** і встановіть її значення на **0**
3.  Створіть три елементи `h2` з **`id`**
4.  Відобразіть початковий рахунок на сторінці
5.  Залогіруйте рахунок у консоль
6.  **Додайте 10** до рахунку
7.  Відобразіть оновлений рахунок
8.  Залогіруйте оновлений рахунок у консоль
9.  **Додайте ще 5** до рахунку
10. Відобразіть та залогіруйте фінальний рахунок

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Variable Reassignment</title>
</head>
<body>
    <h1>Score Tracker</h1>
    
    <h2 id="initial"></h2>
    <h2 id="updated"></h2>
    <h2 id="final"></h2>
    
    <script>
        // Step 1: Create score variable
        let score = 0;
        
        // Step 2: Display and log initial score
        document.getElementById("initial").textContent = "Initial score: " + score;
        console.log("Score:", score);
        
        // Step 3: Add 10 to score
        score += 10;  // This means score = score + 10
        
        // Step 4: Display and log updated score
        // Your code here...
        
        // Step 5: Add 5 more to score
        // Your code here...
        
        // Step 6: Display and log final score
        // Your code here...
    </script>
</body>
</html>
```

### Очікуваний Вивід на Сторінці:

```
Initial score: 0
Updated score: 10
Final score: 15
```

### Очікуваний Вивід у Консолі:

```
Score: 0
Score: 10
Score: 15
```

-----

## Завдання 6: `Const` проти `Let`

**Мета:** Зрозуміти різницю між `const` та `let`.

### Інструкції:

1.  Створіть файл під назвою **`constants.html`**

2.  Створіть такі змінні:
       - Використовуйте **`const`** для: `birthYear`, `hometown`, `schoolName`
       - Використовуйте **`let`** для: `currentYear`, `age`, `grade`

3.  Спробуйте змінити змінну **`const`**

4.  Подивіться на **помилку в консолі**

5.  **Закоментуйте** цей рядок (помилковий)

6.  Змініть змінні **`let`** та відобразіть їх

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Const vs Let</title>
</head>
<body>
    <h1>Understanding Const and Let</h1>
    <div id="output"></div>
    
    <script>
        // Use const for values that won't change
        const birthYear = 2005;  // Your birth year never changes
        const hometown = "Springfield";  // Where you were born doesn't change
        const schoolName = "Central High";
        
        // Use let for values that will change
        let currentYear = 2025;  // The year keeps changing
        let age = 20;  // Your age changes every year
        let grade = 10;  // Your grade changes
        
        // Try to change a const - this will cause an ERROR!
        // birthYear = 2006;  // Uncomment this line to see the error
        
        // Changing let variables is fine
        age = 21;
        grade = 11;
        
        // Display the information
        let info = `
            Birth Year: ${birthYear} (const - cannot change)<br>
            Hometown: ${hometown} (const - cannot change)<br>
            Current Age: ${age} (let - can change)<br>
            Current Grade: ${grade} (let - can change)
        `;
        
        document.getElementById('output').innerHTML = info;
        
        console.log("Birth Year:", birthYear);
        console.log("Age:", age);
    </script>
</body>
</html>
```

### Завдання:

Напишіть **коментарі**, пояснюючи, чому ви використали `const` для одних змінних і `let` для інших.

-----

## Завдання 7: Зневадження Змінних (`Debug the Variables`) 🐛

**Мета:** Знайти та виправити помилки зі змінними.

### Інструкції:

1.  Створіть файл під назвою **`debug-variables.html`**
2.  Скопіюйте цей код (у ньому є помилки\!):

<!-- end list -->

```html
<!DOCTYPE html>
<html>
<head>
    <title>Debug Practice</title>
</head>
<body>
    <h1 id="output"></h1>
    
    <script>
        // Fix the errors in this code!
        let first name = "Emma";
        let age = "25;
        const favoriteColor = "blue";
        let 2ndPlace = "silver";
        
        favoriteColor = "red";
        
        let message = `${firstName} is ${age} years old`;
        document.getElementById('output').textContent = message;
        
        console.log(message);
    </script>
</body>
</html>
```

3.  Знайдіть і виправте **УСІ** помилки
4.  Код повинен запускатися без помилок у консолі

### Помилки, які потрібно знайти (всього 5):

  * ❌ Помилка іменування змінної (пробіли заборонені)
  * ❌ Помилка з лапками рядка (невідповідність лапок)
  * ❌ Помилка переприсвоєння `const` (не можна змінювати `const`)
  * ❌ Помилка іменування змінної (не може починатися з числа)
  * ❌ Помилка невизначеної змінної (одрук у назві змінної)

**Успіх:** Сторінка відображає "Emma is 25 years old" без помилок у консолі.

-----

## Додаткове Завдання: Генератор Mad Lib 🃏

**Мета:** Створити історію Mad Lib, використовуючи змінні.

### Інструкції:

1.  Створіть **`madlib.html`**
2.  Створіть **щонайменше 8 змінних** для різних типів слів
3.  Створіть кумедну історію, використовуючи всі змінні
4.  Відобразіть історію на сторінці з належним форматуванням

### Початковий Код:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Mad Lib Story</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f0f8ff;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
        }
        .story {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            line-height: 1.6;
        }
    </style>
</head>
<body>
    <h1>My Mad Lib Story</h1>
    <div class="story" id="storyOutput"></div>
    
    <script>
        // CHANGE THESE variables to make them your own
        const adjective = "sparkly";
        const noun = "banana";
        const verb = "danced";
        const place = "the moon";
        const animal = "penguin";
        const number = 42;
        const color = "purple";
        const personName = "Bob";
        
        // Create your OWN NEW story using template literals.  Example: 
        let story = `
            <p>Once upon a time, ${personName} went to ${place} and saw a 
            ${color} ${animal}.</p>
            
            <p>The ${animal} ${verb} over to a ${adjective} ${noun} and 
            counted to ${number}.</p>
            
            <p>It was very ${adjective}!</p>
        `;
        
        // Display the story
        document.getElementById('storyOutput').innerHTML = story;
        
        // Also log to console
        console.log("Story:", story);
    </script>
</body>
</html>
```

-----

## Повна Відповідь для Завдання 5:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Variable Reassignment</title>
</head>
<body>
    <h1>Task 5: Variable Reassignment</h1>

        <h2 id="initial"></h2>
    <h2 id="updated"></h2>
    <h2 id="final"></h2>

    <script>
        // Step 1: Create a variable called score and set it to 0
        let score = 0;

        // Step 2: Display the initial score and log to console
        document.getElementById("initial").textContent = "Initial score: " + score;
        console.log("Score:", score);

        // Step 3: Add 10 to the score
        score += 10;

        // Step 4: Display the updated score and log to console
        document.getElementById("updated").textContent = "Updated score: " + score;
        console.log("Score:", score);

        // Step 5: Add 5 more to the score
        score += 5;

        // Step 6: Display the final score and log to console
        document.getElementById("final").textContent = "Final score: " + score;
        console.log("Score:", score);
    </script>
</body>
</html>
```

-----

Бажаєте, щоб я переклав наступний урок (про математичні операції) у такому ж форматі?