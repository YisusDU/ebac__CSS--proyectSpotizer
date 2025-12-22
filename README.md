# 🎧 Spotizer - Advanced CSS Layout
## 🧪 Tech Stack

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![SASS](https://img.shields.io/badge/SASS-CC6699?style=flat&logo=sass&logoColor=white)
![BEM](https://img.shields.io/badge/Methodology-BEM-black?style=flat)

## Preview
<img src="https://github.com/YisusDU/ebac__CSS--proyectSpotizer/blob/main/ASSETS/Img/imagen_2025-12-21_215809380.png?raw=true" alt="Spotizer Interface Preview" width="100%">

## 📁 Overview

This document provides a **comprehensive technical overview** of **Spotizer**, a pixel-perfect clone of the Spotify interface designed to demonstrate mastery over modern CSS Layout systems.

The system enables users to:

- Navigate a responsive, grid-based layout mimicking a real streaming app.
- View complex UI components (Track lists, Album Cards, Player controls).
- Experience seamless adaptability across different screen sizes.

This overview includes:

- **CSS Grid Architecture:** Main layout definition (`grid-template-areas`).
- **Responsive Strategy:** Breakpoint management for dynamic resizing.
- **Component Styling:** Implementation of the BEM methodology.

> For more detailed subsystem documentation, see:
- `Layout System` – Grid & Flexbox usage
- `Theming` – Color variables & Typography
- `Media Queries` – Mobile adaptability

---

## 🧭 System Overview

**Spotizer** is built as a Static Web Application that relies heavily on the browser's rendering engine to create a fluid user experience without JavaScript logic.

### 📐 Grid-Based Layout
The entire application body is governed by a master **CSS Grid** that defines the Sidebar, Main Content, and Player areas, ensuring elements stay anchored regardless of viewport size.

### 📱 Adaptive Responsiveness
Instead of simple fluid widths, the application uses specific **Media Queries** to hide/show columns in the song list and adjust the grid tracks for mobile devices.

### 🎨 Visual Hierarchy
Uses advanced CSS selectors and pseudo-classes (`:hover`, `:nth-child`) to create interactive feedback and alternating row colors for better readability.

> **Sources:**
- `Sass/main.css` (lines 32–39)
- `index.html` (Structure definition)

---

## 🏗️ Architecture & Layout Strategy

The core of the project is the **Holy Grail Layout** implemented via CSS Grid:

1.  **Sidebar (`grid-area: header`):** Fixed navigation panel on the left.
2.  **Main View (`grid-area: main`):** Scrollable content area for albums and lists.
3.  **Player (`grid-area: footer`):** Sticky media controls fixed at the bottom.


> **Sources:**
- `Sass/main.css` (Grid definition)
- `index.html` (lines 13–871)

---

## 🧰 Technology Stack and Project Structure

The project utilizes pre-processed CSS (SASS) compiled into standard CSS:

| Technology | Version | Purpose |
|------------|---------|---------|
| **HTML5** | Semantic | DOM Structure & Accessibility |
| **CSS Grid** | Level 2 | Macro-Layout (Page Structure) |
| **Flexbox** | Level 1 | Micro-Layout (Component Alignment) |
| **GitHub Actions**| CI/CD | Automated Deployment to Pages |

### 🗂️ Project Structure
```text
ebac__CSS--proyectSpotizer/
├── .github/
│   └── workflows/static.yml # CI/CD Pipeline
├── assets/
│   ├── IMG/                 # Album covers & Artist photos
│   └── ICONS/               # UI Icons (Play, Pause, Skip)
├── Sass/
│   └── main.css             # Compiled Stylesheet
└── index.html               # Main Entry Point
```
> **Sources:**
- `.github/workflows/static.yml` (Deployment config)

---

## 🪟 Feature Spotlight: Responsive Grid System

This project implements a sophisticated **Breakpoint System** to handle complex content reflows, ensuring the "PXNDX" artist page looks good on any screen.

### 1. Dynamic Column Hiding
As the screen shrinks, the grid columns for "Date Added" and "Album" are progressively hidden using `display: none` inside media queries.
* **Result:** Prevents horizontal scrolling on smaller screens while keeping the essential "Title" and "Duration" visible.

### 2. Adaptive Card Grid
The album section utilizes `grid-template-columns: repeat(auto-fill, minmax(...))` to automatically flow cards onto new rows based on available width.



> **Sources:**
- `Sass/main.css` (Media Queries section)
- `index.html` (Responsive classes application)

---

## 📚 Relevant Source Files & Logic Map

To understand the styling architecture, follow this hierarchy:

| File Path | Role | Description |
|-----------|------|-------------|
| **`index.html`** | 🦴 **Skeleton** | Defines the semantic structure (`<nav>`, `<main>`, `<footer>`) that maps to the CSS Grid areas. |
| **`Sass/main.css`** | 🎨 **Skin** | The monolithic stylesheet containing the Reset, Typography, Grid definitions, and Component styles. |
| **`.github/workflows/static.yml`** | 🚀 **Deploy** | The automation script that builds and publishes the site to GitHub Pages on every push. |
| **`assets/ICONS/`** | 🖼️ **Assets** | The collection of SVG/PNG icons used for the playback controls and navigation menu. |

---

>[!Note]
>You can check the full documentation <a href="https://deepwiki.com/YisusDU/ebac__CSS--proyectSpotizer">-here-</a>
