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

---

## Why every section heading was stuck at 40% of the row (02, 03, 04)

The section headings were capped with `max-width:12ch` to `16ch`. **`ch` is the advance
width of the digit zero**, and on a condensed display face that is roughly 0.40em, so a
`13ch` cap on a 74px headline lands at about 480px inside a 1160px measure. The headline
wrapped to five or six short lines against an empty right hand side, and the same cap sat
on the big statement block.

The fix was not to guess a wider number. Each heading was rendered in its own real
typeface at 100px, its natural single line width measured off the box, and the font size
worked back from that so the string fills the measure:

| | fills one line at |
|---|---|
| 02 Big Shoulders Display | 94px to 112px, was capped near 74px |
| 03 Saira Condensed | 84px to 103px, was capped near 62px |
| 04 Archivo Black | 69px to 88px, was capped near 56px |

Sizes were then set at about 96% of the fill so a rounding difference cannot push one
word onto a second line, with the `vw` term at `px / 14.4` so the fill holds as the
window narrows. Measured after the change: every section heading is **one line at 89% to
93%** of the measure at 1440, and still 85% at 1024.

The statement block is uncapped and sized to **three lines with the last at 59%**, read
off the real line boxes rather than estimated. At the first attempt it left a single
orphan word on a fourth line, which is what the `ch` caps had been hiding.

The three notes under it were capped at `76ch` to `80ch` and stopped between 65% and 78%
of the row. The body column now keeps a readable 64ch and the label column absorbs the
remainder, so the row spans the full width and the copy still sets at a sane length. A
sweep for any block reaching under 86% of its measure now returns nothing on all three
pages.

Two things fell out of the same audit and were fixed: 04's note body sat at **4.1:1** on
the burst ground and is now full white, and the nav carried both a phone link and a CTA
between 760px and 1010px where it did not fit, which pushed 03 into a 48px sideways
scroll. The phone link now steps out first. Horizontal overflow is zero at 505, 780, 880,
1024 and 1440.

### The same `ch` mistake, one level deeper

The first sweep measured fill against the page container, so it passed anything sitting
in a grid column. A second sweep, measuring every text block against **its own box**,
found the contact headings: they sit in a half width column and then carried a `13ch`
cap on top of that, so "Send us the lot. We send back a number." wrapped to **four lines
inside a 361px box**. Caps removed and sizes set from the measurement: 03 and 04 are now
two lines at 85% and 96%, and 02 needed its heading column widened to `1.14fr` as well.

The same second sweep is the one to run in future. Measuring against the page container
is not enough; anything inside a column has to be measured against the column.

### How A Job Runs, and the section that butted the one above it

Two more from the same pass on 01:

- The process block was five ruled rows of 15px copy on flat ice, the thinnest thing on
  the page. The sequence is the point, so it now has a numbered spine, headings at
  19-24px, and a photograph beside it. Ground stays plain, because the blue field above
  it and the survey contours below are both already carrying pattern.
- The navy panel section still had `padding-top:0` from when it followed another ice
  section. It follows the blurred photo block now, so it was butting a ground change with
  a negative gap. Measured section by section, text bottom to text top, rather than eyed.

The tablet nav fix was applied to 01 as well: it had the same phone pill plus CTA that
does not fit between 760px and 1010px.

### One row style survived the de-card pass, and it was the one hugging the edge

The de-card pass reset `.row` to no fill. `.navypanel .row` is a more specific selector, so
it kept its `rgba(255,255,255,.05)` tint while picking up `padding:16px 0` from the same
pass. A tinted block with zero horizontal padding puts the text flush against its own left
edge, which is what got flagged. Rows on this page are separated by a hairline and nothing
else, so the fill is gone and the panel padding went from `clamp(24px,3.4vw,48px)` to
`clamp(28px,4.2vw,56px)`, since the old clamp resolved to 30px at 880 and that is tight
for a block this dark.

**The check worth keeping:** walk every element that paints its own background, and flag
any that has text and under 10px of horizontal padding. A grep cannot find this one, because
the fill and the padding were declared in two different rules.

### The hero now ends at the fold

`min-height:clamp(560px,74vh,720px)` capped the hero at 720px, so on a normal laptop the
review ticker and the top of the next section were both visible on load. It is now
`clamp(560px,calc(100dvh - 36px),1000px)`: the `- 36px` is the utility bar above it, so the
hero ends **at** the fold rather than overshooting it, which is what pushed the stat bar
under on a short window.

The content still has to fit inside that, and below about 760px of window height it does
not. So everything in the hero steps down together in one query rather than the stat bar
falling off the bottom: headline to 44px, lede to 15px, and the stat bar to tighter
padding. Verified at 1440x900, 1920x1080, 1440x760, 1366x720 and 1600x820: the stat bar
and the floating menu both fit, and the ticker is below the fold every time.

The service area section was the last one still carrying `padding-top:0` from when it
followed a section with the same ground, and the two dark panels went to
`clamp(32px,5vw,68px)` of padding, so the text inset never drops below 32px at any width.
