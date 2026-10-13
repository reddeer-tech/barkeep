# BarKeep — Privacy Policy

Last updated: 2026-10-13

BarKeep is a menu bar and notch app for macOS with companion apps for iPhone and Android,
developed by RedDeer, Inc. This policy explains what data BarKeep accesses and how it is handled.
BarKeep is **local-first**: the menu bar, the notch island, and every core feature run entirely
on your Mac. Some **optional** features — an online account, friends & chat, online multiplayer,
cloud settings sync, premium billing — use RedDeer's servers, and this policy describes exactly
what they store.

## The short version

- Core features process everything **locally on your device**; no account is required.
- Your **email data never leaves your Mac** — BarKeep collects no analytics about your email or
  its contents.
- Optional online features store only what they need (listed below). Deleting your account
  removes it 30 days after the account closes, apart from billing records, reports
  of abuse and requests made on our account deletion web page, which we keep (see below).
- The BarKeep Mac app collects **usage statistics by default** — named feature events only, never
  content, linked to your account while you are signed in — and you can turn this off in
  **Settings → General → Privacy**.
- Your data is **never sold or shared with third parties** for their own purposes.

## What stays on your Mac

BarKeep is a menu-bar/notch utility and, depending on the features you enable, may read local
system state (menu-bar items, calendar/reminders, clipboard, battery, weather location,
now-playing). This information is used to render BarKeep's on-screen features locally and is not
stored by RedDeer. If you use the BarKeep mobile app, some of it passes between your Mac and your
phone through our servers, as described in The BarKeep mobile app below. These are optional,
permission-gated macOS features you control in System Settings.

If you use Claude Code or Cursor on this Mac, BarKeep's optional AI features read the local
session logs those tools already keep, to show your agents' activity in the notch. The
session-coordination feature additionally keeps a small local database under `~/.claude/coord`
(readable only by your macOS user) holding short summaries of what each AI session is doing and
the messages sessions exchange with each other. It stays on your Mac, except that while you are
signed in to BarKeep, the questions, plans and requests to run commands or edit files that your
Claude Code sessions raise pass through our servers, with what each one asks and which session and
folder it comes from, so you can answer them from the BarKeep mobile app. This happens even if you
do not use the mobile app, and when you change your AI Sessions settings or approved folders, those
pass through too, with the list of your Claude Code commands. You can stop the questions in the Mac
app by turning off Answer Claude's questions from your phone, under AI Sessions. If you use the
mobile app's AI features, more of it passes between your phone and your Mac through our servers,
as described in The BarKeep mobile app below. Switching coordination off removes BarKeep's entries
from your Claude configuration and stops all logging.

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
sync. Sending messages, hosting online games or inviting friends to them, and cloud settings sync
from the Mac need Premium. When you use these, RedDeer's servers store:

- **Account**: your email address, display name, and a hashed password (never the password
  itself), plus your friend code.
- **Friends & chat**: your friend list, requests, blocks and your messages. A message is deleted
  once delivered only when you and your friend have both turned chat history off (the switch is
  in the Mac app), and turning it off does not delete messages already stored.
- **Online games**: room and match records (who played what, when — never game content).
- **Cloud settings sync**: the app preferences you choose to sync. Clipboard history, API keys,
  and other sensitive or device-local data are **never** synced (the Sync settings page lists
  exactly what is).
- **Presence**: your friends see whether you are online, away or offline unless you turn that off
  in Settings, Account. Even with it off, someone who knows your friend code and invites you to an
  online game can tell when the invite reaches a device where BarKeep is open.

**Deleting your account** (on the Mac: Settings, Account; on the phone: Settings, Manage account)
closes it straight away, and we erase the data above 30 days later. Without the
app, email admin@reddeer.ai from the email address on your account and we will delete it within
30 days. Deleting your account does not delete billing records (see Payments) or reports of abuse
(see The BarKeep mobile app).

## Payments

