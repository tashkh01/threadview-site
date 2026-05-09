# threadview-site

Static marketing site for [ThreadView](https://threadview.app).

Two pages:
- `index.html` — landing page.
- `privacy.html` — privacy policy (linked from the Chrome Web Store listing).

## Local preview

Open either HTML file directly in a browser, or:

```sh
npx serve .
```

## Deploy to Vercel

1. Create a new Vercel project from this repo.
2. Framework preset: **Other** (this is plain HTML/CSS, no build step).
3. Add `threadview.app` as a custom domain.
4. In Namecheap → Domain List → threadview.app → Manage → Advanced DNS, set the DNS records Vercel shows.
5. `cleanUrls: true` in `vercel.json` makes `threadview.app/privacy` resolve to `privacy.html`.

## Editing copy

Both pages are single self-contained HTML files with inline CSS. To change copy, edit the
HTML directly. To change the visual language, edit the `:root` custom properties at the
top of each `<style>` block — `--paper`, `--brand`, `--font-display`, `--col` (max
reading width), and the `--t-*` font-size clamps drive everything else.

## Files

- `index.html` — landing page (~9KB)
- `privacy.html` — privacy policy (~7KB)
- `icon-128.png` — favicon and brand mark (also used at threadview-extension/icons/)
- `vercel.json` — cleanUrls, security headers, immutable PNG cache
