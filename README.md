# template-static-web

> Minimal, well-organized template for static websites — scalable CSS architecture, organized assets, and GitHub Pages deployment ready from the first commit.

---

# Purpose

`template-static-web` is the starting point for static websites built with:

- HTML
- CSS
- Vanilla JavaScript

No backend and no build step are required.

This template introduces a scalable CSS architecture that prevents the common problem of a single `style.css` becoming an unmaintainable monolith as the project grows.

The template is intentionally lightweight. It provides structure without imposing a framework, making it ideal for:

- SENA frontend exercises
- Portfolio websites
- Landing pages
- Documentation sites
- Any project where direct browser delivery is the appropriate solution

---

# When to Use This Template

## Use `template-static-web` when:

- You are building a website that does not require a backend
- The project uses HTML, CSS, and vanilla JavaScript
- You want to deploy directly to GitHub Pages
- You are learning frontend fundamentals and need a professional starting structure
- You are building a portfolio site, landing page, or documentation site

## Do NOT Use `template-static-web` when:

- Building applications with components, state management, or API consumption → use `template-frontend-app`
- Building projects that require a backend → use `template-backend-api`
- Creating academic deliverables requiring formal documentation → use `template-academic`
- Working on database-focused projects → use `template-database`

---

# Use Cases

This template is suitable for:

- Single-page portfolios
- Personal websites
- Landing pages
- Product showcase pages
- Event websites
- Service listing pages
- SENA multimedia and web development exercises
- Interactive UI prototypes
- Client-side only applications
- Static documentation hubs
- Knowledge base websites

---

# Features

## Modular CSS Structure

CSS is separated into:

- `base/`
- `layout/`
- `components/`

using a centralized imports architecture through `main.css`.

## CSS Variables

Built-in design tokens located in:

```text
css/base/variables.css
```

Including:

- Colors
- Typography values
- Spacing scales
- Transition settings

## Responsive-Ready Layout

Provides structural patterns that support:

- Mobile-first design
- Media queries
- Fluid layouts

## GitHub Actions Deployment Workflow

Includes:

```text
.github/workflows/deploy.yml
```

Automatically deploys the project to GitHub Pages whenever changes are pushed to the `main` branch.

## Clean Folder Convention

Strict asset separation:

- `img/`
- `fonts/`
- `icons/`

keeping the project root organized and predictable.

---

# Architecture and Structure

```text
template-static-web/
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── assets/
│   ├── fonts/
│   ├── icons/
│   └── img/
│
├── css/
│   ├── base/
│   │   ├── reset.css
│   │   ├── typography.css
│   │   └── variables.css
│   │
│   ├── components/
│   │   ├── buttons.css
│   │   └── cards.css
│   │
│   ├── layout/
│   │   ├── footer.css
│   │   ├── header.css
│   │   └── grid.css
│   │
│   └── main.css
│
├── examples/
│   └── index-example.html
│
├── js/
│   ├── components/
│   │   └── navigation.js
│   │
│   └── main.js
│
├── .gitignore
├── index.html
└── README.md
```

---

## Directory Responsibilities

### `.github/workflows/`

Contains deployment automation.

| File | Purpose |
| --- | --- |
| `deploy.yml` | GitHub Pages deployment workflow |

---

### `assets/`

Stores global static resources.

| Directory | Purpose |
| --- | --- |
| `fonts/` | Typography files (`.woff2`, `.ttf`) |
| `icons/` | SVG icons, favicons, interface icons |
| `img/` | Images, illustrations, vectors, backgrounds |

---

### `css/`

Main stylesheet architecture.

#### `base/`

Low-level configuration.

| File | Purpose |
| --- | --- |
| `reset.css` | Browser normalization |
| `typography.css` | Typography system |
| `variables.css` | Design tokens |

#### `components/`

Reusable UI modules.

| File | Purpose |
| --- | --- |
| `buttons.css` | Button styles |
| `cards.css` | Content containers |

#### `layout/`

Page structure.

| File | Purpose |
| --- | --- |
| `header.css` | Header and navigation |
| `footer.css` | Footer structure |
| `grid.css` | Layout containers |

#### `main.css`

Root stylesheet responsible only for imports.

---

### `examples/`

Reference implementations.

| File | Purpose |
| --- | --- |
| `index-example.html` | Demonstrates template usage |

---

### `js/`

Frontend functionality.

| File | Purpose |
| --- | --- |
| `navigation.js` | Mobile navigation behavior |
| `main.js` | Application entry point |

---

# Quick Start

## 1. Initialize the Project

Create a repository from this template using GitHub's **Use this template** button.

Clone the repository:

```bash
git clone https://github.com/your-username/your-project-name.git

cd your-project-name
```

---

## 2. Clean Up Examples (Optional)

Review:

```text
examples/index-example.html
```

to understand how the architecture works.

After reviewing:

```bash
rm -rf examples/
```

---

## 3. Develop Locally

No package manager or build process is required.

### Option A — Direct Browser Access

Open:

```text
index.html
```

directly in the browser.

### Option B — Live Server

Use:

- VS Code Live Server
- Any local HTTP server

### Option C — Python HTTP Server

```bash
python3 -m http.server 8000
```

---

## 4. Build Your Styles

Create new component files inside the appropriate CSS folder.

Example:

```text
css/components/form.css
```

Then register the import in:

```css
/* css/main.css */

@import "./base/variables.css";
@import "./base/reset.css";
@import "./base/typography.css";

@import "./layout/grid.css";
@import "./layout/header.css";
@import "./layout/footer.css";

@import "./components/buttons.css";
@import "./components/cards.css";
@import "./components/form.css";
```

---

# Customization and Scaling Rules

Follow these architectural rules to keep the template maintainable.

| Element | Scalable? | Notes |
| --- | --- | --- |
| `css/` subdirectory names | No  | `base/`, `layout/`, and `components/` are fixed |
| Files inside CSS folders | Yes | Add as many files as needed |
| `css/main.css` | Yes | Imports only |
| `assets/` structure | Yes | Maintain existing conventions |
| `js/main.js` | Yes | Initialize modules here |
| `index.html` | Yes | Main application markup |

---

# Roadmap

- [ ] Add `example-01-basic-page`
- [ ] Add `example-02-components`
- [ ] Add `example-03-responsive`
- [ ] Add a modern CSS reset to `css/base/reset.css`
- [ ] Add `docs/style-guide.md`
- [ ] Add starter versions of:
  - `css/components/buttons.css`
  - `css/components/forms.css`

---

# References

## CSS Methodology

- BEM Methodology

## CSS Documentation

- CSS Custom Properties (MDN)
- CSS Grid Layout Guide – CSS Tricks

## Deployment

- GitHub Pages Documentation

## Design Systems

- Modern CSS Reset – Andy Bell

---

# Ecosystem

Part of the sxiks project ecosystem.

**Type:** Template

**Domain:** Frontend Fundamentals