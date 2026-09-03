# Set Right Homes - four homepage directions

Four complete homepage designs for **Set Right Homes**, an Arizona site work company doing
dirt work / site prep, utility connections, and setting manufactured homes.

**Live gallery:** https://lumen-marketing.github.io/setrighthomes-designs/

---

## The four directions

| # | Name | From | Material | Glass | Type |
|---|------|------|----------|-------|------|
| 01 | **Mesic** | A direct copy of mesiccontracting.com's layout, recoloured to bluish white | Drafting linen: one continuous grid under the whole page, survey contours, film grain | Frosted, over the drafting ground | Plus Jakarta Sans |
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

## Liquid glass

It runs through all four now, not just 01's nav. It is the same physical recipe every
time, retinted for the page it sits on: a blur, a saturation lift, a lit top edge, and a
hairline set 1px inside the border so the edge has thickness.

- **01** frosted glass on the nav, the draggable jump menu, a stat bar hung across the hero
  seam so the photograph refracts through it, the form card, every panel, card, review,
  FAQ row, process row, town chip and the map. Dark glass inside the navy panels.
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
