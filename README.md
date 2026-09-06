# Circuit Analysis — 5 V DC Supply Lab

Hardware lab archive for a **regulated 5 volt DC power supply**: a 20-slide PowerPoint write-up exported as PDF, breadboard photos, and two short videos of the live circuit. **No software build.**

**Extracted** below from `5 VOLT DC SUPPLY.pdf` (pypdf). Filenames and media dates are from `TREE.txt`. Where the slides contradict themselves, both wordings are quoted.

**Author:** Mohammad Rohaan · **Roll:** 22I-2327 · **GitHub:** [rohaan2802](https://github.com/rohaan2802)

---

<img width="3840" height="2160" alt="IMG-20221207-WA0006" src="https://github.com/user-attachments/assets/6d1d689b-7253-4dcc-96c1-b2312f20bd1a" />


## Table of contents

1. [What this archive is](#what-this-archive-is)
2. [PDF metadata](#pdf-metadata)
3. [Objectives and introduction (extracted)](#objectives-and-introduction-extracted)
4. [Apparatus list (extracted)](#apparatus-list-extracted)
5. [Stage-by-stage theory (extracted)](#stage-by-stage-theory-extracted)
6. [Conversion procedure (extracted)](#conversion-procedure-extracted)
7. [Measured result (extracted)](#measured-result-extracted)
8. [Inconsistencies in the write-up](#inconsistencies-in-the-write-up)
9. [Photo and video files](#photo-and-video-files)
10. [How to use the archive](#how-to-use-the-archive)
11. [Safety](#safety)
12. [Limitations](#limitations)
13. [Author](#author)

---

## What this archive is

Course **final project presentation** for a breadboard 5 V regulated supply: 220/230 V AC in, transformer, rectifier, capacitor filter, **LM7805**, LED + 1 kΩ load. Group submission to **Engr. Nimra Fatima**.

| Member | Roll |
|--------|------|
| Mohammad Rohaan | 22I-2327 |
| Taha Sajid Awan | 22I-2302 |
| Talha Tariq | 22I-2309 |

Media timestamps: **5 December 2022** (`IMG_20221205_*`, `video_20221205_*`) and **7 December 2022** (WhatsApp image + PDF creation date).

---

## PDF metadata

| Field | Value |
|-------|--------|
| Title | 5 VOLT DC SUPPLY |
| Author | Mohammad Rohaan |
| Producer / Creator | Microsoft PowerPoint LTSC |
| Creation / mod date | 2022-12-07 03:04:29 +05:00 |
| Pages | 20 |

Slide titles with little or no extractable text (image-only): **APPARATUS IMAGES** (p. 6–7), **PROTEUS IMAGE** (p. 18), **HARDWARE IMAGE** (p. 19). Those pages are photographs/schematic captures inside the PDF, not separate repo files.

---

## Objectives and introduction (extracted)

Page 3: **OBJECTIVES** — designing and analysing a logical circuit; apparatus; theory.

Page 1 title slide: **5 VOLT DC SUPPLY — FINAL PROJECT PRESENTATION**.

Page 4 introduction (quoted in substance):

- 5 V DC supplies are described as common; a 5 V DC output is obtained from a **220 VAC** input using transformers, diodes, and transistors.
- Two types named: **5 V regulated** and **5 V unregulated**.
- Power electronics framed as solid-state conversion; this practical is **AC to DC (rectification)**.
- Goal: construct a **5-volt regulated** supply that delivers regulated 5 V to a load.

---

## Apparatus list (extracted)

From page 5 **APPARATUS**:

| Item | Specification in the PDF |
|------|--------------------------|
| Mains | Power supply **220 Volt** |
| Prototype | **Bread board** (later: Veroboard was recommended; breadboard used) |
| Transformer | Step-down **12 Volt** (page 8 also says a **15 V / 2 A** secondary was chosen) |
| Rectifier | **Bridge rectifier (4 diodes)** |
| Diodes named later | **1N4007**, 1 A, peak reverse voltage **50 V** (page 9) |
| Filter | Capacitor **470 nF** (heading on page 10: Capacitive Filter 470 nF) |
| Regulator | **LM7805** (also written IC7805 / voltage regulator IC) |
| Load | **1 kΩ** |
| Indicator | Small **LED** |

Page 11 LM7805 characteristics as written:

- Output **4.8 V – 5.2 V**
- Input **7 V – 35 V** (page 17 also gives **7.2 V – 35 V**)
- Current **1 A**

Page 12: breadboard for temporary circuits vs Veroboard for soldering; **breadboard used**.

---

## Stage-by-stage theory (extracted)

### Transformer (page 8)

Steps **220 V** mains down and isolates the output. Current rating depends on the load. The same slide states a **15 volt secondary, 2 A** transformer was chosen, while the apparatus list and conclusion say **12 V**.

### Bridge rectifier (page 9)

Four **1N4007** diodes soldered as a bridge; 1 A; PIV 50 V. Converts AC to DC.

### Capacitive filter (page 10)

Rectified DC is not constant (waveform crosses zero). Capacitor “fills the troughs”, removes ripples, smooths for the regulator.

### LM7805 (page 11)

Takes smoothed DC and holds a constant output despite input fluctuation.

### Load and LED (page 13)

1 kΩ as a minimum/base load; LED discussed in the context of needing enough load for the supply to behave.

---

## Conversion procedure (extracted)

Pages 14–17: **“4 Steps to Convert 230V AC to 5V DC”**.

1. **Step down.** 230 V AC → **12 V AC** RMS via step-down transformer. Peak ≈ 12 × √2 ≈ **17 V**.
2. **AC to DC.** 17 V AC peak must become DC before 5 V regulation. The slide names half-wave, full-wave, and bridge rectifiers, then says **“We are using a full wave rectifier… Full wave rectifier consists of 2 diodes”** (this conflicts with the four-diode bridge on the apparatus slides). Pulsating DC; ~0.7 V diode drop mentioned.
3. **Filter.** Pulsating DC smoothed with inductor, capacitor, or RC filter; **capacitor filter** used. Charge on the peak, discharge toward zero → “pure DC” (idealised wording).
4. **Regulate.** Smoothed ~12–15 V DC into **5 V** with **IC7805** (“78” = positive regulator series, “05” = 5 V out). Heat beyond ~7.2 V dropout/headroom discussed; **heat sink** mentioned for thermal protection.

Page 18 is labelled **PROTEUS IMAGE** (simulation screenshot in the PDF). Page 19 is **HARDWARE IMAGE** (physical build).

---

## Measured result (extracted)

Page 20 **RESULTS**:

> When checking with the DMM (Digital Multimeter), the voltage across the load resistance is almost near the 5 volt but the DMM shows **5.06 V**.

**Conclusion** (same page): transformer 230 V → 12 V AC; bridge rectifier to DC; capacitors remove ripples; **IC LM7805** regulates to **+5 V**.

---

## Inconsistencies in the write-up

These are **in the PDF itself**, not guesses:

| Topic | One slide says | Another slide says |
|-------|----------------|--------------------|
| Mains | 220 V | 230 V |
| Secondary | 12 V | 15 V / 2 A chosen |
| Rectifier | Bridge, **4** diodes (1N4007) | Full-wave, **2** diodes |
| Filter value | **470 nF** | Typical teaching labs use hundreds of **µF**; the PDF text is 470 nF |
| 7805 input min | 7 V | 7.2 V |

When rebuilding, prefer the **apparatus list + results** (bridge + LM7805 + 5.06 V on the 1 kΩ load) and treat the “2 diode full-wave” paragraph as reused textbook text.

**Not extracted** (image-only slides): exact Proteus schematic netlist, measured ripple, transformer VA marking on the photo, LED series resistor if separate from 1 kΩ.

---

## Photo and video files

From `TREE.txt` (exact names):

```text
CircuitAnalysis/
├── 5 VOLT DC SUPPLY.pdf
├── IMG-20221207-WA0006.jpeg
├── IMG_20221205_163654.jpg
├── video_20221205_163544.mp4
└── video_20221205_163700.mp4
```

| File | Role |
|------|------|
| PDF | Graded presentation (theory, apparatus, procedure, 5.06 V result) |
| `IMG_20221205_163654.jpg` | Hardware photo, 5 Dec 2022 ~16:36 |
| `video_20221205_163544.mp4` | Live capture ~16:35 |
| `video_20221205_163700.mp4` | Live capture ~16:37 |
| `IMG-20221207-WA0006.jpeg` | Additional photo via WhatsApp, 7 Dec 2022 |

No KiCad/Eagle source, no BOM CSV, no oscilloscope CSV in this repo.

---

## How to use the archive

1. Read `5 VOLT DC SUPPLY.pdf` (PowerPoint-style slides; zoom on Proteus/hardware pages).
2. Compare breadboard photos to the apparatus list (LM7805 orientation, cap polarity, transformer secondary, LED).
3. Watch the two MP4s for power-on / DMM moments.
4. Viewers: any PDF reader, image viewer, and video player. Nothing to compile.

---

## Safety

Documentation only. If you rebuild in a supervised lab:

- Isolate mains with a **properly rated** step-down transformer; fuse the primary.
- Respect electrolytic **polarity** (if a large reservoir cap is used despite the “470 nF” wording).
- Give the 7805 **headroom** (input several volts above 5 V) and a **heat sink** if Vin is high.
- 1N4007 PIV in the write-up is listed as 50 V — 1N4007 is commonly 1000 V PIV; use the datasheet for the part you have.
- Do not work on the 220/230 V side without supervision.

---

## Limitations

- Image-only slides do not yield a typed netlist or Proteus `.pdsprj` file.
- Theory slides mix 2-diode and 4-diode rectifiers and 12 V vs 15 V.
- No tabulated no-load vs loaded measurements beyond the single **5.06 V** DMM reading.
- Videos/photos are unlabelled in the tree (no README in-repo originally).

**Not in this repo:** firmware, MATLAB, or PCB Gerbers.

---

## Author

**Mohammad Rohaan** · Roll **22I-2327** · Group with Taha Sajid Awan (22I-2302) and Talha Tariq (22I-2309) · [github.com/rohaan2802](https://github.com/rohaan2802)
