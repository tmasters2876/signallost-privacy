# Privacy Policy — Signal Lost

**Effective date:** June 15, 2026
**Last updated:** June 15, 2026

Signal Lost is an iOS narrative game published by Thomas Masters. This policy explains what data the app handles, what leaves your device, and what does not.

If you have questions, contact: **tmasters2876@gmail.com**

---

## Summary

- Signal Lost does **not** require an account, sign-in, or any personal information.
- Almost everything happens on your device. Game progress, journal entries, conversations, and notification scheduling are stored locally and never sent anywhere.
- A small number of in-game radio frequencies use an **AI-generated response** feature. When you transmit on those frequencies, your typed message is sent to a server we operate, forwarded to Anthropic's Claude API to generate a reply, and the reply is sent back to your device.
- We do **not** collect analytics, advertising identifiers, location, contacts, or any tracking data of any kind.
- There are no in-app purchases, no subscriptions, and no third-party SDKs aside from the AI proxy described below.

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

## What the app sends off-device, and only when you trigger it

The only feature that transmits data off-device is the **AI radio reply** feature on a small set of in-game frequencies (currently 47.2, 55.5, 63.8, and 88.1 MHz, capped at 2 calls per frequency per playthrough).

When you tap **TRANSMIT** on one of those frequencies, the app sends the following over HTTPS to a Cloudflare Worker we operate at a private URL:

- The text you typed
- A short character description (a "persona" prompt that tells the AI how to respond — chosen by us, not by you)
- The radio frequency value (e.g., `47.2`)
- Up to the last 2 exchanges of dialog on that frequency, so the AI has short conversational context (we keep at most 4 messages of history per frequency on your device, then drop the oldest)

The Cloudflare Worker forwards the same data to **Anthropic's Claude API**, receives a text reply, and returns it to your device. The Worker does this exclusively to keep the Anthropic API key off the app binary; it does **not** retain logs of message content for analytics, advertising, or any other purpose. Standard short-term server logs (timestamps, response codes) are retained only as long as needed to operate the service and are not associated with any personal identifier.

**Important:** Anthropic processes the message text under its own privacy policy and terms. Anthropic's policies are available at [anthropic.com/legal/privacy](https://www.anthropic.com/legal/privacy). We do not control Anthropic's data practices.

If you do not want any of your text leaving your device, simply do not transmit on the AI-enabled frequencies. All other radio frequencies use locally-stored scripted content and never trigger a network call.

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
- **Stop all data transmission:** Avoid transmitting on the AI-enabled frequencies (47.2, 55.5, 63.8, 88.1 MHz). Or disable notifications in iOS Settings → Signal Lost.
- **Remove the app entirely:** Delete it from your home screen. All on-device storage is removed by iOS as part of the standard uninstall.

If you've previously transmitted on an AI frequency and want the Cloudflare Worker's short-term logs of your IP-level request metadata removed, email **tmasters2876@gmail.com** and we will remove them as soon as reasonably possible.

---

## Third parties

We share data with exactly two third parties, and only when you trigger an AI-enabled transmission:

1. **Cloudflare, Inc.** — operates the Worker that proxies AI requests. Cloudflare's privacy policy: [cloudflare.com/privacypolicy](https://www.cloudflare.com/privacypolicy/)
2. **Anthropic, PBC** — operates the Claude AI model that generates the reply text. Anthropic's privacy policy: [anthropic.com/legal/privacy](https://www.anthropic.com/legal/privacy)

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
