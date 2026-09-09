# Design Prompt — "Artisaire" Aesthetic

A reusable art-direction brief for building a site, landing page, or brand system in the
style of a modern heritage-craft stationery brand (wax seals, invitations, fine paper goods).

---

## 1. The One-Paragraph Brief

Design a refined, editorial e-commerce experience for a heritage craft brand that makes wax
seals, brass wax stamps, sealing wax, invitations, and fine stationery. The brand has spent
decades perfecting one small, tactile craft, and the design must communicate that: **luxury
earned through restraint, not ornament.** Everything is poured, pressed, and engraved by hand
in a real studio, so the site should feel like a beautifully art-directed print catalogue that
happens to be interactive — generous white space, oversized product photography, quiet
typography, and a warm, paper-toned palette. The product is small and precious; the layout's
job is to make it feel monumental. Nothing on screen should compete with the wax.

---

## 2. Tone & Voice

**Personality:** Warm, assured, quietly expert. A skilled artisan showing you their work —
proud but never boastful, precise but never clinical.

**Voice attributes**
- **Sensory over technical.** Talk about how things feel: *"buttery smooth," "poured by hand,"*
  *"the right hardness to hold perfect detail."* Lead with texture, then specs.
- **Confident and unhurried.** Short declarative sentences. No exclamation marks, no urgency
  timers, no "HURRY — SALE ENDS." Scarcity is not the lever; craft is.
- **Emotionally anchored to occasions.** Copy is about weddings, love letters, thank-you notes,
  proposals, moments people keep. Frame the product as the thing that makes a moment last.
- **Second person, invitational.** *"Design your own." "For all the ways you love to connect."*
- **Provenance is a feature.** Say where it's made, who made it, and how. Name collaborators
  and artists explicitly.

**Sample lines in-voice**
> Poured and pressed in our studio, for letters, invitations, and moments you want people to keep.

> Engraved in solid brass — a metal that's both gorgeous and exactly the right hardness to hold
> perfect detail.

> Hand-blended for maximum, mail-safe durability, while staying true to a traditional,
> buttery-smooth feel.

**Never sound like:** a discount retailer, a tech startup, a dropshipper, or a luxury brand that
shouts. Avoid "revolutionary," "game-changing," "premium quality," "shop now before it's gone."

---

## 3. Color

The palette is drawn from **paper, wax, and brass.** A near-neutral warm base carries ~90% of
the surface area; saturated color enters almost exclusively through product photography and one
restrained accent.

### Foundation (the page itself)
| Role | Value | Use |
|---|---|---|
| Paper base | `#FAF8F4` | Default page background — warm off-white, never pure `#FFF` |
| Card / raised surface | `#FFFFFF` | Product cards, modals, sticky bars |
| Alternating band | `#F1EDE6` | Section striping to segment a long homepage |
| Warm greige | `#E4DED4` | Hairline borders, dividers, input outlines |
| Ink | `#2B2724` | Headlines and body copy — warm near-black, never `#000` |
| Muted ink | `#6B635B` | Secondary copy, captions, meta, placeholders |

### Accent (used sparingly and deliberately)
| Role | Value | Use |
|---|---|---|
| Sealing wax red | `#8C2F30` | The signature accent — primary CTA, active states, sale tags |
| Deep burgundy | `#5E1F28` | Hover state for the accent, footer background option |
| Antique brass | `#A98A54` | Hairline flourishes, icon strokes, "custom" badges, dividers |
| Sage | `#9BA68E` | Secondary category tint, botanical collections |
| Dusty rose | `#C9A29A` | Wedding-category tint, soft highlights |

### Rules
1. **One accent per viewport.** If a red CTA is on screen, nothing else may be red.
2. **Color arrives through photography.** The wax itself supplies the saturation — sage, terracotta,
   navy, blush, gold. The UI stays neutral so a 36-color product range never clashes with it.
3. **No pure black, no pure white, no cool grays.** Every neutral carries warmth. A cool gray
   instantly reads as generic SaaS and breaks the paper illusion.
4. **No gradients, no glows, no glassmorphism.** Flat, printed, matte.
5. Shadows are barely-there and warm: `0 1px 2px rgba(43,39,36,0.06)`. Elevation comes from
   spacing, not drop shadows.

---

## 4. Typography

