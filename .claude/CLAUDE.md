# Jakob Schumacher Personal Website - Claude Context

## Project Overview

This is a personal website for Jakob Schumacher (Infektionsepidemiologe, Mediziner, Data scientist und Dozent), migrated from Jekyll to Hugo for better performance, security, and SEO.

## Technology Stack

- **Static Site Generator**: Hugo v0.152.2+
- **Theme**: PaperMod (as git submodule)
- **Language**: German (de-de)
- **Hosting**: GitHub Pages with GitHub Actions
- **Deployment**: Automatic on push to master

## Project Structure

- `content/posts/`: Blog posts (previously _posts/ in Jekyll)
- `static/`: Static assets (images, js, favicon)
- `themes/PaperMod/`: PaperMod theme (git submodule)
- `layouts/_default/`: Custom layout overrides (single.html)
- `hugo.toml`: Main configuration file
- `.github/workflows/`: GitHub Actions deployment workflow

## Key Features

1. **SEO Optimized**: Built-in sitemap, robots.txt, Open Graph tags, canonical URLs
2. **Performance**: Fast build times (<100ms), optimized assets
3. **German Localization**: Date formats and UI in German
4. **Cover Images**: Kurzgeschichten have Unsplash images (hidden in lists, shown in posts)
5. **Project Links**: Posts with "webseite" field display clickable links
6. **Automatic Deployment**: GitHub Actions workflow for push-to-deploy

## Development Workflow

### Running Development Server

```bash
hugo server -D
```

### Building the Site

```bash
hugo --gc --minify
```

### Creating New Posts

```bash
hugo new posts/post-title.md
```

### Deployment

Push to master branch - GitHub Actions automatically builds and deploys to GitHub Pages.

## Content Guidelines

### Post Front Matter

Posts should include:
- `title`: Post title
- `date`: Publication date (YYYY-MM-DD HH:MM:SS +0100)
- `tags`: Array of tags (e.g., [Projekt])
- `beschreibung`: Optional description

### Project Posts

Project posts use additional front matter:
- `webseite`: URL to the project (automatically linked below description)
- `beschreibung`: Description of the project

### Kurzgeschichten (Short Stories)

Short stories can include cover images:
```yaml
cover:
  image: "/images/filename.jpg"
  alt: "Image description"
  caption: "Photo credit with link"
  hiddenInList: true
```

## Theme Customization

PaperMod theme with custom modifications:
- **Custom single.html layout**: Displays webseite URL for project posts
- **German date format**: "2. January 2006" format
- **Theme toggle disabled**: Light mode only
- **Configuration**: All in hugo.toml (params must come before sub-sections)

## Important Notes

- Do not use emojis
- Keep design minimal and clean
- Focus on performance and SEO
- All content in German
- Build must pass before committing

## Migration History

**2025-10-17**: Migrated from Jekyll to Hugo
- Posts moved from _posts/ to content/posts/
- Converted .markdown to .md
- Updated front matter for Hugo compatibility
- Created custom minimal theme

**2025-11-12**: Updated to PaperMod theme
- Switched from custom theme to PaperMod
- Added German localization
- Implemented cover images for short stories
- Added automatic webseite URL display
- Set up GitHub Actions deployment
- Disabled theme toggle (light mode only)
