---
title: Masarify — Privacy Policy
layout: default
permalink: /privacy.html
---

# Privacy Policy

_Last updated: 2026-06-14_

Masarify ("we", "our", or "the app") is a personal finance tracker. This
policy describes what data the app collects, how it is used, and your
rights over it.

## What we collect

- **Financial data you enter** — transactions, wallets, budgets, goals,
  recurring rules, categories, and any notes you add. This data is stored
  locally on your device in an encrypted SQLite database.
- **Optional Google Drive backup data** — if you connect your Google
  account, an encrypted backup of your financial data is stored in your
  own Drive's hidden `appDataFolder`. Only you can access it. We never
  read its contents.
- **Voice recordings** (optional, for AI voice memo) — sent transiently
  to Google's Gemini API for transcription, then discarded. Not stored
  by us.
- **AI chat messages** (optional, for AI advisor) — sent transiently
  to Google's Gemini API for inference. Not stored by us beyond the
  local conversation history on your device. If you fill in the optional
  AI personalization profile (Settings), it is stored **on your device**
  and only its contents that accompany an AI request are sent to Gemini,
  exactly like the rest of your AI message.
- **Optional cloud-reminder data** — if you enable Cloud reminders, an
  anonymous device notification token plus your reminder time, timezone,
  and app language are sent to Google's Firebase Cloud Messaging to
  deliver reminders. No financial data is included. Off by default;
  removable at any time.
- **Optional account identity** — if you connect your Google account
  (Settings → Account), your Google email and basic profile (display
  name) are processed by Google's Firebase Authentication to establish a
  secure account identity, and a pseudonymous account identifier is
  created. No financial data is attached to this account. Off by default;
  you can sign out or permanently delete the account at any time.

## What we do NOT collect

- We do not collect personal identifiers (name, phone, address).
- We do not track your device's precise (GPS) location passively or in
  the background — only when you explicitly attach a location to a
  transaction or wallet (see Permissions). If you opt into analytics, our
  processor derives only an **approximate** country/region from your IP
  address — see Analytics & diagnostics.
- We do not use advertising SDKs, ad networks, or ad trackers.
- We do not sell, share, or rent your data.

## Permissions

- **Internet** — for AI features and optional Google Drive backup.
- **Microphone** — only when you actively record an AI voice memo.
- **Notifications** — for bill reminders and recurring rule alerts.
- **Location** — optional. Only when you choose to attach a location to
  a transaction or wallet. Stored on your device; never sent to us or
  any third party.

All permissions are optional. The core finance-tracking features work
fully offline.

## Analytics & diagnostics (optional, OFF by default)

Analytics and crash diagnostics are **off by default**. Only if you explicitly
opt in (in Settings → Privacy) do we collect **anonymous, masked** usage
analytics and crash reports to improve the app. We use these processors:
**PostHog** (product analytics and **masked session replay**, hosted on its
**EU** infrastructure), **Sentry** (crash and error reporting, **EU** region),
and **Google Firebase Analytics and Crashlytics** (usage analytics and crash
diagnostics, processed by Google on servers **outside Egypt**, including the
**United States**). We do not collect personal identifiers, do not enable PII
enrichment, and do not assign an advertising ID or use ad personalization. Your
exact financial amounts, transaction details, balances, wallets, notes, and AI
chat content are **never** sent — sensitive fields are filtered out before any
data leaves your device. The optional **session replay** is fully **masked**:
every piece of text and every image is redacted on your device before a frame is
ever captured, so it records only anonymized layout and interactions (to spot
usability issues) — never your actual content or numbers.

If you have filled in your optional profile (Settings → Profile), we also attach
a few **coarse, anonymized** attributes to your anonymous analytics profile so we
can understand who uses Masarify: an **age range** (never your exact age), an
**income range** (a broad bracket — never your exact income, plus a
representative bracket value so we can gauge an *approximate* average), your
**gender**, and your auto-derived **spending persona**. While analytics is on we
likewise attach a few **coarse, anonymized usage** signals: your **app language**
and **currency** (so we understand which markets use Masarify) and whether you're
on the **free or Pro** plan; a **spending range** (a broad bracket of your
monthly spending, plus a representative bracket value — never your exact totals)
and your **most-used spending category** (only for the app's built-in categories
— the names of any categories you create yourself are never sent); **how actively
you use the app** (for example how many wallets, goals, or custom categories you
keep and a broad band of how many transactions you log) and **budget usage** (how
many budgets you keep and their periods — never their names or amounts); a few
**coarse financial-behavior bands** (for example whether you tend to save, break
even, or overspend, and a needs-versus-wants spending mix — always broad bands,
never exact figures); your **AI-feature usage** band; and **which optional
features you've enabled** (such as app lock, cloud reminders, or backup — never
the protected data behind them). Our analytics processor (PostHog) also derives
an **approximate location** — your **country/region**, from your device's **IP
address** (never a precise or GPS position) — so we can understand which regions
use Masarify. These values are bucketed so they
can't identify you, are never linked to your name or any identifier, and are
only sent while analytics is enabled. You can withdraw consent at any time in
Settings → Privacy, which stops collection immediately; clearing app data also
resets consent to off. This processing is consent-based, and these cross-border
transfers — to PostHog and Sentry in the **EU**, and to Google/Firebase
**outside Egypt (including the US)** — are disclosed here in line with Egypt's
PDPL (Law 151 of 2020).

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
**connect your Google account** (Settings → Account). When you do, we use
**Google's Firebase Authentication** to establish a secure identity for
your app installation. The data involved is limited to your **Google email
address** and **basic profile (display name)**, which are processed by
Google (Firebase) to authenticate you; a pseudonymous **account
identifier** is also created. We do **not** attach your transactions,
amounts, wallets, budgets, notes, or any other financial data to this
account — your finances never leave your device because you signed in.

Signing in is purely additive: it gives you a stable identity (for example
to support future optional cloud sync) and is required for none of the
app's features. You can **sign out** at any time, or **permanently delete
your account** (Settings → Account → Delete account), which removes the
Firebase identity and any associated cloud-reminder record. This identity
sign-in is separate from the optional Google Drive backup sign-in described
above. This processing is based on your explicit consent, and the transfer
to Google/Firebase (on servers outside Egypt) is disclosed here in line
with Egypt's Personal Data Protection Law (Law 151 of 2020).

## Subscriptions

Masarify offers a Pro subscription unlocking advanced features. Billing
is handled by Google Play. We do not see your payment details.

## Data retention and deletion

**Your on-device data.** Your finances live on your device. To delete
everything, uninstall the app or use the in-app **Clear all data** option
(Settings). If you used Drive backup, you can delete that backup from your
Google Drive's "App Data" management page at any time.

**Deleting your account.** If you connected a Google account (see
"Account & sign-in" above), you can permanently delete it and its
associated data in either of two ways:

- **In the app:** Settings → Account → Delete account. This immediately and
  permanently deletes the account identity held by Firebase (your Google
  email, display name, and account identifier) and the associated
  cloud-reminder record. Your on-device finances are not affected.
- **By request, no app needed:** email omarwalidghazal@gmail.com from the
  Google address you signed in with, and we will delete your account and
  any associated data within 30 days.

After deletion we keep no account data, aside from copies Google/Firebase
may hold transiently in their own backups, which expire on Google's
standard schedule. In-app feedback you have sent can likewise be deleted on
request to the same address.

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
