# TapTab — Google Play Data Safety Form Answers

Pre-filled answers for every section of the Google Play Console Data Safety form.
Consistent with the privacy policy at https://taptab-legal.vercel.app/privacy.

Open **Play Console → App content → Data safety** and work through each section below.

---

## 1. Overview

### Does your app collect or share any of the required user data types?

> **Yes**

*Rationale: TapTab collects a small amount of data (crash diagnostics via Sentry, purchase history via Google Play Billing). Even though most data stays on-device, the form requires "Yes" if any data type applies at all.*

### Does your app use data encryption in transit?

> **Yes — all data transmitted is encrypted**

*Rationale: Sentry crash reports are sent over HTTPS. Google Play Billing uses Google’s own encrypted channels. No other data leaves the device.*

### Do you provide a way for users to request that their data be deleted?

> **Yes**

*Rationale: Users can email HelloTapTab@gmail.com to request crash-report deletion from Sentry. On-device data is deleted by uninstalling the app or clearing app storage. This is documented in the privacy policy §7.1.*

---

## 2. Data Types

For each data type below, Google asks: **Is it collected?** and **Is it shared with third parties?**

### Location

| Sub-type | Collected? | Shared? |
|---|---|---|
| Approximate location | **No** | **No** |
| Precise location | **No** | **No** |

### Personal info

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| Name | **Yes** | **No** | Owner enters their name in the profile. Stored on-device only (AsyncStorage). Never transmitted. |
| Email address | **No** | **No** | Not collected. A payment handle (e.g., PayPal email) may look like an email but is entered voluntarily and stays on-device. |
| User IDs | **No** | **No** | No accounts, no login, no user IDs. |
| Address | **No** | **No** | |
| Phone number | **No** | **No** | A Zelle handle may be a phone number but is entered voluntarily and stays on-device. |
| Race and ethnicity | **No** | **No** | |
| Political or religious beliefs | **No** | **No** | |
| Sexual orientation | **No** | **No** | |
| Other personal info | **No** | **No** | |

### Financial info

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| User payment info | **No** | **No** | Google Play handles payment. TapTab never sees card numbers, bank details, or billing addresses. |
| Purchase history | **Yes** | **No** | Google Play Billing confirms whether a $0.50 split-pass was purchased. TapTab receives a success/fail signal, not financial details. |
| Credit score | **No** | **No** | |
| Other financial info | **No** | **No** | Payment handles (Venmo username, Cash App tag, etc.) are entered voluntarily and stored on-device only. |

### Health and fitness

| Sub-type | Collected? | Shared? |
|---|---|---|
| Health info | **No** | **No** |
| Fitness info | **No** | **No** |

### Messages

| Sub-type | Collected? | Shared? |
|---|---|---|
| Emails | **No** | **No** |
| SMS or MMS | **No** | **No** |
| Other in-app messages | **No** | **No** |

### Photos and videos

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| Photos | **Yes** | **No** | Camera / photo library access is used to photograph the receipt. The photo is processed on-device via Google ML Kit OCR and **never uploaded or transmitted**. Held in memory for one session only. |
| Videos | **No** | **No** | |

### Audio files

| Sub-type | Collected? | Shared? |
|---|---|---|
| Voice or sound recordings | **No** | **No** |
| Music files | **No** | **No** |
| Other audio files | **No** | **No** |

### Files and docs

| Sub-type | Collected? | Shared? |
|---|---|---|
| Files and docs | **No** | **No** |

### Calendar

| Sub-type | Collected? | Shared? |
|---|---|---|
| Calendar events | **No** | **No** |

### Contacts

| Sub-type | Collected? | Shared? |
|---|---|---|
| Contacts | **No** | **No** |

### App activity

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| App interactions | **Yes** | **No** | Sentry captures a short breadcrumb trail (button taps, screen transitions) leading up to a crash. Only sent if Sentry is configured. No screenshots. |
| In-app search history | **No** | **No** | |
| Installed apps | **No** | **No** | |
| Other user-generated content | **No** | **No** | |
| Other actions | **No** | **No** | |

### Web browsing

| Sub-type | Collected? | Shared? |
|---|---|---|
| Web browsing history | **No** | **No** |

### App info and performance

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| Crash logs | **Yes** | **Yes** | Stack traces, app version, and generic device info are sent to **Sentry** (third-party crash reporting service) when configured. No personal data, receipt content, or screenshots are included. |
| Diagnostics | **Yes** | **Yes** | Same as crash logs — Sentry receives performance/diagnostic data for debugging. |
| Other app performance data | **No** | **No** | |

