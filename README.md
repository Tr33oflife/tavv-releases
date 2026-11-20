# TavV

**Your Plex library, with a few extras.**

TavV is a fork of the [Plezy](https://github.com/edde746/plezy) Plex client — full Plex browsing and playback, plus a layer of extras Plezy doesn't have. Sign in with your Plex account, point it at your server, and everything below is just there, in the app.

**Platforms:** Android TV · Google TV · Fire TV · Windows (TavV Desktop)

📥 **[Download the latest release](https://github.com/Tr33oflife/tavv-releases/releases/latest)** · [All releases](https://github.com/Tr33oflife/tavv-releases/releases) · [Changelog](#changelog)

![TavV Desktop home screen, sidebar open over a Continue Watching backdrop — Nostalgia Mode, House Party, Fireplace, Lofi & Chill, Radio and Karaoke all live in the rail](docs/images/home.jpg)
*The home screen. Everything TavV adds lives in the sidebar: Nostalgia Mode, House Party, Fireplace, Lofi & Chill, Radio, Karaoke — alongside the full Plex library.*

---

## What you need

- A **Plex account** and access to a **Plex server** with your movies, shows and music. TavV is a player for your library — it doesn't host anything itself.
- The TV builds install like any sideloaded APK; the Windows build is a plain ZIP — unzip and run `tavv.exe`.
- TavV **updates itself**: the in-app updater checks this repo, so once you're installed, new builds arrive in the app.

## Installing on a TV with Downloader

TavV isn't in the Play Store, but the free **Downloader** app installs it in about five minutes using a short code. You only do this once — afterwards, TavV updates itself.

**You need:** your TV or streaming box connected to the internet.

**1. Get the Downloader app.** On your TV, open the Play Store (on Fire TV, the Amazon Appstore), search for **Downloader** by AFTVnews — the orange icon — and install it. It's free.

**2. Open Downloader.** If it asks permission to access files, choose **Allow**. You'll see a box labelled "Enter a URL, Search Term, or Short Code":

![The Downloader app's home screen, with the code box outlined](docs/images/downloader-home.jpg)

**3. Type your code.** Select the box, type the code for your device, then choose **Go**.

- **`7751929`** — 64-bit TVs: Shield Pro, Fire TV Cube, newer Sony & TCL sets
- **`2890643`** — most streaming sticks and boxes: Chromecast with Google TV, Fire TV Sticks, onn boxes, Shield (tube)

Not sure which you have? Use **`2890643`** — it installs on almost everything. If it's the wrong one for your device, nothing breaks; just repeat with the other code.

![Downloader's "Enter a numeric short code" box](docs/images/downloader-code.jpg)

**4. Install.** The file is about 160 MB, so the download takes a minute or two. When "File downloaded successfully" appears, choose **Install**:

![Downloader's download-finished message, with the Install button highlighted](docs/images/downloader-install.jpg)

The first time, your TV may say Downloader isn't allowed to install apps. Choose **Settings** on that message, turn on **Allow from this source**, press Back, and choose **Install** again.

**5. Open TavV and sign in** with your Plex account. That's it.

**If something goes wrong**

- **"Code not found"** — check the digits and try again; they're easy to mistype with a remote.
- **"App not installed"** — the other build fits your device better. Delete the file in Downloader's **Files** tab and repeat with the other code.
- **The download stopped partway** — delete the partial file in Downloader's **Files** tab, then enter the code again.

The codes never change — they always fetch the newest TavV. *Downloader is by [AFTVnews.com](https://www.aftvnews.com/); the screenshots above show that app.*

## What TavV adds

On top of everything Plezy already does well:

### 📺 Nostalgia Mode — live-TV channels from your own library

Custom live-TV-style channels built from your Plex library, with a real channel guide: numbered channels, Now/Next listings, channel surfing with the remote (channel up/down keys zap like a real TV). Build channels with the channel wizard, shape them with dayparts, and define them by **Plex labels** — include only items carrying a label, or ban labels outright.

Channels behave like real cable, too:

- **Episode cooldown** — the same episode can't repeat on the same channel for at least 48 hours (a week where the pool allows), just like regular TV.
- **The fit check** — a quiet background pass that checks whether a title actually belongs on its channel, using outside facts (OMDb) and an optional AI tone pass, and drops the misfits.
- **Sign-off hours** — thin channels sign off overnight (2–6 AM) instead of threadbare repeats; empty channels hide from the guide, leaving gaps in the numbering like real cable.
- **Listing sync** — every TV in the house shares one lineup, on by default. The first set of the day starts the household; the others hear it and join on their own.
- **Play styles** — a channel can broadcast **sequentially** (episodes in order, like a real run) and can refuse **back-to-back episodes of the same show**.
- **Fair rotation** — draws between shows are weighted so a one-season show isn't drowned by the long runs next to it, without looping it either.
- **Wizard dry run** — the channel wizard previews exactly which titles a recipe admits — and flags the ones no genre check vouches for — before the channel exists.
- **More built-in channels (1296)** — Monster Island (kaiju), DC Animated, Licensed to Thrill (spy & action franchises), Ghibli, Final Frontier (Star Trek), Roam (travel & food), Quick Stop (View Askew), and a combined **Christmas** channel that leads with Christmas episodes — a verified master list of 237 across 89 series — and folds Christmas movies in behind them.

![The Nostalgia Mode guide — numbered custom channels with Now/Next programme rows](docs/images/guide.jpg)
*The guide: your channels, numbered and always in the same place, each with what's on now and what's next.*

### 🎵 Music

A full music panel, in the app by default: search (with suggestions as you type, voice search on remotes that offer it, and your recent searches kept), artist and album browsing, playlists, a queue, and playback that resumes where you left it — across restarts, mid-track. Lyrics load in the panel while a song plays — synced line by line when a timed source has them, following the track as it plays, with tap-to-seek.

### 📡 Settings that travel

Set one TV up the way you like it, then share it: **Settings → Services** can send your setup to the other TVs in the household over the household link — no re-typing on a remote. Importing is a deliberate tap on the receiving set, and sign-ins and cheat codes never travel.

### 🔎 Smart search

Library search ranks what you meant: a show whose title matches beats a fuzzy actor match, so the series you typed is the first thing you see.

### 🎧 Lofi & Chill

A listening panel that looks as good as it sounds: lofi radio stations and Jamendo mixes over animated scenes — 3 bundled backgrounds that work offline, plus downloadable lofi loops — with an optional rain layer on top. Pick a station, pick a background, leave it on.

![Lofi & Chill — Lofi Girl Radio playing over the Couch animated background, with station, mix, rain and background controls](docs/images/lofi.jpg)
*Lofi Girl Radio over the Couch scene. Station, Jamendo mix, rain and background are all one tap apart.*

### 🔥 Fireplace

Fireplace scenes made to be left on — bundled scenes plus downloadable ones (Brick Hearth, Fire Pit, Ember Stove download on first pick and play from the device after that), with their own quiet radio: seven SomaFM stations in fireplace themes.

![The Fireplace running full screen](docs/images/fireplace.jpg)
*The Fireplace, full screen. Scenes are real looping footage, not a still picture.*

### 📻 Radio

A standalone radio panel wearing a 1930s cathedral-radio skin — walnut cabinet, a working amber dial, preset push-buttons. Three bands:

- **46 SomaFM stations**, tuned from the panel, with held-OK preset pins (up to 8, they survive restarts)
- **6 Jamendo mixes** — jazz, lounge, chillout, classical, ambient, christmas
- **Radio Browser** (optional, off by default) — **28 genre shelves** from punk and country to hip-hop, talk and comedy, plus search

![The Radio panel in its 1930s cathedral skin, Radio Browser band open on a jazz shelf](docs/images/radio.jpg)
*The Radio panel: cathedral cabinet on the left, the Radio Browser's genre shelves and station list on the right.*

### 🎤 Karaoke

Pick a track from your Plex music library and sing along — line-synced lyrics from LRCLIB light up line by line as the track plays, right in the panel. Unsynced or missing lyrics are labelled honestly. The original vocal stays in; it's a sing-along, not a vocal remover.

### 🥂 House Party & Guest Pass

Watch-together for the household: start a House Party from the player or the guide and other sets in the house can see what's on and follow along. **Guest Pass** (build 1255) turns the household invite into a deliberate thing — send the invite text to someone and they're in the household from anywhere; "Forget this household" on your side re-mints the key and revokes it.

### 🗝️ Cheat codes

Settings → Services → Cheat codes accepts plain phrases that wake hidden panels:

- `ask the bartender` — the **Requests** panel
- `librarian` — the **Books** tab
- `game night` — the **Games** entry
- `external players` — the **External Players** browser

(The original letter codes still work too.)

### 🌐 External Players

A real TV browser, built in (build 1300): a small built-in roster of streaming sites, browsed with a native cursor the remote drives — the D-pad moves the cursor, OK taps, holding OK scrolls the page, and nothing is ever injected into a page. When a stream starts, one press of Play sends it to TavV's own player. Woken by the `external players` cheat phrase; Android only.

### 🖥️ TavV Desktop

The same TavV, same features, built for Windows. Everything above runs on the desktop with full keyboard and mouse control — since build 1262 every panel is clickable, with press-and-hold doing the long-press, exactly like the remote.

### 🎨 Everything free

No supporter pack, no purchase gates: every theme (including Ember, Glacier, Forest, Plum, Paper and the custom palette editor) and every alternate app icon is simply available in every build. The only gates left are Plex Pass for Plex's own features, and the cheat codes above.

---

## Downloads

Grab the newest build from the **[Releases page](https://github.com/Tr33oflife/tavv-releases/releases)**. Each release carries up to three files:

| File | For |
|---|---|
| `TavV-<version>-<build>-armeabi-v7a.apk` | Most streamer TVs: Chromecast with Google TV, Fire TV Sticks, onn boxes, Shield (tube) |
| `TavV-<version>-<build>-arm64-v8a.apk` | 64-bit TVs: Shield Pro (2015–2019), Fire TV Cube gen 2, newer Sony/TCL |
| `TavV-<version>-<build>-windows-x64.zip` | Windows desktop (build 1260 and later) — unzip, run `tavv.exe` |

New to this? Follow the [Downloader guide](#installing-on-a-tv-with-downloader) above — or install the APK with TV Toolbox or any APK installer. All releases are signed with one consistent key, so a newer file installs over an older TavV without removing it first — and once installed, the in-app updater keeps you current from this repo.

> One extra release, **fireplace-loops-v1**, isn't an app update: it carries the downloadable Fireplace scenes for build 1250+. The app fetches them itself on first pick; you don't need to download them by hand.

---

## Changelog

Full notes live on each [release](https://github.com/Tr33oflife/tavv-releases/releases); the headlines:

### Build 1300 — External Players, rebuilt as a native browser

- **External Players returns as a new panel** — browsing is a native cursor layer over the page: the remote moves a cursor, taps land as real touches, holding OK scrolls, and no script is ever injected into a page. The old doorway build stays deleted; if you had the panel before, the `external players` cheat phrase installs the new one fresh.
- **Play in TavV player:** when a stream starts on a site, a "Play in TavV player" prompt appears (or just press Play) and the video opens in TavV's own player.
- **Channel guide:** the House Party / Household / Recent header now starts folded behind a single row and scrolls away with the channels, instead of filling the guide.
- Carries 1299 and 1298 whole.

### Build 1299 — External Players removed

- **External Players is gone, whole** — the panel, its built-in site list, and its cheat phrase are deleted, not hidden. If it was installed, the entry removes itself on update. (The generic web doorway stays: the Games panel and components you install yourself still use it.)
- **Custom channels dealt through the guide (1298):** the built-in list channels and your own wizard channels no longer sit in a block at the very end — they're dealt evenly through the lineup, so zapping reaches them. Channel numbers stay stable day to day.
- Carries 1297 whole.

### Build 1297 — Synced lyrics · [notes](https://github.com/Tr33oflife/tavv-releases/releases/tag/v2.26.0-1297)

- **Synced lyrics:** the Music panel pulls timed lyrics from LRCLIB — the current line highlights and follows the track, and tapping a line seeks to it. Plain lyrics remain the fallback.
- Web doorway navigation rebuilt around a remote-moved cursor.

### Build 1296 — The channel-work build · [notes](https://github.com/Tr33oflife/tavv-releases/releases/tag/v2.26.0-1296)

- **Fair rotation:** channel draws are weighted by the square root of a show's episode count — a 13-episode show next to two long runs goes from ~3% of the channel to ~11%, with repeats days apart.
- **Seven new built-in channels** — Monster Island, DC Animated, Licensed to Thrill, Ghibli, Final Frontier, Roam, Quick Stop — plus **Slasher Alley: After Dark** for the 2000+ slashers, Kung Fu Theater's year cap lifted, and Saturday Morning admitting TV-PG.
- **The Christmas channel:** Christmas episodes first (237 verified episodes across 89 series, matched by name), Christmas movies folded in as the minority share.
- Carries 1288–1295 whole: the **Music panel is on by default** with working lyrics; **wireless settings share** between household TVs; doorway navigation hardened (seek only from the seek bar, the top bar only from the page's very top); the **channel wizard dry run**; music search suggestions, voice search, resume and Load more.

### Build 1287 — House Party entry fix · [notes](https://github.com/Tr33oflife/tavv-releases/releases/tag/v2.26.0-1287)

- The floating House Party chip over library playback is gone; the entry now lives at the end of the player's control bar, where the remote can reach it. The running-party banner stays.

### Build 1262 — Karaoke + mouse fix · [notes](https://github.com/Tr33oflife/tavv-releases/releases/tag/v2.26.0-1262)

- **Karaoke (1261):** a new panel in the music family — pick a track from your Plex music library and sing along to LRCLIB line-synced lyrics in-panel. Unsynced or missing lyrics are labelled honestly.
- **Mouse fix (1262):** clicks now work on every TavV panel (Fireplace, Lofi, Radio, Karaoke, guide cards) — a tap focuses and selects, press-and-hold does the long-press. Keyboard/D-pad behaviour unchanged.
- Windows bundle included.

### Build 1260 — Label channels, Radio Browser in full, first Windows bundle · [notes](https://github.com/Tr33oflife/tavv-releases/releases/tag/v2.26.0-1260)

- **Plex/Jellyfin labels drive custom channels (1259):** a channel can include only items carrying chosen labels and/or ban labels outright (ban wins), picked in the channel wizard from a live scan of your libraries' labels.
- **Radio Browser goes full:** 28 genre shelves — punk, pop-punk, country, hip-hop and rap lead, then rock, classic rock, alternative, metal, pop, 80s, reggae, blues, soul, funk, electronic, dance, latin, talk, comedy, sports, and the mood set.
- **First Windows bundle** — TavV Desktop ships as a ZIP alongside the APKs. (Its mouse issue on the added panels was fixed in 1262.)

### Build 1258 — The Radio panel · [notes](https://github.com/Tr33oflife/tavv-releases/releases/tag/v2.26.0-1258)

- **Radio panel (1257):** 46 SomaFM stations with remote tuning and held-OK presets (up to 8), 6 Jamendo mixes, and an optional Radio Browser band — off by default; while off it renders nothing and makes no requests.
- **The skin (1258):** the panel wears a 1930s cathedral radio — walnut cabinet, a working amber dial whose needle tracks the current stop on its band, preset push-buttons, knob transport.
- Fireplace radio grew by 4 stations (Illinois Street Lounge, Bossa Beyond, Left Coast 70s, Xmas in Frisko — 7 total).

### Build 1256 — House Party chip fix, first Windows source · [notes](https://github.com/Tr33oflife/tavv-releases/releases/tag/v2.26.0-1256)

- The House Party entry chip no longer renders over Nostalgia channels; it remains library playback's way in, and TV sessions use the guide panel's House Party row.
- Same source as the first Windows build (TavV identity + the video-rect fix for the Lofi/Fireplace small-square bug on Windows). Both ABIs ship.

### Build 1255 — Guest Pass · [notes](https://github.com/Tr33oflife/tavv-releases/releases/tag/v2.26.0-1255)

- **Guest Pass:** the listing-sync dialog gains an invite surface — the household's invite text, an "Accept an invite code" field, and provenance for invited households. "Forget this household" re-mints the key and revokes every pass.
- **Back-key fix:** Lofi & Chill and the Fireplace can now be left with a companion remote's Back button.
- **Up Next labels:** banners and the guide now read "Show · S# E# · Episode title" (movies stay plain title).

### Earlier builds

- **1249** — Lofi & Chill performance pass: bundled scenes re-encoded lighter (720p24) for 32-bit hardware.
- **1248** — Lofi & Chill black-background fix: the panel's music and rain move to a dedicated audio player so the scene player always paints.
- **1247** — Upstream Plezy 2.26.0 sync (Dolby Vision, subtitle and seek fixes); **everything free** — the Supporter pack removed; Smart Shuffle button in the library header; remote channel up/down keys zap channels in the player.
- **1246** — The cable pack: **sign-off hours**, **dead channels hidden**, **cheat phrases** (`ask the bartender`, `librarian`); Explore/Jump tabs off by default on fresh installs. Carries 1245: crash reporting stripped out entirely, and the episode-cooldown ledger syncs through the household relay.
- **1244** — **The episode cooldown:** no episode repeats on the same channel within 48 hours minimum, 7-day target, clocked on scheduled airtime.
- **1243** — Lofi background picker: 17 animated backgrounds (3 bundled, 14 downloadable); commentary tracks can no longer be auto-selected or carried onto the next episode.
- **1242** — Lofi scenes fix: the room artwork no longer covers the playing scene.
- **1241** — Fit check gains a high-accuracy AI mode; **listing sync sets itself up** (on by default, households self-join); the guide menu reopens where you left it; Lofi gains real looping video scenes.
- **1240 / 1239** — **The fit check** arrives: OMDb facts drop anime and genre misfits from channels; an optional AI tone pass joins it.
- **1238 – 1236** — A streaming-channels experiment (Pluto and friends) that came and went across three builds; the guide keeps the compact header it produced.
- **1235** — Channel rebuild: guide hardened so a broken channel renders as a named dead row instead of a black screen; schedule export as JSON; channel rule fixes.

---

## About this repo

This repo carries **release files only — no source code**. TavV is a fork of [Plezy](https://github.com/edde746/plezy); upstream's playback fixes flow in through syncs like build 1247's move to Plezy 2.26.0. Fireplace footage via Pixabay.
