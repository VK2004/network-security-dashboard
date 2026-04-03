# Contributing

Thank you for your interest in improving the Network Security Dashboard! Contributions are welcome, whether it's a bug fix, a new visualization, or a documentation improvement.

---

## How to contribute

### 1. Fork the repository

Click **Fork** at the top-right of the repository page to create your own copy.

### 2. Clone your fork

```bash
git clone https://github.com/YOUR-USERNAME/network-security-dashboard.git
cd network-security-dashboard
```

### 3. Create a feature branch

```bash
git checkout -b feature/your-feature-name
```

Use a descriptive branch name, e.g. `feature/geo-ip-map` or `fix/dark-mode-tooltip`.

### 4. Make your changes

Since this is a static HTML/CSS/JS project, no build step is needed. Open `index.html` in your browser to test changes directly.

### 5. Commit and push

```bash
git add .
git commit -m "feat: add geo-IP map panel"
git push origin feature/your-feature-name
```

### 6. Open a Pull Request

Go to the original repository on GitHub and click **New pull request**. Describe what you changed and why.

---

## Guidelines

- **Keep it static** — no build tools, frameworks, or npm dependencies. The dashboard should remain a single self-contained HTML file or a minimal file set.
- **Maintain dark mode** — any new UI elements must respect the `prefers-color-scheme` media query and CSS custom properties already in use.
- **Responsive design** — test on at least one mobile breakpoint before submitting.
- **Data accuracy** — if changing mock data, keep values realistic and consistent with the dashboard narrative.
- **Commit messages** — use the format `type: short description` where type is one of `feat`, `fix`, `docs`, `style`, or `refactor`.

---

## Reporting issues

Open an [issue](../../issues) and include:
- A clear description of the problem
- Steps to reproduce
- Browser and OS version
- A screenshot if applicable
