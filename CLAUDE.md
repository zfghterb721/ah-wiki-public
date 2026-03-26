# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is A&H Games' internal wiki built with MkDocs Material and deployed to Cloudflare Pages. The repository contains employee handbooks, procedures, policies, and organized play documentation for a gaming store business.

## Architecture

- **Documentation Source**: `/docs/` - All markdown content organized by category
- **Static Site Generator**: MkDocs with Material theme
- **Deployment**: Cloudflare Workers/Pages via Wrangler
- **Legacy Content**: `/ah-wiki-old/` - Previous wiki content (archived)
- **Generated Site**: `/site/` - Built static site files
- **Assets**: `/docs/files/` - Images, PDFs, and other media files

## Common Commands

### Development
```bash
# Start local development server (if MkDocs is installed)
mkdocs serve

# Start Wrangler dev server
npm run dev
# or
wrangler dev
```

### Deployment
```bash
# Deploy to Cloudflare Pages
npm run deploy
# or 
wrangler deploy
```

### Content Management
- Documentation lives in `/docs/` with standard MkDocs structure
- Images and files are stored in `/docs/files/`
- Site configuration in `mkdocs.yml`
- Cloudflare configuration in `wrangler.jsonc`

## Content Structure

- `docs/index.md` - Main landing page
- `docs/policies/` - Employee handbook and company policies
- `docs/procedures/` - Operational procedures including organized play guides
- `docs/procedures/organized_play/` - Game-specific tournament and event procedures

## Key Files

- `mkdocs.yml` - MkDocs configuration with Material theme
- `wrangler.jsonc` - Cloudflare Workers configuration
- `package.json` - Node.js dependencies (only Wrangler)

## Python Utilities

- `ah-wiki-old/update_images.py` - Script to download and localize remote images in markdown files (legacy)

## Notes

- The project uses MkDocs Material theme with dark (slate) theme and green primary color
- No build step required for basic markdown editing
- Wrangler serves static files from `/site/` directory
- Python virtual environment in `/venv/` for MkDocs dependencies