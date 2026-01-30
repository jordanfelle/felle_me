# felle.me

Personal website built with Hugo and the Lynx theme.

## Features

- **Static Site Generation**: Built with Hugo for fast, secure static site hosting
- **Lynx Theme**: Uses the Lynx theme from Hugo modules
- **Cloudflare Integration**: Deployed to Cloudflare Pages via Wrangler

## Setup

### Prerequisites

- Go (for Hugo modules)
- Hugo (extended version)
- Node.js (for Wrangler)

### Local Development

Run the Hugo development server:

```bash
hugo server --disableFastRender
```

The site will be available at `http://localhost:1313`.

### Building

Build the site for production:

```bash
hugo --minify
```

This generates the static site in the `public/` directory.

## Deployment

The site is deployed to Cloudflare Pages using Wrangler. Configuration is in [`wrangler.jsonc`](wrangler.jsonc).

### Automatic Deployment

Deployments are handled automatically by Cloudflare Pages when changes are pushed to the configured branch. The build step uses the settings from [`wrangler.jsonc`](wrangler.jsonc), running `hugo --minify` to build the site.

## Project Structure

```
felle_me/
├── archetypes/         # Content templates
├── assets/             # CSS, icons, and other assets
├── config/             # Hugo module configuration
├── shortcodes/         # Custom shortcodes
├── hugo.toml           # Hugo configuration
├── go.mod              # Go module dependencies (for theme)
├── wrangler.jsonc      # Cloudflare Pages deployment configuration
└── renovate.json       # Dependency update configuration
```

## Pre-commit Hooks

This repository uses pre-commit hooks to maintain code quality. See [PRE_COMMIT_SETUP.md](PRE_COMMIT_SETUP.md) for installation and usage instructions.

## License

Content copyright Jordan Felle. Hugo and the Lynx theme are licensed under their respective licenses.
