# Uploading a TavV build to the release repo

The in-app updater on every TV reads **one place only**: the releases of
[github.com/Tr33oflife/tavv-releases](https://github.com/Tr33oflife/tavv-releases).
If a build is not published there, no TV will ever offer it. This guide is the
manual route (GitHub web page). APK Builder's Publish button does the same
thing automatically, with a read-back check.

## The three rules the updater enforces

1. **The APK filename is the update.** The updater parses the version code out
   of the asset name — it never looks inside the file. A wrong name means the
   update is invisible; a wrong code means the wrong offer. Names must be
   exactly:

   `TavV-<version>-<code>-<abi>.apk`

   | ABI | Code | Example filename |
   |---|---|---|
   | armeabi-v7a (32-bit) | build + 1000 | `TavV-2.25.0-1246-armeabi-v7a.apk` |
   | arm64-v8a (64-bit) | build + 2000 | `TavV-2.25.0-2246-arm64-v8a.apk` |

   ("Build" is the number after the `+` in the app version: 2.25.0+246 → build 246.)

2. **Each TV only sees its own ABI line.** A 32-bit TV scans the releases for
   the newest `armeabi-v7a` asset with a code higher than the one installed;
   a 64-bit TV does the same on the `arm64-v8a` line. The two lines never mix.
   A release may carry one ABI or both — a TV whose line is missing from the
   newest release simply falls back to the older releases. Codes must only
   ever climb: never reuse or lower a code.

3. **Same signing key, always.** In-place installs only work because every
   release is signed with the same keystore. An APK signed with anything else
   will download and then fail to install on every TV.

## Steps (GitHub web page)

1. Build the APK(s) as usual (APK Builder, one build per ABI).
2. Rename the output files to the exact pattern above, if they are not
   already named that way.
3. Go to the repo → **Releases** → **Draft a new release**.
4. **Choose a tag** → type a new one: `v<version>-<build>`
   (example: `v2.25.0-1246`) → "Create new tag on publish". Target can stay on
   the default branch.
5. **Release title:** `TavV <version> (<build>) — <one-line headline>`
   (example: `TavV 2.25.0 (1246) — Sign-off hours and hidden dead channels`).
6. **Description:** write what changed in plain language. This text is shown
   in the app's update prompt, so write it for the person holding the remote.
7. **Attach the APK files** in the "Attach binaries" area — both ABIs into
   the *same* release when you have both. If the second ABI is built later,
   open the published release → **Edit** → attach it then; the other line's
   TVs pick it up from there.
8. Click **Publish release**. Drafts are invisible to the updater — a build
   left in draft has not shipped.
9. **Verify:** reload the release page and check the asset names
   character-for-character and that the sizes match your local files. The TVs
   check on their own at startup (at most every ~6 hours), so the offer
   appears without anyone doing anything else.

## Do not

- Do not upload APKs to the plezy-fork repo's releases — nothing reads those.
- Do not rename an asset after uploading; delete it and upload again with the
  right name.
- Do not publish a build whose version codes are lower than the current
  release's — no TV will offer it, by design.
- Do not delete old releases to "tidy up" — they are the fallback each ABI
  line scans when the newest release doesn't carry its asset.
