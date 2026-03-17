# Pre-Launch Checklist Skill

<!-- What is a skill?
     A skill is a focused, reusable task Claude runs on demand. This one walks through
     everything that should work before you share the site with the world.
     Update the checklist below to match your own site's features. -->

Verifies that all key features of the site work correctly before going live.

## Steps

1. Work through the checklist below page by page
2. Mark each item as passed or failed
3. For anything that fails, explain what is broken and how to fix it
4. Report a final summary: ready to launch, or items to fix first

## Checklist

<!-- Replace or add items to match your own site. -->

**All pages**
- [ ] Page loads without errors in the browser console
- [ ] Navigation works on desktop (all links go to the right pages)
- [ ] Navigation works on mobile (hamburger menu opens and closes)
- [ ] Footer shows correct studio name, email, and phone number
- [ ] No placeholder text visible ("Lorem ipsum", "Coming soon", example@email.com)

**Homepage**
- [ ] Hero image loads and looks correct on mobile and desktop
- [ ] "View Our Work" button scrolls to or links to the portfolio section
- [ ] Instagram feed loads (or fallback message shown if feed is unavailable)

**Portfolio / Projects page**
- [ ] All project cards display with a photo, name, and location
- [ ] Clicking a project card opens the correct photo gallery
- [ ] Gallery closes correctly (click outside or press Escape)

**Contact page**
- [ ] Submitting the form with empty fields shows a validation error
- [ ] Submitting with valid details sends the email to the studio
- [ ] A confirmation message appears after successful submission

**Performance**
- [ ] All images load in under 3 seconds on a standard connection
- [ ] No images larger than 500KB

## Dream Home Design example

*Full checklist run before the site goes live:*
```
✅ 14 / 16 items passed

❌ Instagram feed: Not loading — API token missing from environment variables
❌ Contact form: No confirmation message shown after submission — check contact.js line 47

Ready to launch once these 2 items are fixed.
```
