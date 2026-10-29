# 🛰️ Tactical Electronic Counter-Countermeasure (ECCM) & SDR Suite

An interactive, browser-based Electronic Warfare (EW) and Software-Defined Radio (SDR) tactical simulation demonstrating anti-jamming telemetry links using **Direct Sequence Spread Spectrum (DSSS)** and **(7,4) Systematic Hamming Error Correction Coding**.

🔗 **Live Interactive Demo:** [Launch Tactical Suite](https://sarthakakkalkote-tech.github.io/tactical-ecm-sdr-suite/)

---

## 🎯 System Capabilities

- **Air Defence PPI Radar & Flight Attitude HUD**: Real-time canvas simulation of UAV patrol trajectory, ground-based jamming emitter, and attitude gyros.
- **Spectrum & Waterfall Spectrogram**: Real-time frequency vs. time heat-map visualization featuring Spot Tone (+6.0 dB), Swept Chirp (2.4–2.48 GHz), and Barrage Noise jamming modes.
- **DSSS Processing Gain Engine**: Dynamic Spreading Factor configuration ($SF = 7, 15, 31$) delivering up to $+14.91\text{ dB}$ of processing gain to maintain positive anti-jam margins.
- **Interactive (7,4) Hamming FEC Sandbox**: Real-time syndrome vector calculation ($S = H \cdot r^T \pmod 2$) with interactive bit-flip error injection and automatic deterministic bit inversion.
- **Tactical Synthesizer Audio**: Web Audio API-driven tactical feedback for link acquisition and jammer interference alerts.

---

## 📐 Mathematical Formulation

### 1. DSSS Anti-Jamming Margin
$$\text{PG} = 10 \log_{10}(SF)$$
$$\text{AJ Margin} = \text{PG} - \left(\frac{J}{S}\right)$$

When $SF = 7$, $\text{PG} \approx +8.45\text{ dB}$. Against a $+6.0\text{ dB}$ tone jammer, the effective margin remains $+2.45\text{ dB}$, enabling despreading and packet recovery.

### 2. Systematic (7,4) Hamming Error Correction
- **Generator Matrix ($G_{4 \times 7}$)**: $[I_4 \mid P]$
- **Parity-Check Matrix ($H_{3 \times 7}$)**: $[P^T \mid I_3]$
- **Syndrome Decoding**: $S = H \cdot r^T \pmod 2$. If $S \neq \mathbf{0}$, the syndrome matches column $i$ of $H$, identifying the corrupted bit for instantaneous correction.

---

## 💻 Tech Stack
- **Languages**: HTML5 Canvas, Vanilla JavaScript (ES6+), CSS3 Grid & Animations
- **APIs**: Web Audio API (tactical RF alerts)
- **Domain Focus**: Radar Systems, Digital Signal Processing (DSP), Electronic Counter-Countermeasures (ECCM), Spread Spectrum Transceivers

---

## 👥 Engineering Team
- Kaushik Raghuvanshi (Roll No. 71)
- Sarthak Akkalkote (Roll No. 76)
- Aditya Pandey (Roll No. 84)
- Sauravi Kulkarni (Roll No. 11)
