# magoel.github.io

Personal portfolio and blog of Manish Goel, built with [Eleventy](https://www.11ty.dev/).

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start local dev server (http://localhost:8080)
npm run serve

# Build for production
npm run build
```

## 📁 Project Structure

```
├── src/
│   ├── _includes/        # Layouts and templates
│   │   ├── base.njk      # Base HTML layout
│   │   └── post.njk      # Blog post layout
│   ├── posts/            # Blog posts (Markdown)
│   ├── css/              # Stylesheets
│   ├── img/              # Images
│   ├── index.njk         # Home page
│   └── blog.njk          # Blog listing page
├── .eleventy.js          # Eleventy configuration
├── package.json          # Dependencies and scripts
└── .github/workflows/    # GitHub Actions for auto-deploy
```

## ✍️ Adding a New Blog Post

Create a new `.md` file in `src/posts/`:

```markdown
---
title: Your Post Title
date: 2026-02-15
description: A brief description of your post.
layout: post.njk
---

Your content here...
```

## 🌐 Deployment

The site automatically deploys to GitHub Pages when you push to `main`:

1. Push changes to `main` branch
2. GitHub Actions builds the site with Eleventy
3. Built files deploy to GitHub Pages
4. Site live at https://magoel.github.io/

## 📝 License

MIT
