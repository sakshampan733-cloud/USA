# bar.md — mechanisms from the reference

**Reference:** Refero "Structured" · **Live site:** https://structured.money (refuses all connections from here)

## Sources, in order of authority

1. **Official token export** (DESIGN.md / Tailwind / CSS vars / Design Tokens JSON) — supplied by the user. Authoritative for colour, type, spacing, radius.
2. **Rendered hero frame** — one JPEG, pulled off `images.refero.design` with curl. Authoritative where pixels and tokens disagree.
3. Nothing else exists. Refero holds exactly one screenshot; the live site is unreachable.

**There is no motion in any source.** Not one keyframe, duration, easing or scroll rule.

---

### 1. Tokens, applied verbatim
Putty `#c4c3b6` canvas · Ink `#000000` rooms · Bone `#e7e5e4` cards · Chalk `#ebebeb` footer ·
Vellum `#dfdcd5` hairlines · Graphite `#595855` muted · Paper `#ffffff` reverse.
Radii 2 / 9 / 28.8. Section gap 80, card padding 24, element gap 6. Base unit 4.
Serif 16/24/34/52/94/374 · grotesk 9/12/15/16/22/24/26/43. Body is 15px grotesk.

**Fail if:** a colour, radius or type size is off this list.

### 2. Two grounds, hard cuts
Putty and Ink alternate. No gradient, no shadow, no elevation anywhere.

### 3. The wordmark crops — intent over literal value
Mixed case, weight 500, line-height 0.84, tight negative tracking, **cut by both frame edges**.
The token says 374px; that figure assumes Davinci setting the 10-letter "Structured". "Parallel"
is 8 letters in Playfair and stops short of the frame at 374px, so it is sized in `vw` to hold
the stated intent — *"should always feel larger than the screen."*

**Fail if:** the whole word is legible with margin on both sides.

### 4. The action button is a hexagon — pixels beat tokens ✗ token wrong
Tokens say `--radius-buttons: 28.8px`. The rendered button is a **stretched hexagon**: flat top
and bottom, angled ends. Verified by cropping and enlarging the frame. Built as a hexagon with
the 28.8px radius kept underneath as fallback.

### 5. The stat pair is serif — pixels beat prose ✗ prose wrong
DESIGN.md prose says "Helvetica Now 16px weight 500". The frame shows unmistakable serif, and
the token export confirms it: step `base-4` is **Davinci 16px w500 lh1.5**. Built as serif.

### 6. Imagery: classical oil painting or nothing
Full-bleed, or a ~200px circular crop. No border, no radius, no overlay. In the hero the canvas
runs along the floor and **cuts across the base of the wordmark** — the same relationship the
reference's moss has to "Structured".

### 7. Header is two elements
Circled monogram top-left, one text link top-right. Not sticky. Section tabs are allowed
**below** the hero; they are not header chrome.

### 8. Secondary geometry
Hexagon (~12px, 1px stroke) for indicators. Circle for the monogram and image crops. Notched
corners for the floating card. No other shapes.

---

## Motion — SOURCED, from the user's screen recording

A 34s screen recording settled this. Frames extracted with Swift/AVFoundation. These are
observed mechanisms, no longer authored guesses.

### 9. One continuous painted world, panning vertically

Not separate paintings in panels. A single tall illustrated landscape runs full-bleed behind
a whole section — pyramids and cloud at the top, down past temple ruins, a winding path, a
hooded statue, a waterfall, a river, flowers at the base. The camera descends through it as
you scroll. Full-bleed, no container, no radius.

**Fail if:** imagery is panelled, panned horizontally, or sits beside the content instead of
behind it.

### 10. A card pinned dead centre, its copy crossfading

The card never moves. As the world scrolls behind it, the text swaps between statements —
"Bitcoin is the gold standard store of value" → "For Bitcoin to move, it needs liquidity" →
"A yield-bearing asset integrated across DeFi". Small **corner tick marks** sit at its four
corners (angle brackets, not notched edges). Serif ~24px heading, small grotesk body.

**Fail if:** the card moves with the scroll, or the copy is static while the imagery changes.

### 11. A black room of giant type scrolling through a hairline lattice

Enormous serif letters, stacked and travelling vertically — M → MA → MAX → BT → BTC. Behind
them a **hairline diamond lattice with small hexagon nodes** at the intersections. A painted
drapery ribbon in warm peach drifts across the letters on its own path, independent of the type.

**Fail if:** the giant type is shorter than the frame (no travel), or the lattice and the
ribbon move together with it.

### 12. Nothing parked hidden

Reveals apply only to elements JS confirms are off-screen, with a failsafe.
`prefers-reduced-motion` unpins every section and returns the page to static full-bleed plates.