### Device or other IDs

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| Device or other IDs | **No** | **No** | Sentry receives generic device model and OS version but not a persistent device ID, IMEI, or advertising identifier. |

---

## 3. Data Usage and Handling — for each "Yes" above

Google asks follow-up questions for every data type marked as collected or shared. Here are the answers grouped by data type.

### Personal info → Name

| Question | Answer |
|---|---|
| Is this data collected, shared, or both? | **Collected** |
| Is this data processed ephemerally? | **No** — persists on-device in AsyncStorage until user deletes it |
| Is this data required or can users choose? | **Optional** — the owner profile is optional but improves the experience |
| Why is this data collected? | **App functionality** — prefills the owner’s name in payment requests |

### Financial info → Purchase history

| Question | Answer |
|---|---|
| Is this data collected, shared, or both? | **Collected** |
| Is this data processed ephemerally? | **Yes** — TapTab checks purchase success/fail in memory, does not persist it |
| Is this data required or can users choose? | **Required** — the $0.50 split-pass purchase is required to send payment requests |
| Why is this data collected? | **App functionality** — gates the Approve & Send flow behind the IAP |

### Photos → Photos

| Question | Answer |
|---|---|
| Is this data collected, shared, or both? | **Collected** |
| Is this data processed ephemerally? | **Yes** — photo is held in memory for one session, never saved to disk or uploaded |
| Is this data required or can users choose? | **Required** — the app needs a receipt photo to function |
| Why is this data collected? | **App functionality** — on-device OCR extracts line items for the bill split |

### App activity → App interactions

| Question | Answer |
|---|---|
| Is this data collected, shared, or both? | **Collected** |
| Is this data processed ephemerally? | **Yes** — breadcrumbs are only captured at crash time and sent to Sentry |
| Is this data required or can users choose? | **Required** (when Sentry is configured) — but Sentry may not be active in all builds |
| Why is this data collected? | **Analytics** — helps diagnose the sequence of actions leading to a crash |

### App info and performance → Crash logs + Diagnostics

| Question | Answer |
|---|---|
| Is this data collected, shared, or both? | **Both** — collected by TapTab, shared with Sentry |
| Is this data processed ephemerally? | **No** — Sentry retains crash reports for 90 days |
| Is this data required or can users choose? | **Required** (when Sentry is configured) |
| Why is this data collected? | **Analytics** — crash diagnosis and app stability monitoring |

**Who is this data shared with?**

> **Sentry** (https://sentry.io) — third-party crash reporting and performance monitoring service. Sentry receives stack traces, app version, device model, OS version, and breadcrumb trails. Sentry does NOT receive receipt photos, OCR text, names, payment handles, or any personal information.

---

## 4. Additional Declarations

### Does your app use advertising ID?

> **No**

### Does your app comply with the Families Policy?

> **N/A** — TapTab is not targeted at children. Target audience is set to 18+ (the app involves financial transactions).

### Does your app contain ads?

> **No**

### Does your app use precise location for advertising purposes?

> **No** — TapTab does not collect location at all.

---

## 5. Privacy Policy URL

> **https://taptab-legal.vercel.app/privacy**

This URL is live, publicly accessible, and covers all the data types declared above.

---

## Quick Checklist Before Submitting

- [ ] All "Yes" answers above have matching follow-up entries in Section 3
- [ ] The privacy policy URL resolves (test in an incognito browser)
- [ ] The privacy policy mentions Sentry by name and links to Sentry’s own privacy policy
- [ ] The privacy policy mentions Google Play Billing and the $0.50 IAP
- [ ] The privacy policy mentions on-device OCR and camera access
- [ ] Contact email (HelloTapTab@gmail.com) is listed in the privacy policy
- [ ] "Contains ads" is set to No in the Store Listing
- [ ] "In-app purchases" is set to Yes ($0.50 consumable) in the Store Listing

---

## What Reviewers Look For

Common Data Safety rejection reasons and how TapTab avoids them:

| Reason | TapTab’s answer |
|---|---|
| Missing crash-log disclosure | ✓ Crash logs + Diagnostics declared as collected AND shared (with Sentry) |
| Photo access not declared | ✓ Photos declared as collected, ephemeral, required, for app functionality |
| IAP not declared | ✓ Purchase history declared as collected, ephemeral, required |
| Privacy policy doesn’t match form | ✓ Privacy policy covers every data type marked here, with matching third-party service links |
| "No data collected" but app has permissions | ✓ We correctly declare the data types that correspond to our CAMERA and INTERNET permissions |
