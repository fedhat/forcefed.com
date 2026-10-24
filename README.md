# forcefed.com

Static website for Force F.E.D. LLC, hosted on GitHub Pages.

## Files

- `index.html` – the landing page (badge logo is inline SVG)
- `styles.css` – styles
- `logo.webp` – the logo
- `favicon.png` – tab icon (cropped from the logo)
- `404.html` – not-found page
- `CNAME` – custom domain for GitHub Pages
- `.nojekyll` – tells GitHub Pages to serve files as-is

## Deploying

1. Push to the `main` branch on GitHub.
2. In the repo: Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. DNS for `forcefed.com`:
   - Apex `A` records → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Apex `AAAA` records (optional) → `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
   - `www` `CNAME` → `fedhat.github.io`
   Leave existing `MX` records alone so email keeps working.
4. Back in Settings → Pages, confirm the custom domain `forcefed.com` and enable "Enforce HTTPS" once the certificate is issued.

## Local preview

```bash
python3 -m http.server 8080
```
