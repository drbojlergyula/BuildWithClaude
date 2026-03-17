# Content Check Skill

<!-- What is a skill?
     A skill is a focused, reusable task Claude runs on demand. This one scans your
     site for content problems before it goes live or after big edits — things like
     placeholder text left in by accident, images without descriptions, or links that
     don't go anywhere yet. -->

Scans all pages for content problems that should be fixed before the site is seen by visitors.

## Steps

1. Read every `.html` file in the project
2. Check for:
   - Placeholder text: "Lorem ipsum", "Coming soon", "TBD", "Insert text here", "Your name"
   - Links pointing to `#`, `javascript:void(0)`, or `localhost`
   - Images missing an `alt` attribute
   - Empty headings or paragraphs (`<h2></h2>`, `<p></p>`)
   - Contact details still showing example values ("info@example.com", "+1 234 567 890")
3. Output a checklist of findings grouped by page

## Dream Home Design example

*Running this skill before the site launch:*

```
index.html
  ❌ Line 34: Image missing alt text — <img src="images/hero/living-room.jpg">
  ❌ Line 89: Placeholder email found — "info@example.com" in footer
  ✅ No Lorem ipsum text found

about.html
  ✅ All good

projects.html
  ❌ Line 12: Link points to "#" — portfolio filter button not wired up yet
  ❌ Line 56: Image missing alt text — project card thumbnail

contact.html
  ✅ All good

Summary: 4 issues found across 2 pages. Fix before launch.
```
