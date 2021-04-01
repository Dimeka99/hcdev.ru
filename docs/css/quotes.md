---
description: Свойство quotes устанавливает тип кавычек, который применяется в тексте документа
---

# quotes

Свойство **`quotes`** устанавливает тип кавычек, который применяется в тексте документа.

В каждом языке существуют свои традиции для обозначения кавычек, свойство `quotes` позволяет задать вид их отображения по всему тексту и установить, таким образом, его единообразное оформление. Добавление кавычек происходит автоматически для содержимого контейнера [`<q>`](/html/q/), а также для текста, к которому применяется стилевое свойство [`content`](content.md) со значением `open-quote` (открывающая кавычка) или `close-quote` (закрывающая кавычка).

??? info "Списки, счетчики, генерируемый контент"

    <div class="col3" markdown="1">

    - [counter-increment](counter-increment.md)
    - [counter-reset](counter-reset.md)
    - [list-style-image](list-style-image.md)
    - [list-style-type](list-style-type.md)
    - [list-style-position](list-style-position.md)
    - [list-style](list-style.md)

    </div>

    <div class="col3" markdown="1">

    - [content](content.md)
    - **quotes**

    </div>

## Синтаксис

```css
/* Keyword value */
quotes: none;

/* <string> values */
quotes: '«' '»'; /* Set open-quote and close-quote to the French quotation marks */
quotes: '«' '»' '‹' '›'; /* Set two levels of quotation marks */

/* Global values */
quotes: inherit;
quotes: initial;
quotes: unset;
```

## Значения

- В качестве значения используется символ текста (например, `quotes: "«" "»"`) или символ юникода.
- `none` — Кавычки не добавляются.

Значение по-умолчанию зависит от браузера, его настроек и операционной системы

Применяется ко всем элементам

## Спецификации

- [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/generate.html#quotes)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>quotes</title>
    <style>
      q {
        font-family: Times, serif; /* Шрифт с засечками */
        font-style: italic; /* Курсивное начертание текста */
        color: navy; /* Синий цвет текста */
        quotes: '«' '»'; /* Кавычки в виде двойных угловых скобок */
      }
    </style>
  </head>
  <body>
    <p>
      Станислав Лец утверждал:
      <q>Чаще всего выход там, где был вход</q>.
    </p>
  </body>
</html>
```
