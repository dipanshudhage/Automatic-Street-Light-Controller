# Automatic Street Light Controller (LDR & Relay)

An analog, microcontroller-free **Automatic Street Light Controller** that switches a white LED street light panel ON at dusk and OFF at dawn using an LDR voltage divider, a BC547 NPN transistor driver, and an SPDT relay[cite: 4, 5, 8, 9].

Originally built as a **December 2024 mini-project** on a perfboard, this repository includes both the physical prototype with a working demo clip and a custom PCB design with 3D renders and a `.step` model[cite: 8, 9, 10].

---

## Key Features
* **No Microcontroller Needed:** Purely analog light sensing and relay switching.
* **Adjustable Darkness Threshold:** Trimpot (`RV1`) to tune the dusk/dawn switching point[cite: 4, 9].
* **Status Indicators:**
  * **Red LED (`D2`):** Lights up during daytime / standby (`NC` contact)[cite: 4].
  * **Green LED (`D4`) + White LED Panel (`J1`):** Turns ON in darkness (`NO` contact)[cite: 4, 9].
* **Flyback Protection:** `1N4007` diode (`D1`) across the relay coil protects the `BC547` transistor (`Q1`) from coil back-EMF[cite: 4].

---

## Bill of Materials (BOM)

| Designator | Component | Value / Part | Qty |
| :--- | :--- | :--- | :---: |
| `K1` | SPDT Relay | 5V DC Relay (`JQC-3FC(T73)DC5V` / `SRD-05VDC-SL-C`)[cite: 3, 9] | 1 |
| `Q1` | NPN Transistor | `BC547`[cite: 3, 4] | 1 |
| `D1` | Flyback Diode | `1N4007`[cite: 3, 4] | 1 |
| `R5` | Photoresistor | 5mm LDR[cite: 3, 9] | 1 |
| `RV1` | Preset Trimpot | 10kΩ (`104` in prototype)[cite: 3, 4, 9] | 1 |
| `R6` | Resistor | 1kΩ[cite: 3] | 1 |
| `R3`, `R4` | Resistors | 470Ω[cite: 3, 4] | 2 |
| `D2`, `D4` | LEDs | 5mm Red (`D2`) & 5mm Green (`D4`)[cite: 3, 4, 9] | 2 |
| `J1`, `J2` | Screw Terminals | 2-Pin Connectors (`LED PANEL`, `BATTERY`)[cite: 3, 4, 6] | 2 |
| `LOAD` | White LED Panel | 10-SMD White LED Module (`SUNSINE 7126 PK-76`)[cite: 9] | 1 |

---

## Repository Structure

* `pcb-design/` — Schematic, 2D PCB layout, top/bottom 3D renders, and `Automatic-Street-Light-Controller.step`[cite: 10].
* `prototype-and-demo/` — December 2024 perfboard build photos and working demo video clip[cite: 8, 9, 10].

---

## PCB Design

### Schematic
![Schematic](pcb-design/schematic.png)[cite: 10]

### PCB Layout
![PCB Layout](pcb-design/pcb-layout.png)[cite: 10]

### 3D Renders
| Top View | Bottom View |
| :---: | :---: |
| ![3D Top View](pcb-design/3d-top.png)[cite: 10] | ![3D Bottom View](pcb-design/3d-bottom.png)[cite: 10] |

*3D CAD model available at [`pcb-design/Automatic-Street-Light-Controller.step`](pcb-design/Automatic-Street-Light-Controller.step).*[cite: 10]

---

## Prototype & Demo (December 2024)

### Working Demo Clip
Watch the circuit in action: [`prototype-and-demo/Working Demo.mp4`](prototype-and-demo/Working%20Demo.mp4)[cite: 10]

### Perfboard Build
| Top View | Back View |
| :---: | :---: |
| ![Prototype Top](prototype-and-demo/Prototype%20Top.jpeg)[cite: 10] | ![Prototype Back](prototype-and-demo/Prototype%20Back.jpeg)[cite: 10] |

---

## License
Released under the **MIT License** (`LICENSE`)[cite: 10].
