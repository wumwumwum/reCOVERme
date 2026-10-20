# App Data Backup Menu

*A "What's important to you?" menu for backing up data that lives inside apps and online accounts, with the export method for each. Menu paths and policies change often, so spot-check any entry before you promise it to someone. Last compiled: October 2026.*

## How to use this

1. Hand the person the **Menu** (section 1) and ask them to tick what matters.
2. For each tick, look up the method in the **Reference** (section 3) and note it in their tracking table.
3. Set up the **automated** ones once (section 5), and put the **manual** ones on a calendar with a named owner.
4. File everything in the household's folder (section 6) and do a restore check.

**The rule of thumb:** if the data lives in an online account, your server can often pull it with no help from the phone. If it lives only inside the app on the phone, you will need an export, and exports are manual.

### Legend

| Code | Meaning |
| --- | --- |
| **A** | Automatable on your server after a one-time login. No ongoing effort. |
| **S** | Semi-automatic: the service can schedule it, but it expires or needs renewal. |
| **M** | Manual: someone has to trigger the export each time. |
| **X** | No real export. Say so before a loss, not after. |

## 1. The Menu (give this to the person)

**What's important to you? Tick everything you couldn't replace.**

**Messages and chats**

- [ ] WhatsApp chats and media
- [ ] iMessage / Messages
- [ ] Signal
- [ ] Telegram
- [ ] Facebook Messenger
- [ ] Snapchat
- [ ] Discord

**Social media and memories**

- [ ] Facebook posts and photos
- [ ] Instagram posts, stories and messages
- [ ] TikTok videos
- [ ] X (Twitter) posts
- [ ] LinkedIn profile and connections
- [ ] Pinterest boards
- [ ] Reddit history

**Email, contacts and calendar**

- [ ] Gmail
- [ ] iCloud Mail / Outlook / other email
- [ ] Contacts
- [ ] Calendar

**Files and notes**

- [ ] Google Drive
- [ ] Dropbox / OneDrive / Mega
- [ ] iCloud Drive
- [ ] Apple Notes
- [ ] Notion / Evernote / OneNote / Obsidian / Google Keep
- [ ] Todoist / Trello / other task apps

**Photos and video (beyond the phone)**

- [ ] Google Photos
- [ ] iCloud Photos
- [ ] Amazon Photos
- [ ] YouTube channel and uploads

**Health and fitness**

- [ ] Apple Health
- [ ] Fitbit / Garmin / Strava / Samsung Health
- [ ] MyFitnessPal

**Money and records**

- [ ] Bank and card statements
- [ ] PayPal / Venmo
- [ ] Budgeting app (YNAB etc.)
- [ ] Tax documents

**Passwords and logins**

- [ ] Password manager
- [ ] Authenticator app codes

**Media and purchases**

- [ ] Music playlists (Spotify etc.)
- [ ] Kindle / Audible library
- [ ] Amazon order history

**Other:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## 2. Start here: the whole-phone safety net

Before handling apps one at a time, there is one backup that catches many of them at once.

**iPhone:** an **encrypted backup to a computer** (Finder on a Mac, or the Apple Devices app on Windows). Choose "Encrypt local backup" and set a password. An encrypted backup includes more than an unencrypted one: Health data, saved Wi-Fi passwords and much of the app data. It can be restored onto a new iPhone. Write the backup password on the break glass sheet, because a lost password means the backup is useless.

**Android:** Google's own backup covers apps, settings and some data, but it lives in the Google account. For a copy you control, use each app's export (below) plus the Syncthing folder sync. There is no equivalent full local backup that works reliably across apps.

A computer backup is a snapshot, so it needs a reminder (monthly is a good rhythm) or a Wi-Fi sync set up with the computer left on.

## 3. Reference by category

### Messaging

