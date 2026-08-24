# CircuitAnalysis — 5 V DC Supply Lab

Hardware lab archive for a **regulated 5 volt DC power supply**: write-up PDF, board photos, and short videos of the live circuit. **No software build.**

[rohaan2802](https://github.com/rohaan2802)

---

## Table of contents

1. [What this lab is](#what-this-lab-is)
2. [Typical 5 V DC supply stages](#typical-5-v-dc-supply-stages)
3. [Files](#files)
4. [How to use the archive](#how-to-use-the-archive)
5. [Safety](#safety)

---

## What this lab is

Evidence package for a basic electronics / circuit-analysis experiment: build a **mains-derived (or adapter-fed) 5 V** rail, measure it, and document construction. The PDF is the graded write-up (theory, schematic, readings, observations). Photos/videos are the physical proof.

Dated media in the tree: **5–7 Dec 2022** (`IMG_20221205_*`, `video_20221205_*`, WhatsApp image `WA0006`).

---

## Typical 5 V DC supply stages

Use this as the checklist while reading `5 VOLT DC SUPPLY.pdf` (match names to *your* schematic):

| Stage | Role |
|-------|------|
| Transformer (if used) | Step down AC; isolation |
| Rectifier | Bridge diodes → pulsating DC |
| Filter | Reservoir capacitor(s); reduce ripple |
| Regulator | e.g. **7805** (or similar) → ~5 V DC |
| Load / LED | Demonstrate a stable rail |
| Metering | DMM no-load vs loaded; optional scope ripple |

Your PDF may use a wall wart instead of a lab transformer — follow the document, not this table, if they differ.

---

## Files

```text
CircuitAnalysis/
├── 5 VOLT DC SUPPLY.pdf
├── IMG-20221207-WA0006.jpeg
├── IMG_20221205_163654.jpg
├── video_20221205_163544.mp4
└── video_20221205_163700.mp4
```

(Exact names from `TREE.txt`.)

---

## How to use the archive

1. Read the PDF for schematic, part values, and expected voltages.  
2. Compare photos to your breadboard/PCB (regulator orientation, cap polarity, heatsink).  
3. Watch the MP4s for power-on / measurement moments.  

Viewers: any PDF reader, image viewer, and video player.

---

## Safety

Documentation only. If you rebuild: correct transformer VA, **fuse**, polarized capacitors, regulator dropout/headroom, isolated meter practice. Mains-side work belongs in a supervised lab.

**Extend:** export a clean schematic (KiCad), BOM with tolerances, no-load/loaded table in Markdown, scope screenshot of ripple.

---

## Author

Electronics lab coursework · [rohaan2802](https://github.com/rohaan2802)
