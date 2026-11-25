# Властивості оформлення блоків у CSS

## Базова структура для прикладів

```html
<div class="example-block">Блочний елемент</div>
<span class="example-string">Рядковий елемент</span>
```

## Границі (border)

### Основний синтаксис

```css
.element {
  border: 1px solid #000; /* товщина стиль колір */
}
```

### Стилі границь

- `solid` - суцільна лінія
- `dotted` - крапками
- `dashed` - пунктирна
- `double` - дві лінії
- `groove` - змішана лінія
- `ridge` - змішана лінія
- `inset` - змішана лінія
- `outset` - змішана лінія

### Окремі сторони

```css
.element {
  border-top: 2px solid red; /* верхня границя */
  border-right: 2px solid blue; /* права границя */
  border-bottom: 2px solid green; /* нижня границя */
  border-left: 2px solid yellow; /* ліва границя */
}
```

### Скруглення кутів (border-radius)

```css
.element {
  border-radius: 10px; /* всі кути однаково */
  border-radius: 10px 20px 30px 40px; /* за годинниковою стрілкою */
  border-radius: 50%; /* створення кола */
}
```

```css
.element {
  border-radius: 10px 0 0 10px; /* верхні ліві */
  border-radius: 0 10px 10px 0; /* верхні праві */
  border-radius: 0 0 10px 10px; /* нижні праві */
  border-radius: 10px 10px 0 0; /* нижні ліві */
}
```

```css
.element {
  border-radius: 50% 0 0 50%; /* верхні ліві */
  border-radius: 0 50% 50% 0; /* верхні праві */
  border-radius: 0 0 50% 50%; /* нижні праві */
  border-radius: 50% 50% 0 0; /* нижні ліві */
}
```

```css
.element {
  border-radius-top-left: 10px; /* верхній лівий кут  */
  border-radius-top-right: 10px; /* верхній правий кут */
  border-radius-bottom-right: 10px; /* нижній правий кут */
  border-radius-bottom-left: 10px; /* нижній лівий кут */
}
```

## Зовнішня границя (outline)

```css
.element {
  outline: 2px solid red;
}
```

```css
.element {
  outline: 2px solid red;
  outline-offset: 5px;
}
```

```css
.element {
  outline: 2px solid red;
  outline-offset: -5px;
}
```

```css
.element {
  outline: 2px solid red;
  outline-offset: 5px;
  outline-style: double;
}
```

```css
.element {
  outline-offset: 5px;
  outline-style: dotted;
  outline-color: blue;
}
```

### Особливості outline:

- Не впливає на розміри елемента
- Не можна задати для окремих сторін
- Не підтримує border-radius
- Розташовується за межами border

## Тіні (box-shadow)

```css
.element {
  /* зсув-X зсув-Y розмиття розширення колір */
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);

  /* Внутрішня тінь */
  box-shadow: inset 0 0 10px #000;

  /* Множинні тіні */
  box-shadow: 5px 5px 10px black, inset 0 0 5px red;
}
```

## Прозорість (opacity)

```css
.element {
  opacity: 1; /* повністю видимий */
  opacity: 0.5; /* напівпрозорий */
  opacity: 0; /* повністю прозорий */
}
```

### Особливості opacity:

- Значення від 0 до 1
- Впливає на весь елемент та його вміст
- Елемент залишається інтерактивним
- Можна анімувати

## Видимість (visibility)

```css
.element {
  visibility: visible; /* видимий (за замовчуванням) */
  visibility: hidden; /* прихований */
}
```

### Порівняння методів приховування

| Властивість        | Займає місце | Інтерактивність | Анімація |
| ------------------ | ------------ | --------------- | -------- |
| display: none      | Ні           | Ні              | Ні       |
| opacity: 0         | Так          | Так             | Так      |
| visibility: hidden | Так          | Ні              | Так      |

## Особливості для різних типів елементів

### Блочні елементи

- Всі властивості працюють як очікується
- Можна комбінувати різні ефекти

### Рядкові елементи

- `border` може виглядати неочікувано
- `outline` огортає текст по контуру
- `border-radius` працює обмежено

### Зображення

- Всі властивості працюють добре
- Часто використовується для створення круглих аватарок

## Приклади використання

### Картка з тінню

```css
.card {
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
}
```

### Круглий аватар

```css
.avatar {
  border-radius: 50%;
  border: 3px solid white;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}
```

### Кнопка з ефектами

```css
.button {
  border: none;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  transition: opacity 0.3s;
}

.button:hover {
  opacity: 0.8;
}
```

> **Порада**: Використовуйте комбінації властивостей для створення цікавих візуальних ефектів, але пам'ятайте про продуктивність та зручність використання.
