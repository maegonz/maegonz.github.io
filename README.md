# Persephone Manuel — Field Log (Vue + Vite)

Structural layout borrowed from the "ticker / vignette grid / two-column header"
idea, rebuilt from scratch with your own content and the manga field-log palette
(near-black ink, warm paper, blood red, ember yellow) and fonts
(Anton / Fraunces / Manrope / IBM Plex Mono / Caveat).

## Run it locally

```
npm install
npm run dev
```

## Add your images

Drop your existing `figures/` and `doc/` folders (portrait, project GIFs,
report PDFs) into `public/figures` and `public/doc` — the components already
reference those paths, e.g. `/figures/IMG_2328.JPG`.

## Build for deployment

```
npm run build
```

Output lands in `dist/`.
