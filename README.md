# RobCo Terminal Proof of Concept

A static browser-based Fallout-inspired terminal proof of concept.

## What this build is for

This folder is prepared for a small public demo via static hosting such as GitHub Pages.

The public terminal interface is preserved, while admin access is disabled by default so viewers cannot accidentally open the editor with the keyboard shortcut.

## Important notes

- This is a static HTML/CSS/JavaScript project. There is no backend.
- Viewer changes, if admin mode is re-enabled locally, are stored only in that browser's localStorage.
- GitHub Pages is public hosting. Treat the link as public even if you only send it to a few people.
- `robots.txt` and the `noindex` meta tag are included to discourage indexing, but they are not access control.
- The bundled font files are not included in this prep package. Copy your existing `fonts/` folder into this folder before publishing if you want the offline terminal font to load.

## Enable admin mode locally

In `index.html`, change:

```js
const ENABLE_ADMIN_MODE = false;
```

to:

```js
const ENABLE_ADMIN_MODE = true;
```

Then open the page locally and press `Ctrl+Shift+A` to access the admin console.

Before sharing publicly, set it back to `false`.

## Folder layout

```text
index.html
style.css
holotapes/
fonts/              <-- copy this from your working project before deploying
.nojekyll
robots.txt
```

## Quick local test

You can open `index.html` directly in a browser for a basic test.

For a more accurate local static-server test:

```bash
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Included demo content

The base `index.html` is seeded with the proof-of-concept entries from `robco_terminal_backup.json`, including the public notices, security logs, and corrupt medical record directories. Fresh visitors do not need to import a backup file to see these entries.
