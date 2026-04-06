# Privacy Policy for TVBold

**Last Updated: April 6, 2026**

## 1. Introduction

TVBold ("we," "our," or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our mobile application TV Bold (the "App"). It also includes **subscriptions and purchase terms** for **TV Bold Premium** (premium access is granted when the **TVBold Pro** entitlement is active in our subscription system—see §14). Please read this policy carefully. If you do not agree with its terms, please do not access the App.

This disclosure is structured to align with [Apple’s App Privacy Details](https://developer.apple.com/app-store/app-privacy-details/) and the data categories used in App Store Connect.

## 2. Information We Collect

TVBold is designed with privacy in mind. We collect minimal data necessary to provide match schedule information, secure access to our services, optional premium features, and—when you opt in—push notifications for your favorite team.

### 2.1 Data Collected Automatically (Networking and SDKs)

The following data types are collected when you use the App, including via third-party SDKs:

#### Device ID
- **What we collect:** IP addresses sent with network requests; **device and advertising-related identifiers** through integrated SDKs (e.g. Google Mobile Ads). When you enable push notifications and register for alerts (see §2.3), we also transmit an **Apple Push Notification service (APNs) device token** and an **identifier for vendors (IDFV)** to our backend with your favorite team.
- **Purpose:** App Functionality (API access, authentication, notifications infrastructure), Analytics, Third-Party Advertising, subscription management, and—where applicable—device registration for push.
- **Linked to User:** Varies by processor: pseudonymous linkage for our backend (see §2.2); Google Mobile Ads and related ad technology may link data for advertising; RevenueCat links data to your app user identifier (§5.4).
- **Used for Tracking:** No for our own use of Supabase/Firebase analytics as described below; **Yes** may apply to Google’s advertising stack as defined by Apple’s “Tracking” (cross-app/website advertising measurement and related purposes—see §8).
- **Third-party collection:** Supabase, Google (Firebase Analytics, Google Mobile Ads), RevenueCat, Apple (IAP, APNs, DeviceCheck/App Attest as applicable).

#### Product interaction
- **What we collect:** How you use the App (e.g. launches, navigation, interactions with schedules), requests to our backend for match data, Firebase Analytics events we configure, interaction with ads (impressions, clicks), and paywall or subscription UI flows handled via RevenueCat and Apple.
- **Purpose:** App Functionality, Analytics, Third-Party Advertising, subscription-related functionality.
- **Linked to User / Used for Tracking:** As for Device ID—Firebase Analytics is used for product analytics, not as a substitute for the ad network’s tracking disclosure; Google Mobile Ads may link and use data for tracking as described by Google.
- **Third-party collection:** Supabase, Firebase/Google, Google Mobile Ads, RevenueCat.

#### Diagnostics
- **What we collect:** Error and stability-related signals needed to operate the App (including error information that may be emitted by client SDKs or our backend integration). **The App integrates Firebase Analytics for analytics; it does not integrate the Firebase Crashlytics SDK.** We do not represent that full crash report symbolication is collected unless or until we enable a dedicated crash reporting SDK.
- **Purpose:** App Functionality (troubleshooting) and Analytics (stability trends).
- **Linked to User:** Generally **not** linked to your real-world identity; may be associated with pseudonymous IDs where SDKs attach session context.
- **Used for Tracking:** No.
- **Third-party collection:** Supabase (operational logs where applicable), Firebase/Google.

#### Performance data
- **What we collect:** Technical metrics such as app launch timing and performance characteristics collected by Firebase Analytics.
- **Purpose:** Analytics.
- **Linked to User:** No.
- **Used for Tracking:** No.
- **Third-party collection:** Firebase/Google.

#### Advertising data
- **What we collect:** Data about ads served in the App (e.g. impressions, clicks, views) through Google Mobile Ads.
- **Purpose:** Third-Party Advertising.
- **Linked to User:** May be linked for advertising purposes by Google’s systems.
- **Used for Tracking:** May be used for tracking across apps and websites owned by other companies, as defined by Apple.
- **Third-party collection:** Google Mobile Ads.

#### Purchase history
- **What we collect:** We do **not** process your payment card numbers. **Apple** processes in-app purchases. **RevenueCat** processes subscription and transaction-related metadata to determine whether premium access (our **TVBold Pro** entitlement) is active. **In the App today, subscription status for features like ad removal is determined client-side via RevenueCat;** our Supabase Edge Functions include optional **App Store receipt validation** that can be invoked when the App sends a receipt payload—**primarily for server-verified premium content flows when that path is used.**
- **Purpose:** App Functionality (entitlements, restore purchases, optional server-side verification with Apple where needed).
- **Linked to User:** Yes—to your **pseudonymous app user identifier** (Supabase anonymous user id used with RevenueCat) and, on Apple’s systems, your Apple ID (we do not receive your Apple ID password).
- **Used for Tracking:** Not used by us for cross-app advertising tracking; refer to Apple’s and RevenueCat’s policies for their processing.
- **Third-party collection:** Apple, RevenueCat, and our Supabase-hosted backend when a receipt validation request is made.

### 2.2 User ID (Pseudonymous Account)

Under Apple’s **Identifiers → User ID** category, the App uses Supabase **anonymous authentication**:

- **What we collect:** A **pseudonymous user identifier** (UUID) for your anonymous Supabase account and **session tokens (JWTs)** used to authenticate requests to our edge functions.
- **Purpose:** App Functionality and abuse prevention (authenticated API access; aligning subscription restore with the same anonymous profile when RevenueCat `logIn` uses the same id).
- **Linked to User:** It is an account-level identifier but **not** your name, email, or phone number unless you later opt into a different sign-in method (this policy would be updated).
- **Used for Tracking:** Not used by us for third-party advertising tracking.
- **Third-party collection:** Supabase (Auth). RevenueCat receives the same UUID as the RevenueCat **app user ID** when the App links purchases to that identifier.

We do **not** ask you to create a password for this anonymous flow; the Supabase client manages the session per its documentation.

### 2.3 Push Notifications and Device Registration

If you are a **Premium** subscriber and opt in to notifications for a **favorite team**, the App registers your device with our backend:

- **What we collect:** Your **APNs device token** (hex), **IDFV** (or a generated device id if unavailable), and the **favorite team** string you selected, sent to our **register-device** Supabase edge function using your authenticated session. If you turn off notifications in the App, we attempt to **unregister** the token (`unregister-device`).
- **Purpose:** App Functionality (delivering match or team-related notifications you requested).
- **Linked to User:** Yes—associated with your pseudonymous Supabase user id via the authenticated request.
- **Used for Tracking:** No—not used for cross-app advertising tracking by us.
- **Third-party collection:** Supabase (our backend). **Apple** operates APNs delivery; Apple’s use is governed by Apple’s privacy policy.

### 2.4 App Attest and Device Integrity

To reduce automated abuse and protect match data APIs, the App uses **Apple’s App Attest / DeviceCheck** to create **cryptographic attestations or assertions** that your instance can send to our servers with API requests.

- **Purpose:** App Functionality and fraud prevention (verifying that requests come from legitimate app builds).
- **Linked to User:** Can be associated with your pseudonymous account when combined with authenticated calls.
- **Used for Tracking:** No—not used for advertising tracking by us.

### 2.5 Data Stored Locally (Not “Collected” in the Apple Sense by Us)

Unless it is also sent to servers as described above:

- **Usage days / counters** (e.g. for when to show Apple’s in-app review prompt or paywall timing) in **UserDefaults** or similar.
- **Preferences** such as favorite team may be stored locally **and** sent when you register for push as described in §2.3.

### 2.6 Data We Do Not Intend to Collect Directly Today

- **Name, email, phone, or postal address** (unless we add optional account features and update this policy).
- **Precise or coarse location** as a dedicated location feature.
- **Health or fitness** data.
- **Payment card or bank account numbers** (Apple processes payments).
- **Contacts, photos, videos**, or other device media libraries.
- **Browsing history** or **search history** beyond ordinary server logs and analytics events described above.
- **Sensitive categories** beyond what is strictly necessary for the services described.

**Note:** Free-form text you might type in future features could imply additional categories—we will update this policy if that changes.

## 3. How We Collect Information

- **Normal App use:** Network traffic (including IP addresses), authenticated calls with JWT when signed in anonymously, and optional App Attest assertions.
- **Ads:** After the **App Tracking Transparency** prompt (if shown), Google Mobile Ads initializes (§8).
- **Analytics:** Firebase Analytics events from the App.
- **Purchases:** Apple, RevenueCat, and—**when used**—our backend receipt validation with Apple.
- **Push opt-in:** Only after you request notifications; registration requires an active Premium subscription path as implemented in the App.

## 4. How We Use Your Information

- **App Functionality:** Schedules, secure API access, Premium (**TVBold Pro**) features (e.g. reduced/no ads where implemented, favorite-team notifications), device registration, optional server receipt checks, integrity checks.
- **Analytics:** Product improvement via Firebase Analytics.
- **Third-Party Advertising:** Google Mobile Ads for non-Premium users where ads are enabled.
- **Review prompts:** Local usage logic for Apple’s review API.

## 5. Third-Party Service Providers

### 5.1 Supabase

**Anonymous auth**, edge functions (matches, reference data, **register-device** / **unregister-device**, optional **get-premium-content** receipt validation), and hosting. Data may include IP addresses, User ID (UUID), JWTs, device registration fields (§2.3), API telemetry, and receipt payloads when that endpoint is used.

**Purpose:** App Functionality. **Tracking:** Not used by us for advertising tracking through Supabase.

Privacy policy: https://supabase.com/privacy

### 5.2 Firebase (Google)

Firebase **Analytics** (not Crashlytics in the current App build). Data can include device/app usage and performance-related measurements per Google’s implementation.

**Purpose:** Analytics and operational insight. Privacy policy: https://policies.google.com/privacy

### 5.3 Google Mobile Ads

Ads for users without active Premium where configured. Purposes include Third-Party Advertising; linkage and tracking as described by Google and reflected in §2.1 and §8.

Privacy policy: https://policies.google.com/privacy — Ad settings: https://adssettings.google.com

### 5.4 RevenueCat

Subscription management and **TVBold Pro** entitlement state; **logIn** with your anonymous Supabase user id for restore across devices.

Privacy policy: https://www.revenuecat.com/privacy

### 5.5 Apple

App Store purchases, APNs, App Attest/DeviceCheck, and receipt validation endpoints when used.

Privacy policy: https://www.apple.com/legal/privacy/

## 6. Data Storage and Security

HTTPS/TLS for network calls; industry-standard protections from our processors. No payment card storage on our servers. No method is 100% secure.

## 7. Data Retention and Deletion

Retention follows Supabase, Google, and RevenueCat practices and our configuration. Local data is removed on uninstall. Because accounts are anonymous, deletion requests may need corroborating details—contact §15. You may also use Apple, Google, and RevenueCat tools where available.

## 8. App Tracking Transparency (ATT) and “Tracking”

For personalized advertising and measurement, iOS may show a tracking permission dialog. The App’s tracking usage description is presented with that prompt and explains that data may be used to support personalized ads and measure ad effectiveness—consistent with the App’s `NSUserTrackingUsageDescription` in Info.plist. You can change the choice under **Settings → Privacy & Security → Tracking** (wording may vary by iOS version).

Google Mobile Ads may engage in **Tracking** according to Apple’s definition (e.g., linking across apps/sites for ads or measurement). Firebase Analytics is used for product analytics, not as a replacement for Google’s ads tracking disclosures.

## 9. Your Rights and Choices

Access, correction, deletion, or objections may be available depending on your region. Contact us at §15. You may also use processor-specific tools (Apple, Google ad settings, RevenueCat/Supabase as applicable). For subscriptions, use Apple’s subscription management (§14).

## 10. Children’s Privacy

The App is **not** directed to children under 13. If you believe we have information from a child under 13, contact us.

## 11. Changes

We may update this policy and revise the **Last Updated** date. Material changes may be communicated in the App or on the App Store listing.

## 12. International Transfers

Processors may operate globally. By using the App where permitted, you understand data may be processed outside your country.

## 13. Compliance

We aim to comply with applicable privacy laws (e.g. GDPR, UK GDPR, CCPA/CPRA where applicable).

## 14. Subscriptions and Purchase Terms (TV Bold Premium)

These terms apply to **auto-renewing subscriptions** and other **in-app purchases** offered in TV Bold via the **App Store**.

**Naming and entitlements:** The App may refer to this offering as **Premium** or **TV Bold Premium.** In our subscription system, premium access is tied to the **TVBold Pro** entitlement managed with **RevenueCat.** Exact in-app product names, subscription lengths, prices, and any free trial or introductory offer are shown only on the paywall and App Store product page at purchase time and may change by region or offering.

1. **Payment:** Charges are billed to your **Apple ID**; we do not charge your card directly.
2. **Auto-renewal:** Renews each period unless you cancel **at least 24 hours before** the current period ends, at the then-current price.
3. **Manage / cancel:** **Settings → Apple ID → Subscriptions** (or the equivalent App Store subscription management). Uninstalling the App **does not** cancel a subscription.
4. **Refunds:** Follow **Apple’s** refund policies; we cannot grant refunds for Apple-billed purchases ourselves.
5. **Restore:** Use **Restore Purchases** in the App or Apple’s subscription tools on a device signed into the same Apple ID. Restore is linked to a **pseudonymous app user id** (§2.2); loss of both device data and Apple account access may limit restoration.
6. **Features:** Premium may include **ad removal** (where ads are offered) and **favorite-team notifications**, and other features described in the App. We may modify features where permitted by law; billing remains under Apple’s terms.
7. **Apple’s contract:** Purchases are subject to the [**Apple Media Services Terms**](https://www.apple.com/legal/internet-services/itunes/) and [Apple’s **Licensed Application End User License Agreement (Standard EULA)**](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/) where applicable. If any summary here conflicts with Apple’s terms, **Apple’s terms control** for payment, renewal, and refunds.

This section is a **plain-language summary** and is not legal advice.

## 15. Contact Us

**Developer:** Thomas Kramer Nielsen  
**App Name:** TV Bold  
**Bundle Identifier:** thomaskramer.tvbold

**Policy URL (also used in the App):** https://thomas-kramer.dk/privatlivspolitik-tvbold/

For privacy requests, use the contact options published on that page or reach out via **App Store Connect** where available. Include approximate dates and region to help us locate records. We aim to respond within **30 days** unless a different timeline applies by law.

## 16. Consent

By using the App, you acknowledge this policy. If you do not agree, do not use the App.

---

_This Privacy Policy applies to the TV Bold mobile application (bundle id `thomaskramer.tvbold`)._
