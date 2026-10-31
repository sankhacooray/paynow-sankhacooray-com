# paynow.sankhacooray.com

Single-file sandbox (`index.html`) on GitHub Pages: pushing `main` deploys. See README.md.

## Lighthouse
<!-- lighthouse-optimized: 2026-10-31 -->
Baseline (mobile): performance 79, accessibility 96, best-practices 100, SEO 100.
Fixed: contrast — new `--accent-fill` (#d42030, white text 5.2:1) for the CTA and fail banner, `--accent-text` (#ff5c6a dark / #d42030 light) for red text; `--accent` (#ed2939) stays for dots and borders.
Left: no web fonts or images to optimise; inline JS not minified (no build step); gtag/script.google.com findings come from the shared analytics script; GitHub Pages can't set cache headers.
