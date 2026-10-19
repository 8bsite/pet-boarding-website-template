# Free HTML pet boarding website template with GSAP scroll animations — Sill

**Website for a cat boarding house or pet hotel, with rooms and prices, a daily routine, the staff and a booking form: a free HTML template in one file, with GSAP scroll animations, no build step, MIT license. Made by [8B](https://8b.com/), the AI website builder.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE) ![one HTML file: no build](https://img.shields.io/badge/one%20HTML%20file-no%20build-orange) ![GSAP: ScrollTrigger](https://img.shields.io/badge/GSAP-ScrollTrigger-88ce02)

**[Live demo](https://8bsite.github.io/pet-boarding-website-template/)** · **[Use this template](https://github.com/new?template_name=pet-boarding-website-template&template_owner=8bsite)** · **[Download ZIP](https://github.com/8bsite/pet-boarding-website-template/archive/refs/heads/main.zip)** · **[Template page on 8b.com](https://8b.com/templates/sill/)**

<a href="https://8bsite.github.io/pet-boarding-website-template/"><img src="previews/desktop.png" alt="Sill, a free HTML template: first screen on a desktop" width="76.1%"></a> <a href="https://8bsite.github.io/pet-boarding-website-template/"><img src="previews/phone.png" alt="Sill, a free HTML template: first screen on a phone" width="21.9%"></a>

<p align="center"><a href="https://8bsite.github.io/pet-boarding-website-template/"><img src="previews/scroll.gif" alt="Sill, a free HTML template: scrolling through the first sections on a desktop" width="40%"></a><br><sub>Scroll animation</sub></p>

A one-page site for a small boarding house for cats with twelve rooms around a courtyard. Flat blocks of saturated colour separated by thick black gutters; a black hill rises and swallows the first screen while the house's windows light up, the day runs past on a pinned track under a changing sky, and photos peek up over their panels' edges.

Good for: cattery or cat hotel; pet boarding or pet sitting service; dog daycare or kennel (with new photos and rules); small guesthouse or B&B with a handful of rooms; any small service with rooms or packages, a daily schedule and a team.

## Use it with an AI coding agent

Download the files into your project (in Windows PowerShell type `curl.exe`):

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

Give the agent the downloaded file, not a link: from a link it would rebuild a different page. No agent? Click **[Use this template](https://github.com/new?template_name=pet-boarding-website-template&template_owner=8bsite)**, edit `index.html` and turn on **Settings → Pages**.

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

## Design

Palette: ![#0b0a0a](https://img.shields.io/badge/-%230b0a0a-0b0a0a?style=flat-square) ![#f4f1ee](https://img.shields.io/badge/-%23f4f1ee-f4f1ee?style=flat-square) ![#cf6224](https://img.shields.io/badge/-%23cf6224-cf6224?style=flat-square) ![#6e1116](https://img.shields.io/badge/-%236e1116-6e1116?style=flat-square) ![#5a3cd4](https://img.shields.io/badge/-%235a3cd4-5a3cd4?style=flat-square) ![#bca59d](https://img.shields.io/badge/-%23bca59d-bca59d?style=flat-square) ![#a97d9c](https://img.shields.io/badge/-%23a97d9c-a97d9c?style=flat-square) ![#9b3418](https://img.shields.io/badge/-%239b3418-9b3418?style=flat-square) ![#80a89b](https://img.shields.io/badge/-%2380a89b-80a89b?style=flat-square) ![#e3b867](https://img.shields.io/badge/-%23e3b867-e3b867?style=flat-square)  
Fonts: Gabarito, Playwrite US Modern, Rethink Sans (Google Fonts). Change both through the CSS variables in the `:root` block at the top of `<head>`. A big display line with `style="--len:N"` fills its width: set N to its new number of characters.

- The colour panels, gutters, the black hill, the disc and the curls are CSS and SVG, not images: recolour them through the colour variables in :root.
- The opening facade has exactly twelve windows and the quiet section exactly four rules; the scenes and the grid are built for those counts.

## Before you publish

- Replace everything marked `data-8b-placeholder` (social preview image, favicon, phone, form, email) and the invented demo facts: prices, dates, address. [AGENTS.md](AGENTS.md) lists them.
- The form sends nothing yet: connect it to Formspree or Netlify Forms, or remove it.

## Tech

GSAP 3.13.0, ScrollTrigger, SplitText, Lenis 1.3.27 from jsDelivr, 94 KB, no build step. Chrome and Edge 108+, Safari 15.4+, Firefox 101+ (it uses cascade layers, small/dynamic viewport units). With "reduce motion" on, the page is complete and still.

## License

MIT, see [LICENSE](LICENSE); the "Design: 8B" footer link is welcome, not required. Photos, fonts and libraries keep their own licences: [CREDITS.md](CREDITS.md). More free templates: [8b.com/templates](https://8b.com/templates/) · [github.com/8bsite](https://github.com/8bsite).
