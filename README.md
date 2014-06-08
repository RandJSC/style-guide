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

#### Example

```css
/* Indent with 2 spaces */
.foo {
  font-weight: bold;
}
```
