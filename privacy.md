---
title: Masarify — Privacy Policy
layout: default
permalink: /privacy.html
---

# Privacy Policy

_Last updated: 2026-10-11_

Masarify ("we", "our", or "the app") is a personal finance tracker. This
policy describes what data the app collects, how it is used, and your
rights over it.

## What we collect

- **Financial data you enter** — transactions, wallets, budgets, goals,
  recurring rules, categories, and any notes you add. This data is stored
  locally on your device in an encrypted SQLite database.
- **Optional Google Drive backup data** — if you connect your Google
  account, a copy of your financial data, **encrypted on your device**
  (AES-256), is stored in your own Drive's hidden `appDataFolder` — a space
  private to Masarify that other apps and we ourselves never read. The
  encryption key is kept in that same private folder alongside the backup, so
  the data is **recoverable through your own Google account rather than
  zero-knowledge**: Google, as the provider that hosts your Drive, could in
  principle access it, while Masarify and other apps cannot. You can delete
  the backup at any time from your Drive's "App Data" management page.
- **Voice recordings** (optional, for AI voice memo) — sent to Google's Gemini
  API for transcription. Masarify does not retain the recording after the
  request. Google may retain prompts and responses for a limited period for
  abuse monitoring under the Gemini API terms applicable to our service tier;
  on an unpaid tier outside the EEA, Switzerland and the UK, Google may also use
  them to improve its services and human reviewers may process them. Do not put
  sensitive information in an AI recording. So the model can turn "paid the
  rent" into the right transaction, the
  recording is accompanied by a **snapshot of the things it may need to match
  against**: your **category names** (including any you created yourself), your
  **account (wallet) names**, the **names of your savings goals** (the keywords
  you gave a goal stay on your device and are matched there, after the reply
  arrives), your **budgets and the keywords you gave them**, and your **active
  bills and subscriptions with their amounts, currencies and how often they
  repeat**. Budget keywords are free text you wrote, so treat them the way you
  would any note you would not want sent off-device — you can edit or remove
  them at any time in Budgets, and if you never use the voice feature none of
  this is sent at all.
- **AI chat messages** (optional, for AI advisor) — sent to Google's Gemini API
  for inference. Masarify does not store them on its server; the conversation
  history remains locally on your device. The same Google retention, service-
  improvement and possible human-review terms described for voice recordings
  apply, so do not enter sensitive or confidential information. So the assistant can answer
  about your finances, each message is accompanied by a **snapshot of your
  current financial context** — your account (wallet) names, types and balances,
  income and spending totals, the names and progress of your budgets and goals,
  your top spending categories, and your **category names** (including any you
  created yourself, so the assistant can file a spend correctly) — which is sent
  to Gemini alongside the message. If you filled in the
  optional profile (Settings → Profile), your **name, age, gender, job title
  and stated monthly income** are also sent so replies can be tailored to you.
  You can stop that at any time with **Settings → Privacy → "Personalize AI
  with my profile"**, which keeps the AI working on your financial summary
  alone. This is the only circumstance in which account names and balances
  leave your device, it happens only when you use the AI features, and none of
  it is used for advertising.
- **How AI requests reach Gemini** — they do not go to Google directly from your
  phone. Every AI request (chat, voice and automatic categorisation) is sent
  first to **our own server function hosted on Google Firebase in the European
  Union**, which holds the Gemini key, enforces a per-user daily fair-use limit,
  and then forwards the request to **Google's Gemini API**. We do not store the
  content of your request or the reply on that server; what we do keep is a
  **counter** of how many AI requests your app installation has made today, so
  the limit can be enforced and the service protected from abuse.
- **An anonymous service identity** — the first time you use an optional
  server-backed feature (AI, cloud reminders, feedback, a subscription
  purchase or restore, consented first-party analytics, or consented crash
  diagnostics), the app may sign in to Firebase **anonymously**. This
  authenticates requests, applies abuse limits and, where applicable,
  attaches the relevant record to this installation.
  It happens without you signing in to a named account and creates a random
  Firebase identifier not based on your name or email. That raw identifier is
  never stored with analytics events; if you opt into usage analytics, events
  carry a **keyed code derived from it** instead (see Usage analytics). When
  you use Clear all data, the app requests deletion of this installation's
  analytics history and of an installation-only anonymous identity and its
  server records; named accounts remain available until you use Delete
  account. You can contact us below if a network failure prevents that
  request from completing.
- **Required app/device integrity attestation** — on launch, Firebase App Check
  asks Google Play Integrity on Android or Apple App Attest on iOS to provide
  an integrity token plus standard app/SDK and device-class metadata. This is a
  security control used to protect Masarify's backend from forged clients,
  fraud and abuse; it is not advertising, behavioral analytics, or
  cross-app tracking, and it cannot be switched off in Settings. Firebase says
  App Check does not retain the underlying attestation material; ordinary App
  Check tokens are short-lived. Google or Apple processes the attestation under
  its own platform terms.
