# Astro 0.26 & Tailwind CSS 3.0.23

This project is an attempt to create a collection of templates and components with the utility-first CSS framework Tailwind CSS. It is a work in progress.

A preview is available at [Netlify](https://astro025.netlify.app/)

## File Routing

The files imports are in this logic:

    /pages/index.astro -> /layouts/layoutStyles/singleColumn.astro -> /layouts/pageLayout.astro

Then, singleColumn.astro imports three navigation components:

* /components/nav/mainNavbar.astro
* /components/nav/styleSidebar.astro
* /components/nav/templateSidebar.astro

## Project Structure

```
/
├── public/
├── src/
│   ├── components/
│   │   └── nav/
│   │       ├── mainNavbar.astro
│   │       ├── styleSidebar.astro
│   │       └── templateSidebar.astro
│   ├── layouts/
│   │   ├── layoutStyles/
│   │   │   ├── featured.astro
│   │   │   ├── singleColumn.astro
│   │   │   └── split.astro
│   │   └── pageLayout.astro
│   ├── pages/
│   │   ├── accordion.astro
│   │   ├── card.astro
│   │   ├── featured.astro
│   │   ├── index.astro
│   │   ├── single.astro
│   │   └── split.astro
│   ├── styles/
│   └── config.ts
├── astro.config.mjs
├── package.json
├── sandbox.config.json
└── tailwind.config.cjs
```
## HTML5 Elements Structure

```
┌───────────────────────────
│ <html> pageLayout.astro
│ ┌─────────────────────────
│ │ <body> singleColumn.astro
│ │ ┌───────────────────────
│ │ │ <header> mainNavbar.astro
│ │ └───────────────────────
│ │ ┌───────────────────────
│ │ │ <main>
│ │ │ ┌─────────────────────
│ │ │ │ <aside> styleSidebar.astro
│ │ │ └─────────────────────
│ │ │ ┌─────────────────────
│ │ │ │ <slot /> index.astro
│ │ │ └─────────────────────
│ │ │ ┌─────────────────────
│ │ │ │ <aside> templateSidebar.astro
│ │ │ └─────────────────────
│ │ └───────────────────────
│ │ ┌───────────────────────
│ │ │ <footer>
│ │ └───────────────────────
│ └─────────────────────────
└───────────────────────────