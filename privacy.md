---
title: Privacy policy
---

# ytFolder privacy policy

Effective: 2026-11-19 (Chrome Free beta)

ytFolder is a browser extension that organizes YouTube channels with labels. It has no ytFolder
account, no ytFolder servers, no analytics, and no advertising. It does not sell or share data.

## What ytFolder stores

Everything is stored locally in your browser profile, in the extension's own storage:

- **Your catalog:** labels and their hierarchy, saved channels (YouTube channel ID and public name),
  which labels each channel has, and skipped videos (video ID, title, channel ID and the time you
  skipped it).
- **Settings:** whether you turned on public video feeds, whether the ytFolder bar shows on your
  YouTube subscriptions page, whether your labels show in YouTube's menu and which of them you folded there, whether label feeds refresh in the background, your colour theme, prompts you chose not to see again, and whether you
  hid the "Get started" guide.
- **Feed and backup state:** the public feed entries ytFolder fetched for your saved channels
  (video ID, title, link, publish time and thumbnail address, up to 50 per channel, removed after 14
  days), when you last opened each label's video feed (to mark newer videos as new), when YouTube
  last asked ytFolder to slow down (to pause background refresh), and when you last exported a
  backup and how many channels it held (for the backup reminder), and the labels you most recently
  assigned to channels (up to 20, to suggest them on channels without labels).
- **Channel topics:** when you use "Look up topics", the topic categories YouTube returned for each
  looked-up channel and when they were looked up (kept for 30 days), plus a count of today's lookups.
- **A temporary subscription preview:** when you ask ytFolder to read your YouTube subscriptions
  page, the channel list it found is kept in session storage until you save or dismiss it, or the
  browser closes. Nothing is saved to your catalog until you confirm.

Each browser profile has its own separate catalog. Nothing is synced between browsers or devices.

## What ytFolder reads on YouTube

ytFolder runs on `www.youtube.com` pages to add its "Open ytFolder" launcher, and the save button
and your labels beside Subscribe on channel and video pages. On a channel page it reads that
channel's public ID and name; on a video page it reads the public ID and name of the channel that
uploaded the video. It uses them to show which of your labels that channel has and, when you open
the save dialog, to save it. When you open the ytFolder toolbar popup on a YouTube tab, the popup
asks that tab for the same channel ID and name to show its labels; the popup does not read the
tab's address or other pages. Your label names, their nesting and how many videos
from ytFolder's cached feeds are new for each label are also shown as a section in YouTube's left
menu, unless you turn it off in the popup. YouTube's page
scripts cannot read the names, but can see the section's size and therefore roughly how many labels
you have; which channels have which labels is never shown there. On your subscriptions page it reads the listed channels only when you ask it to. On the subscriptions video feed (`/feed/subscriptions`) it reads each video card's channel ID, video ID, type (video, live, upcoming or Short) and whether YouTube shows it as watched, and marks the card with them inside the page, so cards can be filtered by label; these IDs are not stored or sent anywhere. For the label filter on that page, ytFolder's own script there reads your label names, which labels each saved channel has, your skipped video IDs and any looked-up channel topics from the extension. YouTube's page scripts cannot access this, and it is not sent anywhere. Apart from that watched mark on feed cards, it does
not read your watch history, comments, playlists or account details, and it never changes anything
on your YouTube account: no history, watched state, playlists or subscriptions.

## Network requests

ytFolder only makes network requests in the cases below, and only after you turn on public video
feeds or choose "Look up topics".

When you load a label's video feed, after you turn on public video feeds:

- It requests public feeds from `https://www.youtube.com/feeds/videos.xml` for the
  channels in that view.
- It loads video thumbnails from `https://i.ytimg.com/`.

While public video feeds are on, unless you turn off "Check label feeds for new videos" in the
popup:

- Every 30 minutes it requests the same public feeds for up to 50 of your saved channels whose
  cached feed is older than 30 minutes, so new-video counts stay current. If YouTube asks it to slow
  down, it pauses for an hour, longer if it happens again.

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
