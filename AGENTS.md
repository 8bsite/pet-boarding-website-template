# Sill — notes for AI coding agents

One HTML file: markup, inline CSS and inline scripts; GSAP with ScrollTrigger and SplitText, Lenis smooth scroll, all from jsDelivr. No build step, no framework.

## Files
Work from the files: a page read through a link comes back as a summary, and a page rebuilt from it would differ.
```bash
curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/index.html
curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/AGENTS.md
curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/LICENSE
curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/CREDITS.md
```
In Windows PowerShell type `curl.exe`. Publish `index.html` with LICENSE and CREDITS.md; this file, README.md and `previews/` are not part of the site.

## Do not break
- Keep it one file unless the user asks otherwise; no framework or bundler for copy, colour or photo changes.
- Keep the ids and the `data-8b-section` / `data-8b-motion` attributes. Each section has its styles in `<style data-8b-part="section:<id>">` and its animation, if any, in `<script data-8b-part="scene:<id>">`.
- The scripts find these classes and attributes; when you change a section's markup, keep them or update the script:
  - `section-script:nav`: `.nav__toggle` `.nav__close`
  - `section-script:opening`: `.op-s1`
  - `section-script:contact`: `.ct-status`
  - `scene:opening`: `.op-s1` `.op-s2` `.op-ink` `.op-ink__curl` `.op-a` `.op-e` `.op-c` `.op-d` `.op-b` `.op-win` `.op-house`
  - `scene:rooms`: `.rm-room` `.rm-tower` `.rm-name`
  - `scene:day`: `.dy-stage` `.dy-rail` `.dy-track` `.dy-sky` `.dy-disc`
  - `scene:courtyard`: `.cy-window` `.cy-pane` `.cy-tint`
  - `scene:quiet`: `.qt-rules` `.qt-rule` `.qt-word`
  - `scene:contact`: `.ct-grid` `.ct-call` `.ct-write` `.ct-visit` `.ct-hours` `.ct-label`
- Colours, fonts, radii and shadows are CSS variables in the `:root` block (`data-8b-part="tokens"`); change them there and keep body text at 4.5:1 contrast or more.
- Animations run only when the visitor allows motion (`prefers-reduced-motion: no-preference`); the page must stay readable without them.
- A display line with `style="--len:N"` is sized to fill its width: N is its number of characters, spaces included (`The Tower` → 9, `Call` → 4).
- Keep the header comment and `<meta name="generator">`. Keep the "Design: 8B" footer link unless the site owner asks to remove it.

## Replace before publishing
- Everything marked `data-8b-placeholder` (og-image, favicon, phone, form, email); remove the attribute once the real value is in. With no real value: no preview image — delete the `og:image` tag and set `twitter:card` to `summary`; no phone, email or address — remove that link or row.
- Book a stay buttons in the nav, the phone menu, the first screen and the footer: link to #contact now; point them to your online booking page, or keep #contact once the form is connected.
- Ask for dates in the Winter holidays notice on the first screen: link to #contact now; point them to your booking page or a page about holiday availability.
- **The form sends nothing.** `section-script:contact` checks the fields and shows a thank-you message without sending. Pick one:
  - Formspree: set `action="https://formspree.io/f/<id>"` on the form; in the script, before the thank-you message, `await fetch(form.action, { method: 'POST', body: new FormData(form), headers: { Accept: 'application/json' } })` and show it only if the response is ok.
  - Netlify Forms (site on Netlify): add `name="contact" data-netlify="true"` and `<input type="hidden" name="form-name" value="contact">`; send with `fetch('/', { method: 'POST', headers: { 'Content-Type': 'application/x-www-form-urlencoded' }, body: new URLSearchParams(new FormData(form)) })`.
  - No form service: remove the `<form>` together with the script that handles it (it would fail without the form) and keep the email link.
