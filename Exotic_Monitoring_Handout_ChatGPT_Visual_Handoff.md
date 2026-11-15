# Exotic Pet Heart Monitoring Handouts (4 species) — ChatGPT Visual Handoff

**Date:** 2026-11-14
**Owner:** David Pelio, DVM, DACVIM (Cardiology) · Cardiology for Animals
**Attach with this brief:** the five working pages, from `Downloads/Cardiology AI/40_Client_Education/Exotic_Monitoring_Handout/` on the Mac:
- `rabbit/index.html`
- `ferret/index.html`
- `bird/index.html`
- `dragon/index.html`
- `index.html` (the library page that links to all four)

**Where they will live:** a free static site (GitHub Pages), with one link per species: `…/cfa-handouts/rabbit/`, `/ferret/`, `/bird/`, `/dragon/`.

---

## 1. The job

These are **four separate owner-facing web handouts, one per species** (rabbit, ferret, bird, bearded dragon), plus a small library page. Each species page stands alone, because owners get only their own species' link. Owners use their page at home to:
1. count resting breaths, using a built-in 30-second tap counter;
2. know what to watch for in their species;
3. know when to call the vet the same day and when to go to an emergency hospital.

The cardiologist also uses them. Each species page has a **Report paragraph** with a **Copy** button, which he pastes into echo reports.

The pages work and are accurate. They look plain. **Make all four beautiful, as one matching family, without changing what they say or how they work.**

---

## 2. What is locked (do not change)

- **All wording.** Every sentence, list item, report paragraph, citation and the footer are clinically reviewed. Do not rewrite, shorten, merge or "improve" any text. Do not add claims, numbers, tips or species facts.
- **Every number.** Rabbit 30–60 breaths per minute, the 5% weekly weight change for birds, 30 seconds, and the 54 dragons. Do not add new ones.
- **One page per species, at its own folder path.** Do not merge the pages back into one.
- **The section anchors on each page:** `#how`, `#count`, plus that page's species anchor (`#rabbit`, `#ferret`, `#bird` or `#dragon`).
- **The working parts:**
  - Element IDs `start`, `tap`, `left`, `n`, `rate`, `log`.
  - The report-paragraph ID on each page (`t-rabbit`, `t-ferret`, `t-bird` or `t-dragon`).
  - Every `data-copy` button, and the `.copied` message next to it.
  - The `<script>` at the bottom. Restyle freely, but keep these IDs and keep each element type (button stays a button, pre stays a pre).
- **Byline and copyright:** "Cardiology for Animals · David Pelio, DVM, DACVIM (Cardiology)" and "© 2026 David Pelio, DVM, DACVIM (Cardiology) · Cardiology for Animals. All rights reserved."
- **No statement anywhere that the page was made with AI.**

---

## 3. Technical constraints

- **Each page is one self-contained `index.html`.** Plain HTML, CSS and JavaScript, with no framework and no build step. Shared styling may be copied into each page or placed in one shared `assets/site.css` referenced by relative path (`../assets/site.css`).
- **Fonts:** Google Fonts is fine. Any font that lets a stressed owner read a list fast at arm's length on a phone is fine.
- **Images:**
  - Inline SVG, or a PNG/WebP placed in the same folder and referenced by relative path, such as `img/rabbit.webp`.
  - Total page weight should stay under about 1.5 MB.
  - No hotlinked images from other sites.
- **Phone first.** Most owners open it from an emailed link on a phone:
  - It must work at 360 px wide.
  - Tap targets at least 44 px.
  - The **Tap each breath** button must stay large and easy to hit with a thumb while watching the animal.
- **Light and dark mode** must both stay readable.
- **Printing:** it must print cleanly (black-and-white friendly, no clipped sections).
- **Accessibility:**
  - Contrast at WCAG AA or better.
  - Visible keyboard focus.
  - Respect `prefers-reduced-motion`.

---

## 4. Visual direction — synthwave with the Heartline comic style

**The look is Cardiology for Animals synthwave:** a deep violet-to-midnight background, neon magenta and cyan accents, a soft sunset gradient horizon, and a faint perspective grid. It should feel like the practice's 80s neon teaching material, made friendly for owners.

