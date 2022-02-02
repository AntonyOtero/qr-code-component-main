# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### Screenshot

![](./images/screenshot.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [https://antonyotero.github.io/qr-code-component-main/](https://antonyotero.github.io/qr-code-component-main/)

## My process

### What I learned


This project was fairly simple, but some useful CSS tricks and features were put into use. Mainly CSS variables and centering elements using either grids or by setting an element's position and transform properties.

#### __CSS Variables__

I created [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) by targeting the [:root pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/:root) and setting the variables to the values given in the style-guide.md file. In this context the :root pseudo-class represents the html element. While CSS variables can be defined in any scope, it is best practice to define them on the :root pseudo-class. This is so that they can be applied globally.

All variables are required to be prefixed with `--` and written in kebab-case. I chose to group related variables by defining them under a common heading and then using the heading as the start of the variable name.

```css
:root {
  /* Colors */
  --color-white: hsl(0, 0%, 100%);
  --color-light-gray: hsl(212, 45%, 89%);
  --color-grayish-blue: hsl(220, 45%, 55%);
  --color-dark-blue: hsl(218, 44%, 22%);
  /* Typography */
  --font-family: "Outfit", sans-serif;
  --font-size: 15px;
}
```

To use the css variables, you can use the [var()](https://developer.mozilla.org/en-US/docs/Web/CSS/var) function.

```css
body {
  font: var(--font-size) var(--font-family);
  background: var(--color-light-gray);
}
```

#### __Centering elements__

The first method I used to center elements was to set the target elements parent to a [grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout) and then set the [place-items](https://developer.mozilla.org/en-US/docs/Web/CSS/place-items) property to center.

```css
body {
  display: grid;
  place-items: center;
}
```

Another method for centering elements I used in this project is to set the target element's [position](https://developer.mozilla.org/en-US/docs/Web/CSS/position) property to abosolute. Then set the `top` and `left` properties to 50% of the parent element's width and height respectively. lastly, set the [transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform) property to `translate(-50%, -50%)` to center the element. This is necessary because the element's origin is not at the center of the element but at the top left corner of the element.

```css
.element {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

## Author

- Frontend Mentor - [@AntonyOtero](https://www.frontendmentor.io/profile/AntonyOtero)
- Twitter - [@AntonyOtero](https://twitter.com/AntonyOtero)
