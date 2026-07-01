# Frontend Mentor - Loopstudios landing page solution

![GitHub last commit](https://img.shields.io/github/last-commit/berefire/loopstudios-landing-page)
![Repo size](https://img.shields.io/github/repo-size/berefire/loopstudios-landing-page)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Sass](https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white)
![Architecture - BEM](https://img.shields.io/badge/Architecture-BEM-000000?style=for-the-badge)
![CUBE CSS](https://img.shields.io/badge/CUBE%20CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
[![Frontend Mentor](https://img.shields.io/badge/Frontend%20Mentor-3e54a3?style=for-the-badge&logo=frontendmentor&logoColor=white)](https://www.frontendmentor.io/)
![Build Tool - Vite](https://img.shields.io/badge/Build%20Tool-Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Semantic HTML](https://img.shields.io/badge/Semantic%20HTML-ff9800?style=for-the-badge)
![Accessibility](https://img.shields.io/badge/Accessibility-A11Y-0052cc?style=for-the-badge)
![Responsive Layout](https://img.shields.io/badge/Responsive%20Layout-Full%20Support-blue?style=for-the-badge)
![Mobile First](https://img.shields.io/badge/Mobile--First-Design-orange?style=for-the-badge)
[![Google Lighthouse](https://img.shields.io/badge/Lighthouse-Audit-00B0FF?style=for-the-badge&logo=lighthouse&logoColor=white)](./assets/downloads/lighthouse-performance-report.pdf)

This is a solution to the [Loopstudios landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/loopstudios-landing-page-N88J5Onjw). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#️my-process)
  - [Built with](#built-with)
  - [Project architecture](#project-architecture)
  - [Accessibility](#accessibility)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

---

## 📖Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size.
- See hover and focus states for all interactive elements.
- Open and close an accessible mobile navigation menu.
- Navigate the website using only the keyboard.

### 📸Screenshot


### 🔗Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

---

## ⚙️My process

### 🛠Built with

- Semantic HTML5
- Sass (SCSS)
- CUBE CSS architecture
- BEM methodology
- Design Tokens (Primitive & Semantic)
- CSS Custom Properties
- CSS Grid
- Flexbox
- Mobile-first workflow
- Vanilla JavaScript (ES Modules)
- HTML `<dialog>` element
- Vite

---

## 🔎Project architecture

The project follows a scalable architecture inspired by **CUBE CSS** while using **BEM** for component naming.

```html
src/
│
├── assets/
├── js/
├── styles/
│   ├── abstracts/
│   ├── base/
│   ├── compositions/
│   ├── components/
│   ├── tokens/
│   │   ├── primitives/
│   │   └── semantics/
│   └── utilities/
```

The styling system is based on:

- Primitive design tokens
- Semantic design tokens
- Reusable Sass mixins and functions
- CSS custom properties generated from Sass maps

This approach keeps the design system consistent while making components easy to maintain.

---

## ♿Accessibility

Accessibility was considered throughout the project.

Implemented features include:

- Semantic HTML landmarks
- Accessible navigation
- Keyboard navigation
- Visible focus states
- ARIA attributes
- Accessible mobile menu using the native `<dialog>` element
- Focus management when opening and closing the mobile menu
- Scroll locking while the dialog is open
- Screen reader friendly labels

---

### 💡What I learned

This project helped me improve several areas of front-end development.

#### Building a design system with Sass

Instead of hardcoding values, I created primitive and semantic design tokens.

```scss
$colors: (
  "color-bg-footer": primitives.$black,
  "color-fc-footer-text": primitives.$white,
);
```

This made the project much easier to maintain.

#### Creating reusable mixins

For example, media queries are handled using a reusable mixin.

```scss
@mixin mq($breakpoint) {
    $size: map.get(primitives.$breakpoints, $breakpoint);

    @media (min-width: $size) {
        @content;
    }
}
```

#### Managing typography through semantic tokens

Instead of applying font values directly, typography styles are stored in semantic maps.

```scss
@include mixins.text-style(semantics.$text-hero);
```

This allows typography to evolve independently from components.

#### Building accessible UI interactions

The mobile navigation uses the native HTML `<dialog>` element together with JavaScript for:

- opening and closing animations
- focus management
- scroll locking
- keyboard accessibility

---

### 🚀Continued development

In future projects I'd like to continue improving:

- CSS architecture for larger applications
- Advanced JavaScript patterns
- Component-driven development
- Automated accessibility testing
- Performance optimization
- Unit and integration testing

---

### 📚Useful resources

- [https://frontendmentor.io](https://frontendmentor.io) - Great platform for practicing realistic frontend projects.
- [https://cube.fyi](https://cube.fyi) - Excellent resource for learning and applying CUBE CSS.
- [https://developer.mozilla.org](https://developer.mozilla.org) - My primary reference for HTML, CSS, JavaScript, and accessibility.
- [https://www.w3.org/WAI/](https://www.w3.org/WAI/) - Helpful accessibility guidance and best practices.

---

### 🤖AI Collaboration

AI was used as a development assistant throughout this project.

#### Tools

- ChatGPT

#### How AI was used

- Reviewing HTML semantics
- Discussing CSS architecture
- Designing Sass token structure
- Improving accessibility
- Debugging JavaScript
- Reviewing responsive layouts
- Refining Git commit messages
- Explaining CSS Grid and Flexbox layouts

#### What worked well

AI was especially useful for discussing architectural decisions rather than simply generating code. It helped evaluate different implementation approaches while allowing me to make the final design decisions myself.

---

## 👤Author

- Frontend Mentor - [@berefire](https://www.frontendmentor.io/profile/berefire)
- GitHub - [@berefire](https://github.com/berefire)

## 🙏Acknowledgments

Thanks to Frontend Mentor for providing practical challenges that help developers improve real-world frontend skills.

---
