# Set Right Homes - four homepage directions

Four complete homepage designs for **Set Right Homes**, an Arizona site work company doing
dirt work / site prep, utility connections, and setting manufactured homes.

**Live gallery:** https://lumen-marketing.github.io/setrighthomes-designs/

---

## The four directions

| # | Name | From | Material | Glass | Type |
|---|------|------|----------|-------|------|
| 01 | **Mesic** | mesiccontracting.com's layout, recoloured to bluish white and de-boxed | Drafting linen: rules, survey contours, paper grain | Frosted, on the three floating elements only | Bricolage Grotesque + Hanken Grotesk |
| 02 | **Site** | Black + red agency flyer, accent to electric blue | Film stock: grain on a shuffling gate, scanline, vignette, raked light shafts | Smoked, over photographs | Big Shoulders Display |
| 03 | **Plate** | Red diagonal flyer, field to royal blue | Brushed steel with a specular sweep, knurled blue field, tread plate on the seams | Machine guard glazing, bolted at four corners | Saira Condensed |
| 04 | **Burst** | Orange sunburst posters, recoloured blue | Screen print: 45 degree halftone with a misregistered second pull, paper grain | Frosted acetate, ink keyline and hard offset kept | Archivo Black |

**01 Mesic copies the reference site section for section**: navy utility bar, hero photo with a
left gradient and an eyebrow line, blue review ticker, heading plus checklist beside a form
card, before and after proof card, "homes are different" card, big navy panel with bordered
rows, Core Services photo cards, Also On The Truck photo cards, real results card, blue three
up strip, star reviews with quote marks, town chips beside a map, FAQ, contact, footer.
Section headings carry the same short accent underline. Cream became bluish white and the
amber CTA became blue.

---

## Material

None of the four uses a flat colour field any more. Each one owns a single material and
carries it everywhere, so the directions stay distinct from each other:

- **01 Mesic** is a drafting sheet. The 24px minor rule and 144px major rule are painted on
  `<body>`, so the grid runs continuously across every section seam instead of restarting
  at each one. Ice sections are translucent washes over that grid carrying concentric
  survey contours, like the rings on a grading plan. Navy panels get a raked hatch and an
  aggregate speckle.
- **02 Site** is film. Real grain shuffles on a four step gate the way a film gate does, a
  scanline sits at the threshold of visibility, a vignette pulls the eye back to centre,
  and raked light shafts cross the flat bands.
- **03 Plate** is milled metal. Horizontal linisher marks with a specular sweep across the
  width on every steel face; the blue field is knurled instead, a fine diagonal crosshatch
  like the grip on a hand tool, so the two alloys read differently. Tread plate on the
  sheared seams.
- **04 Burst** is printed. Halftone dot screens at 45 degrees with a second screen pulled
  two pixels off register, because a hand pulled print never lines up, and paper grain
  multiplied over the lot.

Every grain veil is a **fixed, `pointer-events: none`** layer, so it never repaints while
the page scrolls.

---

## Rhythm

Texture only reads as texture when something plain sits next to it. The first pass had it
on every ground, which flattened it back out again. So each page now runs **three kinds of
ground**, and no two patterned ones sit next to each other:

| Ground | What it is | How often |
|---|---|---|
| **Plain** | flat colour, nothing on it | most sections. This is the rest |
| **Photograph** | a picture is a ground in its own right, so nothing patterned is laid over it | heroes, chapters, contact bands |
| **Colour + texture** | the page's material at full strength | two or three sections, deliberately placed |

The split that decides it: **grain is the surface, the pattern is the ink.** Grain is the
paper, the film stock, the mill finish — it belongs everywhere and you should barely notice
it. The drafting rules, the light shafts, the brushed face and the halftone are marks made
*on* that surface, and you do not mark every square inch.

Where the ink lands:

- **01 Mesic** drafting rules on Core Services, survey contours on the service area. The
  navy panels and the review ticker keep their raked hatch, because those are objects on
  the page rather than the ground under it.
  The reference site is light the whole way down, and copying it left too long a pale run,
  so three things break it: the ice is pulled toward blue (`#EDF3FB` to `#E2EBF8`), a full
  bleed **photographic band** cuts in after Core Services, and the three up strip and the
  reviews now share one **blue field** with glass cards on it. Only Core Services and the
  FAQ are still white, which makes them read as bright accents rather than the default.
- **02 Site** raked light shafts on the process rail and the service area. Five sections
  are photographs. Everything else is flat near black.
