# Privacy Policy — Mobil Anons

**Last updated:** 2026-07-12 (v1.0 — Google Play compliance update)  
**Developer:** Ar-Se Soft Teknoloji  
**Contact:** info@arsesoft.com  
**App package:** `com.aob.mobilanons`

---

## 1. Overview

Mobil Anons ("the App") is an Android application that provides voice announcements for earthquake alerts, weather briefings, blood donation requests, and custom messages. This Privacy Policy explains what information the App accesses, why it needs it, and how it is handled.

> **Short version:** The App does not collect, store, transmit, or share any personal data with the developer or any third party.

---

## 2. Permissions Used

### 2.1 `INTERNET`
**Why:** Required to fetch live earthquake data from Kandilli Observatory and current weather data from Open-Meteo. All network requests are outbound only — no data is sent to our servers.

### 2.2 `ACCESS_NETWORK_STATE`
**Why:** Used to check whether a network connection is available before attempting to fetch earthquake or weather data, preventing unnecessary error states.

### 2.3 `FOREGROUND_SERVICE`
**Why:** The text-to-speech (TTS) announcement service runs as a foreground service to ensure audio playback is not interrupted when the app is in the background or the screen is off.

### 2.4 `FOREGROUND_SERVICE_MEDIA_PLAYBACK`
**Why:** Required on Android 14+ to declare the specific foreground service type for audio playback. This grants the TTS service permission to play audio while running in the foreground.

### 2.5 `POST_NOTIFICATIONS`
**Why:** Required on Android 13+ (API 33+) to display push notifications for earthquake alerts and the persistent notification that accompanies the foreground TTS service while an announcement is playing.

### 2.6 `RECEIVE_BOOT_COMPLETED`
**Why:** Used to resume background earthquake monitoring and hourly weather announcements after a device restart. If the user has enabled these background features in the app settings, the app restarts those monitoring tasks automatically on boot. No monitoring runs unless explicitly enabled by the user.

### 2.7 `VIBRATE`
**Why:** Used to vibrate the device when an earthquake alert notification is sent.

---

## 3. Data We Do NOT Collect

The App does **not** collect, store, or transmit:

- Personal identification information (name, email, phone number, address)
- Location data (GPS coordinates or network-based location)
- Device identifiers (IMEI, Android ID, advertising ID)
- Usage analytics or crash reports sent to our servers
- Contacts, call logs, messages, or any other sensitive device data
- Audio recordings or microphone data

---

## 4. Background Processing

The App offers two optional background features that run even when the App is closed:

- **Background Earthquake Monitoring:** When enabled, the App queries Kandilli Observatory every 15 minutes using Android WorkManager. If a new earthquake meeting the user's magnitude threshold is detected, a push notification is sent and, if TTS alerts are enabled, the earthquake is announced via the device speaker.
- **Hourly Weather Announcements:** When enabled, the App fetches the current weather for the saved city at the top of every hour and reads it aloud via the TTS engine.

Both features are **disabled by default** and can be toggled on or off at any time from within the App. Neither feature transmits personal data.

---

## 5. Third-Party Services

The App communicates with the following external services. Please review their privacy policies:

| Service | Purpose | Privacy Policy |
|---|---|---|
| [Open-Meteo](https://open-meteo.com/) | Weather data | [open-meteo.com/en/terms](https://open-meteo.com/en/terms) |
| [Kandilli Observatory](http://koeri.boun.edu.tr/) | Earthquake data | Boğaziçi University institutional policy |

These services receive only the technical data required to fulfil the request (e.g., city name for weather lookup). No personal user data is attached to these requests.

---

## 6. Data Storage

All user preferences (city name, magnitude threshold, monitoring toggle states) are stored **locally on the device** using Android SharedPreferences. This data never leaves the device and is deleted when the app is uninstalled.

Earthquake monitoring settings (`earthquake_prefs`) and weather settings (`weather_prefs`) are excluded from Android cloud backup and device-to-device transfer to prevent unintentional background processes from being activated on a new device without explicit user consent.

---

## 7. Children's Privacy

The App does not knowingly collect any data from users under the age of 13. If you believe a child has provided personal information through the App, please contact us immediately.

---

## 8. Changes to This Policy

We may update this Privacy Policy from time to time. Any changes will be reflected by the "Last updated" date at the top of this document. Continued use of the App after changes constitutes acceptance of the updated policy.

---

## 9. Contact Us

If you have any questions or concerns about this Privacy Policy, please contact:

**Ar-Se Soft Teknoloji**  
📧 info@arsesoft.com  
🌐 https://arsesoft.com  
🔒 https://arsesoft.com/mobilanons/privacy
