---
name: metehankaradeniz.com
description: A personal site set like the back of a record sleeve, printed in two inks.
colors:
  cobalt: "#2338A8"
  cobalt-deep: "#1A2A86"
  on-cobalt: "#F6F7FF"
  on-cobalt-2: "#C9D1FF"
  press: "#0E1230"
  ink-ground: "#0A0E2A"
  ink-text: "#ECEEFA"
  ink-text-2: "#AEB5D6"
  ink-rule: "#2A3160"
  ink-link: "#AEBBFF"
  paper-ground: "#FAFAF7"
  paper-text: "#0E1230"
  paper-text-2: "#454B6E"
  paper-rule: "#CDD0DE"
typography:
  display:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(56px, 11vw, 96px)"
    fontWeight: 900
    lineHeight: 0.86
    letterSpacing: "-0.01em"
  heading:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(34px, 5vw, 56px)"
    fontWeight: 900
    lineHeight: 1
  track:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "clamp(18px, 2.2vw, 24px)"
    fontWeight: 700
  body:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.6
  small:
    fontFamily: "Archivo, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "15px"
    fontWeight: 400
rounded:
  none: "0px"
spacing:
  page-pad: "clamp(20px, 5vw, 64px)"
  section: "clamp(56px, 8vw, 104px)"
  row: "11px"
  gap: "10px"
components:
  action-primary:
    backgroundColor: "{colors.on-cobalt}"
    textColor: "{colors.cobalt}"
    rounded: "{rounded.none}"
    height: "46px"
    padding: "0 18px"
  action:
    backgroundColor: "transparent"
    textColor: "{colors.on-cobalt}"
    rounded: "{rounded.none}"
    height: "46px"
    padding: "0 18px"
  action-hover:
    backgroundColor: "{colors.press}"
    textColor: "{colors.on-cobalt}"
  track-row-hover:
    backgroundColor: "{colors.on-cobalt}"
    textColor: "{colors.cobalt}"
---

## Overview

The site is the back of a record sleeve. Who Metehan is, what he made and how to reach him are set as liner
notes: a tracklist that is also the table of contents (A1 About, A2 Crescendo, B1 Credits, B2 Contact), a
credits list for skills, education and club, and one line of fine print at the foot. It deliberately refuses
the usual portfolio template: no split hero with floating badges, no stat cards, no skill chips, no card grid.

## Colors

Two inks. **Cobalt** is printed as whole fields, never as scattered accents: the front block (name, portrait,
tracklist) and the contact block that closes the page. Between them the inner pages sit on the ground.

- The default ground is **deep ink** (`ink-ground`), the direction the owner chose. **Paper** (`paper-ground`
  with `paper-text`) is an opt-in version behind the "Paper version" toggle, remembered per browser.
- Secondary text is tinted from its ground (`on-cobalt-2`, `ink-text-2`, `paper-text-2`), never gray.
- `press` is a fixed blue-black used for hover fills in both versions.
- Every text color pair measures at least 6.3:1.

## Typography

One family, Archivo, used through its width axis: condensed (wdth 62–66) heavy caps for the name and section
headings, slightly condensed (wdth 80) bold for track titles, regular width for text. Track positions use
tabular figures. No second display face, no monospace.

## Layout

A single column with a 1120px max width and `page-pad` sides. The front block is a two-column grid (name and
actions, square portrait) above a full-width tracklist; all four tracks fit in the first viewport at 1280x800.
Inner sections stack: About (text plus a ruled facts list), Crescendo (text, source links, then real
screenshots shown open: one wide, two half-width), Credits (a two-column definition list). Below 640px
everything is one column and the portrait moves above the name at about 220px.

## Elevation & Depth

None. The page is printed matter: separation comes from hairline rules, dotted leaders and the cobalt fields,
never from shadows, blur or glass.

## Shapes

Square corners everywhere (`rounded.none`). The portrait is a square photo in its natural colors (the owner's choice;
an earlier duotone treatment was dropped).

## Components

- **Tracklist row:** position, title, dotted leader, right-aligned note; the whole row is the link. Hover and
  focus invert it (paper on cobalt), with the fill bleeding 10px past the column; rules stay on the column.
- **Action:** a bordered, square button with a drawn SVG icon. The primary action ("Email me") is filled.
- **Section heading:** track position in cobalt beside condensed caps, ruled underneath.
- **Credits row:** label (secondary text) over or beside the value (semibold), with small secondary notes.
- **Monogram:** the MK mark (the owner's own drawing: an M with a notch in its lower right corner, and a K
  whose top-left corner sits in it). It is the favicon on cobalt and sits in the top bar before the site name.
- **Motion:** two moments. On the first visit of a session a cobalt intro assembles the monogram: the M comes
  in from the left edge, the K from the right, until the K locks into the notch (about 1.1s), then the field fades
  away (320ms). A click or key skips it; it never plays under reduced motion. Then the portrait is pulled through
  the press once, top to bottom, starting with its top already printed; also off under reduced motion. Hover
  transitions are 150ms ease-out.

## Do's and Don'ts

- Do keep cobalt as whole fields; don't sprinkle it as an accent color.
- Do write headings as plain words in condensed caps; don't add labels or eyebrows above them, gradient text,
  or the "statement plus italic accent word" pattern.
- Do draw icons as SVG; don't use Unicode arrows or emoji as icons.
- Do show work (real screenshots, open by default); don't hide proof behind a toggle or use placeholder art.
- Don't add shadows, glows, glass, rounded cards, chips, or decorative loops (marquees, spinning badges).
