# Vasya Batmaev — Software Engineer & Applied Researcher

> This is an extended version of my resume with more detail and context than fits on one page. It works well for AI-assisted screening.

## Contact

- Email: vbbatmaev@gmail.com
- Telegram: [t.me/batmaev](https://t.me/batmaev)
- GitHub: [github.com/batmaev](https://github.com/batmaev)
- Location: Moscow, Russia. Ready to relocate. Available for remote work during the relocation process.

## Summary

ML engineer and fullstack developer with a physics and mathematics foundation from MIPT (Russia's top-ranked STEM university). I build algorithm-heavy products end-to-end: ML models (PyTorch, scikit-learn), backends (FastAPI, Docker), and frontends (TypeScript, Svelte, Next.js).

Current PhD research: eye-movement biometrics with near-state-of-the-art liveness detection on consumer hardware. Outside academia — production UIs, sensor data pipelines deployed on real hardware, and community tools with thousands of users.

## Technical Skills

| Area | Technologies |
|---|---|
| **Languages** | Python, TypeScript/JavaScript, Julia, SQL |
| **Working knowledge** | Swift, C/C++, Kotlin (KMP), Haskell |
| **ML / Data Science** | PyTorch, scikit-learn, Bayesian inference (Turing.jl), Plotly, Dash, matplotlib, seaborn |
| **Backend & Infrastructure** | FastAPI, Docker / Docker Compose, REST APIs, SQLite, SQLAlchemy, PostgreSQL, SurrealDB, Caddy, Vercel |
| **Frontend** | Svelte, Next.js, Electron, HTML/CSS/JS, shadcn/ui |
| **Tools** | Git, Linux CLI, LaTeX, Wolfram Mathematica, Cursor, Claude Code |

## Experience

### R&D Engineer / PhD Researcher — MIPT (2024 – present)

Building a challenge-response biometric system that defends against deepfake and replay attacks. Users watch a randomly moving point; their eye movements are recorded (front-facing camera, Tobii, iOS ARKit, or AR glasses) and fed into a neural network. Random trajectories make replay attacks impossible.

The system has two parts: identification (recognizing who the user is) and liveness detection (confirming the signal comes from a real person, not a deepfake). Prior work (DeepEyedentificationLive, Makowski et al., 2021) demonstrated identification on a medical-grade eye tracker. We have not yet reproduced identification on consumer devices. For liveness detection, we achieved **EER = 1.6%** on iPhone ARKit data — a meaningful result given the much lower precision of consumer hardware compared to medical eye trackers.

- Training and evaluating **PyTorch** and **scikit-learn** models on eye-movement time series.
- Built the data collection backend in **FastAPI**: session recording API, trajectory storage, user management.
- Published a peer-reviewed paper (Information Security Issues, 2025).
- Co-supervising a Master's student.

---

### Software Engineer — mixim startup (Nov 2024 – May 2025)

Built the complete UI for a customizable-beverage kiosk in **Electron + Svelte 5**:

- Customer-facing ingredient selection / recommendation screen + a barista screen on a separate display, communicating via **Electron IPC**.
- Implemented offline-resilient state management so the UI never froze when the backend (user accounts, recommendations) went down — which happened often.

---

### iOS Developer — Vependo VPN (Jan 2025)

Ported a VPN app to iOS. Three-language build: **Kotlin Multiplatform** UI, open-source **Go** protocol (XTLS Reality), **Swift** Network Extension. The main challenge was getting the multi-language pipeline to compile with correct entitlements and bundle IDs.

---

### R&D Engineer — MIPT Telecom Research Center (May – Dec 2023)

Worked on a gyro-stabilized satellite antenna that tracks a geostationary satellite from a moving ship.

- Built an IMU data pipeline on **Raspberry Pi**: gyroscope + accelerometer → orientation quaternions via **Kalman filtering** (AHRS library) → time-series files with automatic archival. Deployed on an actual ship to record wave motion data.
- Wrote a **Python** control library for a hexapod robot platform (UDP commands + real-time **Plotly/Dash** monitoring UI) used to simulate ship motion for antenna testing.
- Debugged **C** motor-controller firmware. Tracked down an inclinometer giving wrong readings to a grounding issue — required understanding both the software protocol and the electrical setup.

---

### Open-Source & Community Projects

**@phystech_bot — Telegram university verification bot**

Creates protected invite links for MIPT-only Telegram chats; users verify their university email with a one-time code.

- **6,700+ registered users** — ~84% of the student body, with no official university support. 21 GitHub stars.
- Tech: Docker Compose, aiogram, Telethon, SQLite, SQLAlchemy.

---

**Anonymous student dating service (Telegram Mini App)**

Users post anonymous profiles via a bot; others respond through a Mini App. **1,700+ subscribers.**

- Diagnosed and worked around Russian state-level DPI throttling (connections dropped after ~10–15 KB) by downgrading to HTTP/1.1, shrinking the bundle, and adding API retries.
- Tech: Docker Compose, aiogram, HTML/JS/CSS, Caddy.

---

### Forest classification from satellite imagery (2023)

Unsupervised segmentation of satellite images (deciduous forests, coniferous forests, burn scars) using the Invariant Information Clustering method ([Ji et al., 2019](https://arxiv.org/abs/1807.06653)). Accuracy was validated by expert visual assessment (no ground truth labels available). Published at the IKI RAS (Space Research Institute) conference.

## Education

### PhD candidate, Computer Science — MIPT (2024 – 2027, in progress)

- **Dissertation:** Eye-movement biometrics. Advisor: V.A. Konyavsky.
- The program is mostly online and will not interfere with relocation or full-time work.

### MSc, Scientific Software — MIPT (2022 – 2024)

- **GPA: 5.0 / 5.0, honors diploma.**
- **Thesis:** Bayesian analysis of variable star light curves — estimated mass ratios and orbital inclination of T Coronae Borealis using probabilistic programming in **Julia + Turing.jl**.
- Key courses: Databases (SQL), Statistical Methods, Computational Methods (SVD, Kalman filter), Docker, Advanced Python.

### BSc, Physics — MIPT (2018 – 2022)

- **GPA: 4.98 / 5.0, honors diploma.** Received the Abramov-Frolov scholarship (awarded for top GPA at MIPT).
- **Thesis:** Variational quantum algorithm for the Traveling Salesman Problem, simulated in Google `Cirq`.
- Extensive coursework in quantum mechanics, statistical physics, quantum information & computing, PDEs, probability theory, complex analysis.
- Quantum computing track: quantum cryptography, superconducting quantum systems, physical realizations of qubits.

### Additional Training

- **Algorithms & Data Structures** (VK Education) — implemented algorithms including string algorithms in **C++**.
- **Deep Learning School**, MIPT: neural network fundamentals, training pipelines.
- **Yandex Interface Development School**: led a 3-person frontend team building a text-to-image evaluation tool (Next.js, OAuth/PKCE, shadcn/ui). 24-person cross-functional team, 3-weekend sprint.
- **Functional Programming in Haskell** (Stepik, 2 parts).

## Publications

1. **Defense against deepfake attacks on face recognition systems. Liveness detection via eye movements** — Batmaev V.B., Novikov Yu.A. // Information Security Issues, 2025
2. **Dynamic eye-movement biometrics: trust with untrusted devices** — Batmaev V.B. // MIPT Scientific Conference, 2025
3. **Bayesian parameter estimation of symbiotic variable stars from light curves using probabilistic programming** — Batmaev V.B. // MIPT Scientific Conference, 2024
4. **Forest classification from satellite imagery via neural networks and mutual information maximization** — Matseyko A.V., Batmaev V.B., Kharuk I.V., Fedotova E.V. // IKI RAS Conference on Remote Sensing, 2023

## Olympiads & Awards

**University:**
- **National olympiad ["I'm a Professional"](https://yandex.ru/profi):** 1st place in Russia — Quantum Technologies; 3rd place — Innovative Medicine.

**High school:**
- **All-Russian Physics Olympiad:** regional stage prize winner.
- **"Lomonosov" Math Olympiad (Moscow State University):** 1st degree diploma.
- **"Phystech" Physics Olympiad:** 2nd degree diploma.

## Languages

- **Russian:** native
- **English:** fluent (professional working proficiency)