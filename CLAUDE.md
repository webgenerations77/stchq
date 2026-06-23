# Spinach the Cow — STC-HQ

## Project overview

Marketing website for **Spinach the Cow**, a wholesome lifestyle brand based in Ocean City, MD. The site covers the brand story, team, blog teasers, contact form, and links out to the Shopify store at `shop.spinachthecow.com`.

## Tech stack

- **Pure HTML/CSS/JS** — no build step, no framework, no bundler
- **Tailwind CSS** via CDN (`cdn.tailwindcss.com`) with inline config
- **Fonts**: DM Sans + DM Serif Display (Google Fonts)
- **EmailJS** for the Join Our Team form (currently hidden, credentials not yet configured)
- **Hosting**: GitHub Pages or static hosting (served as plain files)

## File structure

```
index.html          — Main single-page site (all sections in one file)
privacy.html        — Privacy policy
terms.html          — Terms of service
cookies.html        — Cookie policy
accessibility.html  — Accessibility statement
images/Logo.png     — Brand logo
images/team/        — Team member photos (Andrew, Bubba, Clark, Lewis, Flactoid, Sasha, Tony, Charlie, Kelly, Beth, Mark, John)
Staff/              — Source team photos (originals)
```

## Brand colors (Tailwind custom)

| Token             | Hex       |
|--------------------|-----------|
| `brand-green`      | `#A8D5A0` |
| `brand-green-deep` | `#4A9E3F` |
| `brand-green-dark` | `#357A2B` |
| `brand-sky`        | `#B8DFF0` |
| `brand-beige`      | `#E8C87A` |
| `brand-cream`      | `#FAF8F5` |
| `brand-charcoal`   | `#2D2D2D` |

## Key sections in index.html

Hero, About, Shop (featured product + CTA), Our Story (timeline), Our Values, Our Team (12 members), Testimonials, Blog Teaser, Contact Form, Join Our Team (hidden), Newsletter Banner, Footer.

## Development

No install or build needed. Open `index.html` in a browser or serve with any static server:

```sh
npx serve .
```

## Conventions

- Dark mode supported via Tailwind `dark:` classes, toggled with a button that persists to localStorage
- Scroll-reveal animations use IntersectionObserver with `.reveal` / `.visible` classes
- Team photos fall back to gradient placeholders via `onerror` on `<img>` tags
- External links (shop, socials) use `target="_blank" rel="noopener"`
- The Shopify store is separate — this site links to it but does not embed it

## Things to know

- The "Join Our Team" section (`id="careers"`) exists in the HTML but is hidden with `class="hidden"`. EmailJS credentials are placeholder values.
- The Tailwind config is inline in a `<script>` tag, not a separate file.
- There is no CSS file — all custom styles are in a `<style>` block in `index.html`.
- Legal pages (privacy, terms, cookies, accessibility) share the same Tailwind CDN setup but have their own inline configs.
