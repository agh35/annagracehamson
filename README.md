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

Automatic deploy with GitHub Actions

I've added a workflow `.github/workflows/deploy.yml` that will deploy the contents of the `docs/` folder to the `gh-pages` branch whenever you push to `main`.

After you push these changes to GitHub, the workflow will create/update the `gh-pages` branch. In your repository Settings → Pages, set the site source to the `gh-pages` branch (if not already set). For a user site named `username.github.io`, you can also publish from the repository root — if you prefer that, let me know and I can switch the workflow to push to the root of `main` instead.

To push your local changes (from the repo root):

```bash
git add .
git commit -m "Add site files and GitHub Actions deploy workflow"
git push origin main
```

The workflow will run automatically and deploy the `docs/` contents to `gh-pages`.
