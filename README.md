# texas-blinky

A minimal single-transistor LED blinker circuit, designed in KiCad 9.0. My first PCB project.

## How it works

A relaxation oscillator built around a CR2032 coin cell. R1 slowly charges C1 through the base of Q1. Once C1 charges enough to forward-bias Q1, the transistor switches on and D1 flashes. C1 then discharges rapidly through the transistor, which cuts off again — and the cycle repeats.

## Bill of materials

| Ref | Value | Description | Footprint |
|-----|-------|-------------|-----------|
| BT1 | CR2032 | Coin cell battery | Keystone 3034 holder |
| C1 | 47µF | Electrolytic capacitor | Radial, 6.3mm dia, 2.5mm pitch |
| D1 | LED (red) | 5mm through-hole LED | LED_D5.0mm |
| Q1 | MMBT3904 | NPN BJT | TO-92 inline |
| R1 | 1MΩ | Timing / base charge resistor | Axial, DIN0207, 7.62mm pitch |
| R2 | 100Ω | LED current-limiting resistor | Axial, DIN0207, 7.62mm pitch |

## Files

| File | Description |
|------|-------------|
| `texas-blinky.kicad_pro` | KiCad project file |
| `texas-blinky.kicad_sch` | Schematic |
| `texas-blinky.kicad_pcb` | PCB layout |
| `texas-blinky.kicad_prl` | Project local settings (layer visibility, etc.) |
