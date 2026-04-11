# Holidae 🌍

A responsive holiday booking website prototype built for the Web Development Assessment 2.

---

## What it is

Holidae is a front-end website for a fictional holiday booking company. The brief required a fully responsive site that works properly on both mobile and desktop, reflecting real usage data showing 78% of users browse on mobile but 52% complete bookings on desktop.

---

## Pages and features

- **Homepage** — hero section with search bar, key stats, and destination cards
- **Destinations** — six destination cards with lazy-loaded photos, prices and ratings
- **Featured banner** — full-width cinematic image section (Bali)
- **Photo gallery** — CSS Grid mosaic layout
- **Booking calculator** — live price breakdown that updates in real time
- **How it works** — four-step process section
- **How it was built** — tech breakdown cards
- **Footer** — links and branding

---

## Files

| File | What it does |
|------|-------------|
| `holidae_HTML.html` | All page structure and content |
| `holidae_CSS.css` | All styling, layout, and responsive breakpoints |
| `holidae_JS.js` | Hamburger menu, booking calculator, scroll animations, star field |

---

## How to run it

No installation needed. Just download all three files into the same folder and open `holidae_HTML.html` in a browser.

All three files must be in the same folder or the CSS and JavaScript won't load.

---

## Technical highlights

**Viewport meta tag**
Ensures mobile browsers use the actual device width rather than rendering at a fake desktop width and scaling down.

**CSS media queries**
Two breakpoints — 900px for tablets and 768px for phones. At 768px the navigation collapses to a hamburger menu, the destination grid drops to a single column, and the booking calculator stacks vertically.

**CSS custom properties**
All colours and key spacing values are defined as variables at the top of the CSS file so they can be updated in one place.

**CSS Grid and Flexbox**
The destination cards use `grid-template-columns: repeat(3, 1fr)` on desktop, collapsing to `1fr` on mobile. Flexbox handles the navigation bar and search form layouts.

**JavaScript booking calculator**
Guest and night counts are stored in a state object. Every time a stepper button is pressed, the state updates and a render function rewrites the full price breakdown from scratch — keeping everything in sync.

**Hamburger menu**
A JavaScript event listener toggles a CSS class on the mobile menu element to show and hide it.

**Intersection Observer scroll animations**
Content sections fade in as they enter the viewport. Uses the Intersection Observer API rather than a scroll event listener to avoid performance issues on mobile.

**Lazy loading**
All images use `loading="lazy"` so they only load when the user scrolls close to them, improving initial page load speed.

**Touch-friendly sizing**
All interactive buttons are a minimum of 44px tall on mobile, following Apple HIG and Google Material Design accessibility guidelines.

---

## Fonts

- **Playfair Display** — headings (via Google Fonts)
- **Outfit** — body text (via Google Fonts)

Requires an internet connection to load fonts. Site still works without them but falls back to system fonts.

---

## Images

All photography is sourced from [Unsplash](https://unsplash.com) via CDN links. Requires an internet connection to display images.

---

## Known limitations

- The search form, date inputs and destination links are not functional — this is a prototype
- The Book Now button triggers a browser alert rather than a real booking flow
- No backend — no database, no user accounts, no payment processing

---

## Built with

HTML5 · CSS3 · Vanilla JavaScript · Google Fonts · Unsplash

---

*Web Development A2 — Tara Yah — 2026*