- **Optional cloud-reminder data** — if you enable Cloud reminders, an
  anonymous device notification token plus your reminder time, timezone,
  and app language are sent to Google's Firebase Cloud Messaging to
  deliver reminders. No financial data is included. Off by default;
  removable at any time.
- **Optional account identity** — if you sign in (Settings → Account),
  you may connect your **Google account** or use **Sign in with Apple**.
  When signing in with Google, your Google email and basic profile
  (display name) are processed by Google's Firebase Authentication. When
  signing in with Apple, Apple provides a secure token and (optionally)
  your Apple ID email address, processed by Apple and then by Firebase
  Authentication. In both cases a pseudonymous account identifier is
  created. No financial data is attached to this account. Off by default;
  you can sign out or permanently delete the account at any time.

## What we do NOT collect

- Usage analytics do not collect your name, email, phone number, postal address,
  raw account UID or store billing identifier. If you opt in, they are linked to
  a keyed code derived from your app-account ID (see Usage analytics). Optional
  sign-in and feedback collect only the identity fields described above.
- We do not track your device's precise (GPS) location passively or in
  the background — only when you explicitly attach a location to a
  transaction or wallet (see Permissions). If you opt into usage analytics, our
  processor derives an **approximate** location (city level at most) from your
  IP address — see Usage analytics.
- We do not use advertising SDKs, ad networks, or ad trackers.
- We do not sell, share, or rent your data.

## Permissions

- **Internet** — for AI features and optional Google Drive backup.
- **Microphone** — only when you actively record an AI voice memo.
- **Notifications** — for bill reminders and recurring rule alerts.
- **Location** — optional. Only when you choose to attach a location to a
  transaction. The coordinates are stored on your device and are never sent to
  us and never sold. To turn coordinates into a readable place name we send them
  to your device's geocoding service (Google on Android, Apple on iOS), and if
  you open a transaction's map we load map tiles from **OpenStreetMap** using
  those coordinates. We request only **approximate (coarse)** location.

All permissions are optional. The core finance-tracking features work
fully offline.

## Crash & error diagnostics (optional, OFF by default)

Crash diagnostics are separate from usage analytics and are **off by default**.
When the app hits an error or crashes, a report is first **stored on your
device**, for at most 14 days. It leaves the device only if you enable crash
diagnostics — on the consent screen when you set up the app, in the
home-screen prompt, or in Settings → Privacy — and then goes only to **our own
servers on Google Cloud in the European Union**. No third-party crash or
analytics service receives it. If you never enable diagnostics, stored reports
are deleted on the device without being sent, and turning diagnostics off
deletes the reports that have not been sent yet. Turning analytics on does not
turn crash diagnostics on, and either choice can be changed independently.

A crash report contains the exception type, the code location (the stack
trace) and limited app and device context: app version and build, operating
system version, device manufacturer and model, processor type, Android SDK
level, a broad memory band, locale and timezone offset. On Android the app may
also read the system's own record of why its previous run ended (for example a
freeze or a native crash) and report it the same way. Diagnostics also include
**session health** records — when a session started and ended, how long the
app was in the foreground, how many errors occurred and whether it closed
normally or crashed — so that we can measure how often the app crashes.
Performance tracing and profiling are not collected.

Before a report is stored, the app removes database statements and their
values, masks digit sequences, Arabic text and email addresses in error
messages, and keeps only a limited set of breadcrumbs: normalized screen routes
and fixed action names. Reports must not contain amounts, merchant or account
names, notes, AI chat content, your name, email or advertising identifier.
Each report carries this installation's random **installation identifier**
(the same one usage analytics uses), so that repeated crashes on one device are
counted once; it is not your advertising ID, name, email or store account, and
crash reports do not carry the keyed account code described under Usage
analytics. To deliver reports the app signs in to Firebase anonymously (see
"An anonymous service identity" above).

Diagnostics received by our servers are kept for at most **14 months** and
then deleted automatically. **Delete analytics history** and **Clear all data**
also request deletion of the diagnostics sent under this installation
identifier. This processing is based on your explicit consent.

## Usage analytics (optional, OFF by default)

Usage analytics are **off by default**. Only if you explicitly opt in do we
collect **pseudonymous** product analytics to understand feature adoption,
quality and subscription conversion. Events carry a random identifier stored
by this installation of Masarify and a **keyed account code**: a one-way
cryptographic code (HMAC) that our server derives from your app's Firebase
account ID. Neither is your advertising ID, name, email or store account, and
the raw account ID is never stored with analytics. Because both are stable,
events can be grouped into sessions and funnels and linked to the same app
account's subscription record (see Subscriptions); the data is therefore
pseudonymous, not anonymous, and it is linked to your app account.

