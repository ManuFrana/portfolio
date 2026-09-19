---
name: Manuel Frana — Blackened Instrument Chassis
description: A personal CV page built as a blackened instrument chassis that stays dark and unadorned the whole way down, spending its one warm colour only where something is being reported.
colors:
  panel-ink: "#08090B"
  chassis-black: "#0E0E10"
  gunmetal: "#1C1F24"
  mesh: "#3A3D42"
  steel: "#5C6168"
  label-grey: "#7C838C"
  plasma-orange: "#FF8A00"
  plasma-dim: "#8A4A08"
  text-primary: "#DADDE2"
  text-secondary: "#9AA1A9"
  # plasma-adjacent scoped values: selection ink, and the two stops of the
  # engraved plate's hover fill. Never available as text or surface colours.
  selection-ink: "#120800"
  plate-hover-top: "#221A10"
  plate-hover-bottom: "#15100A"
typography:
  display:
    fontFamily: "Big Shoulders Display, system-ui, sans-serif"
    fontSize: "clamp(4.6rem, 13vw, 9rem)"
    fontWeight: 700
    lineHeight: 0.86
    letterSpacing: "0.005em"
  headline:
    fontFamily: "Big Shoulders Display, system-ui, sans-serif"
    fontSize: "clamp(1.9rem, 4.6vw, 3rem)"
    fontWeight: 700
    lineHeight: 0.95
    letterSpacing: "0.012em"
  title:
    fontFamily: "Big Shoulders Display, system-ui, sans-serif"
    fontSize: "clamp(1.25rem, 2.4vw, 1.55rem)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: "0.02em"
  figure:
    fontFamily: "Big Shoulders Display, system-ui, sans-serif"
    fontSize: "clamp(2.8rem, 6.4vw, 4.4rem)"
    fontWeight: 700
    lineHeight: 0.88
    letterSpacing: "0.01em"
  body:
    fontFamily: "Chivo, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: "normal"
  body-dense:
    fontFamily: "Chivo, system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: "normal"
  contact-value:
    fontFamily: "Chivo, system-ui, sans-serif"
    fontSize: "clamp(1rem, 2vw, 1.2rem)"
    fontWeight: 500
    lineHeight: 1.65
    letterSpacing: "normal"
  label:
    fontFamily: "Azeret Mono, ui-monospace, monospace"
    fontSize: "12px"
    fontWeight: 500
    lineHeight: 1.65
    letterSpacing: "0.2em"
  role-line:
    fontFamily: "Azeret Mono, ui-monospace, monospace"
    fontSize: "clamp(12px, 1.5vw, 15px)"
    fontWeight: 500
    lineHeight: 1.65
    letterSpacing: "0.26em"
  code:
    fontFamily: "Azeret Mono, ui-monospace, monospace"
    fontSize: "12.5px"
    fontWeight: 400
    lineHeight: 1.75
    letterSpacing: "normal"
rounded:
  none: "0"
  screw: "50%"
spacing:
  gutter: "clamp(20px, 5vw, 64px)"
  section: "clamp(64px, 9vw, 136px)"
  panel: "clamp(20px, 2.6vw, 30px)"
  row: "17px"
  stack: "14px"
components:
  plate:
    backgroundColor: "linear-gradient(180deg,#1A1D22 0%,#131519 100%)"
    textColor: "{colors.text-primary}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "17px 26px"
  plate-hover:
    backgroundColor: "linear-gradient(180deg,#221A10 0%,#15100A 100%)"
    textColor: "{colors.plasma-orange}"
  plate-sm:
    backgroundColor: "linear-gradient(180deg,#1A1D22 0%,#131519 100%)"
    textColor: "{colors.text-primary}"
    padding: "12px 20px"
  panel:
    backgroundColor: "{colors.chassis-black}"
    textColor: "{colors.text-secondary}"
    rounded: "{rounded.none}"
    padding: "{spacing.panel}"
  note:
    backgroundColor: "rgba(255,138,0,.05)"
    textColor: "{colors.text-secondary}"
    rounded: "{rounded.none}"
    padding: "15px 17px"
  rail:
    backgroundColor: "rgba(14,14,16,.95)"
    textColor: "{colors.text-secondary}"
    rounded: "{rounded.none}"
    padding: "11px {spacing.gutter}"
  code-well:
    backgroundColor: "{colors.code-well}"
    textColor: "{colors.code-text}"
    typography: "{typography.code}"
    rounded: "{rounded.none}"
    padding: "16px 14px"
---

# Design System: Manuel Frana — Blackened Instrument Chassis

