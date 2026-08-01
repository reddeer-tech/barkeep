# BarKeep — Privacy Policy

_Last updated: 2026-08-01_

BarKeep is a macOS menu-bar utility developed by RedDeer, Inc. This policy explains what data
BarKeep accesses and how it is handled. BarKeep is **local-first**: the menu bar, the notch
island, and every core feature run entirely on your Mac. Some **optional** features — an online
account, friends & chat, online multiplayer, cloud settings sync, premium billing — use RedDeer's
servers, and this policy describes exactly what they store.

## The short version

- Core features process everything **locally on your device**; no account is required.
- Your **email data never leaves your Mac** — BarKeep collects no analytics about your email or
  its contents.
- Optional online features store only what they need (listed below); deleting your account
  removes it.
- BarKeep collects **anonymous usage statistics by default** — named feature events only, never
  content — and you can turn this off in **Settings → General → Privacy**.
- Your data is **never sold or shared with third parties** for their own purposes.

## What stays on your Mac

BarKeep is a menu-bar/notch utility and, depending on the features you enable, may read local
system state (menu-bar items, calendar/reminders, clipboard, battery, weather location,
now-playing). This information is used only to render BarKeep's on-screen features locally and
is never transmitted to RedDeer. These are optional, permission-gated macOS features you control
in System Settings.

## Email accounts (Gmail and Outlook)

If you connect an email account, BarKeep uses OAuth 2.0 to obtain **read-only** access
(Google `gmail.readonly`; Microsoft Graph `Mail.Read`). BarKeep uses this access solely to:

- show your recent **unread messages** (sender, subject, and a short preview) in the app, and
- display a brief on-screen notification when **new mail** arrives.

BarKeep does **not** send, delete, modify, or organize your mail, and it does **not** read message
bodies beyond the short preview Google/Microsoft return in the message list.

### Where your email data lives

- **Message data** (sender, subject, preview, timestamps) is fetched on demand and held **only in
  memory** on your Mac to render the UI. It is not written to disk by BarKeep and is not
  transmitted anywhere — not to RedDeer's servers, not into usage statistics, nowhere.
- **OAuth tokens** are stored in the **macOS Keychain** on your device. They never leave your Mac
  except in the direct, encrypted requests your Mac makes to Google/Microsoft.
- **Account metadata** (the email address and provider name, so BarKeep can label your accounts)
  is stored in BarKeep's local settings on your Mac.

### Removing your email data

Removing an account in BarKeep's settings deletes its Keychain token and local metadata
immediately. You can also revoke BarKeep's access at any time from your
[Google Account permissions](https://myaccount.google.com/permissions) or
[Microsoft account apps](https://account.live.com/consent/Manage).

## Google API Services — Limited Use disclosure

BarKeep's use of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the **Limited Use** requirements. Specifically, BarKeep only uses Gmail data to provide the
in-app unread-mail and new-mail features described above, does not transfer this data except as
necessary to provide those features (all processing is on-device), does not use it for advertising,
and allows no humans to read this data.

## Optional account & online features

Creating a BarKeep account (free) enables friends, chat, online multiplayer, and cloud settings
sync. When you use these, RedDeer's servers store:

- **Account**: your email address, display name, and a hashed password (never the password
  itself), plus your friend code.
- **Friends & chat**: your friend list, requests, blocks, and — if you keep chat history enabled —
  your messages. Turning chat history off makes new messages ephemeral (deleted on delivery).
- **Online games**: room and match records (who played what, when — never game content).
- **Cloud settings sync**: the app preferences you choose to sync. Clipboard history, API keys,
  and other sensitive or device-local data are **never** synced (the Sync settings page lists
  exactly what is).
- **Presence**: whether you appear online to friends is opt-out and visible to friends only.

**Deleting your account** (Settings → Account) removes all of the above from our servers.

## Payments

Premium purchases are processed by **Stripe**; your card details go directly to Stripe and are
never seen or stored by RedDeer. We store only your subscription state (plan, status, renewal
date) and a Stripe customer reference.

## Usage statistics (anonymous analytics)

To understand which features matter and where to invest, BarKeep collects anonymous usage
statistics. This is **on by default** and you can turn it off any time in
**Settings → General → Privacy → "Share anonymous usage statistics"** (the choice applies
per-Mac).

**What an event is**: a named action (for example "notch opened", "timer started", "game
started") with a timestamp, a random install identifier, the app version, and the macOS version.
When you are signed in, events are associated with your account so we can offer support and
understand premium usage.

**What is never collected**: message content, email data, clipboard contents, keystrokes, URLs
you visit, file names, screen contents, or anything you type. Events are a fixed list of feature
names — not a recording of your activity.

**Retention**: usage events are kept for approximately 90 days. If you delete your account,
events are immediately de-linked from it (the anonymous install identifier remains, connected to
nothing).

## Crash reporting

Release builds send crash reports to Sentry so we can fix bugs. A crash report contains the app
version, macOS version, hardware architecture, your Mac's hostname, and the technical state of
the app at the crash — never your documents, messages, or email data.

## Changes

We may update this policy; the "Last updated" date reflects the latest revision.

## Contact

Questions? Email **admin@reddeer.ai**.

© RedDeer, Inc.
