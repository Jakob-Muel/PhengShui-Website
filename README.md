# Pheng Shui website

Static support site for the iOS app **Pheng Shui** (`com.jakobmueller.photosorter`), hosted on GitHub Pages.

| Page | URL |
| --- | --- |
| Landing | https://jakob-muel.github.io/PhengShui-Website/ |
| Privacy policy | https://jakob-muel.github.io/PhengShui-Website/privacy/ |
| Support | https://jakob-muel.github.io/PhengShui-Website/support/ |

## Structure

```
index.html            landing page
privacy/index.html    privacy policy  -> /privacy/
support/index.html    support + FAQ   -> /support/
assets/style.css      all styles (values from the app's tokens.css)
assets/icon.png       app icon, 512px
assets/apple-touch-icon.png, favicon.ico, favicon-32.png
.nojekyll             serve files as-is
```

Plain HTML and one CSS file. No JavaScript, no build step, no external fonts or CDNs, no cookies, no trackers. All links are relative, so the site works under the `/PhengShui-Website/` project path and on a custom domain.

## Editing

Edit the HTML directly and push to `main`. GitHub Pages deploys from the `main` branch root.

When the privacy policy changes, update the "Effective" date at the top of `privacy/index.html`.

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```
