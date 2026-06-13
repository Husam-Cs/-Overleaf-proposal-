# -Overleaf-proposal-
# CL-PAVE: Closed-Loop Physiologically Adaptive Virtual Reality System for Exposure Therapy of Specific Phobias

**GP1 — Research Track**
Department of Computer Science, Faculty of Computer and Information Technology
Jordan University of Science and Technology (JUST)

## Team

- Hamzeh Badaro [163343]
- Eman Abu Zeitoun [166016]
- Husam Al-Zu'bi [158032]
- Dareen Halaweh [161118]

**Supervisor:** Dr. Qanita Bani Baker

## Overview

CL-PAVE is a closed-loop, physiologically adaptive VR system for graded exposure therapy of specific phobias. It acquires real-time ECG data from a Polar H10 chest-strap sensor via Bluetooth Low Energy, extracts Heart Rate Variability (HRV) features (HR, RMSSD, SDNN) using a Python inference layer, and streams a continuous arousal regression score over Open Sound Control (OSC) to a standalone Meta Quest 3S running an Unreal Engine 5 environment. The VR scene continuously modulates stimulus parameters (ambient audio, animation speed, stimulus density) to keep the user's arousal within the therapeutic window defined by the inhibitory learning model of exposure therapy.

Two phobia scenarios — acrophobia and arachnophobia — will validate the generalizability of the architecture.

## Project Aims

1. **System Integration** — End-to-end pipeline: Polar H10 (BLE) → Python inference layer → OSC → UE5/Meta Quest 3S, targeting <1.0s latency.
2. **Arousal Estimation Engine** — Continuous arousal regression model from HRV metrics, calibrated against individual baselines and validated via SUDS.
3. **Modulation Mechanics** — Continuous bidirectional modulation of environmental variables to regulate arousal without breaking immersion.
4. **Generalizability Assessment** — Validate the architecture across acrophobia and arachnophobia scenarios.
5. **Data Infrastructure** — Automated session logging for clinical analysis and model refinement.

## Repository Structure

```
.
├── proposal/        # Overleaf/LaTeX source and compiled PDF of the GP1 proposal
├── src/
│   ├── ecg_processing/   # Python BLE acquisition + HRV feature extraction (biosppy/neurokit2)
│   └── ue5_osc/           # Unreal Engine 5 OSC receiver and scene modulation logic
├── data/            # Session logs (CSV) from pilot testing — not yet populated
└── docs/            # Architecture diagrams and supporting documentation
```

## Current Status

| Component | Status |
|---|---|
| System architecture design | Complete |
| Hardware procurement (Polar H10, Meta Quest 3S) | Complete |
| HRV feature extraction (Python) | In Progress |
| Arousal regression model | Pending |
| UE5 OSC receiver module | In Progress |
| Acrophobia VR scenario | In Progress |
| Arachnophobia VR scenario | Pending |
| End-to-end latency validation | Pending |
| SUDS-calibrated model validation | Pending |

## Tech Stack

- **Biosensor:** Polar H10 chest-strap ECG
- **HMD:** Meta Quest 3S (standalone)
- **Processing:** Python 3.x — `biosppy`, `neurokit2`
- **VR Engine:** Unreal Engine 5 (Meta XR SDK)
- **Communication:** Open Sound Control (OSC)

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.
