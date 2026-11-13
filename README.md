# RobôVerde — Android History Website

An educational website exploring the history and evolution of Android, featuring a custom client-side search system, paragraph navigation, and a responsive interface.

[![Live Demo](https://img.shields.io/badge/Live-Demo-3B82F6?style=flat-square)](https://kleinmoretty-coder.github.io/android-site-2.0/)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

**[Explore the Live Website](https://kleinmoretty-coder.github.io/android-site-2.0/)**

---

## Overview

RobôVerde is an educational website about the history, development, and evolution of the Android operating system.

The project originally started as an exercise from Module 4 of the Brazilian programming course *Curso em Vídeo*. It was later revisited and expanded with additional JavaScript functionality, improved code organization, and interactive navigation features.

The main improvement was the development of a custom search system that allows users to locate specific terms in the website's content and navigate between matching paragraphs.

The project represents an early stage of my development experience, particularly in DOM manipulation, JavaScript modules, responsive layouts, and client-side application logic.

## Features

### Client-Side Search

The search system uses a JavaScript data structure containing indexed words associated with their corresponding paragraphs.

When users enter a search term, the application searches the indexed content and identifies matching paragraphs.

The search includes:

- Input normalization.
- Accent-insensitive word matching.
- Identification of matching paragraphs.
- Navigation between search results.
- Visual highlighting of the selected paragraph.
- Automatic smooth scrolling to the matching content.

The entire process runs locally in the browser, without a backend or external search service.

### Search Result Navigation

Users can navigate between matching paragraphs using **Previous** and **Next** controls.

The application tracks search results and scrolls to the selected paragraph, highlighting its position within the page.

**Current limitation:** Search result navigation was developed primarily for desktop screens and has not been fully adapted for mobile devices.

### Dark Mode

The website includes a dark mode toggle, allowing users to switch between light and dark appearances.

### Navigation Menu

A navigation interface provides access to the website's topics and sections.

### Responsive Layout

The main website layout adapts to desktop and mobile screen sizes using CSS Grid, Flexbox, and responsive styling.

Some interactive features, particularly search result navigation, still require mobile-specific improvements.

## How the Search Works

The search implementation is divided into modules responsible for input formatting, indexed content, result processing, and navigation controls.

The general process is:

```text
User enters a search term
           |
           v
Input normalization
           |
           v
Search indexed content
           |
           v
Identify matching paragraphs
           |
           v
Generate navigation results
           |
           v
Highlight selected paragraph
           |
           v
Smooth scroll to its position
```

The search index is stored in a JavaScript module, allowing queries to run without network requests.

Instead of highlighting individual occurrences inside text nodes, the current implementation highlights the matching paragraph as a whole.

This approach was developed as an exercise in data structures, array operations, DOM interactions, and event-driven programming.

## Technologies

| Technology | Purpose |
|---|---|
| HTML5 | Semantic page structure |
| CSS3 | Layout, styling, and responsive design |
| CSS Grid & Flexbox | Interface organization |
| JavaScript | Search, interactions, and navigation |
| ES Modules | Code organization and separation of responsibilities |
| ESLint | Static code analysis |
| Prettier | Code formatting |

The website uses native JavaScript without a frontend framework.

## Project Structure

```text
.
├── index.html
├── assets/
│   ├── css/
│   ├── img/
│   └── js/
│       ├── main.js
│       └── modules/
│           ├── pesquisa.js
│           ├── pesquisadados.js
│           ├── botoesPesquisa.js
│           ├── menuFixed.js
│           ├── botaoDark.js
│           ├── titoloMover.js
│           ├── formatarinput.js
│           └── utils.js
├── eslint.config.mjs
├── package.json
└── LICENSE
```

### JavaScript Modules

| Module | Responsibility |
|---|---|
| `main.js` | Initializes the application and coordinates interface interactions |
| `pesquisa.js` | Processes searches and handles paragraph highlighting |
| `pesquisadados.js` | Stores the indexed content used by the search system |
| `botoesPesquisa.js` | Manages navigation between search results |
| `menuFixed.js` | Handles navigation bar behavior |
| `botaoDark.js` | Controls the dark mode interface |
| `titoloMover.js` | Adjusts title positioning |
| `formatarinput.js` | Normalizes search input |
| `utils.js` | Provides reusable utility functions |

## Getting Started

### Live Version

The website is available through GitHub Pages:

**[Open RobôVerde](https://kleinmoretty-coder.github.io/android-site-2.0/)**

### Run Locally

Clone the repository:

```bash
git clone https://github.com/kleinmoretty-coder/android-site-2.0.git
cd android-site-2.0
```

Start a local HTTP server:

```bash
npx serve .
```

Alternatively, use the **Live Server** extension in Visual Studio Code.

A local HTTP server is recommended because the project uses JavaScript ES Modules, which may encounter browser security restrictions when loaded directly through `file://`.

### Linting

Install the development dependencies:

```bash
npm install
```

Run ESLint:

```bash
npm run eslint
```

## Known Limitations

As an earlier educational project, RobôVerde contains some implementation choices that could be improved with a more structured approach.

The main known limitations are:

- **Mobile search navigation:** the search result controls are not fully adapted for mobile devices.
- **Static search index:** indexed terms are maintained in a JavaScript data structure rather than generated dynamically from the website content.
- **Search matching:** the current implementation focuses on normalized word matching rather than advanced full-text search.
- **Search feedback:** unsuccessful searches currently have limited user-facing feedback.

These limitations do not prevent the project from serving its original educational purpose, but they identify areas that could be improved in future iterations.

## Possible Improvements

- [ ] Adapt search result navigation for mobile devices.
- [ ] Improve search feedback and empty-result handling.
- [ ] Generate the search index automatically from the page content.
- [ ] Reduce unnecessary DOM operations.
- [ ] Improve accessibility and keyboard navigation.
- [ ] Add automated tests for search behavior.
- [ ] Review and simplify the
