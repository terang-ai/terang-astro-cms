# GitHub Pages Deployment

This site is configured for automatic deployment to GitHub Pages with custom domain `blog.terang.ai`.

## Setup Instructions

1. **Add DNS CNAME record:**
   - Type: CNAME
   - Name: blog
   - Value: terang-ai.github.io

2. **Enable GitHub Pages in your repository:**
   - Go to repository Settings → Pages
   - Set Source to "GitHub Actions"
   - The custom domain `blog.terang.ai` will be automatically configured via CNAME file

3. **Push your changes:**
   ```bash
   git add .
   git commit -m "Add GitHub Pages deployment with custom domain"
   git push origin main
   ```

4. **The site will be available at:**
   - `https://blog.terang.ai/`

## Manual Deployment

To deploy manually:
```bash
npm run build
# Upload dist/ folder to any static hosting service
```

## Files Added for Deployment

- `.github/workflows/deploy.yml` - GitHub Actions workflow
- `astro.config.mjs` - Updated with GitHub Pages configuration