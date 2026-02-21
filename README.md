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
cd content
hugo server --disableFastRender
```

The site will be available at `http://localhost:1313`.

### Building

Build the site for production:

```bash
cd content
npm run build
```

This generates the static site in the `content/public/` directory.

## Deployment

The site is deployed to Cloudflare Pages using Wrangler. Configuration is in [`wrangler.jsonc`](wrangler.jsonc).

### Automatic Deployment

Deployments are handled automatically by Cloudflare Pages when changes are pushed to the configured branch. The build step uses the settings from [`wrangler.jsonc`](wrangler.jsonc), running `npm run build` from the `content/` directory to build the site.

## Project Structure

```
felle_me/
├── archetypes/         # Content templates
├── assets/             # CSS, icons, and other assets
├── config/             # Hugo module configuration
├── shortcodes/         # Custom shortcodes
├── hugo.yaml           # Hugo configuration
├── go.mod              # Go module dependencies (for theme)
├── wrangler.jsonc      # Cloudflare Pages deployment configuration
└── renovate.json       # Dependency update configuration
```

## Pre-commit Hooks

This repository uses pre-commit hooks to maintain code quality. See [PRE_COMMIT_SETUP.md](PRE_COMMIT_SETUP.md) for installation and usage instructions.

## External Dependencies

### CDN Usage

When loading external JavaScript and CSS libraries, always use [cdnjs.cloudflare.com](https://cdnjs.cloudflare.com/) as the CDN provider. This ensures consistent, reliable, and fast delivery of assets.

**Example:**

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/library/version/style.min.css" />
```

## License

Content copyright Jordan Felle. Hugo and the Lynx theme are licensed under their respective licenses.
