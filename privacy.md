---
layout: default
title: Privacy Policy
permalink: /privacy
---

# PowerME — Privacy Policy

**Effective date:** 2026-04-27  
**Last updated:** 2026-04-27

---

## 1. Who We Are

PowerME is a fitness and workout tracking application developed by Omer Hedvat ("we", "us", "our"). For questions or concerns, contact us at **powerme.support@gmail.com**.

---

## 2. Information We Collect

### 2.1 Account Information (Firebase Auth)

When you sign in, we collect:
- **Email/password sign-in:** Your email address and a hashed password managed by Firebase Auth.
- **Google Sign-In:** Your Google email address, display name, and profile photo URL, provided by Google's Credential Manager.

We do not store your password — Firebase Auth handles credential storage and authentication securely.

### 2.2 Workout and Profile Data (Firestore)

If you are signed in, the following data is synced to Firebase Firestore to enable cross-device access and backup:
- **Workouts:** exercises performed, sets, reps, weight, duration, RPE, and notes.
- **Routines and workout templates.**
- **Profile data:** date of birth, height, weight, body fat percentage, gender.
- **App settings:** workout style preference, unit system, timer configuration.

Signed-out users store all data locally on-device only (Room database). No data leaves the device without an account.

### 2.3 Crash and Diagnostic Data (Firebase Crashlytics)

We collect crash reports linked to your Firebase UID to diagnose and fix bugs. Crash reports include stack traces, device model, OS version, and app version. No workout content or health values are included in crash reports.

### 2.4 Usage Analytics (Firebase Analytics)

We collect anonymised usage events to understand how the app is used. Examples: workout started, workout finished, screen viewed. **We do not send health metrics, exercise weights, reps, RPE values, or any personally identifying data to Firebase Analytics.**

### 2.5 AI Workout Parsing (Gemini API)

When you use the AI workout import feature:
- Scanned OCR text from your workout photo or typed workout description is sent to Google's Gemini API in the cloud.
- Your personal exercise library (exercise names only, no weights or history) is included for context.
- **We do not persistently store the content sent to Gemini.** Google's data handling is governed by [Google's Privacy Policy](https://policies.google.com/privacy).

### 2.6 On-Device OCR (ML Kit Text Recognition)

Workout photo scanning uses Google's ML Kit Text Recognition SDK. This processing happens **entirely on-device** — no image data is sent to Google or any third party by ML Kit.

### 2.7 Health Connect Data

PowerME reads the following health data types from Android Health Connect, with your explicit permission:

| Data Type | Use |
|---|---|
| Weight | Display and trend charts |
| Body Fat | Display and trend charts |
| Height | BMI and profile display |
| Sleep Session | Sleep trend charts |
| Heart Rate Variability (HRV / RMSSD) | Recovery trend charts |
| Resting Heart Rate | Recovery trend charts |
| Steps | Activity trend charts |
| Heart Rate | Workout session context |
| Active Calories Burned | Workout and trend data |
| VO₂ Max | Fitness level trends |
| Distance | Workout session context |
| Oxygen Saturation (SpO₂) | Health trend charts |
| Respiratory Rate | Health trend charts |
| Exercise Session | Read + Write — records workouts to Health Connect |

**Health Connect data is read from and written to your device only. It is never uploaded to our servers, to Firestore, or to any third party.** Data stored in Health Connect remains under your control via the Health Connect app.

---

## 3. How We Use Your Information

- To provide core app functionality (tracking workouts, displaying trends, syncing data across your devices).
- To restore your data if you reinstall or switch devices.
- To diagnose crashes and fix bugs.
- To understand aggregate usage patterns and improve the app.

We do not sell, rent, or share your personal data with third parties except as described in this policy (Firebase, Google Gemini API).

---

## 4. Data Retention

- **Firestore data** is retained until you delete your account.
- **Health Connect data** is stored on your device by the Health Connect platform. Uninstalling PowerME does not delete Health Connect data; use the Health Connect app to manage or delete it.
- **Crashlytics data** is retained for 90 days per Firebase's standard policy.
- **Analytics data** is aggregated and anonymised; individual events expire per Firebase's standard retention policy.

---

## 5. Account Deletion

You can delete your account at any time from **Profile → Danger Zone → Delete Account**. Deletion:
1. Permanently deletes all data in your Firestore subtree (workouts, routines, settings, profile).
2. Deletes your Firebase Auth user record.
3. Wipes the local Room database on the current device.

Deletion is irreversible and immediate. Health Connect data is unaffected and must be managed separately via the Health Connect app.

---

## 6. Third-Party Services

| Service | Purpose | Privacy Policy |
|---|---|---|
| Firebase Auth | Authentication | [Google Privacy Policy](https://policies.google.com/privacy) |
| Firebase Firestore | Cloud data storage | [Google Privacy Policy](https://policies.google.com/privacy) |
| Firebase Crashlytics | Crash reporting | [Google Privacy Policy](https://policies.google.com/privacy) |
| Firebase Analytics | Usage analytics | [Google Privacy Policy](https://policies.google.com/privacy) |
| Google Gemini API | AI workout parsing | [Google Privacy Policy](https://policies.google.com/privacy) |
| Google ML Kit | On-device OCR | [Google Privacy Policy](https://policies.google.com/privacy) |
| Android Health Connect | Health data platform | [Android Privacy Policy](https://policies.google.com/privacy) |

---

## 7. Children's Privacy

PowerME is not directed to children under 13. We do not knowingly collect personal information from children under 13. If you believe a child under 13 has provided us with personal information, please contact us at powerme.support@gmail.com.

---

## 8. Security

We use industry-standard measures including Firebase's security infrastructure, encrypted transit (HTTPS/TLS), and Android's EncryptedSharedPreferences for sensitive local values. No method of transmission or storage is 100% secure.

---

## 9. Changes to This Policy

We may update this policy from time to time. The "Last updated" date at the top will reflect changes. Continued use of the app after changes constitutes acceptance of the updated policy.

---

## 10. Contact

Questions about this privacy policy? Email us at **powerme.support@gmail.com**.
