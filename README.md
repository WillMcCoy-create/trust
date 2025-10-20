# Trust Page Foundation (v1)

This folder is a drop-in **GitHub Pages** site for your public trust page at `/trust`.

## How to publish (2 steps)

1. **Add this `trust/` folder to your repo** on the `main` branch.
2. In GitHub: **Settings → Pages → Build and deployment → Source = Deploy from a branch**  
   - Branch: `main`  
   - Folder: `/ (root)`  
   - Save.  
   Your site will be at: `https://<your-username>.github.io/trust/`

> You can also serve the whole repo as a site; this folder works as a subpath (`/trust/`).

## Weekly update (manual for now)

Open `trust/index.html` and update **only these 3 values** near the bottom:

```js
window.BADGE_STATE = 'GREEN';      // 'GREEN' | 'YELLOW' | 'RED'
window.VERIFIED_DATE = '2025-10-19';  // YYYY-MM-DD
window.CERT_URL = 'https://example.com/verified-safe-certificate-2025-10-19.pdf';
```

Commit + push. Page updates instantly.

## Later (optional): automate with GitHub Actions

Once ready, your workflow can search/replace those 3 lines during the Sunday publish job.
