# Frontend Mentor - Bento grid solution

This is a solution to the [Bento grid challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Bento grid solution](#frontend-mentor---bento-grid-solution)
  - [Table of contents](#table-of-contents)
  - [📋 Overview](#-overview)
    - [🎯 The challenge](#-the-challenge)
    - [📸 Screenshot](#-screenshot)
    - [🔗 Links](#-links)
  - [⚙️ My process](#️-my-process)
    - [🛠️ Built with](#️-built-with)
    - [📚 What I learned](#-what-i-learned)
    - [🚀 Continued development](#-continued-development)
    - [🤖 AI Collaboration](#-ai-collaboration)
    - [💡 Useful resources](#-useful-resources)
  - [🙏 Acknowledgments](#-acknowledgments)
    - [📬 Let's connect](#-lets-connect)

## 📋 Overview

### 🎯 The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size

### 📸 Screenshot

![Desktop](./desktop-screenshot.png)
![Mobile](./mobile-screenshot.png)

### 🔗 Links

- [Solution URL](https://github.com/juanhastier/bento-grid)
- [Live Site URL](https://juanhastier.github.io/bento-grid)

## ⚙️ My process

### 🛠️ Built with

- Semantic HTML5 markup
- CSS custom properties (variables)
- CSS Grid (grid-template-areas)
- Flexbox
- Mobile-first workflow
- BEM methodology
- Variable fonts (DM Sans)

### 📚 What I learned

This project was a great opportunity to practice complex CSS Grid layouts with `grid-template-areas`.

**Layout strategy:**
I used a mobile-first approach with a single column layout. For tablet (720px), I switched to a 2‑column grid, and for desktop (1200px), I used a 4‑column grid with custom `grid-template-areas` to match the design.

```css
.bento-grid {
  display: grid;
  gap: 1.8rem;
}

@media (min-width: 1200px) {
  .bento-grid {
    grid-template-columns: repeat(4, 1fr);
    grid-template-areas:
      "content-ia   reviews     reviews    posts"
      "content-ia   platforms   schedule   posts"
      "content-ia   audience    follower   follower";
  }
}
```

**Overflowing images:**
Some cards required images to overflow their containers. I used `overflow: hidden` on the card and negative margins on the image. This was simpler and more maintainable than `position: absolute`.

```css
.card--schedule {
  overflow: hidden;
}

.card--schedule .card__image {
  margin-bottom: -2.2rem;
}
```

**BEM and maintainability:**
I organized styles by modifiers (card--reviews, card--follower, etc.) and grouped common properties (gap, alignment, background) to avoid duplication. This made the CSS cleaner and easier to update.

### 🚀 Continued development

I plan to keep improving my frontend skills by focusing on:
- CSS Grid advanced patterns – mastering complex `grid-template-areas` and nested grids.
- Performance – optimizing images and reducing CSS specificity.
- Accessibility – testing with screen readers and improving keyboard navigation.
- CSS variables – exploring more consistent spacing systems for larger projects.

### 🤖 AI Collaboration

I used DeepSeek as an AI assistant throughout this project:
- Brainstorming solutions: Discussed different approaches for the bento grid layout and overflow behavior.
- Debugging: Resolved issues with `grid-template-areas` and overlapping images.
- Code review: Received feedback on CSS organization, BEM naming, and media query consistency.
- Learning: Explored modern CSS features like variable fonts and `font-optical-sizing`.

What worked well:
The AI was helpful for clarifying layout concepts and catching structural issues early.

What didn't work well:
Some suggestions were too generic for this specific design; I had to adapt them manually.

Overall:
Using AI as a pair programming assistant accelerated my learning and helped me produce a more polished final solution.

### 💡 Useful resources

- [MDN Web Docs](https://developer.mozilla.org/) - I really enjoyed studying on MDN, and I will continue to use it in the future.
- [CSS Tricks: CSS Flexbox Layout Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - This is an amazing article which helped me finally understand flexbox layout. I'd recommend it to anyone still learning this concept.
- [CSS Tricks: CSS Grid Layout Guide](https://css-tricks.com/complete-guide-css-grid-layout/) - This is an amazing article which helped me finally understand grid layout. I'd recommend it to anyone still learning this concept.

## 🙏 Acknowledgments

- Frontend Mentor – for the challenge and design assets.
- DeepSeek (AI assistant) – for helping me brainstorm, debug, and review the code.
- Google Fonts – for the DM Sans variable font.
- MDN Web Docs – for documentation on CSS Grid, grid-template-areas, and variable fonts.

### 📬 Let's connect

- Frontend Mentor - [@juanhastier](https://www.frontendmentor.io/profile/juanhastier)
- LinkedIn - [Juan Hastier](https://www.linkedin.com/in/juanhastier)
- GitHub - [juanhastier](https://github.com/juanhastier)
