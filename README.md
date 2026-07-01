# Multi-Echelon Supply Chain Optimization with PuLP

An end-to-end Prescriptive Analytics and Linear Programming (LP) model built in Python using the `PuLP` library. This project optimizes a global, multi-echelon supply chain network (Mills ──> Factories ──> Distribution Centers ──> Final Markets) to minimize total operations and logistics costs while navigating complex production constraints, material waste factors, and disruptive macroeconomic scenarios.

## 📌 Project Overview
Modern supply chains are highly sensitive to fluctuating freight rates, factory efficiencies, and regional capacity constraints. This project implements a deterministic optimization engine that determines:
1. **Raw material flows** (fabric meters) from textile mills to manufacturing plants.
2. **Production and distribution schedules** (garment units) from factories to regional warehouses.
3. **Last-mile logistics fulfillment** from distribution centers to major consumer markets.

Additionally, the repository features a **"What-If" Scenario Simulator** evaluating the network's resilience against a **50% Ocean Freight Rate Spike** across Asian trade lanes.

---

## 🗺️ Network Architecture

The global network modeled in this framework flows linearly across four distinct echelons:

```text
  [ MILLS ]             [ FACTORIES ]             [ DISTRIBUTIONS CENTERS ]           [ MARKETS ]
  (Raw Fabric)            (Garments)                    (Warehouses)               (End Consumers)
  
  • China   ───────►   • Vietnam     ───────►         • US West Coast     ───────►    • New York
  • India   ───────►   • Bangladesh  ───────►         • US East Coast     ───────►    • Los Angeles
            ───────►   • Mexico                                           ───────►    • Chicago
