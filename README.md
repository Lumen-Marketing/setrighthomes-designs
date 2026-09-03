# Set Right Homes - four homepage directions

Four complete homepage designs for **Set Right Homes**, an Arizona site work company doing
dirt work / site prep, utility connections, and setting manufactured homes.

**Live gallery:** https://lumen-marketing.github.io/setrighthomes-designs/

---

## The four directions

| # | Name | From | Depth device | Type |
|---|------|------|--------------|------|
| 01 | **Mesic** | A direct copy of mesiccontracting.com's layout, recoloured to bluish white | Liquid glass over photography | Plus Jakarta Sans |
| 02 | **Site** | Black + red agency flyer, accent to electric blue | Three planes: photo, scrim, plate hung across the boundary | Big Shoulders Display |
| 03 | **Plate** | Red diagonal flyer, field to royal blue | Machined steel: bevelled edges, bolts, recessed panels | Saira Condensed |
| 04 | **Burst** | Orange sunburst posters, recoloured blue | A ray field that laps over the content, hard printed offsets | Archivo Black |

**01 Mesic copies the reference site section for section**: navy utility bar, hero photo with a
left gradient and an eyebrow line, blue review ticker, heading plus checklist beside a form
card, before and after proof card, "homes are different" card, big navy panel with bordered
rows, Core Services photo cards, Also On The Truck photo cards, real results card, blue three
up strip, star reviews with quote marks, town chips beside a map, FAQ, contact, footer.
Section headings carry the same short accent underline. Cream became bluish white and the
amber CTA became blue.

**Liquid glass** is used on 01's sticky nav and its floating jump menu, matching the
LiquidGlassCard component supplied. It is a web approximation of that material: layered
translucency, a 1px inner border, a specular highlight and an inner shadow for edge
refraction. There is no official Apple liquid glass for the web. A solid fallback is
provided under `prefers-reduced-transparency`, and the nav turns solid white once you
scroll past the hero so the links stay readable.

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
  collapses to static.

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
