---
title: "Privacy Policy"
description: "How TapTab handles your information"
---

# Privacy Policy for TapTab

**Last updated:** April 30, 2026
**Effective date:** April 30, 2026

This Privacy Policy describes how TapTab ("**we**", "**us**", "**our**", or the "**App**") handles information when you use the TapTab mobile application on iOS or Android.

---

## Plain-language summary

- **TapTab keeps your data on your device.** There is no TapTab server, no user account, and no sign-up.
- The "owner profile" you set up — your name and one or more payment handles — lives only on your phone.
- **Receipt photos stay on your device.** Optical character recognition (OCR) runs locally; receipt text and bounding boxes are never uploaded by TapTab.
- **Payment requests are dispatched through third-party apps** (Venmo, PayPal, Zelle, Cash App). TapTab never sees, stores, or moves the actual money.
- **Sentry** receives anonymized crash reports so we can fix bugs — this is the only data that leaves your device, and only when a Sentry account has been configured for the app.
- TapTab charges **$0.50 per bill split** through Apple In-App Purchase or Google Play Billing. Apple and Google handle the transaction; we do not see your payment method.

---

## 1. Information we handle

### 1.1. Information you enter

When you set up your owner profile in TapTab, you may enter:

- Your name
- One or more payment handles you choose to share (Venmo username, PayPal email, Zelle phone or email, Cash App handle)

This information is stored on your device only, using the operating system's standard application storage (AsyncStorage on top of the iOS file system or Android SharedPreferences). It is **not** uploaded to any TapTab server, and there is no TapTab account or login.

### 1.2. Camera and photo library

When you scan a receipt, TapTab requests permission to:

- Take a photo with your camera, or
- Choose an existing photo from your photo library

**Receipt photos are processed entirely on your device.** Google ML Kit performs OCR locally to extract item names, prices, and bounding boxes. The photo and the OCR results are never uploaded to TapTab or any third-party server by us.

The photo is held in memory for the duration of one bill-splitting session and discarded when you finish or leave the flow. We do not save it to a cloud, mail it to a server, or share it with anyone.

### 1.3. Tap data and split calculations

While you and your friends tap items on the receipt, TapTab tracks which person tapped which items in temporary in-memory state. This data exists only for the duration of one session and is discarded when you complete or abandon the split. None of it is persisted on your device or transmitted.

### 1.4. Crash reports

TapTab includes the Sentry SDK to help us identify and fix bugs. When the app encounters an unexpected error and Sentry has been configured, Sentry collects:

- A stack trace of the error
- The version of the app
- Generic device information (model, operating system version)
- A short trail of session events leading up to the error (button taps, screen transitions, navigation actions)

Sentry is explicitly configured to **not capture screenshots**, because receipts may contain personal information. We do not log the contents of your owner profile, payment handles, receipt photos, OCR text, names of guests, or split calculations in crash reports.

If a Sentry account has not been configured at the time you install the app, no crash data is collected at all.

### 1.5. In-app purchase information

TapTab charges a $0.50 fee per bill split via Apple In-App Purchase (iOS) or Google Play Billing (Android). When you make a purchase:

- Apple or Google processes your payment using the payment method on your account
- TapTab receives confirmation that a purchase succeeded, but **does not see your payment method, billing address, or any financial details**
- Apple and Google retain transaction records per their own privacy policies for tax, refund, and audit purposes

---

## 2. Information we do NOT collect

To be explicit, TapTab does not collect:

- Email addresses, phone numbers, or postal addresses (other than what you voluntarily enter as a payment handle, which never leaves your device)
- Location data
- Advertising identifiers (IDFA, Advertising ID) for marketing purposes
- Analytics about your usage patterns (other than crash reports as described above)
- Contacts, calendar entries, microphone audio, or other phone data
- Any data about your guests — their names and payment handles entered during a split are never persisted to your device or transmitted

We do not sell your information to anyone, ever.

---

## 3. How we use information

The minimal data we touch is used only for these purposes:

| Data | Purpose |
|---|---|
| Owner profile (name, payment handles) | Pre-fill your details in outgoing payment requests |
| Receipt photo + OCR text | Show item bounding boxes so people can tap to claim items |
| Tap data | Calculate each person's share with proportional tax + tip |
| Crash reports (Sentry, if configured) | Diagnose and fix bugs |
| IAP confirmation | Verify a $0.50 split-pass purchase completed |

We do not use any of this data for advertising, profiling, or any purpose unrelated to the app's core function.

---

## 4. Third-party services

TapTab integrates with the third-party services below. When you interact with them, their privacy policies apply in addition to ours.

