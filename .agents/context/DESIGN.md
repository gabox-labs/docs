---
name: Gabox docs
description: Mintlify documentation site for Gabox, sharing the app's near-black room and electric lime signal.
colors:
  bg: "#0C0E0C"
  primary: "#C7F43A"
  primary-light: "#DBFF6B"
  primary-dark: "#95C000"
  lime-ink: "#15170F"
  rarity-common: "oklch(0.72 0.008 150)"
  rarity-rare: "oklch(0.7 0.15 250)"
  rarity-epic: "oklch(0.85 0.16 90)"
  rarity-mythic: "oklch(0.905 0.205 123)"
typography:
  heading:
    fontFamily: "Sora, ui-sans-serif, system-ui, sans-serif"
    fontWeight: 600
  body:
    fontFamily: "Inter, ui-sans-serif, system-ui, sans-serif"
    fontWeight: 400
    fontFeature: "tnum for every table"
---

# Design system: Gabox docs

## What Mintlify controls and what we control

Mintlify owns the layout, navigation, search, and components. We control:

- `docs.json`: theme `mint`, dark mode only, primary lime `#C7F43A`, Sora for headings and Inter
  for body. These match `gabox-app/docs/DESIGN.md`.
- `style.css`: small overrides only. Tabular figures in tables, transparent mermaid backgrounds,
  the ticket strip colours. Nothing that fights the theme.
- Page content: headings, tables, callouts, Steps, Cards, mermaid diagrams, inline SVG.

## Colour

Restrained. The room is near-black, text is near-white, and lime is the only accent. Lime marks
links, the active sidebar item, primary buttons, and at most one highlighted node per diagram (the
moment of randomness, or the prize landing in the wallet).

The rarity ramp is the one place with more colour: common grey, rare blue, epic gold, mythic lime.
It appears only in the ticket strip and in prize tables, never as decoration.

## Diagrams

Mermaid, with `classDef lime fill:#C7F43A,stroke:#95C000,color:#15170F` for the one highlighted
node. Left to right for flows, sequence diagrams for "who talks to whom", state diagrams for the
life of a draw. Labels are short noun phrases. No emoji in nodes.

## Components

- `Steps` for anything a person does in order.
- `Card` / `Columns` only on the overview page, as a table of contents.
- Callouts: `Note` for a fact, `Warning` for a downside the reader must see, `Tip` for a shortcut.
  At most two callouts per page.
- Tables for every comparison of three or more numbers.
- No nested cards, no accordions that hide the main content.

## Copy

CEFR B2. Second person. Sentence case headings. No em or en dashes. One idea per sentence.
Explain each technical term once, on first use, then use it exactly.
