# glimt

Placeholder site for Glimt, served with GitHub Pages.

- `index.html`: the whole page (Swedish by default, English via the toggle).
- `glimt-wordmark.svg`: the logo. Familjen Grotesk 600 outlines (Familjen, Stockholm, SIL Open Font License), tracked -14 units, the dot of the i replaced by a square the width of the stem, in the accent. The same drawing is inlined in the page; the font itself is not loaded.
- `favicon.svg`: the square dot in the accent colour.
- `fonts/`: Instrument Sans 400/500 for the voice and IBM Plex Mono 400/500 for labels and data, both self-hosted under the SIL Open Font License (`fonts/OFL.txt`, `fonts/OFL-ibm-plex-mono.txt`). No requests to Google or any other third party, no cookies.
- `tia-board.webp`: Fig. 02, the transimpedance amplifier board, rendered from the KiCad layout in `../STM/tia-board/layout` with `kicad-cli pcb render` (perspective, rotate -52,0,28, zoom 0.62, pivot 0,-1,0, high quality, transparent). For the render only, a copy of the board gets a stackup with a black solder mask and the SMA footprints get the library's Amphenol 132289 model, since the Linx footprint has none. The copper's yellow is then shifted toward the page's gold, cropped and saved as WebP.
- `.nojekyll`: serve the files as they are.

## Design system

- One unit, `--u` (14px), is the square dot of the i. Gaps and markers are multiples of it.
- One accent, `--accent`, a warm gold (a gleam, which is what "glimt" means), is used only for the square: the dot, the status marker, the tip apex in the figure.
- The dot is always present. Half a second after load it glints once: brightens, swells a little, and settles. In dark mode it also carries a tight resting glow, like a small light. A sheet of film grain sits over the page. All of it is CSS and SVG, no image files.
- The wordmark is drawn, not typeset: Familjen Grotesk outlines composed into one SVG so it renders identically everywhere. Instrument Sans for the one sentence. IBM Plex Mono, small and lowercase, for everything that is a label, number or status.
