# USA

A nine-night itinerary across two countries — **New York → Las Vegas → Toronto**,
built as a single self-contained web page.

## The page

`index.html` is one file. No build step, no dependencies, no server — open it
in a browser and it runs. Everything is inlined, including the paintings.

Open it locally:

```bash
open index.html
```

## What's in it

**Itinerary** — the opening screen is cut in half by Hassam's *Winter in Union
Square*. Scrolling opens the painting to full bleed and walks the nine days: three
paintings cross-fading as you move city to city, with a pinned card whose copy
changes underneath you. Any day expands to the full schedule with timestamps.

**Hotels** — two shortlisted candidates per city with the trade-offs kept rather
than smoothed over, on a black room of glowing wires.

**Tickets** — what has to be booked ahead and how far ahead. Marks are kept in
your browser only.

**Travel** — three cities as circles. Pick one and its painting takes the frame,
with the whole intra-city route: transfers, durations, what actually takes longer
than the map says.

**Papers** — ESTA, eTA, I-94 and preclearance, in plain language.

## Design

Built on the *Structured* design system (Refero) — putty and ink, Playfair Display
against Inter, hairline borders, no shadows, no gradients. `bar.md` records the
mechanisms it was built against and where the reference's own token export turned
out to disagree with the rendered site.

## Paintings

All public domain:

| Painting | Artist | Source |
|---|---|---|
| *Winter in Union Square* (1889–90) | Childe Hassam | The Metropolitan Museum of Art |
| *Grand Canyon of the Colorado River* | Thomas Moran | Google Art Project |
| *Niagara* (1857) | Frederic Edwin Church | National Gallery of Art |
| *The Rocky Mountains, Lander's Peak* (1863) | Albert Bierstadt | The Metropolitan Museum of Art |

## Status

Dates are not set. Hotels are shortlisted, not booked. Nothing here is a
reservation — verify entry requirements with official sources before travelling.
