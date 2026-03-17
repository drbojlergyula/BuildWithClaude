# Architecture

This document describes the high-level system architecture, data flow, and component relationships.

## System Overview

<!-- Replace with a description of your app's stack and architecture. Example: -->

This is a modern HTML + JavaScript application with a lightweight Node.js backend. The frontend is plain HTML/CSS/JS served as static files; the backend exposes a REST API that the frontend calls via `fetch`.

## Data Flow

<!-- Replace with your app's actual data flow. Example: -->

```
User interacts with the UI
      ↓
JavaScript handles event and validates input
      ↓
fetch() → POST /api/data { payload }
      ↓
Server processes request and queries database
      ↓
JSON response returned
      ↓
JavaScript updates the DOM with the result
```

## Component Architecture

<!-- List the key files and folders in your project, grouped by layer. Describe what each does. Example: -->

### Pages

- `index.html` — Homepage with hero section, featured services, and image gallery
- `about.html` — Company story, team bios, and office photos
- `contact.html` — Contact form with validation and Google Maps embed

### JavaScript Modules

- `js/main.js` — Page init, mobile nav toggle, smooth scroll
- `js/gallery.js` — Lightbox image viewer with keyboard navigation
- `js/contact.js` — Contact form validation and `fetch`-based submission

### Styles

- `css/styles.css` — Global styles, layout, typography
- `css/components.css` — Reusable UI components (cards, buttons, forms)

### Assets

- `images/` — Optimized photos (hero banner, team headshots, gallery)

### API Layer

<!-- List your backend endpoints if you have a server. Example: -->

- `/api/contact` — Accepts form submission and sends notification email
