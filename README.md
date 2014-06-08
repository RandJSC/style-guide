Fifth Room Creative Programming Style Guide
============================================

by Mike Green (@mikedamage)

---

Table of Contents
-----------------

- [Introduction](#introduction)
- [Code Formatting](#code-formatting)
  - [CSS/SCSS](#cssscss)
  - [CoffeeScript](#coffeescript)
  - [HTML5](#html5)
  - [JavaScript](#javascript)
  - [JSON](#json)
  - [PHP](#php)
  - [Ruby](#ruby)
- [Project Folder Structure](#structure)
- [Project QA Procedures](#qa)

---

## Introduction

The purpose of this guide is to provide guidelines for how code produced by FRC should be formatted, how projects should be laid out, and how projects should be QA'd before release.

## Code Formatting

### CSS/SCSS

- Use 2 spaces for indentation.
- Use [OOCSS](http://www.smashingmagazine.com/2011/12/12/an-introduction-to-object-oriented-css-oocss/) principles. Figure out which properties elements share in common, then write overrides to handle the differences.
- If you notice that you're repeating yourself, you're doing it wrong.
- Be as specific as possible with selectors. Don't be afraid of `>`.
- If you need to use a style repeatedly with minor variations, write a Sass mixin.
- If you need to use a style repeatedly with no variations, use a non-printing `%` class and include it with `@extend`.
- Split styles into partials named for what they style (i.e. `_header.scss`).

#### Examples

```css
/* Indent with 2 spaces */
.foo {
  font-weight: bold;
}

/* Write generic styles first and use the cascade to override */
ul {
  padding-left: 20px;
  font-size: 1em;
}

ul.no-bullets {
  list-style: none;
  padding-left: 0;
}
```

### CoffeeScript

- Use 2 spaces for indentation
- Keep lines to a maximum of 80 characters
- For functions that take more than 1 function as arguments, write each function ahead of time and store as variables.
- Refer to [JavaScript](#javascript) guidelines. Many of them also apply to CoffeeScript.

#### Examples

```coffee
# Keep lines short for readability. Don't do this:
foo = if bar.hasOwnProperty('reallyLongPropertyName') then bar.getReallyLongFunctionName() else []

# Break up the statement like this instead:
foo = if bar.hasOwnProperty('reallyLongPropertyName')
then bar.reallyLongFunctionName()
else []

# Chains can be broken up and indented like this:
$('.element').
  find('.foo').
    addClass('bar').
    end().
  find('.quuz').
    removeClass('active')
```
