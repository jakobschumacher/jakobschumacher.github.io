# Jakob Schumacher Personal Website - Claude Context

## Project Overview

This is a personal website for Jakob Schumacher (Infektionsepidemiologe, Mediziner, Data scientist und Dozent), migrated from Jekyll to Hugo for better performance, security, and SEO.

## Technology Stack

- **Static Site Generator**: Hugo v0.123.7+
- **Theme**: Custom minimal theme (themes/minimal/)
- **Language**: German (de-de)
- **Hosting**: GitHub Pages

## Project Structure

- `content/posts/`: Blog posts (previously _posts/ in Jekyll)
- `content/epiprojects.md`: Projects page
- `static/`: Static assets (images, js, favicon)
- `themes/minimal/`: Custom lightweight theme
- `layouts/shortcodes/`: Custom shortcodes (e.g., projects-list.html)
- `hugo.toml`: Main configuration file

## Key Features

1. **SEO Optimized**: Built-in sitemap, robots.txt, Open Graph tags, canonical URLs
2. **Performance**: Minimal CSS, no JavaScript dependencies, fast build times (<100ms)
3. **Security**: No Ruby dependencies, no security vulnerabilities from Jekyll plugins
4. **Maintainability**: Simple structure, easy to update

## Development Workflow

### Building the Site

```bash
hugo --gc --minify
```

### Running Development Server

```bash
hugo server -D
```

### Creating New Posts

```bash
hugo new posts/post-title.md
```

## Content Guidelines

### Post Front Matter

Posts should include:
- `title`: Post title
- `date`: Publication date (YYYY-MM-DD HH:MM:SS +0100)
- `tags`: Array of tags (e.g., [Projekt])
- `beschreibung`: Optional description

### Project Posts

Project posts use additional front matter:
- `webseite`: URL to the project
- `beschreibung`: Description of the project

## Theme Customization

The minimal theme includes:
- **Head partial**: SEO meta tags, minimal inline CSS
- **Header partial**: Site title, navigation, subtitle
- **Footer partial**: Copyright notice
- **Layouts**: list.html, single.html, index.html
- **Shortcodes**: projects-list.html for displaying projects

## Important Notes

- Do not use emojis
- Keep design minimal and clean
- Focus on performance and SEO
- All content in German
- Build must pass before committing

## Migration History

Migrated from Jekyll on 2025-10-17:
- Posts moved from _posts/ to content/posts/
- Converted .markdown to .md
- Updated front matter for Hugo compatibility
- Created custom minimal theme
- Preserved all content and static assets
