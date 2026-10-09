# Pinouts & orientation notes

## LM7805 (typical TO-220, flat face toward you, leads down)

```text
   ___________
  |  LM7805   |
  |___________|
    |   |   |
    1   2   3
   IN  GND OUT
```

| Pin | Name | Connects to |
|-----|------|-------------|
| 1 | INPUT | Filtered DC from bridge/capacitor (+) |
| 2 | GROUND | Circuit common / transformer secondary reference / load (−) |
| 3 | OUTPUT | +5 V to 1 kΩ load and LED path |

Always confirm silk/marking for your exact package variant.

## Bridge rectifier (four discrete diodes)

Conceptual diamond:

```text
          AC ~
           |
      D1       D2
           |
     (+)——filter——(−)
           |
      D4       D3
           |
          AC ~
```

- Two AC nodes ← transformer secondary  
- (+) → filter + and 7805 IN  
- (−) → common GND  

Wrong diode direction is the most common “almost works” failure mode.

## LED

Long lead typically anode (+) toward the +5 V side through a series resistor; cathode toward GND. Match the original breadboard photo if rebuilding identically.
