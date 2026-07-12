# 📢 Mobil Anons

<p align="center">
  <img src="img/1024.png" width="120" alt="Mobil Anons Logo" />
</p>

<p align="center">
  <strong>Your voice on the airwaves — earthquake alerts, weather briefings, blood donation calls & custom announcements, all in one app.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Android-green?logo=android" />
  <img src="https://img.shields.io/badge/Min%20SDK-24-blue" />
  <img src="https://img.shields.io/badge/Target%20SDK-35-blue" />
  <img src="https://img.shields.io/badge/Language-Kotlin-orange?logo=kotlin" />
  <img src="https://img.shields.io/badge/License-MIT-lightgrey" />
</p>

---

## ✨ What is Mobil Anons?

**Mobil Anons** is the official Android companion to the *Anons Sistemi* desktop application by **Ar-Se Soft Teknoloji**. It brings the same powerful voice announcement features that amateur radio operators and emergency coordinators rely on — right to their Android device.

Whether you are monitoring seismic activity, broadcasting live weather conditions, requesting urgent blood donations, or simply need to push a custom voice message over the air — Mobil Anons keeps you connected and informed.

---

## 🚀 Features

| Feature | Description |
|---|---|
| 🌍 **Earthquake Monitor** | Live earthquake data from Kandilli Observatory. Filter by minimum magnitude and announce any event with one tap. |
| 🔔 **Background Earthquake Alerts** | Optional background monitoring — Kandilli is queried every 15 minutes. Push notification (and optional TTS announcement) sent automatically when a new earthquake exceeds your magnitude threshold. Resumes after device reboot. |
| 🌤 **Weather Briefings** | Real-time weather from Open-Meteo for any city. Temperature, feels-like, humidity and wind speed — all in a single card. |
| 🕐 **Hourly Weather Announcements** | Optional background worker that announces the current weather via TTS at the top of every hour. |
| 🩸 **Blood Donation Alerts** | Instantly announce urgent blood group needs with hospital name and contact information. |
| 📢 **Manual Announcements** | Type any text and have it read aloud in natural Turkish speech using Android's built-in TTS engine. |
| ℹ **About** | Credits for Ar-Se Soft and Amatör Telsizcilik. Theme switcher (light / system / dark). |

---

## 📱 Screenshots

> *Coming soon — screenshots will be added before Play Store release.*

---

## ✅ Google Play Compliance

| Check | Status |
|---|---|
| compileSdk / targetSdk = 35 | ✓ |
| minSdk = 24 (Android 7.0) | ✓ |
| No analytics or ad SDKs | ✓ |
| Cleartext HTTP only for Kandilli (no HTTPS available) | ✓ |
| All permissions declared and justified | ✓ |
| Foreground service type declared (`mediaPlayback`) | ✓ |
| `POST_NOTIFICATIONS` runtime permission request | ✓ |
| Background workers started via `ContextCompat.startForegroundService()` | ✓ |
| Notification small icon uses `drawable` (not `mipmap`) | ✓ |
| SharedPreferences excluded from cloud backup (`backup_rules.xml`) | ✓ |
| Android 12+ data extraction rules (`data_extraction_rules.xml`) | ✓ |
| Privacy policy linked in app (Hakkında screen) | ✓ |
| Release build: minifyEnabled + ProGuard | ✓ |

---

## 🔧 Technical Details

- **Package:** `com.aob.mobilanons`
- **Compile SDK:** 35
- **Min SDK:** 24 (Android 7.0 Nougat)
- **Target SDK:** 35
- **Language:** Kotlin
- **Architecture:** Single-Activity + Navigation Component + ViewBinding
- **TTS Engine:** Android TextToSpeech (`tr-TR` locale, 0.9× rate)
- **Weather API:** [Open-Meteo](https://open-meteo.com/) (free, no key required)
- **Earthquake Data:** [Kandilli Observatory](http://koeri.boun.edu.tr/) — HTML scraping via OkHttp

---

## 📦 Build & Install

1. Clone or download this repository
2. Open in **Android Studio Hedgehog** or newer
3. Let Gradle sync finish
4. Run on a device or emulator (API 24+)

```bash
# or via command line
./gradlew assembleDebug
```

---

## 🌐 Data Sources

| Source | Usage |
|---|---|
| [Kandilli Observatory](http://koeri.boun.edu.tr/) | Live earthquake list (last 500 events) |
| [Open-Meteo Geocoding](https://geocoding-api.open-meteo.com/) | City coordinate lookup |
| [Open-Meteo Forecast](https://api.open-meteo.com/) | Current weather conditions |

---

## 👥 Credits

| Name | Role |
|---|---|
| **Ar-Se Soft Teknoloji** | Original concept & development — [arsesoft.com](https://arsesoft.com) |
| **Amatör Telsizcilik** | Community partner — [@amator_telsizcilik](https://instagram.com/amator_telsizcilik) |

---

## 📄 License

This project is released under the [MIT License](LICENSE).

---

## 🔒 Privacy

See [PRIVACY_POLICY.md](PRIVACY_POLICY.md) for full details on what data is (and isn't) collected.

**Short version:** No personal data is collected, stored, or transmitted. All settings are stored locally on the device only. The app has no analytics, no crash reporting, and no ad SDKs.
