# Deploy to GitHub Pages

## Quick Deploy (one-time setup)

```bash
# 1. Create a new repository on GitHub named "health-dashboard"

# 2. Initialize git and push
cd /root/clawd/nightly-builds/2026-01-28-health-dashboard
git init
git add docs/
git commit -m "Deploy to GitHub Pages"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/health-dashboard.git
git push -u origin main
```

## 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Settings → Pages
3. Source: "Deploy from a branch"
4. Branch: "main" (or "gh-pages"), folder: "/ (root)"
5. Click Save

## 4. Access Your Dashboard

Your dashboard will be live at:
```
https://YOUR-USERNAME.github.io/health-dashboard/
```

## Updating

```bash
git add docs/
git commit -m "Update dashboard"
git push
```

GitHub Pages will auto-update in ~1 minute.

---

## Data Persistence

This version uses **localStorage** to save your data in the browser. 
Data stays on your device and isn't synced to a server.

For persistent storage across devices, consider:
- Using the Node.js version with a shared data file
- Manual JSON export/import using the textarea