- **03 Plate** the brushed face on the statement band and the service area; the blue field
  and the contact bar stay knurled. The plates themselves stay milled everywhere, because
  that is object material, not ground.
- **04 Burst** halftone on the hero, the blue plane, the service area and the contact band.
  It also gained a **full bleed photographic band**, which it did not have before, so all
  three grounds are present.

---

## Liquid glass

It runs through all four now, not just 01's nav. It is the same physical recipe every
time, retinted for the page it sits on: a blur, a saturation lift, a lit top edge, and a
hairline set 1px inside the border so the edge has thickness.

- **01** frosted glass on three elements only: the nav, the draggable jump menu, and the
  stat bar sitting on the hero photograph. Everything else lost its container, see below.
- **02** smoked glass: a draggable card floated over the hero photograph, the job lists
  inside each full bleed chapter, the figures rail, the contact details, the sticky nav,
  and a floating call pill that appears once the hero is behind you.
- **03** machine guard glazing: square cut, tinted toward the field blue, **bolted at four
  corners**. A draggable spec panel over the hero, the who-we-are list set into the blue
  field, the review cores inside their bolted steel frames, the contact details, the nav.
- **04** frosted acetate, a printed transparency pinned over the poster. It keeps this
  direction's two rules, the 2px ink keyline and the hard offset in the accent colour, so
  it reads as a sheet pinned to the print rather than a card floating over it.

There is **no official Apple liquid glass for the web**; these are approximations, and the
files say so. A solid fallback is provided under `prefers-reduced-transparency`, and
`backdrop-filter` is dropped below 760px, where a dozen stacked blurs costs real frames.

Ground and Poster were removed at your request.

---

## Photography

Every picture is a real, commercially licensed photograph, self hosted in `/assets`. Nothing
is drawn, nothing is hotlinked, nothing is a placeholder rectangle.

They are still **stand ins**. Replace them with Set Right Homes' own job photos and the site
gets substantially better. Worth shooting:

- a graded pad before delivery
- a home coming off the toter
- piers and anchor straps before skirting goes on
- an open trench with the inspector's tape
- a finished home with skirting and final grade

Licences and photographer credits are in [PHOTO-CREDITS.md](PHOTO-CREDITS.md). Several are
CC BY or CC BY-SA, which means **if you keep them, you must credit the photographer somewhere
on the site**. Using the client's own photos removes that obligation entirely.

---

## Before this goes live

**1. Replace the placeholders.** Search any file for `SWAP:`.

| Placeholder | Currently |
|---|---|
| Phone | `(623) 555-0142`, a 555 number, deliberately non working |
| Email | `office@setrighthomes.com` |
| Address | `PO Box 1188, Surprise, AZ 85374` |
| Licence | `AZ ROC #123456` |
| Figures | 600+ homes, 17 yrs, 8 counties, 5 day set week |
| Reviews | three invented customers |
| Towns | twelve West Valley and rural AZ towns |

Direction 04 also advertises a **free lot walk**. Confirm that is an offer the business makes.

**2. Wire up the form.** All five validate and show a success state, but they do not send
anywhere. Point them at an inbox, Formspree, Netlify Forms or a Supabase function.

---

## Notes

- **Light locked, not dual mode.** The brief specified a bluish white look, so the light
  palette is the brand. Directions 02 and 03 are dark by design, not by system preference.
- **Counters degrade safely.** The animated figures hold their final value in the markup and
  only animate when they scroll into view, so a JS or observer failure shows a real number
  rather than a zero.
- **Motion honours `prefers-reduced-motion`** everywhere. Every reveal, counter and hover
  collapses to static, including 02's animated film grain.
- **Blur is kept off scrolling containers.** It sits on fixed and sticky chrome and on
  discrete cards, never on large scrolling areas, and is switched off entirely on phones.

## Files

```
index.html               gallery chooser
assets/                  14 licensed photographs, self hosted
PHOTO-CREDITS.md         licence and attribution for each
01-mesic/index.html
02-site/index.html
03-plate/index.html
04-burst/index.html
```

---

## The de-slop pass on 01

The client's boss said it read as AI made. He was right, and the cause was mine: liquid
glass had been asked for, and I had put a card round every single thing on the page.

Audited against the anti-slop checklist, 01 failed six ways and the other three
directions failed none of them. What it had:

