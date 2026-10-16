# style

The shared style of Francesco Di Maggio's sites: one family, each site with its own character.

| Site | Address | Repository |
|---|---|---|
| Personal site | [francescodimaggio.nl](https://francescodimaggio.nl/) | [francesco-di-maggio.github.io](https://github.com/francesco-di-maggio/francesco-di-maggio.github.io) |
| TSOST, with its course | [/tsost/](https://francescodimaggio.nl/tsost/) | [tsost](https://github.com/francesco-di-maggio/tsost) |
| TESI | [/tesi/](https://francescodimaggio.nl/tesi/) | [tesi](https://github.com/francesco-di-maggio/tesi) |
| mqtt-max | [/mqtt-max/](https://francescodimaggio.nl/mqtt-max/) | [mqtt-max](https://github.com/francesco-di-maggio/mqtt-max) |

Style guide: [francescodimaggio.nl/style](https://francescodimaggio.nl/style/)

## Use

Load the tokens, then the base, then the site's own styles:

```html
<link rel="stylesheet" href="https://francescodimaggio.nl/style/v1/tokens.css">
<link rel="stylesheet" href="https://francescodimaggio.nl/style/v1/base.css">
```

| File | Holds |
|---|---|
| `v1/tokens.css` | Colours, fonts, radii, light and dark |
| `v1/base.css` | Page, header, mark, nav, type, panels, lists, facts, prose, code, tables, search, controls, footer |

The mqtt-max Remote is the exception: it stays one self-contained file, so it can be opened locally or shipped with the Max package. It follows the same tokens by hand.

A change that keeps every site intact goes into `v1`. A change that would break a site goes into `v2`, and each site moves when ready.

## Shared

- **Marks.** One glyph per site, in the header and the favicon: personal site dot, TSOST ripple, TESI four modules, mqtt-max line. The orange part breathes in the header (3 s, scale 1.2, opacity 0.4) and stays still with reduced motion. Marks are capitals by CSS; the source keeps each name's own spelling.
- **Parts.** A part with its own structure keeps the site's mark, adds its name and swaps the nav row for its own tabs: TSOST / COURSE, MQTT-MAX / REMOTE. Where the header is too narrow, the glyph alone leads back.
- **Nav and icons.** The nav lists sections. Views of the whole (timeline, graph) and tools (search, theme) are icons in the header.
- **Accent.** Orange only for what is on: current, connected, now.
- **Filled.** A filled tile (`a.panel.primary`: label, title, caption, →) only for the one main thing to do on a page: open the Remote, download a tool. Reading pages have none.
- **Lists.** A row is a bold title with up to two grey lines, and on the right a date, or → when the date is the section label. The whole row is one link. Every list has a label above it.
- **Item pages.** Title, a one-line lead (the item's summary, also shown under it in lists), facts, then the text. Previous and next at the foot, as the pager.
- **Dates.** Open ranges `2024–present` with the accent dot in rows, closed `2022–2024`; in facts panels `2024-06 – present`.
- **Tab titles.** A home is its name; a page is `Page · Site`; a part's page is `Page · Part · Site`.
- **Footer.** `© year Francesco Di Maggio` on the left, linking to the personal site; email, GitHub and LinkedIn on the right.
- **Share images.** 1200×630, dark: the mark top left, a 96 px headline, one dim mono line.
- **Text.** Lean and factual. Short declarative sentences, exact values, one fact in one place.
- **Names.** Each name keeps its real spelling in text: TSOST and TESI (acronyms), modulo and mqtt-max (package names). Capitals come from the label style (marks, nav, labels). In tabs, a tool's name is written as its header shows it: MQTT-MAX, and MODULO if it gets its own site.
- **Full stops.** Sentences end with one: leads, summaries, captions, hints. Fragments do not: metadata lines (authors, venue · type, date · focus), labels, titles.
- **Grey.** `--dim` is #6d6d6a on light, #828288 on dark (WCAG AA).

## Licence

MIT
