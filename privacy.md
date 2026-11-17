---
title: Privacy policy
---

# ytFolder privacy policy

Effective: 2026-11-17 (Chrome Free beta)

ytFolder is a browser extension that organizes YouTube channels with labels. It has no ytFolder
account, no ytFolder servers, no analytics, and no advertising. It does not sell or share data.

## What ytFolder stores

Everything is stored locally in your browser profile, in the extension's own storage:

- **Your catalog:** labels and their hierarchy, saved channels (YouTube channel ID and public name),
  which labels each channel has, and skipped videos (video ID, title, channel ID and the time you
  skipped it).
- **Settings:** whether you turned on public video feeds.
- **Channel topics:** when you use "Look up topics", the topic categories YouTube returned for each
  looked-up channel and when they were looked up (kept for 30 days), plus a count of today's lookups.
- **A temporary subscription preview:** when you ask ytFolder to read your YouTube subscriptions
  page, the channel list it found is kept in session storage until you save or dismiss it, or the
  browser closes. Nothing is saved to your catalog until you confirm.

Each browser profile has its own separate catalog. Nothing is synced between browsers or devices.

## What ytFolder reads on YouTube

ytFolder runs on `www.youtube.com` pages to add its "Open ytFolder" launcher and the save button
beside Subscribe. On a channel page it reads that channel's public ID and name when you open the
save dialog. On your subscriptions page it reads the listed channels only when you ask it to. On the subscriptions video feed (`/feed/subscriptions`) it reads each video card's channel ID, video ID, type (video, live, upcoming or Short) and whether YouTube shows it as watched, and marks the card with them inside the page, so cards can be filtered by label; these IDs are not stored or sent anywhere. For the label filter on that page, ytFolder's own script there reads your label names, which labels each saved channel has, and your skipped video IDs from the extension. YouTube's page scripts cannot access this, and it is not sent anywhere. Apart from that watched mark on feed cards, it does
not read your watch history, comments, playlists or account details, and it never changes anything
on your YouTube account: no history, watched state, playlists or subscriptions.

## Network requests

ytFolder only makes network requests in two cases, both started by you.

When you load a label's video feed, after you turn on public video feeds:

- It requests public feeds from `https://www.youtube.com/feeds/videos.xml` for the
  channels in that view.
- It loads video thumbnails from `https://i.ytimg.com/`.

When you choose "Look up topics":

- It sends the IDs of up to 50 of your saved channels to the YouTube Data API
  (`https://www.googleapis.com/youtube/v3/channels`) and receives their public topic categories.

These requests are sent without cookies or a referrer, so they are not tied to your YouTube
sign-in. Opening a video or channel link takes you to YouTube like any other link.

Topic lookup uses YouTube API Services. By using it you agree to the
[YouTube Terms of Service](https://www.youtube.com/t/terms), and Google's handling of the request
is covered by the [Google Privacy Policy](https://policies.google.com/privacy), which also applies
to the feed and thumbnail requests. Topic lookup uses no Google sign-in and accesses no account
data.

## Backups

"Export catalog" downloads a JSON file to your computer. Restoring reads a file you choose. ytFolder
does not upload these files anywhere.

## Deleting your data

Removing the extension deletes its local storage, including your catalog. Export a backup first if
you want to keep it.

## Changes and contact

Changes to this policy will be published here with a new effective date. Questions and feedback:
<https://github.com/Lebedevsd/ytfolder-site/discussions>.