- **17 boxed component types** on one page. Panel, form, service card, review, FAQ row,
  map, thumbnail, trio, town chip, hint, list row, nav list, contact row, strip cell,
  stat cell, photo band cell, badge.
- **Six identical three-equal-column grids.** The single most templated AI pattern.
- **20 decorative dots**, none of which meant anything.
- **One font family** for the whole page, so nothing had a voice.
- **Explainer paragraphs** restating their own heading.
- **Eight different corner radii**, and spacing off any grid: 9, 11, 13, 14.5px.

What it has now:

- **Four containers, and each earns it.** The form, because a form is genuinely a
  container. The proof plate, because it is the one white plate on the navy field. The
  navy panel, because it is a colour block. The three glass elements, because they float
  over photography and are the thing that was asked for. Everything else is separated by
  a hairline, by space, or by weight.
- **Core Services is one large item beside two stacked**, which is a different layout
  family from the three up that follows it.
- **Bricolage Grotesque** for display against a light **Hanken Grotesk** body. Bold
  engineered display against a quiet body carries the hierarchy the boxes were carrying.
- **One shape rule**: everything square, buttons 4px.
- **8pt spacing** throughout: 8 16 24 32 40 48 64 80 96.
- Explainer paragraphs, both eyebrow pills, every decorative dot and two duplicate CTA
  labels are gone. The hero headline is two lines instead of four.

Directions 02, 03 and 04 were audited the same way and passed. 02 has one corner radius
and one boxed type. 03's bolted plates and 04's ink keylines are the concept of those
directions, not decoration, so they stay.

---

## The glass, the grounds and the photo galleries (01 Mesic)

Three things were wrong and one was missing.

### The glass was a tinted rectangle

`backdrop-filter` on its own is a blur, not a material. The first attempt at fixing it
overcorrected: four directional inner glows, one per side, plus a 1px border and rim
lines down both edges. That is not thickness, that is **a white frame drawn round a
box**, and it was the next thing to get flagged.

Glass is lit from ONE direction. So the pane now has no border at all, no side or bottom
glows, and only a hairline catch along the top edge with a soft falloff under it. A
shallow sheen sits across the top third, inset from both sides so it can never close
into an outline. Everything else is the backdrop coming through, at `saturate(230%)` so
the colour of whatever is behind survives the tint.

The second missing piece is that light on glass **moves**. A specular hot spot now
follows the pointer, driven by two custom properties written from one passive
`pointermove` coalesced into a single animation frame. It is dim at rest and only lights
up while the pointer is on that pane, which is both more physical and safer for
contrast.

The third is shape. A lens has no corners. The glass is the only thing on this page with
a radius, and that is what makes it read as a different material from the paper it
floats over.

**Contrast was measured on the rendered pixels, not assumed.** At the first attempt the
white labels on the stat bar sat at 3.4:1 and the menu labels at 2.4:1. Fixing it took
a heavier navy tint, `brightness(.94)` (glass attenuates, it does not brighten), moving
the resting highlight off the label row, and dropping its strength from .40 to .13.
Worst ratio on any glass now measures 4.81:1.

### Two grounds that were flat colour

- **`.aggregate`** on the estimate block. Four dot lattices at sizes that share no
  factor, so they never line up into a visible grid. It reads as compacted base course,
  which is the material this company actually sells.
- **`.blurshot`** on the manufactured-homes block. A photograph at `blur(34px)` used as a
  colour field rather than as an image. The scrim is light because the type on it is
  ink. Measured at 3.7:1 against the body grey on the first pass, so that section scopes
  its own darker `--muted` and the scrim was lifted. Now 5.25:1 at its worst row.

### The same three-photo grid, twice

Photography is what this business sells and a 320px thumbnail sells nothing. Both grids
are gone, replaced by two different layout families so the two photo sections do not
read as one repeated block:

- **Accordion strip** for the services. Six panels share the width; the one under the
  pointer takes a third of it and opens its copy. Hover, focus and tap all drive the same
  state. Below 900px it becomes a plain stack with every caption already open.
- **Drag filmstrip** for recent work. Mixed slide widths, scroll snapped, running off the
  right edge of the page. Drag to pan, arrow buttons, arrow keys, and a progress rule that
  is sized once and then only translated so nothing lays out while the strip moves.

The empty ground both of those sections left underneath got filled: a photograph under
the estimate checklist, and a sticky short column beside the long about list.

**Shape rule, updated:** everything square, buttons 4px, glass 26px. That is the one
documented exception and it applies to nothing else.
