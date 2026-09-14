# Blog redesign patch

This patch keeps the current Jekyll/GitHub Pages architecture and changes only presentation/layout.

## Replace these files in the repository

- `_config.yml`
- `_layouts/default.html`
- `_layouts/page.html`
- `_layouts/post.html`
- `assets/css/site.css`
- `index.md`
- `blog.md`

## What changes

- narrower, quieter reading column
- simplified header inspired by text-first personal sites
- removes redundant Home link and visible tagline from the header
- rectangular portrait instead of pill/circle portrait
- article lists show title + month/year + subtitle
- post pages render front-matter subtitle and use natural-language dates
- first Markdown H1 inside posts is hidden to avoid duplicate titles
- improved long-form typography
- minimal light/dark toggle
- removes the redundant Explore section from the homepage
- homepage becomes intro → essays → research → contact

## Important

The visual direction is inspired by the restraint of nabeelqu.co, not copied. The typography, proportions, content hierarchy, and details are adapted to Adela's research + essay site.

For the best article lists, keep adding a `subtitle:` field to each post's front matter.
