# Project structure and integration

## Purpose

This repository contains the presentation layer for a travel discovery experience. It is intentionally framework-light: EJS templates are separated from public image assets and can be integrated into an Express application without modifying the templates.

## Directory conventions

| Location | Purpose |
| --- | --- |
| `views/` | EJS templates rendered by the host server. |
| `public/` | Static travel and background images referenced by the templates. |
| `docs/demo.mp4` | Recorded application walkthrough linked from the README. |

## Integration requirements

The host application is responsible for:

- Configuring EJS as the view engine.
- Serving `public/` as the static-assets directory.
- Providing GET and POST routes referenced in the templates.
- Supplying any authentication, search, persistence, or validation behavior.

The supplied templates deliberately contain no application server, package manifest, database configuration, or credentials. This keeps the bundle portable, but it means the repository cannot be run standalone.

## Demo guidance

The repository includes a recorded MP4 walkthrough at `docs/demo.mp4`. If the demo is replaced, keep the filename and link stable, optimize the video before committing it, and ensure it does not expose personal data or credentials.