| App | How to get the data | Code | Notes |
| --- | --- | --- | --- |
| **WhatsApp** | Settings › Chats › Chat Backup (to iCloud or Google Drive). For a copy you control: open a chat › Export Chat › Save to Files, with or without media. | M | The cloud backup is tied to the Apple or Google account, so it shares the lockout risk. Enable the end-to-end encrypted backup option and record the key. Android local backups sit in a folder Syncthing can reach. Per-chat export is tedious for many chats. |
| **iMessage / Messages** | No clean export from the phone. The encrypted computer backup (section 2) contains it. A Mac can print or export individual conversations. | M | Turn on Messages in iCloud as a sync copy, but remember sync is not backup. |
| **Signal** | Android: Settings › Chats › Chat backups, which writes an encrypted file protected by a long passphrase. iPhone has historically had no local backup. Check Signal's current options, because it has been adding its own encrypted backup feature. | M or X | Signal is built so that data stays on the device. A lost phone can mean lost history if you don't use a backup. |
| **Telegram** | Telegram Desktop › Settings › Advanced › Export Telegram Data (HTML or JSON, with media). | M | Done from a computer, not the phone. Cloud chats are stored by Telegram, but secret chats are not. |
| **Facebook Messenger** | Part of Meta's data download (see Social media). | M |  |
| **Snapchat** | accounts.snapchat.com › My Data. Also request Memories. | M | Memories can be large and arrive as separate download links that expire. |
| **Discord** | User Settings › Privacy & Safety › Request all of my Data. | M | You get your own messages, not full server history. |

### Social media

| App | How to get the data | Code | Notes |
| --- | --- | --- | --- |
| **Facebook / Instagram** | Accounts Center › Your information and permissions › Download your information. Choose date range, format (HTML or JSON) and media quality. | M (or S) | Meta lets you schedule repeating exports in some cases. Check the options when you create one. Choose high media quality. |
| **TikTok** | Settings › Account › Download your data. | M | Takes days. The link expires. Your own videos are best saved from the app directly. |
| **X (Twitter)** | Settings › Your account › Download an archive of your data. | M | Needs a verification code. |
| **LinkedIn** | Settings & Privacy › Data privacy › Get a copy of your data. | M | A quick archive is ready in minutes. The fuller one takes up to a day. |
| **Pinterest** | Settings › Privacy and data › Request your data. | M |  |
| **Reddit** | Settings or the data request page on reddit.com. | M | Saved posts can vanish when threads are deleted. |
| **YouTube** | Google Takeout (see Google). Also download your own videos in YouTube Studio. | S |  |

### Google account (one tool for many apps)

**Google Takeout** exports Gmail, Drive, Photos, Calendar, Contacts, Keep, YouTube and more. According to published guides, you choose the products, the file type and size, and the delivery method: \<cite index="10-1">a link by email, or saving to a cloud service such as Drive, Dropbox, OneDrive or Box,\</cite> and you can \<cite index="11-1">export once or set up an automatic export that repeats every two months for a year.\</cite> A Takeout export is a copy, not a move: \<cite index="15-1">downloading your data doesn't delete it from Google's servers.\</cite>

| Data | Best method | Code |
| --- | --- | --- |
| Gmail | Takeout (Mail), or IMAP sync to your server for continuous backup (section 5) | A with IMAP; S with Takeout |
| Google Drive | rclone from the server (section 5), or Takeout | A |
| Google Photos | Takeout. API-based tools often return reduced-quality or stripped files, so avoid them for originals. | S or M |
| Calendar and Contacts | Takeout, or CalDAV and CardDAV sync (section 5) | A or S |
| Keep notes | Takeout | S |
| YouTube | Takeout, plus Studio downloads | S |

**Caveat:** Takeout's scheduled option runs for one year, then stops. Put a yearly reminder in your calendar to recreate it. A business or school Google account may not allow Takeout at all.

### Apple account

| Data | Method | Code |
| --- | --- | --- |
| Everything Apple holds | privacy.apple.com › Request a copy of your data (choose categories). Takes days. | M |
| iCloud Photos | icloudpd on the server (see section 5), or the data request, or Photos export on a Mac | A (with limits) or M |
| Contacts | iCloud.com › Contacts › select all › Export vCard | M |
| Calendar | CalDAV sync (section 5), or export from the Calendar app on a Mac | A or M |
| Apple Notes | No bulk export on iPhone. On a Mac, notes can be exported one at a time as PDF. Third-party exporters exist but are unofficial. | M or X |
| Apple Health | Health app › profile picture › Export All Health Data. Produces a zip. | M |
| Passwords | Passwords app › export, where available on your OS version. Treat the file as highly sensitive. | M |
| iCloud Drive | Copy folders to a computer. Automated server access is fragile. | M |
| Voice Memos, Reminders | Share to Files, or use the encrypted computer backup | M |

