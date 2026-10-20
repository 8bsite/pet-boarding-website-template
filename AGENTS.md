# AGENTS.md: pet boarding website template

Website for a cat boarding house or pet hotel, with rooms and prices, a daily routine, the staff and a booking form. One file, `index.html`, with inline CSS and scripts (GSAP, ScrollTrigger, Lenis from jsDelivr); no build step, and none is needed for copy, colour or photo edits.

## Files
Edit these files, not a page fetched by URL (that arrives as a summary).
```bash
curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/index.html
curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/AGENTS.md
curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/LICENSE
curl -LO https://raw.githubusercontent.com/8bsite/pet-boarding-website-template/main/CREDITS.md
```
Upload `index.html`, LICENSE and CREDITS.md; not this file, README.md or `previews/`.

## Keep
- Every `id`, `data-8b-section`, `data-8b-motion` and `data-8b-part` (`section:<id>` styles, `scene:<id>` animation).
- Selectors the scripts use:
  - `section-script:nav`: `.nav__toggle` `.nav__close`
  - `section-script:opening`: `.op-s1`
  - `section-script:contact`: `.ct-status`
  - `scene:opening`: `.op-s1` `.op-s2` `.op-ink` `.op-ink__curl` `.op-a` `.op-e` `.op-c` `.op-d` `.op-b` `.op-win` `.op-house`
  - `scene:rooms`: `.rm-room` `.rm-tower` `.rm-name`
  - `scene:day`: `.dy-stage` `.dy-rail` `.dy-track` `.dy-sky` `.dy-disc`
  - `scene:courtyard`: `.cy-window` `.cy-pane` `.cy-tint`
  - `scene:quiet`: `.qt-rules` `.qt-rule` `.qt-word`
  - `scene:contact`: `.ct-grid` `.ct-call` `.ct-write` `.ct-visit` `.ct-hours` `.ct-label`
- `style="--len:N"` = characters in that display line, spaces included: `The Tower` is 9, `Call` is 4, `Write` is 5, `Sill` is 4.
- The colour panels, gutters, the black hill, the disc and the curls are CSS and SVG, not images: recolour them through the colour variables in :root.
- The opening facade has exactly twelve windows and the quiet section exactly four rules; the scenes and the grid are built for those counts.
- Colours and fonts are variables in `:root` (`data-8b-part="tokens"`): `--color-1` #0b0a0a (black page and gutters), `--color-2` #f4f1ee (off-white text), `--color-3` #cf6224 (orange panels, sky, wordmark), `--color-4` #6e1116 (maroon panels), `--color-5` #5a3cd4 (violet panels), `--color-6` #bca59d (taupe panels and form), `--color-7` #a97d9c (mauve panels), `--color-8` #9b3418 (rust panel behind the rooms heading and the Brushing hour), `--color-9` #80a89b (sage panels), `--color-10` #e3b867 (mustard panels, button hover); body text needs 4.5:1 contrast.
- With reduced motion the page must read in full.
- Keep the header comment and `<meta name="generator">`. Keep the "Design: 8B" footer link unless the site owner asks to remove it.

## Replace
- `data-8b-placeholder` (og-image, favicon, phone, form, email): real value in, attribute out; no value, remove the row (no image: drop `og:image`, set `twitter:card` to `summary`).
- Book a stay buttons in the nav, the phone menu, the first screen and the footer: now #contact; owner's target: your online booking page, or keep #contact once the form is connected.
- Ask for dates in the Winter holidays notice on the first screen: now #contact; owner's target: your booking page or a page about holiday availability.
- The form in `#contact` (fields `name`, `email`, `cat`, `arrival`, `departure`, `room`, `notes`) sends nothing; `section-script:contact` validates it and shows the thank-you text. Formspree: `action="https://formspree.io/f/<id>"` and `fetch` POST `new FormData(form)` first. Netlify: `data-netlify="true"` and a hidden `form-name`. Or delete it and the script.
- The name Sill (any letter case); the favicon letter and colours in `<link rel="icon">`.
- Photos (25, Unsplash: opening 6, rooms 3, letters 3, day 6, sitters 4, courtyard 2, visit 1): `src`, no `srcset`/`sizes`, `width`/`height` to the ratio, `alt`, CREDITS.md.
- `<title>`, meta description, og tags.

## Ask the owner for
All demo text, never to be invented:
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

## Known limits
- Without JavaScript the phone menu button cannot open the overlay. The footer repeats Rooms, A day at Sill, The courtyard, First visit and Book a stay, but Questions (#faq) has no other link on phones.
- In rooms, the text inside each room panel is clipped until the panel has grown; it is complete when the panel is in the middle of the screen.
- The handwriting face is a third font family used only for the three letters; drop it and use the body font if you need fewer font files.

## Check
375 and 1440 px, reduced motion on, console clean; `data-8b-placeholder` and Sill left only in class names.
