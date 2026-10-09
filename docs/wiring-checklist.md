# Wiring checklist (secondary side)

Tick while comparing to `IMG_20221205_163654.jpg` and the apparatus list.

## Power entry

- [ ] Transformer secondary only on the breadboard rails (no primary wiring on the board)
- [ ] Secondary leads firmly inserted / screwed

## Rectifier

- [ ] Four diodes form a closed bridge
- [ ] AC nodes identified
- [ ] DC + and − identified before the capacitor

## Filter

- [ ] Capacitor across DC +/−
- [ ] Electrolytic: stripe/minus to GND if used
- [ ] Value documented (PDF says 470 nF — verify lab guidance)

## Regulator

- [ ] 7805 IN ← filtered +
- [ ] 7805 GND ← common
- [ ] 7805 OUT → load rail
- [ ] Optional input/output ceramics if your lab requires them

## Load

- [ ] 1 kΩ across OUT and GND
- [ ] LED path oriented correctly
- [ ] DMM probes ready across the load for the acceptance reading
