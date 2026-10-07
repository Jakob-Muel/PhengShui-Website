# Pheng Shui website

Static support site for the iOS app **Pheng Shui** (`com.jakobmueller.photosorter`), hosted on GitHub Pages.

Available in English (`/en/`) and German (`/de/`). Every page has a DE/EN picker in the top right that links to the same page in the other language.

| Page | English | Deutsch |
| --- | --- | --- |
| Landing | https://jakob-muel.github.io/PhengShui-Website/en/ | https://jakob-muel.github.io/PhengShui-Website/de/ |
| Privacy policy | https://jakob-muel.github.io/PhengShui-Website/en/privacy/ | https://jakob-muel.github.io/PhengShui-Website/de/privacy/ |
| Support | https://jakob-muel.github.io/PhengShui-Website/en/support/ | https://jakob-muel.github.io/PhengShui-Website/de/support/ |
| Legal notice / Impressum | https://jakob-muel.github.io/PhengShui-Website/en/legal-notice/ | https://jakob-muel.github.io/PhengShui-Website/de/impressum/ |

The old URLs `/`, `/privacy/` and `/support/` still work: they redirect to the visitor's browser language (German -> `/de/`, everything else -> `/en/`).

## Structure

```
en/index.html, en/privacy/, en/support/, en/legal-notice/   English pages
de/index.html, de/privacy/, de/support/, de/impressum/      German pages
index.html, privacy/, support/            language redirects (keep: old links point here)
assets/style.css      all styles (values from the app's tokens.css)
assets/icon.png       app icon, 512px
assets/apple-touch-icon.png, favicon.ico, favicon-32.png
.nojekyll             serve files as-is
```

Plain HTML and one CSS file. No build step, no external fonts or CDNs, no cookies, no trackers. The only JavaScript is the small inline language redirect in the three redirect pages; without JavaScript they fall back to English. All links are relative, so the site works under the `/PhengShui-Website/` project path and on a custom domain.

## Editing

Edit the HTML directly and push to `main`. GitHub Pages deploys from the `main` branch root.

Change both languages together. When the privacy policy changes, update the date at the top of `en/privacy/index.html` ("Effective") and `de/privacy/index.html` ("Gültig ab").

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```
