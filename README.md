# Adela — minimal Jekyll site

This is a minimal, text-first Jekyll site intended to be deployed on GitHub Pages via GitHub Actions.

## Local preview
1. Install Ruby + Bundler.
2. `bundle install`
3. `bundle exec jekyll serve`
4. Open http://localhost:4000

## Deploy on GitHub Pages
- In GitHub: Settings → Pages → Source = GitHub Actions.
- Commit and push; Actions will build and deploy.

## Customize
- Edit `_config.yml` (title, description, `url`).
- Put your email + social links into `/contact/`.
- Add posts to `_posts/` (Markdown).
