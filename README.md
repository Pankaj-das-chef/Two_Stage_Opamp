# Two Stage Opamp
---

## Circuit Overview

The circuit consists of three key sections:

### 1. **Biasing Stage**
- **Purpose:** Provides stable reference bias current of `30 µA` for tail current sources in the amplifier.
- **Key Component:** Transistor **M8** and a current source.

### 2. **Stage 1 – Differential Amplifier**
- **Transistors:** M1, M2 (differential pair); M3, M4 (PMOS current mirror load); M5 (tail current source).
- **Function:** Converts differential input signal to a single-ended output. Uses current mirror for gain and biasing.

### 3. **Stage 2 – Gain Stage**
- **Transistors:** M6 (PMOS load), M7 (common-source NMOS amplifier).
- **Capacitors:** Compensation capacitor `Cc = 3 pF`, Load capacitor `CL = 10 pF`.
- **Function:** Provides additional gain and drives capacitive load.

---

## Circuit Specifications

| Parameter               | Value               |
|------------------------|---------------------|
| VDD                    | +2.5 V              |
| VSS                    | -2.5 V              |
| Total Supply Voltage   | 5 V                 |
| Tail Current (Stage 1) | 30 µA               |
| Bias Current (Stage 2) | 95 µA               |
| Load Capacitance       | 10 pF               |
| Miller Capacitance     | 3 pF                |
| Simulation Tool        | LTspice             |

---

![image](https://github.com/user-attachments/assets/0506a90a-effa-4f77-8bde-a60485610f6a)
## Transistor Dimensions

| Transistor | W/L (µm) | Function             |
|------------|----------|----------------------|
| M1, M2     | 3 / 1    | Differential Pair     |
| M3, M4     | 15 / 1   | PMOS Load (mirror)    |
| M5, M8     | 4.5 / 1  | Current Sources       |
| M6         | 94 / 1   | Load for M7           |
| M7         | 14 / 1   | Gain Stage Amp        |

---

## Simulation Features
- **AC Analysis:** To extract gain, phase margin, and bandwidth.
- **DC Sweep:** For biasing validation and common-mode range estimation.

---

## Key Results

- **Open-Loop Gain:** 4734
- **Phase Margin:** Improved via Miller compensation
- **Output Swing:** Near rail-to-rail
- **Slew Rate:** Optimized with higher bias current in stage 2

---
![image](https://github.com/user-attachments/assets/0f27792e-e197-460f-a8f0-04659f381021)


## 📚 References

- Razavi, B. *Design of Analog CMOS Integrated Circuits.*


