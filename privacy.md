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
- **A temporary subscription preview:** when you ask ytFolder to read your YouTube subscriptions
  page, the channel list it found is kept in session storage until you save or dismiss it, or the
  browser closes. Nothing is saved to your catalog until you confirm.

Each browser profile has its own separate catalog. Nothing is synced between browsers or devices.

## What ytFolder reads on YouTube

ytFolder runs on `www.youtube.com` pages to add its "Open ytFolder" launcher and the save button
beside Subscribe. On a channel page it reads that channel's public ID and name when you open the
save dialog. On your subscriptions page it reads the listed channels only when you ask it to. It does
not read your watch history, comments, playlists or account details, and it never changes anything
on your YouTube account: no history, watched state, playlists or subscriptions.

## Network requests

ytFolder only makes network requests when you load a label's video feed, after you turn on public
video feeds:

- It requests public feeds from `https://www.youtube.com/feeds/videos.xml` for the
  channels in that view.
- It loads video thumbnails from `https://i.ytimg.com/`.

These requests are sent without cookies or a referrer, so they are not tied to your YouTube
sign-in. Google's own privacy policy applies to them. Opening a video or channel link takes you to
YouTube like any other link.

## Backups

"Export catalog" downloads a JSON file to your computer. Restoring reads a file you choose. ytFolder
does not upload these files anywhere.

## Deleting your data

Removing the extension deletes its local storage, including your catalog. Export a backup first if
you want to keep it.

## Changes and contact

Changes to this policy will be published here with a new effective date. Questions and feedback:
<https://github.com/Lebedevsd/ytfolder-site/discussions>.
