# Bonfire CSS Framework

A lightweight, SASS-powered utility and component framework built around a warm, earthy color palette. It provides core styles for common HTML elements and a set of utility classes for rapid development.

---

## Installation

### 1. Get the Code

Clone the repository to your local machine:

```bash
git clone <YOUR_REPO_URL> bonfire-css
cd bonfire-css
```

### 2. Run the Sass Watcher (Required for Customization)

If you plan to modify any SCSS files, you must run the Sass compiler.  
This command watches your source files and compiles the output to `css/bonfire.css`:

```bash
# Run this from the project's root directory
sass --watch src/main.scss:css/bonfire.css
```

---

## Usage

### 1. Link the Stylesheet

Include the compiled CSS file in the `<head>` of your HTML document:

```html
<link rel="stylesheet" href="./css/bonfire.css" />
```

### 2. Base Layout

Wrap your main content in the `.container` class for a centered, max-width wrapper:

```html
<div class="container">
    <!-- Your content here -->
</div>
```

### 3. Components & Utilities

Use component classes for styled elements (like buttons) and utility classes for quick adjustments (like spacing, colors, and borders).

| Type       | Class Pattern        | Example |
|-------------|----------------------|----------|
| Component   | `.btn-primary`       | `<button class="btn btn-primary">Action</button>` |
| Color       | `.text-* .bg-*`      | `<p class="text-danger bg-light">...</p>` |
| Spacing     | `.p{d}-{size}` (m or p) | `<div class="pt-2 mb-4">...</div>` |
| Font        | `.fw-bold .fs-xl`    | `<span class="fw-bold fs-xl">Text</span>` |

---

## Customization

The theme colors, fonts, and sizing are controlled by **CSS Custom Properties (Variables)**, which are easy to override.

| CSS Variable          | Default Value      | Description |
|------------------------|--------------------|--------------|
| `--color-primary`      | Pumpkin Orange     | Main action color. |
| `--color-secondary`    | Bright Yellow      | Supporting accent color. |
| `--font-family-body`   | Merriweather, serif | Base body font. |

### To Customize the Theme

1. Create a new CSS file and link it **after** `bonfire.css`.  
2. Override the desired CSS variables within the `:root` selector.

```css
/* Your custom-styles.css */
:root {
    /* Changes the primary color globally */
    --color-primary: #5c8f42; 
    
    /* Changes the font for all body text */
    --font-family-body: 'Arial', sans-serif;
}
```

---

**Bonfire CSS** — Ignite your front-end with warmth and simplicity.
