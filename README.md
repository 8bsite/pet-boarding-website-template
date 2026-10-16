# Free HTML pet boarding website template with GSAP scroll animations — Sill

**Website for a cat boarding house or pet hotel, with rooms and prices, a daily routine, the staff and a booking form: a free HTML template in one file, with GSAP scroll animations, no build step, MIT license. Made by [8B](https://8b.com/), the AI website builder.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE) ![one HTML file: no build](https://img.shields.io/badge/one%20HTML%20file-no%20build-orange) ![GSAP: ScrollTrigger](https://img.shields.io/badge/GSAP-ScrollTrigger-88ce02)

**[Live demo](https://8bsite.github.io/pet-boarding-website-template/)** · **[Use this template](https://github.com/new?template_name=pet-boarding-website-template&template_owner=8bsite)** · **[Download ZIP](https://github.com/8bsite/pet-boarding-website-template/archive/refs/heads/main.zip)**

<a href="https://8bsite.github.io/pet-boarding-website-template/"><img src="previews/desktop.png" alt="Sill, a free HTML template: first screen on a desktop" width="76.1%"></a> <a href="https://8bsite.github.io/pet-boarding-website-template/"><img src="previews/phone.png" alt="Sill, a free HTML template: first screen on a phone" width="21.9%"></a>

<p align="center"><a href="https://8bsite.github.io/pet-boarding-website-template/"><img src="previews/scroll.gif" alt="Sill, a free HTML template: scrolling through the first sections on a desktop" width="40%"></a><br><sub>Scroll animation</sub></p>

A one-page site for a small boarding house for cats with twelve rooms around a courtyard. Flat blocks of saturated colour separated by thick black gutters; a black hill rises and swallows the first screen while the house's windows light up, the day runs past on a pinned track under a changing sky, and photos peek up over their panels' edges.

Good for: cattery or cat hotel; pet boarding or pet sitting service; dog daycare or kennel (with new photos and rules); small guesthouse or B&B with a handful of rooms; any small service with rooms or packages, a daily schedule and a team. Free for personal and commercial use (MIT), made by [8B](https://8b.com/).

## Quick start

Pick one:

- **With an AI coding agent** (Claude Code, Codex, Cursor, Windsurf…). Download the files into your project (in Windows PowerShell type `curl.exe`):
  ```bash
  curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/index.html
  curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/AGENTS.md
  curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/LICENSE
  curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/CREDITS.md
  ```
  Then give your agent this prompt:
  ```text
  Read AGENTS.md, then edit index.html. Use this template as the base for a site for <your pet boarding business: which animals you take, the rooms or packages and their prices, the daily routine, the team, where you are, how to book>. Keep the layout, the motion and the single-file format; replace the brand name, copy, photos, prices, hours, staff, address, links and contacts, and recolour it through the CSS variables if needed.
  ```
  Give the agent the downloaded file, not a link: an agent reads a link as a summary and would rebuild a different page.
- **No code.** Download the ZIP, unzip it, replace the contacts and texts in `index.html`, put `index.html` into an empty folder and drag that folder onto [Netlify Drop](https://app.netlify.com/drop). The page is online in a minute.
- **On GitHub.** Click **[Use this template](https://github.com/new?template_name=pet-boarding-website-template&template_owner=8bsite)** to get your own copy, then **Settings → Pages → Deploy from a branch → main**. Your site appears at `https://<you>.github.io/<repo>/`.

## What's on the page

- **Navigation** — black top bar: wordmark, five section links, Book a stay button; hides on scroll down; phone menu overlay of colour panels
- **Rooms with a view, for cats.** — two screens: a grid of colour panels with headline, photo, intro, price and buttons, then a facade of twelve coloured windows (demo: twelve rooms, five with cats)
- **Three shapes of room** — room types as panels of different shapes, each with photo, text and price per night, plus an "every room has" list (demo: Ledge, Tower, Burrow)
- **A letter every evening** — three short notes in a handwriting font with photos (demo: the evening letters sitters send to owners); works as testimonials
- **A day at Sill** — pinned horizontal track of six timed panels under a sky band (demo: the cats' daily schedule from 07:00 to 21:00)
- **Four people, always in the house** — team of four: portraits behind coloured ledges at stepped heights, name and role on each ledge
- **Every window faces the courtyard** — one photo cut into six window panes by black mullions, with heading, text, a three-item list and a second photo with caption (demo: the courtyard view)
- **Your first visit** — four numbered steps as a rising staircase of panels, a photo on the top step (demo: what happens on a first visit)
- **A quiet house, by rule** — four rules or promises as panels with one big word each (demo: No dogs, One cat, Own air, Vet close)
- **Questions owners ask** — questions and answers (native &lt;details&gt;) beside a heading panel with a phone link
- **Book a room** — booking form framed by four contact panels: Call, Visit, Hours, Write (phone, address, opening hours, email are placeholders)
- **Footer** — black footer: links, address, phone, email, a one-line note, copyright with the Design: 8B credit, and a large wordmark

## Before you publish

- Replace everything marked `data-8b-placeholder` (social preview image, favicon, phone, form, email) and the invented demo facts — prices, dates, address. [AGENTS.md](AGENTS.md) lists them.
- The contact form does not send anything yet: connect it to a form service (Formspree, Netlify Forms) or remove it; [AGENTS.md](AGENTS.md) shows both.

## Customize

- **Colours and fonts**: CSS variables in the `:root` block at the top of `<head>`.
- **Text**: edit it in place. A big display line with `style="--len:N"` fills its width: set N to its new number of characters.
- **Photos**: replace `src`, delete `srcset` and `sizes` (they list Unsplash sizes) and update the `alt` texts.
- **Animations**: each section's animation is one `<script data-8b-part="scene:<id>">` block at the end of the file. For native scroll, delete the Lenis block in `page-init`.

## For developers

- **Stack.** HTML and CSS (custom properties, cascade layers) with GSAP 3.13.0, ScrollTrigger, SplitText, Lenis 1.3.27 from jsDelivr. No build step, no framework, no npm. 94 KB.
- **Layout of the file.** `<head>`: CSS variables, shared classes, then one style block per section. Then the markup, one element per section with a one-line comment above it. End of `<body>`: small behaviour scripts, the libraries, smooth scroll (`page-init`), the effects, one animation script per section.
- **Browsers.** Chrome and Edge 108+, Safari 15.4+, Firefox 101+ (it uses cascade layers, small/dynamic viewport units).
- **Accessibility.** Motion runs only when the visitor's system allows it; with "reduce motion" the page is complete and still. FAQ answers use native `<details>` and open without JavaScript. Every photo has alt text.
- **External requests.** fonts.gstatic.com, images.unsplash.com, cdn.jsdelivr.net. No analytics, no cookies. To self-host everything (offline use, or Google Fonts and GDPR in the EU), download those files and change the URLs.
- **Licences of the parts.** GSAP is free, commercial use included, under its own standard licence (not MIT); Lenis is MIT; fonts are SIL OFL; photos are under the Unsplash License. See [CREDITS.md](CREDITS.md).

## FAQ

**Can I use it for a client or a commercial site?** Yes. The code is MIT: use it, change it, sell the site you build with it.

**Do I have to keep the "Design: 8B" link?** No. It is welcome, not required.

**Can I use it in React, Next.js, Astro or Vue?** Yes. Move each section's markup and style block into a component and run its animation script in `useGSAP()` (React) or `onMounted` (Vue); start Lenis once. Or keep it as a separate static landing page next to your app (`example.com` for the landing, `app.example.com` for the app).

**Why doesn't the contact form send?** It is a demo. Connect it to Formspree, Netlify Forms or your backend; AGENTS.md has the steps.

**Where are the photos from?** Unsplash; they load from Unsplash's servers. Replace them with your own when you can.

## More free templates

[More 8B templates on GitHub](https://github.com/8bsite) · [8b.com](https://8b.com/)

## License

The template code is MIT licensed — see [LICENSE](LICENSE). Photos, fonts and libraries keep their own licences — see [CREDITS.md](CREDITS.md).
