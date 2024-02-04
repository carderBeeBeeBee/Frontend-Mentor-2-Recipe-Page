# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### Screenshot

[Desktop](./screenshots/desktop-screenshot.png)
[Mobile](./screenshots/mobile-screenshot.png)

### Links

- Solution URL: [Solution](https://carderbeebeebee.github.io/Frontend-Mentor-2-Recipe-Page/)
- Live Site URL: [Live site](https://carderbeebeebee.github.io/Frontend-Mentor-2-Recipe-Page/)

## My process

I started by focusing on the mobile design, as I understand that a mobile-first workflow is generally best practice. I tried to go through each section of the page in order - if I got to a point where I felt stuck and was not sure how to progress, I took a break and moved on to another section that I felt more confident working on, and then came back to the section that I was struggling with. I tried to think carefully about how the site should be structured to be responsive and to easily adapt to the desktop version.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Mobile-first workflow

### What I learned

```html - using <span> tags to create bold text at the beginning of a list item. I also used my first <hr> in this project
<li><span class="list-item-bold">Enjoy:</span> Serve hot, with additional salt and pepper if needed.</li>
```
```css - implementing static fonts using the @font-face rule
@font-face {
    font-family: "Outfit";
    src: url("/assets/fonts/outfit/Outfit-VariableFont_wght.ttf");
    font-style: normal;
    font-weight: 400 600 700;
}
```
```css - displaying list items as a table in order to style the item counters seperately to the rest of the item using the ::before pesudo-selector - also, learning about CSS counters!
li {
    display: table;
    table-layout: fixed;
}

li::before {
    width: 30px;
    color: #854632;
    font-weight: 700;
    display: table-cell;
}

ol {
    list-style: none;
}

ol li {
    counter-increment: ol-counter;
}

ol li::before {
    content: counter(ol-counter)". ";
}
```
```css - learning about how table borders can be styled using border-collapse: collapse;, as well as the use of the last-child selector
table {
    border-collapse: collapse;
}

tr {
    border-bottom: 1px solid #e4ded8;
}

tr:last-child {
    border-bottom: none;
}
```
```js - no js used this time!
```

### Continued development

I would definitely like to use CSS counters more to fully understand their use-cases and potential applications. More practice styling lists would also be good, as it is great to finally understand how this can be done. I could also use more practice with CSS tables as I don't feel fully confident with these yet.

### Useful resources

- [Stack Overflow](https://stackoverflow.com/) - Various substack threads were extremely helpful for understanding not just the correct CSS properties to use to solve certain problems, but why they work. In particular, this was great to see multiple perspectives on how list items can be styled.
- [W3 Schools](https://www.w3schools.com/) - As ever, an invaluable resource. This was really helpful for a number of things - one memorable one was about styling the contents of table cells, which showed me the vertical-align property.

## Author

- Website - [carderBee](https://carderbeebeebee.github.io/)
- Frontend Mentor - [@carderBee](https://www.frontendmentor.io/profile/carderBee)

## Acknowledgments

[Stack Overflow](https://stackoverflow.com/questions/57242345/how-to-do-css-style-for-ordered-list-numbers) - User zer00ne on Stack Overflow for his very helpful answer to another user's question about styling ordered lists.
