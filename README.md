# 🦖 Bruce 2.0 Ultra Suite & Studio for M5Stack Cardputer ADV

![Bruce 2.0 Banner](https://img.shields.io/badge/Platform-ESP32--S3-orange?style=for-the-badge&logo=espressif)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![Build](https://img.shields.io/badge/Build-PlatformIO-green?style=for-the-badge&logo=platformio)
![Theme](https://img.shields.io/badge/Theme-Dino%20%2F%20Schnabeltier-yellow?style=for-the-badge)

**Bruce 2.0 Ultra** is a massive, feature-packed firmware evolution for the **M5Stack Cardputer ADV** (ESP32-S3). Designed for portable pentesting, RF analysis, hardware debugging, and seamless offline mesh communication — packed into a custom **Dino & Schnabeltier Pixel-Art Aesthetic**.

Together with **Bruce 2.0 Studio** (Desktop Companion App), flashing, managing, and remotely controlling your Cardputer has never been easier.

---

## 🌟 Key Features

### 📡 Wireless & RF Suite (Wi-Fi, BLE, Sub-GHz, NRF24)
* **Wi-Fi PCAP Logger:** Promiscuous-mode sniffing saved directly to SD card (`.pcap` format, Wireshark compatible).
* **Wi-Fi Channel Occupancy Monitor:** Visual live dashboard showing 2.4 GHz channel usage (Channels 1–13).
* **Probe Request Counter & Vendor Lookup:** Passive device tracker with offline OUI database matching via SD card.
* **Sub-GHz Waterfall Spectrogram:** Real-time 433 MHz / 868 MHz signal analysis using CC1101.
* **NRF24 Multi-Channel Sweeper:** Passive 2.4 GHz RF scanner and interference detection.

### 💬 ESP-NOW Mesh 2.0
* **Background Processing:** Multi-threaded core task keeping message reception active system-wide.
* **Status Bar Notifications:** Global unread message indicator (letter icon) in the header bar.
* **Direct Messaging & User Identities:** Set custom nicknames and maintain a local contact list.
* **Typing Indicators & AES-128 Encryption:** Live *"Name is typing..."* status and optional pre-shared key encryption.
* **Flicker-Free UI:** Double-buffered chat interface (`TFT_eSprite`) with text wrapping and vertical scrolling.

### 🔌 Hardware Lab & System Utilities
* **I2S Microphone Oscilloscope & FFT:** Live visual waveform and frequency spectrum plot.
* **GPIO Mini Logic Analyzer & Volt-Meter:** Real-time digital pin state graphing and analog voltage measurements.
* **UART Serial Bridge & Interceptor:** Hardware terminal interface for external microcontrollers.
* **SD File Manager & Hex Editor:** Browse, view hex dumps, and edit text files (`nano.cpp`) directly on device.
* **Dynamic CPU Scaling & Battery Profiler:** Switch between 80 / 160 / 240 MHz to balance performance and battery life.

---

## 💻 Bruce 2.0 Studio (Desktop Companion App)

The repository includes cross-platform desktop companion software:

* ⚡ **1-Click WebSerial Flasher:** Connect via USB-C and flash the latest GitHub release directly without compiling.
* 🛠️ **Automated SD Card Setup:** One-click directory initialization (`theme.json`, assets, pcap folders).
* 🖥️ **Live Screen Mirroring & Virtual Keyboard:** Remote control your Cardputer and stream its TFT display to your PC.
* 🎨 **Visual Theme Editor:** Customize UI colors (`0x4FE0` Dino Green / `0xFFE0` Schnabeltier Yellow) via a GUI color picker.
* 📁 **PCAP & Log Extractor:** Easily pull Wi-Fi packet dumps and sub-GHz logs directly to your desktop.


🛠️ Build & Installation
Option 1: Via Bruce Studio (Recommended)
Download Bruce 2.0 Studio from the Releases page.

Plug in your M5Stack Cardputer ADV via USB-C.

Click "Flash Latest Release" and follow the SD Card Setup Wizard.

Option 2: Build from Source (PlatformIO)
Bash
# Clone the repository
git clone [https://github.com/YOUR_USERNAME/bruce-2.0-ultra.git](https://github.com/YOUR_USERNAME/bruce-2.0-ultra.git)
cd bruce-2.0-ultra

# Build firmware for Cardputer
pio run -e cardputer

# Flash to device
pio run -e cardputer -t upload