Premium bought on our website is processed by Stripe, and Premium bought in the mobile app by
Google Play or the App Store. Your full card number goes to them and never reaches RedDeer. We
store your subscription state (plan, status, renewal date), the Stripe customer reference or the
store's purchase record, and a record of each payment, renewal, refund and cancellation. A record
of a payment on our website can include the name, email address and billing country or postcode
you paid with and, for a refund, your card type, last four digits and expiry date. Deleting your
account does not delete these billing records, we keep them for at least 7 years for tax and
accounting purposes and many of them still include your account ID. Stripe, Google and Apple keep
their own records.

## Usage statistics

The BarKeep Mac app collects usage statistics to understand which features matter and where to
invest. This is **on by default** and you can turn it off any time in
**Settings → General → Privacy → "Share anonymous usage statistics"** (the choice applies
per-Mac).

**What an event is**: a named action (for example "notch opened", "timer started", "game
started") with a timestamp, a random install identifier, a random identifier for each launch of
the app, the app version, and the macOS version, and for some events a few details, such as which
settings page, tab or game it was about, or which plan a checkout was for.
When you are signed in, events are associated with your account so we can offer support and
understand premium usage.

**What is never collected**: message content, email data, clipboard contents, keystrokes, URLs
you visit, file names, screen contents, or anything you type. Events are a fixed list of feature
names — not a recording of your activity.

**Retention**: usage events are kept for approximately 90 days. If you delete your account,
events are immediately de-linked from it (the anonymous install identifier remains, connected to
nothing).

## Crash reporting

The BarKeep Mac app's release builds send crash reports to Sentry so we can fix bugs. A crash
report contains the app version, macOS version, hardware architecture, your Mac's hostname, and
the technical state of the app at the crash — never your documents, messages, or email data.

## Changes

We may update this policy; the "Last updated" date reflects the latest revision.

## The BarKeep mobile app

This section covers BarKeep for Android and iPhone. The app needs a BarKeep account, but on
iPhone, and on Android from the next update, you can play the games without one, and playing them
that way sends us nothing apart from the feature check below. Signed in or not, the app asks our
server which features are switched on when it starts and when it comes back on screen, with no
account or device ID in that request. The app shows no ads and does not use an advertising ID. It
has no analytics or crash reporting tools of our own, so the usage statistics and crash reporting
sections above apply to the Mac app only. We count sign-ups and purchases from our account and
purchase records for our own figures. On Android
the app uses Google's Play Billing Library for purchases. Each time the app starts, that library
sends Google its own logs about the billing requests it makes and whether they worked, even if you
never buy anything. The logs include details about your phone such as its make and model, Android
version, language and country settings, mobile carrier and network type. They go to Google, not
to us.

What the app sends to our servers and we keep:

- Your account: email address, password (stored only as a hash), optional display name, account
  ID and friend code (the phone app calls it your account code). We also keep when you last signed
  in, and when you first signed in on a phone and on a Mac
- Your devices: a random ID the app creates when installed, a device label (the device's network
  name) and whether the device is a phone or a Mac, so you stay signed in per device and relayed
  data reaches the right one. We also keep when each device last connected. Signing out ends that
  device's session.
- Notes, game scores, favourites and game options, and settings you change from the phone, synced
  to your account until you delete them or the account. On iPhone, and on Android from the next
  update, they sync only with Premium. Without it your changes stay on the phone, deletions
  included, so anything synced earlier stays with us
- Chat: the messages you send, kept so both of you can read them later unless you and your friend
  have both turned chat history off, in which case a message is deleted once delivered. The switch
  is in the Mac app, and turning it off does not delete messages already stored. While chat
  history is on, the app also keeps a copy of recent messages on your phone. We also keep which
  message you last read in each conversation, and when
- Friends: your friends, friend requests (including declined and cancelled ones) and blocks. Your
  friends see whether you are online, away or offline. Online means BarKeep is running on your Mac
  or open on screen on your phone, and away means your Mac is locked, on its screensaver or idle.
  You can turn this off only in the Mac app, under Settings, Account. Even with it off, someone
  who knows your friend code and invites you to an online game can tell when the invite reaches a
  device where BarKeep is open.
- Friend requests: anyone with a BarKeep account who knows your friend code or your email address
  can send you a friend request. As soon as they send it, before you accept, they can see your
  display name, your friend code and when you created your account, and anyone with an account who
  has your friend code can see the same without sending a request. None of this works for someone
  you have blocked.
- Terms: the app remembers on your phone when you accepted the Terms of Use, and that record syncs
  to your account with your settings, with or without Premium. On iPhone, and on Android from the
  next update, the same goes for the time you allowed AI data sharing (see AI sessions below), and
  if you withdraw it the app deletes that record, after which we keep only when it first reached
  us and when you withdrew it
- Reports: when you report a message we keep a copy of it with the reason you picked, who sent it
  and when, and your account. When you report an AI response we keep the text of that response
  (up to 4,000 characters) with your reason, the AI session's ID, your email address and your
  account. When you report a person we keep a report naming them with your email address and your
  account so we can follow up, and we block them for you. Message reports stay after either
  account is deleted, as the record of how we handled abuse, and a report about a person stays if
  that person deletes their account. A report you filed about an AI response or a person is erased
  with your own account.
- Purchases: if you buy BarKeep Premium through Google Play or the App Store we receive the
  store's purchase record (purchase token or transaction ID, product, status and renewal date).
  App Store records also include the price, the currency and the country of your App Store
  account. We also receive the store's later notices about renewals, cancellations and refunds. We
  check Google Play purchases with Google, and App Store purchases by checking Apple's signature on
  them. So the store can link a purchase to your account, Google receives a scrambled form of your
  account ID and Apple receives your account ID as it is. Card details never reach us. We keep
  these records after your account is deleted, as described in Payments above.

What passes through our servers without being kept:

- Between your phone and your Mac when both use your account: your Mac's vitals (such as CPU,
  memory, battery and whether it is locked), what it is playing with the cover art, its reminders
  and, while clipboard sharing is on in the Mac app (it is on by default), the text of recent
  clipboard entries and the names of copied files, plus the commands you send back.
