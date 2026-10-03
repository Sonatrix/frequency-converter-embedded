# ⚡ FreqConvert Pro Suite: Interactive Frequency Converter Explorer

An advanced, web-based interactive simulation suite for exploring **Frequency Conversion Principles** across Industrial Power Electronics (VFDs, Space Vector PWM), RF Telecommunications (Heterodyne Down/Up-converters, Image Rejection), and Digital Signal Processing (DSP).

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-Canvas%20%26%20Web%20Audio-orange.svg)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-v3.0-38bdf8.svg)

---

## 🌟 Key Features

### 1. Dual Conversion Modes
* **Low to High (Up-conversion):** Frequency Multipliers (Doublers/Triplers), RF Heterodyne Up-converters ($f_{out} = f_{LO} + f_{in}$), and Step-Up Cycloconverters.
* **High to Low (Down-conversion):** Superheterodyne Down-converters ($f_{out} = |f_{LO} - f_{in}|$), Variable Frequency Drives (VFD Rectifier-Inverter), and Digital Frequency Dividers ($f_{out} = f_{in} / N$).

### 2. Industrial VFD & Power Electronics Domain
* **Space Vector PWM (SVPWM) Visualizer:** Real-time 2D $\alpha$-$\beta$ stationary frame tracking rotating voltage vector $\vec{V}_{ref}$ across 6 active switching sectors.
* **Control Strategies:** Switch between Volts/Hertz ($V/f$), Field-Oriented Control (FOC), and Direct Torque Control (DTC).
* **Inverter Non-Idealities:** Inverter dead-time insertion toggle showing zero-crossing notch distortion and harmonic generation ($5^{\text{th}}, 7^{\text{th}}$ harmonics).
* **Dynamic Induction Motor Load:** Simulated telemetry gauges for Speed (RPM), Electromagnetic Torque ($\text{N}\cdot\text{m}$), and Rotor Slip ($s\%$).

### 3. RF Heterodyne & Telecom Domain
* **Intermodulation Distortion (IMD3):** Toggle 3rd-order intermodulation spurs ($2f_1 - f_2, 2f_2 - f_1$).
* **Image Frequency Rejection:** Analyze image frequency leakage ($f_{img} = f_{LO} + f_{IF}$) and apply **Hartley** or **Weaver** filter topologies.
* **Oscillator Impairments:** Phase noise skirts ($\text{dBc/Hz}$) and Local Oscillator (LO) feedthrough leakage.

### 4. Interactive DSP & Audio Electronics
* **Web Audio API Tone Synthesizer:** Real-time audio pitch generation with dynamic master volume control ($0\% - 200\%$) and integrated `DynamicsCompressorNode` anti-clipping limiter.
* **2D Waterfall Spectrogram:** Time-variant scrolling STFT matrix plot tracking frequency sweeps over time.
* **Interactive Oscilloscope & FFT:** Real-time time-domain traces with probes ($V_{pp}, V_{rms}, \Delta t$, THD%) and frequency-domain spectrum analysis.
* **Data Export:** Export high-resolution time-series waveform data directly to `.csv` for analysis in MATLAB, Python, or LTSpice.

---

## 🚀 Live Demo & Quick Start

### Option A: Run Locally (No Installation Needed)
1. Clone or download this repository:
   ```bash
   git clone https://github.com/your-username/freqconvert-pro.git
   ```
2. Open `index.html` directly in any modern web browser (Chrome, Firefox, Edge, Safari).

### Option B: Deploy via GitHub Pages
1. Push `index.html` and `README.md` to your GitHub repository.
2. Go to **Settings** $\rightarrow$ **Pages**.
3. Under **Branch**, select `main` and `/ (root)`.
4. Click **Save**. Your site will be live at:
   `https://<your-username>.github.io/<your-repo-name>/`

---

## 🧮 Theoretical Background

### Heterodyne Frequency Mixing
$$v_{mix}(t) = \cos(2\pi f_{in} t) \cdot \cos(2\pi f_{LO} t) = \frac{1}{2}\left[\cos(2\pi (f_{LO}-f_{in})t) + \cos(2\pi (f_{LO}+f_{in})t)\right]$$

### Space Vector PWM (SVPWM)
$$\vec{V}_{ref} = \frac{2}{3}\left(V_a + V_b e^{j\frac{2\pi}{3}} + V_c e^{j\frac{4\pi}{3}}\right)$$

### Synchronous Motor Speed
$$N_s = \frac{120 \cdot f_{out}}{P}$$

---

## 🛠️ Built With

* **HTML5 Canvas API** — Real-time high-performance 60 FPS rendering.
* **Web Audio API** — Real-time waveform audio synthesis & dynamics compression.
* **Tailwind CSS** — Modern dark-mode UI styling.
* **KaTeX** — Fast mathematical formula rendering.
* **Lucide Icons** — Vector interface icons.

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).