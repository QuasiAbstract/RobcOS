# Deploying to GitHub Pages

## 1. Copy missing local assets

This prep package does not include the font files. Before uploading, copy your current working project's `fonts/` folder into this folder.

Expected font paths referenced by `style.css`:

```text
fonts/fixedsys-excelsior-301-webfont/FSEX300.woff
fonts/fixedsys-excelsior-301/FSEX300.ttf
```

## 2. Create a repository

Create a new repository on GitHub, for example:

```text
robco-terminal-poc
```

For the simplest GitHub Pages setup, use a public repository.

## 3. Upload the project files

The repository root should contain:

```text
index.html
style.css
holotapes/
fonts/
.nojekyll
robots.txt
README.md
DEPLOY_GITHUB_PAGES.md
```

Do not put these inside an extra wrapper folder unless you intend to publish from `/docs` or configure a different Pages source.

## 4. Enable GitHub Pages

In the repository:

1. Open **Settings**.
2. Open **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch: `main`.
5. Select folder: `/ (root)`.
6. Save.

GitHub will show the published Pages URL after the deployment finishes.

## 5. Share cautiously

For a select-few proof of concept, send the Pages URL directly. Assume it is public; anyone with the link can view it, and static-site assets can be inspected by visitors.

## 6. Updating content later

For local editing:

1. Set `ENABLE_ADMIN_MODE` to `true` in `index.html`.
2. Open the page locally.
3. Use `Ctrl+Shift+A` to enter admin mode.
4. Edit entries.
5. Export the backup JSON.
6. Import/apply that content to your working project as needed.
7. Set `ENABLE_ADMIN_MODE` back to `false` before publishing again.