**Advanced Data Protection** turns on extra end-to-end encryption at Apple. It is good for privacy, but it blocks several server-side pulls (such as icloudpd). Decide with the person which matters more.

### Notes, files and tasks

| App | Method | Code | Notes |
| --- | --- | --- | --- |
| **Notion** | Settings › Export all workspace content (Markdown, HTML or CSV). An API is available for automation. | M (A with API) | Workspace exports may be limited to admins. |
| **Evernote** | Export notebooks as ENEX files. | M | Per-notebook. |
| **OneNote** | Download notebooks via OneDrive, or export sections to PDF. | M | No clean bulk export. |
| **Obsidian** | Notes are plain files already. Sync the vault folder with Syncthing. | A |  |
| **Todoist** | Settings › Backups (automatic) or export a project as CSV. | S |  |
| **Trello** | Board menu › Print and export › Export as JSON. | M | One board at a time. |
| **Dropbox / OneDrive / Mega** | rclone from the server. | A |  |

### Email, contacts and calendar (beyond Google)

| Data | Method | Code |
| --- | --- | --- |
| iCloud Mail | IMAP with an app-specific password, synced to the server | A |
| Outlook / Microsoft 365 mail | IMAP sync, or export to PST from Outlook on a computer | A or M |
| Other email providers | IMAP sync | A |
| Contacts and calendars on most services | CardDAV and CalDAV sync to the server | A |

### Photos and video elsewhere

| Service | Method | Code |
| --- | --- | --- |
| Amazon Photos | Desktop app › download, or the request-my-data page | M |
| Shared family albums | Save to the camera roll first, so Immich picks them up | M |
| Snapchat Memories | My Data request | M |

### Health and fitness

| App | Method | Code |
| --- | --- | --- |
| **Apple Health** | Export All Health Data (above) | M |
| **Fitbit** | Google Takeout or the Fitbit data export in account settings | S |
| **Garmin Connect** | Account management › Export your data | M |
| **Strava** | Settings › My Account › Download or Delete Your Account › request your archive | M |
| **Samsung Health** | Settings › Download personal data | M |
| **MyFitnessPal** | Export from the website (a premium feature on some plans) | M |

### Money and records

| Data | Method | Code |
| --- | --- | --- |
| Bank and card statements | Download PDFs and CSVs from the bank's website each month or year | M |
| PayPal, Venmo, Cash App | Statements and activity downloads in account settings | M |
| Budgeting apps (YNAB etc.) | Export to CSV from the web app | M |
| Tax returns | Save the PDF filed copy and the source documents in the Documents folder each year | M |
| Insurance, medical portals | Download visit summaries and policy PDFs | M |

Record-keeping beats clever tools here. A yearly "paperwork day" works better than any automation.

### Passwords and authenticators

| Item | Method | Code | Notes |
| --- | --- | --- | --- |
| **Bitwarden** | Export an encrypted JSON from the web vault, or use the command-line tool for scheduled exports. | M or A | Store the export encrypted and keep the password separate. |
| **1Password** | Export from the desktop app. | M |  |
| **Browser-saved passwords** | Export to CSV, import into a password manager, then delete the CSV. | M | The CSV is unencrypted. Never leave it on a shared drive. |
| **Authenticator apps** | Use each account's printed recovery codes first. Some apps offer an account transfer or encrypted backup. | M or X | Some apps have no export at all. Moving to a password manager that stores codes, plus recovery codes on paper, is safest. |

### Media and purchases

| Item | Method | Code |
| --- | --- | --- |
| **Spotify** | Privacy settings › Download your data (history, playlists list). Playlist tracks need a third-party exporter. | M |
| **Kindle / Audible** | Download purchased files through the Amazon content library. Some formats are locked by DRM. | M or X |
| **Streaming services** (Netflix, Disney+) | Nothing to back up. | X |
| **Amazon orders** | Request My Data, or download order history reports | M |
| **Games** | Usually saved to the platform's cloud. Check that cloud saves are on. | X |

## 4. Menu to method: a quick decision guide

For each ticked item, ask:

