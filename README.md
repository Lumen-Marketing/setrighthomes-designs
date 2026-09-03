# Set Right Homes - five homepage directions

Five complete homepage designs for **Set Right Homes**, an Arizona site work company doing
dirt work / site prep, utility connections, and setting manufactured homes.

**Live gallery:** https://lumen-marketing.github.io/setrighthomes-designs/

---

## The five directions

| # | Name | From | Depth device | Type | Density |
|---|------|------|--------------|------|---------|
| 01 | **Ground** | Mesic Contracting's section order, in ice blue | Crossing planes, photos bleeding off the viewport | Schibsted Grotesk | mid |
| 02 | **Site** | Black + red agency flyer, accent to electric blue | Three planes: photo, scrim, plate hung across the boundary | Big Shoulders Display | sparse |
| 03 | **Poster** | Blue + orange construction kit, recoloured cobalt | Offset trays with a core at a concentric radius | Bricolage Grotesque | mid |
| 04 | **Plate** | Red diagonal flyer, field to royal blue | Machined steel: bevelled edges, bolts, recessed panels | Saira Condensed | dense |
| 05 | **Burst** | Orange sunburst posters, recoloured blue | A ray field that laps over the content, hard printed offsets | Archivo Black | loud |

No two share a hero composition, a corner radius system, a display face, or a depth device.
They deliberately do not share a section order either. Only the content is the same, so the
comparison is about design.

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

Direction 05 also advertises a **free lot walk**. Confirm that is an offer the business makes.

**2. Wire up the form.** All five validate and show a success state, but they do not send
anywhere. Point them at an inbox, Formspree, Netlify Forms or a Supabase function.

---

## Notes

- **Light locked, not dual mode.** The brief specified a bluish white look, so the light
  palette is the brand. Directions 02 and 04 are dark by design, not by system preference.
- **Counters degrade safely.** The animated figures hold their final value in the markup and
  only animate when they scroll into view, so a JS or observer failure shows a real number
  rather than a zero.
- **Motion honours `prefers-reduced-motion`** everywhere. Every reveal, counter and hover
  collapses to static.

## Files

```
index.html               gallery chooser
assets/                  14 licensed photographs, self hosted
PHOTO-CREDITS.md         licence and attribution for each
01-ground/index.html
02-site/index.html
03-poster/index.html
04-plate/index.html
05-burst/index.html
```
