# CLAUDE.md - AI Agent Instructions

## Project Overview

Personal portfolio and blog for Manish Goel, hosted at https://magoel.github.io/

## Tech Stack

- **Static Site Generator**: Eleventy (11ty) v2.x
- **Templating**: Nunjucks (.njk files)
- **Styling**: Plain CSS (no preprocessor)
- **Hosting**: GitHub Pages via GitHub Actions
- **Content**: Markdown for blog posts

## Project Structure

```
magoel.github.io/
├── src/                    # Source files (Eleventy input)
│   ├── _includes/          # Layouts and partials
│   │   ├── base.njk        # Base HTML layout (head, nav, footer)
│   │   └── post.njk        # Blog post template
│   ├── posts/              # Blog posts as Markdown files
│   ├── css/
│   │   └── style.css       # All styles (light theme)
│   ├── img/                # Images (profile photo, etc.)
│   ├── index.njk           # Home page
│   └── blog.njk            # Blog listing page
├── _site/                  # Build output (gitignored)
├── .eleventy.js            # Eleventy configuration
├── package.json            # Dependencies and scripts
└── .github/workflows/
    └── deploy.yml          # Auto-deploy to GitHub Pages
```

## Common Tasks

### Add a New Blog Post

1. Create `src/posts/your-post-slug.md`
2. Include frontmatter:
   ```markdown
   ---
   title: Your Post Title
   date: YYYY-MM-DD
   description: Brief description for listing page.
   layout: post.njk
   ---
   
   Post content in Markdown...
   ```
3. Posts auto-sort by date (newest first)

### Modify Home Page Content

Edit `src/index.njk` - it contains all sections:
- Hero (photo, name, tagline, links)
- About
- Experience Highlights
- Skills
- Education
- Contact

### Change Styling

Edit `src/css/style.css` - organized sections:
- Reset & Base
- Typography
- Layout (header, main, footer)
- Hero Section
- Content Sections
- Blog List
- Single Post
- Responsive breakpoints at bottom

### Add New Pages

1. Create `src/your-page.njk`
2. Add frontmatter with layout:
   ```njk
   ---
   layout: base.njk
   title: Page Title
   ---
   ```
3. Add nav link in `src/_includes/base.njk`

## Build Commands

```bash
npm install      # Install dependencies (first time)
npm run serve    # Local dev server at http://localhost:8080
npm run build    # Build to _site/ folder
npm run clean    # Remove _site/ folder
```

## Deployment

- **Automatic**: Push to `main` branch triggers GitHub Actions
- **Workflow**: `.github/workflows/deploy.yml`
- **Build**: Eleventy generates `_site/`, deployed to GitHub Pages
- **URL**: https://magoel.github.io/

## Conventions

- **File naming**: Use kebab-case for posts (`my-new-post.md`)
- **Dates**: Use ISO format (YYYY-MM-DD) in frontmatter
- **Images**: Place in `src/img/`, reference as `/img/filename.ext`
- **Links**: Use absolute paths from root (`/blog/`, `/img/photo.jpg`)
- **CSS**: Add new styles at the end of relevant section, keep mobile styles in `@media` block at bottom

## Key Files Reference

| File | Purpose |
|------|---------|
| `.eleventy.js` | Input/output dirs, collections, filters |
| `src/_includes/base.njk` | HTML shell, nav, footer |
| `src/_includes/post.njk` | Blog post wrapper |
| `src/index.njk` | Home page content |
| `src/blog.njk` | Blog listing with posts loop |
| `src/css/style.css` | All styling |

## Owner Info

- **Name**: Manish Goel
- **Email**: manish.dce@gmail.com
- **GitHub**: https://github.com/magoel
- **Site**: https://magoel.github.io/
