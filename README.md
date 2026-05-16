# ⚡ DotDash – Morse Code Suite

**DotDash** is a fully self-contained, browser-based Morse Code encoder/decoder.  
Convert between **text, Morse code, and audio** — all inside a single HTML file.

✅ Works **100% offline**  
✅ No dependencies  
✅ Real-time audio decoding with adaptive intelligence  

---

## 🆕 Version 1.2.1 Updates

### 🧠 Advanced Audio Decoding Engine
- **Adaptive signal detection** using RMS + dynamic thresholds
- **Rolling energy normalization** improves accuracy in noisy environments
- **K-means clustering** for:
  - Letter gap detection
  - Word gap detection
- **Signal buffering system** for real-time mic decoding stability
- **Adaptive dot duration estimation** (median-based, auto-adjusting)

### 🔊 Enhanced Signal Detection
- New `SignalDetector` class with:
  - RMS energy processing
  - Goertzel-based frequency analysis (foundation for tone locking)
- Improved thresholding logic for better detection of weak signals

### 📡 Improved Audio File Decoding
- Smarter burst detection and merging
- Adaptive merge gaps based on signal timing
- Multi-cluster gap analysis (4-cluster K-means)
- Better handling of:
  - Quiet audio files
  - Fragmented signals
  - Irregular timing

### 🧹 Reset Controls (New Feature)
- Added **🛠 Reset Sliders** button
- Instantly resets:
  - Dot duration
  - Frequency
  - Volume
  - Sensitivity
  - Dot estimate

### ✍️ Text Encoding Improvements
- Handles **newline characters intelligently**
- Prevents accidental word breaks from formatting
- More accurate Morse spacing output

### 🎛️ UI / UX Improvements
- Reset button styling
- Improved status feedback ("Settings Reset")
- Better error handling and debug logging
- Cleaner decode output logic
- Smarter audio toggle behavior

---

## 🚀 Features

### 🔤 Text ↔ Morse
- Encode English → Morse (live preview)
- Decode Morse → English
- Supports:
  - Letters (A–Z)
  - Numbers (0–9)
  - Punctuation

### 🔊 Morse Audio
- Play Morse code tones
- Adjustable:
  - Dot duration
  - Frequency
  - Volume
- Export to `.wav`

### 🎙️ Audio Decoding

#### Microphone (Real-Time)
- Adaptive thresholding
- Signal buffering
- Live waveform visualization
- Auto-adjusting timing detection

#### File Upload
- Supports: `mp3`, `wav`, `ogg`, `m4a`
- Intelligent decoding pipeline:
  - RMS normalization
  - Burst segmentation
  - Gap clustering (K-means)
- Displays:
  - Decoded text
  - Detection status

### ⌨️ Manual Morse Input
- Real-time decoding
- Input filtering
- Optional audio feedback
- Error highlighting for unknown sequences

### 📚 Morse Reference
- Interactive grid layout
- Responsive design
- Full character set

---

## 🧠 How It Works (v1.2.1)

### Signal Detection Pipeline
1. Capture audio (mic/file)
2. Compute RMS energy
3. Apply adaptive threshold (rolling history)
4. Detect signal vs silence
5. Buffer signals for analysis

### Decoding Intelligence
- **Dot/Dash Classification**
  - Based on adaptive timing estimate
- **Gap Detection**
  - K-means clustering identifies:
    - intra-letter gaps
    - letter gaps
    - word gaps
- **Dynamic Adjustment**
  - Continuously recalibrates during decoding

### Audio Generation
- Web Audio API (Oscillator + Gain)
- OfflineAudioContext for WAV export
- Manual WAV encoding

---

## 🛠️ Tech Stack

- HTML5
- CSS3 (custom theme)
- Vanilla JavaScript
- Web Audio API
- Canvas API

No frameworks. No build tools.

---

## 📦 Installation

### Run Locally
1. Download `index.html`
2. Open in browser

### Offline Mode
- Use built-in download link inside app

---

## ⚙️ Controls Overview

| Control | Description |
|--------|-------------|
| Dot Duration | Speed of Morse timing |
| Frequency | Tone pitch |
| Volume | Audio output level |
| Sensitivity | Signal detection threshold |
| Dot Estimate | Initial decode timing |
| Reset Sliders | Restore defaults instantly |

---

## ⚠️ Limitations

- Audio decoding depends on:
  - Signal clarity
  - Background noise
  - Consistent timing
- Extremely distorted or compressed audio may reduce accuracy
- Microphone quality impacts real-time decoding

---

## 🧪 Debug & Diagnostics (New)

- Console logging for:
  - Signal bursts
  - Threshold calculations
  - K-means clustering
  - Audio file diagnostics
- Built-in helpers:
  - `debugSignalDetection()`
  - `quickVolumeCheck()`

---

## 📄 License
This project is licensed under the MIT License.

See the full license in the LICENSE file.


---

## 👨‍💻 Author

**Jeffrey Lassen**  
Version: `1.2.7`  
Last Updated: `05/16/2026`

https://github.com/jhlassen17

---

## ☕ Support

If you find this useful:  
👉 https://buymeacoffee.com/hanf

---

## 💡 Future Ideas

- Frequency auto-locking (complete Goertzel integration)
- WPM (Words Per Minute) presets
- Save/load sessions
- Mobile-first UI enhancements
- Export decoded transcripts

---
