# Latham Moffatt, P.C. — Website

A modern rebuild of [lathammoffatt.com](https://www.lathammoffatt.com/) for Latham Moffatt, P.C.,
Attorneys at Law, Athens, Alabama.

## Stack

Dependency-free static site: semantic HTML, one hand-written CSS file, a small
progressive-enhancement JS file. No build step, no framework. Deploy the repo
root to any static host (GitHub Pages, Netlify, Cloudflare Pages, cPanel).

- **Type**: Cormorant Garamond (display) + Public Sans (text), self-hosted WOFF2
  in `assets/fonts/` (both SIL Open Font License, via Fontsource packages).
- **Icons**: [Phosphor Icons](https://phosphoricons.com/) (MIT), inlined as SVG.
- **Design**: law-library palette — deep green, warm paper, single brass accent.
  Light and dark themes via `prefers-color-scheme`. WCAG AA contrast verified
  for all text pairs. `prefers-reduced-motion` honored.

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home: hero, credibility strip, practice areas, firm intro, why choose us, attorneys, first-meeting guide, call band |
| `about.html` | Firm story, timeline (1964 to today), values, service area |
| `attorneys.html` | Full bios: Byrd R. Latham, James D. Moffatt |
| `practice-areas.html` | Family law, criminal defense, estate planning, probate, personal injury, mediation (anchor links) |
| `faq.html` | Plain-language FAQ with FAQPage structured data |
| `contact.html` | Call-first contact page: phone, address, hours, directions |
| `404.html` | Not-found page (picked up automatically by GitHub Pages / Netlify) |

`robots.txt` and `sitemap.xml` are included; JSON-LD `LegalService` data is on
the home page for local SEO.

## TODO before launch

1. **Photography.** The site ships with styled placeholders; drop real photos into
   `assets/img/` and swap them in at the commented image slots:
   - `index.html` hero panel: the two attorneys together, the office exterior, or the
     Limestone County Courthouse (portrait, ~1200×1400)
   - `index.html` + `attorneys.html`: attorney headshots `byrd-latham.jpg`, `jim-moffatt.jpg` (portrait, ~900×1080)
   - Optional practice-area photos for `practice-areas.html` (criminal, family, probate).
     There are no image slots there yet; add them to `.area-head` if the firm supplies art.
2. **Open Graph image.** `assets/img/og.png` (1200×630) is referenced from every
   page head. A generated placeholder is included; replace with a branded one if desired.
3. **Contact form (optional).** The contact page is call-first by design. To add a
   form, create one on [Formspree](https://formspree.io) (or use Netlify Forms) with
   the firm's email and add the form to `contact.html`.
4. **Verify facts with the firm** before launch: hours, the AV Preeminent rating
   year, and each attorney's practice description. All copy was drawn from the
   firm's existing site and public directory listings.
   Two claims on the home page deserve a second look against the Alabama Rules of
   Professional Conduct on advertising (Rule 7.1–7.3) before launch: the
   "no recovery, no fee" personal injury policy (some states require noting that a
   client may still owe case expenses) and "same-day consultations, based on our
   schedule."
5. **URLs.** Canonicals/sitemap point at `*.html` paths. If your host serves
   extensionless URLs, update `sitemap.xml`, the `rel="canonical"` tags, and nav links.

## Content sources

Firm facts (address, phone, hours, bios, ratings) were taken from the firm's
current site and public listings (Martindale, BBB, chamber of commerce) in July 2026.
The required Alabama attorney-advertising disclaimer is in the footer of every page.
