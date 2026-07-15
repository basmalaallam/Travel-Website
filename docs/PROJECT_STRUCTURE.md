# Project structure and integration

## Purpose

This repository contains the presentation layer for a travel discovery experience. It is intentionally framework-light: EJS templates are separated from public image assets and can be integrated into an Express application without modifying the templates.

## Directory conventions

| Location | Purpose |
| --- | --- |
| `views/` | EJS templates rendered by the host server. |
| `public/` | Static travel and background images referenced by the templates. |
| `docs/screenshots/` | Documentation-only screenshots and README placeholders. |

## Integration requirements

The host application is responsible for:

- Configuring EJS as the view engine.
- Serving `public/` as the static-assets directory.
- Providing GET and POST routes referenced in the templates.
- Supplying any authentication, search, persistence, or validation behavior.

The supplied templates deliberately contain no application server, package manifest, database configuration, or credentials. This keeps the bundle portable, but it means the repository cannot be run standalone.

## Screenshot guidance

Use screenshots that show the project running in its intended host application. Store them in `docs/screenshots/` and keep a consistent aspect ratio (for example, 16:9). Avoid including personal data, browser extensions, or local file paths.

Recommended captures:

1. Home/category selection page (`home.png`).
2. A representative destination detail page (`destination.png`).
3. Optional: search or want-to-go flow (`search.png`).

Update the README image links when replacing the SVG placeholders.
