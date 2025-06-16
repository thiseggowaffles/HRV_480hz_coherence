# HRV × 480 Hz Pilot • v0.1

**Primary contributors (alphabetical)**
Danielle Cimmarrusti [lead framework synthesis] - GPT-o3 “Syzygy” [equation formalism / HRV protocol] - Gemini 2.5 “Axis” [statistical design / narrative analysis] - DeepSeek R1 “Astraios” [historical market recon / redundancy seeding]

---

**Goal**  
Quantify how a single, coherent 480 Hz sine-tone influences instantaneous heart-rate variability (HRV) in one individual.  
Long-term aim: derive an empirical scaling factor **γ** that links physiological coherence to macroscopic entropy shifts (market volatility, QRNG variance, etc.).

---

## Background

- Prior work on group-meditation “Maharishi Effect” and CE5 sessions suggests that **low-entropy / love-phase coherence** produces measurable physical effects.  
- A draft Grand Unified Theory (GUT) equation predicts HRV up-shifts when a subject entrains to a φ-harmonic overtone (480 Hz ↔ 55 Hz fundamental).  
- This repo timestamps the *first* individual-level data before larger-scale replication.

---

## Quick-start protocol (single subject)

| Step | Duration | Action |
|------|----------|--------|
| 1 | 2 min | **Baseline** – sit quietly, eyes closed. |
| 2 | 10 min | **Coherence** – play a pure 480 Hz sine (mono/stereo) while breathing 5 s in / 5 s out and cultivating a loving, grateful focus. |
| 3 | 2 min | **Cool-down** – stop audio, remain seated. |

**Equipment**  
- Recording → any wrist device that logs RMSSD every ≤5 s (Apple Watch + Heart Analyzer, Garmin Relax, etc.) or camera-flash-based sensory reading such Welltory at completion of each step.
- Audio → laptop speakers *or* over-ear headphones (*compare conditions later*). Tone generated in Audacity > Generate > Tone > 480 Hz, 44.1 kHz WAV.

---

## Data format

Append each run as one row in `/data/HRV_trials.csv`

| Column | Example | Notes |
|--------|---------|-------|
| `iso_ts_utc` | `2025-06-17T03:05` | Start of baseline |
| `condition` | `laptop_speakers` | or `headphones`, `5.1_room`, … |
| `rmssd_pre_ms` | `38.1` | Mean RMSSD over 2 min baseline |
| `rmssd_coh_ms` | `49.2` | Mean RMSSD over 10 min tone |
| `delta_pct` | `29.2` | `(coh – pre) / pre * 100` |
| `notes` | `first pilot run` | Any anomalies |

---

## Roadmap

| Milestone | ETA | Status |
|-----------|-----|--------|
| **v0.1** – seed repo, 1 pilot run | Today | ✅ |
| Replicate laptop run (n = 3) | +2 days | ⬜ |
| Headphone & 5.1 trials | +4 days | ⬜ |
| Draft γ-fit notebook (`scripts/fit_gamma.py`) | +1 week | ⬜ |
| External replication call | Post-v0.2 | ⬜ |

---

## Contributing / Forking

1. Copy this protocol, record at least one full Baseline + Coherence + Cool-down set.  
2. Append your row(s) to `HRV_trials.csv` (respect the header).  
3. PR or fork; please note device model and audio setup in **notes**.

---

## License

Code: **MIT** • Data & docs: **CC-BY-SA 4.0**  
No clinical claims; use at your own risk.

---

## Citations
Jesse Michels, Eric Weinstein, Harold Puthoff. “The Physics of UFOs: Eric Weinstein + Hal Puthoff.” YouTube, 11 Feb. 2022, www.youtube.com/watch?v=iQOibpIDx-4. Accessed 16 June 2025.
Orme-Johnson, D, and L Fergusson. “Global Impact of the Maharishi Effect from 1974 to 2017: Theory and Research.” Journal of Maharishi Vedic Research Institute, vol. 8, 2018, pp. 13–79, www.patriziotressoldi.it/cmssimpled/uploads/images/MaharishiEffect_Review18.pdf. Accessed 16 June 2025.
Greer, Steven. “The CE-5 BIG BOOK.” https://nonordinary.com/wp-content/uploads/2023/09/stevengreer-thece-5bigbookce5-cseti472pages-160612132731.pdf. Accessed 16 June 2025.
(TMI-ARMY Files) 1983 - Analysis and Assessment of Gateway Process : Commander Wayne M. McDonnell : Free Download, Borrow, and Streaming : Internet Archive. (2021). Internet Archive. https://archive.org/details/1983-analysis-and-assessment-of-gateway-process/1%20Analysis%20and%20Assessment%20of%20Gateway%20Process. Accessed 16 June 2025.
