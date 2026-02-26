# 🎨 Roovix Design System

<div align="center">

![Roovix](https://img.shields.io/badge/Roovix-Knowledge%20Base-0969da?style=for-the-badge)
![Version](https://img.shields.io/badge/version-2.0.0-success?style=for-the-badge)
![Light/Dark](https://img.shields.io/badge/mode-light%20%7C%20dark-blue?style=for-the-badge)
![Components](https://img.shields.io/badge/components-50+-orange?style=for-the-badge)

**Official Design System for Roovix Knowledge Base Platform**  
*A comprehensive guide for all Roovix employees*

[Getting Started](#-getting-started) • [Colors](#-colors) • [Typography](#-typography) • [Components](#-components) • [Dark Mode](#-dark-mode)

</div>

---

## 📋 Table of Contents

- [Introduction](#-introduction)
- [Quick Start](#-quick-start)
- [File Structure](#-file-structure)
- [Core Concepts](#-core-concepts)
- [Colors](#-colors)
- [Typography](#-typography)
- [Spacing System](#-spacing-system)
- [Components](#-components)
- [Dark Mode](#-dark-mode)
- [How to Use](#-how-to-use)
- [Examples](#-examples)
- [Best Practices](#-best-practices)
- [Troubleshooting](#-troubleshooting)
- [FAQ](#-faq)

---

## 📖 Introduction

Welcome to the **Roovix Design System**! This guide helps you create consistent, beautiful interfaces for the Roovix Knowledge Base Platform.

### Why Use This System?

- ✅ **Consistency** - All Roovix products look and feel the same
- ✅ **Efficiency** - Reusable components save development time
- ✅ **Accessibility** - Built with WCAG 2.1 AA standards
- ✅ **Dark Mode** - Automatic support for light/dark themes
- ✅ **Mobile Ready** - Responsive design out of the box

---

## 🚀 Quick Start

### For New Projects

```bash
# 1. Copy the CSS files to your project
cp roovix-base.css your-project/src/styles/
cp roovix-components.css your-project/src/styles/

# 2. Add to your HTML
<link rel="stylesheet" href="styles/roovix-base.css">
<link rel="stylesheet" href="styles/roovix-components.css">

# 3. Add theme attribute
<html data-theme="light"> <!-- or "dark" -->

# 4. Start building!
```

### For Existing Projects

```bash
# Just add the CSS files and update your HTML classes
# No need to rewrite everything - use our classes alongside yours
```

---

## 📁 File Structure

```
roovix-design-system/
│
├── 📄 roovix-base.css        # Core variables (colors, spacing, typography)
├── 📄 roovix-components.css   # All UI components
└── 📄 README.md               # This guide
```

---

## 🎯 Core Concepts

### 1. The roovix- Prefix

All classes start with `roovix-` to avoid conflicts:

```html
<!-- Good - uses our prefix -->
<button class="roovix-btn roovix-btn-primary">Click me</button>

<!-- Wrong - missing prefix -->
<button class="btn btn-primary">Click me</button>
```

### 2. Two Themes: Light & Dark

```html
<!-- Light mode (default) -->
<html data-theme="light">

<!-- Dark mode -->
<html data-theme="dark">
```

### 3. Size Variants

Most components come in multiple sizes:

```html
<button class="roovix-btn roovix-btn-sm">Small</button>
<button class="roovix-btn roovix-btn-base">Default</button>
<button class="roovix-btn roovix-btn-lg">Large</button>
```

---

## 🎨 Colors

### Primary Colors

| Variable | Light Mode | Dark Mode | Usage |
|----------|------------|-----------|-------|
| `--roovix-bg-primary` | `#ffffff` | `#0d1117` | Main background |
| `--roovix-bg-secondary` | `#f6f8fa` | `#151b23` | Cards, sidebars |
| `--roovix-text-primary` | `#1f2328` | `#f0f6fc` | Main text |
| `--roovix-text-secondary` | `#59636e` | `#9198a1` | Subtitles, metadata |

### Semantic Colors

| Color | Variable | Light | Dark | Use For |
|-------|----------|-------|------|---------|
| 🟢 Success | `--roovix-text-success` | `#1a7f37` | `#3fb950` | Success messages |
| 🔴 Danger | `--roovix-text-danger` | `#d1242f` | `#f85149` | Errors, deletions |
| 🟡 Warning | `--roovix-text-warning` | `#9a6700` | `#d29922` | Warnings |
| 🔵 Info | `--roovix-text-info` | `#0969da` | `#4493f8` | Information |

### Using Colors in CSS

```css
.my-element {
  background-color: var(--roovix-bg-primary);
  color: var(--roovix-text-primary);
  border: 1px solid var(--roovix-border-default);
}
```

---

## 📝 Typography

### Font Sizes

| Class | Size | Usage |
|-------|------|-------|
| `--text-xs` | 12px | Labels, footnotes |
| `--text-sm` | 14px | Secondary text |
| `--text-base` | 16px | Body text |
| `--text-md` | 18px | Large body |
| `--text-lg` | 20px | Small headings |
| `--text-xl` | 24px | Section headings |
| `--text-2xl` | 32px | Page titles |
| `--text-3xl` | 40px | Hero titles |

### Font Weights

| Class | Weight | Usage |
|-------|--------|-------|
| `--font-light` | 300 | Less important text |
| `--font-normal` | 400 | Body text |
| `--font-medium` | 500 | Emphasized text |
| `--font-semibold` | 600 | Subheadings |
| `--font-bold` | 700 | Headings |

### Example

```css
.page-title {
  font-size: var(--text-2xl);
  font-weight: var(--font-bold);
  color: var(--roovix-text-primary);
}
```

---

## 📏 Spacing System

We use an 8px grid system:

| Variable | Pixels | Usage |
|----------|--------|-------|
| `--space-1` | 4px | Tiny gaps |
| `--space-2` | 8px | Small gaps |
| `--space-3` | 12px | Between elements |
| `--space-4` | 16px | Standard padding |
| `--space-6` | 24px | Large sections |
| `--space-8` | 32px | Between sections |
| `--space-12` | 48px | Page sections |
| `--space-16` | 64px | Major sections |

### Usage

```css
.card {
  padding: var(--space-4);
  margin-bottom: var(--space-6);
  gap: var(--space-2);
}
```

---

## 🧩 Components

### 1. Buttons

#### Button Types

```html
<!-- Primary - Main actions -->
<button class="roovix-btn roovix-btn-primary">Create Article</button>

<!-- Secondary - Alternative actions -->
<button class="roovix-btn roovix-btn-secondary">Cancel</button>

<!-- Danger - Destructive actions -->
<button class="roovix-btn roovix-btn-danger">Delete</button>

<!-- Outline - Less emphasis -->
<button class="roovix-btn roovix-btn-outline">Learn More</button>

<!-- Ghost - Minimal emphasis -->
<button class="roovix-btn roovix-btn-ghost">Settings</button>

<!-- Link - Like a link but button -->
<button class="roovix-btn roovix-btn-link">Forgot password?</button>
```

#### Button Sizes

```html
<button class="roovix-btn roovix-btn-xs">Extra Small</button>
<button class="roovix-btn roovix-btn-sm">Small</button>
<button class="roovix-btn roovix-btn-base">Default</button>
<button class="roovix-btn roovix-btn-md">Medium</button>
<button class="roovix-btn roovix-btn-lg">Large</button>
<button class="roovix-btn roovix-btn-xl">Extra Large</button>
```

#### Icon Buttons

```html
<!-- Icon only -->
<button class="roovix-btn roovix-btn-icon roovix-btn-primary">
  <svg><!-- icon --></svg>
</button>

<!-- With text -->
<button class="roovix-btn roovix-btn-primary roovix-btn-icon-left">
  <svg><!-- icon --></svg>
  <span>Save</span>
</button>
```

#### Button States

```html
<!-- Disabled -->
<button class="roovix-btn roovix-btn-primary" disabled>Can't click</button>

<!-- Loading -->
<button class="roovix-btn roovix-btn-primary">
  <span class="roovix-loader roovix-loader-xs"></span>
  <span>Loading...</span>
</button>
```

#### Button Group

```html
<div class="roovix-btn-group">
  <button class="roovix-btn roovix-btn-secondary">Left</button>
  <button class="roovix-btn roovix-btn-secondary">Middle</button>
  <button class="roovix-btn roovix-btn-secondary">Right</button>
</div>
```

---

### 2. Cards

#### Basic Card

```html
<div class="roovix-card">
  <div class="roovix-card-header">
    <h3 class="roovix-card-title">Article Title</h3>
    <span class="roovix-badge roovix-badge-success">Published</span>
  </div>
  <div class="roovix-card-body">
    <p>This is the card content. It can contain any HTML elements.</p>
  </div>
  <div class="roovix-card-footer">
    <span class="roovix-text-secondary">Updated 2h ago</span>
    <button class="roovix-btn roovix-btn-primary">Read More</button>
  </div>
</div>
```

#### Card Sizes

```html
<div class="roovix-card roovix-card-sm">Small Card</div>
<div class="roovix-card roovix-card-md">Default Card</div>
<div class="roovix-card roovix-card-lg">Large Card</div>
<div class="roovix-card roovix-card-xl">Extra Large Card</div>
```

#### Card with Shadow

```html
<div class="roovix-card roovix-card-shadow-sm">Subtle shadow</div>
<div class="roovix-card roovix-card-shadow-md">Medium shadow</div>
<div class="roovix-card roovix-card-shadow-lg">Large shadow</div>
<div class="roovix-card roovix-card-shadow-floating">Floating effect</div>
```

#### Interactive Card

```html
<div class="roovix-card roovix-card-interactive">
  <!-- Hover effects work automatically -->
</div>
```

---

### 3. Avatars

#### Avatar Sizes

```html
<img class="roovix-avatar roovix-avatar-xs" src="user.jpg" alt="User">
<img class="roovix-avatar roovix-avatar-sm" src="user.jpg" alt="User">
<img class="roovix-avatar roovix-avatar-base" src="user.jpg" alt="User">
<img class="roovix-avatar roovix-avatar-md" src="user.jpg" alt="User">
<img class="roovix-avatar roovix-avatar-lg" src="user.jpg" alt="User">
<img class="roovix-avatar roovix-avatar-xl" src="user.jpg" alt="User">
<img class="roovix-avatar roovix-avatar-2xl" src="user.jpg" alt="User">
```

#### Avatar with Status

```html
<div class="roovix-avatar-container">
  <img class="roovix-avatar roovix-avatar-md" src="user.jpg" alt="User">
  <span class="roovix-avatar-status roovix-avatar-status-online"></span>
</div>

<!-- Status types: online, offline, away, busy -->
```

#### Avatar Group (Stack)

```html
<div class="roovix-avatar-group">
  <img class="roovix-avatar roovix-avatar-base" src="user1.jpg" alt="User 1">
  <img class="roovix-avatar roovix-avatar-base" src="user2.jpg" alt="User 2">
  <img class="roovix-avatar roovix-avatar-base" src="user3.jpg" alt="User 3">
  <span class="roovix-avatar-count">+5</span>
</div>
```

#### Text Avatar

```html
<div class="roovix-avatar roovix-avatar-base">JD</div>
```

---

### 4. Badges

#### Badge Types

```html
<span class="roovix-badge roovix-badge-primary">Primary</span>
<span class="roovix-badge roovix-badge-secondary">Secondary</span>
<span class="roovix-badge roovix-badge-success">Success</span>
<span class="roovix-badge roovix-badge-danger">Danger</span>
<span class="roovix-badge roovix-badge-warning">Warning</span>
<span class="roovix-badge roovix-badge-info">Info</span>
<span class="roovix-badge roovix-badge-done">Done</span>
```

#### Badge Sizes

```html
<span class="roovix-badge roovix-badge-sm">Small</span>
<span class="roovix-badge roovix-badge-base">Default</span>
<span class="roovix-badge roovix-badge-lg">Large</span>
```

#### Badge with Icon

```html
<span class="roovix-badge roovix-badge-success roovix-badge-icon-left">
  <svg><!-- icon --></svg>
  <span>Completed</span>
</span>
```

---

### 5. Forms

#### Text Input

```html
<div class="roovix-form-group">
  <label class="roovix-form-label">Email</label>
  <input type="email" class="roovix-input" placeholder="Enter your email">
  <span class="roovix-form-hint">We'll never share your email</span>
</div>
```

#### Input States

```html
<!-- Error state -->
<input class="roovix-input roovix-input-error" value="Wrong value">
<span class="roovix-form-error">This field is required</span>

<!-- Success state -->
<input class="roovix-input roovix-input-success" value="Correct">

<!-- Disabled -->
<input class="roovix-input" disabled value="Cannot edit">
```

#### Input Sizes

```html
<input class="roovix-input roovix-input-sm" placeholder="Small">
<input class="roovix-input" placeholder="Default">
<input class="roovix-input roovix-input-lg" placeholder="Large">
```

#### Textarea

```html
<textarea class="roovix-textarea" placeholder="Write something..."></textarea>
```

#### Select Dropdown

```html
<select class="roovix-select">
  <option>Option 1</option>
  <option>Option 2</option>
  <option>Option 3</option>
</select>
```

#### Checkbox

```html
<label class="roovix-checkbox">
  <input type="checkbox">
  <span class="roovix-checkbox-label">Remember me</span>
</label>
```

#### Radio

```html
<label class="roovix-radio">
  <input type="radio" name="option">
  <span class="roovix-radio-label">Option A</span>
</label>
```

#### Toggle/Switch

```html
<label class="roovix-toggle">
  <input type="checkbox">
  <span class="roovix-toggle-slider"></span>
</label>
```

#### Form Layout

```html
<div class="roovix-form-group">
  <label class="roovix-form-label">Full Name</label>
  <input class="roovix-input" placeholder="John Doe">
</div>

<div class="roovix-form-group">
  <label class="roovix-form-label">Email</label>
  <input class="roovix-input" type="email" placeholder="john@example.com">
</div>

<div class="roovix-form-group">
  <button class="roovix-btn roovix-btn-primary">Submit</button>
</div>
```

---

### 6. Alerts

#### Alert Types

```html
<div class="roovix-alert roovix-alert-success">
  <div class="roovix-alert-icon">✅</div>
  <div class="roovix-alert-content">
    <div class="roovix-alert-title">Success!</div>
    <p>Your changes have been saved.</p>
  </div>
  <button class="roovix-alert-close">×</button>
</div>

<div class="roovix-alert roovix-alert-danger">
  <div class="roovix-alert-icon">❌</div>
  <div>Error: Unable to save changes.</div>
</div>

<div class="roovix-alert roovix-alert-warning">
  <div class="roovix-alert-icon">⚠️</div>
  <div>Your session will expire soon.</div>
</div>

<div class="roovix-alert roovix-alert-info">
  <div class="roovix-alert-icon">ℹ️</div>
  <div>New features available.</div>
</div>
```

#### Alert Sizes

```html
<div class="roovix-alert roovix-alert-sm">Small alert</div>
<div class="roovix-alert">Default alert</div>
<div class="roovix-alert roovix-alert-lg">Large alert</div>
```

---

### 7. Navigation

#### Navbar

```html
<nav class="roovix-navbar">
  <div class="roovix-navbar-brand">
    <img src="logo.svg" alt="Roovix" height="32">
    <span>Knowledge Base</span>
  </div>
  
  <div class="roovix-navbar-nav">
    <a href="#" class="roovix-navbar-item active">Home</a>
    <a href="#" class="roovix-navbar-item">Articles</a>
    <a href="#" class="roovix-navbar-item">Categories</a>
    <a href="#" class="roovix-navbar-item">About</a>
  </div>
  
  <div class="roovix-navbar-actions">
    <button class="roovix-btn roovix-btn-primary">Sign In</button>
  </div>
</nav>
```

#### Side Navigation

```html
<div class="roovix-side-nav">
  <div class="roovix-side-nav-header">MAIN</div>
  
  <a href="#" class="roovix-side-nav-item active">
    <svg class="roovix-side-nav-icon"><!-- icon --></svg>
    <span>Dashboard</span>
  </a>
  
  <a href="#" class="roovix-side-nav-item">
    <svg class="roovix-side-nav-icon"><!-- icon --></svg>
    <span>Articles</span>
  </a>
  
  <a href="#" class="roovix-side-nav-item">
    <svg class="roovix-side-nav-icon"><!-- icon --></svg>
    <span>Analytics</span>
  </a>
  
  <div class="roovix-side-nav-header">SETTINGS</div>
  
  <a href="#" class="roovix-side-nav-item">
    <span>Profile</span>
  </a>
</div>
```

#### Tabs

```html
<div class="roovix-tabs">
  <button class="roovix-tab active">Overview</button>
  <button class="roovix-tab">Articles</button>
  <button class="roovix-tab">Comments</button>
  <button class="roovix-tab">Settings</button>
</div>
```

#### Breadcrumbs

```html
<nav class="roovix-breadcrumb">
  <span class="roovix-breadcrumb-item">
    <a href="#">Home</a>
  </span>
  <span class="roovix-breadcrumb-separator">/</span>
  <span class="roovix-breadcrumb-item">
    <a href="#">Knowledge Base</a>
  </span>
  <span class="roovix-breadcrumb-separator">/</span>
  <span class="roovix-breadcrumb-item active">Current Page</span>
</nav>
```

#### Pagination

```html
<ul class="roovix-pagination">
  <li class="roovix-page-item"><a href="#" class="roovix-page-link">←</a></li>
  <li class="roovix-page-item"><a href="#" class="roovix-page-link">1</a></li>
  <li class="roovix-page-item active"><a href="#" class="roovix-page-link">2</a></li>
  <li class="roovix-page-item"><a href="#" class="roovix-page-link">3</a></li>
  <li class="roovix-page-item"><a href="#" class="roovix-page-link">4</a></li>
  <li class="roovix-page-item"><a href="#" class="roovix-page-link">5</a></li>
  <li class="roovix-page-item"><a href="#" class="roovix-page-link">→</a></li>
</ul>
```

---

### 8. Tables

#### Basic Table

```html
<table class="roovix-table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Role</th>
      <th>Status</th>
      <th>Actions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>Admin</td>
      <td><span class="roovix-badge roovix-badge-success">Active</span></td>
      <td class="roovix-table-actions">
        <button class="roovix-btn roovix-btn-sm">Edit</button>
      </td>
    </tr>
    <tr>
      <td>Jane Smith</td>
      <td>Editor</td>
      <td><span class="roovix-badge roovix-badge-warning">Pending</span></td>
      <td class="roovix-table-actions">
        <button class="roovix-btn roovix-btn-sm">Edit</button>
      </td>
    </tr>
  </tbody>
</table>
```

#### Table Variants

```html
<!-- Bordered table -->
<table class="roovix-table roovix-table-bordered">

<!-- Striped rows -->
<table class="roovix-table roovix-table-striped">

<!-- Small table -->
<table class="roovix-table roovix-table-sm">

<!-- Large table -->
<table class="roovix-table roovix-table-lg">
```

---

### 9. Modals

```html
<!-- Modal trigger -->
<button onclick="document.querySelector('.roovix-modal-overlay').style.display='flex'">
  Open Modal
</button>

<!-- Modal overlay -->
<div class="roovix-modal-overlay" style="display: none;">
  <div class="roovix-modal roovix-modal-md">
    <div class="roovix-modal-header">
      <h3 class="roovix-modal-title">Confirm Action</h3>
      <button class="roovix-modal-close">×</button>
    </div>
    <div class="roovix-modal-body">
      <p>Are you sure you want to delete this article?</p>
    </div>
    <div class="roovix-modal-footer">
      <button class="roovix-btn roovix-btn-secondary">Cancel</button>
      <button class="roovix-btn roovix-btn-danger">Delete</button>
    </div>
  </div>
</div>
```

#### Modal Sizes

```html
<div class="roovix-modal roovix-modal-sm">Small</div>
<div class="roovix-modal roovix-modal-md">Medium (default)</div>
<div class="roovix-modal roovix-modal-lg">Large</div>
<div class="roovix-modal roovix-modal-xl">Extra Large</div>
<div class="roovix-modal roovix-modal-full">Full screen</div>
```

---

### 10. Dropdowns

```html
<div class="roovix-dropdown">
  <button class="roovix-btn roovix-btn-secondary">Options ▼</button>
  
  <div class="roovix-dropdown-menu">
    <div class="roovix-dropdown-header">ACCOUNT</div>
    <a href="#" class="roovix-dropdown-item">Profile</a>
    <a href="#" class="roovix-dropdown-item">Settings</a>
    <div class="roovix-dropdown-divider"></div>
    <a href="#" class="roovix-dropdown-item">Logout</a>
  </div>
</div>

<script>
// Toggle dropdown
document.querySelector('.roovix-btn').addEventListener('click', function() {
  document.querySelector('.roovix-dropdown-menu').classList.toggle('show');
});
</script>
```

#### Dropdown Positions

```html
<!-- Right aligned (default) -->
<div class="roovix-dropdown-menu">...</div>

<!-- Left aligned -->
<div class="roovix-dropdown-menu roovix-dropdown-menu-left">...</div>

<!-- Centered -->
<div class="roovix-dropdown-menu roovix-dropdown-menu-center">...</div>
```

---

### 11. Tooltips

```html
<div class="roovix-tooltip">
  Hover over me
  <span class="roovix-tooltip-content">This is a tooltip</span>
</div>

<!-- Tooltip positions -->
<div class="roovix-tooltip roovix-tooltip-top">Top</div>
<div class="roovix-tooltip roovix-tooltip-bottom">Bottom</div>
<div class="roovix-tooltip roovix-tooltip-left">Left</div>
<div class="roovix-tooltip roovix-tooltip-right">Right</div>
```

---

### 12. Progress Bars

```html
<div class="roovix-progress">
  <div class="roovix-progress-bar" style="width: 75%;"></div>
</div>

<!-- With label -->
<div>
  <div class="roovix-progress-label">
    <span>Completion</span>
    <span>75%</span>
  </div>
  <div class="roovix-progress">
    <div class="roovix-progress-bar" style="width: 75%;"></div>
  </div>
</div>

<!-- Different sizes -->
<div class="roovix-progress roovix-progress-xs"></div>
<div class="roovix-progress roovix-progress-sm"></div>
<div class="roovix-progress roovix-progress-md"></div>
<div class="roovix-progress roovix-progress-lg"></div>
<div class="roovix-progress roovix-progress-xl"></div>

<!-- Different colors -->
<div class="roovix-progress roovix-progress-success"></div>
<div class="roovix-progress roovix-progress-danger"></div>
<div class="roovix-progress roovix-progress-warning"></div>
<div class="roovix-progress roovix-progress-info"></div>
```

---

### 13. Loaders / Spinners

```html
<!-- Spinner -->
<div class="roovix-loader"></div>

<!-- Different sizes -->
<div class="roovix-loader roovix-loader-xs"></div>
<div class="roovix-loader roovix-loader-sm"></div>
<div class="roovix-loader roovix-loader-md"></div>
<div class="roovix-loader roovix-loader-lg"></div>
<div class="roovix-loader roovix-loader-xl"></div>

<!-- Different colors -->
<div class="roovix-loader roovix-loader-primary"></div>
<div class="roovix-loader roovix-loader-success"></div>
<div class="roovix-loader roovix-loader-danger"></div>

<!-- Dots loader -->
<div class="roovix-loader-dots">
  <span></span><span></span><span></span>
</div>

<!-- Inside a button -->
<button class="roovix-btn roovix-btn-primary" disabled>
  <span class="roovix-loader roovix-loader-xs"></span>
  <span>Loading...</span>
</button>
```

---

### 14. Skeleton Loaders

```html
<!-- Text skeleton -->
<div class="roovix-skeleton roovix-skeleton-title"></div>
<div class="roovix-skeleton roovix-skeleton-text"></div>
<div class="roovix-skeleton roovix-skeleton-text"></div>
<div class="roovix-skeleton roovix-skeleton-text roovix-skeleton-text-sm"></div>

<!-- Avatar skeleton -->
<div class="roovix-skeleton roovix-skeleton-avatar"></div>
<div class="roovix-skeleton roovix-skeleton-avatar-sm"></div>
<div class="roovix-skeleton roovix-skeleton-avatar-lg"></div>

<!-- Button skeleton -->
<div class="roovix-skeleton roovix-skeleton-button"></div>

<!-- Card skeleton -->
<div class="roovix-skeleton roovix-skeleton-card"></div>

<!-- Complete card loading state -->
<div class="roovix-card">
  <div class="roovix-card-header">
    <div class="roovix-skeleton roovix-skeleton-title"></div>
  </div>
  <div class="roovix-card-body">
    <div class="roovix-skeleton roovix-skeleton-text"></div>
    <div class="roovix-skeleton roovix-skeleton-text"></div>
    <div class="roovix-skeleton roovix-skeleton-text roovix-skeleton-text-sm"></div>
  </div>
  <div class="roovix-card-footer">
    <div class="roovix-skeleton roovix-skeleton-button"></div>
  </div>
</div>
```

---

### 15. Lists

```html
<ul class="roovix-list">
  <li class="roovix-list-item">
    <span class="roovix-list-icon">📁</span>
    <div class="roovix-list-content">
      <div class="roovix-list-title">Project Documents</div>
      <div class="roovix-list-subtitle">24 files, 120 MB</div>
    </div>
    <div class="roovix-list-action">
      <button class="roovix-btn roovix-btn-sm">Download</button>
    </div>
  </li>
  
  <li class="roovix-list-item">
    <span class="roovix-list-icon">📊</span>
    <div class="roovix-list-content">
      <div class="roovix-list-title">Analytics Report</div>
      <div class="roovix-list-subtitle">Updated 2 hours ago</div>
    </div>
    <span class="roovix-badge roovix-badge-success">New</span>
  </li>
</ul>

<!-- List sizes -->
<ul class="roovix-list roovix-list-sm">Small items</ul>
<ul class="roovix-list">Default items</ul>
<ul class="roovix-list roovix-list-lg">Large items</ul>

<!-- Divided list (with border) -->
<ul class="roovix-list roovix-list-divided">...</ul>
```

---

### 16. Tags / Chips

```html
<span class="roovix-tag">JavaScript</span>
<span class="roovix-tag">React</span>
<span class="roovix-tag">TypeScript</span>

<!-- Removable tag -->
<span class="roovix-tag roovix-tag-removable">
  <span>Filter</span>
  <button class="roovix-tag-remove">×</button>
</span>

<!-- Tag sizes -->
<span class="roovix-tag roovix-tag-sm">Small</span>
<span class="roovix-tag">Default</span>
<span class="roovix-tag roovix-tag-lg">Large</span>

<!-- Tag colors -->
<span class="roovix-tag roovix-tag-primary">Primary</span>
<span class="roovix-tag roovix-tag-success">Success</span>
<span class="roovix-tag roovix-tag-danger">Danger</span>
```

---

### 17. Dividers

```html
<!-- Horizontal divider -->
<hr class="roovix-divider">

<!-- Vertical divider (in flex containers) -->
<div style="display: flex;">
  <span>Left</span>
  <span class="roovix-divider-vertical"></span>
  <span>Right</span>
</div>

<!-- Divider with text -->
<div class="roovix-divider-label">OR CONTINUE WITH</div>
```

---

### 18. Utility Classes

#### Text Colors

```html
<p class="roovix-text-primary">Primary text</p>
<p class="roovix-text-secondary">Secondary text</p>
<p class="roovix-text-tertiary">Tertiary text</p>
<p class="roovix-text-success">Success text</p>
<p class="roovix-text-danger">Danger text</p>
<p class="roovix-text-warning">Warning text</p>
<p class="roovix-text-info">Info text</p>
<p class="roovix-text-link">Link text</p>
```

#### Background Colors

```html
<div class="roovix-bg-primary">Primary background</div>
<div class="roovix-bg-secondary">Secondary background</div>
<div class="roovix-bg-success">Success background</div>
<div class="roovix-bg-danger">Danger background</div>
```

#### Borders

```html
<div class="roovix-border">All sides</div>
<div class="roovix-border-top">Top only</div>
<div class="roovix-border-bottom">Bottom only</div>
<div class="roovix-border-left">Left only</div>
<div class="roovix-border-right">Right only</div>
<div class="roovix-border-success">Success border</div>
<div class="roovix-border-danger">Danger border</div>
```

#### Shadows

```html
<div class="roovix-shadow-none">No shadow</div>
<div class="roovix-shadow-xs">Extra small shadow</div>
<div class="roovix-shadow-sm">Small shadow</div>
<div class="roovix-shadow-md">Medium shadow</div>
<div class="roovix-shadow-lg">Large shadow</div>
<div class="roovix-shadow-floating-sm">Floating shadow</div>
```

#### Spacing

```html
<div class="roovix-m-4">Margin 16px</div>
<div class="roovix-p-4">Padding 16px</div>
<div class="roovix-mx-auto">Center horizontally</div>
```

#### Flex

```html
<div class="roovix-flex roovix-items-center roovix-justify-between">
  <span>Left</span>
  <span>Right</span>
</div>
```

---

## 🌓 Dark Mode

### How It Works

Dark mode is controlled by the `data-theme` attribute on the HTML tag:

```html
<!-- Light mode -->
<html data-theme="light">

<!-- Dark mode -->
<html data-theme="dark">
```

### Theme Switcher Component

```html
<button onclick="toggleRoovixTheme()" class="roovix-btn roovix-btn-secondary">
  <span class="light-icon">☀️</span>
  <span class="dark-icon">🌙</span>
  <span>Toggle Theme</span>
</button>

<style>
.light-icon, .dark-icon {
  display: inline-block;
}
[data-theme="light"] .dark-icon,
[data-theme="dark"] .light-icon {
  display: none;
}
</style>

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
if (savedTheme) {
  document.documentElement.setAttribute('data-theme', savedTheme);
} else if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
  document.documentElement.setAttribute('data-theme', 'dark');
}
</script>
```

---

## 💻 How to Use

### In HTML

```html
<!-- Add classes directly to elements -->
<button class="roovix-btn roovix-btn-primary">Click me</button>
<div class="roovix-card roovix-card-shadow-md">Content</div>
```

### In CSS

```css
/* Use CSS variables */
.custom-component {
  background-color: var(--roovix-bg-primary);
  color: var(--roovix-text-primary);
  padding: var(--space-4);
  border: 1px solid var(--roovix-border-default);
  border-radius: var(--radius-md);
}

/* Use component classes */
.custom-component {
  composes: roovix-card roovix-card-shadow-sm;
}
```

### In React

```jsx
function Button({ children, variant = 'primary', size = 'base' }) {
  return (
    <button className={`roovix-btn roovix-btn-${variant} roovix-btn-${size}`}>
      {children}
    </button>
  );
}

// Usage
<Button variant="primary" size="lg">Click me</Button>
```

### In Vue

```vue
<template>
  <button :class="['roovix-btn', `roovix-btn-${variant}`, `roovix-btn-${size}`]">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    variant: { default: 'primary' },
    size: { default: 'base' }
  }
}
</script>
```

---

## 📱 Responsive Design

The design system is mobile-first with these breakpoints:

```css
/* Mobile (default) */
.element { ... }

/* Tablet (640px and up) */
@media (min-width: 640px) {
  .element { ... }
}

/* Desktop (1024px and up) */
@media (min-width: 1024px) {
  .element { ... }
}
```

### Responsive Classes

```html
<div class="roovix-flex roovix-sm\:flex roovix-lg\:flex">
  <!-- Shows/hides at different breakpoints -->
</div>

<div class="roovix-hidden roovix-md\:block">
  <!-- Hidden on mobile, visible on tablet and up -->
</div>
```

---

## ✅ Best Practices

### DO's

```html
<!-- ✓ Use our semantic class names -->
<button class="roovix-btn roovix-btn-primary">Save</button>

<!-- ✓ Use size variants consistently -->
<button class="roovix-btn roovix-btn-sm">Small</button>
<button class="roovix-btn roovix-btn-base">Default</button>

<!-- ✓ Use our utility classes -->
<div class="roovix-flex roovix-items-center roovix-gap-2">
  <span>Icon</span>
  <span>Text</span>
</div>

<!-- ✓ Test in both light and dark modes -->
```

### DON'Ts

```html
<!-- ✗ Don't hardcode colors -->
<button style="background: blue;">Bad</button>

<!-- ✗ Don't create custom sizes -->
<div style="padding: 13px;">Inconsistent</div>

<!-- ✗ Don't forget the roovix- prefix -->
<button class="btn-primary">Wrong</button>

<!-- ✗ Don't override component styles directly -->
.roovix-btn-primary {
  background: purple; /* Don't do this */
}
```

---

## ❌ Troubleshooting

### Common Issues

| Problem | Solution |
|---------|----------|
| **Styles not loading** | Check if CSS files are linked correctly |
| **Wrong colors** | Verify `data-theme` attribute is set |
| **Components look wrong** | Make sure you're using `roovix-` prefix |
| **Dark mode not working** | Check if `data-theme="dark"` is on HTML tag |
| **Spacing issues** | Use our spacing variables instead of custom values |

### Quick Fixes

```html
<!-- If dark mode isn't working, check this -->
<html data-theme="dark"> <!-- Must be on html tag, not body -->

<!-- If styles are conflicting, add !important temporarily -->
<div style="color: var(--roovix-text-primary) !important;">Test</div>
```

---

## ❓ FAQ

### Q: Can I use this with Tailwind CSS?
**A:** Yes! Our design system works great alongside Tailwind. Just use our classes for components and Tailwind for layouts.

### Q: How do I create a new component?
**A:** Use our CSS variables for consistency:
```css
.my-new-component {
  background: var(--roovix-bg-primary);
  color: var(--roovix-text-primary);
  padding: var(--space-4);
  border-radius: var(--radius-md);
}
```

### Q: Do I need to include both CSS files?
**A:** Yes. `roovix-base.css` has all the variables, and `roovix-components.css` has the actual components.

### Q: How do I customize a component?
**A:** Create a new class and combine with ours:
```html
<div class="roovix-card my-special-card">
  <!-- Your custom styles in my-special-card -->
</div>
```

### Q: Does it work with frameworks?
**A:** Yes! Works with React, Vue, Angular, and vanilla HTML.

### Q: How do I add new colors?
**A:** Extend the variables in your own CSS:
```css
:root {
  --roovix-brand-color: #ff0000;
}

[data-theme="dark"] {
  --roovix-brand-color: #ff6666;
}
```

---

## 📚 Quick Reference

### Most Used Classes

```html
<!-- Buttons -->
roovix-btn roovix-btn-primary
roovix-btn roovix-btn-secondary
roovix-btn roovix-btn-danger

<!-- Cards -->
roovix-card
roovix-card-header
roovix-card-body
roovix-card-footer

<!-- Avatars -->
roovix-avatar roovix-avatar-md

<!-- Badges -->
roovix-badge roovix-badge-success

<!-- Forms -->
roovix-input
roovix-form-group
roovix-form-label

<!-- Alerts -->
roovix-alert roovix-alert-info

<!-- Utilities -->
roovix-text-primary
roovix-bg-secondary
roovix-flex roovix-items-center
```

---

## 🆘 Getting Help

- **Email**: design-system@roovix.com

---

<div align="center">

**Made with ❤️ by the Roovix Team**

[![YouTube](https://img.shields.io/badge/YouTube-Subscribe-red?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@roovix)

**Version 2.0.0 | Last Updated: March 2024**

</div>
