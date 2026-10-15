---
layout: default
title: Privacy Policy
permalink: /privacy
---

# PowerME — Privacy Policy

**Effective date:** 2026-04-27  
**Last updated:** 2026-10-15

This revision corrects section 2.2 to list all the data synced to Firebase Firestore, corrects section 2.7 to say which Health Connect data is synced, updates section 2.5 to match what the AI features send, and adds to section 2.5 how Google may use the data sent to the Gemini API.

---

## 1. Who We Are

PowerME is a fitness and workout tracking application developed by Omer Hedvat ("we", "us", "our"). For questions or concerns, contact us at **powerme.support@gmail.com**.

---

## 2. Information We Collect

### 2.1 Account Information (Firebase Auth)

When you sign in, we collect:
- **Email/password sign-in:** your email address and a hashed password managed by Firebase Auth.
- **Google Sign-In:** your Google email address, display name and profile photo URL, provided by Google's Credential Manager.

We do not store your password. Firebase Auth handles credential storage and authentication.

### 2.2 Workout and Profile Data (Firebase Firestore)

If you are signed in, the following data is synced to Firebase Firestore so that you can use it on other devices and restore it after a reinstall:

- **Profile data:** email address, name, birth year, height, weight, body fat percentage, gender, occupation type, average sleep hours, training goals, experience level, training days per week, preferred training days, and your free-text goal notes. If you connect Health Connect, the height, weight and body fat percentage values the app reads from it update these profile fields.
- **Workouts:** routine name, start and end time, duration, total volume and notes. For each set: the exercise name and equipment, set type, weight, reps, RPE, distance, time, rest duration, set notes, superset and block grouping, and start and end time. For timed or interval blocks (for example AMRAP, EMOM or Tabata): the block settings, rounds and round times, RPE and block notes.
- **Routines and workout templates:** the routine name and when you last performed it; the exercises and their order, target sets, reps, weights, rest times and distances, sticky notes, progression settings, and block structure.
- **Custom exercises you create:** name, muscle group, equipment, exercise type, and movement classification (joints and movement pattern).
- **Body measurement history:** a dated log of the weight, body fat percentage and height values you enter. If you connect Health Connect, the weight, height and VO₂ Max values the app reads from it are also added to this log.
- **Routine scores:** the results of routine scoring and the inputs saved with them (see 2.5).
- **Settings and preferences:** available plates, rest-timer sound and vibration, theme, unit system, daily step target, keep-screen-on, RPE mode, timed-set setup time, language, timer sound and workout style.

Your injury records are stored only on your device and are not synced. Routine scores do, however, include the lists of exercises flagged because of your injuries (see 2.5).

If you are not signed in, your workout and profile data stays in a local database on your device and is not synced.

### 2.3 Crash and Diagnostic Data (Firebase Crashlytics)

We collect crash reports linked to your Firebase UID to diagnose and fix bugs. Crash reports include stack traces, device model, OS version and app version. No workout content or health values are included in crash reports.

### 2.4 Usage Analytics (Firebase Analytics)

We collect anonymised usage events to understand how the app is used. Examples: workout started, workout finished, screen viewed. **We do not send health metrics, exercise weights, reps, RPE values, or any personally identifying data to Firebase Analytics.**

### 2.5 AI Features (Google Gemini API)

Several features in PowerME work by sending data to Google's Gemini API in the cloud. **When you use these features, health and fitness information about you, including your injuries, your age, gender and self-reported sleep hours, and your workout performance, is sent to Google, a third party, so that the feature can produce its result.** The lists below say what each feature sends and whether it runs only when you ask for it or on its own.

**Features that run only when you tap a button:**

- **Workout parsing.** When you type or dictate a workout and ask the app to read it, the text you entered is sent. If you ask the app to generate a workout in conversation, the free-text training-focus note from your profile is sent as well.
- **Translation.** This is part of workout parsing. If the text you entered is not in English, the full text is first sent to be translated. You do not choose this separately; it happens whenever you parse non-English text.
- **Workout photo scanning.** The photograph you take of a workout is sent as an image (see 2.6).
- **Routine scoring.** When you ask the app to score routines, it sends your age, gender, self-reported average sleep hours, experience level and training days per week; your goals and free-text training note; the full structure of the routines being scored; your recent adherence percentages; and the reasoning text and severity score that the injury classification feature (below) produced about your injuries. The app asks for your consent once before the first use of this feature.

**Features that run automatically, without a button press:**

- **Injury classification.** When you save an injury, its free-text description, the joints affected and the severity are sent, together with the names of candidate exercises, so that the app can mark exercises as safe or to be avoided. **This happens at every severity, including mild.** It runs in the background after you save.
- **Performance report.** After a workout, your goals and, for each exercise, planned and actual reps, planned and actual weight, RPE, time under tension and a computed verdict are sent so that the report can be written in plain language.
- **Post-workout insight.** After an interval or metcon-style block (for example AMRAP, EMOM or Tabata), the workout type, duration, per-round times, your RPE ratings, the names of exercises from earlier blocks and a pacing score are sent. No Health Connect data is included (see 2.7).

