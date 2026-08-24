# Victory International Trading - Hosting Guide

## For Production Hosting

When deploying to hosting platforms, exclude these files (use .deployignore as reference):

### Files to Keep Locally Only:
- `*.md` files (documentation)
- `test*.html` (test versions)
- `tasks/` folder (development files)
- `img/fmcg/` folder (unused large images)
- `.git*` files

### Production Files Only:
- `index.html` (main page)
- `about.html` (about page)  
- `catalogue.html` (brands page)
- `img/` folder (essential images only)
- `manifest.json` (PWA config)
- `robots.txt` (SEO)
- Logo and asset files

## Hosting Platforms:

### GitHub Pages
1. Go to repository Settings → Pages
2. Deploy from main branch
3. Site: `https://quantumtaskai.github.io/victory-web/`

### Netlify
1. Drag production files only (use .deployignore as guide)
2. Or connect GitHub and configure build settings

### Vercel
1. Import GitHub repository
2. Configure ignore patterns in settings

## Note:
Keep all .md files locally for development reference. They provide valuable documentation but aren't needed for the live website.