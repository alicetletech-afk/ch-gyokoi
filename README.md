# Gyokoi / 陈翼飞 — Personal Profile V7

Static portfolio, finalized from the supplied V7 ZIP. No build step or package installation is required.

## Local preview

From this directory, run:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000 in a browser. Stop the server with Ctrl+C.

## GitHub Pages

Upload the contents of this directory to `alicetletech-afk/ch-gyokoi`, preserving the `assets/` folder. In the repository, select Settings → Pages → Deploy from a branch → main → / (root), then Save. The expected project URL is https://alicetletech-afk.github.io/ch-gyokoi/ after Pages finishes deployment.

All local assets use relative paths, including the downloadable resume. `.nojekyll` allows static serving. The only external display dependency is Google Fonts; system sans-serif fonts provide a fallback.

## Assets

The original V7 profile image, Instagram profile screenshot, TikTok and Lemon8 thumbnails, and resume PDF are preserved. Four supplied photo collages appear in upload order in a square 2×2 gallery, beside the 9:16 profile screenshot. Cropping uses CSS `object-fit: cover`; the original JPEGs remain unchanged.

See QA.md for verification results and external-service limitations.
