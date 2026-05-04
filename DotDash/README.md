# ⚡ DotDash – Morse Code Suite

**DotDash** is a fully self-contained, browser-based Morse Code encoder/decoder.  
It converts between text, Morse code, and audio — all in a single HTML file with **no dependencies**.

✅ Works **100% offline**  
✅ No install required  
✅ Runs in any modern browser  

---

## 🚀 Features

### 🔤 Text ↔ Morse
- Encode English text → Morse code (live preview)
- Decode Morse code → English text
- Supports letters, numbers, and punctuation

### 🔊 Morse Audio
- Play Morse code as audio tones
- Adjustable:
  - Dot duration
  - Frequency
  - Volume
- Download Morse as `.wav` file

### 🎙️ Audio Decoding
- Decode Morse from:
  - Microphone input (real-time)
  - Uploaded audio files (`mp3`, `wav`, `ogg`, etc.)
- Adaptive timing detection
- Displays:
  - Detected Morse
  - Decoded text
  - Live waveform

### ⌨️ Manual Morse Input
- Real-time decoding as you type
- Input validation (only `. - /`)
- Optional audio feedback per keystroke

### 📚 Built-in Reference
- Interactive Morse code reference table
- Covers:
  - A–Z
  - 0–9
  - Common punctuation

---

## 📦 Installation

No installation needed.

### Option 1: Run Locally
1. Download `index.html`
2. Open it in your browser

### Option 2: Use Offline Mode
- Click the **“Download Offline Version”** link inside the app  
- Save it anywhere and run anytime without internet

---

## 🧠 How It Works

- **Encoding**: Uses a static `MORSE_MAP` lookup table
- **Audio Generation**: Web Audio API (Oscillator + Gain nodes)
- **WAV Export**: OfflineAudioContext + manual WAV encoding
- **Decoding (Mic/File)**:
  - RMS signal detection
  - Adaptive dot duration estimation
  - Timing-based symbol classification (dot vs dash)

---

## 🛠️ Tech Stack

- HTML5
- CSS3 (custom UI theme)
- Vanilla JavaScript
- Web Audio API
- Canvas API (waveform visualization)

No frameworks. No libraries. No build step.

---

## 📸 Screenshots

*(Optional — add screenshots here for GitHub polish)*

---

## ⚙️ Controls Overview

| Control | Description |
|--------|-------------|
| Dot Duration | Speed of Morse timing |
| Frequency | Tone pitch (Hz) |
| Volume | Playback volume |
| Sensitivity | Audio decoding threshold |
| Dot Estimate | Initial timing guess for decoding |

---

## ⚠️ Limitations

- Audio decoding accuracy depends on:
  - Noise levels
  - Signal clarity
  - Consistent timing
- Microphone decoding may vary by device/browser
- Extremely fast or irregular Morse may not decode perfectly

---

## 📄 License

© 2026 Lassens.IT  
All rights reserved unless otherwise specified.

---

## 👨‍💻 Author

**Jeffrey Lassen**  
Version: `1.0.9`  
Last Updated: `05/03/2026`
