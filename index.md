# Privacy Policy — Signal Lost

**Effective date:** June 15, 2026
**Last updated:** November 5, 2026

Signal Lost is an iOS narrative game published by Thomas Masters. This policy explains what data the app handles, what leaves your device, and what does not.

If you have questions, contact: **tmasters2876@gmail.com**

---

## Summary

- Signal Lost does **not** require an account, sign-in, or any personal information.
- Almost everything happens on your device. Game progress, journal entries, conversations, and notification scheduling are stored locally and never sent anywhere.
- Since version 1.3, **nothing you type ever leaves your device**. Every radio reply in the game is scripted and stored in the app. (Earlier versions had an AI reply feature on a few frequencies; see "Versions before 1.3" below.)
- We do **not** collect analytics, advertising identifiers, location, contacts, or any tracking data of any kind.
- There are no subscriptions and no third-party SDKs. The only purchases are optional tips ("Support the Station"), processed entirely by Apple.

---

## What stays on your device

The following information is created and stored entirely on your iPhone or iPad. It is never transmitted off-device by the app:

- Your game state (story progress, beat indices, world flags)
- Your transmission log (messages you send and receive)
- Your journal entries
- The list of contacts you've encountered (Elias, June, etc.)
- The schedule of upcoming in-game radio signal windows
- iOS notification preferences and pending local notifications
- Settings such as static muting

This information is stored using Apple's SwiftData framework in the app's private sandbox. It is included in iCloud device backups if you have those enabled, but only to the extent Apple's standard backup behavior applies — we receive nothing.

---

## What the app sends off-device

**Signal Lost 1.3 and later:** the game itself makes no network calls. Every radio frequency, including 47.2, 55.5, 63.8 and 88.1 MHz, answers with scripted content stored inside the app.

The only things that involve Apple's servers are features Apple runs for you:

- **Tips ("Support the Station"):** optional purchases processed by Apple through the App Store. We never see your payment information; the app only learns whether a purchase succeeded. Apple's handling is covered by Apple's Privacy Policy.
- **Game Center:** if you are signed in to Game Center, your achievements are reported to Apple's Game Center service under Apple's Privacy Policy. We do not receive your Game Center identity. If you are not signed in, nothing is sent and the game plays the same.

### Versions before 1.3

Earlier versions (up to 1.2) had an **AI radio reply** feature on 47.2, 55.5, 63.8 and 88.1 MHz, capped at 2 replies per frequency. When you transmitted on one of those frequencies, the app sent the text you typed, the frequency, a short character description chosen by us, and up to the last 2 exchanges on that frequency over HTTPS to a Cloudflare Worker we operated, which forwarded it to **Anthropic's Claude API** for a reply. The Worker kept no logs of message content; Anthropic processed the text under its own [privacy policy](https://www.anthropic.com/legal/privacy). Version 1.3 removed this feature completely. If you are still on an older version, updating stops all of it.

---

## What we do NOT collect

We want to be specific about this because most apps collect at least one of these. Signal Lost collects **none** of:

- Your name, email, phone number, or any contact information
- Your Apple ID, sign-in credentials, or any account identifier
- IDFA, IDFV, or any advertising or tracking identifier
- Device fingerprinting data
- Crash logs (Apple's standard system-level crash reporting may apply if you have opted in to share with developers via iOS Settings, but Signal Lost does not embed any third-party crash SDK)
- Analytics events, screen views, session duration, retention metrics, or behavioral data
- Your location, even coarse
- Access to your contacts, photos, microphone, camera, calendar, reminders, or health data
- Voiceprint, biometric, or audio recordings of any kind

There are no third-party advertising networks, no analytics SDKs (no Firebase, no Mixpanel, no Amplitude, no Google Analytics), and no embedded tracking pixels.

---

## Notifications

Signal Lost asks permission to send notifications so it can alert you when an in-game radio transmission window opens or is about to close. These notifications are scheduled **locally on your device** using Apple's `UNUserNotificationCenter`. There is no remote push server, no APNs token sent anywhere, and no notification analytics. If you decline notification permission, the game still works — you'll just see new content the next time you open the app.

---

## Background activity

Signal Lost requests Apple's standard `fetch` and `processing` background modes so it can advance in-game time and fire narrative events even while you are not in the app. This background activity is local-only and does not transmit anything off-device.

---

## Children

Signal Lost is rated 12+ on the App Store and is not directed at children under the age of 13. We do not knowingly collect any information about children, but the app does not request personal information from anyone of any age, so this distinction is largely moot in practice.

---

## Your rights and choices

Because Signal Lost stores all your data on your device, you control it directly:

- **Delete all game data:** Open the app → Settings → DANGER → RESET STATION. This permanently wipes your save.
- **Stop all data transmission:** Update to version 1.3 or later, which sends nothing off-device. Notifications are local and can be turned off in iOS Settings → Signal Lost.
- **Remove the app entirely:** Delete it from your home screen. All on-device storage is removed by iOS as part of the standard uninstall.

If you transmitted on an AI frequency in a version before 1.3 and want any remaining short-term request logs removed, email **tmasters2876@gmail.com** and we will remove them as soon as reasonably possible.

---

## Third parties

Signal Lost 1.3 and later shares no data with any third party. Apple processes tips and Game Center as described above, under Apple's own policies.

Versions before 1.3 shared typed messages on the AI frequencies with **Cloudflare, Inc.** ([privacy policy](https://www.cloudflare.com/privacypolicy/)), which ran the proxy, and **Anthropic, PBC** ([privacy policy](https://www.anthropic.com/legal/privacy)), which generated the replies.

We do not sell, rent, lease, or otherwise share any user data with any other party, ever, for any purpose. There is no advertising network. There is no data broker relationship.

---

## Changes to this policy

If we change how the app handles data, we will update this page and revise the "Last updated" date at the top. For significant changes, we'll also update the app's description on the App Store. Continued use of the app after a change indicates acceptance of the revised policy.

---

## Contact

For privacy questions, data deletion requests, or any other concerns related to Signal Lost:

**Email:** tmasters2876@gmail.com
**Developer:** Thomas Masters

This page is the canonical privacy policy for Signal Lost and is referenced from the app's App Store listing.
