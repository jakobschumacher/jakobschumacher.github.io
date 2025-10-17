# Persönliche Webseite von Jakob Schumacher

Diese Webseite wurde von Jekyll zu Hugo migriert für bessere Performance, Sicherheit und SEO.

## Technologie

- **Static Site Generator**: Hugo v0.123.7+
- **Theme**: Minimal (custom theme)
- **Hosting**: GitHub Pages ready

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
├── content/          # Inhalte (Posts, Seiten)
│   ├── posts/       # Blog-Posts
│   └── epiprojects.md
├── static/          # Statische Assets (Bilder, JS, CSS)
├── themes/minimal/  # Custom minimal theme
├── layouts/         # Custom layouts und shortcodes
└── hugo.toml       # Konfiguration
```

## Neue Posts erstellen

```bash
hugo new posts/mein-neuer-post.md
```

## Deployment

### GitHub Pages

1. Build mit `hugo --gc --minify`
2. Pushe die generierten Dateien im `public/` Ordner

### Alternativ: GitHub Actions

GitHub Actions können automatisch den Build-Prozess übernehmen.

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
