---
description: namespace - это правила определяющие пространства имён XML, которые будут использованы в таблице стилей
---

# @namespace

**`@namespace`** - это правила определяющие пространства имён XML, которые будут использованы в таблице стилей. Они применяются чтобы ограничить CSS селекторы только элементами принадлежащими конкретному пространству имён. Namespace'ы полезны, в основном, когда идёт взаимодействие с документами содержащими множество неймспейсов, такими как HTML5 со встроенным SVG, MathML или XML.

??? info "@-правила"

    <div class="col3" markdown="1">

    - [@charset](charset.md)
    - [@import](import.md)
    - **@namespace**
    - [@media](media.md)
    - [@supports](supports.md)
    - [@document](document.md)
    - [@page](page.md)
    - [@font-face](font-face.md)
    - [@keyframes](keyframes.md)
    - [@viewport](viewport.md)
    - [@counter-style](counter-style.md)
    - [@font-feature-values](font-feature-values.md)

    </div>

## Синтаксис

```css
@namespace url('http://www.w3.org/1999/xhtml');
@namespace svg url('http://www.w3.org/2000/svg');

/* This matches all XHTML <a> elements, as XHTML is the default unprefixed namespace */
a {
}

/* This matches all SVG <a> elements */
svg|a {
}

/* This matches both XHTML and SVG <a> elements */
*|a {
}
```

## Описание

Любое `@namespace` правило обязано следовать всем [`@charset`](charset.md) и [`@import`](import.md) правилам, а так же всем описаниям стилей в таблице стилей.

`@namespace` может быть использован для определения стандартного пространства имён для конкретной таблице стилей. Когда стандартное пространство имён определено, все селекторы (но не атрибуты селекторов) применяются только к элементам в этом неймспейсе.

!!! warn "Заметка"

    В XML, если префикс отличается от атрибута (Например, `xlink:href`), то аттрибут не будет иметь неймспейса. Другими словами, аттрибуты не могут наследовать пространство имён элемента в котором они находятся.

`@namespace` правила можно использовать для определения префиксов имён. Когда селектор имеет префикс, он будет выбирать элементы совпадающие по неймспейсу и именам или атрибутам.

В HTML5 существуют сторонние элементы которые автоматически ассоциируются с соответствующими пространствами имён. Это значит, что HTML элементы будут действовать так, как если бы они находились в пространстве имён (`http://www.w3.org/1999/xhtml`), также если они не имеют xmlns аттрибута где-либо в документе, то такие элементы как `<svg>` и `<math>` будут ассоциироваться с их стандартными пространствами имён (`http://www.w3.org/2000/svg` и `http://www.w3.org/1998/Math/MathML`).

## Спецификация

- [CSS Namespaces Module](https://drafts.csswg.org/css-namespaces-3/#declaration)

## Поддержка браузерами

- Chrome 1.0+
- Firefox 1.0
- IE 9+
- Opera 8.0+
- Safari 3.0+

## Ссылки

- [@namespace](https://developer.mozilla.org/ru/docs/Web/CSS/@namespace) <sup><small>MDN (рус.)</small></sup>
