# Buck Converter

A high-efficiency DC-DC step-down (buck) converter PCB designed in KiCad 8. Converts a higher DC input voltage to a lower regulated DC output, suitable for embedded systems and power supply applications.

---

## Features
- Adjustable output voltage via feedback resistor divider
- High switching efficiency (up to 92%)
- Onboard inductor, catch diode, and output capacitors
- Input and output screw terminal connectors
- LED power indicator

## Specifications

| Parameter | Value |
|-----------|-------|
| Controller IC | LM2596-ADJ |
| Input Voltage | 4.5V – 40V |
| Output Voltage | 1.25V – 35V (adjustable) |
| Max Output Current | 3A |
| Switching Frequency | ~150kHz |
| Efficiency | Up to 92% |
| PCB Layers | 2 |
| Designed With | KiCad 8 |

## Project Structure

```
├── Schematic/       # KiCad schematic (.kicad_sch, PDF)
├── PCB/             # PCB layout (.kicad_pcb, .kicad_pro)
├── Gerbers/         # Fabrication files
├── BOM/             # Bill of materials (CSV)
├── 3D/              # 3D model (.step)
└── Images/          # PCB renders and schematic screenshots
```

## How It Works

The LM2596 switches at 150kHz, driving current through an inductor. The LC output filter averages the switched waveform into steady DC. A feedback resistor divider compares the output to the IC's internal 1.23V reference to regulate the output voltage.

## Bill of Materials (Summary)

| Component | Value | Qty |
|-----------|-------|-----|
| Buck IC | LM2596-ADJ | 1 |
| Inductor | 68µH | 1 |
| Schottky Diode | 1N5822 | 1 |
| Output Capacitor | 220µF / 50V | 1 |
| Input Capacitor | 100µF / 50V | 1 |
| Trim Pot | 10kΩ | 1 |
| Screw Terminals | 2-pin | 2 |

## Fabrication

Gerber files are in `/Gerbers`, ready for JLCPCB, PCBWay, or similar.

## License

This project is licensed under the [CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN OHL-S v2)](https://ohwr.org/cern_ohl_s_v2.txt).

## Author

**Abhi90808** — [GitHub Profile](https://github.com/Abhi90808)
