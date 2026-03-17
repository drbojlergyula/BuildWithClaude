# /add-project Command

<!-- What is a command?
     A command is a shortcut you type in Claude Code (e.g. /add-project) to run a
     multi-step task without having to explain every step. This one guides you through
     adding a new completed project to the Dream Home Design portfolio.
     Edit the steps below to match your own project structure if needed. -->

Adds a new completed interior design project to the portfolio.

## When to use it

Run `/add-project` whenever the studio completes a new project and wants to add it to the website.

## Steps

1. Ask the user for the project details:
   - Project name
   - Location (city, country)
   - Short description (2–3 sentences about the style and scope)
   - Number of photos to be added
2. Create a new entry in `data/projects.json` with the details provided
3. Create a new image folder under `images/projects/[project-slug]/`
4. Remind the user to add the project photos to that folder, sized to 1200×800px and under 300KB each
5. Confirm the new project card appears correctly on `projects.html`
6. Report: "Project added. Drop your photos into `images/projects/[project-slug]/` and the gallery will update automatically."

## Dream Home Design example

```
User runs: /add-project

Claude asks:
  Project name? → "Villa Rosenberg – Living & Dining"
  Location? → "Vienna, Austria"
  Description? → "Full redesign of an 80m² open-plan living and dining area.
                  Warm oak tones, custom built-in shelving, and natural linen fabrics."

Claude then:
  → Adds entry to data/projects.json
  → Creates folder: images/projects/villa-rosenberg/
  → Reports: "Done. Add your photos to images/projects/villa-rosenberg/
              (1200×800px, max 300KB each). The project card will appear
              on the portfolio page automatically."
```
