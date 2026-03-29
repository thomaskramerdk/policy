# Privacy Policy for TVBold

**Last Updated: March 29, 2026**

## 1. Introduction

TVBold ("we," "our," or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our mobile application TV Bold (the "App"). It also includes **subscriptions and purchase terms** for TV Bold Premium. Please read this policy carefully. If you do not agree with its terms, please do not access the App.

## 2. Information We Collect

TVBold is designed with privacy in mind. We collect minimal data necessary to provide match schedule information, secure access to our services, and optional premium features. In accordance with Apple's App Privacy Details requirements, we disclose the following data types collected by the App and our third-party service providers:

### 2.1 Data Collected Automatically

The following data types are collected automatically when you use the App:

#### Device ID
- **What we collect:** IP addresses transmitted as part of network requests to our service providers (Supabase, Firebase, Google Mobile Ads, RevenueCat, and Apple when validating purchases or receipts)
- **Purpose:** App Functionality (network communication, match data, authentication, subscription verification), Analytics, Third-Party Advertising, and subscription management
- **Linked to User:** No (for Supabase operational logs and Firebase analytics as described below) / Yes (for Google Mobile Ads — may be linked for advertising; for RevenueCat — linked to an app user identifier as described in §2.3 and §5.4)
- **Used for Tracking:** No (for Supabase and Firebase) / Yes (for Google Mobile Ads — may be used to track you across apps and websites)
- **Third-Party Collection:** Collected by Supabase, Firebase/Google, Google Mobile Ads, RevenueCat, and Apple as applicable

#### Product Interaction
- **What we collect:** Information about how you interact with the App, such as app launches, taps, and interactions with match schedules. This includes match data queries sent to Supabase, app usage events sent to Firebase Analytics, ad interactions (impressions, clicks, views) sent to Google Mobile Ads, and interactions with paywalls or subscription flows processed via RevenueCat and Apple.
- **Purpose:** App Functionality, Analytics, Third-Party Advertising, and subscription-related functionality
- **Linked to User:** No (for Supabase and Firebase) / Yes (for Google Mobile Ads; for RevenueCat — tied to app user ID)
- **Used for Tracking:** No (for Supabase and Firebase) / Yes (for Google Mobile Ads)
- **Third-Party Collection:** Collected by Supabase, Firebase/Google, Google Mobile Ads, and RevenueCat as applicable

#### Crash Data (Diagnostics)
- **What we collect:** Crash logs and error information when the App encounters errors or crashes. This may include error logs from Supabase SDK and crash reports from Firebase Analytics.
- **Purpose:** App Functionality (error handling and debugging) and Analytics (stability)
- **Linked to User:** No — not linked to your real-world identity (may be associated with pseudonymous identifiers used for auth or subscriptions where those SDKs attach context)
- **Used for Tracking:** No
- **Third-Party Collection:** Collected by Supabase and Firebase/Google

#### Performance Data
- **What we collect:** Technical performance metrics such as app launch time, performance data, and energy usage collected by Firebase Analytics.
- **Purpose:** Analytics
- **Linked to User:** No
- **Used for Tracking:** No
- **Third-Party Collection:** Collected by Firebase/Google

#### Advertising Data
- **What we collect:** Information about advertisements you have seen, including which ads were displayed, when they were shown, and how you interacted with them (impressions, clicks, views).
- **Purpose:** Third-Party Advertising
- **Linked to User:** Yes — may be linked for advertising purposes
- **Used for Tracking:** Yes — may be used to track you across apps and websites owned by other companies
- **Third-Party Collection:** Collected by Google Mobile Ads

#### Purchase History (subscriptions and in-app purchases)
- **What we collect:** We do not process your payment card details. **Apple** processes payments for in-app subscriptions. **RevenueCat** receives subscription and transaction-related data from Apple (and the App) to provide entitlement status (e.g. whether Premium is active). Our **Supabase Edge Functions** may receive an **App Store receipt** or related data from the App to **verify** subscription status with **Apple's receipt validation services** before returning premium content.
- **Purpose:** App Functionality (unlock Premium features: e.g. ad removal, favorite-team notifications; verify eligibility server-side where implemented)
- **Linked to User:** Yes — linked to your **anonymous app user identifier** (Supabase user UUID used as RevenueCat app user ID) and to your Apple ID on Apple's systems (we do not receive your Apple ID password)
- **Used for Tracking:** No — not used by us for cross-app advertising tracking; third-party policies (Apple, RevenueCat) govern their own use
- **Third-Party Collection:** Apple, RevenueCat, and our backend infrastructure (Supabase-hosted functions) as described above

### 2.2 Anonymous Account and Identifiers

To secure access to our backend and to support **restore purchases across devices**, the App uses **anonymous sign-in** with Supabase:

- **What we collect / generate:** A **pseudonymous user identifier** (UUID) for your anonymous Supabase account, and **session tokens (JWTs)** used to authenticate requests from the App to our services.
- **Purpose:** App Functionality and fraud prevention (authenticated access to edge functions, alignment of subscription state with the same anonymous user across installs/devices when combined with RevenueCat `logIn` using that UUID).
- **Linked to User:** The UUID is **not** your name, email, or phone number. It is a **pseudonymous** account identifier. If you later sign in with a real identity (if we add that in the future), this section will be updated.
- **Used for Tracking:** No — not used for third-party advertising tracking by us.
- **Third-Party Collection:** Supabase (authentication/session). RevenueCat receives the same UUID as the **app user ID** when the App links your subscription to that identifier.

We do **not** ask you to create a password for TV Bold for this anonymous flow; session handling is performed by the Supabase client according to their practices.

### 2.3 Data Stored Locally (Not Collected)

The following data is stored locally on your device and is **not** transmitted to us as "content" in the same way as server logs (some local state may still affect what the App sends in API calls):

- **App Usage Count / Usage Days:** Stored locally (e.g. iOS UserDefaults) to determine when to show Apple's native app review prompt and certain paywall timing. This stays on the device unless indirectly reflected in generic analytics events.
- **Network Connection Status:** Monitored on-device for error handling; not transmitted as a standalone "status feed."

### 2.4 Data We Do NOT Collect (or Do Not Collect Directly)

We do **not** intend to collect the following **directly from you** in the App today:

- **Name, email address, phone number, or postal address** (unless we add optional account features later and update this policy)
- **Location data** (precise or coarse)
- **Health or fitness data**
- **Payment card numbers or bank account details** — payments are handled by **Apple**; we do not receive your full card data
- **Contacts, photos, videos, or other media** from your device
- **Browsing history or in-app search history** beyond what is implied by normal server logs and analytics as described above
- **Sensitive categories** of personal data as commonly understood under privacy laws (beyond what is necessary for the services described)

**Important:** We **do** use pseudonymous identifiers, subscription status, and purchase-related data as described in §2.1 and §2.2. That is **not** the same as collecting your name or payment card.

## 3. How We Collect Information

We collect information in the following ways:

- **When you use the App:** Network requests carry IP addresses and may include authenticated headers (JWT) for Supabase edge functions.
- **When you use Premium or the paywall:** Apple and RevenueCat process purchase and subscription data; the App may send receipt or validation payloads to our backend for **server-side verification** with Apple.
- **Automatically via SDKs:** Supabase, Firebase Analytics, Google Mobile Ads, and RevenueCat collect data as described in Section 5.
- **Locally on your device:** Usage counters and preferences stored in UserDefaults or similar; primarily for on-device logic.

## 4. How We Use Your Information

We use the information we collect for:

- **App Functionality:** Match schedules; authenticated API access; **Premium** features (e.g. removing ads where applicable, enabling favorite-team notifications); **subscription verification** (client and server-side where implemented); error handling and stability.
- **Analytics:** Understanding usage, improving features, performance and diagnostics (Firebase and related tooling).
- **Third-Party Advertising:** Serving and measuring ads via Google Mobile Ads (non-Premium users where ads are shown).
- **App Review Prompts:** Local usage tracking to show Apple's review prompt; not shared off-device as a dedicated "profile."

## 5. Third-Party Service Providers

We use the following third-party services that may collect information:

### 5.1 Supabase

We use Supabase (supabase-swift SDK and Supabase Auth) for **anonymous authentication**, **edge functions** (including optional **receipt validation** and premium content delivery), and related infrastructure.

**Data types may include:**
- **Device ID:** IP addresses on requests to Supabase
- **User ID:** Pseudonymous anonymous user UUID and session tokens for authenticated requests
- **Product Interaction:** Requests to edge functions (e.g. match data, premium routes)
- **Purchase-related data:** When the App sends data for **Apple receipt validation**, our functions process that payload to verify subscription status with Apple
- **Crash Data:** Error logs where applicable

**Purpose:** App Functionality (auth, API access, premium verification, database-backed services)

**Data Linking:** Request data may be associated with your **anonymous user id** for authorization and logging. This is pseudonymous, not your real name or email unless you later provide such data.

**Tracking:** Not used by us for advertising tracking through Supabase.

Privacy Policy: https://supabase.com/privacy

### 5.2 Firebase (Google)

The App includes Firebase SDK with Firebase Analytics enabled.

**Data Types Collected by Firebase:** Device ID, product interaction, crash data, performance data (as in prior sections).

**Purpose:** Analytics and App Functionality (stability).

**Data Linking / Tracking:** As described in §2.1 — analytics data is not used for advertising tracking by Firebase in the way Google Mobile Ads is.

Privacy Policy: https://policies.google.com/privacy

### 5.3 Google Mobile Ads

The App may display advertisements when you are not a Premium subscriber (subject to app configuration).

**Data Types:** Device ID, product interaction, advertising data.

**Purpose:** Third-Party Advertising.

**Data Linking / Tracking:** May be linked and used for tracking as described by Google.

Privacy Policy: https://policies.google.com/privacy  
Ad settings: https://adssettings.google.com

**Note:** You can control personalized advertising and ATT as described in §8 and §9.

### 5.4 RevenueCat

We use **RevenueCat** to manage in-app purchases and subscription entitlements (e.g. **Premium**).

**Data types may include:** App user identifier (we use the same pseudonymous UUID as Supabase anonymous `user.id` where the App calls `logIn`), subscription status, product identifiers, transaction-related metadata, and device/network information as described in RevenueCat's policy.

**Purpose:** App Functionality (determine entitlement, restore purchases, present offerings).

**Data Linking:** Subscription data is linked to your **app user ID** (pseudonymous).

**Tracking:** Not used by us for cross-app advertising; see RevenueCat's policy for their processing.

Privacy Policy: https://www.revenuecat.com/privacy

### 5.5 Apple (App Store, StoreKit, receipt validation)

**Apple** processes payments for digital subscriptions and in-app purchases. Apple's collection and use of data is governed by Apple's privacy policy: https://www.apple.com/legal/privacy/

We do not receive your Apple ID password. Subscription management (cancel, refund requests through Apple) is handled under **Apple's terms and policies** for the App Store.

## 6. Data Storage and Security

- Network communications use HTTPS/TLS.
- Local data (e.g. usage counters) uses iOS storage mechanisms appropriate to the App.
- Match and operational data are hosted on Supabase; we rely on their security measures for that infrastructure.
- Subscription state is synchronized via RevenueCat and Apple; we do not store your payment card on our servers.

No method of transmission or storage is 100% secure.

## 7. Data Retention and Deletion

### 7.1 Data Retention

- **Supabase:** Auth sessions, logs, and edge-function processing (including receipt validation logs if any) are retained per Supabase practices and our configuration.
- **Firebase:** Per Google's retention and analytics policies.
- **Google Mobile Ads:** Per Google's policies.
- **RevenueCat:** Per RevenueCat's policies for subscriber and transaction records.
- **Apple:** Per Apple's policies for purchase history and subscriptions.
- **Local Device Data:** Until uninstall or app data clear.

### 7.2 Data Deletion

- **Local:** Uninstalling the App removes local data stored by the App.
- **Pseudonymous account and server-side data:** Because your account is **anonymous**, deletion requests may require information that can correlate your requests to server logs (e.g. approximate timing, device details you provide). Contact us as in §15. We will assist within practical limits and coordinate with processors where feasible.
- **Apple / RevenueCat / Google:** You may also use **Apple's subscription and privacy tools**, **Google's ad settings**, and **RevenueCat-supported flows** (e.g. via the App or their documentation) where applicable for data subject requests handled by those controllers.

We may retain information where required by law or for legitimate purposes (e.g. disputes, security).

## 8. Data Linking and Tracking

- **Pseudonymous account:** Your anonymous Supabase UUID and RevenueCat app user ID **link** subscription and API activity to a stable pseudonym, not necessarily to your real-world identity.
- **Firebase / Supabase (non-ad):** Generally not used to build advertising profiles across third-party apps by us.
- **Google Mobile Ads:** May link and track for advertising as described above.
- **ATT:** You may be prompted for permission to track; you can change this in iOS Settings.

## 9. Your Rights and Choices

- **Access / information:** Contact us (§15). Third parties (Apple, Google, RevenueCat, Supabase) may offer their own portals or processes.
- **Deletion:** Uninstall for local data; contact us for assistance with pseudonymous server-side data. Full deletion across all processors may require actions with **Apple**, **Google**, and **RevenueCat** as well.
- **Withdraw consent / stop processing:** Discontinue use of the App; note that basic networking still involves IP processing.
- **Subscriptions:** Manage, cancel, and request refunds where applicable through **Apple** (see §14).
- **EEA / UK / California:** If applicable laws grant you additional rights (access, correction, portability, objection, etc.), you may contact us and we will respond in accordance with applicable law.

## 10. Children's Privacy

The App is not intended for children under 13. We do not knowingly collect personal information from children under 13. If you believe a child has provided personal information, contact us and we will take appropriate steps.

## 11. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. We will post the new version here and update the "Last Updated" date. Material changes may also be communicated through the App or App Store listing where appropriate.

## 12. International Data Transfers

Your information may be processed in countries other than your country of residence (e.g. where Supabase, Google, RevenueCat, or Apple operate). By using the App, you acknowledge such transfers where permitted by law.

## 13. Compliance with Laws

We aim to comply with applicable laws, including GDPR (EEA/UK where applicable), CCPA/CPRA (California) where applicable, and other local privacy laws.

## 14. Subscriptions and Purchase Terms (TV Bold Premium)

These terms apply to **auto-renewing subscriptions** purchased in the App via the **App Store** (e.g. **TV Bold Premium** / product identifiers such as `tvbold.premium.monthly` as offered in the App). **Prices, billing period, and any trial** are shown **in the App and on the App Store at the time of purchase** and may vary by region.

1. **Payment:** Charges are billed to your **Apple ID**. We do not charge your card directly.
2. **Auto-renewal:** Unless you turn off auto-renewal **at least 24 hours before** the end of the current period, your subscription renews for the same duration at the then-current price.
3. **Manage / cancel:** Open **Settings → Apple ID → Subscriptions** on your device (or equivalent App Store subscription management). Uninstalling the App does **not** cancel the subscription.
4. **Refunds:** Refund requests for App Store purchases follow **Apple's policies and procedures**; we cannot issue refunds for Apple-billed IAP ourselves.
5. **Restore purchases:** Use **Restore Purchases** in the App (or Apple's subscription management) on a device signed in with the same Apple ID. We link entitlements to a **pseudonymous app user id** (see §2.2); if you lose access to both your device data and Apple account recovery, restoration may be limited.
6. **Premium features:** May include (as described in the App) **removing ads** and **notifications for favorite teams**, and other features we add. We may change, add, or discontinue specific Premium features with reasonable notice where required by law; your subscription remains governed by Apple’s terms for billing and cancellation.
7. **Apple’s terms:** Your purchase is also subject to **Apple Media Services Terms** and App Store rules. If there is a conflict between a short summary here and Apple’s terms, **Apple’s terms control** for payment and subscription management.

This section is for convenience and does not constitute legal advice.

## 15. Contact Us

If you have questions about this Privacy Policy or our data practices:

**Developer:** Thomas Kramer Nielsen  
**App Name:** TV Bold  
**Bundle Identifier:** thomaskramer.tvbold

**Channels:**
- App Store Connect messaging (if available for your region)
- **Website / policy:** https://thomas-kramer.dk/privatlivspolitik-tvbold/
- **Contact:** Use the support or contact option published on **https://thomas-kramer.dk/privatlivspolitik-tvbold/** for privacy-related requests, or reach out via App Store Connect.

Please include information that helps us locate your request (e.g. approximate date of use, region). We aim to respond within a reasonable time, typically within **30 days** where applicable laws do not require a different timeline.

## 16. Consent

By using the App, you consent to the collection and use of information as described in this Privacy Policy. If you do not agree, please do not use the App.

---

_This Privacy Policy is effective as of March 29, 2026, and applies to all users of the TV Bold mobile application._
