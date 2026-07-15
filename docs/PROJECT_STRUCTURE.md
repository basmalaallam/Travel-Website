# Project structure and integration

## Purpose

This repository contains the presentation layer for a travel discovery experience. It is intentionally framework-light: EJS templates are separated from public image assets and can be integrated into an Express application without modifying the templates.

## Directory conventions

| Location | Purpose |
| --- | --- |
| `views/` | EJS templates rendered by the host server. |
| `public/` | Static travel and background images referenced by the templates. |
| README demo link | Public Google Drive walkthrough of the application. |

## Integration requirements

The host application is responsible for:

- Configuring EJS as the view engine.
- Serving `public/` as the static-assets directory.
- Providing GET and POST routes referenced in the templates.
- Supplying any authentication, search, persistence, or validation behavior.

The supplied templates deliberately contain no application server, package manifest, database configuration, or credentials. This keeps the bundle portable, but it means the repository cannot be run standalone.

## Demo guidance

The README links to the public Google Drive walkthrough supplied for this project. If the demo is replaced, update that link and ensure the shared file does not expose personal data or credentials.