A two-family system: a **high-contrast serif** for voice and a **quiet sans** for utility.
The serif does the emoting; the sans gets out of the way.

### Display / Headline — refined serif
Use a transitional or Didone-adjacent serif with real thick-thin contrast and elegant,
slightly condensed forms.
*Candidates:* Canela, Ogg, Freight Display, Editorial New, Reckless.
*Free alternates:* Cormorant Garamond, Playfair Display, EB Garamond, Lora.

- H1 — `clamp(2.75rem, 6vw, 5rem)` / line-height `1.05` / letter-spacing `-0.02em` / weight 400
- H2 — `clamp(2rem, 4vw, 3.25rem)` / line-height `1.12` / letter-spacing `-0.015em`
- H3 — `1.5rem` / line-height `1.25`
- **Weight stays light-to-regular.** Never bold the display serif — elegance lives in the
  thin strokes, and bolding destroys it. Size and space create hierarchy, not weight.
- Sentence case for headlines. Title Case only for product names.

### Body / UI — humanist or neo-grotesque sans
*Candidates:* Söhne, Suisse Int'l, Neue Haas Grotesk, GT America.
*Free alternates:* Inter, Work Sans, Karla, Jost.

- Body — `1rem`–`1.0625rem` / line-height `1.65` / weight 400 / max measure **68ch**
- Small / meta — `0.8125rem` / line-height `1.5` / color `#6B635B`

### The eyebrow — the signature move
Wide-tracked, uppercase micro-labels above headlines and as section markers. This single
detail does more for the "fine stationery" feel than anything else.
```css
.eyebrow {
  font-family: var(--sans);
  font-size: 0.6875rem;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.18em;
  color: #6B635B;
}
```
Apply the same treatment to: nav links, button labels, tab labels, footer column headings,
and breadcrumb trails.

### Rules
- **Exactly two families.** A third is clutter.
- Never letterspace lowercase serif text. Only uppercase sans gets tracking.
- Italic serif is reserved for pull quotes and testimonials — it should feel like handwriting's
  well-mannered cousin, used maybe twice per page.
- No text shadows, no all-caps body copy, no underlines except on inline links.

---

## 5. Layout & Grid

**Structure:** 12-column grid, `1280px` max content width, `1440px` for full-bleed imagery
sections. Gutters `24px` mobile / `32px` desktop.

**Spacing scale (8px base):** `8 / 16 / 24 / 32 / 48 / 64 / 96 / 128`.
Section vertical padding is generous — `96px` mobile, `128–160px` desktop. **When a layout
feels wrong, the fix is almost always more space, not more design.**

### Page architecture (homepage, top to bottom)
1. **Announcement bar** — one line, centered, uppercase tracked micro-type, `#2B2724` on
   `#F1EDE6`. Free shipping threshold or a seasonal note. Dismissible.
2. **Header** — sticky, `#FAF8F4`, `72–80px` tall. Wordmark centered *or* hard left; nav in
   tracked uppercase sans; right cluster = search, account, cart. A hairline bottom border
   (`1px #E4DED4`) appears only after scroll. Category nav opens a **mega-menu** with text
   columns plus one featured image tile.
3. **Hero** — full-bleed lifestyle photograph, viewport height `78–88vh`. A single serif
   headline plus one sentence and one button, left-aligned in the lower third or centered on
   a quiet area of the image. Text sits on the photo directly where contrast allows; otherwise
   a soft `rgba(43,39,36,0.25)` scrim, never a heavy overlay.
4. **Category tiles** — 3 or 4 across (`Wax Seals` / `Wax Stamps` / `Sealing Wax` / `Invitations`).
   Portrait `4:5` images, an eyebrow label and a serif title beneath. No borders, no cards —
   the photos are the tiles.
5. **Editorial split** — asymmetric 5/7 or 7/5 image-and-text pair. Image bleeds to one page
   edge; text block sits in generous white space with an eyebrow, serif H2, two-sentence
   paragraph, and a text-link CTA with an arrow. Alternate sides down the page.
6. **Bestsellers carousel** — 4-up desktop, 1.4-up mobile (peek the next card to signal swipe).
   Free-scroll with hidden scrollbar; minimal arrow controls.
