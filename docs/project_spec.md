# Project Spec

This document defines **what** you are building and **why**. It covers product requirements and engineering decisions.
For the technical breakdown of how it is built (file structure, data flow, components), see [Architecture](docs/architecture.md).

---

# Part 1: Product Requirements

<!-- Describe your product clearly enough that someone unfamiliar with it would understand what it does, who it's for, and why it exists. Be specific — vague requirements lead to the wrong product being built. -->

## What Is This Product?

<!-- One paragraph. What does it do, and what problem does it solve? Example: -->

Dream Home Design is a company website for an interior design studio. It introduces the studio, showcases completed projects with photos, and lets potential clients get in touch. It also displays the studio's live Instagram feed so visitors see the latest work without the site needing manual updates.

## Who Is It For?

<!-- Who are your users? What do they want to do? Example: -->

- **Potential clients** — people looking for an interior designer who want to see the quality of work and get a feel for the studio's style before making contact
- **The studio team** — they need to be able to update project references and contact details without a developer

## Features & User Stories

<!-- List the key features. Write each as: "A [user] can [do something] so that [goal]."
     Be specific. Bad: "Users can view projects." Good: "A visitor can browse completed projects displayed as photo cards with a short description, so they can evaluate the studio's style." -->

### Homepage
- A visitor can see a full-screen hero image with the studio's tagline and a "View Our Work" button, so they immediately understand what the studio does.
- A visitor can read a short "About Us" summary with a photo of the team, so they feel a personal connection before exploring further.

### Project References (Portfolio)
- A visitor can browse completed projects displayed as a grid of photo cards, each with a project name, location, and short description.
- A visitor can click a project card to open a larger image gallery for that project, so they can see the full scope of the work.

### Instagram Feed
- A visitor can see the studio's latest Instagram posts embedded on the homepage, so the site always feels current without manual updates.

### Contact Form
- A visitor can fill in their name, email, phone number, and a message, so they can enquire about a project.
- The studio receives an email notification for each submission.
- The visitor sees a confirmation message after submitting, so they know it was received.

### General
- All pages are fully responsive and work well on mobile, tablet, and desktop.
- The site loads quickly, with images optimised for the web.

---

# Part 2: Engineering Requirements

<!-- This section captures the technical decisions for your project. If you are not sure about some of these, leave them blank and discuss with your developer. -->

## Tech Stack

<!-- Replace with your chosen technologies. Example: -->

| Layer | Technology | Notes |
|---|---|---|
| Frontend | HTML, CSS, JavaScript | No framework needed for a simple company site |
| Styling | Tailwind CSS | Utility-first, easy to customise |
| Backend | Node.js + Express | Handles contact form submissions only |
| Email | Resend (or Nodemailer) | Sends notification email on form submit |
| Instagram Feed | Instagram Basic Display API | Embedded on homepage |
| Hosting | Netlify or Vercel | Static site + serverless function for the form |

## System Design Preferences

<!-- These are decisions that keep the codebase consistent. Agree on them upfront. Example: -->

- **API style:** REST (simple fetch calls, no GraphQL needed for this project)
- **File structure:** Layer-based (`/pages`, `/css`, `/js`, `/images`) — straightforward for a small site
- **Naming convention:** kebab-case for files (`project-card.js`), camelCase for JavaScript variables
- **No database:** Project references are stored as static JSON or Markdown files edited directly — no CMS needed for MVP

## API Design

<!-- Document any backend endpoints your project needs. Example: -->

### POST /api/contact

Receives the contact form submission and sends an email to the studio.

**Request:**
```json
{
  "name": "string",
  "email": "string",
  "phone": "string (optional)",
  "message": "string"
}
```

**Response (success):**
```json
{
  "success": true,
  "message": "Thank you, we will be in touch shortly."
}
```

**Response (error):**
```json
{
  "success": false,
  "error": "VALIDATION_ERROR | SEND_FAILED",
  "message": "Human-readable error message"
}
```

## Project Structure

<!-- Show the folder and file layout. See [Architecture](docs/architecture.md) for a detailed description of each file's role. Example: -->

```
dreamhomedesign/
├── index.html              # Homepage
├── projects.html           # Full portfolio grid
├── contact.html            # Contact form page
├── css/
│   ├── styles.css          # Global styles and layout
│   └── components.css      # Cards, buttons, forms
├── js/
│   ├── main.js             # Nav, scroll, page init
│   ├── gallery.js          # Project photo lightbox
│   ├── instagram.js        # Instagram feed embed
│   └── contact.js          # Form validation + submission
├── images/
│   ├── hero/               # Full-screen hero images
│   ├── projects/           # Project reference photos
│   └── team/               # Team headshots
├── data/
│   └── projects.json       # Project references (edit to add new work)
├── api/
│   └── contact.js          # Serverless function — email handler
└── .env.example            # Required environment variables
```
