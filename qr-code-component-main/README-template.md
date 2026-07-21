# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### Screenshot

![Screenshot of the completed QR code component](./screenshot.png)

### Links

- Solution URL: 📝 [Add your solution URL here](https://your-solution-url.com)
- Live Site URL: 📝 [Add your live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS Flexbox
- Google Fonts (Outfit)
- A mobile-friendly `max-width` approach
- HSL color values from the provided style guide

### What I learned

This was my first component build, and I structured the HTML first before touching any styling. A few concepts really clicked for me along the way.

**Centering with Flexbox.** I learned that centering happens on the *parent* container, not the element you want to center. I also hit the classic gotcha where vertical centering does nothing until the container is tall enough — `min-height: 100vh` gives the body the full window height so there's actually room to center within:

```css
body {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
```

**Taming an oversized image.** My QR code image originally displayed at its full natural size and overflowed everywhere. Capping it to the width of its container fixed it instantly, and this is a trick I'll reuse on every project:

```css
img {
  max-width: 100%;
}
```

**Web fonts are a two-step process.** Importing a font in the HTML `<head>` only *downloads* it — I still had to *apply* it in CSS with `font-family` before anything changed. "Download in HTML, apply in CSS" is the mental model that finally made it make sense.

**Inheritance saves repetition.** Setting `text-align: center` and `font-family` once on a parent flows the style down to its children, so I didn't have to repeat myself on every element.

I also got more comfortable reading `hsl()` color values (the third number controls lightness), the difference between `<img>` and `<link>`, and why the `<head>` and `<body>` do completely different jobs.

### Continued development

Going forward I want to keep practicing:

- Fine-tuning spacing by eye to match a design more precisely
- Building responsive layouts that adapt across screen sizes
- Getting more fluent with the box model (padding vs. margin vs. border)

### Useful resources

- [Google Fonts](https://fonts.google.com/specimen/Outfit) - Used this to import the Outfit font and grab the embed code for weights 400 and 700.
- [MDN Web Docs](https://developer.mozilla.org) - A reliable reference for HTML and CSS properties.
- [CSS-Tricks Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - A helpful visual reference for understanding how Flexbox aligns items.

### AI Collaboration

I worked through this challenge with an AI assistant acting as a guided mentor.

- **What I used:** Claude, configured as a patient step-by-step mentor for beginners.
- **How I used it:** Rather than giving me finished code, it gave hints and explanations and asked questions, so I wrote every line myself. It helped me debug issues like the overflowing image and the font not applying, and explained the *why* behind each fix.
- **What worked well:** Being guided instead of handed answers meant the concepts actually stuck. Breaking each problem into small steps kept it from feeling overwhelming.

## Author

- Frontend Mentor - [@britb1](https://www.frontendmentor.io/profile/britb1)
