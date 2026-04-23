# Happy Lobster Bar — Landing Page

Static HTML landing page for **The Happy Lobster Bar** — the on-site, live, made-to-order lobster bar catering service. This page is hosted on Vercel and embedded as an iframe at `happylobsterchicago.com/the-bar`.

## Structure

```
happy-lobster-bar-page/
├── public/
│   ├── index.html              ← the whole page
│   ├── colors_and_type.css     ← design tokens (colors, fonts, CSS vars)
│   ├── bar.css                 ← section styles (hero, marquee, etc.)
│   ├── assets/                 ← photos, logos, badges
│   └── fonts/                  ← Hammersmith One, Cormorant, Wonderful Sunset
├── package.json
├── vercel.json                 ← iframe-permissive headers
└── README.md                   ← you are here
```

## Editing content

All page copy lives in `public/index.html`. Search for the section you want to change — sections are commented top-to-bottom:

- `<!-- HERO -->`
- `<!-- MARQUEE -->`
- `<!-- WHAT THE BAR IS -->`
- `<!-- STATS -->`
- `<!-- HOW IT WORKS -->`
- `<!-- TESTIMONIALS -->`
- `<!-- INQUIRY -->`

Edit the text directly, commit, push, and Vercel auto-deploys in ~30 seconds.

## Form submissions

The inquiry form uses `mailto:` to open the visitor's email client with all the form fields pre-filled in the body. The recipient is set at the bottom of `index.html` in the `submitInquiry()` function — currently `hello@happylobsterchicago.com`.

When ready to upgrade to a real backend (Formspree, Vercel API route, etc.), replace the `mailto:` line in `submitInquiry()` with a `fetch()` call to your chosen endpoint.

## Local preview

```bash
npm run dev
# Opens on http://localhost:3000
```

## Deployment

Pushes to the main branch auto-deploy to Vercel. The live URL is the Vercel-assigned `*.vercel.app` domain.
