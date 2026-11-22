# NiPay website

The public one-page website for NIPAY Ltd. Its job right now is credibility: grant reviewers, partner banks, regulators and future hires should find a clear, honest page when they search for NiPay. It is not yet a merchant sign-up page.

Built with [Astro](https://astro.build) as a static site (plain HTML and CSS, almost no JavaScript), so it loads fast on mobile data. TypeScript is the only language, in line with the NiPay Engineering Handbook.

## Run it

Needs Node.js 22 or later.

```bash
npm install
npm run dev       # local preview at http://localhost:4321
npm run build     # production files in dist/
npm run preview   # serve the built site
```

## Where things live

| Path | What it is |
| --- | --- |
| `src/site.ts` | Facts used across the page: email, LinkedIn, legal name, location. Change them here. |
| `src/styles/global.css` | Brand Identity v1 tokens (colours, spacing) and shared styles. |
| `src/components/` | One file per section, in page order: Header, Hero, Problem, HowItWorks, Promise, ForBanks, Status, Contact, Footer. |
| `src/components/Mark.astro` | The brush-stroke mark. Never redraw or alter it. |
| `public/favicon.svg` | App icon: Lime tile, Forest mark. |

## Content rules (read before editing copy)

- Say "registered company, in development, pursuing the BNR sandbox and partner-bank route". Never say or imply that NiPay is licensed.
- No partner logos, merchant numbers or testimonials until they are real and approved.
- No interest rates on the site until BNR's position is confirmed.
- No forms that collect personal data until a privacy notice is published (Law 058/2021).
- Every statistic names its source.
- Brand: Forest Ink #0B2A1C, Kigali Lime #B6F03C, Signal Orange #FF6B1A only as a rare signal, Inter only.

## Before launch

- [ ] Real domain in `astro.config.mjs` (`site`) and email in `src/site.ts`
- [ ] Founder photo (`public/`) and bio in `src/components/Status.astro`
- [ ] Social share image (1200 × 630)
- [ ] Kinyarwanda version, checked by a native speaker

## Deploy

Hosted on Vercel. Every push to `main` deploys automatically; pull requests get a preview link.