**What we keep.** We do not keep a log of the text, photographs or other content sent to Gemini. Two sets of results are saved, because the app needs them again later:

- **Exercise classifications produced from your injuries.** These stay on your device and are not uploaded.
- **Routine scores.** These are saved together with the inputs used to produce them (your goals, the names and weekly frequency of the routines scored, and the lists of exercises flagged because of your injuries) and sync across your devices through Firebase Firestore.

**Which API key is used, and what Google may do with the data.** By default, the AI features use a Gemini API key that we provide. That key is on Google's free tier: it is not linked to a billing account. For free-tier use, Google's [Gemini API Additional Terms](https://ai.google.dev/gemini-api/terms) allow Google to use the content sent to Gemini, and the responses, to provide, improve and develop its products, services and machine learning technologies, and human reviewers may read and annotate that content. Google says it disconnects this data from the Google Account, API key and Cloud project before reviewers see it.

You can instead enter your own Gemini API key in the app's settings. The app then sends the same data described above using your key, and the key you provided is used instead of ours. How Google handles that data depends on your key's tier under the same terms: for a key linked to an active billing account (a paid key), Google states that it does not use your prompts or responses to improve its products; for a free-tier key of your own, the free-tier terms above apply. When you enter your own key, the app sends the fixed word "hi" to check that the key works. No personal data is included in that check.

Google's data handling is governed by [Google's Privacy Policy](https://policies.google.com/privacy).

### 2.6 Workout Photo Scanning (Google Gemini API)

When you scan a workout photo, the photograph itself is sent to Google's Gemini API as an image and read there. The image is not processed on your device.

**Correction.** A previous version of this policy stated that photo scanning used Google's ML Kit Text Recognition SDK and that processing happened entirely on-device, with no image data leaving your phone. That is no longer accurate. The app does not use ML Kit; photos you scan are sent to Google as described in 2.5.

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

**Some Health Connect data is synced to Firestore.** If you are signed in, the weight, height and body fat percentage values the app reads from Health Connect update your profile, and the weight, height and VO₂ Max values it reads are added to your body measurement history. Both are synced to Firebase Firestore with the rest of your account data (see 2.2). The other Health Connect data types in the table above stay on your device and are not synced to our servers or to Firestore. Apart from this sync, no Health Connect data leaves your device, and none of it is sent to Google's Gemini API.

Deleting data in the Health Connect app does not remove values already synced to your PowerME account; deleting your account removes them (see 5). Data stored in Health Connect remains under your control through the Health Connect app.

---

## 3. How We Use Your Information

- To provide core app functionality (tracking workouts, displaying trends, syncing data across your devices).
- To restore your data if you reinstall or switch devices.
- To provide AI features (workout parsing and translation, photo scanning, injury classification, performance reports, post-workout insights and routine scoring), which send the data described in section 2.5 to Google's Gemini API.
- To diagnose crashes and fix bugs.
- To understand aggregate usage patterns and improve the app.

We do not sell or rent your personal data. We share it with third parties only as described in this policy: with Google's Firebase services for sign-in, sync, crash reporting and analytics, and with Google's Gemini API for the AI features described in section 2.5, which includes health and fitness information such as your injuries, age, sleep hours and workout performance.

---

## 4. Data Retention

- **Firestore data** is retained until you delete your account.
- **Health Connect data** is stored on your device by the Health Connect platform. Uninstalling PowerME does not delete Health Connect data; use the Health Connect app to manage or delete it.
- **Crashlytics data** is retained for 90 days per Firebase's standard policy.
- **Analytics data** is aggregated and anonymised; individual events expire per Firebase's standard retention policy.

---

## 5. Account Deletion

You can delete your account at any time from **Profile → Danger Zone → Delete Account**. Deletion:
1. Permanently deletes all data in your Firestore subtree: everything listed in section 2.2 (profile, workouts, routines, custom exercises, body measurement history, routine scores, and settings and preferences).
2. Deletes your Firebase Auth user record.
3. Wipes the local database on the current device.

Deletion is irreversible and immediate. Health Connect data is unaffected and must be managed separately through the Health Connect app.

---

## 6. Third-Party Services

| Service | Purpose | Privacy Policy |
|---|---|---|
| Firebase Auth | Authentication | [Google Privacy Policy](https://policies.google.com/privacy) |
| Firebase Firestore | Cloud data storage | [Google Privacy Policy](https://policies.google.com/privacy) |
| Firebase Crashlytics | Crash reporting | [Google Privacy Policy](https://policies.google.com/privacy) |
| Firebase Analytics | Usage analytics | [Google Privacy Policy](https://policies.google.com/privacy) |
| Google Gemini API | AI features: workout parsing and translation, photo scanning, injury classification, performance reports, post-workout insights, routine scoring | [Google Privacy Policy](https://policies.google.com/privacy) |
| Android Health Connect | Health data platform | [Google Privacy Policy](https://policies.google.com/privacy) |

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
