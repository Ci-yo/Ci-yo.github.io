# Xiyao Chen — academic portfolio

Static source for the [research portfolio](https://ci-yo.github.io/).

The site uses plain HTML/CSS. It has no Node.js build step or npm dependencies.

## Step-by-step guide

### 1. Download the source

Install [Git](https://git-scm.com/downloads) and
[Python 3](https://www.python.org/downloads/), then run in a terminal:

```bash
git clone https://github.com/Ci-yo/Ci-yo.github.io.git
cd Ci-yo.github.io
```

Alternatively, use **Code → Download ZIP**, extract it and open a terminal in
the folder containing `index.html`.

### 2. Preview the site locally

```bash
python -m http.server 8000 --bind 127.0.0.1
```

Open [the local preview](http://127.0.0.1:8000/) in your browser. Keep the
terminal running; press **Ctrl+C** when finished. On Windows, use `py` if
`python` is not recognised.

Use the local HTTP server so links such as `/projects/` resolve against the
site root. Double-clicking an HTML file is not a reliable preview of those
links. Any fully qualified `https://ci-yo.github.io/...` link still opens the
published website; use the local URL when checking an edited page.

### 3. Edit the relevant file

| Change | File |
|---|---|
| Landing-page introduction or selected work | [`index.html`](index.html) |
| Project descriptions and repository links | [`projects/index.html`](projects/index.html) |
| Research timeline | [`trail/index.html`](trail/index.html) |
| Shared spacing, colours or responsive styles | [`assets/style.css`](assets/style.css) |
| Public CV | `assets/XiyaoChen_CV.pdf`; preserve the filename or update all links. |

Save the file and refresh the browser. There is no generated build folder.
Keep the research/coursework distinction described below.

### 4. Check the preview before publishing

Open `/`, `/projects/`, `/trail/` and `/cv/`. Check navigation, project links,
the CV destination, images and a narrow browser viewport. The `/cv/` page is a
compatibility redirect, so verify its destination after editing any CV link.

In the terminal:

```bash
git diff --check
git diff
```

Confirm the diff contains only the intended public edits before committing.

### 5. Publish through GitHub Pages

For maintainers with repository write access, stage the specific files you
changed, commit, and push to `main`. Check the repository's **Settings → Pages**
for the configured publishing source and its deployment status. The presence
of this README does not configure Pages automatically.

Once deployment succeeds, open the [published website](https://ci-yo.github.io/)
and repeat the navigation check. A push and a successful deployment are
separate steps.

### Troubleshooting

| Symptom | Action |
|---|---|
| Port 8000 is already in use | Start the server on 8001 and open `http://127.0.0.1:8001/`. |
| A local page returns 404 | Start the server from this repository root, not from `projects/`. |
| CSS changes seem absent | Hard-refresh the page and confirm you are viewing the local URL. |
| Local preview works but the public site is unchanged | Inspect the Pages publishing source and latest deployment status. |

## Structure

- `index.html` — concise landing page with a three-domain research lens, selected projects, current focus, and research trail
- `projects/index.html` — research experiences first; coursework and tools in a separate section
- `trail/index.html` — research trajectory without duplicating the CV
- `cv/index.html` — compatibility redirect from the former HTML CV URL to the PDF
- `assets/XiyaoChen_CV.pdf` — current public two-page CV
- `assets/style.css` — shared design system
- `assets/favicon.svg` — site icon

## Update rule

Keep the hierarchy explicit:

1. research evidence;
2. research story / trajectory;
3. selected coursework and software builds.

The 2026 cross-technology m6A research project and `BIO215_P3_m6APrediction` are deliberately presented as separate projects.
