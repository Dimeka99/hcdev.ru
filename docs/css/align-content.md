---
description: Свойство align-content задаёт тип выравнивания строк внутри флекс-контейнера по поперечной оси при наличии свободного пространства
---

# align-content

Свойство **`align-content`** задаёт тип выравнивания строк внутри флекс-контейнера по поперечной оси при наличии свободного пространства.

## Демо

<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/align-content.html" title="MDN Web Docs Interactive Example" loading="lazy" data-readystate="complete"></iframe>

Это свойство не влияет на однострочные flex-контейнеры (т. е. с `flex-wrap: nowrap`).

??? info "Flexbox и выравнивание"

    <div class="col3" markdown="1">

    - [flex](flex.md)
    - [flex-basis](flex-basis.md)
    - [flex-direction](flex-direction.md)
    - [flex-flow](flex-flow.md)
    - [flex-grow](flex-grow.md)
    - [flex-shrink](flex-shrink.md)
    - [flex-wrap](flex-wrap.md)
    - [order](order.md)

    </div>

    <div class="col3" markdown="1">

    - [justify-content](justify-content.md)
    - **align-content**
    - [place-content](place-content.md)
    - [justify-items](justify-items.md)
    - [align-items](align-items.md)
    - [place-items](place-items.md)
    - [justify-self](justify-self.md)
    - [align-self](align-self.md)
    - [place-self](place-self.md)
    - [row-gap](row-gap.md)
    - [column-gap](column-gap.md)
    - [gap](gap.md)

    </div>

## Синтаксис

```css
/* Positional alignment */
align-content: center; /* Pack items around the center */
align-content: start; /* Pack items from the start */
align-content: end; /* Pack items from the end */
align-content: flex-start; /* Pack flex items from the start */
align-content: flex-end; /* Pack flex items from the end */
align-content: left; /* Pack items from the left */
align-content: right; /* Pack items from the right */

/* Baseline alignment */
align-content: baseline;
align-content: first baseline;
align-content: last baseline;

/* Distributed alignment */

/* Distribute items evenly
The first item is flush with the start,
the last is flush with the end */
align-content: space-between;

/* Distribute items evenly
Items have a half-size space
on either end */
align-content: space-around;

/* Distribute items evenly
Items have equal space around them */
align-content: space-evenly;

/* Distribute items evenly
Stretch 'auto'-sized items to fit
the container */
align-content: stretch;

/* Overflow alignment */
align-content: safe center;
align-content: unsafe center;

/* Global values */
align-content: inherit;
align-content: initial;
align-content: unset;
```

## Значения

Значение по-умолчанию: `stretch`

Применяется к флекс-контейнеру

<table>
<thead>
<tr class="header"><th>Значение</th><th>Положение</th><th>Описание</th></tr>
</thead>
<tbody>
<tr><td><code>flex-start</code></td><td><img src="/css/flex-start.png" alt="flex-start" /></td><td>Строки располагаются в начале поперечной оси. Каждая следующая строка идёт вровень с предыдущей.</td></tr>
<tr><td><code>center</code></td><td><img src="/css/flex-center.png" alt="center"/></td><td>Строки располагаются по центру контейнера.</td></tr>
<tr><td><code>flex-end</code></td><td><img src="/css/flex-end.png" alt="flex-end" /></td><td>Строки располагаются начиная с конца поперечной оси. Каждая предыдущая строка идёт вровень со следующей.</td></tr>
<tr><td><code>space-between</code></td><td><img src="/css/space-between.png" alt="space-between" /></td><td>Строки равномерно распределяются в контейнере и расстояние между ними одинаково.</td></tr>
<tr><td><code>space-around</code></td><td><img src="/css/space-around.png" alt="space-around" /></td><td>Строки равномерно распределяются таким образом, чтобы пространство между двумя соседними строками было одинаковым. Пустое пространство перед первой строкой и после последней строки равно половине пространства между двумя соседними строками.</td></tr>
<tr><td><code>stretch</code></td><td><img src="/css/stretch.png" alt="stretch" /></td><td>Строки равномерно растягиваются, заполняя свободное пространство.</td></tr>
</tbody>
</table>

## Спецификации

- [CSS Flexible Box Layout Module](https://www.w3.org/TR/css-flexbox/#propdef-align-content)

## Поддержка браузерами

<p class="ciu_embed" data-feature="flexbox" data-periods="future_1,current,past_1,past_2"></p>

## Пример

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>align-content</title>
    <style>
      .flex-container {
        width: 70px;
        height: 240px;
        border: 1px solid #333;
        padding: 10px;
        display: flex;
        flex-wrap: wrap;
        align-content: center;
      }
      .flex-container div {
        width: 70px;
        height: 70px;
        border-radius: 50%;
      }
      .red {
        background: red;
      }
      .yellow {
        background: yellow;
      }
      .green {
        background: green;
      }
    </style>
  </head>
  <body>
    <div class="flex-container">
      <div class="red"></div>
      <div class="yellow"></div>
      <div class="green"></div>
    </div>
  </body>
</html>
```

## Примечание

Safari до версии 9 поддерживает свойство `-webkit-align-content`.

## Ссылки

- Свойство [`align-content`](https://developer.mozilla.org/ru/docs/Web/CSS/align-content) <sup><small>MDN (рус.)</small></sup>