| Service | What it does | Privacy policy |
|---|---|---|
| Google ML Kit | On-device OCR. ML Kit does not transmit data during text recognition. | https://developers.google.com/ml-kit/terms |
| Sentry | Receives anonymized crash reports when configured. | https://sentry.io/privacy/ |
| Apple In-App Purchase | Processes the $0.50 split-pass purchase on iOS. | https://www.apple.com/legal/privacy/ |
| Google Play Billing | Processes the $0.50 split-pass purchase on Android. | https://policies.google.com/privacy |
| Venmo | Opened via deep link to send a payment charge. We pass a handle, amount, and note. | https://venmo.com/legal/us-privacy-policy |
| PayPal / PayPal.me | Opened via a web link to send a payment. | https://www.paypal.com/us/legalhub/privacy-full |
| Cash App | Opened via deep link to send a payment. | https://cash.app/legal/us/en-us/privacy |
| Zelle | Recipient information is shown in-app; Zelle has no deep-link integration. | https://www.zellepay.com/legal/privacy-policy |

---

## 5. Where your data lives

| Data | Location |
|---|---|
| Owner profile (name, payment handles) | Your device's app storage |
| Receipt photo | Your device's photo library and/or temporary app cache |
| Tap data, calculated shares, splits | In memory only, during a single session |
| Crash reports | Sentry servers (United States or EU), if Sentry is configured |
| Purchase records | Apple servers (iOS) or Google servers (Android) |

---

## 6. Data retention

- **Owner profile:** persists on your device until you delete it in the app or uninstall TapTab
- **Receipt photos and tap data:** discarded at the end of each session
- **Crash reports:** retained for 90 days by Sentry per its standard policy
- **Apple / Google purchase records:** retained per Apple's and Google's policies, typically several years for tax and refund purposes

---

## 7. Your rights and choices

### 7.1. Access and deletion

Because TapTab stores almost everything on your device, you control most of your data directly:

- **Delete your owner profile:** open TapTab and clear your profile in settings, or uninstall the app to remove all on-device data
- **Revoke camera or photo library permission:** in your device's system settings under "TapTab"
- **Delete crash reports:** email us with the subject line "Privacy — Crash Report Deletion" along with your device's general info, and we will request deletion from Sentry
- **Delete purchase records:** contact Apple or Google directly per their respective data deletion policies

### 7.2. California residents (CCPA / CPRA)

If you are a California resident, you have the right to know what personal information we collect, the right to delete it, the right to opt out of any sale or sharing of personal information, and the right to non-discrimination for exercising your privacy rights. **TapTab does not sell or share your personal information.** To exercise other rights, contact us at the email below.

### 7.3. Other U.S. state privacy laws

Residents of states with comprehensive privacy laws (currently including Virginia, Colorado, Connecticut, Utah, Texas, Oregon, Montana, and others) have rights similar to those described above. Contact us to exercise them.

### 7.4. European residents (GDPR / UK GDPR)

If you are in the European Economic Area, the United Kingdom, or Switzerland, you have the right to access, rectify, port, or delete your personal data, and to object to or restrict our processing. To exercise these rights, contact us at the email below.

The legal basis for our limited processing of crash reports is our legitimate interest in maintaining and improving the app's stability and security.

---

## 8. Children's privacy

TapTab is not directed to children under 13 (or under 16 in the European Economic Area, the United Kingdom, and Switzerland). We do not knowingly collect personal information from children. If you become aware that a child has provided information through TapTab, please contact us and we will take reasonable steps to remove it.

---

## 9. Security

TapTab maintains no servers, user accounts, or stored credentials, which substantially reduces the surface area for a data breach. Owner profile data is stored on your device using your operating system's standard application storage. Crash reports are transmitted to Sentry over HTTPS. In-app purchases are processed by Apple or Google over their own secure channels.

No system is perfectly secure; if you become aware of a vulnerability, please report it to the email below.

---

## 10. International users

TapTab is operated from the United States. If you use TapTab from outside the United States, please be aware that crash reports (if Sentry is configured) and purchase records (via Apple or Google) may be transferred to and processed in the United States or other countries. By using TapTab, you consent to this transfer.

---

## 11. Changes to this policy

We may update this privacy policy as TapTab evolves. The "Last updated" date at the top of this page reflects the most recent change. Material changes will be announced in the app's release notes. Continued use of TapTab after a change indicates your acceptance of the revised policy.

A version history of this policy is maintained in the public repository where it is hosted, so you can see exactly what changed and when.

---

## 12. Contact

For privacy questions, data deletion requests, or to report a vulnerability:

**Email:** HelloTapTab@gmail.com
**Subject line:** "TapTab Privacy"

We aim to respond within 7 business days.
