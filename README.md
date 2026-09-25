# 🚦 Adaptive Traffic Light Controller — Model-Based Design (Simulink → Arduino / STM32)

![MATLAB/Simulink](https://img.shields.io/badge/MATLAB%2FSimulink-Stateflow-blue)
![Arduino](https://img.shields.io/badge/Target-Arduino%20Uno-00979D)
![STM32](https://img.shields.io/badge/Target-STM32-03234B)
![Tinkercad](https://img.shields.io/badge/Prototype-Tinkercad-orange)

An adaptive traffic-light controller that changes signal timing according to traffic density at a junction. It was designed with **Model-Based Design**: the control logic is modelled and simulated in **MATLAB/Simulink**, prototyped virtually in **Tinkercad**, and deployed on **Arduino Uno** and **STM32** hardware.

---

## 📌 What the system does

- Reads traffic density at the junction through **3 analog** and **3 digital** inputs.
- Drives **9 digital outputs** (red / amber / green for each approach).
- Extends or shortens each green phase according to the measured density instead of using fixed timings.

## 🔄 Development flow

| Stage | Tool | Where to look |
| :--- | :--- | :--- |
| Control-logic modelling & simulation | MATLAB / Simulink | [`SmartTC_Project/Simulation/`](SmartTC_Project/Simulation/) |
| Virtual prototype | Tinkercad | [Tinkercad model](https://www.tinkercad.com/things/hLeGNquayHd/editel?returnTo=%2Fdashboard&sharecode=9o8Co3ha0FYXQ2WgP38SyBCF3VPplbhYBZKHiCZhICw) · [`SmartTC_Project/Tinkercad/`](SmartTC_Project/Tinkercad/) |
| Hardware build (Arduino Uno) | Arduino + Simulink | [`SmartTC_Project/Hardware Implenetation/`](SmartTC_Project/Hardware%20Implenetation/) |
| Deployment to STM32 | Simulink STM32 support | [`SmartTC_Project/STM32_Simulink_Model/`](SmartTC_Project/STM32_Simulink_Model/) |

## 🧩 Simulink models

| Model | Description |
| :--- | :--- |
| [`Santhosh_simulation/STC_Santhosh1.slx`](SmartTC_Project/Simulation/Santhosh_simulation/STC_Santhosh1.slx) | Adaptive controller logic (Santhosh) |
| [`Santhosh_simulation/type2_STC.slx`](SmartTC_Project/Simulation/Santhosh_simulation/type2_STC.slx) | Alternative control strategy (Santhosh) |
| [`Santhosh_simulation/Arduino_STC.slx`](SmartTC_Project/Simulation/Santhosh_simulation/Arduino_STC.slx) | Arduino-targeted model (Santhosh) |
| [`STC_SIva.slx`](SmartTC_Project/Simulation/STC_SIva.slx) | Controller variant (Siva) |
| [`Traffic_controller_Sagar.slx`](SmartTC_Project/Simulation/Traffic_controller_Sagar.slx) | Controller variant (Sagar) |
| [`stm32.slx`](SmartTC_Project/STM32_Simulink_Model/stm32.slx) | STM32 deployment model, with a step-by-step guide in [`Document_STM32.docx`](SmartTC_Project/STM32_Simulink_Model/Document_STM32.docx) |

## 🎥 Demos

- Tinkercad simulation: [video](SmartTC_Project/Tinkercad/WhatsApp%20Video%202025-02-16%20at%2021.51.51_0427e33d.mp4) · [prototype image](SmartTC_Project/Tinkercad/WhatsApp%20Image%202025-02-16%20at%2021.20.21_befedc2d.jpg)
- Hardware implementation: [videos](SmartTC_Project/Hardware%20Implenetation/)
- STM32 deployment: [videos](SmartTC_Project/STM32_Simulink_Model/)
- Project presentation: [`MODEL BASED DESIGN.pptx`](MODEL%20BASED%20DESIGN.pptx)

## ▶️ How to run

1. Open any `.slx` model from the table above in MATLAB/Simulink.
2. Press **Run** and watch the signal states in the Scope / Stateflow chart.
3. For hardware: install the *Simulink Support Package for Arduino Hardware* (or *for STM32*), connect the board, and use **Build, Deploy & Start**.

## 👥 Team

Challa Santhosh · Siva ([@siva6014](https://github.com/siva6014)) · Sagar ([@KJ-Sagar](https://github.com/KJ-Sagar)) — GITAM University, Bengaluru

## 👤 Author

**Challa Santhosh** — Model-Based Design & Embedded AI Engineer  
[LinkedIn](https://www.linkedin.com/in/challa-santhosh-36693828a/) · [GitHub](https://github.com/Challa200Santhosh) · sschalla10@gmail.com
