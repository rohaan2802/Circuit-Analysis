# Troubleshooting — 5 V DC supply lab

Power down before rewiring. Mains work only under supervision.

| Symptom | Likely cause | What to check |
|---------|--------------|---------------|
| 0 V on load | No AC secondary / open fuse / wrong DMM range | Transformer secondary AC with DMM AC mode; fuse; probes |
| ~0.7–2 V DC | Incomplete bridge or floating ground | Diode orientations; common GND to 7805 pin 2 |
| Pulsating / unstable reading | Missing or wrong filter | Cap across DC rails; polarity; value realistically sized |
| ~12–15 V on “5 V” node | Regulator bypassed or wrong pinout | 7805 pins: IN / GND / OUT; output taken from pin 3 |
| ~3–4 V out | Dropout / Vin too low / overloaded | Measure Vin into 7805; reduce load; verify secondary |
| 7805 very hot | High (Vin−5)×I | Heat sink; lower Vin or load current |
| LED dark but 5 V OK | LED polarity / series resistor | Flip LED; confirm series path |
| LED bright then dies | No current limit | Add proper series resistance |
| Output >5.2 V continuously | Wrong IC / shorted regulator | Part marking; replace 7805 |
| Bridge diodes hot | Reverse assembly / short | Recheck bridge; look for solder bridges |

## Quick measurement map

1. Transformer secondary: AC volts  
2. Bridge output (pre-cap): pulsating DC  
3. After filter (7805 input): smoother DC (often ~12–15 V region)  
4. Across 1 kΩ load: ~5.0 V (archive: **5.06 V**)