1. **Is it in an online account?** If yes, try an automated pull (rclone, IMAP, CalDAV or Takeout). Done once.
2. **Is it only on the phone?** Use the app's export, or the encrypted computer backup.
3. **Is it a one-off record** (statements, tax documents)? Make it an annual routine.
4. **Is it unrecoverable?** (Signal on iPhone without backup, some authenticators.) Tell the person plainly and agree what to do.

## 5. Automation recipes (set up once)

### Cloud storage to your server with rclone

```
sudo apt install rclone
rclone config
```

Create a remote (for example `gdrive` or `dropbox`) and sign in when it opens the authorisation page. Then:

```
rclone sync gdrive: /srv/data/households/anna/exports/google-drive --backup-dir /srv/data/households/anna/exports/google-drive-deleted/$(date +%F)
```

The `--backup-dir` option keeps files that were deleted or changed in the source, so a deletion at Google doesn't erase your copy. Schedule it nightly with a systemd timer or cron, and ping Healthchecks.io when it succeeds.

### Email to your server over IMAP

Use `mbsync` (isync) or `imapsync`. For Gmail and iCloud, create an **app-specific password** (or use OAuth where required). A minimal `mbsync` setup has one IMAP account section, one store on disk, and a channel that pulls everything:

```
IMAPAccount anna
Host imap.example.com
User anna@example.com
PassCmd "cat /root/.mail-pass-anna"
TLSType IMAPS

IMAPStore anna-remote
Account anna

MaildirStore anna-local
Path /srv/data/households/anna/exports/mail/
Inbox /srv/data/households/anna/exports/mail/INBOX
SubFolders Verbatim

Channel anna
Far :anna-remote:
Near :anna-local:
Patterns *
Sync Pull
Create Near
```

Run `mbsync anna` nightly. `Sync Pull` means a deletion upstream won't remove your copy of messages already pulled.

### Contacts and calendars with vdirsyncer

`vdirsyncer` syncs CardDAV and CalDAV accounts (iCloud, Nextcloud, Fastmail, and Google with OAuth) to local files. Use it in pull-only mode, then include the folder in your restic jobs.

### iCloud Photos with icloudpd

The open-source `icloudpd` downloads originals from iCloud Photos. Limits to flag: it asks for two-factor re-authentication every so often (set a reminder), and it does not work if Advanced Data Protection is on.

### Google Takeout on a schedule

Create the export with delivery to Drive, frequency every two months, then let rclone pull the Takeout folder to your server. Recreate it every year.

## 6. Handling exports on your side

**Folder layout (per household):**

```
/srv/data/households/anna/exports/
  whatsapp/2026-10-13/
  facebook/2026-10-13/
  google-takeout/2026-08/
  apple-health/2026-10-13/
  google-drive/ (live copy)
  mail/ (live copy)
```

**Habits:**

- **Date every export** and keep the previous one. Never overwrite the only copy.
- **Record the key.** If an export or backup is encrypted, the key goes on the break glass sheet.
- **Include `exports/` in the offsite jobs** so it gets the same protection as photos.
- **Sensitive exports** (health, finance, passwords, private messages) go into an encrypted vault or a separate repository, especially for Type 2 and 3 households.
- **Delete the leftovers.** Exports sitting in Downloads, email or a chat thread are a risk. Move them, then clear them.
- **Open one.** For each new source, open the export once and confirm it contains what the person cares about.

**Tracking table (one per household):**

| App | Where data lives | Method | Code | How often | Who does it | Lands in | Last done | Next due |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |  |

**Suggested cadences:**

- Automated pulls: nightly, with a monitoring ping.
- Chat and social exports: every 3 to 6 months, or before any phone change.
- Health and fitness: every 6 months.
- Statements and tax documents: monthly or yearly paperwork day.
- Takeout schedule: renew yearly.

## 7. What you can't promise

Tell people this at the menu stage:

- **Some apps have no export** (some authenticators, streaming libraries, game progress).
- **Exports are snapshots.** Anything created after the export date is not in it.
- **Formats may not be reusable.** A JSON file can prove that data existed but may not restore it into the app.
- **Terms change.** Services alter their export tools, add fees or drop features. Your list needs a yearly review.
- **Some data is not theirs to keep** (licensed music and video, DRM books).
- **Shared content** (group chats, family albums) may contain other people's private data. Handle it with the same care as the rest.
