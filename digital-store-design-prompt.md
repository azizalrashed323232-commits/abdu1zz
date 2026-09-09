# Design Prompt — Digital Art & Printables Store
### Artisaire's aesthetic, translated for downloadable goods

For a store selling high-quality **wall art prints (digital), worksheets, and other digital
products**. Adapted from the Artisaire brief — same restraint, same warmth, same editorial
calm — but rebuilt around the fact that nothing here ships in a box.

---

## 1. The Translation — what changes and why

Artisaire's design works because the product is a small, precious, physical object and the
layout makes it monumental. You don't have an object. Every borrowed element needs a job that
still makes sense.

| Artisaire's move | Why it worked | Your equivalent |
|---|---|---|
| Macro photography of wax texture | Made the product touchable | **Mockups** — framed art on real walls, worksheets printed on a desk |
| "Poured by hand in our studio" | Provenance as trust anchor | **Human authorship** — designed by a person, test-printed, not auto-generated |
| Unboxing / shipping ritual | Delayed gratification, anticipation | **Instant download** — reframe as the benefit, not the absence of one |
| Solid brass, mail-safe wax | Material quality specs | **File quality specs** — 300 DPI, formats, dimensions, color profile |
| Free shipping threshold | Cart-value lever | **Bundles** — the margin play for digital goods |
| Warm cream background everywhere | Paper illusion | **Warm chrome, neutral gallery ground for artwork** (see §3) |
| Color variant swatches | Physical choice | **Aspect-ratio / size / format selectors** |

### The core design problem
**Digital goods feel weightless, and weightless reads as cheap.** Your entire design job is
giving files the perceived weight of objects. Three levers do it:

1. **Scale** — show artwork enormous. A 1600px-wide preview says "this is worth $18" in a way a
   400px thumbnail never will.
2. **Context** — mockups that place the file in a real room or on a real desk. The buyer must
   see the outcome, not the asset.
3. **Specificity** — exact dimensions, exact file list, exact print sizes. Vagueness reads as
   low effort; precision reads as craft. This replaces Artisaire's material story entirely.

---

## 2. Tone & Voice

Keep Artisaire's register — warm, assured, quietly expert, unhurried — and re-point it.

**What replaces the artisan story:** you are the designer. Say so. In a market flooded with
auto-generated filler, *human authorship and real testing* is the premium signal, exactly as
"made in our studio" was for wax. Lead with the work behind the file.

**In-voice lines**
> Drawn by hand, test-printed on real paper, and refined until the color was right.

> Yours the moment you check out. Print it at home tonight, or send it to a lab for something
> you'll keep for years.

> Five sizes, every common frame ratio, at 300 DPI — so it looks as good at A1 as it does at 5×7.

> Everything you need for a full term, in one file. Print it once, use it every year.

**Two products, two moods, one voice.**
- **Wall art** — emotional, aspirational, sensory. Talk about rooms, light, mood, living with it.
- **Worksheets** — practical, generous, competent. Talk about time saved, ground covered,
  what it does for the person using it. Warm but *useful*.

Same vocabulary and rhythm; different promise. Never let the worksheet copy get corporate, and
never let the wall-art copy get precious.

**Never:** "instant download!!!", "limited time only", "only 3 left" (a lie on an infinite good —
it destroys trust faster than anything else on this list), "AI-powered", "premium quality" as a
bare claim with no specifics behind it.

---

## 3. Color

Keep the warm paper foundation for the **site chrome**. But there's a critical exception
Artisaire never had to solve:

> ⚠️ **Artwork previews must sit on a neutral ground.** A warm cream background casts a tint
> over every print preview and misrepresents the colors your customer is buying. Warm cream is
> right for the page; it is wrong directly behind artwork.

So: warm paper for the page, a **neutral gallery card** behind every artwork preview.

