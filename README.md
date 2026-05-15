# Backup Power Generation Using a Synchronous Generator

> **MATLAB/Simulink simulation of a synchronous motor driven as a generator, converting 2800 rpm mechanical input into stable 220 V / 50 Hz AC power for a small workshop.**

---

## 📌 Overview

A small workshop experiences frequent power outages. An available diesel engine shaft (2800 rpm) is used to mechanically drive a **synchronous motor**, operating it as a **generator**. The target output is **800–1200 W at 220 V, 50 Hz**, with ≥75% efficiency and ≤±10% voltage regulation.

This project models the system in **MATLAB/Simulink**, validates theoretical calculations, and demonstrates a low‑cost backup power solution.

---

## 🎯 Key Results

| Parameter | Value | Target | Status |
|-----------|-------|--------|--------|
| Output Voltage (RMS) | 219.10 V | 220 V ±10% | ✅ Within range |
| Output Current | 2.613 A | – | – |
| Efficiency | **99.71%** | ≥75% | ✅ Exceeds |
| Voltage Regulation | 22.35% | ≤±10% | ⚠️ Higher (see report) |
| Stability | Steady at 2.5–3 s | – | ✅ Stable |

*Note: Voltage regulation can be improved by adjusting field excitation – see load tests in report.*

---

## 🛠️ Technologies & Tools

- **MATLAB/Simulink** – Synchronous Machine block, RMS calculation, scopes
- **Mathematical modeling** – per‑unit system, base impedance, copper losses, three‑phase power
- **Load analysis** – resistive load tests from no‑load to 1000 W

---

## 🔧 How It Works

1. **Mechanical input** – Constant speed of 314.2 rad/s (2800 rpm) from a diesel engine.
2. **Electrical excitation** – Constant DC field voltage (1.45 V) applied to the rotor.
3. **Generator action** – The synchronous machine produces three‑phase AC voltage at 50 Hz.
4. **Load connection** – Three‑phase resistive load simulates workshop equipment.
5. **Monitoring** – RMS voltage/current displays and scopes verify steady‑state operation.

---

## 📊 Simulation Results (Selected Loads)

| Load (W) | Field Excitation (V) | V_L_avg (V) | I_L_avg (A) | P_out (W) |
|----------|----------------------|-------------|-------------|-----------|
| 1000     | 1.45                 | 219.10      | 2.613       | 991.60    |
| 750      | 1.45                 | 237.97      | 2.129       | 877.50    |
| 500      | 1.45                 | 253.70      | 1.513       | 664.80    |
| 250      | 1.45                 | 264.17      | 0.788       | 360.55    |
| No‑Load  | 1.45                 | 268.07      | 0.003       | 1.49      |

*Full test results including adjusted excitation are in the report (Appendix).*

---

## 🧠 Theoretical Calculations (Sample)

- **Base impedance** – \( Z_{base} = \frac{220^2}{1000} = 48.4\,\Omega \)
- **Stator resistance** – \( R_s = 0.00285 \times 48.4 = 0.1379\,\Omega \)
- **Copper losses** – \( P_{loss} = 3 \times (2.665)^2 \times 0.1379 = 2.94\,\text{W} \)
- **Mechanical input power** – \( P_{in} = 1031.5 + 2.94 = 1034.44\,\text{W} \)
- **Efficiency** – \( \eta = \frac{1031.5}{1034.44} \times 100 = 99.71\% \)
- **Voltage regulation** – \( VR\% = \frac{268.07 - 219.10}{219.10} \times 100 = 22.35\% \)


---

## 👥 Team

- [Muhammad Shariq](https://www.linkedin.com/in/muhammad-shariq-715653344) (24K-6084)
- [Muhammad Ali Siddiqui](https://www.linkedin.com/in/muhammad-ali-42524a40b) (24K-6121)
- [Syed Muneeb Ahmed](https://www.linkedin.com/in/syed-muneeb-ahmed-027950393) (24K-6030)
- [Abdullah Hussain](https://www.linkedin.com/in/abdullah-hussain-19422b380) (24K-6037)
- [Syed Hassaan Ali](https://www.linkedin.com/in/hassaan-ali-685973305) (24K-6106)

---

## 📜 License

Educational use only.

## 🔗 Connect with Me

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-blue?logo=linkedin)](https://www.linkedin.com/in/syed-muneeb-ahmed-027950393)  
[![GitHub](https://img.shields.io/badge/-GitHub-black?logo=github)](https://github.com/Buns-Dev)
