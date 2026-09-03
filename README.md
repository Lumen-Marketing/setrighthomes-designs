# Set Right Homes — five homepage directions

Five complete, self-contained homepage designs for **Set Right Homes**, an Arizona site work
company doing dirt work / site prep, utility connections, and setting manufactured homes.

**Live gallery:** https://lumen-marketing.github.io/setrighthomes-designs/

Open the gallery, flip between the five directions, toggle desktop vs phone, and open any
one full screen. Pick the one that feels like the company and we build that out properly.

---

## The five directions

| # | Name | Where it came from | Depth device | Type |
|---|------|--------------------|--------------|------|
| 01 | **Blue White** | The Mesic Contracting site, rebuilt in ice blue and white | Overlapping sheet layers | Manrope |
| 02 | **Midnight** | Black + red agency flyer, accent recoloured to electric blue | White card lifting off a dark ground | Archivo |
| 03 | **Cobalt** | Blue + orange construction social kit, orange swapped for white and sky | Arcs that crop content into domes | Figtree |
| 04 | **Blade** | Red diagonal flyer, field recoloured to royal blue | Angled planes shearing across the page | Barlow Condensed |
| 05 | **Sunburst** | Orange sunburst posters, recoloured blue on ice white | Hard offset sticker shadows plus tilt | Baloo 2 |

Direction 01 follows the section order of mesiccontracting.com as asked: hero, trust strip,
core services, "manufactured homes are different" explainer, process, stats, secondary work,
project gallery, testimonials, service area, FAQ, contact.

Every direction carries the **same content** so they can be compared fairly. What changes is
the personality: palette weighting, type, layout family, shape language and depth device.
No two share a corner radius system, a headline font, or a hero composition.

---

## What is in every design

- Full homepage: hero, services, process, projects, testimonials, service area, FAQ, contact
- Sticky nav that changes state on scroll, plus a working mobile drawer
- Scroll reveal with stagger, animated stat counters, card hover, button press states
- FAQ accordion, one panel open at a time, animated open and close
- Estimate form with inline validation, error states and a success state
- Mobile layouts declared explicitly per section, down to 360px
- `prefers-reduced-motion` honoured everywhere: all motion collapses to static

Each design is **one HTML file**. Nothing to build, nothing to install. Two external
resources only: Google Fonts and the Phosphor icon webfont.

---

## Before this goes live

### 1. Replace the placeholders

Every phone number, address, licence number and statistic is invented. Search any file for
`SWAP:` to find them all. Specifically:

| Placeholder | Currently |
|---|---|
| Phone | `(623) 555-0142` — a 555 number, deliberately non-working |
| Email | `office@setrighthomes.com` |
| Address | `PO Box 1188, Surprise, AZ 85374` |
| Licence | `AZ ROC #123456` |
| Homes set | `600+` |
| Years in business | `17 yrs` |
| Counties | `8` |
| Typical set week | `5 days` |
| Hours | Monday to Friday, 6:30am to 4pm |
| Testimonials | Three invented customers with invented names |
| Service area towns | Twelve West Valley and rural AZ towns |

Design 05 also advertises a **free lot walk**. Confirm that is an offer the business
actually wants to make before publishing it.

### 2. Drop in real photos

Every image slot currently holds a hand drawn technical view: a site plan with the pier grid
and utility runs, a compacted pad cross section, a pier and anchor cutaway, a trench section,
a skirting and final grade detail. They are accurate and they hold the layout, but real job
photos will beat them.

To swap one, find the comment above it:

```html
<!-- SWAP: photo of a finished compacted pad, 1000x620 -->
<div class="slot">
  <svg ...>...</svg>     <!-- replace this whole svg -->
</div>
```

Replace the `<svg>` with `<img src="..." alt="...">`. Nothing else changes; the container
keeps its own aspect ratio, radius and crop.

Photos worth shooting: a graded pad before delivery, a home coming off the toter, piers and
anchor straps before skirting, an open trench with the inspector's tape, and a finished home
with skirting and final grade.

### 3. Wire up the form

All five forms validate and show a success message, but they do not send anywhere. Point
them at an inbox, Formspree, Netlify Forms or a Supabase function before launch.

---

## Notes on decisions made

- **Light locked, not dual mode.** The brief specified a bluish white look, so the light
  palette is the brand and the pages do not flip to a dark theme on a phone set to dark mode.
  Design 02 is dark by design, not by system preference.
- **No stock photography.** Rather than fill the page with generic stock that reads as
  filler, the image slots carry real technical drawings until real photos exist.
- **Copy is plain contractor English.** Written to sound like someone who has actually stood
  on a lot: "soft fill under a pier shows up as a stuck door eighteen months later." Verify
  the technical claims against how the business actually runs before publishing.

---

## Files

```
index.html              gallery chooser
01-bluewhite/index.html
02-midnight/index.html
03-cobalt/index.html
04-blade/index.html
05-sunburst/index.html
```