## Overview

**Creative North Star: "The Blackened Instrument Chassis"**

This is a machined, powered-down laboratory instrument standing in a dark room. Everything the
visitor touches is chassis furniture: hairline-bordered gunmetal panels, engraved plates with
corner screws, a fixed rail along the bottom edge. The page is quiet from top to bottom and
spends its one warm colour only where something is actually being reported — two figures, a
status box, a keyword in a code listing, and the element under the cursor. Nothing glows,
nothing blurs, nothing is rounded except a 3px screw head.

The world descends from a nixie-tube laboratory counter, but **the tube itself is deliberately
gone**. The user removed it after the build ("replace the tubes with simple numbers, I do not
like the tubes at all"). What survives is the chassis the tube was mounted in: the palette, the
engraved-plate components, the caps lettering, and the single emitted-signal colour. The two
standalone figures are now plain Big Shoulders numerals in plasma orange. A future surface must
not reinstate tube glass, anode mesh, segment stripes or ignite animations; the absence is the
design, not an omission.

Density is low and the rhythm is vertical: a full-viewport hero, then sections separated only by
1px gunmetal rules, no decorative dividers and no card shadows. Depth comes entirely from tonal
layering — panel ink under chassis black under gunmetal borders — and never from elevation.

**Key Characteristics:**
- Near-black ground with hairline gunmetal separation, no shadows anywhere
- One warm signal colour, used on well under 5% of any screen
- Big Shoulders caps for lettering, Chivo for prose, Azeret Mono for every label
- Square corners everywhere; the only curve is a 3px screw dot
- The hero owns the full first viewport at every width

## Colors

A near-monochrome greyscale machined from black up to bone white, cut once by a single emitted
orange.

### Primary
- **Plasma Orange** (`{colors.plasma-orange}`): The only warm colour on the page and the only
  signal. It appears on the two standalone project figures, the STATUS box heading and border
  tint, keyword tokens inside code listings, the text selection background, the focus ring, and
  every hover/focus state on plates and contact rows. Nothing else.
- **Plasma Dim** (`{colors.plasma-dim}`): The burnt border variant. Used only as the 1px border
  of the STATUS note, so the note reads as warm without becoming a coloured block.

### Neutral
- **Panel Ink** (`{colors.panel-ink}`): The page ground and the browser theme colour. The
  darkest surface in the system; everything sits on it.
- **Chassis Black** (`{colors.chassis-black}`): One step up from ground. The fill of gunmetal
  panels, figure frames, and the translucent bottom rail.
- **Gunmetal** (`{colors.gunmetal}`): The hairline. Every section rule, panel border, table
  row divider, figure border and figcaption separator is 1px of this and nothing else.
- **Mesh** (`{colors.mesh}`): Slightly brighter machined edge, reserved for the engraved plate
  border and the scrollbar thumb.
- **Steel** (`{colors.steel}`): Structural metal only — the 3px corner screw dots on plates,
  the 11px dash rules that stand in for list bullets, the scrollbar thumb on hover.
- **Label Grey** (`{colors.label-grey}`): The text colour for every engraved caps label:
  `.lbl`, spec-row terms, figcaptions, job dates, code headers, project stack lines, plate
  icons at rest.
- **Text Primary** (`{colors.text-primary}`): Headings, the name, plate wording, contact
  values, emphasised words inside prose.
- **Text Secondary** (`{colors.text-secondary}`): All running prose, list items, spec
  definitions, the hero role line, the rail identity.
- **Code Well / Code Text / Code Comment** (`{colors.code-well}`, `{colors.code-text}`,
  `{colors.code-comment}`): The listing surface sits one shade off the ground; its body is
  slightly cooler than page text and its comments recede.

### Named Rules

**The Signal Rule.** Plasma orange is signal, never decoration. It is allowed on exactly five
things: the standalone `.fig-n` figures, the STATUS note, code keyword tokens, interactive
hover/focus states, and the browser selection/focus ring. A new orange surface must be
reporting something, or it is wrong.

**The Steel-Is-Not-Text Rule.** `{colors.steel}` draws rules, borders and screw dots and never
carries type. Engraved label text uses `{colors.label-grey}`, which clears 4.5:1 on both the
panel-ink ground and the code well. These two tokens were collapsed once during the build and
produced a real contrast failure; do not re-collapse them.

**The Hairline Rule.** Every separation in the system is 1px of gunmetal. There is no second
border weight, no double rule, no dashed or dotted divider.

## Typography

**Display Font:** Big Shoulders Display (with system-ui, sans-serif)
**Body Font:** Chivo (with system-ui, sans-serif)
**Label/Mono Font:** Azeret Mono (with ui-monospace, monospace)

**Character:** Big Shoulders is condensed industrial signage — it reads as lettering stamped on
a chassis, not as a headline typeface. Chivo underneath it is plain, slightly mechanical grotesk
prose that never competes. Azeret Mono handles everything that is a label, a date, a stack list
or a line of code, always in tracked caps when it is a label.

### Hierarchy
- **Display** (700, `{typography.display.fontSize}`, 0.86 line-height, uppercase): The name in
  the hero, split across two lines. One instance per page.
- **Headline** (700, `{typography.headline.fontSize}`, 0.95, uppercase): Section headings.
- **Title** (700, `{typography.title.fontSize}`, 1.05, uppercase): Panel headings and job
  titles.
- **Figure** (700, `{typography.figure.fontSize}`, 0.88, plasma orange): The two standalone
  numerals beside Catox. Never used for a number that lives inside a sentence.
- **Body** (400, 16px, 1.65, max 66ch): Running prose in text-secondary, with emphasised spans
  lifted to text-primary at weight 600. Dense variants drop to 15–15.5px inside panels, spec
  rows and job bullets (bullets cap at 74ch).
- **Label** (500, 12px, 0.2em tracking, uppercase): Engraved caps labels. Tracking varies by
  role between 0.1em and 0.2em and tightens as the string lengthens.
- **Role line** (500, clamp 12–15px, 0.26em tracking, uppercase): One instance — the hero role
  under the name. The widest tracking in the system.

### Named Rules

**The Figures-In-Sentences Rule.** Numbers belong inside prose. Only two figures on the whole
page stand alone, and both sit in the last third beside the project that earned them. The
system refuses a stat wall.

**The Tracked-Caps-Are-Labels Rule.** Uppercase with letter-spacing is reserved for mono labels
and the single hero role line. No paragraph, list item or definition is ever uppercased.

## Layout

A single centred column: `max-width: 1140px` with `width: 100%` and a fluid gutter
(`{spacing.gutter}`). The `width: 100%` is load-bearing — without it, `margin: 0 auto` inside
the column-flex hero defeats `stretch` and shrink-wraps the hero to its content.

The hero is `min-height: 100svh` and vertically centred, so it owns the full first viewport at
every width. It carries the name, a hairline, the role line and the CV plate, and nothing else.

Sections are separated by a 1px gunmetal top border with `{spacing.section}` of vertical
padding. Two-column areas use `minmax(0, 1.15fr) minmax(0, 1fr)` for prose-plus-panels and a
balanced `minmax(0, 1fr) minmax(0, 1fr)` for project grids. Spec rows are a fixed 178px term
column against a flexible definition column.

Responsive: at 860px every grid collapses to a single column and spec rows stack term over
definition. At 560px the rail drops its role suffix and tightens.

**The Minmax-Zero Rule.** Every collapsed grid template uses `minmax(0, 1fr)`, never bare
`1fr`. A bare `1fr` resolves its minimum to `min-content`, and the `<pre>` code listing then
blows the column out of the viewport.

## Elevation & Depth

**There are no shadows in this system — zero `box-shadow` declarations ship.** Depth is purely
tonal: panel ink for the ground, chassis black for panels and wells, gunmetal hairlines to
describe the edge where one plane meets the next. The engraved plate is the only surface with
any modelling, and it gets it from a 2-stop vertical gradient (`#1A1D22` → `#131519`) plus its
mesh border and two steel screw dots — a machined face catching room light, not an object
floating above the page.

**The No-Lift Rule.** Nothing in this world casts, glows or lifts. If a surface needs to read
as separate, change its tone and give it a gunmetal hairline.

### Motion
One authored motion exists: the fixed chassis rail translates up from `translateY(102%)` to rest
over 0.32s `cubic-bezier(.16, 1, .3, 1)`, triggered once the hero scrolls out of view. Everything
else is a 0.18–0.2s ease colour/border transition on hover and focus. `prefers-reduced-motion`
collapses all transitions to 0.01ms.

## Shapes

Square. Every container, plate, panel, note, figure and code well has zero radius. The single
curved form in the system is the 3px `50%` screw dot mounted at each end of an engraved plate.

Borders are always 1px and always gunmetal, except the plate (mesh) and the STATUS note
(plasma-dim). Bullet lists use no disc: each item is offset 24px and draws an 11px × 1px steel
dash with `::before`, set at `top: .68em`.

Icons are inline stroked SVG on a 24×24 viewBox at `stroke-width` 1.7–1.9 with square linecaps,
sized 14–20px, inheriting `currentColor`. There are no icon fonts and no glyph characters.

## Components

### Buttons — the Engraved Plate
- **Shape:** Square (0 radius), 1px mesh border, with a 3px steel screw dot inset 9px from each
  end.
- **Primary:** Vertical gunmetal gradient face, text-primary mono caps at 13px / 0.18em, padding
  `17px 26px`, an inline download or arrow SVG in label grey. A `.plate-sm` variant drops to
  `12px 20px` / 12px for the rail and skip link.
- **Hover / Focus:** Border and text and icon all shift to plasma orange; the face gradient
  warms to `#221A10` → `#15100A` over 0.2s. Focus-visible gets the global 2px plasma outline at
  3px offset in addition.

### Cards / Containers — the Gunmetal Panel
- **Corner Style:** Square (0 radius).
- **Background:** Chassis black on the panel-ink ground.
- **Shadow Strategy:** None; see Elevation & Depth.
- **Border:** 1px gunmetal.
- **Internal Padding:** `{spacing.panel}`. Stacked panels sit 14px apart. A panel holds a Title
  heading and one 15px paragraph.

### Navigation — the Chassis Rail
Fixed to the bottom edge, full width, 95%-opaque chassis black with a 1px gunmetal top border,
hidden below the fold until the hero leaves the viewport. It carries the identity in 12px mono
(name in text-primary, role suffix in text-secondary) on the left and a small CV plate on the
right. Below 560px the role suffix is dropped and the padding tightens to 9px. It is a
persistent CV handle, not a link menu — this page has no nav links.

### Data Rows — the Specification List
A definition list on a 178px / flexible grid, each row 17px of vertical padding with a 1px
gunmetal bottom border. Terms are 12px mono caps in label grey with 4px of optical top padding;
definitions are 15px text-secondary. Collapses to stacked term-over-definition at 860px.

### Code Listing
A bordered well one shade off the ground, with a mono caps header strip (label grey, 1px
gunmetal underline, `overflow-wrap: anywhere` so long paths do not overflow) above a
horizontally scrollable `<pre>`. Only two token classes exist: comments in code-comment and
keywords in plasma orange.

### Status Note
The one warm container: `plasma-dim` 1px border over a 5%-alpha orange wash, with a block mono
caps heading in plasma orange and 14.5px secondary body capped at 64ch. Reserved for stating
what is and is not true about a project.

### Contact Row
A full-width link row, 20px vertical padding, 1px gunmetal bottom border: a mono caps label
stacked over a 1rem–1.2rem text-primary value on the left, a 20px arrow icon on the right. On
hover or focus the value goes plasma orange and the icon goes orange and nudges 2px right, 2px
up.

### Figure Pair
Two stacked units in a flex row: a large Big Shoulders numeral in plasma orange over a 12px mono
caps label. The only standalone numerals on the page.

## Do's and Don'ts

### Do:
- **Do** keep plasma orange to signal only — figures, STATUS, code keywords, hover/focus and
  browser selection.
- **Do** draw every separation as a 1px gunmetal hairline.
- **Do** use `{colors.label-grey}` for engraved label text and `{colors.steel}` only for rules,
  borders and screw dots.
- **Do** keep `width: 100%` on the centred wrapper; the column-flex hero shrink-wraps without it.
- **Do** write collapsed grid templates as `minmax(0, 1fr)`.
- **Do** keep the hero at `min-height: 100svh` carrying name, role and the CV plate only.
- **Do** theme browser surfaces — selection, focus ring and scrollbar — from the palette.
- **Do** draw list bullets as 11px steel dash rules with `::before`.
- **Do** put figures inside sentences; only project-earned figures may stand alone.

### Don't:
- **Don't** reinstate the nixie tube, its glass, its anode mesh, its segment stripes or its
  ignite animation. The user removed it; plain numerals are its replacement.
- **Don't** add a kicker or eyebrow line beside a heading, and don't number sections or figures
  `01 / 02 / 03`. Both were removed on craft grounds.
- **Don't** add a slogan or tagline anywhere on the page.
- **Don't** add a box-shadow, a glow, a backdrop blur or a border radius above 0 (the 3px screw
  dot excepted).
- **Don't** uppercase running prose; tracked caps belong to mono labels and the single hero role
  line.
- **Don't** introduce a second accent colour or a second border weight.
- **Don't** build a stat wall of standalone numbers.