7. **Custom / made-to-order block** — the highest-value path. Full-bleed dark or wax-red band
   with centered serif copy and a single strong CTA. This is the one place a saturated
   background is allowed.
8. **Craft / provenance story** — studio and process photography (hands, molten wax, brass
   engraving) with short copy about hand-pouring and in-house manufacturing.
9. **Social proof** — review count and star rating stated plainly, plus 2–3 short testimonials
   in italic serif. Understated, no badge clutter.
10. **Instagram / UGC grid** — 5–6 square images edge to edge, one line of copy above.
11. **Newsletter** — centered, single input with an inline submit, one line of copy. On the
    alternating band color, not on a colored field.
12. **Footer** — 4 link columns with tracked uppercase headings, wordmark, payment icons,
    country/currency selector, legal row. On `#F1EDE6` or `#2B2724`, tall and calm.

### Product page
Sticky image gallery on the left (or a vertical scrolling stack), sticky buy-column on the
right containing: product title in serif, price, review stars, **color/variant swatches as
actual round wax-colored chips** (never a dropdown), quantity, one primary CTA, then collapsible
accordions for Details / Materials / Shipping. Below the fold: a full-bleed lifestyle photo,
a "how it's made" strip, reviews, and related products.

### Responsive
Mobile is a single column with the same generous rhythm — do not compress the spacing scale
below `64px` section padding. Multi-column tile rows become horizontal scrollers rather than
stacking into an endless column. The mega-menu becomes a full-screen drawer with an accordion.

---

## 6. Components

- **Primary button** — solid `#8C2F30`, white uppercase tracked label at `0.75rem`, padding
  `16px 32px`, border-radius **`2px`** (near-square; softness comes from color, not corners).
  Hover deepens to `#5E1F28` over `200ms`.
- **Secondary button** — `1px` solid `#2B2724`, transparent fill, ink label. Hover inverts to
  solid ink with paper-colored text.
- **Text link CTA** — ink label with a trailing arrow `→` and a `1px` underline that grows from
  left to right on hover. Use this far more often than buttons in editorial sections.
- **Product card** — no border, no shadow, no background. Portrait `4:5` image, then eyebrow
  category, serif name, price. Hover swaps to a second image with a `400ms` cross-fade and
  reveals a "Quick add" bar at the image's base.
- **Inputs** — transparent fill, `1px #E4DED4` bottom-or-full border, label above in eyebrow
  style. Focus turns the border to `#2B2724`. No rounded pills.
- **Badges** — tiny tracked uppercase text in brass or ink, no filled pill background.
  "Handmade," "Made to order," "New."
- **Cart** — a right-side drawer on paper background, not a page redirect.

---

## 7. Imagery & Art Direction

Photography carries the entire brand. Budget accordingly — this design fails completely with
stock imagery.

- **Light:** soft, warm, directional daylight. Gentle shadows with visible falloff. Never flat
  studio lighting, never hard flash.
- **Surfaces:** textured paper, linen, marble, raw wood, silk ribbon. The materials should read
  as touchable.
- **Composition:** confident negative space — often the product occupies a third of the frame
  with the rest given to a quiet surface. That empty space is where the headline lands.
- **Three photo types, mixed deliberately:**
  1. *Macro detail* — the seal's impression, wax texture, brass engraving. Shallow depth of field.
  2. *Styled flat lay* — invitation suites shot from directly above with envelopes, ribbon,
     florals, and stamps arranged with editorial precision.
  3. *Hands at work* — the studio, molten wax being poured, a stamp being pressed. Provenance
     made literal.
- **Grade:** warm, slightly desaturated, film-like. Lifted blacks, creamy highlights. Consistent
  across every image — a mismatched grade is the fastest way to break this design.
- **Iconography:** thin `1.25px` line icons only, minimal set (search, account, cart, arrows).
  Custom botanical or crest line-illustrations may appear as decorative dividers in brass.
- **Video:** short, silent, autoplay-loop clips of wax pouring or a seal lifting away. Muted,
  slow, no cuts.

---

## 8. Motion

Restrained and slow. The site should feel calm and considered, never springy or playful.

- Transitions `200–400ms`, easing `cubic-bezier(0.4, 0, 0.2, 1)`.
- Sections fade up `16px` on scroll into view, once, staggered `60ms` between siblings.
- Image hovers scale `1.03` over `600ms` inside an `overflow:hidden` frame.
- No parallax, no bounce, no scroll-jacking, no counters, no confetti.
- Respect `prefers-reduced-motion` by disabling all transforms and fades.

