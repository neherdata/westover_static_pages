# Westover Static Pages

Monorepo for personal Westover-branded static sites deployed on Cloudflare Pages.

## Sites

- **westover.dev** - Personal landing page
- **westover.expert** - Consulting services catalog
- **westover.services** - Internal tools portal
- **westover.lol** - Personal domain
- **resume.westover.dev** - Professional resume

## Deployment

Each site is deployed as a separate Cloudflare Pages project from this monorepo.

### Cloudflare Pages Configuration

Each project should be configured with:
- **Build command**: `echo "Static site - no build needed"`
- **Build output directory**: `<site-directory>` (e.g., `westover.dev`)
- **Root directory**: `<site-directory>`
- **Build watch paths**: `<site-directory>/**`

## Structure

```
westover_static_pages/
├── westover.dev/
├── westover.expert/
├── westover.services/
├── westover.lol/
└── resume.westover.dev/
```

## Development

Each site is a standalone static HTML site. To preview locally:

```bash
cd <site-directory>
python -m http.server 8000
```

## DNS

All domains managed via Cloudflare DNS and deployed via Cloudflare Pages.
