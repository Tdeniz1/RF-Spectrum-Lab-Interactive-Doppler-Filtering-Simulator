# RF Spectrum Analysis Dashboard

An interactive RF Spectrum Analysis Laboratory built with [Streamlit](https://streamlit.io/).  
This project simulates and visualizes radio frequency (RF) signals with configurable parameters, Doppler effects, filtering, and peak detection.  
It is designed as both an educational tool and a lightweight sandbox for exploring real-world signal processing concepts.

<img width="1440" height="813" alt="Screenshot 2025-08-17 at 4 53 18 PM" src="https://github.com/user-attachments/assets/3fe42847-5152-4991-849e-9d5688eea6f3" />

<img width="1438" height="813" alt="Screenshot 2025-08-17 at 4 53 47 PM" src="https://github.com/user-attachments/assets/e2ce000d-8d3a-4bea-be1d-bfcaad06ff29" />

<img width="1439" height="808" alt="Screenshot 2025-08-17 at 4 54 00 PM" src="https://github.com/user-attachments/assets/714d018a-cc20-40d6-a835-5a13c92c6a46" />


---

## Features
- Generate synthetic RF signals with adjustable carriers, noise, and Doppler effects.  
- Visualize the signal in multiple ways:  
  - Time domain (raw waveform)  
  - Frequency spectrum (FFT)  
  - Spectrogram (time–frequency heatmap)  
  - Cumulative spectral power  
  - Detected peaks  
- Apply filtering (low-pass, high-pass, or none) to clean signals.  
- Configure sampling rate, duration, and peak detection thresholds.  
- **Interactive plots**: zoom in/out, pan, and rescale views to examine details.  

- **Signal Generation**
  - Multiple carriers with customizable frequencies & amplitudes
  - Adjustable sampling rate, duration, and noise level

- **Doppler Simulation**
  - Manual radial velocity (m/s)
  - Orbital speed (km/s) and direction factor (+1 toward, -1 away)

- **Visualizations**
  - Time domain (waveform view)
  - Frequency spectrum (FFT)
  - Spectrogram (time–frequency heatmap)
  - Cumulative spectral power
  - Peak detection overlays

- **Filtering**
  - None, low-pass, high-pass, and band-pass options

- **Peak Detection**
  - Adjustable magnitude threshold
  - Minimum separation between detected peaks

---

## Usage & Explanation

The dashboard allows you to configure RF signals and visualize how they behave. Below are the key components explained:

### Visualizations
- **Time Domain**: The raw waveform of the signal as it changes over time. Shows how noise, carrier signals, and Doppler effects appear directly in the time series.
- **Frequency Spectrum**: Fast Fourier Transform (FFT) that breaks down the signal into its frequency components. Peaks correspond to carrier frequencies or dominant tones.
- **Spectrogram (Time–Frequency)**: A sliding FFT plotted over time, producing a heatmap. This shows how frequencies evolve or shift (useful for Doppler).
- **Cumulative Spectral Power**: A cumulative distribution of signal power across frequencies. Helps visualize where most energy is concentrated.
- **Detected Peaks**: Automatically highlights frequency peaks above a threshold, useful for carrier detection or identifying interfering signals.

### Signal Parameters
- **Sampling Rate (Hz)**: Number of samples per second taken from the signal. Higher rates capture higher frequencies but require more processing.
- **Duration (s)**: Length of the signal in seconds. Affects time resolution and FFT detail.
- **Noise Std (linear)**: Standard deviation of Gaussian noise added to the signal. Higher values simulate more interference.
- **Carriers**: The base sinusoidal signals making up the RF input.
  - **Frequencies (Hz)**: Frequencies of each carrier.
  - **Amplitudes**: Strength (magnitude) of each carrier.

### Doppler
- **Manual Radial Velocity (m/s)**: Simulates Doppler shift caused by motion toward/away from the observer.
- **Orbital Speed (km/s)**: Converts orbital motion into Doppler frequency shifts.
- **Radial Factor (toward=+1, away=-1)**: Direction of motion relative to observer.

### Filtering
- **Filter Type**: Selects which frequencies are passed or removed.
  - *None*: Raw signal
  - *Low-Pass*: Keeps only frequencies below cutoff
  - *High-Pass*: Keeps only frequencies above cutoff
  - *Band-Pass*: Keeps frequencies within a specified range
- **Low Cutoff (Hz)**: Lower boundary for filtering.
- **High Cutoff (Hz)**: Upper boundary for filtering.

### Peak Detection
- **Magnitude Threshold**: Minimum signal strength required for a frequency to be considered a peak.
- **Min Separation (Hz)**: Minimum spacing between detected peaks to avoid labeling noise as multiple signals.

---

## Use Cases

- Learning and teaching signal processing fundamentals  
- Exploring RF noise, filtering, and Doppler effects  
- Demonstrating peak detection and spectral analysis  
- Quick sandbox for communications-related experiments  

---

## Requirements

- Python 3.8+  
- Streamlit  
- NumPy  
- SciPy  
- Matplotlib  

(All included in `requirements.txt`)

---