Collected fields are limited by a closed schema. They include canonical feature
events and screen names; session and event IDs; app version, platform, locale,
OS-major version, broad device/screen classes and timezone offset; coarse counts
and bands such as wallet/goal adoption, transaction-count band, budget-health
band, AI-usage band, free/Pro tier, broad age/income/spending brackets and a
built-in top-category key. Our first-party schema does **not** collect gender,
exact profile values, bracket midpoints, exact financial amounts, balances,
individual transaction or recurring-bill details, custom names, notes, AI
content, raw error messages, full device model, precise coordinates,
advertising IDs, or screen recordings. Purchase-funnel events may contain only
a low-cardinality store product key (such as monthly/yearly and a
founding-offer band) and a closed outcome such as started, succeeded, restored,
failed, or cancelled; they never contain a store receipt, purchase token, order
number, price, or payment details. Route query strings and record IDs are
removed. Unknown fields and events are rejected on the device and again by our
server.

Our server may derive an **approximate city, region and country** from the
request IP using an offline **DB-IP** database (IP Geolocation by
[DB-IP](https://db-ip.com)). The IP is used in memory for this lookup and is
**never stored** or sent to a geolocation service. We collect no postal code and
no precise/GPS location for analytics.

Analytics are sent only to our own servers on **Google Cloud in the European
Union**; no third-party analytics service receives them. Events wait on your
device, for at most 7 days, until they can be delivered. No screen frames or
session recordings are collected.

Firebase authentication protects the ingest callable. Our server derives the
keyed account code from the authenticated account ID, which is used only in
memory and never stored or logged with analytics. We use the code to answer
product questions — which features subscribers use before and after
subscribing, whether the paywall works, why people cancel — never for
advertising, and never combined with data from other companies. The code is
never shared with a third party. We do not add your name, email or store
account to analytics. Broad income, spending, savings and budget-health brackets are kept
only where the law permits; our server can drop them without an app update.

Raw analytics events are kept for at most **14 months** and then deleted
automatically. You can stop future collection at any time, clear unsent events,
or use **Settings → Privacy → Delete analytics history** to request deletion
for the current installation. Clearing app data also requests deletion of the
current installation's analytics history, gives the installation a new
identifier, and resets consent to off. Deleting your account deletes analytics
linked to its keyed account code. Deleting analytics does not cancel a store subscription
or delete an optional Masarify account because those systems are deliberately
separate. After deletion, we retain only a keyed, non-reversible tombstone for
at most 14 months—without the raw installation ID or any events—so a restored
device backup cannot accidentally reuse an identifier that was deleted. This
processing is based on your explicit consent.

## Cloud reminders (optional, OFF by default)

Masarify can remind you about your spending using on-device notifications,
which work fully offline. If you additionally turn on **Cloud reminders**
(Settings → Reminders), we register your device with **Google's Firebase
Cloud Messaging (FCM)** so reminders can be delivered even when the app is
closed. When enabled, a small amount of non-financial data is sent to and
processed by Google (Firebase) on servers **outside Egypt**: an **anonymous
device notification token** (a pseudonymous identifier for your app
installation, not tied to your name or account), your chosen **reminder
schedule** — the daily-reminder time and the **dates** of any bill or
subscription reminders you've set — your **timezone**, and your **app
language**. We never send your financial data — transactions, amounts,
wallets, budgets, notes, bill names, and AI content are never included in
reminder messages or their metadata; a bill push only says a reminder is due.
You can
turn Cloud reminders off at any time; doing so deletes the token from your
device and removes it from our records the next time your device is online,
which stops the transfer. Uninstalling the app, or prolonged inactivity,
also invalidates the token. This processing is based on your explicit
consent, and this cross-border transfer to Google/Firebase is disclosed
here in line with Egypt's Personal Data Protection Law (Law 151 of 2020).

## In-app feedback (optional)

You can send us feedback from inside the app (Settings → Send feedback, or
the home-screen invitation). When you choose to submit, the following is
sent to and stored on **Google's Firebase (Firestore)** on servers
**outside Egypt**: your **message text**, the **category** you picked
(bug/idea/other), your **app version**, **platform** (e.g. android), the
**app language**, and — only if you type it — an **optional contact
email**. We never attach your financial data, and submissions are not
linked to your identity unless you include your email. Feedback is used
solely to fix issues and improve the app, is never sold or shared, and you
can request deletion of any submission at any time via the contact email
below. Sending feedback is always your explicit action — nothing is sent
automatically.

## Account & sign-in (optional, OFF by default)

Masarify works fully without any account — by default you use the app
anonymously and all of your data stays on your device. You may optionally
sign in (Settings → Account) using either **Google** or **Sign in with
Apple**.

**Sign in with Google:** We use **Google's Firebase Authentication** to
establish a secure identity. The data involved is limited to your **Google
email address** and **basic profile (display name)**, which are processed
by Google (Firebase) to authenticate you.

**Sign in with Apple:** Apple authenticates you and provides a secure token
and — if you do not choose to hide your email — your **Apple ID email
address**, which is processed by Apple and then by Firebase Authentication
to establish a secure identity. If you choose to hide your email, Apple
provides a private relay address instead. No display name is shared unless
you provide one.

In both cases a pseudonymous **account identifier** is created. We do
**not** attach your transactions, amounts, wallets, budgets, notes, or any
other financial data to this account — your finances never leave your
device because you signed in.

Signing in is purely additive: it gives you a stable identity (for example
to support future optional cloud sync) and is required for none of the
app's features. You can **sign out** at any time, or **permanently delete
your account** (Settings → Account → Delete account), which removes the
Firebase identity and any associated cloud-reminder record. The Google
sign-in is separate from the optional Google Drive backup sign-in described
above. This processing is based on your explicit consent, and the transfer
to Google/Firebase (on servers outside Egypt) is disclosed here in line
with Egypt's Personal Data Protection Law (Law 151 of 2020).

## Subscriptions

Masarify offers a Pro subscription unlocking advanced features. Billing
is handled by Google Play (on Android) or the Apple App Store (on iOS).
We do not see your payment-card or bank details. When you subscribe, the app
sends the store an opaque, store-specific billing identifier: Google receives a
64-character keyed hash; Apple receives a random UUID. Our billing registry
stores the mapping between that identifier and the Firebase account used for
the purchase. When you buy or restore, the app also sends the store's proof of
purchase to our server, which verifies it with Google or Apple and records
which app account holds the subscription. We also receive the stores' own
subscription notifications (Google Play real-time notifications and Apple App
Store Server Notifications). These records hold the product and plan or offer,
the purchase token or transaction ID, status, region, and renewal, expiry,
cancellation and refund dates — and, where the store provides it, the reason
category you chose when cancelling, never any text you typed. We never fill a
gap by trusting subscription status the app reports about itself. Subscription
records are used for app functionality, fraud prevention, support and account
deletion, and — only if you opted into usage analytics — linked through the
keyed account code to understand how subscribers use Masarify. Never for
advertising.

## Data retention and deletion

**Your on-device data.** Your finances live on your device. To delete
everything, uninstall the app or use the in-app **Clear all data** option
(Settings). If you used Drive backup, you can delete that backup from your
Google Drive's "App Data" management page at any time.

**Deleting your account.** If you signed in — via Google or Sign in with
Apple (see "Account & sign-in" above) — you can permanently delete your
account and its associated data in either of two ways:

- **In the app:** Settings → Account → Delete account. This immediately and
  permanently deletes the account identity held by Firebase (your email,
  display name or relay address, and account identifier) together with
  everything on our servers that is linked to it: your **cloud-reminder and
  bill-reminder registrations**, your **AI usage counters**, and your
  **founding-member, billing-identity and subscription records** if you have
  them, and **usage analytics linked to your keyed account code**. This does not
  cancel a store subscription; manage that in Google Play or the App Store.
  Your on-device finances are not affected. If any part of that server-side clean-up does not complete
  immediately, the app tells you so rather than reporting success, and a daily
  job finishes it within 24 hours.
- **By request, no app needed:** email omarwalidghazal@gmail.com from the
  address associated with the account you signed in with, and we will
  delete your account and any associated data within 30 days.

After deletion we keep no account data, aside from copies Google/Firebase
may hold transiently in their own backups, which expire on Google's
standard schedule.

Three things are deliberate exceptions, and we would rather name them than let
you assume otherwise:

- **In-app feedback** is stored without any link to your account — that is what
  makes it anonymous — so we cannot find your messages in order to delete them
  automatically. Email the address above and we will remove them.
- **A Google Drive backup** lives in your own Drive, not ours. Delete it from
  Drive's "App Data" management page whenever you like.
- **Older, installation-only analytics** — analytics collected before you
  accepted this version of the policy is tied only to an installation
  identifier, not your account, so account deletion cannot find it. Use
  **Delete analytics history** (or Clear all data) on that installation if you
  also want it erased.

## Children's privacy

Masarify is intended for users aged 18 and older. Because its AI features
use Google's Gemini API — which requires users to be 18+ — the app is not
directed at, and must not be used by, anyone under 18. We do not knowingly
collect data from minors.

## Changes to this policy

We may update this policy. Changes will be reflected here with an
updated "Last updated" date.

## Contact

For privacy questions: omarwalidghazal@gmail.com
