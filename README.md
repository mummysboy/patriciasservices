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

## Quote form
Every "Get a Free Quote" button opens a modal form (name, phone, email, service, home size, details). On submit:
- **On a phone** — opens the visitor's Messages app pre-addressed to **(808) 476-2343** with all the lead details filled in. The visitor taps Send and the lead (plus their own number) arrives as a text.
- **On desktop** (no SMS app) — falls back to composing an email to the business.

Works on any static host with no backend. The business number/email are set as `BIZ_PHONE` / `BIZ_EMAIL` constants in the submit handler in `index.html`.

**To text leads fully automatically** (from any device, no visitor action), add an SMS service such as [Twilio](https://twilio.com) behind a small serverless function (e.g. on Netlify/Vercel) and POST the form to it. This requires moving off GitHub Pages and a small monthly cost.

> The desktop email fallback sends to `biohealth2@gmail.com` (the `BIZ_EMAIL` constant in the submit handler).

## Notes
- Background images are stock placeholders. Replacing them with real, high-resolution before/after photos of actual work is the highest-impact upgrade.
- To swap an image, drop a file into `img/` using the same name (`hero.jpg`, `deep.jpg`, `rental.jpg`, `commercial.jpg`).
