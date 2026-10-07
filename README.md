# Divo — website

Marketing, support and legal pages for **Divo: Gujarati Calendar** (iOS). Static HTML served by GitHub Pages at https://alexriakhin.com/Divo/. This repository is the `DivoWebsite` submodule of the app repository (`Shubh`).

```
src/<page>.html        page bodies; first line is a <!-- {json} --> comment (title, description, nav)
tools/build_site.py    wraps each body in the shared header/footer → <page>.html, writes sitemap.xml
assets/css/site.css    styles (cream, saffron, maroon, gold; light + dark), matching the app's Theme.swift
assets/img/            app icon and simulator screenshots
favicons/              generated from the app icon
```

```bash
python3 tools/build_site.py          # rebuild every page after editing src/
python3 -m http.server 8765          # preview at http://localhost:8765
```

The App Store listing links to `support.html` and `privacy.html`. Keep those paths stable. Update the "Coming soon" buttons in `src/index.html` with the App Store link once the app is live.
