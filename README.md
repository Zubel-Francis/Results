# Frontend Mentor - Results Summary Component Solution

This is my solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV).

The project recreates a responsive results card with a score panel, summary rows, category icons, and an interactive continue button.

## Table of Contents

- [Overview](#overview)
  - [The Challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My Process](#my-process)
  - [Built With](#built-with)
  - [What I Learned](#what-i-learned)
  - [Continued Development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The Challenge

Users should be able to:

- View the result and summary component at desktop and mobile screen sizes
- See the card change from a two-column desktop layout to a stacked mobile layout
- See hover and focus states on the continue button
- Read each result category with its matching icon, color, and score

### Screenshot

Add your finished screenshot here:

```md
![Solution screenshot](./screenshot.jpg)
```

### Links

- Solution URL: Add your Frontend Mentor solution link here
- Live Site URL: Add your live project link here

## My Process

### Built With

- Semantic HTML5
- CSS custom properties
- CSS Grid
- Flexbox
- Local `@font-face`
- Responsive media queries
- `rem` units for scalable sizing
- `clamp()` and `min()` for flexible layout sizing
- Logical CSS properties like `margin-block` and `padding-inline`

### What I Learned

This project helped me practice recreating a component from a design image and making it responsive.

The main card uses CSS Grid on desktop:

```css
.results-card {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
}
```

On mobile, the grid becomes one column:

```css
@media (max-width: 43.75rem) {
    .results-card {
        grid-template-columns: 1fr;
    }
}
```

I also used a local variable font with `@font-face`:

```css
@font-face {
    font-family: 'Hanken Grotesk';
    src: url('./assets/fonts/HankenGrotesk-VariableFont_wght.ttf') format('truetype');
    font-weight: 500 800;
    font-style: normal;
}
```

The button active state uses a gradient to match the provided active-state design:

```css
.continue-button:hover,
.continue-button:focus-visible {
    background: linear-gradient(
        to bottom,
        var(--color-light-slate-blue),
        var(--color-light-royal-blue)
    );
}
```

### Continued Development

In future projects, I want to keep improving:

- Matching exact design spacing from screenshots
- Creating cleaner responsive card layouts
- Using custom properties consistently
- Improving accessible button and focus states
- Structuring repeated UI items with semantic HTML

### AI Collaboration

I used AI assistance to help convert the provided design images into responsive HTML and CSS, improve the CSS with variables and relative units, and write a README that explains the work.

## Author

- Frontend Mentor: Add your Frontend Mentor username here
- Website: Add your website or portfolio link here