**The characters come from Heartline.** Heartline is the practice's owner summary, and its patient portraits are made in ChatGPT in the chat **"Create Dog Image"** with the prompt **"Create golden hour character."** Every species character on these pages must be drawn in **that same comic portrait style**, so the handouts and Heartline look like one family.

**Readability rules over the neon:**
- Body text sits on solid dark panels, never directly on the gradient or grid.
- Text is off-white on violet at WCAG AA contrast or better.
- Neon is for edges, headings, buttons and glow, not for paragraphs.
- A worried owner at night must be able to read every list in one glance on a phone.

**Color roles:**
- Neon cyan: calm daily-check lists and the breath counter.
- Neon amber or gold: the "Call your veterinarian the same day" boxes.
- **Emergency red is reserved** for the "Go to an emergency hospital now" boxes only. Use a hot red-pink with a strong outline and glow, unmistakably the loudest element on the page. Red appears nowhere else.
- Magenta: headings and accents.

**Comic styling of the UI:**
- Panels with bold ink outlines and slight drop shadows, like comic panels.
- Section headings in a comic-display face, used sparingly.
- Speech-bubble styling is welcome for the species character's one-line greeting at the top. The bubble may repeat only the page title, with no new claims.

**Hierarchy each species page must make obvious, in this order:**
1. Species character (hero, comic Heartline style) and the page title.
2. The short intro paragraph.
3. How to count, and the breath counter.
4. **Every day / Every week** list. Cyan, calm.
5. **Call your veterinarian the same day if.** Amber.
6. **Go to an emergency hospital now if.** Red, loudest element on the page.
7. **Report paragraph.** Clearly secondary, visibly "for the vet." Collapsed by default is acceptable, but the Copy button must still work.

**Breath counter:** make it feel like an arcade tool.
- A large circular neon tap button.
- A glowing countdown ring for the 30 seconds.
- A big readout of breaths per minute.
- Keep the existing IDs.

**Library page:** four big comic-panel cards, one per species character, each with Open and Copy link. Same synthwave world.

---

## 5. Illustrations

Make one hero character per species in the **Heartline "golden hour character" comic portrait style**, about 320 × 320 on a transparent background:
- a domestic rabbit (lop or upright-eared);
- a domestic ferret;
- a medium parrot (African grey or Amazon);
- a central bearded dragon.

Also make a smaller version of each, about 120 × 120, for the library page cards.

Rules:
- Same style, line weight and lighting across all four, matching existing Heartline portraits.
- Anatomically believable for the species.
- Friendly and calm, never sick-looking or distressed.
- No text in the art.
- No existing mascot or brand character.
- Not traced from a stock photo.

Optional: a small neon chest-rising icon for the "How to count" section.

---

## 6. Deliverables

1. `rabbit/index.html`, `ferret/index.html`, `bird/index.html`, `dragon/index.html` and the library `index.html`, restyled, with all of §2 intact.
2. `assets/` with the shared stylesheet (if used) and the eight character images (four hero, four small), as WebP or PNG, each under 80 KB.
3. One phone-width screenshot of each species page and of the library page.

---

## 7. Rejection criteria

Send it back if any of these are true:
1. **Any wording changed.** This includes text, numbers, citations, report paragraphs or the footer.
2. **The counter or a Copy button no longer works.** Test each before delivering.
3. **An anchor or ID was renamed or removed.**
4. **Emergency boxes are not the most urgent-looking element,** or red is used anywhere else.
5. **Text sits directly on the gradient or grid,** or any paragraph fails AA contrast.
6. **The characters do not match the Heartline comic portrait style,** or the four do not match each other.
7. **The pages were merged into one,** or a species page links to the other species' content.
8. **Any page breaks at 360 px wide,** or anything scrolls sideways.
9. **The illustrations contain text** or look like a known character.
10. **Any note says AI made it.**
11. **It needs a build tool, framework or external host** beyond Google Fonts and the pages' own `assets/` folder.

---

© 2026 David Pelio, DVM, DACVIM (Cardiology) · Cardiology for Animals · All rights reserved
