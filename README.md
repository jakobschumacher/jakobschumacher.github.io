# Persönliche Webseite von Jakob Schumacher

Diese Webseite wurde von Jekyll zu Hugo migriert für bessere Performance, Sicherheit und SEO.

## Technologie

- **Static Site Generator**: Hugo v0.152.2+
- **Theme**: PaperMod (git submodule)
- **Hosting**: GitHub Pages mit GitHub Actions

## Vorteile der Hugo-Migration

1. **Performance**: Hugo ist extrem schnell - Build-Zeiten unter 100ms
2. **Sicherheit**: Keine Ruby-Abhängigkeiten mehr, keine Sicherheitslücken in Jekyll-Plugins
3. **SEO**: Eingebaute SEO-Features (Sitemap, robots.txt, Open Graph Tags)
4. **Wartbarkeit**: Einfachere Struktur, keine komplexen Dependencies

## Lokale Entwicklung

### Voraussetzungen

- Hugo v0.123.7 oder neuer

### Site bauen

```bash
hugo
```

### Development Server starten

```bash
hugo server -D
```

Die Website ist dann unter `http://localhost:1313` verfügbar.

## Struktur

```
.
├── content/posts/        # Blog-Posts
├── static/              # Statische Assets (Bilder, JS, CSS)
├── themes/PaperMod/     # PaperMod Theme (Submodule)
├── layouts/_default/    # Custom Layout-Overrides
├── .github/workflows/   # GitHub Actions Deployment
└── hugo.toml           # Konfiguration
```

## Neue Posts erstellen

```bash
hugo new posts/mein-neuer-post.md
```

## Deployment

Die Website wird automatisch via GitHub Actions deployed:

1. Änderungen committen
2. Push zu `master` Branch
3. GitHub Actions baut und deployed automatisch

Manueller Build (optional):
```bash
hugo --gc --minify
```

## SEO Features

- Automatische Sitemap-Generierung (`/sitemap.xml`)
- robots.txt
- Open Graph Meta Tags
- Kanonische URLs
- Saubere, semantische HTML-Struktur
- Schnelle Ladezeiten

## Migration Notes

- Alle Posts aus `_posts/` wurden nach `content/posts/` migriert
- Front Matter wurde für Hugo angepasst
- Custom shortcodes für Projekt-Listings
- Minimales, performance-optimiertes Theme
