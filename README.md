# Conduction-Cooled REBCO Space Propulsion Digital Twin & NASA SBIR Blueprint

[![Live Interactive Demo](https://img.shields.io/badge/Demo-Live%20WebGL%20App-0284c7?style=for-the-badge&logo=github)](https://msamsonov1.github.io/nasa-sbir-hts-propulsion/)
[![Target Topics](https://img.shields.io/badge/NASA%20SBIR-TX01.01%20%7C%20TX03.01-082f49?style=for-the-badge)](https://msamsonov1.github.io/nasa-sbir-hts-propulsion/)
[![Tech Stack](https://img.shields.io/badge/Stack-Three.js%20%7C%20Chart.js%20%7C%20TailwindCSS-38bdf8?style=for-the-badge)](https://msamsonov1.github.io/nasa-sbir-hts-propulsion/)

> **Interactive digital twin, multi-physics quench simulator, and NASA SBIR/STTR technical proposal framework for cryogen-free, conduction-cooled 2G REBCO high-temperature superconducting (HTS) magnets in space fusion and plasma propulsion.**

---

## 🚀 Live Demo & Web App

Explore the live browser-based simulator and full technical documentation here:  
👉 **[https://msamsonov1.github.io/nasa-sbir-hts-propulsion/](https://msamsonov1.github.io/nasa-sbir-hts-propulsion/)**

---

## 📌 Executive Summary

Realizing compact fusion and plasma propulsion systems—such as **Direct Fusion Drive (DFD)**, **Field-Reversed Configurations (FRC)**, and **Magnetic Nozzles**—requires on-axis magnetic field strengths between **$8\text{ T}$ and $15\text{ T}$**.

Conventional Low-Temperature Superconductors (NbTi, $\text{Nb}_3\text{Sn}$) rely on liquid helium at $4.2\text{ K}$, introducing severe boil-off risks, cryogenic complexity, and prohibitive radiator area requirements. 

This repository presents an architecture engineered for **cryogen-free conduction cooling ($20\text{ K to } 50\text{ K}$)** via solid-state cryocoolers and thermal busbars. By operating at elevated cryogenic temperatures, radiator mass drops by over **80%** due to Stefan-Boltzmann scaling:

$$\dot{Q}_{\text{rad}} = \epsilon \sigma A \left( T_{\text{rad}}^4 - T_{\text{sink}}^4 \right)$$

---

## ⚡ Core Engineering Pillars

1. **Conduction-Cooled Busbars:** Direct thermal coupling using flexible aluminum and high-purity pyrolytic graphite busbars connected to closed-cycle pulse-tube cryocoolers (zero liquid cryogen).
2. **Non-Insulated (NI) Winding Topology:** Passive self-protection against catastrophic quench burnout. Local normal zones divert azimuthal current ($I_\theta$) radially ($I_r$) into adjacent turns through calibrated turn-to-turn contact resistance ($R_c$).
3. **Screening-Current and Stress FEA:** Modeling electro-mechanical hoop stresses ($\sigma_\theta$) and screening-current-induced peel forces up to $600\text{ MPa}$ on CTE-matched composite mandrels.

---

## 🛠️ Interactive Features in This Repository

* **Interactive 3D WebGL Digital Twin:** Built with Three.js to render a double-pancake 2G REBCO magnet assembly, CTE titanium mandrel, thermal busbars, dynamic vector contours, and plasma exhaust geometry.
* **Real-Time Solver Controls:** Adjust operating temperature ($4.2\text{ K} - 77\text{ K}$), transport current ($50\text{ A} - 500\text{ A}$), and winding turns to calculate on-axis magnetic flux density ($B_0$), hoop stress, and Stefan-Boltzmann thermal radiator mass cuts in real time.
* **Transient Hotspot & Quench Engine:** Built-in transient simulator demonstrating turn-to-turn passive current shunting and temperature stabilization during a normal-zone event.
* **Full NASA SBIR Phase I Proposal Text:** Complete, formatted technical documentation targeting **NASA SBIR TX01.01 (Advanced In-Space Propulsion)** and **TX03.01 (Power & Energy Storage)** with downloadable Markdown export.

---

## 🤝 Hardware Lab Partnership (Open Call)

**RF WaveCode specializes in software modeling, multi-physics digital twins, and government proposal writing.** To advance this architecture from **TRL 2 to TRL 4**, we are actively seeking experimental laboratory partners (university groups, national labs, or private magnetics facilities) to co-author and execute NASA/DoD SBIR and STTR contracts.

### Division of Responsibility

| RF WaveCode (Software Lead) | Hardware Partner Lab (Experimental Lead) |
| :--- | :--- |
| Coupled electromechanical & thermal FEA solvers | Tension-regulated winding rig for 4 mm / 12 mm REBCO tape |
| Dynamic quench & screening-current models | Vacuum cryostat capable of base temperatures $\le 30\text{ K}$ |
| High-speed lab telemetry DAQ & alert pipelines | High-current DC power supply ($500\text{ A} - 1{,}000\text{ A}$) |
| SBIR lead technical writing, budgeting, & compliance | Empirical critical current ($I_c$) & quench validation |

📩 **Interested in co-applying or collaborating?**  
Contact us at: **[support@rfwavecode.com](mailto:support@rfwavecode.com)** *(Mutual NDAs available upon request)*

---

## 💻 Tech Stack & Deployment

* **Runtime:** Zero-dependency static client-side web application
* **Visualization:** [Three.js](https://threejs.org/) (WebGL 3D Rendering)
* **Plots:** [Chart.js](https://www.chartjs.org/) (Transient Current Sharing & Quench Curves)
* **Typography & Math:** [KaTeX](https://katex.org/) (LaTeX formula rendering)
* **Styling:** [Tailwind CSS](https://tailwindcss.com/)
* **Hosting:** GitHub Pages

---
© 2026 RF WaveCode Incorporated. All rights reserved; the simulation software, algorithms, 
and digital twin models are proprietary and may not be reproduced, modified, or distributed without prior written permission.

## 📦 Local Development

Clone the repository and open `index.html` in any modern web browser:

```bash
git clone [https://github.com/msamsonov1/nasa-sbir-hts-propulsion.git](https://github.com/msamsonov1/nasa-sbir-hts-propulsion.git)
cd nasa-sbir-hts-propulsion

# Using Python to run a local static server:
python3 -m http.server 8000