---

## 9. Accessibility & Craft Details

- Verify contrast: `#6B635B` on `#FAF8F4` is fine for meta text but **must not** be used for
  body copy at small sizes — drop to `#5A534B` if it fails 4.5:1.
- Wax-color swatches need text labels (not color alone) for variant selection.
- Every image needs descriptive alt text — this is a visual product catalogue.
- Visible focus rings: `2px` solid `#2B2724` with `2px` offset. Do not remove outlines.
- Tracked uppercase text must never drop below `11px`.

---

## 10. Anti-Patterns — do not do these

✗ Pure white background or pure black text
✗ Bold weights on the display serif
✗ Rounded, pill-shaped buttons or `12px+` border radii
✗ Drop shadows and card borders on product tiles
✗ Countdown timers, spinning discount wheels, aggressive popups
✗ More than two typefaces
✗ Cool gray neutrals
✗ Gradients, glows, glassmorphism
✗ Dense grids — 5+ products per row destroys the editorial feel
✗ Stock photography of generic "office supplies"
✗ Emoji anywhere in the interface

---

## 11. Condensed Prompt (copy-paste version)

> Design a refined, editorial e-commerce site for a heritage craft brand selling handmade wax
> seals, solid-brass wax stamps, sealing wax, and fine invitations. The mood is *luxury earned
> through restraint* — a beautifully art-directed print catalogue that happens to be
> interactive.
>
> **Color:** warm paper neutrals only — `#FAF8F4` background, `#2B2724` warm near-black text,
> `#F1EDE6` alternating bands, `#E4DED4` hairlines — with a single sealing-wax red accent
> `#8C2F30` (hover `#5E1F28`) and antique brass `#A98A54` for fine details. No pure black or
> white, no cool grays, no gradients or shadows. All saturation comes from product photography.
>
> **Type:** two families. A light, high-contrast display serif (Canela / Cormorant Garamond) for
> headlines at `clamp(2.75rem, 6vw, 5rem)`, weight 400 only — never bold. A quiet sans (Söhne /
> Inter) for body at `1rem`/`1.65` line-height and a 68ch measure. Signature detail: uppercase
> eyebrow labels at `11px`, `500` weight, `0.18em` letter-spacing above every section heading,
> and on all nav links and button labels.
>
> **Layout:** 12-column, `1280px` max width, 8px spacing scale, `128–160px` section padding.
> Sticky minimal header with a mega-menu → full-bleed `85vh` hero with one serif headline and
> one button → 4 portrait category tiles (`4:5`, no borders) → alternating asymmetric editorial
> image/text splits → bestsellers carousel → a full-bleed wax-red custom-orders band → studio
> craft story → understated reviews → Instagram grid → newsletter → tall 4-column footer.
>
> **Components:** near-square `2px` radius buttons with tracked uppercase labels; borderless,
> shadowless product cards with a `400ms` image cross-fade on hover; round wax-colored chips for
> variant selection; underline-grow text links with trailing arrows.
>
> **Imagery:** soft warm directional daylight, textured paper and linen surfaces, generous
> negative space, macro wax detail, styled overhead flat lays, and hands-at-work studio shots.
> Warm, slightly desaturated film grade applied consistently.
>
> **Motion:** slow and calm — `200–400ms` transitions, a single `16px` fade-up on scroll, subtle
> `1.03` image hover scale. No parallax, bounce, or scroll-jacking.
>
> **Voice:** warm, assured, quietly expert. Sensory and tactile ("poured by hand," "buttery
> smooth," "engraved in solid brass"). Occasion-led — weddings, love letters, thank-you notes,
> moments people keep. Provenance stated plainly. No urgency tactics, no exclamation marks,
> no hype.

---

## Provenance note

This brief was assembled from the brand's published copy, product architecture, and third-party
descriptions of its storefront, gathered via web search. The live site could not be rendered
directly from this environment (the domain is blocked by the network egress policy), so the
**structural, color, and typographic specifications above are art direction consistent with the
brand rather than measured values read off the page.** Exact hex codes, font files, and section
order should be verified against the live site before being treated as a spec.
