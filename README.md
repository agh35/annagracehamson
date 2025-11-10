# Personal Website (GitHub Pages)

This repository contains a minimal GitHub Pages-ready personal website. It uses the `docs/` folder as the published site root so you can keep everything simple (plain HTML/CSS, no build step).

Replace the placeholder assets with your real files:
- `docs/assets/resume/resume.pdf` — your resume PDF (already added)
- `docs/assets/images/headshot.jpg` — your headshot image (already added)
- `docs/assets/images/` — add project images here (e.g. `project1.jpg`)

How to preview locally

1. From the repository root, serve the `docs/` folder with Python:

```bash
cd docs
python3 -m http.server 8000
# then open http://localhost:8000 in your browser
```

Publishing to GitHub Pages

1. Push this repository to GitHub.
2. In the repository Settings → Pages, set the source to the branch you use (e.g. `main`) and the folder to `/docs`.
3. Save — GitHub will publish the site at `https://<your-username>.github.io/<your-repo>/`.

Notes

- If you prefer using the README as a homepage, GitHub will render the README on the repo page, but Pages only publishes static sites from `docs/` (or the root for some configurations).
- The site is intentionally minimal and easy to edit. See `docs/index.html` and `docs/style.css` to tweak layout and styles.

If you'd like, I can add a GitHub Actions workflow to auto-deploy or finish recommended VS Code extensions and tips.