- AI sessions: the prompts you type, the replies and reasoning, the tool activity the session
  reports (file paths, file contents it read or changed, commands and their output), permission
  requests and questions, including ones from Claude Code sessions running elsewhere on your Mac,
  and your answers, your list of current and past sessions with their titles, folders and
  settings, when each was last used and which app it runs in, the cost, token use and usage limits
  Claude Code reports, the names and descriptions of your Claude Code slash commands and skills,
  your approved folders and the folder names you browse to approve one. When you open a session,
  past or still running, its transcript passes through as well, with each new message while you
  have it open. The AI is the Claude Code or Cursor tool on your Mac. It runs under your own
  account with Anthropic or Cursor, and their privacy policies cover what it sends them. On
  iPhone, and on Android from the next update, the app asks your permission before it sends your
  first prompt or answer, and you can withdraw it in Settings under AI data sharing. The
  permission covers only what the phone sends into a session, your prompts and answers, the rest
  of what is listed here can pass between your phone and your Mac without it

Everything travels over encrypted connections (HTTPS and secure WebSockets). Our hosting
provider's request logs record the IP address of every request the app makes, and our own logs
record it with your email address each time you sign up or enter your password. On the phone your
sign-in token is kept encrypted by the phone's secure key storage. On Android it is left out of
device backups and out of transfers to a new phone. On iPhone it is kept in the iOS Keychain,
which is part of your iPhone backups, and restoring an encrypted backup can move it to a new
iPhone.

### Deleting your account

In the phone app go to Settings, Manage account, Delete account (on the Mac
it is under Settings, Account). Deleting in the app closes the account straight away, and we erase
the data above 30 days later. Until then you can get the account back by signing in
to the phone app and tapping Restore account. Without the app, email admin@reddeer.ai from the
email address on your account and we will delete it within 30 days. Billing records (kept for at least 7 years, see Payments) and
the reports described above stay after the account is erased, and if you asked through our account
deletion web page we also keep that request, with the email address, IP address and browser it
came from. A subscription bought on our website is cancelled when the account closes and is not
restored with it. A Google Play or App Store subscription is billed by Google or Apple, please
cancel it there, because deleting your account does not stop it.

BarKeep is not directed at children and we do not knowingly collect data from anyone under 13.

## Contact

Questions? Email **admin@reddeer.ai**.

© RedDeer, Inc.