### Foundation
| Role | Value | Use |
|---|---|---|
| Paper base | `#FAF8F4` | Page background, warm off-white |
| **Gallery ground** | `#F4F4F2` | **Directly behind artwork previews — near-neutral, no cast** |
| Card / raised | `#FFFFFF` | Worksheet previews, modals, sticky buy bar |
| Alternating band | `#F1EDE6` | Section striping |
| Hairline | `#E4DED4` | Borders, dividers, the frame line around previews |
| Ink | `#2B2724` | Headlines, body |
| Muted ink | `#5A534B` | Secondary copy (darkened from Artisaire's for contrast compliance) |

### Accent — pick one and own it
Artisaire's sealing-wax red is *theirs*. You need your own. Recommended for art + printables:

| Option | Value | Reads as |
|---|---|---|
| **Clay** (recommended) | `#B4634A` / hover `#8F4B36` | Warm, earthy, gallery-adjacent, works with both categories |
| Ink blue | `#2F4156` / hover `#1E2C3A` | Studious, calm, leans the worksheet side |
| Deep olive | `#5A6248` / hover `#434A34` | Botanical, natural, leans the wall-art side |

Plus **antique brass `#A98A54`** for fine details, badges, and dividers.

### Category tinting (optional, subtle)
Give each category one tint used only for eyebrow labels and category tiles — never for large
fills: **Wall Art → clay `#B4634A`**, **Worksheets → ink blue `#2F4156`**, **Other → brass**.
This lets a mixed catalogue stay legible without a second design system.

### Rules
1. One accent per viewport.
2. **Never put a colored background behind an artwork preview.** Neutral or white only.
3. No pure black or white in the chrome, no cool grays, no gradients or glows.
4. Shadows barely exist: `0 1px 2px rgba(43,39,36,0.06)`. A print preview gets a `1px #E4DED4`
   hairline instead of a shadow — it reads as a mat, not a card.

---

## 4. Typography

Same two-family system as Artisaire. It survives the translation intact.

**Display serif** — light, high-contrast, weight 400 only, never bold.
*Canela, Ogg, Editorial New* / free: *Cormorant Garamond, Playfair Display, EB Garamond*
- H1 `clamp(2.75rem, 6vw, 5rem)` / lh `1.05` / ls `-0.02em`
- H2 `clamp(2rem, 4vw, 3.25rem)` / lh `1.12`

**Sans** — carries more weight here than at Artisaire, because worksheets are functional and
spec tables are everywhere.
*Söhne, Suisse Int'l* / free: *Inter, Work Sans*
- Body `1rem`–`1.0625rem` / lh `1.65` / measure 68ch
- Spec text / file lists `0.875rem` / lh `1.5` / tabular numerals on

**The eyebrow** stays the signature detail — uppercase, `11px`, weight 500, `0.18em` tracking,
on section headings, nav, buttons, and footer columns.

```css
.eyebrow {
  font-family: var(--sans);
  font-size: 0.6875rem;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.18em;
  color: #5A534B;
}
```

**Adaptation:** in worksheet sections, let the sans lead and the serif recede to section
headings only. In wall-art sections, the serif leads. **Still exactly two families** — the shift
is in proportion, not inventory.

**Use tabular numerals** (`font-variant-numeric: tabular-nums`) in every size chart, dimension
list, and price. It's a small thing that makes spec tables look engineered rather than typed.

---

## 5. Homepage Architecture

1. **Announcement bar** — `#F1EDE6`, tracked micro-type. Not free shipping — **"Instant
   download • Print at home or at a lab • 300 DPI files"**. This is your first trust signal;
   don't waste it on a discount code.
2. **Header** — sticky, `#FAF8F4`, `72–80px`. Wordmark left or centered, tracked uppercase nav.
   Mega-menu splits cleanly: **Wall Art** (by style / room / color) · **Worksheets** (by subject
   / age / use) · **Bundles** · **Freebies**.
3. **Hero** — full-bleed `78–88vh` styled interior with your art framed on the wall. One serif
   headline, one sentence, one button. Show the *outcome*, never a floating file icon.
4. **Category entry — 3 tiles.** Wall Art / Worksheets / Bundles. Portrait `4:5`, borderless,
   eyebrow + serif title. These two categories are different enough that a generic "Shop All"
   as the only door will lose people.
5. **"How it works" — 3 steps.** Choose → Download instantly → Print at home or at a lab.
   Physical stores don't need this; **digital stores absolutely do.** Thin brass line icons,
   one line of copy each. Removes the single biggest hesitation.
6. **Bestsellers carousel** — 4-up desktop, 1.4-up mobile. Artwork on gallery ground, not mockups
   (mockups on hover — see §8).
7. **Editorial split** — asymmetric 5/7 image/text, alternating sides. Use these to sell a
   *collection* or a use case ("A full term of phonics practice", "Warm neutrals for a quiet room").
8. **Quality / specs band** — the trust module. Full-bleed on the alternating band:
   **300 DPI · 5 aspect ratios · PDF + JPG + PNG · Instant delivery · Personal & commercial
   licensing available.** Set in tracked sans across a row. This is your "solid brass" —
   material honesty stated plainly.
9. **Maker's note** — a short, real paragraph about who designs this and how. Photo of the desk,
   the process, a hand at work if it's honest. Your provenance story.
10. **Freebie / lead magnet** — one genuinely good free download in exchange for an email.
    For digital goods the list *is* the business; give it a real section, not a popup.
11. **Reviews** — plainly stated count and rating, 2–3 short italic-serif testimonials.
12. **Newsletter + tall 4-column footer** — footer must carry **License terms, Print guide,
    Refund policy, FAQ**. These aren't legal afterthoughts; buyers actively look for them.

Section padding stays generous: `96px` mobile, `128–160px` desktop.

---

## 6. Product Page — the real work

Sticky preview gallery left, sticky buy column right.

### Preview gallery (left)
Order matters:
1. **The artwork flat**, full width, on gallery ground `#F4F4F2` with a `1px` hairline mat.
   Large — `1400px+`. Let people actually judge it.
2. **Room mockups** — 2–3 framed contexts, different rooms and frame colors.
3. **Scale reference** — the piece on a wall with a sofa or door for size sense.
4. **Detail crop** at 100% — proves the resolution. The digital equivalent of Artisaire's
   macro shot.
5. For worksheets: **every page** as a preview, or a clearly labelled representative set.
   Under-previewing worksheets is the #1 conversion killer in that category — people need to
   see what they're getting.

**Watermark previews, but lightly.** Heavy tiling makes the work impossible to judge and
insults the buyer. A single small mark in a corner, or a low-opacity diagonal, is enough.

### Buy column (right)
- Serif product title, price with tabular numerals, star rating
- **Format / size selector as labelled chips** — `A-series`, `US Letter`, `2:3`, `3:4`, `4:5`,
  `ISO`. Chips with **text labels**, never a bare dropdown, never color-only.
- One primary CTA: **"Instant download"** (not "Add to cart" — say what happens)
- **📄 What's included** — an explicit file manifest, always open, never hidden in an accordion:
  ```
  1 × PDF (print-ready, 300 DPI)     1 × JPG (300 DPI, 6000 × 9000 px)
  1 × PNG (transparent background)   5 aspect ratios · A1 → 5×7
  ```
  **This module is the single most important element on a digital product page.** It is your
  materials spec. Vagueness here loses the sale.
- Then accordions: **Print guide** (paper stock, home vs lab, recommended services) ·
  **License** (personal / commercial, in plain English, not legalese) · **Refunds** (digital
  goods are usually final sale — say it kindly and clearly up front rather than burying it)

### Below the fold
Full-bleed lifestyle shot → the maker's note → reviews with customer photos of *printed* results
(enormously persuasive — actively solicit these) → related products and the bundle upsell:
**"Part of the [Collection] — get all 12 for $34."**

---

## 7. Components

- **Primary button** — accent fill, white tracked uppercase label `0.75rem`, padding `16px 32px`,
  radius **`2px`**. Hover deepens over `200ms`.
- **Secondary** — `1px` ink border, transparent, inverts on hover.
- **Text link** — ink + trailing `→`, underline grows left-to-right on hover. Use these more
  than buttons in editorial sections.
- **Product card** — no shadow, no fill. Artwork on gallery ground with a hairline mat, then
  eyebrow category, serif name, price. **Hover cross-fades from flat artwork to room mockup**
  over `400ms` — this is the digital-store version of Artisaire's second-image hover, and it's
  the highest-value interaction on your site.
- **Worksheet card** — same frame, but show a *fanned multi-page* preview so the quantity reads
  instantly. Add a small tracked badge: `12 PAGES`.
- **File-type badges** — tiny tracked uppercase in brass, no filled pill. `PDF` `JPG` `PNG`.
- **Size chips** — bordered rectangles with text labels, `2px` radius, ink border when selected.
- **Inputs** — transparent, `1px #E4DED4`, eyebrow label above, ink border on focus.
- **Cart** — right-side drawer on paper ground.

---

## 8. Imagery & Mockup Art Direction

You have no product to photograph, so **mockup quality *is* your photography budget.** Bad
mockups are the fastest way to look like a template store.

- **Light:** soft, warm, directional daylight with visible falloff. Never flat, never harsh.
- **Interiors:** quiet, warm-neutral rooms — linen, oak, plaster, ceramics, a single plant.
  Uncluttered. The room supports the art; it never competes.
- **Frames:** vary them across the gallery — light oak, thin black, unfinished wood, a mat.
  Shows the art is versatile.
- **Worksheet staging:** printed pages on a warm wood or paper desk, with a pencil, a mug, a
  clipboard. Slight overhead angle. Makes a file feel like a thing you hold.
- **Also show:** a tablet or laptop for anything screen-usable, but **never as the only preview.**
- **Grade:** warm, slightly desaturated, film-like, lifted blacks — applied *identically* across
  every mockup. Inconsistent grading is what makes a digital store look scraped together.
- ⚠️ **Never let the grade touch the artwork itself.** The flat preview must be color-accurate.
  Grade the room, not the print.
- **Icons:** thin `1.25px` line only — download, print, file, ratio. Small custom set.
- **Optional motion:** a short silent loop of a print being placed in a frame or pages coming
  off a printer. Slow, no cuts.

---

## 9. Motion

`200–400ms`, easing `cubic-bezier(0.4, 0, 0.2, 1)`. Sections fade up `16px` once on scroll,
staggered `60ms`. Card image cross-fade `400ms`. Image hover scale `1.03` over `600ms` inside
`overflow:hidden`. No parallax, bounce, scroll-jacking, or counters. Honor
`prefers-reduced-motion`.

---

## 10. Trust & Conversion — digital-specific

Digital storefronts carry a credibility gap physical ones don't. Close it structurally:

- **State specs everywhere.** DPI, pixel dimensions, file formats, page counts, ratios.
- **Preview generously.** Every worksheet page. The detail crop at 100%.
- **Be explicit about licensing** in plain language, on the product page, not only in the footer.
- **Say refund terms up front,** warmly. Hiding "final sale" until checkout costs you trust and
  invites disputes.
- **Show printed results** from real customers.
- **Deliver instantly and say so** — the download link on screen *and* emailed.
- **Never fake scarcity or urgency.** You are selling an infinite good; every "only 2 left" is
  provably false and poisons everything else on the page.

## 11. Accessibility

Contrast-check `#5A534B` on `#FAF8F4` for body copy. Size and format chips need text labels, not
color alone. Descriptive alt text on every preview — this is a visual catalogue. Focus rings
`2px solid #2B2724` with `2px` offset. Tracked uppercase never below `11px`.

---

## 12. Anti-Patterns

✗ Colored or warm backgrounds behind artwork previews (misrepresents what's being sold)
✗ A room mockup as the *only* preview, with no flat artwork
✗ Heavy tiled watermarks that make the work impossible to judge
✗ Hiding the file list, dimensions, or license behind a collapsed accordion
✗ Fake scarcity or countdown timers on infinite goods
✗ Under-previewing worksheets — show the pages
✗ Grading or filtering the artwork preview itself
✗ Bold weights on the display serif · more than two typefaces · cool grays · pure black/white
✗ Pill buttons, drop shadows on cards, gradients, glassmorphism
✗ Dense 5-up grids — kills the editorial feel
✗ Generic marketplace mockups everyone else is using
✗ Emoji in the interface

---

## 13. Condensed Prompt (copy-paste)

> Design a refined, editorial e-commerce site for a digital store selling high-quality
> printable wall art, worksheets, and downloadable goods. The mood is *luxury earned through
> restraint* — a beautifully art-directed gallery catalogue that happens to be interactive. The
> central design challenge: digital files feel weightless, so the layout must give them the
> perceived weight of objects through scale, real-world context, and precise specification.
>
> **Color:** warm paper neutrals — `#FAF8F4` page, `#2B2724` warm near-black text, `#F1EDE6`
> bands, `#E4DED4` hairlines, `#5A534B` secondary — with one clay accent `#B4634A` (hover
> `#8F4B36`) and antique brass `#A98A54` for fine details. Critically: artwork previews sit on a
> **neutral `#F4F4F2` gallery ground with a 1px hairline mat**, never on warm cream, so print
> colors aren't misrepresented. No pure black/white, no cool grays, no gradients or shadows.
>
> **Type:** two families only. Light high-contrast display serif (Canela / Cormorant Garamond)
> for headlines, weight 400, never bold. Quiet sans (Söhne / Inter) for body and all spec text,
> with tabular numerals in every size chart and price. Signature detail: uppercase eyebrow
> labels at `11px`, weight 500, `0.18em` tracking above section headings and on nav and buttons.
> Serif leads in wall-art sections; sans leads in worksheet sections.
>
> **Layout:** 12-column, `1280px` max, 8px scale, `128–160px` section padding. Sticky header with
> a mega-menu split into Wall Art / Worksheets / Bundles → full-bleed `85vh` hero showing framed
> art in a styled room → 3 category tiles → a **"How it works" 3-step strip** (choose → instant
> download → print) → bestsellers → alternating editorial splits → a **specs trust band** (300
> DPI · 5 ratios · PDF/JPG/PNG · instant delivery · licensing) → maker's note → free download
> lead magnet → reviews → footer carrying license, print guide, and refund policy.
>
> **Product page:** sticky preview gallery (flat artwork large on neutral ground → room mockups →
> scale reference → 100% detail crop → every worksheet page) beside a sticky buy column with
> labelled ratio/format chips, an "Instant download" CTA, and an always-visible **"What's
> included" file manifest** listing formats, DPI, pixel dimensions, ratios, and page count. Then
> plain-English print guide, license, and refund accordions.
>
> **Components:** `2px` radius buttons with tracked uppercase labels; borderless product cards
> that **cross-fade from flat artwork to room mockup on hover** over `400ms`; fanned multi-page
> previews with a page-count badge for worksheets; brass file-type badges.
>
> **Imagery:** high-quality mockups are the entire photography budget — warm directional
> daylight, quiet linen/oak/plaster interiors, varied frame styles, printed worksheets staged on
> a wood desk. Consistent warm, slightly desaturated film grade on the *rooms only* — never on
> the artwork preview itself.
>
> **Motion:** slow and calm. `200–400ms`, one `16px` fade-up on scroll, `1.03` hover scale. No
> parallax or bounce.
>
> **Voice:** warm, assured, quietly expert. Human authorship as the trust anchor — designed by
> hand, test-printed, refined. Specific over vague: exact sizes, formats, and DPI instead of
> "premium quality." Wall art speaks to rooms, light, and mood; worksheets speak to time saved
> and ground covered. Absolutely no urgency tactics or fake scarcity on infinite goods.

---

### One thing to refine
The worksheet half of this brief points slightly different directions depending on your
audience — **classroom teachers**, **homeschool parents**, **business/productivity planners**,
or **kids' activities** each want a different warmth, density, and accent. The wall-art half
shifts too depending on style (abstract / botanical / vintage / line art / nursery). Tell me
which and I'll tighten the palette, voice, and worksheet card design around it.
