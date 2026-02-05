# CLAUDE.md

## Repository Overview

This is **FraserMacdonald.github.io**, a GitHub Pages static site repository. It serves as Fraser Macdonald's personal website and hosts a Tesla third-party public key for authentication integration.

## Directory Structure

```
FraserMacdonald.github.io/
├── .well-known/
│   └── appspecific/
│       └── com.tesla.3p.public-key.pem   # Tesla ECDSA public key
├── .nojekyll                              # Disables Jekyll processing
├── index.md                               # Site homepage
└── CLAUDE.md                              # This file
```

## Key Files

| File | Purpose |
|------|---------|
| `index.md` | Homepage content rendered by GitHub Pages |
| `.nojekyll` | Empty file that tells GitHub Pages to skip Jekyll and serve raw content |
| `.well-known/appspecific/com.tesla.3p.public-key.pem` | ECDSA P-256 public key for Tesla third-party integration (RFC 8615 well-known URI) |

## Technologies

- **GitHub Pages** for static site hosting
- **Markdown** for content authoring
- **No build step** - content is served directly (Jekyll is disabled via `.nojekyll`)

## Development Workflow

1. Content is authored in Markdown (`.md` files)
2. GitHub Pages serves the site directly at `https://frasermacdonald.github.io/`
3. No build tools, bundlers, or CI pipelines are configured
4. No package manager or dependency files exist

## Conventions

- **No Jekyll**: The `.nojekyll` file is intentional. Do not remove it. Content is served as-is without Jekyll transformation.
- **Well-known URIs**: The `.well-known/` directory follows RFC 8615. Files here must be accessible at their exact URL paths for external service verification (e.g., Tesla authentication).
- **Commit style**: Short imperative messages describing the change (e.g., "Create index.md").

## Important Notes for AI Assistants

- Do not modify or regenerate the Tesla public key (`com.tesla.3p.public-key.pem`). It is a cryptographic credential used for external service integration.
- The `.nojekyll` file must remain present to prevent Jekyll processing.
- The `.well-known/` directory structure and file paths are significant for external service discovery and must not be renamed or reorganized.
- This is a minimal, early-stage repository. Keep changes simple and avoid introducing unnecessary tooling or complexity.
