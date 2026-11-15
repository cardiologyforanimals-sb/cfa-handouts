# Exotic Pet Heart Monitoring Handout — ChatGPT Visual Handoff

**Date:** 2026-11-14
**Owner:** David Pelio, DVM, DACVIM (Cardiology) · Cardiology for Animals
**Attach with this brief:** `exotic-monitoring/index.html`, the working page. Its folder on the Mac is `Downloads/Cardiology AI/40_Client_Education/Exotic_Monitoring_Handout/`.
**Where it will live:** a free static site (GitHub Pages) at `…/cfa-handouts/exotic-monitoring/`. A small index page at `…/cfa-handouts/` links to it.

---

## 1. The job

This is an owner-facing web handout. Owners of rabbits, ferrets, pet birds and bearded dragons with heart disease use it at home to:
1. count resting breaths, using a built-in 30-second tap counter;
2. know what to watch for in their species;
3. know when to call the vet the same day and when to go to an emergency hospital.

The cardiologist also uses it. Each species section has a **Report paragraph** with a **Copy** button, which he pastes into echo reports.

The page works and is accurate. It looks plain. **Make it beautiful without changing what it says or how it works.**

---

## 2. What is locked (do not change)

- **All wording.** Every sentence, list item, report paragraph, citation and the footer are clinically reviewed. Do not rewrite, shorten, merge or "improve" any text. Do not add claims, numbers, tips or species facts.
- **Every number.** Rabbit 30–60 breaths per minute, the 5% weekly weight change for birds, 30 seconds, and the 54 dragons. Do not add new ones.
- **The four species and their order:** Rabbit, Ferret, Bird, Bearded dragon.
- **The section anchors:** `#rabbit`, `#ferret`, `#bird`, `#dragon`, `#count`, `#how`. Report links point to them.
- **The working parts:**
  - Element IDs `start`, `tap`, `left`, `n`, `rate`, `log`.
  - The four report-paragraph IDs: `t-rabbit`, `t-ferret`, `t-bird`, `t-dragon`.
  - Every `data-copy` button, and the `.copied` message next to it.
  - The `<script>` at the bottom. Restyle freely, but keep these IDs and keep each element type (button stays a button, pre stays a pre).
- **Byline and copyright:** "Cardiology for Animals · David Pelio, DVM, DACVIM (Cardiology)" and "© 2026 David Pelio, DVM, DACVIM (Cardiology) · Cardiology for Animals. All rights reserved."
- **No statement anywhere that the page was made with AI.**

---

## 3. Technical constraints

- **One self-contained `index.html`.** It is plain HTML, CSS and JavaScript, with no framework and no build step.
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

## 4. Visual direction

**Feel:** calm, warm, trustworthy, clinical-but-kind. This is read by a worried owner at night. It should feel like a well-designed specialty hospital handout, not an app store page and not a children's book.

**Palette anchor:** the practice's document colors are navy `#1F4E79` and light blue `#DCE6F1`.
- Build from these.
- You may add one warm accent per species, used sparingly:
  - Rabbit: soft sage.
  - Ferret: warm sand.
  - Bird: teal.
  - Bearded dragon: terracotta.
- **Emergency red is reserved** for the "Go to an emergency hospital now" boxes only. It must stand out from everything else on the page.

**Hierarchy each species section must make obvious, in this order:**
1. Species name, with a small original illustration (see §5).
2. The short intro paragraph.
3. **Every day / Every week** list. Calm styling.
4. **Call your veterinarian the same day if.** Amber/caution styling.
5. **Go to an emergency hospital now if.** Red styling, the most visually urgent element on the page.
6. **Report paragraph.** Clearly secondary, visibly "for the vet." Collapsed by default is acceptable, but the Copy button must still work.

**Breath counter:** make it feel like a tool.
- A large circular tap target.
- A visible countdown ring or bar for the 30 seconds.
- A clear big readout of breaths per minute.
- Keep the existing IDs.

**Species navigation at the top:** four large, friendly buttons, each with its small illustration, plus "Breath counter."

---

## 5. Illustrations

Make one small original illustration per species, about 160 × 160, in one consistent style for all four:
- Simple line-and-flat-color.
- Friendly, not cartoonish.
- Anatomically believable: a lop or upright-eared domestic rabbit, a domestic ferret, a medium parrot such as an African grey or Amazon, and a central bearded dragon.

Rules:
- No text in the art.
- No existing mascot or brand character.
- Not traced from a stock photo.

Optional: a tiny chest-rising icon for the "How to count" section.

---

## 6. Deliverables

1. `index.html`: the restyled page, with all of §2 intact.
2. `img/` with the four species illustrations (and any icon), as WebP or PNG, each under 60 KB.
3. One phone-width screenshot and one desktop screenshot of the finished page.

---

## 7. Rejection criteria

Send it back if any of these are true:
1. **Any wording changed.** This includes text, numbers, citations, report paragraphs or the footer.
2. **The counter or a Copy button no longer works.** Test each before delivering.
3. **An anchor or ID was renamed or removed.**
4. **Emergency boxes are not the most urgent-looking element,** or red is used anywhere else.
5. **It breaks at 360 px wide,** or anything scrolls sideways.
6. **The illustrations contain text,** look like a known character, or are inconsistent in style across species.
7. **Any note says AI made it.**
8. **It needs a build tool, framework or external host** beyond Google Fonts and the page's own `img/` folder.

---

© 2026 David Pelio, DVM, DACVIM (Cardiology) · Cardiology for Animals · All rights reserved
