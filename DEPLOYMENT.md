# Deployment Guide — GitHub Pages

This guide walks you through publishing the Network Security Dashboard to **GitHub Pages** so it's accessible at a public URL.

---

## Prerequisites

- A [GitHub account](https://github.com)
- [Git](https://git-scm.com/) installed on your machine
- The `network_security_dashboard.html` file (rename to `index.html` before deploying)

---

## Step 1 — Prepare your file

GitHub Pages serves `index.html` as the entry point. Rename your file:

```bash
mv network_security_dashboard.html index.html
```

---

## Step 2 — Create a new GitHub repository

1. Go to [https://github.com/new](https://github.com/new)
2. Set the repository name to `network-security-dashboard` (or any name you prefer)
3. Set visibility to **Public** *(GitHub Pages is free for public repos)*
4. Do **not** initialize with a README — you'll push your own files
5. Click **Create repository**

---

## Step 3 — Push your files

In your project folder, run:

```bash
git init
git add .
git commit -m "Initial commit: Network Security Dashboard"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/network-security-dashboard.git
git push -u origin main
```

> Replace `YOUR-USERNAME` with your actual GitHub username.

---

## Step 4 — Enable GitHub Pages

1. Open your repository on GitHub
2. Click **Settings** (top tab)
3. In the left sidebar, click **Pages**
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**

GitHub will display a banner:
> *"Your site is live at https://YOUR-USERNAME.github.io/network-security-dashboard/"*

This may take **1–3 minutes** to propagate.

---

## Step 5 — Verify your deployment

Visit:

```
https://YOUR-USERNAME.github.io/network-security-dashboard/
```

You should see the fully rendered dashboard with the Chart.js timeline loading correctly.

---

## Updating the dashboard

Whenever you make changes, push them to the `main` branch and GitHub Pages will automatically redeploy:

```bash
git add .
git commit -m "Update: describe your change here"
git push
```

Redeployment typically takes under 60 seconds.

---

## Troubleshooting

| Issue | Solution |
|---|---|
| Site shows 404 | Ensure your file is named `index.html` and is in the root of the repo |
| Chart not rendering | Check browser console; ensure Chart.js CDN is reachable |
| Changes not reflecting | Hard-refresh the page (`Ctrl+Shift+R` / `Cmd+Shift+R`) or wait a minute |
| Dark mode not working | Test in a browser where system dark mode is enabled |

---

## Custom domain (optional)

To use your own domain (e.g. `dashboard.yoursite.com`):

1. In **Settings → Pages**, enter your domain under **Custom domain**
2. Add a `CNAME` file to your repo root containing just the domain name
3. Configure a `CNAME` DNS record at your registrar pointing to `YOUR-USERNAME.github.io`
