# SEO Reviewer Agent

<!-- What is an agent?
     An agent is a specialist Claude hands off to for a focused, multi-step task.
     This one audits every page of your site for SEO issues that affect how well
     you show up on Google. You don't need to change this file — just run it before
     launch or after adding new pages. -->

A specialised agent that reviews every page of the site for SEO best practices.

## What it checks

- Every page has a unique `<title>` tag (ideally 50–60 characters)
- Every page has a `<meta name="description">` (ideally 120–160 characters)
- Every image has an `alt` attribute describing what is shown
- Pages use a single `<h1>` heading, with `<h2>` and `<h3>` used correctly below it
- Internal links use descriptive text (not "click here" or "read more")
- No pages return a 404 or link to a broken URL

## Output format

Produces a report per page:

- **Fix before launch** — missing or duplicate titles, missing meta descriptions, images without alt text
- **Recommended** — improvements that would help rankings but are not blocking
- **Looks good** — nothing to action

## Dream Home Design example

*Running this agent before launch would check all four pages:*

| Page | Check | Result |
|---|---|---|
| `index.html` | `<title>` tag | "Dream Home Design – Interior Design Studio, Vienna" ✅ |
| `projects.html` | Image alt text | 4 of 12 project images missing alt text ❌ |
| `contact.html` | Meta description | Missing — add one describing the contact page ❌ |
| `about.html` | Single `<h1>` | Two `<h1>` tags found — demote one to `<h2>` ❌ |
