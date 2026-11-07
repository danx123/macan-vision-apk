# Macan Vision — Official Release

<p align="center">
  <strong>Global Free-to-Air Live TV & Online Radio Streaming Player for Android</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Release-v1.2.6-FF9E0B?style=for-the-badge" alt="Release Version" />
  <img src="https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Platform" />
  <img src="https://img.shields.io/badge/Architecture-Jetpack%20Compose-4285F4?style=for-the-badge" alt="Jetpack Compose" />
  <img src="https://img.shields.io/badge/Engine-Media3%20ExoPlayer-00E5FF?style=for-the-badge" alt="Media3 ExoPlayer" />
</p>

---

<img width="2176" height="1600" alt="vision-mobile" src="https://github.com/user-attachments/assets/9fcee6a5-dcf5-461c-b619-91511973287d" />

---

## Overview

**Macan Vision** is a modern, high-performance multimedia broadcast player designed for Android. Built with a signature dark cinematic aesthetic ("Tiger Amber" & "Obsidian Surface"), it delivers seamless access to thousands of public television channels and international radio stations worldwide without requiring subscriptions or hardware antennas.

Powered by Google's **AndroidX Media3 (ExoPlayer)** and an integrated **hardware-accelerated Audio FX DSP suite**, Macan Vision ensures low-latency playback, resilient auto-reconnect logic, background playback handling, and granular sound tailoring.

---

## Key Highlights & Features

### 📺 Live Television Streaming
- **Broad Directory:** Access thousands of global and regional Free-to-Air (FTA) channels organized by category (News, Sports, Entertainment, Movies, Music, Kids, Religious, and General).
- **Adaptive Resolution Detection:** Automatic stream tag extraction (e.g., `1080p`, `720p`) with customizable aspect-ratio switching (Fit vs. Zoom-fill).
- **Stream Resilience:** Adaptive load control buffer strategies optimized for live HTTP/HLS (`.m3u8`) and direct media streams with intelligent retry routines.

### 📻 Global Radio Hub
- **50,000+ Stations Worldwide:** Real-time directory query integration via the public Radio-Browser API, filterable by genre, station name, bitrate, and codec (AAC, MP3).
- **Real-Time Sound Visualizer:** Ambient audio visualization bar animations directly synchronized with live playback status.
- **Fail-Safe Offline Mode:** Curated fallback catalogs ensure playback even under constrained network connectivity.

### 🎛️ Studio-Grade Audio & DSP Suite
Directly communicates with the Android native hardware audio session:
- **5-Band Equalizer:** Fine-tune audio across 60 Hz, 230 Hz, 910 Hz, 3.6 kHz, and 14 kHz bands.
- **Tuned Presets:** Fast switching between *Normal, Pop, Rock, Jazz, Classical, Dance, Vocal, Bass Heavy,* and *Flat*.
- **Bass Boost:** Low-frequency enhancement up to 1000‰ strength.
- **3D Spatial Virtualizer:** Stereo soundstage simulation for headphones and external speaker systems.
- **Dynamic Normalization / ReplayGain:** Built-in loudness enhancer to balance high dynamic range streams and eliminate sudden volume spikes between channels.

### 📱 Lock Screen & Background Media Control
- Fully integrated with Android **MediaSession** and background foreground services.
- Rich lock-screen notification cards with live station logos, program status, playback controls, and dismiss actions.
- Full compatibility with Android 13+ runtime notification permissions (`POST_NOTIFICATIONS`).

### ⚡ Persistent Experience & Local Storage
- **Local Favorites:** Fast SQLite database powered by **Room** to bookmark favorite TV channels and radio stations.
- **Session Restoration:** Automatically restores your last chosen country filter, category selection, interface language, and currently playing stream on restart.
- **Bilingual Interface:** Instant real-time localization support between English and Indonesian with system auto-detect.

---

## Technical Specifications

| Component | Specification |
| :--- | :--- |
| **Minimum Android Version** | Android 7.0 (API level 24+) |
| **Target Android Version** | Android 14+ (API level 34+) |
| **UI Framework** | 100% Declarative Jetpack Compose (Material Design 3) |
| **Media Engine** | AndroidX Media3 ExoPlayer (`1.x`) |
| **Data Engine & Networking** | Retrofit 2, Moshi Kotlin, OkHttp 3 |
| **Local Persistence** | Jetpack Room SQLite Database |
| **Image Loading** | Coil Compose (with memory & disk caching) |
| **Theme & Design** | Obsidian Cinema (`#0B0E14`), Tiger Amber (`#FF9E0B`), Electric Cyan (`#00E5FF`) |

---

## Permission Disclosures

Macan Vision requests only essential permissions required to deliver real-time streaming services:

- `android.permission.INTERNET`: Required to fetch stream directories and decode live media over HTTP/HTTPS.
- `android.permission.ACCESS_NETWORK_STATE`: Monitors connection changes to handle smooth reconnects.
- `android.permission.FOREGROUND_SERVICE` & `FOREGROUND_SERVICE_MEDIA_PLAYBACK`: Keeps radio broadcasts running uninterrupted when multitasking or when the screen is locked.
- `android.permission.POST_NOTIFICATIONS`: Displays active player controls on the notification shade and lock screen (Android 13+).
- `android.permission.WAKE_LOCK`: Prevents CPU deep sleep during continuous live audio playback.
- `android.permission.MODIFY_AUDIO_SETTINGS`: Routes sound through the hardware equalizer, virtualizer, and loudness DSP.

---

## Legal & Public Stream Disclaimer

Macan Vision operates exclusively as an open-source media player and aggregator:
1. Macan Vision does **not** host, store, re-broadcast, or distribute any proprietary audio or video content.
2. Channel lists and radio indexes are queried from publicly accessible directories (such as public IPTV-org registries and community-maintained Radio-Browser indices).
3. All broadcast trademarks, channel names, station logos, and streams belong exclusively to their respective copyright holders. If you are a copyright holder wishing to report or exclude any public index link, please submit a request to the upstream public directory maintainers.
