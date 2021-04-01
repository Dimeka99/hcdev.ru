---
description: Свойство border-spacing задаёт расстояние между границами ячеек в таблице
---

# border-spacing

Свойство **`border-spacing`** задаёт расстояние между границами ячеек в таблице.

`border-spacing` не работает в случае, когда для таблицы установлено свойство [`border-collapse`](border-collapse.md) со значением `collapse`.

??? info "Колонки и таблицы"

    <div class="col3" markdown="1">

    - [column-count](column-count.md)
    - [column-fill](column-fill.md)
    - [column-gap](column-gap.md)
    - [column-rule](column-rule.md)
    - [column-rule-color](column-rule-color.md)
    - [column-rule-style](column-rule-style.md)
    - [column-rule-width](column-rule-width.md)
    - [column-span](column-span.md)
    - [column-width](column-width.md)
    - [columns](columns.md)

    </div>

    <div class="col3" markdown="1">

    - [border-collapse](border-collapse.md)
    - **border-spacing**
    - [caption-side](caption-side.md)
    - [empty-cells](empty-cells.md)
    - [table-layout](table-layout.md)
    - [vertical-align](vertical-align.md)

    </div>

## Синтаксис

```css
/* <length> */
border-spacing: 2px;

/* horizontal <length> | vertical <length> */
border-spacing: 1cm 2em;

/* Global values */
border-spacing: inherit;
border-spacing: initial;
border-spacing: unset;
```

## Значения

Одно значение устанавливает одновременно расстояние по вертикали и горизонтали между границами ячеек. Если значений два, то первое определяет горизонтальное расстояние, а второе — вертикальное.

### Примечание

Если к элементу [`<table>`](../html/table.md) добавлен атрибут `cellspacing`, то при использовании стилевого свойства `border-spacing` атрибут `cellspacing` не принимается во внимание и его значение игнорируется.

Значение по-умолчанию:

```css
border-spacing: 0;
```

Применяется к таблицам

## Спецификации

- [CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/tables.html#separated-borders)

## Описание и примеры

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>border-spacing</title>
    <style>
      table {
        border: 4px double #333; /* Рамка вокруг таблицы */
        border-collapse: separate; /* Способ отображения границы */
        width: 100%; /* Ширина таблицы */
        border-spacing: 7px 11px; /* Расстояние между ячейками */
      }
      td {
        padding: 5px; /* Поля вокруг текста */
        border: 1px solid #a52a2a; /* Граница вокруг ячеек */
      }
    </style>
  </head>
  <body>
    <table>
      <tr>
        <td>1</td>
        <td>2</td>
      </tr>
      <tr>
        <td>3</td>
        <td>4</td>
      </tr>
    </table>
  </body>
</html>
```
