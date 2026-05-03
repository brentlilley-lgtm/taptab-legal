# TabTap — Google Play Data Safety Form Answers

Pre-filled answers for every section of the Google Play Console Data Safety form.
Consistent with the privacy policy at https://taptab-legal.vercel.app/privacy.

Open **Play Console → App content → Data safety** and work through each section below.

---

## 1. Overview

### Does your app collect or share any of the required user data types?

> **Yes**

### Does your app use data encryption in transit?

> **Yes — all data transmitted is encrypted**

### Do you provide a way for users to request that their data be deleted?

> **Yes**

*Users can email HelloTapTab@gmail.com to request crash-report deletion from Sentry. On-device data is deleted by uninstalling the app or clearing app storage.*

---

## 2. Data Types

### Personal info

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| Name | **Yes** | **No** | Owner enters their name in the profile. Stored on-device only. Never transmitted. |
| Email address | **No** | **No** | |
| User IDs | **No** | **No** | No accounts, no login. |
| Phone number | **No** | **No** | |
| Other personal info | **No** | **No** | |

### Financial info

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| User payment info | **No** | **No** | Google Play handles payment. TabTap never sees card numbers or billing details. |
| Purchase history | **Yes** | **No** | Google Play Billing confirms whether a $0.50 split-pass was purchased. Ephemeral. |
| Other financial info | **No** | **No** | |

### Photos and videos

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| Photos | **Yes** | **No** | Receipt photo is processed on-device via Google ML Kit OCR. **Never uploaded.** Ephemeral. |
| Videos | **No** | **No** | |

### App activity

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| App interactions | **Yes** | **No** | Sentry captures a short breadcrumb trail leading up to a crash. Only if Sentry configured. |
| Other actions | **No** | **No** | |

### App info and performance

| Sub-type | Collected? | Shared? | Notes |
|---|---|---|---|
| Crash logs | **Yes** | **Yes** | Sent to **Sentry** when configured. No personal data, receipt content, or screenshots. |
| Diagnostics | **Yes** | **Yes** | Same as crash logs. |

### Device or other IDs

| Sub-type | Collected? | Shared? |
|---|---|---|
| Device or other IDs | **No** | **No** |

---

## 3. Data Usage and Handling

### Personal info → Name
- Collected, not shared · Persists on-device · Optional · Purpose: **App functionality**

### Financial info → Purchase history
- Collected, not shared · Ephemeral · Required · Purpose: **App functionality**

### Photos → Photos
- Collected, not shared · Ephemeral · Required · Purpose: **App functionality**

### App activity → App interactions
- Collected, not shared · Ephemeral · Required (when Sentry configured) · Purpose: **Analytics**

### App info → Crash logs + Diagnostics
- Collected AND shared · Retained 90 days by Sentry · Required (when Sentry configured)
- **Shared with:** Sentry (https://sentry.io) — stack traces, app version, device model, OS version, breadcrumb trails only. NO receipt photos, OCR text, names, payment handles.

---

## 4. Additional Declarations

- **Advertising ID:** No
- **Families Policy:** N/A (target audience is 18+)
- **Contains ads:** No
- **Location for ads:** No

---

## 5. Privacy Policy URL

> **https://taptab-legal.vercel.app/privacy**

---

## Pre-Submit Checklist

- [ ] Privacy policy URL resolves (test in incognito)
- [ ] Privacy policy mentions Sentry by name and links to Sentry’s policy
- [ ] Privacy policy mentions Google Play Billing and the $0.50 IAP
- [ ] Privacy policy mentions on-device OCR and camera access
- [ ] Contact email (HelloTapTab@gmail.com) is listed in the privacy policy
- [ ] "Contains ads" is set to No in the Store Listing
- [ ] "In-app purchases" is set to Yes ($0.50 consumable) in the Store Listing
