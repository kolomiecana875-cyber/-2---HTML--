# Завдання 3 - Реалізація HTML-сторінки зі списком визначень та виносками

## Опис завдання

Створити HTML-сторінку зі списком визначень та виносками. Сторінку стилізувати так, як показано на зображенні нижче.

## Структура проекту

```
task-03/
├── index.html
└── style.css
```

## Покрокова інструкція

### 1. Створення базової структури HTML

- Створіть файл `index.html`
- Встановіть заголовок сторінки "HTML Terms Definitions"
- Додайте базову структуру HTML-документа (doctype, html, head, body)
- Підключіть файл стилів style.css

### 2. Створення контейнера для списку визначень

- Створіть контейнер для всього контенту з класом "container"
- Використовуйте теги `<dl>` (definition list), `<dt>` (definition term) та `<dd>` (definition description) для створення списку визначень

### 3. Додавання термінів та їх визначень

Додайте наступні терміни та їх визначення:

1. **TAG**

   - Визначення: "In information systems, a tag is a keyword or term assigned to a piece of information (such as an Internet bookmark, digital image, database record, or computer file). This kind of metadata helps describe an item and allows it to be found again by browsing or searching.[1] Tags are generally chosen informally and personally by the item's creator or by its viewer, depending on the system, although they may also be chosen from a controlled vocabulary.[2]"

2. **ATTRIBUTE**

   - Визначення: "HTML attributes are special words used inside the opening tag to control the element's behaviour. HTML attributes are a modifier of an HTML element type. An attribute either modifies the default functionality of an element type or provides functionality to certain element types unable to function correctly without them. In HTML syntax, an attribute is added to an HTML start tag."

3. **ELEMENT**
   - Визначення: "An HTML element is an individual component of an HTML (Hypertext Markup Language) document or web page.[vague] HTML is composed of a tree of HTML nodes, such as text nodes. Each node can have HTML attributes specified. Nodes can also have content, including other nodes and text. Many HTML nodes represent semantics, or meaning. For example, the <title> node represents the title of the document."

### 4. Додавання виносок

Додайте виноски в кінці документа:

1. [1] Some users, however, see tags not as metadata but as "just more content": Berendt, Bettina; Hanser, Christoph (2007). "Tags are not metadata, but 'just more content'—to some people" (PDF). Proceedings of the International Conference on Weblogs and Social Media (ICWSM), Boulder, Colorado, USA, March 26–28, 2007. Menlo Park, CA: International Joint Conferences on Artificial Intelligence. OCLC 799635928.

2. [2] Smith, Gene (2008). Tagging: people-powered metadata for the social web. Berkeley: New Riders Press. ISBN 9780321529176. OCLC 154806677.

### 5. Додавання стилів (CSS)

У файлі `style.css` створіть стилі.

### 6. Налаштування посилань на виноски

- Додайте до визначень посилання на виноски, використовуючи теги `<sup>` та `<a>` з відповідними ідентифікаторами
- Створіть розділ для виносок з класом "footnotes"
- Додайте ідентифікатори до виносок, щоб можна було на них посилатися

## Вимоги до форматування

- Використання списку визначень (`<dl>`, `<dt>`, `<dd>`) для структурування термінів та їх визначень
- Стилізація термінів:
  - Темно-синій фон для термінів
  - Білий колір тексту для термінів
  - Великі літери для термінів
- Стилізація визначень:
  - Світло-блакитний фон для визначень
  - Вирівнювання тексту визначень по ширині
- Стилізація виносок:
  - Розділення виносок від основного контенту горизонтальною лінією
  - Менший розмір шрифту для виносок
  - Правильне форматування посилань на виноски у верхньому індексі

## Результат

Після виконання всіх кроків ви отримаєте HTML-сторінку зі списком визначень та виносками, яка має:

- Чітко структуровані терміни та їх визначення
- Стилізований вигляд з кольоровим оформленням
- Правильно оформлені виноски з посиланнями
- Семантично коректну структуру документа