- Invented demo facts (ask the user for the real ones; do not make up prices, dates or addresses):
  - Prices: "From €31 a night" (opening), The Ledge €34, The Tower €39, The Burrow €31 a night, "fits two siblings" (rooms), "the second cat pays half" (faq).
  - Size and team: twelve single rooms, four sitters, "sitters in the house day and night", one cat per room (opening, sitters, quiet, footer note, page title and meta description).
  - Location: Utrecht (title, meta description, opening) and the address "Example Street 1, 3500 AA Utrecht. Ring the green bell." (contact, footer); the phone +31 30 000 0000 and hello@sill.example are placeholders.
  - Room details: a ledge forty centimetres deep, a radiator shelf, "the lamps go on at seven" (opening); a two-metre ledge, a hammock and a bird feeder, five shelves and a rope, a covered bed (rooms); "a heated ledge from October", own window and fresh-air vent (rooms, quiet).
  - Guests named on the page: Olive ("Room 4 · Olive, staying nine nights"), the window names Pip, Moss, Bruno, Mochi, Saar (opening); the letters to "Ana" about Olive, Mochi and Bruno, with days and times (Tuesday 18:40, Wednesday 18:35, Thursday 18:50) and room numbers (letters).
  - Holiday offer: "Christmas and New Year rooms are open for booking" (opening, Winter holidays notice).
  - Service promises: an evening letter with a photo at half past six, the first one on the first day (letters, visit); a free half-hour visit, "the first night costs nothing extra", "most cats settle on the second day" (visit); medication including insulin "at no extra cost" (faq); "a sitter always picks up" (faq) and "a sitter answers within one working day" (the form's thank-you line).
  - Daily schedule: 07:00 breakfast, 09:30 window watch, 12:00 play hour, 14:00 long nap, 17:30 brushing, 21:00 lights low, a night sitter on the sofa downstairs (day).
  - Staff: Noor, Jasper, Ilse and Daan (the owner) with duties such as "gives a pill in four seconds" (sitters, letter signatures); the portraits are stock photos of real people, and their alt texts name them.
  - The building and courtyard: no street side, two brick wings, a lawn, "a linden tree, sixty years old", a feeder refilled at seven, ivy that turns red in October, sparrows at six (opening, courtyard).
  - House rules: no dogs at all, one cat per room unless siblings, a separate vent per room, "a cat clinic two streets away, on call day and night" (quiet).
  - Booking terms: vaccinations against cat flu and feline panleukopenia at least two weeks before arrival and the passport on the first day; minimum stay two nights; day guests on weekdays from eight to six (faq).
  - Hours: phone daily 8–20 (contact); drop-off and pick-up 8:00–11:00 and 17:00–19:00, Sundays evening only (faq, contact).
  - "© 2026 Sill" and "Twelve rooms, four sitters, one courtyard" (footer).
- `<title>`, the meta description and the og tags; photos (Unsplash, see CREDITS.md) when the user has their own.

## Notes
- The colour panels, gutters, the black hill, the disc and the curls are CSS and SVG, not images: recolour them through the colour variables in :root.
- The opening facade has exactly twelve windows and the quiet section exactly four rules; the scenes and the grid are built for those counts.
- Without JavaScript the phone menu button cannot open the overlay; the links stay reachable in the footer.
- In rooms, the text inside each room panel is clipped until the panel has grown; it is complete when the panel is in the middle of the screen.
- The handwriting face is a third font family used only for the three letters; drop it and use the body font if you need fewer font files.

## Common edits
- Rebrand: search the old name (`Sill`) in any letter case and replace every match; change the favicon letter and colours in `<link rel="icon">`.
- Photos: replace `src` and delete `srcset` and `sizes` (they list Unsplash sizes), keep `width`/`height` to the new photo's ratio, update `alt` and CREDITS.md.
- Remove a section: delete its markup, its `section:<id>` and `scene-style:<id>` styles, its `scene:<id>` and `section-script:<id>` scripts, and links to `#<id>`.
- Native scroll instead of smooth scroll: delete the Lenis block in `page-init` and the Lenis `<script>` tag.

## Check and publish
- Open the page at 375 and 1440 px, with reduced motion on, with the console open.
- Search `data-8b-placeholder` and the old name: nothing should be left but class names.
