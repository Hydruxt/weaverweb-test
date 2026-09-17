# Bright Flow Plumbing — Website

Astro + Tailwind static site for **Bright Flow Plumbing** (Austin, TX). Built as a conversion-focused Google Business Profile landing experience: clear CTAs, fast pages, mobile-first.

## Before launch checklist

1. **Phone number** — Site currently uses demo number `(512) 555-0199` (`tel:+15125550199`). Replace with Marcus’s real number everywhere (Header, Footer, Contact, Home CTAs). Search for `555-0199`.
2. **Formspree** — Contact form posts to `https://formspree.io/f/REPLACE_ME`. Create a Formspree form that delivers to `marcus@brightflowplumbing.com`, then replace `REPLACE_ME` in `src/pages/contact.astro`.
3. **Domain / analytics** — Point Cloudflare Pages custom domain and add analytics if desired.
4. **Content review** — Confirm service list, service area towns, and About copy with Marcus.

## Local development

```bash
npm install
npm run dev
```

Open http://localhost:4321

## Build

```bash
npm run build
npm run preview
```

Output is static HTML in `dist/` — ready for Cloudflare Pages, Netlify, or any static host.

## Deploy to Cloudflare Pages (later)

1. Push this repo to GitHub.
2. In Cloudflare Dashboard → Pages → Create project → Connect Git.
3. Build settings:
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
   - **Node version:** 20 (or current LTS)
4. Add custom domain when ready.

Or deploy from CLI:

```bash
npx wrangler pages deploy dist --project-name=bright-flow-plumbing
```

## Site map

| Path | Page |
|------|------|
| `/` | Home |
| `/services` | Services |
| `/about` | About |
| `/contact` | Contact / Request Service |

## Stack

- [Astro](https://astro.build) 4.x (static)
- [@astrojs/tailwind](https://docs.astro.build/en/guides/integrations-guide/tailwind/)
- Tailwind CSS 3.x

## Contact (production)

- Email: marcus@brightflowplumbing.com
- Phone: replace demo `(512) 555-0199` before launch
