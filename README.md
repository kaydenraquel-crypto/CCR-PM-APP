# CCR PM Playbook

**Colorado Commercial Repairs** — Preventive Maintenance Playbook PWA

A self-contained Progressive Web App for managing commercial equipment preventive maintenance contracts, scheduling, pricing, and client documentation.

## Features

- **Asset Management** — Track commercial equipment across client locations
- **PM Scheduling** — Automated maintenance schedules with cadence optimization
- **Pricing Calculator** — ASU-based pricing with travel zones and niche equipment premiums
- **Quote Generator** — Professional service agreement proposals
- **Client Packets** — Full service partnership documentation with signature blocks
- **PM Reports** — Visit documentation with photo support
- **Offline Support** — Works without internet via service worker caching
- **Installable** — Add to home screen on mobile or desktop

## Deployment

### GitHub Pages (Recommended)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, root `/`
4. Your app will be live at `https://[username].github.io/CCR-PM-APP/`

### Local Development

```bash
# Any simple HTTP server works
python3 -m http.server 8000
# Then open http://localhost:8000
```

> **Note:** PWA install and service worker require HTTPS or localhost. Opening `index.html` directly via `file://` will work for the app itself but won't enable install or offline caching.

## File Structure

```
CCR-PM-APP/
├── index.html          # Complete app (single-file architecture)
├── manifest.json       # PWA manifest
├── sw.js               # Service worker for offline caching
├── favicon.png         # Browser tab icon
├── icons/
│   ├── apple-touch-icon.png
│   ├── icon-72x72.png
│   ├── icon-96x96.png
│   ├── icon-128x128.png
│   ├── icon-144x144.png
│   ├── icon-152x152.png
│   ├── icon-192x192.png
│   ├── icon-384x384.png
│   └── icon-512x512.png
└── README.md
```

## Tech Stack

- Vanilla HTML/CSS/JS (no build step)
- IndexedDB via localStorage for data persistence
- Service Worker for offline caching
- Web Manifest for PWA installation

## License

Proprietary — Colorado Commercial Repairs LLC © 2025
