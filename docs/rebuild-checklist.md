# Rebuild checklist — 5 V regulated supply

Use this before powering a supervised lab rebuild. Prefer the apparatus list + hardware photos + **5.06 V** result when PDF slides disagree.

## Before wiring

- [ ] Lab supervisor present for any mains connection
- [ ] Transformer primary fused / correctly rated
- [ ] Secondary voltage matches the transformer you actually have (check label)
- [ ] Diodes are 1N4007 (or datasheet-verified equivalents)
- [ ] LM7805 pinout confirmed for your package (see `pinouts.md`)
- [ ] Capacitor polarity known if electrolytic is used
- [ ] Load is 1 kΩ (or documented substitute) before claiming “5 V result”

## Wiring order (recommended)

1. [ ] Build **secondary-side only** first (never leave exposed mains on the breadboard)
2. [ ] Wire bridge rectifier orientation (AC legs vs +/− DC)
3. [ ] Add filter capacitor across DC rails (observe polarity)
4. [ ] Wire LM7805: input ← filtered DC, GND common, output → load
5. [ ] Add 1 kΩ load (+ LED path as on the original board)
6. [ ] Visual check against `IMG_20221205_163654.jpg`

## Power-up

- [ ] DMM on DC volts across the load **before** claiming success
- [ ] Expect roughly **5.0 V** (archive measurement: **5.06 V**)
- [ ] If output is 0 V / wrong: power down, use `troubleshooting.md`
- [ ] Feel 7805 temperature; add heat sink if too hot for continuous duty

## Evidence to capture (optional but useful)

- [ ] Photo of full breadboard
- [ ] DMM reading photo/video
- [ ] Note Vin (pre-regulator) and Vout (load) in `measurement-log.md`
