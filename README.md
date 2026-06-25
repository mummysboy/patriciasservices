# Patricia's Services — Website

A single-page, Tesla-inspired marketing site for Patricia's Services, a Honolulu / O‘ahu cleaning company.

## Features
- Full-viewport sections with full-bleed photography and smooth in-page navigation
- Minimalist black/white layout warmed with a Hawaiian ocean-teal & sunset-coral palette
- Services: deep cleaning, vacation-rental turnovers, commercial cleaning
- Reputation, transparent pricing, and quote/contact CTAs
- SEO-ready: keyword title/description, single H1, and a fully populated `LocalBusiness` JSON-LD (NAP, hours, price range, 4.8★ rating)
- Fully responsive with a mobile menu

## Structure
```
index.html      # the entire site (HTML + CSS + JS inline)
img/            # section background photos (Unsplash, free for commercial use)
```

## Run locally
Just open `index.html` in a browser, or serve the folder:
```
python3 -m http.server
```

## Deploy
Works as a static site on GitHub Pages, Netlify, Vercel, or any static host. For GitHub Pages: Settings → Pages → deploy from `main` / root.

## Notes
- Background images are stock placeholders. Replacing them with real, high-resolution before/after photos of actual work is the highest-impact upgrade.
- To swap an image, drop a file into `img/` using the same name (`hero.jpg`, `deep.jpg`, `rental.jpg`, `commercial.jpg`).
