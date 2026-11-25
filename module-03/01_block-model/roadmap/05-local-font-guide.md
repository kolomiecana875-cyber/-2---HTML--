# Інструкція з підключення локального шрифту

## Крок 1: Створення структури файлів

1. Створіть папку `fonts` у корені вашого проєкту
2. Помістіть файли шрифтів у цю папку

Приклад структури:
```
project/
├── fonts/
│   ├── MyFont-Regular.woff2
│   ├── MyFont-Regular.woff
│   ├── MyFont-Bold.woff2
│   └── MyFont-Bold.woff
├── css/
│   └── style.css
└── index.html
```

## Крок 2: Підключення шрифту через @font-face

У вашому CSS файлі (наприклад, `style.css`):

```css
@font-face {
    font-family: 'MyFont';  /* Назва, яку ви будете використовувати */
    src: url('../fonts/MyFont-Regular.woff2') format('woff2'),
         url('../fonts/MyFont-Regular.woff') format('woff');
    font-weight: 400;  /* Звичайна вага шрифту */
    font-style: normal;
}

/* Якщо у вас є жирне накреслення */
@font-face {
    font-family: 'MyFont';
    src: url('../fonts/MyFont-Bold.woff2') format('woff2'),
         url('../fonts/MyFont-Bold.woff') format('woff');
    font-weight: 700;  /* Жирний шрифт */
    font-style: normal;
}
```

## Крок 3: Використання шрифту

```css
body {
    font-family: 'MyFont', Arial, sans-serif;
}

/* Для жирного тексту */
strong {
    font-weight: 700;
}
```

## Важливі примітки:

1. **Формати файлів**
   - `.woff2` - найновіший формат, найкраща компресія
   - `.woff` - хороша підтримка браузерами
   - Вказуйте `.woff2` першим для кращої продуктивності

2. **Шляхи до файлів**
   - Використовуйте відносні шляхи
   - Перевірте правильність шляхів відносно CSS файлу

3. **Оптимізація**
   - Використовуйте тільки потрібні накреслення
   - Конвертуйте шрифти у WOFF2 та WOFF формати
   - Видаліть невикористовувані символи для зменшення розміру

4. **Fallback шрифти**
   - Завжди вказуйте альтернативні системні шрифти
   - Враховуйте схожість з вашим основним шрифтом

## Приклад повного коду

```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мій сайт</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <h1>Заголовок з моїм шрифтом</h1>
    <p>Звичайний текст з моїм шрифтом</p>
    <p><strong>Жирний текст з моїм шрифтом</strong></p>
</body>
</html>
```

```css
/* style.css */
@font-face {
    font-family: 'MyFont';
    src: url('../fonts/MyFont-Regular.woff2') format('woff2'),
         url('../fonts/MyFont-Regular.woff') format('woff');
    font-weight: 400;
    font-style: normal;
    font-display: swap; /* Для кращого відображення під час завантаження */
}

@font-face {
    font-family: 'MyFont';
    src: url('../fonts/MyFont-Bold.woff2') format('woff2'),
         url('../fonts/MyFont-Bold.woff') format('woff');
    font-weight: 700;
    font-style: normal;
    font-display: swap;
}

body {
    font-family: 'MyFont', Arial, sans-serif;
    font-weight: 400;
}

h1 {
    font-weight: 700;
}

strong {
    font-weight: 700;
}
```

## Перевірка роботи

1. Відкрийте сайт у різних браузерах
2. Перевірте, чи коректно відображаються всі накреслення
3. Перевірте швидкість завантаження через інструменти розробника

## Поширені помилки

1. ❌ Неправильні шляхи до файлів
2. ❌ Відсутні fallback шрифти
3. ❌ Використання застарілих форматів (ttf, eot)
4. ❌ Завантаження всіх можливих накреслень

## Рекомендації

1. ✅ Використовуйте сучасні формати (woff2, woff)
2. ✅ Оптимізуйте розмір файлів шрифтів
3. ✅ Додавайте font-display для кращого UX
4. ✅ Тестуйте в різних браузерах
