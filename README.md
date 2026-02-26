# 🎨 Roovix Theme System

<div align="center">

![Roovix](https://img.shields.io/badge/Roovix-Knowledge%20Base-0969da?style=for-the-badge)
![Version](https://img.shields.io/badge/version-2.0.0-success?style=for-the-badge)
![Light/Dark](https://img.shields.io/badge/mode-light%20%7C%20dark-blue?style=for-the-badge)
![Tailwind](https://img.shields.io/badge/Tailwind-Ready-38B2AC?style=for-the-badge)
![GitHub](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

**Official theme system for Roovix Knowledge Base Platform**  
*Dual-mode (light/dark) CSS theme with 300+ semantic variables*

[Features](#-features) • [Quick Start](#-quick-start) • [Usage](#-usage) • [Variables](#-css-variables) • [Components](#-components) • [Team](#-team)

</div>

---

## 📖 About Roovix

**Roovix** is an enterprise knowledge management platform designed to help organizations capture, organize, and share knowledge effectively. This theme system embodies our brand identity:

- **Clarity** - Clean, readable interfaces
- **Depth** - Rich visual hierarchy  
- **Intelligence** - Smart, intuitive design
- **Consistency** - Unified experience across all touchpoints

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🌓 **Dual Mode** | Perfectly tuned Light & Dark themes for Roovix |
| 🎨 **Semantic Variables** | 300+ CSS variables named for knowledge platform UI |
| ⚡ **Tailwind Ready** | Seamless integration with Tailwind CSS |
| ♿ **Accessible** | WCAG 2.1 AA compliant for enterprise use |
| 📱 **Responsive** | Mobile-first, works on all devices |
| 🔧 **Customizable** | Easy to extend with brand-specific colors |

---

## 🚀 Quick Start

### 1. Add to your project

```bash
cp roovix-theme.css your-project/src/styles/
```

### 2. Include in your HTML

```html
<link rel="stylesheet" href="path/to/roovix-theme.css">
```

### 3. Set your theme

```html
<!-- Light mode (default) -->
<html data-theme="light">

<!-- Dark mode -->
<html data-theme="dark">
```

### 4. Add theme switcher

```html
<button onclick="toggleRoovixTheme()">Switch Theme</button>

<script>
function toggleRoovixTheme() {
  const html = document.documentElement;
  const current = html.getAttribute('data-theme') || 'light';
  const next = current === 'light' ? 'dark' : 'light';
  
  html.setAttribute('data-theme', next);
  localStorage.setItem('roovix-theme', next);
}

// Load saved preference
const savedTheme = localStorage.getItem('roovix-theme');
if (savedTheme) document.documentElement.setAttribute('data-theme', savedTheme);
</script>
```

---

## 🎨 Roovix Brand Colors

### Primary Palette

| Variable | Light Mode | Dark Mode | Usage |
|----------|------------|-----------|-------|
| `--bg-primary` | `#ffffff` | `#0d1117` | Main background |
| `--text-primary` | `#1f2328` | `#f0f6fc` | Primary content |
| `--text-accent` | `#0969da` | `#4493f8` | Links, actions |
| `--surface-card` | `#ffffff` | `#151b23` | Cards, containers |

### Semantic Palette

| Variable | Light | Dark | Purpose |
|----------|-------|------|---------|
| `--status-success` | `#1a7f37` | `#3fb950` | Success states |
| `--status-danger` | `#d1242f` | `#f85149` | Error states |
| `--status-warning` | `#9a6700` | `#d29922` | Warning states |
| `--status-info` | `#0969da` | `#4493f8` | Info states |

---

## 📦 CSS Variables Reference

### Background Colors

```css
--bg-primary      /* Main app background */
--bg-secondary    /* Secondary surfaces (cards, sidebars) */
--bg-tertiary     /* Tertiary surfaces (elevated) */
--bg-inset        /* Deepest background (modals) */
--bg-muted        /* Muted backgrounds */
--bg-emphasis     /* Emphasized backgrounds (tooltips) */

--surface-card    /* Card containers */
--surface-dropdown/* Dropdown menus */
--surface-modal   /* Modal dialogs */
--surface-tooltip /* Tooltips */
--surface-sidebar /* Sidebar navigation */
--surface-header  /* Header bars */
```

### Text Colors

```css
--text-primary    /* Primary content (headings, body) */
--text-secondary  /* Secondary text (metadata, captions) */
--text-tertiary   /* Tertiary text (placeholders) */
--text-disabled   /* Disabled states */
--text-inverse    /* Text on dark backgrounds */
--text-on-emphasis/* Text on colored backgrounds */
--text-white      /* Pure white text */
--text-black      /* Pure black text */

--text-success    /* Success messages */
--text-danger     /* Error messages */
--text-warning    /* Warning messages */
--text-info       /* Information messages */
--text-done       /* Completed states */
--text-link       /* Hyperlinks */
--text-accent     /* Accent text */
```

### Border Colors

```css
--border-default  /* Default borders */
--border-muted    /* Subtle borders */
--border-emphasis /* Emphasized borders */
--border-disabled /* Disabled borders */
--border-accent   /* Accent borders (blue) */
--border-success  /* Success borders (green) */
--border-danger   /* Danger borders (red) */
--border-warning  /* Warning borders (yellow) */
--border-info     /* Info borders (blue) */
```

### Button Colors

```css
/* Primary buttons */
--btn-primary-bg
--btn-primary-bg-hover
--btn-primary-bg-active
--btn-primary-bg-disabled
--btn-primary-text
--btn-primary-text-disabled

/* Default buttons */
--btn-default-bg
--btn-default-bg-hover
--btn-default-bg-active
--btn-default-text
--btn-default-border

/* Danger buttons */
--btn-danger-bg-hover
--btn-danger-text
--btn-danger-icon

/* Special */
--btn-star-color  /* Star/favorite color */
```

### Status Colors

```css
--status-success-bg
--status-success-bg-muted
--status-success-text
--status-success-border

--status-danger-bg
--status-danger-bg-muted
--status-danger-text
--status-danger-border

--status-warning-bg
--status-warning-bg-muted
--status-warning-text
--status-warning-border

--status-info-bg
--status-info-bg-muted
--status-info-text
--status-info-border
```

### Code & Syntax

```css
--code-bg         /* Code block background */
--code-text       /* Code text */
--code-comment    /* Comments (gray) */
--code-keyword    /* Keywords (red/purple) */
--code-string     /* Strings (green/blue) */
--code-constant   /* Constants (blue) */
--code-variable   /* Variables (orange) */
--code-function   /* Functions (purple) */
--code-tag        /* HTML tags (green) */
```

### Shadows

```css
--shadow-xs       /* Extra small */
--shadow-sm       /* Small */
--shadow-md       /* Medium */
--shadow-lg       /* Large */
--shadow-floating /* Floating elements (modals) */
--shadow-inset    /* Inner shadows */
```

---

## 💻 Usage Examples

### Basic Usage

```css
.my-component {
  background-color: var(--bg-primary);
  color: var(--text-primary);
  border: 1px solid var(--border-default);
  box-shadow: var(--shadow-sm);
}
```

### With Tailwind

```html
<div class="bg-[var(--bg-primary)] text-[var(--text-primary)] 
            border border-[var(--border-default)]">
  Content
</div>
```

### Button Components

```html
<button class="roovix-btn roovix-btn-primary">Create Article</button>
<button class="roovix-btn roovix-btn-default">Cancel</button>
<button class="roovix-btn roovix-btn-danger">Delete</button>

<style>
.roovix-btn {
  display: inline-flex;
  align-items: center;
  padding: 0.5rem 1rem;
  border-radius: 0.375rem;
  font-weight: 500;
  cursor: pointer;
  border: 1px solid transparent;
}

.roovix-btn-primary {
  background-color: var(--btn-primary-bg);
  color: var(--btn-primary-text);
}

.roovix-btn-primary:hover {
  background-color: var(--btn-primary-bg-hover);
}

.roovix-btn-danger {
  color: var(--btn-danger-text);
}

.roovix-btn-danger:hover {
  background-color: var(--btn-danger-bg-hover);
  color: var(--btn-danger-text-hover);
}
</style>
```

### Card Components

```html
<div class="roovix-card">
  <div class="roovix-card-header">
    <h3>Knowledge Article</h3>
    <span class="roovix-badge roovix-badge-success">Published</span>
  </div>
  <div class="roovix-card-body">
    <p>Article content goes here...</p>
  </div>
  <div class="roovix-card-footer">
    <span class="text-secondary">Updated 2 hours ago</span>
    <button class="roovix-btn roovix-btn-primary">Read More</button>
  </div>
</div>

<style>
.roovix-card {
  background-color: var(--surface-card);
  border: 1px solid var(--border-default);
  border-radius: 0.5rem;
  box-shadow: var(--shadow-sm);
}

.roovix-card-header {
  padding: 1rem;
  border-bottom: 1px solid var(--border-muted);
}

.roovix-card-body {
  padding: 1rem;
}

.roovix-card-footer {
  padding: 1rem;
  border-top: 1px solid var(--border-muted);
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
```

### Status Badges

```html
<span class="roovix-badge roovix-badge-success">Active</span>
<span class="roovix-badge roovix-badge-danger">Archived</span>
<span class="roovix-badge roovix-badge-warning">Pending</span>
<span class="roovix-badge roovix-badge-info">Review</span>

<style>
.roovix-badge {
  display: inline-flex;
  align-items: center;
  border-radius: 2rem;
  padding: 0.25rem 0.75rem;
  font-size: 0.75rem;
  font-weight: 500;
  border: 1px solid transparent;
}

.roovix-badge-success {
  background-color: var(--status-success-bg-muted);
  color: var(--status-success-text);
  border-color: var(--status-success-border);
}

.roovix-badge-danger {
  background-color: var(--status-danger-bg-muted);
  color: var(--status-danger-text);
  border-color: var(--status-danger-border);
}

.roovix-badge-warning {
  background-color: var(--status-warning-bg-muted);
  color: var(--status-warning-text);
  border-color: var(--status-warning-border);
}

.roovix-badge-info {
  background-color: var(--status-info-bg-muted);
  color: var(--status-info-text);
  border-color: var(--status-info-border);
}
</style>
```

### Form Inputs

```html
<div class="roovix-form-group">
  <label class="roovix-label">Search Knowledge Base</label>
  <input type="text" class="roovix-input" placeholder="Enter search terms...">
</div>

<style>
.roovix-input {
  background-color: var(--input-bg);
  color: var(--input-text);
  border: 1px solid var(--input-border);
  border-radius: 0.375rem;
  padding: 0.5rem 0.75rem;
  width: 100%;
}

.roovix-input:focus {
  outline: none;
  border-color: var(--input-border-focus);
  box-shadow: 0 0 0 3px var(--status-info-bg-muted);
}

.roovix-label {
  display: block;
  margin-bottom: 0.5rem;
  color: var(--text-secondary);
  font-weight: 500;
}
</style>
```

---

## 🌓 Theme Switcher Component

### Complete Toggle Component

```html
<div class="roovix-theme-switcher">
  <button 
    class="roovix-theme-toggle" 
    onclick="RoovixTheme.toggle()"
    aria-label="Switch between light and dark mode">
    <span class="light-icon">☀️</span>
    <span class="dark-icon">🌙</span>
  </button>
</div>

<style>
.roovix-theme-toggle {
  background: transparent;
  border: 1px solid var(--border-default);
  border-radius: 2rem;
  padding: 0.5rem 1rem;
  cursor: pointer;
  color: var(--text-primary);
}

.light-icon, .dark-icon {
  display: inline-block;
  transition: transform 0.3s ease;
}

[data-theme="light"] .dark-icon,
[data-theme="dark"] .light-icon {
  display: none;
}

[data-theme="light"] .light-icon {
  transform: rotate(0deg);
}

[data-theme="dark"] .dark-icon {
  transform: rotate(360deg);
}
</style>

<script>
window.RoovixTheme = {
  init() {
    const saved = localStorage.getItem('roovix-theme');
    if (saved) {
      document.documentElement.setAttribute('data-theme', saved);
    } else {
      const systemDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
      document.documentElement.setAttribute('data-theme', systemDark ? 'dark' : 'light');
    }
  },
  
  toggle() {
    const html = document.documentElement;
    const current = html.getAttribute('data-theme') || 'light';
    const next = current === 'light' ? 'dark' : 'light';
    
    html.setAttribute('data-theme', next);
    localStorage.setItem('roovix-theme', next);
    
    window.dispatchEvent(new CustomEvent('roovix-theme-change', {
      detail: { theme: next }
    }));
  },
  
  getCurrent() {
    return document.documentElement.getAttribute('data-theme') || 'light';
  }
};

RoovixTheme.init();
</script>
```

---

## 🧩 Complete Page Example

```html
<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Roovix Knowledge Base</title>
  <link rel="stylesheet" href="roovix-theme.css">
  <style>
    .roovix-header {
      background-color: var(--surface-header);
      padding: 0.75rem 2rem;
      display: flex;
      align-items: center;
      gap: 2rem;
      border-bottom: 1px solid var(--header-border-divider);
    }
    
    .header-brand {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      color: var(--header-fg-logo);
    }
    
    .header-search {
      flex: 1;
      max-width: 400px;
    }
    
    .search-input {
      width: 100%;
      background-color: var(--surface-header-search);
      border: 1px solid var(--headerSearch-borderColor);
      color: var(--text-white);
      padding: 0.5rem 1rem;
      border-radius: 0.375rem;
    }
    
    .header-actions {
      display: flex;
      align-items: center;
      gap: 1rem;
    }
    
    .roovix-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2rem;
    }
    
    .welcome-section {
      text-align: center;
      padding: 3rem 1rem;
      background: linear-gradient(135deg, var(--bg-primary) 0%, var(--bg-secondary) 100%);
      border-radius: 1rem;
      margin-bottom: 3rem;
    }
    
    .welcome-title {
      font-size: 2.5rem;
      font-weight: 700;
      margin-bottom: 0.5rem;
      color: var(--text-primary);
    }
    
    .welcome-subtitle {
      font-size: 1.25rem;
      color: var(--text-secondary);
    }
    
    .section-title {
      font-size: 1.875rem;
      font-weight: 600;
      margin-bottom: 2rem;
      color: var(--text-primary);
    }
    
    .categories-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
      margin-bottom: 3rem;
    }
    
    .category-card {
      text-align: center;
      padding: 2rem;
    }
    
    .category-icon {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }
    
    .category-card h3 {
      margin-bottom: 0.5rem;
      font-size: 1.25rem;
    }
    
    .category-card p {
      color: var(--text-secondary);
      margin-bottom: 1rem;
    }
    
    .text-secondary {
      color: var(--text-secondary);
    }
    
    .read-more {
      color: var(--text-link);
      text-decoration: none;
      font-weight: 500;
    }
    
    .read-more:hover {
      text-decoration: underline;
    }
    
    .roovix-footer {
      background-color: var(--bg-secondary);
      padding: 2rem;
      text-align: center;
      border-top: 1px solid var(--border-muted);
      color: var(--text-secondary);
    }
  </style>
</head>
<body>
  <header class="roovix-header">
    <div class="header-brand">
      <img src="logo.svg" alt="Roovix" class="header-logo">
      <span class="header-title">Knowledge Base</span>
    </div>
    
    <div class="header-search">
      <input type="search" placeholder="Search knowledge..." class="search-input">
    </div>
    
    <div class="header-actions">
      <button class="roovix-theme-toggle" onclick="RoovixTheme.toggle()">
        <span class="light-icon">☀️</span>
        <span class="dark-icon">🌙</span>
      </button>
      <button class="roovix-btn roovix-btn-primary">Sign In</button>
    </div>
  </header>

  <main class="roovix-container">
    <section class="welcome-section">
      <h1 class="welcome-title">Welcome to Roovix</h1>
      <p class="welcome-subtitle">Your enterprise knowledge platform</p>
    </section>

    <section class="categories-section">
      <h2 class="section-title">Browse by Category</h2>
      <div class="categories-grid">
        <div class="roovix-card category-card">
          <div class="category-icon">📚</div>
          <h3>Documentation</h3>
          <p>Technical guides and docs</p>
          <span class="roovix-badge roovix-badge-info">124 articles</span>
        </div>
        
        <div class="roovix-card category-card">
          <div class="category-icon">🎓</div>
          <h3>Tutorials</h3>
          <p>Step-by-step learning</p>
          <span class="roovix-badge roovix-badge-success">89 articles</span>
        </div>
        
        <div class="roovix-card category-card">
          <div class="category-icon">💡</div>
          <h3>Best Practices</h3>
          <p>Industry standards</p>
          <span class="roovix-badge roovix-badge-warning">56 articles</span>
        </div>
        
        <div class="roovix-card category-card">
          <div class="category-icon">🔧</div>
          <h3>Troubleshooting</h3>
          <p>Common solutions</p>
          <span class="roovix-badge roovix-badge-danger">42 articles</span>
        </div>
      </div>
    </section>

    <section class="featured-section">
      <h2 class="section-title">Featured Articles</h2>
      <div class="articles-grid">
        <div class="roovix-card">
          <div class="roovix-card-header">
            <h3>Getting Started with Roovix</h3>
            <span class="roovix-badge roovix-badge-success">New</span>
          </div>
          <div class="roovix-card-body">
            <p>Learn the basics of navigating and using the Roovix platform...</p>
          </div>
          <div class="roovix-card-footer">
            <span class="text-secondary">5 min read</span>
            <a href="#" class="read-more">Read →</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer class="roovix-footer">
    <p>&copy; 2024 Roovix. All rights reserved.</p>
  </footer>

  <script>
    window.RoovixTheme = {
      init() {
        const saved = localStorage.getItem('roovix-theme');
        if (saved) {
          document.documentElement.setAttribute('data-theme', saved);
        }
      },
      
      toggle() {
        const html = document.documentElement;
        const current = html.getAttribute('data-theme') || 'light';
        const next = current === 'light' ? 'dark' : 'light';
        
        html.setAttribute('data-theme', next);
        localStorage.setItem('roovix-theme', next);
      }
    };
    
    RoovixTheme.init();
  </script>
</body>
</html>
```

---

## 📱 Responsive Breakpoints

```css
/* Mobile First - default styles for mobile */

/* Tablet */
@media (min-width: 640px) {
  .container {
    padding: 1.5rem;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .container {
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
  }
}

/* Large Desktop */
@media (min-width: 1280px) {
  .container {
    padding: 2.5rem;
    max-width: 1400px;
  }
}
```

---

## ♿ Accessibility Features

```css
/* Focus styles */
:focus-visible {
  outline: 2px solid var(--focus-outline);
  outline-offset: 2px;
}

/* Reduced motion */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 🔧 Customization Guide

### Adding Brand Colors

```css
:root {
  --roovix-brand-purple: #6f42c1;
  --roovix-brand-gradient: linear-gradient(135deg, #0969da, #6f42c1);
}

[data-theme="dark"] {
  --roovix-brand-purple: #b392f0;
}
```

### Component Overrides

```css
[data-theme="dark"] .special-component {
  background-color: #1a2634;
  border-color: #4a5568;
}
```

---

## 🧪 Testing Checklist

- [ ] Light mode renders correctly
- [ ] Dark mode renders correctly
- [ ] Theme switching works smoothly
- [ ] All interactive elements have hover states
- [ ] Focus indicators are visible
- [ ] Color contrast meets WCAG standards
- [ ] Mobile responsive design works
- [ ] No hardcoded colors (all use CSS variables)

---

## 📄 License

MIT © Roovix. All rights reserved.

---

<div align="center">

**Made with ❤️ by the Roovix Team**

[![YouTube](https://img.shields.io/badge/YouTube-Subscribe-red?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@roovix)

**Questions?** Contact #design-system on Slack

</div>
