# Xiyao Chen — academic portfolio

Static source for **https://ci-yo.github.io/**.

This refresh intentionally uses plain HTML/CSS instead of a generated `_next/` export so the portfolio remains easy to maintain.

## Structure

- `index.html` — landing page, selected research, research fingerprint, research trail preview
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
