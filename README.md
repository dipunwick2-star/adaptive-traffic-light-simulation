# Adaptive Traffic Light Control — Simulation Study

A simulation study comparing **fixed-time** and **adaptive-time** traffic light control systems at a signal-controlled intersection, analysed across multiple traffic scenarios.

> **Course:** CSC 446 — Simulation Study  
> **Author:** Dipun Wickramaratne  
> **Supervisor:** Dr. Kui Wu  
> **Date:** December 2024

---

## Overview

This project simulates traffic flow at a two-direction intersection (north-south and east-west) to evaluate the performance of two traffic light strategies:

- **Fixed-Time System** — uses predetermined green light durations for straight and left-turn traffic.
- **Adaptive-Time System** — dynamically adjusts green light durations based on real-time queue lengths and traffic volume.

The simulation is run under three traffic scenarios: **normal**, **rush hour**, and **low traffic**.

---

## Key Findings

| Scenario | Better System | Reason |
|---|---|---|
| Normal Traffic | Adaptive | Higher efficiency (96.3% vs 77.8%) and shorter queues |
| Rush Hour | Adaptive | Served ~440 cars vs ~240, efficiency 81% vs 40% |
| Low Traffic | Fixed | Better overall throughput and 100% efficiency |

The adaptive system is strongly recommended for normal and high-traffic conditions. In low traffic, both systems perform comparably, though the fixed-time system has longer waiting times.

---

## Simulation Metrics

The following metrics are tracked across all simulation runs:

- **Total Cars Served** — number of vehicles that cleared the intersection
- **Average Waiting Time** — average time a vehicle spends in queue
- **Average Queue Length** — mean number of vehicles waiting per cycle
- **Traffic Flow Efficiency (%)** — percentage of generated cars successfully served

---

## How It Works

1. **Traffic Generation** — Vehicles are randomly generated each cycle based on the selected traffic scenario and a seed for reproducibility.
2. **Queue Management** — Fixed mode uses separate left-turn and straight queues; adaptive mode uses a single combined queue.
3. **Green Light Logic** — Fixed mode uses preset durations; adaptive mode scales durations based on queue size.
4. **Multiple Runs** — Each scenario is run 5 times with different seeds to ensure statistical validity.
5. **Statistical Analysis** — Mean, standard deviation, standard error, and 95% confidence intervals are computed for all metrics.

---

## Project Structure

```
├── README.md
├── project_final.ipynb                    # Main simulation source code
└── A_Simulation_Study_on_Adaptive_Traffic_Light_Control.docx  # Full report
```

---

## Running the Simulation

Make sure you have Python and Jupyter installed, then run:

```bash
jupyter notebook final_project.ipynb
```

Or open `final_project.ipynb` directly in **VS Code** or **JupyterLab** and run all cells.

---

## Future Improvements

- Fine-tune green light durations based on specific queue thresholds
- Add more adaptive options for low traffic conditions
- Incorporate real-world factors such as pedestrian crossings, emergency vehicle priority, and vehicle incidents

---

## Full Report

The complete simulation report including detailed methodology, statistical tables, and analysis is available in [`A_Simulation_Study_on_Adaptive_Traffic_Light_Control.docx`](./A_Simulation_Study_on_Adaptive_Traffic_Light_Control.docx).
